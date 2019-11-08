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
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="d8f3d-103">Töökäsu plaanimine konkreetsele kuupäevale ja kellaajale</span><span class="sxs-lookup"><span data-stu-id="d8f3d-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d8f3d-104">Kui töökäsk on vaja plaanida konkreetsele kuupäevale *ja* kellaajale, saate tühistada standardse plaanimise protsessi varahalduses ja töökäsu kohta luua konkreetse ajakava.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="d8f3d-105">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="d8f3d-106">Töökäsu loendis klõpsake töökäsu ID-le veerus **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="d8f3d-107">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-107">Click **Edit**.</span></span>

4. <span data-ttu-id="d8f3d-108">Sisestage algus- ja lõppkuupäevad ja kellaajad väljadele **Eeldatav algus** ja **Eeldatav lõpp** kiirkaardil **Töökäsu päis**.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![Joonis 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="d8f3d-110">Vahekaardil **Üldine** klõpsake valikut **Plaani**, et kasutada standardset plaanimise protsessi, või klõpsake valikut **Lähetus**, kui soovite määrata töökäsku konkreetsele töötajale.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="d8f3d-111">Selleks, et tühistada olemasolevat võimsuse reserveerimist, mis kinnitab, et töökäsk on plaanitud oodatavasse perioodi, tehke alloleval joonisel näidatud valikud dialoogis **Plaani töökäsk** > jaotises **Piiratud võimsus**.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="d8f3d-112">See tähendab, et plaanimise protsessis ignoreeritakse olemasolevaid võimsuse reserveerimisi, sest töökäsk peab algama eeldataval algusajal.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![Joonis 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="d8f3d-114">Plaanimise alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="d8f3d-115">Kui plaanimise protsessi tulemusena tehakse topeltbroneeringuid, näete ekraanil sõnumit ja saate seotud töökäskusid kohandada.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="d8f3d-116">Hooldustöötaja töökäsu jaoks plaanimiseks peab see töötaja eeldataval alguskuupäeval ja -ajal olema saadaval.</span><span class="sxs-lookup"><span data-stu-id="d8f3d-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="d8f3d-117">Töötaja saadavust seadistatakse [töötaja kalendris](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="d8f3d-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

