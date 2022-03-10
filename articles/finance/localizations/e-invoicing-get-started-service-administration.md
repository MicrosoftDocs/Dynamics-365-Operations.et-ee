---
title: Elektroonilise arvelduse teenusehaldusega alustamine
description: Selles teemas selgitatakse, kuidas elektroonilise arveldusega alustada.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f77c8fd1696b74f852d04cc0a696d4816ef9af1f
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/23/2022
ms.locfileid: "7984824"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Elektroonilise arvelduse teenusehaldusega alustamine

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Eeltingimused

Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused.

- Teil peab olema juurdepääs oma Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kontole.
- Teil peab olema LCS-projekt, mis hõlmab Microsofti teenuste Dynamics 365 Finance või Dynamics 365 Supply Chain Management versiooni 10.0.17 või uuemat versiooni. Peale selle peavad need rakendused olema juurutatud ühes järgmistest Azure'i geograafilistest piirkondadest.

    - Ameerika Ühendriigid
    - Euroopa
    - Ühendkuningriik
    - Aasia

- Teil peab olema juurdepääs oma Dynamics 365 teenuse Regulatory Configuration Services (RCS) kontole.
- Te peate mooduli Funktsioonihaldus kaudu oma RCS-i konto jaoks globaliseerimisfunktsiooni aktiveerima. Lisateavet vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).
- Peate looma Azure'is võtmehoidla ja salvestamiskonto. Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Installi Lifecycle Services-is lisandmodul mikroteenuste jaoks

1. Logige sisse oma LCS-i kontole ja valige LCS-i projekti juhtpaneelil LCS-i projekt.
2. Valige projektis **Keskkonnad** armatuurlaual oma juurutatud keskkond. Teie valitud keskkond peab töötama.
3. Valige **Power Platform Integratsioon** vahekaardil **Keskkonna lisandmoodulid** väljagrupis **Installi uus lisandmoodul**.
4. Valige **Elektrooniline arveldamine**.
5. Väljale **AAD-rakenduse ID** sisestage **091c98b0-a1c9-4b02-b62c-7753395ccabe**. See väärtus ei muutu.
6. Sisestage väljale **AAD rentniku ID** oma Azure'i tellimuse konto ID. Teie Azure Active Directory (Azure AD) rentnik peaks olema sama rentnik, mida kasutatakse RCS-is.
7. Tingimustega nõustumiseks valige märkeruut.
8. Valige **Installi**. Install võib kesta kuni mitu minutit.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Määrake parameetrid RCS integratsioonile koos Elekrtoonilise arveldusega

1. Logige oma RCS-i kontole sisse.
2. Tööruumi **Globaliseerimisfunktsioonid** jaotisest **Seotud sätted** valige **Elektroonilise aruandluse parameetrid**.
3. Sisestage vahekaardil **E-arveldus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.

    | Azure'i andmekeskuse geograafiline piirkond | Teenuse lõpp-punkti URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Ameerika Ühendriigid              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Euroopa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Ühendkuningriik             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Aasia                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Veenduge, et välja **Rakenduse ID** väärtuseks oleks määratud **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. See väärtus ei muutu.
5. Väljale **LCS-i keskkonna id** sisestage oma LCS-i keskkonna ID.
6. Valige **Salvesta** ja sulgege seejärel leht.

## <a name="create-key-vault-references"></a>Võtmehoidla viite loomine

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige paan **Elektrooniline arveldus**.
3. Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Teenusekeskkond** ja seejärel valige **Võtmehoidla parameetrid**.
4. Võtmehoidla viite loomiseks valige **Uus**.
5. Väljale **Nimi** sisestage võtmehoidla viite nimi. Väljale **Kirjeldus** sisestage kirjeldus.
6. Väljale **Võtmehoidla URL** kleepige võtmehoidja saladus Azure'i võtmehoidlast. Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).
7. Valige käsk **Salvesta**.

## <a name="create-storage-account-secret"></a>Salvestuskonto saladuse loomine

1. Lehel **Keskkonna häälestus** Tegevuspaanil, valige **Teenusekeskkond** > **Võtmehoidla parameetrid**.
2. Valige **Võtmehoidla viide** ja jaotisest **Sertifikaadid** valige **Lisa**.
3. Väljal **Nimi** sisesta salvestuskonto saladuse nimi. Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Väljalt **Tüüp** valige **Vali**.
6. Valige **Salvesta** ja sulgege seejärel leht.

## <a name="create-a-digital-certificate-secret"></a>Digitaalserdi saladuse loomine

1. Lehelt **Keskkonna seadistused** tegevuspaanil valige **Teenusekeskkond** ja seejärel valige **Võtmehoidla parameetrid**.
2. Valige **Võtmehoidla viide** ja seejärel jaotisest **Sertifikaadid** valige **Lisa**.
3. Väljal **Nimi** sisestage digitaalse sertifikaadi saladuse nimi. Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Tehke väljal **Tüüp** valik **Sertifikaat**.
6. Valige **Salvesta** ja sulgege seejärel leht.

## <a name="create-a-service-environment"></a>Teenusekeskkonna loomine

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige paan **Elektrooniline arveldus**.
3. Lehel **Keskkondade seadistused** valige toimingupaanil suvand **Teenusekeskkond**.
4. Valige uue teenusekeskkonna loomiseks **Uus**.
5. Sisestage väljale **Nimi** e-arvelduse keskkonna nimi. Väljale **Kirjeldus** sisestage kirjeldus.
6. Valige väljal **Salvestuskonto SAS-tõendi saladus** salvestuskonto juurdepääsu autentimiseks kasutatava serdi nimi.
7. Valige jaotises **Kasutajad** käsk **Lisa**, et lisada kasutaja, kellel on lubatud keskkonna kaudu elektroonilisi arveid edastada ning salvestuskontoga ühendus luua.
8. Sisestage väljale **Kasutaja ID** kasutaja pseudonüüm. Sisestage väljale **E-post** kasutaja e-posti aadress.
9. Valige käsk **Salvesta**.
10. Kui teie riigi-/regioonipõhiste arvete puhul on digiallkirjade rakendamiseks vaja serdiahelat, valige toimingupaanil suvand **Võtmehoidla parameetrid** ja seejärel valige **Serdiahel** ning toimige järgmiselt.

    1. Serdiahela loomiseks valige **Uus**.
    2. Sisestage väljale **Nimi** serdiahela nimi. Väljale **Kirjeldus** sisestage kirjeldus.
    3. Valige jaotises **Serdid** käsk **Lisa**, et ahelale sert lisada.
    4. Kasutage nuppu **Üles** või **Alla**, et ahelas serdi asukohta muuta.
    5. Valige **Salvesta** ja sulgege seejärel leht.
    6. Sulgege leht.

11. Valige lehe **Teenusekeskkond** toimingupaanil käsk **Avalda**, et keskkond pilves avaldada. Välja **Olek** väärtuseks määratakse **Avaldatud**.

## <a name="create-a-connected-application"></a>Ühendatud rakenduse loomine

1. Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Ühendatud rakendused**.
2. Valige ühendatud rakenduse loomiseks **Uus**.
3. Sisestage väljale **Nimi** ühendatava rakenduse nimi.
4. Sisestage väljale **Rakendus** ühendatava teenuse Finance ja Supply Chain Management keskkonna URL.
4. Sisestage väljale **Rentnik** ühendatava teenuse Finance ja Supply Chain Management keskkonna rentnik.
5. Valige käsk **Salvesta**.
6. Keskkonnaga lodud ühenduse testimiseks valige toimingupaanil käsk **Kontrolli ühendust**. Seejärel sulgege leht.

## <a name="link-connected-applications-to-environments"></a>Ühendatud rakenduste keskkondadega linkimine

1. Valige lehel **Keskkondade seadistused** suvand **Uus**, et ühendatud rakendus keskkonnale määrata.
2. Valige väljal **Ühendatud rakendus** ühendatud rakendus.
3. Valige väljal **Teenusekeskkond** teenusekeskkond.
4. Valige **Salvesta** ja sulgege seejärel leht.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Elektroonilise arvelduse integratsiooni seadistamine Finantsis ja Supply Chain Management -is

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Elektroonilise arvelduse integratsioonifunktsiooni sisselülitamine

1. Logige oma teenuse Finance või Supply Chain Management eksemplari sisse.
2. Tööruumis **Funktsioonihaldus** otsige üles funktsioon **Elektroonilise arvelduse integratsioon**. Kui seda funktsiooni lehel ei kuvata, valige käsk **Kontrolli värskendusi**.
3. Valige funktsioon ja seejärel valige **Luba kohe**.

### <a name="set-up-the-service-endpoint-url"></a>Teenuse lõpp-punkti URL-i seadistamine

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Sisestage vahekaardil **E-arveldus** väljale **Lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.

    | Azure'i andmekeskuse geograafiline piirkond | Teenuse lõpp-punkti URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Ameerika Ühendriigid              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Euroopa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Ühendkuningriik             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Aasia                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Väljale **Keskkond** sisestage teenusekeskkonna nimi, mis on avaldatud Elektroonilises arvelduses.
4. Valige **Salvesta** ja sulgege seejärel leht.

### <a name="enable-flighting-keys-for-finance-or-supply-chain-management-version-10017"></a>Lubage Flighting võtmed Finance jaoks või Supply Chain Management versioon 10.0.17

1. Käivitage järgmine SQL-i käsk.

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Käivitage käsk IISreset kõigi AOS-ite jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
