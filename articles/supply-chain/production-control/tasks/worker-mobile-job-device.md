---
title: Töötaja konfigureerimine töö mobiilse seadme abil
description: See artikkel selgitab, kuidas määrata õigeid rolle töötaja kasutajakontole ja seejärel lubada töötajal tööde juhtimisega registreerimisi teha.
author: johanhoffmann
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f6f51a66d49cafd172ba123bf883fb41cdcb5c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844301"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Töötaja konfigureerimine töö mobiilse seadme abil

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas määrata õigeid rolle töötaja kasutajakontole ja seejärel lubada töötajal tööde juhtimisega registreerimisi teha.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]