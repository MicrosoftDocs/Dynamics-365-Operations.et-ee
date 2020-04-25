---
title: Töötaja konfigureerimine töö mobiilse seadme abil
description: Selles teemas selgitatakse töötaja kasutajakontole õigete rollide määramist ja töötajale tööde juhtimise süsteemi registreerimiste tegemise lubamist.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1086a88c341b95d6af03adc81c4e3e5d76adc69
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210199"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Töötaja konfigureerimine töö mobiilse seadme abil

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse töötaja kasutajakontole õigete rollide määramist ja töötajale tööde juhtimise süsteemi registreerimiste tegemise lubamist.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Töötajale teatud rolli määramise kontrollimine

Selles näites kontrollige enne töötaja konto konfigureerimist, et „SHANNONILE“ on määratud maisina operaatori roll.

1. Avage **Navigeerimispaan > Moodulid > Süsteemiadministraator > Kasutajad > Kasutajad**.
2. Otsige kasutajat kiirfiltrist. Selles näites sisestage `shannon`.
3. Valige link kuvatava kasutajakonto veerus **Kasutaja ID**.
4. Valige puus **Kasutaja rollid** jaotis **Rollid > Masina operaator**.
5. Avalehele naasmiseks sulgege lehed **kasutaja üksikasjad** ja **kasutajad**.

## <a name="configure-worker-account"></a>Töötaja konto konfigureerimine
1. Avage **Navigeerimispaan > Moodulid > Inimressursid > Töötajad > Töötajad**.
2. Otsige kasutajat kiirfiltrist. Selles näites sisestage `shannon`.
3. Valige link kuvatava kasutajakonto veerus **Nimi**.
4. Valige vahekaart **Aja registreerimine**.
5. Valige **Registreerimisterminaalides aktiveerimine**.
6. Sisestage või valige väärtused järgmistele väljadele.  

    - **Kalkulatsioonigrupp**  
    - **Vaike-arvutusgrupp**  
    - **Kinnitusegrupp**  
    - **Standardreeglid**  
    - **Reegligrupp**  

7. Valige nupp **OK**.
8. Uue kellaaja registreerimisega töötaja märgi numbri sisestamiseks valige **Redigeeri**. Sisestage väärtus väljale **Märgi ID**.
9. Valige käsk **Salvesta**.
10. Sulgege lehed **Töötaja üksikasjad** ja **Töötajad**.

## <a name="assign-worker-to-device-group"></a>Seadmete rühmale töötaja määramine
1. Avage **Tootmise juhtimine > Häälestus > Tootmise käivitamine > Seadmete töökaardi konfigureerimine**.
2. Valige **Lisa**.
3. Valige loendist soovitud töötaja. Selles näites valige **SHANNON**.
4. Valige nupp **OK**.
5. Valige suvand **Redigeeri**.
6. Väljal **Tootmisüksus** saate määrata töötajale vaikefiltri. See tagab, et kui töötaja seadmesse sisse logib, kuvatakse ainult valitud tootmisüksuse tootmistööd. Sisestage soovitud väärtus.
7. Sulgege leht.

