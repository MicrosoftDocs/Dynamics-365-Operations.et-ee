--- 
title: " Jaemüügikanalite jaoks finantsdimensioonide loomine ja kauplustes dimensiooniväärtuste konfigureerimine"
description: "See protseduur selgitab jaemüügikanali finantsdimensiooni loomist dimensiooniväärtuste abil ja jaekauplustes finantsdimensiooni väärtuste konfigureerimise etappe."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 56b586e971cfd4684f3c0b259270cc8b31521ac9
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="31cb6-103"> Jaemüügikanalite jaoks finantsdimensioonide loomine ja kauplustes dimensiooniväärtuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="31cb6-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="31cb6-104">See protseduur selgitab jaemüügikanali finantsdimensiooni loomist dimensiooniväärtuste abil ja jaekauplustes finantsdimensiooni väärtuste konfigureerimise etappe.</span><span class="sxs-lookup"><span data-stu-id="31cb6-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="31cb6-105">Teema ei sisalda muid seotud etappe, näiteks dimensioonikogumite ja kontostruktuuride loomist.</span><span class="sxs-lookup"><span data-stu-id="31cb6-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="31cb6-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="31cb6-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="31cb6-107">Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="31cb6-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="31cb6-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="31cb6-108">Click New.</span></span>
3. <span data-ttu-id="31cb6-109">Valige väljal Kasuta väärtusi suvand Jaemüügikanalid.</span><span class="sxs-lookup"><span data-stu-id="31cb6-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="31cb6-110">Sisestage väärtus väljale Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="31cb6-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="31cb6-111">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="31cb6-111">Click Activate.</span></span>
6. <span data-ttu-id="31cb6-112">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="31cb6-112">Click Close.</span></span>
7. <span data-ttu-id="31cb6-113">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="31cb6-113">Click Activate.</span></span>
8. <span data-ttu-id="31cb6-114">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="31cb6-114">Click Dimension values.</span></span>
9. <span data-ttu-id="31cb6-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="31cb6-115">Close the page.</span></span>
10. <span data-ttu-id="31cb6-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="31cb6-116">Click Save.</span></span>
11. <span data-ttu-id="31cb6-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="31cb6-117">Close the page.</span></span>
12. <span data-ttu-id="31cb6-118">Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.</span><span class="sxs-lookup"><span data-stu-id="31cb6-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="31cb6-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="31cb6-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="31cb6-120">Laiendage jaotist Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="31cb6-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="31cb6-121">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="31cb6-121">Click Edit.</span></span>
16. <span data-ttu-id="31cb6-122">Klõpsake väljal Retailchannel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="31cb6-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="31cb6-123">Leidke ja valige loendist värskendatava kaupluse dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="31cb6-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="31cb6-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="31cb6-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="31cb6-125">Klõpsake väljal CostCenter otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="31cb6-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="31cb6-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="31cb6-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="31cb6-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="31cb6-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="31cb6-128">Klõpsake väljal Osakond otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="31cb6-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="31cb6-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="31cb6-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="31cb6-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="31cb6-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="31cb6-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="31cb6-131">Click Save.</span></span>


