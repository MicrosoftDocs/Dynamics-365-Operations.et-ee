---
title: "Mittetootmiskeskkonna standardkulude värskendamine"
description: "Selles artiklis antakse juhiseid mittetootmiskeskkonna standardkulude värskendamise kohta."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0386ca1e5e7bf6e578ba2abf1b2c9eefe4dd2a02
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="8fbbf-103">Mittetootmiskeskkonna standardkulude värskendamine</span><span class="sxs-lookup"><span data-stu-id="8fbbf-103">Update standard costs in a non-manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8fbbf-104">Selles artiklis antakse juhiseid mittetootmiskeskkonna standardkulude värskendamise kohta.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="8fbbf-105">Järgmised juhised eeldavad, et kasutate kaheversioonilist lähenemist standardkulu värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="8fbbf-106">Selles lähenemises sisaldab üks kuluarvutuse versioon standardkulusid, mis määratleti algselt külmutatud perioodiks, ja teine kuluarvutuse versioon sisaldab astmelisi värskendusi.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="8fbbf-107">Iga värskendus sisestatakse teise kuluarvutuse versiooni kuuluva kulukirjena ja lubatakse lõpuks.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="8fbbf-108">Teine võimalus on üheversiooniline lähenemine, mis kasutab algselt määratletud standardkulude kogumit.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="8fbbf-109">Kaheversiooniline lähenemine nõuab teise kuluarvutuse versiooni määratlemist.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="8fbbf-110">Siin on juhised selle kuluarvutuse versiooni määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="8fbbf-111">Määrake kulutüüp **Standardkulud**.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="8fbbf-112">Määrake kirjeldav identifikaator, mis näitab kuluarvutuse versiooni sisu, nt **2016-VÄRSKENDUSED**.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="8fbbf-113">Veenduge, et sisu sisaldab kulukirjeid.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="8fbbf-114">Lubage kõigile laoaladele kulukirjete sisestamine.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="8fbbf-115">Laoala määramisel saab kulukirjeid sisestada ainult selle laoala jaoks.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="8fbbf-116">Märkige taandepõhimõtteks **Pole**.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="8fbbf-117">Taandepõhimõte kehtib ainult toodetud kaupade kulukalkulatsioonidele.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="8fbbf-118">Uute kaupade standardsete kulude parandamiseks, korrigeerimiseks või värskendamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="8fbbf-119">Kasutage **Kuluarvutuse versiooni** **seadistamise** lehte, et lubada kulu andmete sisestamine teise kuluarvutuse versiooni.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="8fbbf-120">Soovi korral saate vältida ootel kulude aktiveerimist, nii et aktiveerimine lubatakse pärast ootel kulude terviklikku ja täpset määramist.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="8fbbf-121">Soovi korral võite sisestada ka kuupäeva väljale **Alguskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="8fbbf-122">Üldjuhisena kasutage kuupäeva, millal kavatsete astmelised värskendused aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="8fbbf-123">Teine võimalus on jätta kuluarvutuse versiooni väli **Alguskuupäev** tühjaks ja sisestada siis kuupäev iga kulukirje väljale **Alguskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="8fbbf-124">Kasutage lehte **Kauba hind** värskenduste sisestamiseks kauba kulukirjetena, mis sisalduvad teises kuluarvutuse versioonis.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="8fbbf-125">Kasutage aruannet **Kauba hinnad** teises kuluarvutuse versioonis sisalduvate kauba kulukirjete terviklikkuse ja täpsuse kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="8fbbf-126">Kasutage lehte **Kuluarvutuse versiooni hooldus** blokeerimislipu muutmiseks, et lubada teises kuluarvutuse versioonis sisalduvate ootel kulukirjete aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="8fbbf-127">Kasutage lehte **Hindade aktiveerimine** (mille saab avada lehelt **Kuluarvutuse versiooni hooldus**) kõigi teises kuluarvutuse versioonis sisalduvate ootel kauba kulukirjete aktiveerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="8fbbf-128">Ootel kulukirjeid saab aktiveerida ka eraldi kaupade kohta, klõpsates nuppu **Ootel hinna aktiveerimine** lehel **Kauba hind**.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="8fbbf-129">Täiendava andmete hoolduse vältimiseks kasutage lehte **Kuluarvutuse versiooni seadistus** blokeerimislippude muutmiseks, et lubada teises kuluarvutuse versioonis sisalduvate ootel kulukirjete aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="8fbbf-130">Blokeerimispoliitikad takistavad uute ootel kulude sisestamist ja ootel kulude aktiveerimist.</span><span class="sxs-lookup"><span data-stu-id="8fbbf-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





