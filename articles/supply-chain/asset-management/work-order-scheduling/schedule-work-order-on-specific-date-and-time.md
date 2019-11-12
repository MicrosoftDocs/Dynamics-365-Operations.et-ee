---
title: Töökäsu plaanimine konkreetsele kuupäevale ja kellaajale
description: Selles teemas selgitatakse, kuidas varahalduses plaanida töökäsku konkreetsele kuupäevale ja kellaajale.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 634bbb4326d560848d36f579a1179187d8369087
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652030"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Töökäsu plaanimine konkreetsele kuupäevale ja kellaajale

[!include [banner](../../includes/banner.md)]

 

Kui töökäsk on vaja plaanida konkreetsele kuupäevale *ja* kellaajale, saate tühistada standardse plaanimise protsessi varahalduses ja töökäsu kohta luua konkreetse ajakava.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.

2. Töökäsu loendis klõpsake töökäsu ID-le veerus **Töökäsk**.

3. Klõpsake valikut **Redigeeri**.

4. Sisestage algus- ja lõppkuupäevad ja kellaajad väljadele **Eeldatav algus** ja **Eeldatav lõpp** kiirkaardil **Töökäsu päis**.

    ![Joonis 1](media/05-work-order-scheduling.png)

5. Vahekaardil **Üldine** klõpsake valikut **Plaani**, et kasutada standardset plaanimise protsessi, või klõpsake valikut **Lähetus**, kui soovite määrata töökäsku konkreetsele töötajale.

6. Selleks, et tühistada olemasolevat võimsuse reserveerimist, mis kinnitab, et töökäsk on plaanitud oodatavasse perioodi, tehke alloleval joonisel näidatud valikud dialoogis **Plaani töökäsk** > jaotises **Piiratud võimsus**. See tähendab, et plaanimise protsessis ignoreeritakse olemasolevaid võimsuse reserveerimisi, sest töökäsk peab algama eeldataval algusajal.

    ![Joonis 2](media/06-work-order-scheduling.png)

7. Plaanimise alustamiseks klõpsake **OK**.

8. Kui plaanimise protsessi tulemusena tehakse topeltbroneeringuid, näete ekraanil sõnumit ja saate seotud töökäskusid kohandada.

>[!NOTE]
>Hooldustöötaja töökäsu jaoks plaanimiseks peab see töötaja eeldataval alguskuupäeval ja -ajal olema saadaval. Töötaja saadavust seadistatakse [töötaja kalendris](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 

