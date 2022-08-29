---
title: Kassa paigutuse kujundaja installimine
description: Saate kasutada ühe klõpsuga kujundajat, et kujundada kaupluste, registrite, kassapidajate ja juhatajate jaoks režiimis Horisontaalne või režiimis Vertikaalne erinevaid Modern POS-i (MPOS) ja pilvekassa paigutusi.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.industry: Retail
ms.search.form: RetailTillLayout
ms.openlocfilehash: a610dbb9db63236ae7d182692f45f21c56982c69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274255"
---
# <a name="install-the-pos-layout-designer"></a>Kassa paigutuse kujundaja installimine

[!include [banner](includes/banner.md)]

Saate kasutada ühe klõpsuga kujundajat, et kujundada kaupluste, registrite, kassapidajate ja juhatajate jaoks režiimis Horisontaalne või režiimis Vertikaalne erinevaid Modern POS-i (MPOS) ja pilvekassa paigutusi.

Uudse jaemüügikassa (MPOS) või pilve kassa graafilist kujundust juhib kassasahtli sisu paigutus. Paigutus juhib erinevate objektide asukohta. Näited hõlmavad kogupaigutust, kaubavõrgustiku paigutust, kliendi paigutust, makse paigutust ja erinevate menüünuppude paigutust. Paigutused hõlmavad ka töötajatele esitatava müügiliidese üldist ilmet.

## <a name="install-the-one-click-designer"></a>Ühe klõpsuga kujundaja installimine

1. Rakenduses Commerce kasutage vasakut ülamenüüd, et navigeerida asukohta **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Ekraanipaigutused**.
2. Valige mis tahes paigutus, millel on rakenduse tüüp **Modern POS Windowsi jaoks** või **Pilve POS** ja klõpsake seejärel valikut **Paigutusekujundaja**.
3. Ühe klõpsuga kujundaja installi käivitamiseks klõpsake Internet Exploreri akna alumisse ossa ilmuval teavitusribal käsku **Ava**. (Teistes brauserites võib teavitusriba ilmuda kusagile mujale.)
4. Ilmuvas teateaknas **Rakenduse käivitamine - turbehoiatus** klõpsake valikut **Käivita**, et installida jaemüügikujundaja host. Installi edenemist näitab edenemisnäidik.
5. Pärast installimise lõpulejõudmist sisestage kujundaja käivitamiseks lehel **Sisselogimine** oma Commerce’i kasutajanimi ja parool ning klõpsake valikut **Sisselogimine**.
6. Pärast mandaatide kinnitamist ja kujundaja käivitamist saate kujundada oma enda paigutuse või muuta olemasolevat paigutust.

    [![Paigutus ühe klõpsuga kujundajas.](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Paigutusekujundaja installimise tõrkeotsing

- Kui klõpsate valikut **Kujundaja**, ei ilmu allalaadimiseks (või käivitamiseks) installiprogrammi või teie praegused turbesätted ei võimalda teil faili alla laadida. 

    **Lahendused**

    - Internet Exploreris veenduge, et hüpikakna blokeerija oleks selle saidi puhul keelatud. Klõpsake suvandeid **Sätted** &gt; **Suvandid** &gt; **Privaatsus** &gt; **Hüpikakna blokeerija leidmine** ja muutke sätet, kui muutmine on vajalik.
    - Lisage Internet Exploreris Commerce’i URL usaldusväärsete saitide loendisse. Klõpsake suvandeid **Sätted** &gt; **Suvandid** &gt; **Turve** &gt; **Usaldusväärsed saidid** &gt; **Saidid** &gt; **Lisa**.

- Programm ei käivitu ja teil palutakse hankijaga ühendust võtta.

    **Lahendus.** Lisage Internet Exploreris Commerce’i URL usaldusväärsete saitide loendisse. Klõpsake valikuid **Säte** &gt; **Suvandid** &gt; **Turve** &gt; **Usaldusväärsed saidid** &gt; **Saidid** &gt; **Lisa**.

**Teadaolev probleem:** kujundaja ei tööta õigesti brauserites Google Chrome ja Mozilla Firefox. Töötame selle probleemi lahendamiseks.

## <a name="additional-resources"></a>Lisaressursid

[Retail Modern POS-i (MPOS) konfigureerimine, installimine ja aktiveerimine](retail-modern-pos-device-activation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
