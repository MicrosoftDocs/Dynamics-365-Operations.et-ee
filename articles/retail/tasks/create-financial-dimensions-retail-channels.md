---
title: Jaemüügikanalite jaoks finantsdimensioonide loomine ja kauplustes dimensiooniväärtuste konfigureerimine
description: See protseduur selgitab jaemüügikanali finantsdimensiooni loomist dimensiooniväärtuste abil ja jaekauplustes finantsdimensiooni väärtuste konfigureerimise etappe.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf32d17a36fd699141ce697d23e20b2eb5cbfa54
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "354525"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="e31cc-103">Jaemüügikanalite jaoks finantsdimensioonide loomine ja kauplustes dimensiooniväärtuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e31cc-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e31cc-104">See protseduur selgitab jaemüügikanali finantsdimensiooni loomist dimensiooniväärtuste abil ja jaekauplustes finantsdimensiooni väärtuste konfigureerimise etappe.</span><span class="sxs-lookup"><span data-stu-id="e31cc-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="e31cc-105">Teema ei sisalda muid seotud etappe, näiteks dimensioonikogumite ja kontostruktuuride loomist.</span><span class="sxs-lookup"><span data-stu-id="e31cc-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="e31cc-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="e31cc-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e31cc-107">Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="e31cc-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="e31cc-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e31cc-108">Click New.</span></span>
3. <span data-ttu-id="e31cc-109">Valige väljal Kasuta väärtusi suvand Jaemüügikanalid.</span><span class="sxs-lookup"><span data-stu-id="e31cc-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="e31cc-110">Sisestage väärtus väljale Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="e31cc-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="e31cc-111">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="e31cc-111">Click Activate.</span></span>
6. <span data-ttu-id="e31cc-112">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="e31cc-112">Click Close.</span></span>
7. <span data-ttu-id="e31cc-113">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="e31cc-113">Click Activate.</span></span>
8. <span data-ttu-id="e31cc-114">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="e31cc-114">Click Dimension values.</span></span>
9. <span data-ttu-id="e31cc-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e31cc-115">Close the page.</span></span>
10. <span data-ttu-id="e31cc-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e31cc-116">Click Save.</span></span>
11. <span data-ttu-id="e31cc-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e31cc-117">Close the page.</span></span>
12. <span data-ttu-id="e31cc-118">Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.</span><span class="sxs-lookup"><span data-stu-id="e31cc-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="e31cc-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e31cc-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e31cc-120">Laiendage jaotist Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="e31cc-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="e31cc-121">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e31cc-121">Click Edit.</span></span>
16. <span data-ttu-id="e31cc-122">Klõpsake väljal Retailchannel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e31cc-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="e31cc-123">Leidke ja valige loendist värskendatava kaupluse dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="e31cc-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="e31cc-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e31cc-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="e31cc-125">Klõpsake väljal CostCenter otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e31cc-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="e31cc-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e31cc-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="e31cc-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e31cc-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="e31cc-128">Klõpsake väljal Osakond otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e31cc-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="e31cc-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e31cc-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="e31cc-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e31cc-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="e31cc-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e31cc-131">Click Save.</span></span>

