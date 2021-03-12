---
title: Jaemüügikanalite jaoks finantsdimensioonide loomine ja kauplustes dimensiooniväärtuste konfigureerimine
description: See protseduur selgitab ärikanali finantsdimensiooni loomist dimensiooniväärtuste abil ja kauplustes finantsdimensiooni väärtuste konfigureerimise etappe.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86fc9c9a400bee1280b32f10b1e8f55e581e1984
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964741"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="9ba8f-103">Jaemüügikanalite jaoks finantsdimensioonide loomine ja kauplustes dimensiooniväärtuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9ba8f-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ba8f-104">See protseduur selgitab ärikanali finantsdimensiooni loomist dimensiooniväärtuste abil ja kauplustes finantsdimensiooni väärtuste konfigureerimise etappe.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="9ba8f-105">Teema ei sisalda muid seotud etappe, näiteks dimensioonikogumite ja kontostruktuuride loomist.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="9ba8f-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9ba8f-107">Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="9ba8f-108">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-108">Click New.</span></span>
3. <span data-ttu-id="9ba8f-109">Valige väljal Kasuta väärtusi suvand "Ärikanalid".</span><span class="sxs-lookup"><span data-stu-id="9ba8f-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="9ba8f-110">Sisestage väärtus väljale Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="9ba8f-111">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-111">Click Activate.</span></span>
6. <span data-ttu-id="9ba8f-112">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-112">Click Close.</span></span>
7. <span data-ttu-id="9ba8f-113">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-113">Click Activate.</span></span>
8. <span data-ttu-id="9ba8f-114">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-114">Click Dimension values.</span></span>
9. <span data-ttu-id="9ba8f-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-115">Close the page.</span></span>
10. <span data-ttu-id="9ba8f-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-116">Click Save.</span></span>
11. <span data-ttu-id="9ba8f-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-117">Close the page.</span></span>
12. <span data-ttu-id="9ba8f-118">Minge jaotisse Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="9ba8f-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9ba8f-120">Laiendage jaotist Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="9ba8f-121">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-121">Click Edit.</span></span>
16. <span data-ttu-id="9ba8f-122">Klõpsake väljal Ärikanal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="9ba8f-123">Leidke ja valige loendist värskendatava kaupluse dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="9ba8f-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="9ba8f-125">Klõpsake väljal CostCenter otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9ba8f-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="9ba8f-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="9ba8f-128">Klõpsake väljal Osakond otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="9ba8f-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="9ba8f-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="9ba8f-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-131">Click Save.</span></span>

