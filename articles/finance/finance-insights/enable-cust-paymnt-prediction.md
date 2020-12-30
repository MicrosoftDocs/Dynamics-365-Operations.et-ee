---
title: Kliendimaksete prognoosimise lubamine (eelversioon)
description: Selles teemas selgitatakse, kuidas lülitada sisse ja konfigureerida finantsülevaadetes kliendimakse prognooside funktsioon.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644989"
---
# <a name="enable-customer-payment-predictions-preview"></a>Kliendimaksete prognoosimise lubamine (eelversioon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas selgitatakse, kuidas lülitada sisse ja konfigureerida finantsülevaadetes kliendimakse prognooside funktsioon. Te lülitate funktsiooni tööruumis **Funktsioonihaldus** sisse ja sisestate konfiguratsiooni sätted lehel **Finantsülevaadete parameetrid**. See teema sisaldab ka teavet, mis võib aidata teil funktsiooni tõhusalt kasutada.

> [!NOTE]
> Enne järgmiste etappide täitmist täitke kindlasti eeltingimuse etapid jaotises [Finantsülevaadete konfigureerimine](configure-for-fin-insites.md).

1. Kasutage teavet teenuse Microsoft Dynamics Lifecycle Services (LCS) lehelt, et ühendada Azure SQL-i esmane eksemplar selle keskkonnaga. Käivitage järgmine Transact-SQL (T-SQL) käsk, et lülitada liivakasti keskkonna eelväljaanded sisse. (Enne rakendusobjekti serveriga \[AOS\] eemalt ühenduse loomist võib olla vajalik, et peate LCS-is lülitama oma IP-aadressi juurdepääsu sisse.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > Kui teie Microsoft Dynamics 365 Finance on Service Fabricu juurutus, saate selle sammu vahele jätta. Finantsülevaadete meeskond peaks olema väljaande juba teie jaoks sisse lülitanud. Kui te funktsiooni tööruumis **Funktsioonihaldus** ei näe või kui selle sisselülitamisel esineb probleeme, võtke ühendust aadressil <fiap@microsoft.com>.

2. Kliendimaksete ülevaadete funktsiooni sisselülitamine.

    1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
    2. Leidke funktsioon, mille nimi on **Kliendimakse ülevaated (eelversioon)**.
    3. Valige **Luba kohe**.

    Kliendimakse ülevaadete funktsioon on nüüd sisse lülitatud ja konfigureerimiseks valmis.

3. Kliendimaksete ülevaadete funktsiooni konfigureerimine.

    1. Avage suvand **Krediidihaldus ja võlanõuded \> Seadistamine \> Finantsülevaated \> Finantsülevaadete parameetrid**.

        [![Finantsteabe parameetrite leht enne funktsiooni konfigureerimist](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Valige lehel **Finantsülevaadete parameetrid** vahekaardil **Kliendimaksete ülevaated** link **Prognoosimudelis kasutatavate andmeväljade kuvamine**, et avada leht **Prognoosimudeli andmeväljad**. Siin saate vaadata väljade vaikeloendit, mida kasutatakse kliendimaksete prognooside jaoks tehisintellekti (AI) prognoosimismudeli loomiseks.

        Prognoosimudeli loomiseks väljade vaikeloendi kasutamiseks sulgege leht **Prognoosimudeli andmeväljad** ja määrake seejärel lehel **Finantsülevaadete parameetrid** suvand **Funktsiooni lubamine** valikule **Jah**.

    3. Määrake väga hilise kande periood, et määratleda, mida tähendab teie ettevõtte jaoks prognoosisalv **Väga hilja**.

        Iga avatud arve puhul ennustab süsteem makse tõenäosuse kolme salve seast: **õigel ajal**, **hilja** ja **väga hilja**.

        - **Õigel ajal** – see salv hõlmab makseid, mida prognoositakse, et makstakse kande tähtajal või enne seda.
        - **Hilja** – see salv hõlmab makseid, mille maksmine prognoositakse pärast kande tähtaega, kuid enne kande perioodi „väga hilja” algamist.
        - **Väga hilja** – see salv hõlmab makseid, mille maksmine prognoositakse pärast kande perioodi „väga hilja” algamist.

        > [!NOTE]
        > Kui muudate kande perioodi „väga hilja” ja valite suvandi **Hilise lävendi muutmine** pärast seda, kui tehisintellekti prognoosimise mudel on kliendimaksete jaoks on loodud, olemasolev prognoosimise mudel kustutatakse ja luuakse uus mudel. Uus prognoosimise mudel teisaldab kanded perioodile „väga hilja”, mis põhineb selle määratlemiseks sisestatud sätetel.

    4. Kui olete tehingu perioodi „väga hilja” määratlenud, valige prognoosimise mudeli loomiseks suvand **Prognoosimise mudeli loomine**. Jaotis **Prognoosimise mudel** lehel **Finantsülevaadete parameetrid** näitab prognoosimise mudeli olekut.

        > [!NOTE]
        > Prognoosimise mudeli loomise ajal saate igal ajal protsessi taaskäivitamiseks valida suvandi **Lähtesta mudeli loomine**.

    Funktsioon on nüüd konfigureeritud ja kasutamiseks valmis.

Pärast seda, kui funktsioon on sisse lülitatud ja konfigureeritud ning prognoosimise mudel on loodud ja töötab, kuvab jaotise **Prognoosimise mudel** leht **Finantsülevaadete parameetrid** mudeli täpsuse, nagu järgmisel illustratsioonil on näidatud.

[![Prognoosimise mudeli täpsus finantsülevaadete parameetrite lehel](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Väljastuse üksikasjad

Finantsülevaadete avalik eelversioon on prooviversioonina juurutamiseks saadaval Ameerika Ühendriikides, Euroopas ja Ühendkuningriigis. Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.

Avaliku eelvaate funktsioone saab ja tuleb sisse lülitada ainult Järgu 2 liivakasti keskkondades. Liivakasti keskkonnas loodud seadistust ja AI mudeleid ei saa migreerida töökeskkonda. Lisateavet leiate teemast [Microsoft Dynamics 365 eelversioonide täiendavad kasutustingimused](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Privaatsusavaldus

Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.
