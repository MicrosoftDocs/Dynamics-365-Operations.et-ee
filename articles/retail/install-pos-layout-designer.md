---
title: "Jaemüügikassa paigutuse kujundaja installimine"
description: "Saate kasutada ühe klõpsuga kujundajat, et kujundada kaupluste, registrite, kassapidajate ja juhatajate jaoks režiimis Horisontaalne või režiimis Vertikaalne erinevaid uudse jaemüügikassa (MPOS) ja pilve kassa paigutusi."
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 30adfefd5ec70ddce348dab2481d518875e01ff2
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="install-the-retail-pos-layout-designer"></a>Jaemüügikassa paigutuse kujundaja installimine

[!include [banner](includes/banner.md)]

Saate kasutada ühe klõpsuga kujundajat, et kujundada kaupluste, registrite, kassapidajate ja juhatajate jaoks režiimis Horisontaalne või režiimis Vertikaalne erinevaid uudse jaemüügikassa (MPOS) ja pilve kassa paigutusi.

Tänapäevase jamüügikassa (MPOS) või pilve kassa graafilist kujundust juhib kassa paigutus. Paigutus juhib erinevate objektide asukohta. Näited hõlmavad kogupaigutust, kaubavõrgustiku paigutust, kliendi paigutust, makse paigutust ja erinevate menüünuppude paigutust. Paigutused hõlmavad ka töötajatele esitatava müügiliidese üldist ilmet.

## <a name="install-the-one-click-designer"></a>Ühe klõpsuga kujundaja installimine
1.  Rakenduses Microsoft Dynamics 365 for Retail kasutage üleval vasakul olevat menüüd, et navigeerida asukohta **Jaemüük** **ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Ekraani paigutused**.
2.  Valige mis tahes paigutus, millel on rakenduse tüüp **Modern POS Windowsi jaoks** või **Pilve POS** ja klõpsake seejärel valikut **Paigutusekujundaja**.
3.  Ühe klõpsuga kujundaja installi käitamiseks klõpsake Internet Exploreri akna alumisse ossa ilmuval teavitusribal käsku **Ava**. (Teistes brauserites võib teavitusriba ilmuda kusagile mujale.)
4.  Ilmuvas teateaknas **Rakenduse käivitamine - turbehoiatus** klõpsake valikut **Käivita**, et installida jaemüügikujundaja host. Installi edenemist näitab edenemisnäidik.
5.  Pärast installi lõpetamist sisestage lehele **Sisselogimine** kujundaja käivitamiseks oma Microsoft 365 for Retaili kasutajanimi ja parool ning klõpsake seejärel valikut **Sisselogimine**.
6.  Pärast mandaatide kinnitamist ja kujundaja käivitamist saate kujundada oma enda paigutuse või muuta olemasolevat paigutust. [![Paigutus ühe klõpsuga kujundajas](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Paigutusekujundaja installimise tõrkeotsing
-   Kui klõpsate valikut **Kujundaja**, ei ilmu allalaadimiseks (või käivitamiseks) installiprogrammi või teie praegused turbesätted ei võimalda teil faili alla laadida. **Lahendused**
    -   Internet Exploreris veenduge, et hüpikakna blokeerija on selle tegevuskoha jaoks keelatud. Klõpsake suvandeid **Sätted** &gt; **Suvandid** &gt; **Privaatsus** &gt; **Hüpikakna blokeerija leidmine** ja muutke sätet, kui muutmine on vajalik.
    -   Lisage Dynamics 365 for Retaili URL Internet Exploreris usaldusväärsete saitide hulka. Klõpsake suvandeid **Sätted** &gt; **Suvandid** &gt; **Turve** &gt; **Usaldusväärsed saidid** &gt; **Saidid** &gt; **Lisa**.
-   Programm ei käivitu ja teil palutakse hankijaga ühendust võtta. **Lahendus:** lisage Dynamics 365 for Retail Internet Exploreris usaldusväärsete saitide hulka. Klõpsake valikuid **Säte** &gt; **Suvandid** &gt; **Turve** &gt; **Usaldusväärsed saidid** &gt; **Saidid** &gt; **Lisa**.

**Teadaolev probleem:** kujundaja ei tööta õigesti brauserites Google Chrome ja Mozilla Firefox. Töötame selle probleemi lahendamiseks.

<a name="additional-resources"></a>Lisaressursid
--------

[Tänapäevase jaemüügikassa konfigureerimine, allalaadimine, installimine ja aktiveerimine](retail-modern-pos-device-activation.md)




