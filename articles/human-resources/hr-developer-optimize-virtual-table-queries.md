---
title: Dataverse'i virtuaalsete tabelite päringute optimeerimine
description: Dataverse virtuaalsete tabelipäringute jõudluse optimeerimine ja tõrkeotsing
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4057740fc4c6ddd696b37b6373dcfcd43881305e
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534213"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Dataverse'i virtuaalsete tabelite päringute optimeerimine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Väljasta

### <a name="overview"></a>Ülevaade

Dataverse virtuaalsete tabelite kasutamisel integratsioonide ja muude andmeühenduste arendamiseks Dynamics 365 Human Resources rakendusega saate kogeda jõudlusprobleeme virtuaalsete tabelitega seotud päringutega. Aeglane päringu täitmine võib toimuda erinevate klientide või liideste vahel. Näiteks võib ilmneda probleem järgmistel juhtudel.

- Virtuaalse tabeli päringu esitamisel Dataverse Web API kaudu
- Power Api loomine virtuaalse tabeli vastu
- Power BI aruande koostamisel virtuaalsele tabelile

Kõik need liidesed võivad jõudlusprobleemi esile tuua.

Personaliosakonna Dataverse virtuaaltabelite aeglase jõudluse üheks põhjuseks on tabeli [navigeerimisatribuutidega](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) seotud virtuaalse tabeli võõrvõtme veerud. Kui virtuaalse tabeli jaoks luuakse navigeerimisatribuudid, lisatakse tabelisse võõrvõtme veerg, mis tähistab seotud virtuaalse tabeli võtmeveeru võtme väärtust. Näiteks lisatakse veerg **_mshr_fk_person_id_value** olemile **mshr_hcmworkerbaseentity**, mille **mshr_dirpersonentity** olemi välisvõtme atribuut. Kuna nende võõrvõtmete veergude väärtusi säilitatakse tabelis, võib väärtuste toomine avaldada negatiivset mõju virtuaalse tabeli päringu jõudlusele.

### <a name="potential-symptoms"></a>Võimalikud sümptomid

Näide, kus seda mõju võite näha, on päringutes olemi Töötaja ( **mshr_hcmworkerentity**) või Baastöötaja (**mshr_hcmworkerbaseentity**) vastu. Jõudluse probleem võib ilmneda mitmel erineval viisil:

- **Aeglane päringu tegevus**: virtuaaltabeli vastane päring võib tagastada oodatud tulemused, kuid päringu täitmise lõpuleviimiseks kulub oodatust kauem aega.
- **Päringu ajalõpp**: päring võib ajalõppu ja tagastada järgmise tõrke: "Luba saadi finantside ja toimingute kutsumiseks, kuid finantsid ja toimingud tagastasid tõrke tüübiga InternalServerError."
- **Ootamatu tõrge**: päring võib tagastada tõrketüübi 400 järgmise teatega: "Ilmnes ootamatu tõrge."

  ![Vea tüüp 400 HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Ahendamine**: päring võib serveri ressursse üle kasutada ja muutuda ahendamiseks. Sel juhul tagastab päring järgmise tõrke: "Finantside ja toimingute kutsumiseks saadi luba, kuid finantsid ja toimingud tagastasid vea tüübiga 429." Lisateavet personaliosakonna ahendamise kohta leiate teemast [Ahendamise KKK](./hr-admin-integration-throttling-faq.md).

  ![Vea tüüp 429 HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Lahendus

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Andmepäringusse kaasatud veergude arvu piiramine

Virtuaalsete tabelite puhul on üks meetoditest, millel on kõige suurem potentsiaal päringu jõudluse parandamiseks, päringus valitud veergude arvu piiramine. Päringu toimivuse optimeerimise üldjuhend on piirata päringus tagastatud veerge ainult nende omadustega, mida vajate. See kehtib eriti virtuaalsete tabelite võõrvõtmete veergude kohta. Kui te ei vaja integratsiooniks või aruandeks võõrvõtmete veergude väärtusi, siis struktureerige päring, et valida ainult need veerud, mida vajate (v.a võõrvõtme veerud).

#### <a name="selecting-columns-in-an-odata-query"></a>Veergude valimine OData päringus

Dataverse Web API kaudu virtuaalsest tabelist päringu tegemisel saate piirata päringusse kaasatud veergude arvu, kasutades **$select** süsteemipäringut ja määratleda veerud, mille kohta vajate tulemite tagastamist. Jõudluse maksimeerimiseks jätke päringust välja võõrvõtme veerud (need, millel on **_mshr_FK_** eesliide).

Näiteks järgmine päring **mshr_hcmworkerbaseentity** olemi vastu sisaldab ainult **$select** päringu suvandiklauslis sisalduvaid veerge, v.a võõrvõtme väärtused. See pakub olulisi täiustusi jõudluses päringu üle, mis sisaldab kõiki tabeliveerge.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Soovitus piirata valitud veergude arvu kehtib ka siis, kui kasutate **$expand** päringu suvandit päringu laiendamiseks seotud virtuaalsetele tabelitele navigeerimisatribuutide kaudu. Näiteks järgmine päring sisaldab olemit **mshr_hcmworkerbaseentity** koos laiendatud veergudega olemist **mshr_dirpersonentity**. Pange tähele, **$select** päringu suvand on kaasatud ka päringu **$expand** suvandi klauslisse.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Kasutades seda meetodit andmete toomiseks päringu **$select** valikuga päringu **$expand** valikus, näete tavaliselt suuremat jõudluse parendust, kui navigeerimisaviis üksuste vahel on mitu-ühele suhe. Te ei pruugi näha sama kahanemist päringu täitmisajas ühe-mitmele suhte laiendamisel. Lisateavet Dataverse virtuaaltabelite seose definitsiooni kohta vt [Tabeliseosed](/powerapps/maker/data-platform/create-edit-entity-relationships).

Lisateavet Dataverse Web API **$select** ja **$expand** kasutamise kohta vt teemast [Seotud üksusekirjete hankimine päringuga](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Veergude valimine rakenduses Power BI

Kui teil tekib Power BI aruande Dataverse virtuaalse tabeli suhtes aruande ülesehitamisel mis tahes peatse jõudlusel, saate parandada jõudlust, välistades võõrvõtme veerud aruande tabelist valitud veergudest. Näiteks kui kasutate aruande loomiseks olemi **mshr_hcmworkerbaseentity** vastu rakendust Power BI Desktop, saate kasutada järgmisi samme aruande päringusse kaasamiseks veergude valimiseks.

1. Power BI Desktop rakenduses valige toiminguribaripploendis **Too andmed** valige väärtus **Veel...**.
2. Sisestage aknas **Hangi andmed** otsinguboksi **Common Data Service**, valige ühendus **Common Data Service** ja valige käsk **Ühenda**.
3. Akna Common Data Service väljas **Serveri URL** sisestage oma Dataverse keskkonna organisatsiooni URI ja valige **OK**.
  
   ![Sisestage Dataverse'i keskkonda URI.](./media/PowerBIDataverseURLSetup.png)
  
4. Laiendage aknas Navigator sõlm **Olemid**.
5. Otsinguboksis sisestage **mshr_hcmworkerbaseentity** ja valige olem.
6. Valige **Andmete transformeermine**.
7. Power Query Valige redaktori aknas täpsem **redaktor**.
8. Aknas **Täpsem redaktor** uuendage päringut nii, et see otsiks välja järgmisena, lisades või eemaldades kõik vajalikud veerud massiivile.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Saate päringut uuendada redaktori täpsemas redaktoris Power Query.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Valige suvand **Valmis**.

   > [!NOTE]
   > Kui olete enne päringu värskendamist päringult saanud tõrke tüübist 429, peate võib-olla enne päringu värskendamist ootama uuesti prooviperioodi, et see saaks täielikult lõpule viia.

10. Klõpsake **nuppu Sule ja rakenda** redaktori Power Query tegevusribal.

Siis saate alustada Power BI aruande ülesehimist virtuaaltabelist valitud veergude suhtes.

#### <a name="selecting-columns-in-power-apps"></a>Veergude valimine rakenduses Power Apps

Sarnaselt Dataverse Web API ja Power BI päringutega saate parandada Power Apps Dataverse virtuaaltabelitel põhineva päringu jõudlust, jättes rakendusest välja seotud tabelite veerud. Kui lehele on lisatud seotud tabeli veerge, sisaldab andmete toomiseks loodud päringu URL ka seotud tabeli võõrvõti atribuute. See, nagu ülaltoodud [OData päringu veergude valimise](#selecting-columns-in-power-apps) näites, vähendab jõudlust täiendavate andmeotsingute tõttu.

Selle probleemi lahendamiseks saate kinnitada, et ükski seotud tabelite andmeväli ei ole teie Power App'i andmevormile kaasatud.

1. Valige puuvaate paanil ekraanile andmevorm.
2. Valige paanil **Atribuudid** suvand **Redigeeri** atribuudis **Väljad**.
3. Kontrollige **andme** paanil, et ükski valitud väli ei ole andmeallika virtuaaltabeli väljaks.

Näiteks kui üks rakenduse lehel kaasatud andmeväljadest viitab teisele tabelile, nt **ThisItem.Worker.Name**, kus **töötaja** on seotud tabel, võib andmete toomisel jõudlust vähendada.

Saate kasutada [Power Apps Monitori](/powerapps/maker/monitor-overview), et Power App'i andmete toomiseks kaasaks päringusse ainult vajalikud veerud. Toimingu getRows jaoks loodud URL-i saate vaadata, kindlustamaks, et teie rakendusele valitud veerud on andmete toomisel optimaalsed.

![Kasutage Power Apps Monitor funktsiooni getData toimingu analüüsimiseks.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Andmepäringu filtreerimine

Teine meetod päringu täitmise jõudluse parandamiseks on päringutulemites tagastatud kirjete arvu piiramine. Seda saate teha tulemuste filtreerimisega, et tagada ainult vajalike kirjete saamine.

Lisateavet päringuandmete filtreerimise kohta vt [filtreerimistulemustest](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).

### <a name="limiting-the-page-size-of-the-query"></a>Päringu lehekülje suuruse piiramine

Suurte andmekomplektiga töötamisel saate päringutulemused jagada mitmeks leheks, lisades andmepäringutele `odata.maxpagesize` eelispäise.

Lisateavet saalimise kohta vt[Määrake lehel tagastamiseks üksuste arv](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Vt ka

- [Dataverse'i virtuaalsete tabelite konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md)
- [Human Resourcesi virtuaalsete tabelite KKK](hr-admin-virtual-entity-faq.md)
- [Ahendamise KKK](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
