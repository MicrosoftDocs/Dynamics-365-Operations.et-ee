---
title: Üleminek osapoole ja globaalse aadressiraamatu mudelile
description: See artikkel kirjeldab, kuidas täiendada topeltkirjutuse andmeid osapoolele ja globaalse aadressiraamatu mudelile.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 02ab3675db0d78efa1e4e43188d79bb1e763a713
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111814"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Üleminek osapoole ja globaalse aadressiraamatu mudelile

[!include [banner](../../includes/banner.md)]



Andmete [Microsoft Azure tehase mallid](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) aitavad teil täiendada järgmisi olemasolevaid andmeid topeltkirjutuses osapoolele ja globaalse aadressiraamatu mudelile: **andmed** konto, **·** **kontaktide** ja hankija tabelites ning posti- ja elektroonilised aadressid.

Antud on järgmised kolm Data Factory malle. Need aitavad viia vastavusse nii finantside ja toimingute rakenduste kui ka klienditeeninduse rakenduste andmeid.

- **[Osapoole mall](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (täiendage andmeid topeltkirjutusega osapoole-GAB skeemiks/arm_template.json)** – see **mall** **aitab** täiendada osapoole ja kontaktandmeid, mis on **seotud** konto, **kontakti** ja hankija **andmetega.**
- **[Osapoole postiaadressi](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) mall (täiendage andmeid topeltkirjutusega osapoole-GAB skeemiks/täiendage osapoole postiaadressiks - GAB/arm_template.json)** –**see** mall aitab täiendada konto, **·** **kontakti** ja hankija andmetega seotud postiaadresse.
- **[Osapoole elektroonilise aadressi mall](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (täiendusandmed topeltkirjutusega osapoole-GAB skeemiks/osapoole elektrooniliseks aadressiks – GAB/arm_template.json)** – **see** mall aitab täiendada konto, **·** **kontakti** ja hankija andmetega seotud elektroonilisi aadresse.

Protsessi lõpus luuakse järgmised komaga eraldatud failid (.csv).

| Failinimi | Eesmärk |
|---|---|
| FoNewParty.csv | See fail aitab luua uusi **osapoole kirjeid** finantside ja toimingute rakenduses. |
| ImpordiFONewPostalAddressLocation.csv | See fail aitab luua uued **postiaadressi asukoha** kirjed finantside ja toimingute rakenduses. |
| ImpordiFONewPartyPostalAddress.csv | See fail aitab luua uued **osapoole postiaadressi** kirjed finantside ja toimingute rakenduses. |
| ImpordiFONewPostalAddress.csv | See fail aitab luua uusi **postiaadressi** kirjeid finantside ja toimingute rakenduses. |
| ImpordiFONewElectronicAddress.csv | See fail aitab luua uusi **elektroonilise aadressi** kirjeid finantside ja toimingute rakenduses. |

See artikkel selgitab, kuidas kasutada data factory malle ja uuendada andmeid. Kui te ühtegi kohandust ei tee, saate malle kasutada nii, nagu need on. Kuid kui teil on konto, kontakti **ja** **·** **hankija andmete kohandusi, peate malle muutma selles artiklis kirjeldatud viisil.**

> [!IMPORTANT]
> Osapoole postiaadressi ja osapoole elektroonilise aadressi mallide käivitamiseks on erijuhised. Esmalt peate käivitama osapoole malli, seejärel osapoole postiaadressi malli ja seejärel osapoole elektroonilise aadressi malli. Iga mall on mõeldud impordiks eraldi andme tehas.

## <a name="prerequisites"></a>Eeltingimused

Enne osapoole ja globaalse aadressiraamatu mudeli täiendamist peavad olema täidetud järgmised eeltingimused:

+ Teil peab olema Azure'i [kordustellimus](https://portal.azure.com/).
+ Teil peab olema juurdepääs [mallidele](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Olete olemasolev topeltkirjutamise klient.

## <a name="prepare-for-the-upgrade"></a>Täienduseks ettevalmistamine

Uuendus vajab järgmist ettevalmistust:

+ **Täielik sünkroonimine:** nii finants- ja toimingute keskkond kui ka kliendi kaasamise keskkond **on tabelite Konto (Klient)**, **·** **Kontakt ja Hankija täielikult sünkroonitud olekus.**
+ **Integreerimisvõtmed**: **konto (klient)**, **kontakt** **ja** hankija tabelid kliendikogemuse rakendustes kasutavad boksist väljaminev integreerimisvõtmeid. Kui kohandasite integratsioonivõtmeid, peate malli kohandama.
+ **Osapoole number:** kõigil **täiendamist** vajav **konto**-, kontakti **·**- ja hankijakirjel on osapoole number. Osapoolenumbrita kirjeid eiratakse. Kui soovite neid kirjeid täiendada, lisage neile osapoole number enne täiendusprotsessi käivitamist.
+ **Süsteemikatkestus–** värskendusprotsessi ajal tuleb teil võtta nii finantside kui ka toimingute keskkond ning kliendi kaasamise keskkond võrguühenduseta.
+ **Hetktõmmis:** tehke hetktõmmis nii finantside ja toimingute rakendustest kui ka kliendi kaasamise rakendustest. Seejärel saate vajadusel kasutada hetktõmmiseid eelmise oleku taastamiseks.

## <a name="deployment"></a>Juurutamine

1. Laadige mallid alla [Dynamics-365-FastTrack-Implementation-Assetsst](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Logige sisse [Azure’i portaali](https://portal.azure.com/).
3. Looge [ressursigrupp](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Looge loodud ressursirühmas [talletuskonto](/azure/storage/common/storage-account-create?tabs=azure-portal).
5. Looge loodud [ressursigrupis](/azure/data-factory/quickstart-create-data-factory-portal) andme tehas.
6. Avage andmete tehas ja valige Autori > **Monitori paani**.
7. Klõpsake menüüs **Haldamine** nuppu **ARM-mall**.
8. Valige **osapoole malli importimiseks** mall **Import** ARM.
9. Importige mall andmevabrikusse. Sisestage **projekti üksikasjade** ja **eksemplari üksikasjade** jaoks järgmised väärtused.

    | Väli | Väärtus |
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

11. Avage **haldamine**. Valige jaotises **Ühendused** väärtus **Lingitud teenus**. Seejärel valige **DynamicsCrmLinkedService**. Dialoogiboksis Redigeeri **lingitud teenust (Dynamics CRM)** sisestage järgmised väärtused.

    | Väli | Väärtus |
    |---|---|
    | Nimi | DynamicsCrmLinkedService |
    | Kirjeldus | Lingitud teenused CRM-i eksemplariga ühenduse loomiseks olemite andmete toomiseks |
    | Ühenduse loomine integratsiooni käitusaja kaudu | AutoResolvelntegrationRuntime |
    | Juurutamistüüp | Võrgus |
    | Teenuse Uri | `https://<organization-name>.crm[x].dynamics.com` |
    | Autentimise tüüp | Office365 |
    | Kasutaja nimi | |
    | Parool või Azure'i võtmehoidla | Parool |
    | Parool | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Andmete tehase mallide käivitamiseks valmistumine

See jaotis kirjeldab seadistust, mida nõutakse enne osapoole postiaadressi ja osapoole elektroonilise aadressi andmete tehase mallide käivitamist.

### <a name="setup-to-run-the-party-postal-address-template"></a>Osapoole postiaadressi malli käivitamise häälestus

1. Logige sisse klienditeeninduse rakendustesse ja minge **sätete** \> **isikupärastamise sätetesse.** Seejärel konfigureerige **vahekaardil** Üldine ajavööndi säte süsteemiadministraatori konto jaoks. Ajavöönd peab olema koordineeritud maailmaajas (UTC), et värskendada finantside ja toimingute rakenduste postiaadresside "kehtib alates" ja "kehtiv kuni" kuupäevi.

    ![Ajavööndi säte süsteemiadministraatori konto jaoks.](media/ADF-1.png)

2. Andmete tehases, vahekaardil **Haldamine** globaalsete parameetrite **all** looge järgmine globaalne parameeter.

    | Number | Nimi | Tüüp | Väärtus |
    |---|---|---|---|
    | 1 | PostiaadressIdPrefix | string | Selle parameetriga lisatakse seerianumber vastloodud postiaadressidele eesliitena. Sisestage kindlasti string, mis ei ole vastuolus postiaadressidega finantside ja operatsioonide rakendustes ja kliendikogemuse rakendustes. Kasutage näiteks **ADF-PAD-.** |

    ![Vahekaardil Haldamine loodud postalAddressIdPrefix globaalne parameeter.](media/ADF-2.png)

3. Kui olete lõpetanud, valige käsk **Avalda kõik**.

    ![Nupp Avalda kõik.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Osapoole elektroonilise aadressi malli käivitamise häälestus

1. Andmete tehases, vahekaardil **Haldamine** globaalsete parameetrite **all** looge järgmised globaalsed parameetrid.

    | Number | Nimi | Tüüp | Väärtus |
    |---|---|---|---|
    | 1 | IsFOSource | Bool | See parameeter määratleb, millised esmased süsteemiaadressid vastuolude korral asendatakse. Kui see väärtus on **tõene**, asendavad finantside ja toimingute rakenduste esmased aadressid kliendikogemuse rakendustes esmased aadressid. Kui väärtus on väär **, asendavad** kliendi kaasamise rakenduste esmased aadressid finantside ja toimingute rakenduste esmased aadressid. |
    | 2 | ElektroonilineAddressIdPrefix | string | See parameeter lisab eesliitena vastloodud elektroonilistele aadressidele seerianumbri. Sisestage kindlasti string, mis ei satu vastuollu elektrooniliste aadressidega finantside ja operatsioonide rakendustes ja kliendikogemuse rakendustes. Näiteks kasutage ADF-EAD **-**. |

    ![IsFOSource ja ElectronicAddressIdPrefix globaalsed parameetrid on loodud vahekaardil Haldamine.](media/ADF-4.png)

2. Kui olete lõpetanud, valige käsk **Avalda kõik**.

## <a name="run-the-templates"></a>Mallide käitamine

1. Peatage järgmised osapoole **,** konto **,** kontakti **ja hankija** topeltkirjutuse kaardid, **mis** kasutavad finantside ja toimingute rakendusi:

    + CDS-osapooled (msdyn_parties) 
    + Kliendid V3 (kontod)
    + Kliendi V3 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + Hankija V2 (msdyn_vendor)
    + Kontaktid V2 (msdyn_contactforparties)
    + CDS-osapoole postiaadresside asukohad (msdyn_partypostaladdresses)
    + CDS-i postiaadresside ajalugu V2 (msdyn_postaladdresses)
    + CDS-i postiaadresside asukohad (msdyn_postaladdresscollections)
    + Osapoole kontaktid V3 (msdyn_partyelectronicaddresses)

2. Veenduge, et vastekaardid on tabelist **msdy_dualwriteruntimeconfig** eemaldatud Dataverse.
3. Installige [kahekirjutajalised osapoole ja globaalse aadressiraamatu lahendused](https://aka.ms/dual-write-gab) AppSource rakendusest.
4. Finantside ja toimingute rakenduses käivitage esialgne **sünkroonimine** järgmiste tabelite jaoks, kui need sisaldavad andmeid:

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

        + Loomine

            + Microsoft.Dynamics.GABExtended.Kirje.CreatePartyAddress: kliendiaddressi loomine

        + Värskenda

            + Microsoft.Dynamics.GABExtended.Kirje.CreatePartyAddress: kliendiaddressi uuendamine

        + Kustutusklahv

            + Microsoft.Dynamics.GABExtended.Kirje.DeleteCustomerAddress: kliendiaddressi kustutamine

    + msdyn_partypostaladdress

        + Loomine

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: loodud msdyn_partypostaladdress

        + Värskenda

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: kliendi msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: toote msdyn_partypostaladdress

    + msdyn_postaladdress

        + Loomine

            + Microsoft.Dynamics.GABExtended.Saate.PostalAddress: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Saate.PostalAddressPostCreate: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: loo msdyn_postaladdress

        + Värskenda

            + Microsoft.Dynamics.GABExtended.Update.PostalAddressUpdate: kliendi msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: kliendi msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Loomine

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: kauba msdyn_partyelectronicaddress

        + Värskenda

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: toote msdyn_partyelectronicaddress

        + Kustutusklahv

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

7. Käitage mall andmete tehases, valides käsu **Käivita kohe**, nagu näha järgmises illustratsioonis. Olenevalt andmemahust võib selleks protsessiks vajada mõni tund.

    ![Malli käivitamine.](media/data-factory-trigger.png)

    > [!NOTE]
    > Kui teil on konto **, kontakti** **ja** hankija **kohandusi**, peate malli muutma.

8. Importige uued **osapoole** kirjed finantside ja toimingute rakendusse.

    1. Laadige alla **FONewParty.csv Azure** Blob ladustamise fail. Tee on partybootstrapping **/output/FONewParty.csv**.
    2. Teisendage **FONewParty.csv fail** Exceli faili ja importige Exceli fail finantside ja toimingute rakendusse. Kui CSV-import teile töötab, saate selle otse .csv importida. Olenevalt andmemahust võib selle lõpule viimine võtta mitu tundi. Lisateavet vt [Andmete importimis- ja eksportimistööde ülevaade](../data-import-export-job.md).

    ![Osapoole kirjete Dataverse importimine](media/data-factory-import-party.png)

9. Käitage andmete tehases osapoole postiaadress ja osapoole elektroonilise aadressi mallid üksteise järel.

    + Osapoole postiaadressi malli kõik kliendisessi rakenduse postiaadressi kirjed ja seostab need vastavate konto-, **kontakti**- ja **hankijakirjetega**.**·** Samuti loob see kolm .csv: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv ja ImportFONewPostalAddress.csv.
    + Osapoole elektroonilise aadressi malli kõik kliendisessi rakenduse elektroonilised aadressid ja seostatakse need vastavate konto-, **kontakti**- ja **hankijakirjetega**.**·** See loob ka ühe .csv: ImportFONewElectronicAddress.csv.

    ![Osapoole postiaadressi ja osapoole elektroonilise aadressi mallide käitamine](media/ADF-7.png)

10. Finantside ja toimingute rakenduse värskendamiseks nende andmetega peate teisendama .csv failid Exceli [töövihikusse ja importima need finantside ja toimingute rakendusse](../data-import-export-job.md). Kui CSV-import teile töötab, saate need otse .csv importida. Olenevalt mahust võib selle lõpule viimine võtta mitu tundi.

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

        + Loomine

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: loodud msdyn_partypostaladdress

        + Värskenda

            + Microsoft.Dynamics.GABExtended.Malli.CreateCustomerAddress: kliendi msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Identifikaator.PartyPostalAddress: toote msdyn_partypostaladdress

    + msdyn_postaladdress

        + Loomine

            + Microsoft.Dynamics.GABExtended.Saate.PostalAddress: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Saate.PostalAddressPostCreate: msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: loo msdyn_postaladdress

        + Värskenda

            + Microsoft.Dynamics.GABExtended.Update.PostalAddressUpdate: kliendi msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.UuendusCustomerAddress: kliendi msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Loomine

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: kauba msdyn_partyelectronicaddress

        + Värskenda

            + Microsoft.Dynamics.GABExtended.Elec.PartyElectronicAddressSync: toote msdyn_partyelectronicaddress

        + Kustutusklahv

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

13. Käivitage osapoole **kirjega** seotud kaardid, nagu on kirjeldatud osapoole ja [globaalses aadressiraamatus](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Andmevab tehase mallide selgitus

See jaotis viib teid läbi andme tehasmallide sammude.

### <a name="steps-in-the-party-template"></a>Osapoole malli etapid

1. Sammud 1–6 määratlevad ettevõtted, mis on topeltkirjutusega lubatud ja koostetvad nende jaoks filtriklausli.
2. Sammud 7-1 kuni 7-9 toob andmeid nii finantside ja toimingute rakendusest kui ka kliendikogemuse rakendusest ja etapist, kus andmed on versioonitäienduseks.
3. Sammud 8–9 võrdlevad finantside **ja** operatsioonide rakenduse ning kliendi kaasamise rakenduse vaheliste konto-, **·** **kontakti**- ja hankijakirjete osapoolenumbrit. Kõik osapoolenumbrita kirjed jäetakse vahele.
4. 10. etapp loob .csv faili osapoolekirjetele, mis tuleb luua Customer Engagementi rakenduses ja finantside ja toimingute rakenduses.

    - **FOCDSParty.csv** – see fail sisaldab mõlema süsteemi kõiki osapoolekirjeid, sõltumata sellest, kas ettevõte on lubatud topeltkirjutuse jaoks.
    - **FONewParty.csv** – Dataverse see fail sisaldab pakutavate osapoolekirjete alamkogumit (**nt potentsiaalse kliendi tüübi kontosid**).

5. 11. etapp loob osapooled kliendi kaasamise rakenduses.
6. 12. etapp toob kliendikogemuse rakendusest globaalselt kordumatud ID-d (GUID-d) **ja etapid, et neid saaks seostada järgmiste sammudega konto-,** **·** **kontakti- ja hankijakirjetega.**
7. 13. etapp seostab **konto**, **kontakti ja** hankija kirjed **osapoole** GUID-dega.
8. Sammud 14-1 kuni 14-3 **·** **värskendage** kliendikogemuse rakenduses osapoole GUID-dega konto, **kontakt**- ja hankijakirjeid.
9. Sammud 15–1 kuni 15-3 valmistage **ette** kontakti osapoole kirjete jaoks **konto**-, **kontakti-** ja hankijakirjete **jaoks**.
10. Sammud 16–1–16–7 toob viiteandmed (nt tervitused ja isiklikud märgitüübid) **ja seostab need osapoolekirjete kontaktiga**.
11. 17. etapp ühendab osapoole **kirjete kontakti konto** **-**, kontakti **- ja** hankijakirjete **jaoks**.
12. 18. etapp impordib **osapoole kirjete kontakti** customer Engagementi rakendusesse.

### <a name="steps-in-the-party-postal-address-template"></a>Osapoole postiaadressi malli etapid

1. Sammud 1-1 kuni 1-10 toob andmeid nii finantside ja toimingute rakendusest kui ka kliendikogemuse rakendusest ja etapist, kus andmed uuendatakse.
2. 2. etapp normaliseerib postiaadressi andmed finantside ja operatsioonide rakenduses postiaadressi ja osapoole postiaadressi ühendamisega.
3. 3. sammus dedlikatsioonid ja ühendatakse kliendikogemuse rakenduse konto, kontakti ja hankija aadressiandmed.
4. 4. sammus .csv finantside ja toimingute rakenduse jaoks uued failid, et luua uued aadressiandmed, mis põhinevad konto, kontakti ja hankija aadressidel.
5. Sammuga 5-1 .csv kliendi kaasamise rakendusele failid, et luua kõik aadressiandmed, mis põhinevad nii finantside kui ka toimingute rakendusel ja kliendi kaasamise rakendusel.
6. 5.2. etapp teisendab .csv faili käsitsi importimiseks finantside ja toimingute impordivormingusse.

    - ImpordiFONewPostalAddressLocation.csv
    - ImpordiFONewPartyPostalAddress.csv
    - ImpordiFONewPostalAddress.csv

7. 6. etapp impordib postiaadresside kogumise andmed customer Engagementi rakendusesse.
8. 7. sammus tuuakse klienditeeninduse rakendusest postiaadresside kogumise andmed.
9. 8. etapp loob kliendi aadressiandmed ja seostab postiaadresside kogumise ID.
10. Sammud 9-1 kuni 9-2 seostavad osapoole ja postiaadresside kogumi ID-d postiaadresside ja osapoole postiaadressidega.
11. Sammud 10-1 kuni 10-3 impordivad kliendi aadresse, postiaadresse ja osapoole postiaadresse klienditeeninduse rakendusse.

### <a name="steps-in-the-party-electronic-address-template"></a>Osapoole elektroonilise aadressi malli etapid

1. Etapid 1–1–5 toob andmeid nii finantside ja toimingute rakendusest kui ka kliendikogemuse rakendusest ja etapist, kus andmed on versioonitäienduseks.
2. 2. etapp konsolideerib kliendi kaasamise rakenduse elektroonilised aadressid konto-, kontakti- ja hankijaüksustest.
3. 3. etapp ühendab rakendusest Customer Engagement ja finantside ja toimingute rakendusest esmased elektroonilised aadressiandmed.
4. 4. etapp loob .csv faili.

    - Looge uued elektroonilised aadressiandmed finantside ja toimingute rakenduse jaoks, mis põhinevad konto, kontaktil ja hankija aadressidel.
    - Looge uued elektroonilised aadressiandmed kliendi kaasamise rakenduse jaoks, mis põhinevad elektroonilisel aadressil, kontol, kontaktil ja hankija aadressidel finantside ja toimingute rakenduses.

5. 5.1. etapp impordib elektroonilised aadressid klienditeeninduse rakendusse.
6. Sammuga 5-2 .csv rakendusse Customer Engagement kontode ja kontaktide esmaste aadresside värskendamiseks uusi faile.
7. Sammud 6-1 kuni 6-2 impordikontod ja kontakti esmased aadressid customer Engagementi rakendusse.

## <a name="troubleshooting"></a>Tõrkeotsing

1. Kui protsess nurjub, käivitage andmete tehas uuesti. Alustage nurjunud tegevusest.
2. Andmevabiku loodud faile saab kasutada andmete valideerimiseks.
3. Andme tehas töötab andmefailide .csv põhjal. Kui koma on kaasatud mis tahes välja väärtusesse, võib see olla koos tulemustega. Peate eemaldama väljaväärtustelt kõik komad.
4. Vahekaart **Seire** annab teavet kõigi töödeldud etappide ja andmete kohta. Valige selle silumiseks kindel juhis.

    ![Jälgimise vahekaart.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Lisateave malli kohta

Lisateavet malli kohta vt kommentaaridest [Azure Data Factory malli lugemiseks](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).

