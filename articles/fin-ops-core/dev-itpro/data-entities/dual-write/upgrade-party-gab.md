---
title: Üleminek osapoole ja globaalse aadressiraamatu mudelile
description: See teema kirjeldab, kuidas uuendada kahekirjutajalisi andmeid osalise ja globaalse aadressiraamatu mudelile.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 7434c2ed486fe0546a746afdd2c4c4aacdcc3d5c
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817284"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Üleminek osapoole ja globaalse aadressiraamatu mudelile

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Data Factory mallid aitavad teil täiendada järgmisi olemasolevaid andmeid topeltkirjutuses osapoolele ja globaalse aadressiraamatu mudelile: andmed kontos, kontaktide ja hankija tabelites ning posti- ja [Microsoft Azure](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)**·** **·** **·** elektroonilised aadressid.

Antud on järgmised kolm Data Factory malle. Need aitavad viia vastavusse nii rakenduste kui ka Finance and Operations kliendi kaasamise rakenduste andmed.

- **[Osapoole mall (täiendage andmeid topeltkirjutusega](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) osapoole-GAB skeemiks/arm_template.json) – see mall aitab täiendada osapoole- ja kontaktiandmeid, mis on seotud konto, kontakti ja** **hankija** **·** **·** **·** **·** andmetega.
- **[Osapoole postiaadressi mall (täiendage andmeid topeltkirjutusega osapoole-GAB skeemiks/täiendage osapoole postiaadressiks](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) - GAB/arm_template.json) – see mall aitab täiendada postiaadresse, mis on seostatud konto, kontakti ja hankija** **·** **·** **·** andmetega.
- **[Osapoole elektroonilise aadressi mall (täiendusandmed topeltkirjutusega osapoole-GAB skeemiks/osapoole elektrooniliseks aadressiks](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) – GAB/arm_template.json) – see mall aitab täiendada elektroonilisi aadresse, mis on seostatud konto, kontakti ja hankija** **·** **·** **·** andmetega.

Protsessi lõpus luuakse järgmised komaga eraldatud failid (.csv).

| Failinimi | Eesmärk |
|---|---|
| FONewParty.csv | See fail aitab rakenduses **luua** uusi Finance and Operations osapoolekirjeid. |
| ImpordiFONewPostalAddressLocation.csv | See fail aitab rakenduses **luua uusi** postiaadressi asukoha Finance and Operations kirjeid. |
| ImpordiFONewPartyPostalAddress.csv | See fail aitab rakenduses **luua uusi osapoole** postiaadressi Finance and Operations kirjeid. |
| ImpordiFONewPostalAddress.csv | See fail aitab rakenduses **luua** uusi postiaadressi Finance and Operations kirjeid. |
| ImpordiFONewElectronicAddress.csv | See fail aitab rakenduses **luua uusi elektroonilise aadressi** Finance and Operations kirjeid. |

See teema kirjeldab, kuidas kasutada data factory malle ja uuendada andmeid. Kui te ühtegi kohandust ei tee, saate malle kasutada nii, nagu need on. Kuid kui teil on konto, kontakti ja hankija andmete **·** **·** **·** kohandusi, peate malle muutma selles teemas kirjeldatud viisil.

> [!IMPORTANT]
> Osapoole postiaadressi ja osapoole elektroonilise aadressi mallide käivitamiseks on erijuhised. Esmalt peate käivitama osapoole malli, seejärel osapoole postiaadressi malli ja seejärel osapoole elektroonilise aadressi malli.

## <a name="prerequisites"></a>Eeltingimused

Enne osapoole ja globaalse aadressiraamatu mudeli täiendamist peavad olema täidetud järgmised eeltingimused:

+ Teil peab olema [Azure'i](https://portal.azure.com/) kordustellimus.
+ Teil peab olema juurdepääs [...](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) mallidele.
+ Olete olemasolev topeltkirjutamise klient.

## <a name="prepare-for-the-upgrade"></a>Täienduseks ettevalmistamine

Uuendus vajab järgmist ettevalmistust:

+ **Täielik sünkroonimine: nii finants- ja toimingute keskkond kui ka kliendi kaasamise keskkond on tabelite Konto (Klient), Kontakt ja** Hankija **täielikult** **·** **·** sünkroonitud olekus.
+ **Integratsioonivõtmed: konto (klient), kontakt ja hankija tabelid kliendikogemuse rakendustes kasutavad** **·** **·** **·** boksist väljas klahve. Kui kohandasite integratsioonivõtmeid, peate malli kohandama.
+ **Osapoole number:** **kõikidel konto (kliendi), kontakti ja** hankija **·** **·** kirjetel, mida täiendatakse, on osapoole number. Osapoolenumbrita kirjeid eiratakse. Kui soovite neid kirjeid täiendada, lisage neile osapoole number enne täiendusprotsessi käivitamist.
+ **Süsteemikatkestus– värskendusprotsessi ajal tuleb teil võtta nii finantside kui ka toimingute keskkond ning kliendi kaasamise** keskkond võrguühenduseta.
+ **·** Hetktõmmis: tehke hetktõmmis rakendustest Finance and Operations ja kliendi kaasamise rakendustest. Seejärel saate vajadusel kasutada hetktõmmiseid eelmise oleku taastamiseks.

## <a name="deployment"></a>Juurutamine

1. Laadige mallid alla [Dynamics-365-FastTrack-Implementation-Assetsst.](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)
2. Logige sisse [Azure’i portaali](https://portal.azure.com/).
3. Looge [ressursigrupp](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Looge loodud ressursirühmas [talletuskonto](/azure/storage/common/storage-account-create?tabs=azure-portal).
5. Looge [loodud](/azure/data-factory/quickstart-create-data-factory-portal) ressursigrupis andme tehas.
6. Avage andmete tehas ja valige Autori **> Monitori** paani.
7. Klõpsake menüüs **Haldamine** nuppu **ARM-mall**.
8. Valige **osapoole malli importimiseks mall Import** **·** ARM.
9. Importige mall andmevabrikusse. Sisestage **projekti üksikasjade** ja **eksemplari üksikasjade** jaoks järgmised väärtused.

    | Field | Väärtus |
    |---|---|
    | Kordustellimus | Azure'i kordustellimus |
    | Ressursigrupp | Sisestage sama ressurss, mille alusel ladustamiskonto luuakse. |
    | Regioon | Piirkond |
    | Vabriku nimi | Tehase nimi |
    | FO lingitud Service_service põhivõti | Rakenduse võti |
    | Azure Blobi Storage_connection string | Azure'i bloobi talletusühenduse string |
    | Dynamics Crm-iga lingitud Service_password | Kasutajanimaks määratav kasutajakonto parool |
    | FO lingitud Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO lingitud Service_properties_type Properties_tenant | Teave (domeeninimi või rentniku ID) teie avalduses nimetatud rentniku kohta |
    | FO lingitud Service_properties_type Properties_aad resursi ID | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO lingitud Service_properties_type Properties_service põhi-ID | Rakenduse kliendi ID |
    | Dynamics Crm-iga lingitud Service_properties_type Properties_username | Kasutajanimi, mida kasutatakse Dynamics 365-ga ühenduse loomiseks |

    Lisateavet vt järgmistest teemadest:

    - [Kasutage Resource Manager malli iga keskkonna puhul käsitsi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Lingitud teenuse atribuudid](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Andmete kopeerimine Azure Data Factory abil](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Pärast juurutamist valideerige andmevabriku andmekogumid, andmevoog ja lingitud teenus.

    ![Andmekogumid, andmevoog ja lingitud teenus.](media/data-factory-validate.png)

11. Avage **·** haldamine. Valige jaotises **Ühendused** väärtus **Lingitud teenus**. Seejärel valige **DynamicsCrmLinkedService.** Dialoogiboksis **Lingitud teenuse redigeerimine Dynamics CRM** () sisestage järgmised väärtused.

    | Field | Väärtus |
    |---|---|
    | Nimi | DynamicsCrmLinkedService |
    | Kirjeldus | Lingitud teenused CRM-i eksemplariga ühenduse loomiseks olemite andmete toomiseks |
    | Ühenduse loomine integratsiooni käitusaja kaudu | AutoResolvelntegrationRuntime |
    | Juurutamistüüp | Võrgus |
    | Teenuse Uri | `https://<organization-name>.crm[x].dynamics.com` |
    | Autentimise tüüp | Office365 |
    | Kasutajanimi | |
    | Parool või Azure'i võtmehoidla | Parool |
    | Parool | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Andmete tehase mallide käivitamiseks valmistumine

See jaotis kirjeldab seadistust, mida nõutakse enne osapoole postiaadressi ja osapoole elektroonilise aadressi andmete tehase mallide käivitamist.

### <a name="setup-to-run-the-party-postal-address-template"></a>Osapoole postiaadressi malli käivitamise häälestus

1. Logige sisse kliendikogemuse rakendustesse ja minge **sätete** \> **isikupärastamise** sätetesse. Seejärel konfigureerige **·** vahekaardil Üldine ajavööndi säte süsteemiadministraatori konto jaoks. Ajavöönd peab olema koordineeritud maailmaajas (UTC), et värskendada rakendustest pärit postiaadresside "kehtib alates" ja "kehtiv kuni" Finance and Operations kuupäevi.

    ![Ajavööndi säte süsteemiadministraatori konto jaoks.](media/ADF-1.png)

2. Andmete tehases, vahekaardil **Haldamine** globaalsete **parameetrite all looge** järgmine globaalne parameeter.

    | Number | Nimi | Tüüp | Väärtus |
    |---|---|---|---|
    | 1 | PostiaadressIdPrefix | string | Selle parameetriga lisatakse seerianumber vastloodud postiaadressidele eesliitena. Sisestage kindlasti string, mis ei satu vastuollu rakenduste ja Finance and Operations kliendikogemuse rakenduste postiaadressidega. Näiteks kasutage **ADF-PAD-**. |

    ![Vahekaardil Haldamine loodud postalAddressIdPrefix globaalne parameeter.](media/ADF-2.png)

3. Kui olete lõpetanud, valige käsk **Avalda** kõik.

    ![Nupp Avalda kõik.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Osapoole elektroonilise aadressi malli käivitamise häälestus

1. Andmete tehases, vahekaardil **·** Halda, **globaalsete parameetrite all** looge järgmised globaalsed parameetrid.

    | Number | Nimi | Tüüp | Väärtus |
    |---|---|---|---|
    | 1 | IsFOSource | Bool | See parameeter määratleb, millised esmased süsteemiaadressid vastuolude korral asendatakse. Kui see väärtus on **·** tõene, asendavad rakenduste Finance and Operations esmased aadressid kliendikogemuse rakendustes esmased aadressid. Kui väärtus on **·** väär, asendavad kliendi kaasamise rakenduste esmased aadressid peamised aadressid Finance and Operations rakendustes. |
    | 2 | ElektroonilineAddressIdPrefix | string | See parameeter lisab eesliitena vastloodud elektroonilistele aadressidele seerianumbri. Sisestage kindlasti string, mis ei satu vastuollu rakenduste ja kliendikogemuse Finance and Operations rakenduste elektrooniliste aadressidega. Näiteks kasutage **ADF-EAD-**. |

    ![IsFOSource ja ElectronicAddressIdPrefix globaalsed parameetrid on loodud vahekaardil Haldamine.](media/ADF-4.png)

2. Kui olete lõpetanud, valige käsk **Avalda** kõik.

## <a name="run-the-templates"></a>Mallide käitamine

1. Peatage järgmised **·** konto, **kontakt ja hankija** **·** topeltkirjutuse kaardid, mis rakendust Finance and Operations kasutavad:

    + Kliendid V3 (kontod)
    + Kliendi V3 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + Hankija V2 (msdyn_vendor)

2. Veenduge, et vastekaardid on **tabelist msdy_dualwriteruntimeconfig** eemaldatud Dataverse.
3. Installige [kahekirjutajalised osapoole ja globaalse aadressiraamatu lahendused](https://aka.ms/dual-write-gab) AppSource rakendusest.
4. Rakenduses Finance and Operations käivitage **esialgne sünkroonimine** järgmiste tabelite jaoks, kui need sisaldavad andmeid:

    + Tervitused
    + Isiklikud märgitüübid
    + Viisakusväljend
    + Kontaktisiku tiitlid
    + Otsustamisrollid
    + Püsikliendi tasemed

5. Keelake klienditeeninduse rakenduses järgmised lisandmooduli etapid.

    + Konto uuendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konto värskendamine
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konto värskendamine

    + Kontakti värskendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontakti värskendamine
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontakti värskendamine

    + msdyn_party värskendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party värskendamine

    + msdyn_vendor värskendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor värskendamine

    + Customeraddress

        + Loo

            + Microsoft.Dynamics.GABExtended.Kirje.CreatePartyAddress: kliendiaddressi loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Kirje.CreatePartyAddress: kliendiaddressi uuendamine

        + Kustuta

            + Microsoft.Dynamics.GABExtended.Kirje.DeleteCustomerAddress: kliendiaddressi kustutamine

    + msdyn_partypostaladdress

        + Loo

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: loo msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: loodud msdyn_partypostaladdress

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: kliendi msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: toote msdyn_partypostaladdress

    + msdyn_postaladdress

        + Loo

            + Microsoft.Dynamics.GABExtended.Sisesta.PostalAddress: uue msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Saate.PostalAddressPostCreate: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: kauba msdyn_postaladdress

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Update.PostalAddressUpdate: kliendi msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: kliendi msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Loo

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: kauba msdyn_partyelectronicaddress

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: toote msdyn_partyelectronicaddress

        + Kustuta

            + Microsoft.Dynamics.GABExtended.Elec.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress

6. Keelake kliendi kaasamise rakenduses järgmised töövood.

    + Hankijate loomine kontode tabelis
    + Hankijate loomine kontode tabelis
    + Isiku tüübiga hankijate loomine kontaktide tabelis
    + Isiku tüübiga hankijate loomine hankijate tabelis
    + Hankijate värskendamine kontode tabelis
    + Hankijate värskendamine hankijate tabelis
    + Isiku tüübiga hankijate värskendamine kontaktide tabelis
    + Isiku tüübiga hankijate värskendamine hankijate tabelis

7. Käitage mall andmete tehases, valides käsu **Käivita** kohe, nagu näha järgmises illustratsioonis. Olenevalt andmemahust võib selleks protsessiks vajada mõni tund.

    ![Malli käivitamine.](media/data-factory-trigger.png)

    > [!NOTE]
    > Kui olete kohandanud **·** konto, **kontakti** ja **·** hankija, peate malli muutma.

8. Importige uued **osapoole** kirjed Finance and Operations rakendusse.

    1. Laadige alla **fail FONewParty.csv** Azure Blobi mäluseadmest. Tee on **partybootstrapping/output/FONewParty.csv.**
    2. Teisendage **fail FONewParty.csv** Exceli faili ja importige Exceli fail Finance and Operations rakendusse. Kui CSV-import teie eest töötab, saate importida .csv-faili otse. Olenevalt andmemahust võib selle lõpule viimine võtta mitu tundi. Lisateavet vt [Andmete importimis- ja eksportimistööde ülevaade](../data-import-export-job.md).

    ![Osapoole Dataverse kirjete importimine](media/data-factory-import-party.png)

9. Käitage andmete tehases osapoole postiaadress ja osapoole elektroonilise aadressi mallid üksteise järel.

    + Osapoole postiaadressi malli kõik kliendisessi rakenduse postiaadressi kirjed ja seostab need vastavate konto, kontaktide ja **·** hankija **·** **·** kirjetega. Samuti loob see kolm .CSV-faili: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv ja ImportFONewPostalAddress.csv.
    + Osapoole elektroonilise aadressi malli kõik kliendisessi rakenduse elektroonilised aadressid ja seostab need vastavate konto, kontaktide ja **·** hankija **·** **·** kirjetega. Samuti loob see ühe .CSV-faili: ImportFONewElectronicAddress.csv.

    ![Osapoole postiaadressi ja osapoole elektroonilise aadressi mallide käitamine](media/ADF-7.png)

10. Rakenduse Finance and Operations värskendamiseks nende andmetega peate teisendama .CSV-failid Exceli töövihikusse ja [importima selle Finance and Operations](/data-entities/data-import-export-job) rakendusse. Kui CSV-import teie eest töötab, saate importida .csv-failid otse. Olenevalt mahust võib selle lõpule viimine võtta mitu tundi.

    ![Õnnestunud import.](media/ADF-8.png)

11. Kliendikogemuse rakenduses lubage järgmised lisandmooduli etapid.

    + Konto uuendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konto värskendamine
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konto värskendamine

    + Kontakti värskendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontakti värskendamine
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontakti värskendamine

    + msdyn_party värskendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party värskendamine

    + msdyn_vendor värskendamine

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor värskendamine

    + msdyn_partypostaladdress

        + Loo

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: loo msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: loodud msdyn_partypostaladdress

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: kliendi msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: toote msdyn_partypostaladdress

    + msdyn_postaladdress

        + Loo

            + Microsoft.Dynamics.GABExtended.Sisesta.PostalAddress: uue msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Saate.PostalAddressPostCreate: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: kauba msdyn_postaladdress

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Update.PostalAddressUpdate: kliendi msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: kliendi msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Loo

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: kauba msdyn_partyelectronicaddress

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: toote msdyn_partyelectronicaddress

        + Kustuta

            + Microsoft.Dynamics.GABExtended.Elec.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress

12. Kliendikogemuse rakenduses aktiveerige järgmised töövood, kui te need eelnevalt inaktiveerisite:

    + Hankijate loomine kontode tabelis
    + Hankijate loomine kontode tabelis
    + Isiku tüübiga hankijate loomine kontaktide tabelis
    + Isiku tüübiga hankijate loomine hankijate tabelis
    + Hankijate värskendamine kontode tabelis
    + Hankijate värskendamine hankijate tabelis
    + Isiku tüübiga hankijate värskendamine kontaktide tabelis
    + Isiku tüübiga hankijate värskendamine hankijate tabelis

13. Käivitage **osapoole** kirjega seotud kaardid, nagu on kirjeldatud [osapoole ja globaalses aadressiraamatus.](party-gab.md)

## <a name="explanation-of-the-data-factory-templates"></a>Andmevab tehase mallide selgitus

See jaotis viib teid läbi andme tehasmallide sammude.

### <a name="steps-in-the-party-template"></a>Osapoole malli etapid

1. Sammud 1–6 määratlevad ettevõtted, mis on topeltkirjutusega lubatud ja koostetvad nende jaoks filtriklausli.
2. Etapid 7-1 kuni 7-9 toob andmeid nii rakendusest kui ka kliendikogemuse rakendusest ja Finance and Operations etapist, mille andmed on uuendamiseks.
3. Sammud 8–9 võrdlevad rakenduse ja kliendi kaasamise rakenduse vaheliste konto, kontaktide ja **·** hankija kirjete **·** **·** Finance and Operations osapoolenumbrit. Kõik osapoolenumbrita kirjed jäetakse vahele.
4. 10. etapp loob kaks .CSV-faili osapoolekirjetele, mis tuleb luua customer Engagementi rakenduses ja Finance and Operations rakenduses.

    - **FOCDSParty.csv – see fail sisaldab kõigi mõlema süsteemi osapoolekirjeid, sõltumata sellest, kas ettevõte** on lubatud topeltkirjutuse jaoks.
    - **FONewParty.csv – see fail sisaldab osapoolekirjete alamkogumit, mida on teada (nt potentsiaalse kliendi** Dataverse tüübi **·** kontod).

5. 11. etapp loob osapooled kliendi kaasamise rakenduses.
6. 12. etapp toob kliendikogemuse rakendusest globaalselt kordumatud ID-d (GUID-d) ja etapid, et neid saaks seostada järgmiste sammudega konto-, kontakti- ja **·** **·** **·** hankijakirjetega.
7. 13. etapp seostab **·** konto, **kontakti ja hankija kirjed osapoole** **·** GUID-dega.
8. Sammud 14-1 kuni 14-3 värskendage kliendikogemuse rakenduses **·** osapoole **·** GUID-dega konto, kontakt ja **·** hankija kirjed.
9. Sammud 15-1 kuni 15-3 valmistage ette kontakti osapoole kirjete **·** jaoks **·** konto, kontakti ja hankija **kirjete** **·** jaoks.
10. Sammud 16–1–16–7 toob viiteandmed (nt tervitused ja isiklikud märgitüübid) ja seostab need osapoolekirjete **·** kontaktiga.
11. 17. etapp ühendab **osapoole kirjete kontakti** **·** konto, kontakti ja hankija **·** **·** kirjetega.
12. 18. etapp **impordib osapoole kirjete** kontakti customer Engagementi rakendusesse.

### <a name="steps-in-the-party-postal-address-template"></a>Osapoole postiaadressi malli etapid

1. Etapid 1-1 kuni 1-10 toob andmeid nii rakendusest kui ka kliendikogemuse rakendusest Finance and Operations ja etapist, kus andmed on uuendamiseks.
2. 2. sammus de normaliseerib rakenduse postiaadressi andmed postiaadressi ja Finance and Operations postiaadressi ühendamise teel.
3. 3. sammus dedlikatsioonid ja ühendatakse kliendikogemuse rakenduse konto, kontakti ja hankija aadressiandmed.
4. 4. etapp loob rakendusele .CSV-failid, et luua uued aadressiandmed, mis põhinevad Finance and Operations konto, kontaktil ja hankija aadressidel.
5. Sammuga 5-1 luuakse .CSV-failid customer Engagementi rakendusele, et luua kõik aadressiandmed, mis põhinevad nii rakendusel kui ka Finance and Operations kliendikogemuse rakendusel.
6. 5.2. etapp teisendab .CSV-failid käsitsi Finance and Operations importimiseks impordivormingusse.

    - ImpordiFONewPostalAddressLocation.csv
    - ImpordiFONewPartyPostalAddress.csv
    - ImpordiFONewPostalAddress.csv

7. 6. etapp impordib postiaadresside kogumise andmed customer Engagementi rakendusesse.
8. 7. sammus tuuakse klienditeeninduse rakendusest postiaadresside kogumise andmed.
9. 8. etapp loob kliendi aadressiandmed ja seostab postiaadresside kogumise ID.
10. Sammud 9-1 kuni 9-2 seostavad osapoole ja postiaadresside kogumi ID-d postiaadresside ja osapoole postiaadressidega.
11. Sammud 10-1 kuni 10-3 impordivad kliendi aadresse, postiaadresse ja osapoole postiaadresse klienditeeninduse rakendusse.

### <a name="steps-in-the-party-electronic-address-template"></a>Osapoole elektroonilise aadressi malli etapid

1. Etapid 1–1–5 toob andmeid nii rakendusest kui ka kliendikogemuse rakendusest ja Finance and Operations etapist, mille andmed on uuendamiseks.
2. 2. etapp konsolideerib kliendi kaasamise rakenduse elektroonilised aadressid konto-, kontakti- ja hankijaüksustest.
3. 3. etapp ühendab rakendusest Customer Engagement ja rakendusest esmased elektroonilise aadressi Finance and Operations andmed.
4. 4. etapp loob .CSV-failid.

    - Looge rakenduse jaoks uued elektroonilise aadressi Finance and Operations andmed, mis põhinevad konto, kontakti ja hankija aadressidel.
    - Looge uued elektroonilised aadressiandmed kliendi kaasamise rakenduse jaoks, mis põhinevad rakenduses elektroonilisel aadressil, kontol, kontaktil ja hankija Finance and Operations aadressidel.

5. 5.1. etapp impordib elektroonilised aadressid klienditeeninduse rakendusse.
6. Sammuga 5-2 luuakse .CSV-failid, et värskendada kontode ja kontaktide esmaseid aadresse Customer Engagementi rakenduses.
7. Sammud 6-1 kuni 6-2 impordikontod ja kontakti esmased aadressid customer Engagementi rakendusse.

## <a name="troubleshooting"></a>Tõrkeotsing

1. Kui protsess nurjub, käivitage andmete tehas uuesti. Alustage nurjunud tegevusest.
2. Andmevabiku loodud faile saab kasutada andmete valideerimiseks.
3. Andmete tehas töötab .CSV-failide põhjal. Kui koma on kaasatud mis tahes välja väärtusesse, võib see olla koos tulemustega. Peate eemaldama väljaväärtustelt kõik komad.
4. Vahekaart **·** Seire annab teavet kõigi töödeldud etappide ja andmete kohta. Valige selle silumiseks kindel juhis.

    ![Jälgimise vahekaart.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Lisateave malli kohta

Lisateavet malli kohta vt kommentaaridest [Azure Data Factory malli lugemiseks.](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)
