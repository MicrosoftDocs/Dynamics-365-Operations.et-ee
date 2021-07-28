---
title: Töökäsu plaanimine konkreetsele kuupäevale ja kellaajale
description: Selles teemas selgitatakse, kuidas varahalduses plaanida töökäsku konkreetsele kuupäevale ja kellaajale.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c28ade5bb6a22b9d15380085ea479e79ba246c1e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354056"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Töökäsu plaanimine konkreetsele kuupäevale ja kellaajale

[!include [banner](../../includes/banner.md)]

 

Kui töökäsk on vaja plaanida konkreetsele kuupäevale *ja* kellaajale, saate tühistada standardse plaanimise protsessi varahalduses ja töökäsu kohta luua konkreetse ajakava.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.

2. Töökäsu loendis klõpsake töökäsu ID-le veerus **Töökäsk**.

3. Klõpsake valikut **Redigeeri**.

4. Sisestage algus- ja lõppkuupäevad ja kellaajad väljadele **Eeldatav algus** ja **Eeldatav lõpp** kiirkaardil **Töökäsu päis**.

    ![Joonis 1.](media/05-work-order-scheduling.png)

5. Vahekaardil **Üldine** klõpsake valikut **Plaani**, et kasutada standardset plaanimise protsessi, või klõpsake valikut **Lähetus**, kui soovite määrata töökäsku konkreetsele töötajale.

6. Selleks, et tühistada olemasolevat võimsuse reserveerimist, mis kinnitab, et töökäsk on plaanitud oodatavasse perioodi, tehke alloleval joonisel näidatud valikud dialoogis **Plaani töökäsk** > jaotises **Piiratud võimsus**. See tähendab, et plaanimise protsessis ignoreeritakse olemasolevaid võimsuse reserveerimisi, sest töökäsk peab algama eeldataval algusajal.

    ![Joonis 2.](media/06-work-order-scheduling.png)

7. Plaanimise alustamiseks klõpsake **OK**.

8. Kui plaanimise protsessi tulemusena tehakse topeltbroneeringuid, näete ekraanil sõnumit ja saate seotud töökäskusid kohandada.

>[!NOTE]
>Hooldustöötaja töökäsu jaoks plaanimiseks peab see töötaja eeldataval alguskuupäeval ja -ajal olema saadaval. Töötaja saadavust seadistatakse [töötaja kalendris](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]