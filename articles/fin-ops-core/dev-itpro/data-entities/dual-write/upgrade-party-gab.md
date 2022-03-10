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
ms.openlocfilehash: 579a7d19ee7196d3242c78bd9915df24ec479c31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060475"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Üleminek osapoole ja globaalse aadressiraamatu mudelile

[!include [banner](../../includes/banner.md)]



[Microsoft Azure Andmetehase mallid](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) aitavad teil täiendada järgmisi olemasolevaid andmeid topeltkirjutuses osapoole ja globaalse aadressiraamatu mudelile: andmed tabelites Konto **,** Kontakt **ja** Hankija **ning** posti- ja elektroonilised aadressid.

Esitatakse järgmised kolm Andmetehase malli. Need aitavad sobitada nii Finance and Operationsi rakenduste kui ka klientide kaasamise rakenduste andmeid.

- **[Osapoole mall](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (andmete täiendamine kahepalgeliste partei-GAB skeemiks/arm_template.json)** – see mall aitab täiendada **osapoole**- ja **kontaktiandmeid**, mis on seotud konto,kontakti **·** **ja** hankija **andmetega.**
- **[Osapoole postiaadressi mall](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (andmete täiendamine kahepalgeliste partei-GAB skeemiks/üleminek osapoole postiaadressile - GAB/arm_template.json)** – See mall aitab uuendada konto **,** kontakti **ja** hankija **andmetega** seotud postiaadresse.
- **[Osapoole elektrooniline aadressimall](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (andmete täiendamine kahepalgeliste partei-GAB skeemiks/üleminek osapoole elektroonilisele aadressile - GAB/arm_template.json)** – see mall aitab uuendada elektroonilisi aadresse, mis on seotud konto **,** kontakti **ja** hankija **andmetega**.

Protsessi lõpus luuakse järgmised komaeraldusega väärtuste (.csv) failid.

| Failinimi | Eesmärk |
|---|---|
| FONewParty.csv | See fail aitab rakenduses Finance and Operations luua uusi **osapoolekirjeid**. |
| ImportFOUusPostalAddressLocation.csv | See fail aitab rakenduses Finance and Operations luua uusi **postiaadressi asukohakirjeid**. |
| ImportFOUuusPartyPostalAddress.csv | See fail aitab rakenduses Finance and Operations luua uusi **osapoole postiaadressi** kirjeid. |
| ImportFOUusPostalAddress.csv | See fail aitab rakenduses Finance and Operations luua uusi **postiaadressi** kirjeid. |
| ImportFOUuusElektroonikaAddress.csv | See fail aitab rakenduses Finance and Operations luua uusi **elektroonilisi aadressikirjeid**. |

Selles teemas selgitatakse, kuidas kasutada Andmetehase malle ja andmeid täiendada. Kui teil pole kohandusi, saate malle kasutada nii, nagu need on. Kui teil on aga ettevõtte **,** kontakti **ja** hankija **andmete kohandusi**, peate selles teemas kirjeldatud malle muutma.

> [!IMPORTANT]
> Partei postiaadressi ja partei elektrooniliste aadressimallide käitamiseks on olemas spetsiaalsed juhised. Esmalt peate käivitama parteimalli, seejärel partei postiaadressi malli ja seejärel partei elektroonilise aadressi malli. Iga mall on mõeldud importimiseks eraldi andmetehases.

## <a name="prerequisites"></a>Eeltingimused

Enne peo- ja globaalse aadressiraamatu mudelile üle minna peavad olema järgmised eeltingimused.

+ Teil peab olema Azure'i [tellimus](https://portal.azure.com/).
+ Teil peab olema juurdepääs [mallidele](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Olete olemasolev topeltkirjutamise klient.

## <a name="prepare-for-the-upgrade"></a>Täienduseks ettevalmistamine

Täiendamine nõuab järgmist ettevalmistust.

+ **Täielik sünkroonimine:** nii finants- ja operatsioonide keskkond kui ka kliendi kaasamise keskkond on tabelite Konto (klient), Kontakt **ja** **Hankija** **täielikult** sünkroonitud olekus.
+ **Integratsioonivõtmed:** **kliendi kaasamise rakenduste tabelid Konto (klient),** Kontakt **ja** **Hankija** kasutavad väljamineku integratsioonivõtmeid. Kui kohandasite integratsioonivõtmeid, peate malli kohandama.
+ **Osapoole number:** kõigil **uuendatavatel konto-**, **kontakti**- ja **hankijakirjetel** on osapoole number. Kirjeid, millel pole peonumbrit, ignoreeritakse. Kui soovite neid kirjeid täiendada, lisage neile enne täiendusprotsessi alustamist osapoole number.
+ **Süsteemi katkestus:** Täiendusprotsessi ajal peate nii Finance and Operationsi keskkonna kui ka kliendi kaasamiskeskkonna võrguühenduseta lülitama.
+ **Hetktõmmis:** Tehke hetktõmmis nii Finance and Operationsi kui ka klientide kaasamise rakendustest. Seejärel saate vajaduse korral kasutada hetktõmmiseid eelmise oleku taastamiseks.

## <a name="deployment"></a>Juurutamine

1. Laadige mallid alla aadressilt [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Logige sisse [Azure’i portaali](https://portal.azure.com/).
3. Looge [ressursigrupp](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Looge loodud ressursirühmas [talletuskonto](/azure/storage/common/storage-account-create?tabs=azure-portal).
5. Loo [andmevabrik](/azure/data-factory/quickstart-create-data-factory-portal) loodud ressursirühmas.
6. Avage andmetehas ja valige **Autor ja jälgija** plaat.
7. Klõpsake menüüs **Haldamine** nuppu **ARM-mall**.
8. Valige **Impordi ARM-mall** importida **Pidu** malli.
9. Importige mall andmevabrikusse. Sisestage **projekti üksikasjade** ja **eksemplari üksikasjade** jaoks järgmised väärtused.

    | Field | Väärtus |
    |---|---|
    | Kordustellimus | Azure'i tellimus |
    | Ressursigrupp | Esitage sama ressurss, mille all salvestuskonto on loodud. |
    | Regioon | Regioon |
    | Vabriku nimi | Tehase nimi |
    | FO lingitud Service_service põhivõti | Rakenduse võti |
    | Azure Blobi Storage_connection string | Azure Blobi salvestusruumi ühenduse string |
    | Dynamics Crm-iga lingitud Service_password | Selle kasutajakonto parool, mille määrate kasutajanimeks |
    | FO lingitud Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO lingitud Service_properties_type Properties_tenant | Teave (domeeninimi või rentniku ID) selle rentniku kohta, kelle all teie rakendus asub |
    | FO lingitud Service_properties_type Properties_aad resursi ID | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO lingitud Service_properties_type Properties_service põhi-ID | Rakenduse kliendi ID |
    | Dynamics Crm-iga lingitud Service_properties_type Properties_username | Kasutajanimi, mida kasutatakse Dynamics 365-ga ühenduse loomiseks |

    Lisateavet vt järgmistest teemadest:

    - [Kasutage Resource Manager malli iga keskkonna puhul käsitsi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Lingitud teenuse atribuudid](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Andmete kopeerimine Azure Data Factory abil](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Pärast juurutamist valideerige andmevabriku andmekogumid, andmevoog ja lingitud teenus.

    ![Andmekogumid, andmevoog ja lingitud teenus.](media/data-factory-validate.png)

11. Minema **Halda**. Valige jaotises **Ühendused** väärtus **Lingitud teenus**. Seejärel valige **DynamicsCrmLinkedService**. Aastal **Redigeeri lingitud teenust (Dynamics CRM)** dialoogiboksi, sisestage järgmised väärtused.

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

## <a name="prepare-to-run-the-data-factory-templates"></a>Valmistuge Data Factory mallide käitamiseks

Selles jaotises kirjeldatakse häälestust, mis on vajalik enne osapoole postiaadressi ja osapoole elektroonilise aadressi andmetehase mallide käivitamist.

### <a name="setup-to-run-the-party-postal-address-template"></a>Seadistage Party postiaadressi malli käitamiseks

1. Logige sisse klientide kaasamise rakendustesse ja minge aadressile **Seaded** \> **Isikupärastamise seaded**. Seejärel, kohta **Kindral** vahekaardil konfigureerige süsteemiadministraatori konto ajavööndi seaded. Ajavöönd peab olema kooskõlastatud universaalajas (UTC), et värskendada Finance and Operationsi rakenduste postiaadresside kuupäevi "kehtiv alates" ja "kehtiv kuni".

    ![Süsteemiadministraatori konto ajavööndi seadistus.](media/ADF-1.png)

2. Andmetehases **Halda** sakk, all **Globaalsed parameetrid**, looge järgmine globaalne parameeter.

    | Number | Nimi | Tüüp | Väärtus |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | string | See parameeter lisab vastloodud postiaadressidele eesliitena seerianumbri. Sisestage kindlasti string, mis poleks vastuolus Finance and Operationsi ja klientide kaasamise rakenduste postiaadressidega. Näiteks kasutada **ADF-PAD-**. |

    ![Vahekaardil Halda loodud globaalne parameeter PostalAddressIdPrefix.](media/ADF-2.png)

3. Kui olete lõpetanud, valige **Avalda kõik**.

    ![Nupp Avalda kõik.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Seadistage peo elektroonilise aadressi malli käitamiseks

1. Andmetehases **Halda** sakk, all **Globaalsed parameetrid**, looge järgmised globaalsed parameetrid.

    | Number | Nimi | Tüüp | Väärtus |
    |---|---|---|---|
    | 1 | IsFOSource | bool | See parameeter määrab, millised esmased süsteemiaadressid konfliktide korral asendatakse. Kui väärtus on **tõsi**, asendavad peamised aadressid Finance and Operationsi rakendustes esmased aadressid klientide kaasamise rakendustes. Kui väärtus on **vale**, asendavad esmased aadressid klientide kaasamise rakendustes esmased aadressid rakendustes Finance and Operations. |
    | 2 | ElectronicAddressIdPrefix | string | See parameeter lisab vastloodud elektroonilistele aadressidele prefiksina seerianumbri. Sisestage kindlasti string, mis ei oleks vastuolus Finance and Operationsi ja klientide kaasamise rakenduste elektrooniliste aadressidega. Näiteks kasutada **ADF-EAD-**. |

    ![IsFOSource ja ElectronicAddressIdPrefix globaalsed parameetrid, mis on loodud vahekaardil Haldamine.](media/ADF-4.png)

2. Kui olete lõpetanud, valige **Avalda kõik**.

## <a name="run-the-templates"></a>Käivitage mallid

1. Lõpetage järgmine **Konto**, **ühendust**, ja **Müüja** topeltkirjutatavad kaardid, mis kasutavad rakendust Finance and Operations:

    + Kliendid V3 (kontod)
    + Kliendi V3 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + Hankija V2 (msdyn_vendor)

2. Veenduge, et kaardid eemaldatakse **msdy_dualwriteruntimeconfig** laud sisse Dataverse.
3. Installige [kahekirjutajalised osapoole ja globaalse aadressiraamatu lahendused](https://aka.ms/dual-write-gab) AppSource rakendusest.
4. Käivitage rakenduses Finance and Operations **Esialgne sünkroonimine** järgmiste tabelite jaoks, kui need sisaldavad andmeid:

    + Tervitused
    + Isiklikud märgitüübid
    + Viisakusväljend
    + Kontaktisiku tiitlid
    + Otsustamisrollid
    + Püsikliendi tasemed

5. Kliendi kaasamise rakenduses keelake järgmised pistikprogrammi toimingud.

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

    + Kliendiaadress

        + Loo

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: kliendiaadressi loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: kliendiaadressi värskendamine

        + Kustuta

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: kliendiaadressi kustutamine

    + msdyn_partypostaladdress

        + Loo

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdressi loomine
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdressi loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdressi värskendus
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdressi värskendus

    + msdyn_postiaadress

        + Loo

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdressi loomine
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdressi loomine
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdressi loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdressi värskendus
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdressi värskendus

    + msdyn_partyelectronicaddress

        + Loo

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddressi värskendus

        + Kustuta

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress kustutamine

6. Keelake kliendi kaasamise rakenduses järgmised töövood.

    + Hankijate loomine kontode tabelis
    + Hankijate loomine kontode tabelis
    + Isiku tüübiga hankijate loomine kontaktide tabelis
    + Isiku tüübiga hankijate loomine hankijate tabelis
    + Hankijate värskendamine kontode tabelis
    + Hankijate värskendamine hankijate tabelis
    + Isiku tüübiga hankijate värskendamine kontaktide tabelis
    + Isiku tüübiga hankijate värskendamine hankijate tabelis

7. Andmetehases käivitage mall, valides **Käivitage kohe** nagu on näidatud järgmisel joonisel. Sõltuvalt andmemahust võib selle protsessi lõpuleviimiseks kuluda paar tundi.

    ![Malli käivitamine.](media/data-factory-trigger.png)

    > [!NOTE]
    > Kui teil on kohandusi **Konto**, **ühendust**, ja **Müüja**, peate malli muutma.

8. Importige uus **Pidu** kirjed rakendusse Finance and Operations.

    1. Laadige alla **FONewParty.csv** fail Azure Blobi salvestusruumist. Tee on **partybootstrapping/output/FONewParty.csv**.
    2. Teisendage **FONewParty.csv** faili Exceli failiks ja importige Exceli fail rakendusse Finance and Operations. Kui CSV-importimine teie jaoks toimib, saate ka CSV-faili otse importida. Selle toimingu sooritamiseks võib olenevalt andmemahust kuluda paar tundi. Lisateavet vt [Andmete importimis- ja eksportimistööde ülevaade](../data-import-export-job.md).

    ![Importimine Dataverse Peo rekordid.](media/data-factory-import-party.png)

9. Andmetehases käivitage üksteise järel Partei postiaadressi ja Partei elektroonilise aadressi mallid.

    + Partei postiaadressi mall tühistab kliendi kaasamise rakenduses kõik postiaadressi kirjed ja seostab need vastavate **Konto**, **ühendust**, ja **Müüja** rekordid. Samuti genereerib see kolm CSV-faili: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv ja ImportFONewPostalAddress.csv.
    + Partei elektroonilise aadressi mall lisab kõik elektroonilised aadressid kliendi kaasamise rakenduses ja seostab need vastavate **Konto**, **ühendust**, ja **Müüja** rekordid. Samuti genereerib see ühe .csv-faili: ImportFONewElectronicAddress.csv.

    ![Partei postiaadressi ja partei elektroonilise aadressi mallide käitamine.](media/ADF-7.png)

10. Rakenduse Finance and Operations värskendamiseks nende andmetega peate teisendama .csv-failid Exceli töövihikuks ja [importige see rakendusse Finance and Operations](/data-entities/data-import-export-job). Kui CSV-importimine teie jaoks toimib, saate ka CSV-failid otse importida. Selle sammu lõpuleviimiseks võib olenevalt helitugevusest kuluda paar tundi.

    ![Edukas import.](media/ADF-8.png)

11. Lubage kliendi kaasamise rakenduses järgmised pistikprogrammi toimingud.

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

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdressi loomine
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdressi loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdressi värskendus
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdressi värskendus

    + msdyn_postiaadress

        + Loo

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdressi loomine
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdressi loomine
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdressi loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdressi värskendus
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdressi värskendus
 
    + msdyn_partyelectronicaddress

        + Loo

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress loomine

        + Värskendus

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddressi värskendus

        + Kustuta

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress kustutamine

12. Kui olete need varem inaktiveerinud, aktiveerige kliendi kaasamise rakenduses järgmised töövood.

    + Hankijate loomine kontode tabelis
    + Hankijate loomine kontode tabelis
    + Isiku tüübiga hankijate loomine kontaktide tabelis
    + Isiku tüübiga hankijate loomine hankijate tabelis
    + Hankijate värskendamine kontode tabelis
    + Hankijate värskendamine hankijate tabelis
    + Isiku tüübiga hankijate värskendamine kontaktide tabelis
    + Isiku tüübiga hankijate värskendamine hankijate tabelis

13. Käivitage **Pidu** rekordiga seotud kaardid, nagu on kirjeldatud punktis [Partei ja globaalne aadressiraamat](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Data Factory mallide selgitus

See jaotis viib teid läbi iga Data Factory malli toimingud.

### <a name="steps-in-the-party-template"></a>Sammud Party mallis

1. Sammudes 1–6 tehakse kindlaks ettevõtted, millel on kahekordne kirjutamine lubatud, ja luuakse nende jaoks filtriklausel.
2. Sammudes 7-1 kuni 7-9 hangitakse andmed nii rakendusest Finance and Operations kui ka kliendi kaasamise rakendusest ning viiakse need andmed täiendamiseks etapiviisiliselt.
3. Sammudes 8–9 võrrelge peonumbrit **Konto**, **ühendust**, ja **Müüja** kirjed rakenduse Finance and Operations ja kliendi kaasamise rakenduse vahel. Kõik kirjed, millel pole peonumbrit, jäetakse vahele.
4. Samm 10 loob kaks CSV-faili osapoole kirjete jaoks, mis tuleb luua kliendi kaasamise rakenduses ja rakenduses Finance and Operations.

    - **FOCDSParty.csv** – See fail sisaldab mõlema süsteemi kõiki osapoolte kirjeid, olenemata sellest, kas ettevõttel on kahekordne kirjutamine lubatud.
    - **FONewParty.csv** – See fail sisaldab osapoole kirjete alamhulka, mis Dataverse on teadlik (näiteks kontodest **Väljavaade** tüüp).

5. 11. samm loob osapooled kliendi kaasamise rakenduses.
6. 12. samm hangib kliendi kaasamise rakendusest osapoolte globaalselt kordumatud identifikaatorid (GUID-id) ja etapiviisiliselt neid saab seostada **Konto**, **ühendust**, ja **Müüja** salvestab järgmistes etappides.
7. Samm 13 seostab **Konto**, **ühendust**, ja **Müüja** parteide GUID-idega kirjed.
8. Sammud 14-1 kuni 14-3 värskendavad **Konto**, **ühendust**, ja **Müüja** salvestab osapoolte GUID-idega kliendi kaasamise rakenduses.
9. Etappide 15-1 kuni 15-3 ettevalmistamine **Võtke peoga ühendust** rekordid **Konto**, **ühendust**, ja **Müüja** rekordid.
10. Sammud 16-1 kuni 16-7 toovad viiteandmed, nagu tervitused ja isiklikud märgitüübid, ning seostavad need **Võtke peoga ühendust** rekordid.
11. Samm 17 liidab **Võtke peoga ühendust** rekordid **Konto**, **ühendust**, ja **Müüja** rekordid.
12. Samm 18 impordib **Võtke peoga ühendust** salvestab kliendi kaasamise rakendusse.

### <a name="steps-in-the-party-postal-address-template"></a>Partei postiaadressi malli sammud

1. Sammudes 1–1 kuni 1–10 hangitakse andmed nii rakendusest Finance and Operations kui ka kliendi kaasamise rakendusest ning viiakse need andmed täiendamiseks etapiviisiliselt.
2. 2. toiming denormaliseerib postiaadressi andmed rakenduses Finance and Operations, ühendades postiaadressi ja osapoole postiaadressi.
3. 3. samm eemaldab ja liidab kliendi kaasamise rakendusest konto, kontakti ja hankija aadressi andmed.
4. 4. toiming loob rakenduse Finance and Operations jaoks csv-failid, et luua uued aadressiandmed, mis põhinevad konto, kontakti ja hankija aadressidel.
5. Samm 5-1 loob kliendi kaasamisrakenduse jaoks csv-failid, et luua kõik aadressiandmed, mis põhinevad nii rakendusel Finance and Operations kui ka kliendi kaasamise rakendusel.
6. Samm 5-2 teisendab CSV-failid käsitsi importimiseks Finance and Operationsi impordivormingusse.

    - ImportFOUusPostalAddressLocation.csv
    - ImportFOUuusPartyPostalAddress.csv
    - ImportFOUusPostalAddress.csv

7. 6. toiming impordib postiaadressi kogumise andmed kliendi kaasamise rakendusse.
8. 7. toimingus hangitakse kliendi kaasamise rakendusest postiaadressi kogumise andmed.
9. Samm 8 loob kliendi aadressiandmed ja seostab postiaadressi kogumise ID.
10. Sammud 9-1 kuni 9-2 seotud osapoolte ja postiaadresside kogumise ID-d koos postiaadresside ja osapoolte postiaadressidega.
11. Sammud 10-1 kuni 10-3 importige klientide kaasamise rakendusse klientide aadressid, postiaadressid ja osapoolte postiaadressid.

### <a name="steps-in-the-party-electronic-address-template"></a>Partei elektroonilise aadressi malli sammud

1. Sammudes 1–1 kuni 1–5 hangitakse andmed nii rakendusest Finance and Operations kui ka kliendi kaasamise rakendusest ning viiakse need andmed täiendamiseks etapiviisiliselt.
2. 2. samm koondab kliendi kaasamise rakenduses konto, kontakti ja hankija üksuste elektroonilised aadressid.
3. 3. samm liidab esmased elektroonilised aadressiandmed kliendi kaasamise rakendusest ja rakendusest Finance and Operations.
4. 4. toiming loob .csv-failid.

    - Looge rakenduse Finance and Operations jaoks uued elektroonilised aadressiandmed konto, kontakti ja hankija aadresside põhjal.
    - Looge kliendi kaasamise rakenduse jaoks uued elektroonilised aadressiandmed, mis põhinevad rakenduses Finance and Operations elektroonilisel aadressil, kontol, kontakt- ja hankija aadressidel.

5. Samm 5-1 impordib elektroonilised aadressid kliendi kaasamise rakendusse.
6. Samm 5-2 loob CSV-failid, et värskendada kliendi kaasamise rakenduses olevate kontode ja kontaktide peamisi aadresse.
7. Sammud 6-1 kuni 6-2 importige kontod ja kontaktandmed esmased aadressid kliendi kaasamise rakendusse.

## <a name="troubleshooting"></a>Tõrkeotsing

1. Kui protsess ebaõnnestub, käivitage andmetehas uuesti. Alusta ebaõnnestunud tegevusest.
2. Mõnda andmetehase poolt loodud faile saab kasutada andmete kontrollimiseks.
3. Andmete tehas töötab .csv-failide põhjal. Seega, kui mis tahes välja väärtus sisaldab koma, võib see tulemusi segada. Peate välja väärtustest eemaldama kõik komad.
4. The **Järelevalve** vahekaart sisaldab teavet kõigi töödeldud sammude ja andmete kohta. Valige selle silumiseks kindel juhis.

    ![Jälgimise vahekaart.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Lisateave malli kohta

Malli kohta lisateabe saamiseks vt [Kommentaarid Azure Data Factory malli readme kohta](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
