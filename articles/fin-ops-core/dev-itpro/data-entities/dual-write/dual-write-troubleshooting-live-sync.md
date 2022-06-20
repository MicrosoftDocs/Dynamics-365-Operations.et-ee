---
title: Reaalajas sünkroonimise probleemide tõrkeotsing
description: See artikkel pakub tõrkeotsingu teavet, mis aitab teil reaalajas sünkroonimise probleemid lahendada.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9d27331b940a95168810c2f1ec4ae240a9df93a8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896701"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Reaalajas sünkroonimise probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]



See artikkel pakub tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning rakenduste vahel Microsoft Dataverse. Eelkõige annab see teavet, mis aitab lahendada reaalajas sünkroonimisega seotud probleeme.

> [!IMPORTANT]
> Mõned küsimused, mida see artikkel käsitleb, võivad nõuda kas süsteemiadministraatori rolli või Azure Active Directory (Azure AD) rentniku administraatori mandaate. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Reaalajas sünkroonimine näitab rea loomisel tõrget

Kui loote finantside ja toimingute rakenduses rea, võite saada järgmise tõrketeate:

*\[{\\„tõrge\\”:{\\„kood\\”:\\„0x80072560\\”,\\„sõnum\\”:\\„Kasutaja pole organisatsiooni liige.\\”}}\], Kaugserver tagastas tõrke: (403) keelatud.”}}”.*

Probleemi lahendamiseks järgige juhiseid teemas [Süsteemi nõuded ja eeltingimused](requirements-and-prerequisites.md). Nende sammude lõpule viimiseks peab rakenduses Dataverse loodud topeltkirjutuse kasutajatel olema süsteemiadministraatori roll. Vaikeomanikust meeskonnal peab samuti olema süsteemiadministraatori roll.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Reaalajas sünkroonimine näitab tabeliandmete salvestamisel tõrget

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui proovite tabeliandmeid finantside ja toimingute rakendusse salvestada, võite saada järgmise tõrketeate:

*Andmebaasi muudatusi ei saa salvestada. Tööüksus ei saa kannet kinnitada. Üksuse uoms-i ei saa andmeid kirjutada. Üksusesse UnitOfMeasureEntity kirjutamine nurjus, kuna tõrketeade ei saa sünkroonida üksuse uoms-i.*

Probleemi lahendamiseks veenduge, et eeltingimuse viiteandmed on olemas nii rakenduses Finantsid ja Toimingud kui ka Dataverse. Näiteks kui kliendikirje kuulub kindlasse kliendigruppi, veenduge, et see kliendigrupp on Dataverse'is olemas.

Kui andmed on olemas mõlemas kohas ja olete teinud kindlaks, et probleem ei ole seotud andmetega, toimige järgmiselt.

1. Üksuse **DualWriteProjectConfigurationEntity** avamine Exceli lisandmooduliga. Lisandmooduli kasutamiseks lubage **kujundusrežiim Finantside ja toimingute Exceli lisandmoodulis ja lisage töölehele DualWriteProjectConfigurationEntity**. Lisateavet vaata [üksuse andmete kuvamiseks ja värskendamiseks Exceli`ga](../../office-integration/use-excel-add-in.md).
2. Valige ja kustutage kirjed, mis väljastab topeltkirjutuse kaardi ja projekti probleemid. Iga topeltkirjutuse vastendamise kohta on kaks kirjet.
3. Avaldage muudatused Exceli lisandmooduli abil. See samm on oluline, kuna see kustutab kirjed üksusest ja aluseks olevatest tabelitest.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Finantside ja toimingute rakenduses andmete loomisel lugege või kirjutage privileegitõrkeid.

Võite saada tõrketeate "Bad Request" (Vigane taotlus), kui loote andmeid rakenduses Finantsid ja toimingud.

![Vigase taotluse tõrketeate näide.](media/error_record_id_source.png)

Probleemi lahendamiseks peate määrama vastendatud Dynamics 365 Sales`i või Dynamics 365 Customer Service'i äriüksusele õige turberolli puuduva privileegi lubamiseks.

1. Rakendusest Finantsid ja toimingud leidke andmeintegratsiooni ühenduse komplektis vastendatud äriüksus.

    ![Organisatsiooni vastendamine.](media/mapped_business_unit.png)

2. Logige customer engagement rakenduse keskkonda sisse, liikuge jaotisesse **Sätted \> Turve** ja otsige üles vastendatud äriüksuse meeskond.

    ![Vastendatud äriüksuse meeskond.](media/setting_security_page.png)

3. Avage redigeerimiseks meeskonna lehekülg ja valige suvand **Halda rolle**.

    ![Rollide haldamise nupp.](media/manage_team_roles.png)

4. Määrake dialoogiboksis **Töörühmarollide haldamine** roll, mis omab vastavate tabelite lugemis-/kirjutusõigusi, ja seejärel valige **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Sünkroonimisprobleemide parandamine keskkonnas, millel on hiljuti muudetud Dataverse'i keskkond

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui loote finantside ja toimingute rakenduses andmeid, võite saada järgmise tõrketeate:

*{„entityName”:„CustCustomerV3Entity”,„executionStatus”:2,„fieldResponses”:\[\],„recordResponses”:\[{„errorMessage”:„**Lasti ei saanud luua üksusele CustCustomerV3Entity**”,„logDateTime”:„2019-08-27T18:51:52.5843124Z”,„verboseError”:„Lasti loomine nurjus tõrkega kehtetu URI: URI on tühi.”}\],„isErrorCountUpdated”:true}*

Kliendikaasamise rakenduse tõrge näeb välja selline:

> ISV koodist ilmnes ootamatu tõrge. (TõrkeTüüp = KliendiTõrge) Ootamatu erand lisandmoodulist (Käivita): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: üksuse konto töötlemine nurjus – (ühenduse loomise katse nurjus, kuna ühendatud osapool ei reageerinud pärast teatavat ajavahemikku või loodud ühendus nurjus, kuna ühendatud host ei vastanud.

See tõrge ilmneb, kui Dataverse keskkond on valesti lähtestatud, kui proovite luua andmeid rakenduses Finantsid ja toimingud.

> [!IMPORTANT]
> Kui olete keskkonnad uuesti linkinud, peate kõik üksuse vastendused peatama, enne kui jätkate vähendamise samme.

Probleemi lahendamiseks peate läbima etapid nii finantside Dataverse kui ka toimingute rakenduses.

1. Finantside ja toimingute rakenduses järgige neid samme.

    1. Üksuse **DualWriteProjectConfigurationEntity** avamine Exceli lisandmooduliga. Lisandmooduli kasutamiseks lubage **kujundusrežiim Finantside ja toimingute Exceli lisandmoodulis ja lisage töölehele DualWriteProjectConfigurationEntity**. Lisateavet vaata [üksuse andmete kuvamiseks ja värskendamiseks Exceli`ga](../../office-integration/use-excel-add-in.md).
    2. Valige ja kustutage kirjed, mis väljastab topeltkirjutuse kaardi ja projekti probleemid. Iga topeltkirjutuse vastendamise kohta on kaks kirjet.
    3. Avaldage muudatused Exceli lisandmooduli abil. See samm on oluline, kuna see kustutab kirjed üksusest ja aluseks olevatest tabelitest.
    4. Tõrgete vältimiseks finantside ja toimingute või keskkondade Dataverse uuesti linkimisel veenduge, et topeltkirjutuse konfiguratsioone ei jääks.

2. Rakenduses Dataverse tehke järgmist:

    1. Logige oma keskkonda Dataverse sisse (näiteks, `https://*****.crm.dynamics.com/`).
    2. Minge **Täpsemate sätete** \> **Täpsemasse otsingusse**.
    3. Valige **DualWrite'i käitusaja konfiguratsioon**.
    4. Valige vaadatav veerg.
    5. Konfiguratsioonide vaatamiseks valige **tulemused**.
    6. Kustutage kõik eksemplarid.

3. Finantside ja toimingute rakenduses järgige neid samme.

    1. Üksuse **DualWriteProjectConfigurationEntity** avamine Exceli lisandmooduliga. Lisandmooduli kasutamiseks lubage **kujundusrežiim Finantside ja toimingute Exceli lisandmoodulis ja lisage töölehele DualWriteProjectConfigurationEntity**. Lisateavet vaata [üksuse andmete kuvamiseks ja värskendamiseks Exceli`ga](../../office-integration/use-excel-add-in.md).
    2. Valige ja kustutage kirjed, mis väljastab topeltkirjutuse kaardi ja projekti probleemid. Iga topeltkirjutuse vastendamise kohta on kaks kirjet.
    3. Avaldage muudatused Exceli lisandmooduli abil. See samm on oluline, kuna see kustutab kirjed üksusest ja aluseks olevatest tabelitest.
    4. Tõrgete vältimiseks finantside ja toimingute või keskkondade Dataverse uuesti linkimisel veenduge, et topeltkirjutuse konfiguratsioone ei jääks.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Reaalajas sünkroonimistõrge pärast andmebaasi täieliku koopia kopeerimist

Võite saada järgmise tõrketeate pärast andmebaasi täieliku koopia käivitamist ühest süsteemist teise ja seejärel proovida andmebaasitoimingut käitada:

*SecureConfig Organization (???) ei vasta tegelikule CRM-organisatsioonile (???).*

Tõrketeade kuvatakse topeltkirjutuse käitusaja lisandmoodulist, et tagada ühes süsteemis seadistatud topeltkirjutuse konfiguratsiooni ei saa teises süsteemis kasutada.

Probleemi lahendamiseks kustutage kõik tabeli **msdyn_dualwriteruntimeconfig** kirjed peale andmebaasi taastamist. Lisateabe saamiseks vt [linkimise lõpetamine ja uuesti linkimine topeltkirjutuskeskkonnaga](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Reaalajas sünkroonimisprobleemid, mille põhjuseks on topeltkirjutuse kaartide vale päringufiltri süntaks

Kuigi topeltkirjutuse kaardi filtri päringuavaldis on süntaktiliselt õige, ei pruugi see ootuspäraselt töötada. Filtriavaldis asub üksusel, mitte päringuobjekti üksikul andmeallikal. Seetõttu ei tagasta loodav SQL-päring oodatud tulemusi.

Siin on näide.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Võite oodata projekte, mille ema pole välja filtreeritud. Ent filter ei tööta, sest see on tõlgitud päringusse, mis sarnaneb järgmise näitega.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Tegelik tulemus on, et `parentProject` välja väärtuseks on seatud `null`. Kuid `null` pole sama, mis tühi string. Selle lahknevuse tõttu ei tagasta päringufilter kehtivaid tulemusi.

Probleemi lahendamiseks tehke järgmist.

1. Lisage arvutatud veerg, mida saab lisada laiendusmudelisse ja mida varundatakse loogikaga, mis teisendab `null` tühja stringi.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Kasutage vaikeveeru asemel filtrit uuel arvutatud veerul.

Filtri hindamiseks arenduskeskkonnas saate kasutada järgmisi X++ koode tulemuste kinnitamiseks. Käivitage see kood eraldi programmina. Saate seda kasutada, et hinnata erinevaid filtreid, mida üksusele kohaldada enne, kui kasutate neid filtreid topeltkirjutuse kaartidel. Lahknevuste hindamiseks saab päringu käivitada andmebaasi vastu.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Finantside ja toimingute rakenduste andmed pole sünkroonitud rakendusega Dataverse

Reaalajas sünkroonimise ajal võib tekkida probleem, kus ainult osa andmeid sünkroonitakse Finantside ja toimingute Dataverse rakendustest või ei sünkroonita andmeid üldse.

> [!NOTE]
> Peate selle probleemi arenduse ajal parandama.

Enne probleemi lahendamist vaadake üle järgmised eeltingimused:

+ Kontrollige, et kohandatud muudatused kirjutatakse ühte kandeulatusse.
+ Ärisündmused ja topeltkirjutuse raamistikku ei käsitleta `doinsert()`, `doUpdate()` ja `recordset()` operatsioone või kirjeid, kus `skipBusinessEvents(true)` on märgitud. Kui teie kood on nende funktsioonide sees, ei käivitata topeltkirjutust.
+ Ärisündmused peavad olema registreeritud vastendatud andmeallikale. Mõned andmeallikad võivad kasutada välist liitmist ja võivad olla märgitud kirjutuskaitstuks finantside ja toimingute rakendustes. Neid andmeallikaid ei jälgita.
+ Muudatused käivitatakse ainult siis, kui muudatused on vastendatud väljadel. Vastendamata väljamuudatused ei käivita topeltkirjutust.
+ Veenduge, et filtri hinnangud annavad kehtiva tulemuse.

### <a name="troubleshooting-steps"></a>Tõrkeotsingu sammud

1. Vaadake välja vastendamised üle topeltkirjutuse halduslehel. Kui väli pole finantside ja toimingute rakendustes vastendatud Dataverse, siis seda ei jälgita. Näiteks järgmise näite korral jälgitakse välja **Kirjeldus** Dataverse väärtuse alusel, kuid mitte rakenduste Finantsid ja Toimingud abil. Finantside ja toimingute rakendustes ei jälgita sellele väljale muudatusi.

    ![Jälgitud väli.](media/live-sync-troubleshooting-1.png)

2. Määrake, kas ärisündmuste definitsioonis jälgitakse andmeallikat. Näiteks järgmisel joonisel ei jälgita muudatuste puhul ühtegi tabelit **DefaultDimensionDAV** ja selle aluseks olevaid tabeleid. Andmeallikaid, mis kasutavad välist liitmist ja mis on märgitud kirjutuskaitstuks, ei jälgita.

    ![Väljad, mida ei jälgita.](media/live-sync-troubleshooting-2.png)

3. Määratlege, kas vastendatud tabeli väljad kuvatakse **ÄRISÜNDMUSDEFINITSIOON** tabelis nagu näha järgmises illustratsioonis. Kui te ei leia välja, mida päringu tulemusest otsite, ei käivita seda topeltkirjutus.

    ![Tabeli jälitatud väli.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Näidisstsenaarium

Finantside ja toimingute rakendustes värskendatakse kontaktikirje aadressi, kuid aadressi muudatust ei sünkroonitud Dataverse. See olukord ilmneb, kuna tabelil **BusinessEventsDefinition** ükski kirje ei sisalda mõjutatud tabeli ja üksuse kombinatsiooni. Täpsemalt pole **LogisticsPostalAddress** tabel otseseks andmeallikaks üksusel **smmKontaktpersoonCDSV2Üksus**. Üksuse **smmKontaktpersoonCDSV2Üksus** on **smmKontaktPersoonV2Üksus** andmeallikaks ja **smmKontaktPersoonV2Üksus** on omakorda **LogistikaPostilAadressBaasÜksus** kui andmeallikaks. Tabel **LogisticsPostalAddress** on **LogisticsPostalAddressBaseEntity** andmeallikas.

Sarnane olukord võib tekkida mõnedes ebastandardses mustrites, nt juhtumites, kus finantside ja toimingute rakendustes muudetavad tabelid ei ole selle üksusega seotud. Näiteks arvutatakse üksuse **smmKontaktPersoonCDSV2Üksus** esmase aadressi andmed. Topeltkirjutuse raamistik püüab määrata, kuidas aluseks oleva tabeli muudatus vastendatakse tagasi üksustele. Tavaliselt piisab sellest lähenemisest. Kuid mõnel juhul on link nii keerukas, et peate olema kindel. Veenduge, et **RecId** seotud tabel on üksuses otse saadaval. Seejärel lisage staatiline meetod tabeli muutuste jälgimiseks.

Näiteks vaadake üle **smmKontaktPersoonCDSV2Üksus::getEntityDataSourceToFieldMapping()** meetod. **CustCustomerV3üksus** ja **VendVendorV2Üksus** on muudetud selle olukorra lahendamiseks.

Probleemi lahendamiseks tehke järgmist.

1. Lisage väli **EsmanePostiAadressRecId** üksusele **smmKontaktPersoonV2Üksus**. Muutke see sisemiseks.

    ![Üksusele smmContactPersonV2Entity on lisatud väli.](media/Troubleshoot_live_sync_issue_1.png)

2. Lisage sama väli **smmContactPersonV2Entity** üksusele.

    ![Üksusele smmContactPersonCDSV2Entity on lisatud väli.](media/Troubleshoot_live_sync_issue_2.png)

3. Lisage järgmine meetod **smmKontaktPersoonCDSV2Üksus** klassile.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Sünkroonige andmebaas ja koostage rakendus.
5. Peatage kõik topeltkirjutuse kaardid, mis luuakse **smmKontaktPersoonCDSV2Üksus** üksuses.
6. Kaardi käivitamine. Peaksite nägema uut tabelit (**logisticsPostalAddress** selles näites) mida olete hakanud jälgima, kasutades tabeli **RefTabelNimi** veerus reale kus **refentitynimi** väärtus võrdub **smmKontaktPersoonCDSV2Üksus** **BusinessEventsDefinition** tabelis.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Tõrge kirje loomisel, kus finantside ja toimingute rakendusest samasse partiisse saadetakse Dataverse mitu kirjet

Iga kande puhul loob rakendus Finance and Operations andmed partiina ja saadab need pakett-tööna.Dataverse Kui kaks kirjet luuakse ühe ja sama kande osana ja need teineteisele viitavad, võite saada tõrketeate, mis sarnaneb järgmise näitega rakenduses Finantsid ja toimingud:

*Ei saa kirjutada andmeid üksusesse aaa_fundingsources. Ei saa otsida ebecsfs_contracts koos väärtustega {PC00...}. Ei saa otsida aaa_fundingsources väärtustega {PC00...}. Kirjutab aaa_fundingsources nurjumisega tõrketeatega Eranditeade: kaugserver tagastas tõrke: (400) vale taotlus.*

Probleemi lahendamiseks looge finants- ja toimingute rakenduses üksuseseosed, mis näitavad, et kaks üksust on üksteisega seotud ja seotud kirjeid käsitletakse samas kandes.

## <a name="enable-verbose-logging-of-error-messages"></a>Luba tõrketeadete paljusõnaline logimine

Finantside ja toimingute rakenduses võib ilmneda tõrkeid, mis on seotud keskkonnaga Dataverse. Veateade ei pruugi sisaldada sõnumi täisteksti või muid asjakohaseid andmeid. Lisateabe saamiseks saate lubada paljusõnalise **logimise, häälestades IsDebugMode** lipu, mis on **olemas üksuses DualWriteProjectConfigurationEntity** kõigis finantside ja toimingute rakenduste projektikonfiguratsioonides.

1. Üksuse **DualWriteProjectConfigurationEntity** avamine Exceli lisandmooduliga. Lisandmooduli kasutamiseks lubage **kujundusrežiim Finantside ja toimingute Exceli lisandmoodulis ja lisage töölehele DualWriteProjectConfigurationEntity**. Lisateavet vaata [üksuse andmete kuvamiseks ja värskendamiseks Exceli`ga](../../office-integration/use-excel-add-in.md).
2. Seadke projektis **IsDebugMode** lipu väärtuseks **Jah**.
3. Käivitage stsenaarium.
4. Verbose logid on saadaval tabelis **DualWriteErrorLog**. Andmete otsimiseks tabelibrause abil kasutage järgmist URL-i: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Silumisrežiimis rohkem logide hõivamiseks installige värskendus [KB 4595434 (Paranda tühjade väärtuste puhul topeltkirjutuse otse sünkroonimisel)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Tõrge kliendi aadressi või kontakti lisamisel

Kui proovite kliendi aadressi lisada või finantside ja toimingute rakendustes ühendust võtta, võite saada järgmise tõrketeate Dataverse:

*Andmeid ei saa kirjutada üksusesse msdyn_partypostaladdresses. Kirjutamine DirPartyPostalAddressLocationCDSEntity nurjus tõrketeate taotlusega, mille olekukood on BadRequest ja CDS-i tõrkekood: 0x80040265 vastussõnum: tõrge ilmnes pluginas. Kirje, mille atribuudiväärtused on Asukoha ID-kood, on juba olemas. Üksusevõtme asukoha ID-võti nõuab, et see atribuudikomplekt sisaldaks kordumatuid väärtusi. Valige kordumatud väärtused ja proovige uuesti.*

Probleemi lahendamiseks installige topeltkirjutusega orkestratsioonipaketi versioon (2.2.2.60), et võti **Aadress** tabelis oleks määratletud nagu järgmises tabelis.

| Atribuut | Väärtus |
|---|---|
| Kuvatav nimi | **Asukohavõti** |
| Nimi | **msdyn_locationkey** |
| Väljad | **msdyn_locationid**, **emaid** |
| Olek | **Aktiivne** |
| Süsteemi töö | Tühi |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Tõrge kliendi lisamisel rakendusse Dataverse

Kui proovite salvestada klienti rakendusse Dataverse, võidakse kuvada järgmine tõrketeade:

*RecordError0": Üksuse Klientide V3 kirjutamine nurjus teadmata erandiga – osapoole tüüpi Organisatsiooni puhul ei leitud osapoolekirjet'"}.*

Kui klient on rakenduses Dataverse loodud, luuakse uus osapoole number. Tõrketeade kuvatakse siis, kui kliendikirje koos osapoolega sünkroonitakse finantside ja toimingute rakendustega, kuid kliendikirjel on juba teine osapoolenumber.

Probleemi lahendamiseks leidke klient osapooleotsingu kaudu. Kui klienti veel pole, looge uus kliendi kirje. Kui klient on olemas, kasutage olemasolevat osapoolt uue kliendikirje loomiseks.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Tõrge uue kliendi, hankija või kontakti loomisel aknas Dataverse

Võite saada järgmise tõrketeate, kui proovite lisada uut klienti, hankijat või kontakti rakenduses Dataverse:

*Osapoole tüüpi ei saa värskendada 'DirOrganization' üksusest üksuseks 'DirPerson', selle asemel tuleb kustutada olemasolev osapool, millele järgneb uue tüübiga sisestamine.*

Rakenduses Dataverse on numbrijada **msdyn_party** tabelis. Kui konto on loodud rakenduses Dataverse, luuakse uus osapool (nt **Osapool-001** tüübist **Organisatsioon**). Need andmed saadetakse rakendusesse Finantsid ja Toimingud. Kui keskkond Dataverse lähtestatakse või Dataverse Dataverse finantside ja toimingute keskkond on lingitud muu keskkonnaga ja seejärel luuakse uus kontaktikirje, luuakse uus osapoole väärtus, **mille alguses on Party-001**. Praegu luuakse osapoole kirjeks **Osapool-001** tüübiga **Isik**. Kui need andmed on sünkroonitud, näitavad finantside ja toimingute rakendused eelnevat tõrketeadet, sest organisatsiooni **tüüpi osapoolekirje Party-001** **on** juba olemas.

Probleemi parandamiseks muutke automaatne numbrijada välja **msdyn_partynumber** jaoks **msdyn_party** tabelis Dataverse erinevaks automaatseks numbriseeriaks.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Kliendi või kontakti vastendamise jõudluse probleem

Teil võib olla võimalik marginaaliliselt parandada klientide ja kontaktide reaalajas sünkroonimise jõudlust, kohandades **getEntityDataSourceToFieldMapping** meetodit (üksuses **CustCustomerV3Entity** ja **getEntityDataSourceToFieldMapping** meetodit üksuses **smmKontaktPersoonCDSV2Üksus**). Need kohandused vähendavad tabeli **BusinessEventsDefinition** kirjete arvu. See kirjete arvu vähendamine vähendab omakorda tõstatud sündmuste arvu.

Meetod **getEntityDataSourceToFieldMapping** üksuses **CustCustomerV3Entity** tagab, et kliendi elektroonilise aadressi või postiaadressi uuendamine käivitab ärisündmused, nii et uuendatud andmed saadetakse Dataverse`i. Kui te ei kasuta kõiki välju ja ei vaja topeltkirjutuses teavet, sisestage meetodis välja sobivad read. Iga selles meetodis lisatud jälgitud väli ja tabel lisab **BusinessEventsDefinition** tabelile kirje jälgitud tabeli ja jälgitud üksuse kombinatsiooni kohta.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Samal moel **getEntityDataSourceToFieldMapping** meetod **smmKontaktPersoonCDSV2Üksus** üksus tagab, et kliendi elektroonilise aadressi või postiaadressi uuendamine käivitab ärisündmused, nii et uuendatud andmed saadetakse Dataverse`i. Selle meetodi puhul saate sisestada kommentaare iga välja kohta, mida te ei kasuta.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Järgige pärast meetodite uuendamist neid samme.

1. Sünkroonige andmebaas ja koostage rakendus.
2. Peatage kõik topeltkirjutuse kaardid, mis luuakse **smmKontaktPersoonCDSV2Üksus** ja **TavKlientV3Üksus** üksuses.
3. Kaartide käivitamine. Peaksite nägema vähem kirjeid **smmContactPersonCDSV2Entity** ja **CustCustomerV3Entity** üksustes ja **BusinessEventsDefinitioni** tabelis ning jõudlus võib marginaalselt paraneda.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
