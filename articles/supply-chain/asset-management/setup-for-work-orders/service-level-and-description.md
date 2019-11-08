---
title: Teenindustase ja kirjeldus
description: Selles teemas selgitatakse teenindustaset ja kirjeldust varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7dd577c930c6cc17da6baee30d3558656de01a09
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569819"
---
# <a name="service-level-and-description"></a><span data-ttu-id="db8af-103">Teenindustase ja kirjeldus</span><span class="sxs-lookup"><span data-stu-id="db8af-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="db8af-104">Kui loote töökäsu, võite soovida määratleda selle teenindustasemeid ja lisada sellele üldise kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="db8af-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="db8af-105">Töökäsu teenindustasemeid saate luua lehel **Töökäsu teenindustasemed** ja kirjeldusi lehel **Töökäsu kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="db8af-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="db8af-106">Teenindustaseme loomine</span><span class="sxs-lookup"><span data-stu-id="db8af-106">Create a service level</span></span>

1. <span data-ttu-id="db8af-107">Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Teenindustase**.</span><span class="sxs-lookup"><span data-stu-id="db8af-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="db8af-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="db8af-108">Select **New**.</span></span>
3. <span data-ttu-id="db8af-109">Sisestage väljale **Teenindustase** teenindustase (näiteks arv).</span><span class="sxs-lookup"><span data-stu-id="db8af-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="db8af-110">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="db8af-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="db8af-111">Kiirkaardil **Töökäsud** saate määratleda oodatavat alguse ja lõpukuupäeva ning kellaaega.</span><span class="sxs-lookup"><span data-stu-id="db8af-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="db8af-112">Selle kiirkaardi väljad määratlevad ajaperioodi, mille kestel töökäsud tuleks alustada ja lõpetada.</span><span class="sxs-lookup"><span data-stu-id="db8af-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="db8af-113">Neid kasutatakse käsitsi loodud töökäskude korral ja hooldusnõuetel põhinevate töökäskude korral.</span><span class="sxs-lookup"><span data-stu-id="db8af-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="db8af-114">Sisestage väljale **Alguspäev** päevade arv, et määrata periood, mille jooksul töökäsku peaks alustama.</span><span class="sxs-lookup"><span data-stu-id="db8af-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="db8af-115">Päevade arvu arvutatakse alates töökäsu loomise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="db8af-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="db8af-116">Näiteks, kui töökäsk peaks algama siis, kui see loodi, sisestage **0**.</span><span class="sxs-lookup"><span data-stu-id="db8af-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="db8af-117">Kui töökäsk peaks algama ühe nädala jooksul pärast selle loomist, sisestage **7**.</span><span class="sxs-lookup"><span data-stu-id="db8af-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="db8af-118">Töökäsu alguskuupäeva seadistamiseks seadistage lisaks alguskuupäevale suvand **Määra algusaeg** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="db8af-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="db8af-119">Siis sisestage algusaeg väljale **Algusaeg**.</span><span class="sxs-lookup"><span data-stu-id="db8af-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="db8af-120">Kui seadistasite suvandi olekusse **Ei**, kasutatakse praegust kellaaega.</span><span class="sxs-lookup"><span data-stu-id="db8af-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="db8af-121">Sisestage väljale **Lõpp-päev** päevade arv, et määrata periood, mille jooksul töökäsku peaks lõpetama.</span><span class="sxs-lookup"><span data-stu-id="db8af-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="db8af-122">Päevade arvu arvutatakse alates töökäsu alguskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="db8af-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="db8af-123">Näiteks, kui töökäsk peaks lõppema ühe nädala jooksul alates alguskuupäevast, sisestage **7**.</span><span class="sxs-lookup"><span data-stu-id="db8af-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="db8af-124">Töökäsu lõppkellaaja seadistamiseks seadistage lisaks lõpp-päevale suvand **Määra lõppkellaaeg** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="db8af-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="db8af-125">Siis sisestage lõppkellaaeg väljale **Lõppkellaaeg**.</span><span class="sxs-lookup"><span data-stu-id="db8af-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="db8af-126">Kui seadistasite suvandi olekusse **Ei**, kasutatakse praegust kellaaega.</span><span class="sxs-lookup"><span data-stu-id="db8af-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="db8af-127">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="db8af-127">Select **Save**.</span></span>

![Töökäskude teenusetaseme leht](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="db8af-129">Kirjelduse loomine</span><span class="sxs-lookup"><span data-stu-id="db8af-129">Create a description</span></span>

1. <span data-ttu-id="db8af-130">Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="db8af-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="db8af-131">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="db8af-131">Select **New**.</span></span>
3. <span data-ttu-id="db8af-132">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="db8af-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="db8af-133">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="db8af-133">Select **Save**.</span></span>
