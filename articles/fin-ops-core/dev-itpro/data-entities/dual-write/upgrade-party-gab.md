---
title: Üleminek osapoole ja globaalse aadressiraamatu mudelile
description: See teema kirjeldab, kuidas uuendada kahekirjutajalisi andmeid osalise ja globaalse aadressiraamatu mudelile.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857366"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Üleminek osapoole ja globaalse aadressiraamatu mudelile

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Azure'i andmetehase mall](https://aka.ms/dual-write-gab-adf) aitab teil täiendada olemasolevaid tabelite **Konto**, **Kontakt** ja **Hankija** andmeid kahekirjutamisel osapoole ja globaalse aadressiraamatu mudelile. Mall sobitab nii Finance and Operations rakenduste kui ka kliendikaasamise rakenduste andmed. Protsessi lõpus luuakse **osapoole** kirjete **osapoole**- ja **kontakti** väljad ning seostatakse need kliendikaasamise rakenduste kirjetega **Konto**, **Kontakt** ja **Hankija**. Finance and Operations rakenduses uute **osapoole** kirjete loomiseks luuakse .csv fail (`FONewParty.csv`).  Selles teemas on juhised malli Data Factory malli kasutamiseks ja andmete täiendamiseks.

Kui teil kohandusi pole, saate malli kasutada nii, nagu see on. Kui teil on kohandusi kirjetes **Konto**, **Kontakt** ja **Hankija**, peate malli muutma järgmiste juhiste abil.

> [!Note]
> Mall aitab uuendada ainult **osapoole** andmeid. Tulevases väljaandes lisatakse posti- ja elektroonilised aadressid.

## <a name="prerequisites"></a>Eeltingimused

Järgmised eeldused on vajalikud.

+ [Azure'i tellimus](https://portal.azure.com/)
+ [Juurdepääs mallile](https://aka.ms/dual-write-gab-adf)
+ Olete olemasolev topeltkirjutamise klient.

## <a name="prepare-for-the-upgrade"></a>Täienduseks ettevalmistamine

+ **Täielikult sünkroonitud**: mõlemas keskkonnas on kirjed **Konto (klient)**, **Kontakt** ja **Hankija** täielikult sünkroonitud olekuga.
+ **Integratsioonivõtmed**: kliendikaasamise rakenduste tabeleid **Konto (klient)**, **Kontakt** ja **Hankija** kasutavad väljaminekuks saadetud integratsioonivõtmeid. Kui kohandasite integratsioonivõtmeid, peate malli kohandama.
+ **Osapoole number**: kõigil täiendamisele minevatel kirjetel **Konto (Klient)**, **Kontakt** ja **Hankija** on **osapoole number**. **Osapoole** numbrita kirjeid ignoreeritakse. Kui soovite neid kirjeid täiendada, lisage neile enne täiendusprotsessi alustamist **osapoole** number.
+ **Süsteemi katkestus**: versiooniuuendusprotsessi ajal peate kasutama nii Finance and Operations ja kliendikaasamise keskkondi võrguühenduseta.
+ **Hetktõmmis**: tehke hetktõmmiseid nii klientide kaasamise kui ka Finance and Operations rakendustest. Kasutage vajadusel hetktõmmiseid eelmise oleku taastamiseks.

## <a name="deployment"></a>Juurutamine

1. Laadige mall alla rakendusest [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. Logige sisse rakendusse [Microsoft Azure](https://portal.azure.com/).

3. Looge [ressursigrupp](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Looge loodud ressursirühmas [talletuskonto](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal).

5. Looge ülal loodud ressursirühmas [andmevabrik](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal).

6. Avage andmevabrik ja valige paan **Autor ja monitor**.

7. Klõpsake menüüs **Haldamine** nuppu **ARM-mall**.

8. **Osapoole** malli importimiseks valige **Impordi ARM mall**.

9. Importige mall andmevabrikusse. Sisestage **projekti üksikasjade** ja **eksemplari üksikasjade** jaoks järgmised väärtused.

    Field | Väärtus
    ---|---
    Kordustellimus | Azure'i tellimus
    Ressursigrupp | Sisestage sama ressurss, mille all salvestusruumikonto luuakse.
    Regioon | Määrake piirkond.
    Vabriku nimi | Määrake vabriku nimi.
    FO lingitud Service_service põhivõti | Määrake rakenduse võti.
    Azure Blobi Storage_connection string | Azure Blobi hoidla ühenduse string.
    Dynamics Crm-iga lingitud Service_password | Kasutajanimeks määratud kasutajakonto parool.
    FO lingitud Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO lingitud Service_properties_type Properties_tenant | Määrake üürniku teave (domeeninimi või üürniku ID), mille all teie rakendus asub.
    FO lingitud Service_properties_type Properties_aad resursi ID | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO lingitud Service_properties_type Properties_service põhi-ID | Määrake rakenduse kliendi ID.
    Dynamics Crm-iga lingitud Service_properties_type Properties_username | Kasutajanimi Dynamicsiga ühenduse loomiseks.

    Lisateavet leiate teemast [Ressursihalduri malli käsitsi reklaamimine iga keskkonna jaoks ](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Lingitud teenuse atribuudid ](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties)ja [Andmete kopeerimine Azure'i andmevabriku abil](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Pärast juurutamist valideerige andmevabriku andmekogumid, andmevoog ja lingitud teenus.

   ![Andmekogumid, andmevoog ja lingitud teenus](media/data-factory-validate.png)

11. Liikuge jaotisse **Haldamine**. Valige jaotises **Ühendused** väärtus **Lingitud teenus**. Valige **DynamicsCrmLinkedService**. Sisestage vormil **Lingitud teenuse redigeerimine (Dynamics CRM)** järgmised väärtused.

    Field | Väärtus
    ---|---
    Nimi | DynamicsCrmLinkedService
    Kirjeldus | Lingitud teenused CRM-i eksemplariga ühenduse loomiseks olemite andmete toomiseks
    Ühenduse loomine integratsiooni käitusaja kaudu | AutoResolvelntegrationRuntime
    Juurutamistüüp | Võrgus
    Teenuse Uri | `https://<organization-name>.crm[x].dynamics.com`
    Autentimise tüüp | Office365
    Kasutajanimi |
    Parool või Azure'i võtmehoidla | Parool
    Parool |

## <a name="run-the-template"></a>Käitage mall

1. Finance and Operations rakenduse abil saate peatada järgmiste **konto**, **kontakti** ja **hankija** topeltkirjutamise.

    + Kliendid V3 (kontod)
    + Kliendi V3 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + CDS'i kontakti V2 (kontaktid)
    + Hankija V2 (msdyn_vendor)

2. Veenduge, et kaardid on Dataverse tabelist `msdy_dualwriteruntimeconfig` eemaldatud.

3. Installige [kahekirjutajalised osapoole ja globaalse aadressiraamatu lahendused](https://aka.ms/dual-write-gab) AppSource rakendusest.

4. Kui Finance and Operations rakenduses sisaldavad andmeid järgmised tabelid, käivitage nende jaoks **esmane sünkroonimine**.

    + Tervitused
    + Isiklikud märgitüübid
    + Viisakusväljend
    + Kontaktisiku tiitlid
    + Otsustamisrollid
    + Püsikliendi tasemed

5. Keelake kliendi kaasamise rakenduses järgmised plugina juhised.

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

6. Keelake kliendi kaasamise rakenduses järgmised töövood.

    + Hankijate loomine kontode tabelis
    + Hankijate loomine kontode tabelis
    + Isiku tüübiga hankijate loomine kontaktide tabelis
    + Isiku tüübiga hankijate loomine hankijate tabelis
    + Hankijate värskendamine kontode tabelis
    + Hankijate värskendamine hankijate tabelis
    + Isiku tüübiga hankijate värskendamine kontaktide tabelis
    + Isiku tüübiga hankijate värskendamine hankijate tabelis

7. Käivitage mall andmevabrikus, valides käsu **Käivita kohe**, nagu on näidatud järgmisel pildil. Selle protsessi lõpuleviimiseks võib andmemahu põhjal kuluda mõni tund.

    ![Päästiku käivitamine](media/data-factory-trigger.png)

    > [!NOTE]
    > Kui teil on kohandusi kirjetes **Konto**, **Kontakt** ja **Hankija**, peate malli muutma.

8. Importige rakenduses Finance and Operations uued **osapoole** kirjed.

    + Laadige `FONewParty.csv` fail alla Azure'i bloobimälust. Vorming on `partybootstrapping/output/FONewParty.csv`.
    + Teisendage `FONewParty.csv` fail Exceli failiks ja importige Exceli fail Finance and Operations rakendusse.  Kui CSV import töötab teie jaoks, saate importida CSV faili otse. Sõltuvalt andmemahust võib importimiseks kuluda mõni tund. Lisateavet vt [Andmete importimis- ja eksportimistööde ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).

    ![Dataversi osapoole kirjete importimine](media/data-factory-import-party.png)

9. Lubage kliendi kaasamise rakenduses järgmised plugina juhised.

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

10. Aktiveerige kliendikaasamise rakendustes järgmised töövood, kui desaktiveerisite need eelmistes juhistes.

    + Hankijate loomine kontode tabelis
    + Hankijate loomine kontode tabelis
    + Isiku tüübiga hankijate loomine kontaktide tabelis
    + Isiku tüübiga hankijate loomine hankijate tabelis
    + Hankijate värskendamine kontode tabelis
    + Hankijate värskendamine hankijate tabelis
    + Isiku tüübiga hankijate värskendamine kontaktide tabelis
    + Isiku tüübiga hankijate värskendamine hankijate tabelis

11. Käivitage **osapoolega** seotud kaardid, nagu on juhendatud [osapoole- ja globaalses aadressiraamatus](party-gab.md).

## <a name="troubleshooting"></a>Tõrkeotsing

1. Kui protsess ebaõnnestub, käivitage vabrik uuesti, alustades ebaõnnestunud tegevusest.
2. Mõned failid loob andmevabrik, mida saate kasutada andmete valideerimise eesmärgil.
3. Andmevabrik töötab komaeraldusega CSV-failide põhjal. Kui on välja väärtus, millel on koma, võib see tulemusi häirida. Te peate komad eemaldama.
4. Vahekaart **Jälgimine** sisaldab teavet kõigi töödeldavate toimingute ja andmete kohta. Valige selle silumiseks kindel juhis.

    ![Vahekaart Jälgimine](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Lisateave malli kohta

Leiate [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) faili kohta kommentaare.
