---
title: Elektroonilise arvelduse lisandmooduli teenuse halduse kasutamise alustamine
description: Selles teemas selgitatakse, kuidas elektroonilise arvelduse lisandmooduli kasutamist alustada.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104368"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Elektroonilise arvelduse lisandmooduli teenuse halduse kasutamise alustamine

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Eeltingimused

Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused.

- Teil peab olema juurdepääs oma Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kontole.
- Teil peab olema LCS-projekt, mis hõlmab Microsofti teenuste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management versiooni 10.0.13 või uuemat versiooni. Peale selle peavad need rakendused olema juurutatud ühes järgmistest Azure'i geograafilistest piirkondadest.

    - Ida-USA
    - Lääne-USA
    - Põhja-EL
    - Lääne-EL

- Teil peab olema juurdepääs oma Dynamics 365 teenuse Regulatory Configuration Services (RCS) kontole.
- Te peate mooduli Funktsioonihaldus kaudu oma RCS-i konto jaoks globaliseerimisfunktsiooni aktiveerima. Lisateavet vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).
- Peate looma Azure'is võtmehoidla ja salvestamiskonto. Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Teenuses Lifecycle Services mikroteenuste jaoks lisandmooduli installimine

1. Logige oma LCS-i kontole sisse.
2. Valige paan **Eelvaate funktsiooni haldamine**.
3. Valige jaotises **Avaliku eelvaateversiooni funktsioonid** suvand **E-arvelduse teenus**.
4. Veenduge, et suvandi **Funktsiooni eelversioon on lubatud** väärtuseks oleks valitud **Jah**.

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>RCS-i elektroonilise arvelduse lisandmooduliga integratsiooni parameetrite seadistamine

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** valige suvand **Elektroonilise aruandluse parameetrid**.
3. Sisestage vahekaardil **E-arvelduse teenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.

    | Azure'i andmekeskuse geograafiline piirkond | Teenuse lõpp-punkti URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Ida-USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Lääne-USA                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Põhja-EL                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Lääne-EL                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Veenduge, et välja **Rakenduse ID** väärtuseks oleks määratud **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. See väärtus ei muutu.
5. Sisestage väljale **LCS-i keskkonna ID** oma LCS-i tellimuse konto ID.
6. Valige **Salvesta** ja sulgege seejärel leht.

## <a name="create-key-vault-secret"></a>Võtmehoidla saladuse loomine

1. Logige oma RCS-i kontole sisse.
2. Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkonnad** paan **E-arveldus**.
3. Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Teenusekeskkond** ja seejärel valige **Võtmehoidla parameetrid**.
4. Võtmehoidla saladuse loomiseks valige **Uus**.
5. Sisestage väljale **Nimi** võtmehoidla saladuse nimi. Väljale **Kirjeldus** sisestage kirjeldus.
6. Kleepige väljale **Võtmehoidla URL** Azure'i võtmehoidlast saladus.
7. Valige käsk **Salvesta**.

## <a name="create-storage-account-secret"></a>Salvestuskonto saladuse loomine

1. Valige lehe **Võtmehoidla parameetrid** jaotises **Sertifikaadid** käsk **Lisa**.
2. Sisestage väljale **Nimi** sama salvestuskonto saladus. Väljale **Kirjeldus** sisestage kirjeldus.
3. Tehke väljal **Tüüp** valik **Sertifikaat**.
4. Valige **Salvesta** ja sulgege seejärel leht.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Elektroonilise arvelduse lisandmooduli keskkonna loomine

1. Logige oma RCS-i kontole sisse.
2. Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkonnad** paan **E-arveldus**.

## <a name="create-a-service-environment"></a>Teenusekeskkonna loomine

1. Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Teenusekeskkond**.
2. Valige uue teenusekeskkonna loomiseks **Uus**.
3. Sisestage väljale **Nimi** e-arvelduse keskkonna nimi. Väljale **Kirjeldus** sisestage kirjeldus.
4. Valige väljal **Salvestuskonto SAS-tõendi saladus** salvestuskonto juurdepääsu autentimiseks kasutatava serdi nimi.
5. Valige jaotises **Kasutajad** käsk **Lisa**, et lisada kasutaja, kellel on lubatud keskkonna kaudu elektroonilisi arveid edastada ning salvestuskontoga ühendus luua.
6. Sisestage väljale **Kasutaja ID** kasutaja pseudonüüm. Sisestage väljale **E-post** kasutaja e-posti aadress.
7. Valige käsk **Salvesta**.
8. Kui teie riigi-/regioonipõhiste arvete puhul on digiallkirjade rakendamiseks vaja serdiahelat, valige toimingupaanil suvand **Võtmehoidla parameetrid** ja seejärel valige **Serdiahel** ning toimige järgmiselt.

    1. Serdiahela loomiseks valige **Uus**.
    2. Sisestage väljale **Nimi** serdiahela nimi. Väljale **Kirjeldus** sisestage kirjeldus.
    3. Valige jaotises **Serdid** käsk **Lisa**, et ahelale sert lisada.
    4. Kasutage nuppu **Üles** või **Alla**, et ahelas serdi asukohta muuta.
    5. Valige **Salvesta** ja sulgege seejärel leht.
    6. Sulgege leht.
9. Valige lehe **Teenusekeskkond** toimingupaanil käsk **Avalda**, et keskkond pilves avaldada. Välja **Olek** väärtuseks määratakse **Avaldatud**.

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

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine teenustes Finance ja Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Elektroonilise arvelduse lisandmooduli integratsioonifunktsiooni sisselülitamine

1. Logige oma teenuse Finance või Supply Chain Management eksemplari sisse.
2. Otsige tööruumis **Funktsioonihaldus** üles funktsioon **Elektroonilise arvelduse lisandmooduli integratsioon**. Kui seda funktsiooni lehel ei kuvata, valige käsk **Kontrolli värskendusi**.
3. Valige funktsioon ja seejärel valige **Luba kohe**.

### <a name="set-up-the-service-endpoint-url"></a>Teenuse lõpp-punkti URL-i seadistamine

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Sisestage vahekaardil **Edastusteenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.

    | Azure'i andmekeskuse geograafiline piirkond | Teenuse lõpp-punkti URL                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Ida-USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Lääne-USA                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Põhja-EL                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Lääne-EL                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Sisestage väljale **Keskkond** elektroonilise arvelduse lisandmooduli keskkonna nimi.
4. Valige **Salvesta** ja sulgege seejärel leht.
