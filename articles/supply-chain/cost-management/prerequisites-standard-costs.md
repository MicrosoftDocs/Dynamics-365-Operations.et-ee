---
title: Standardkulude eeltingimused
description: "Selles teemas kirjeldatakse standardkulude kasutamise põhisamme."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e63f2b4289b640e601492425331ea8f3804d139a
ms.openlocfilehash: 4f505a2de89863d1a12d415795fdfb82b3557bc0
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="13df5-103">Standardkulude eeltingimused</span><span class="sxs-lookup"><span data-stu-id="13df5-103">Prerequisites for standard costs</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="13df5-104">Selles teemas kirjeldatakse standardkulude kasutamise põhisamme.</span><span class="sxs-lookup"><span data-stu-id="13df5-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="13df5-105">Järgmised etapid sõltuvad ettevõtte toimingutest.</span><span class="sxs-lookup"><span data-stu-id="13df5-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="13df5-106">Näiteks erinevad need mittetöötleva keskkonna, protsesse mittekasutava töötleva keskkonna ja protsesse kasutava töötleva keskkonna puhul.</span><span class="sxs-lookup"><span data-stu-id="13df5-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="13df5-107">Standardkulude seadistamiseks läbige järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="13df5-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="13df5-108">**1. Looge standardkuludele kauba mudeligrupp.**</span><span class="sxs-lookup"><span data-stu-id="13df5-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="13df5-109">Kasutage lehte **Kauba mudeligrupid** standardkuludele uue grupi loomiseks ja määrake üksuse **Standardkulu** laomudel.</span><span class="sxs-lookup"><span data-stu-id="13df5-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="13df5-110">Kauba mudeligrupi identifikaator peab olema selgitav, nt **Std kulud**.</span><span class="sxs-lookup"><span data-stu-id="13df5-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="13df5-111">Märkige ruudud näitamaks, et grupp peaks lubama finantsilist negatiivset laovaru ning sisestama füüsilisi ja finantsilisi laovarusid.</span><span class="sxs-lookup"><span data-stu-id="13df5-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="13df5-112">See standardkulugrupp määratakse kaupadele.</span><span class="sxs-lookup"><span data-stu-id="13df5-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="13df5-113">**2. Määrake pearaamatukontod, mis vastavad standardkulu erinevustele.**</span><span class="sxs-lookup"><span data-stu-id="13df5-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="13df5-114">Kasutage lehte **Kontoplaan** standardkulude erinevustele vastavate pearaamatukontode määramiseks.</span><span class="sxs-lookup"><span data-stu-id="13df5-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="13df5-115">Need pearaamatukontod peavad olema määratud enne, kui need lehele **Sisestamine** määratakse.</span><span class="sxs-lookup"><span data-stu-id="13df5-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="13df5-116">Pearaamatukontod võivad kajastada kaubagruppe ja kulugruppe.</span><span class="sxs-lookup"><span data-stu-id="13df5-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="13df5-117">**3. Määrake pearaamatukontod kaubasisestustele, mis vastavad standardkulu erinevustele.**</span><span class="sxs-lookup"><span data-stu-id="13df5-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="13df5-118">Kasutage lehte **Sisestamine** standardkulu erinevustele vastavate pearaamatukontode määramiseks.</span><span class="sxs-lookup"><span data-stu-id="13df5-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="13df5-119">Te saate erinevuste pearaamatukontod määrata kauba (või kaubagrupi) ja kulugrupi (või kulugrupi tüübi) alusel või et pearaamatukonto kohanduks kõigile kaupadele ja kulugruppidele.</span><span class="sxs-lookup"><span data-stu-id="13df5-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="13df5-120">Need valikud vastavad kulusuhetele tabelites, gruppides ja mõlemas).</span><span class="sxs-lookup"><span data-stu-id="13df5-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="13df5-121">Enne kauba sisestusreeglite määratlemist lubage lehel **Kandekombinatsioonid** kulusuhted (tabelites, gruppides ja mõlemas).</span><span class="sxs-lookup"><span data-stu-id="13df5-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="13df5-122">**4. Määrake standardkuludele vastavad laoparameetrid.**</span><span class="sxs-lookup"><span data-stu-id="13df5-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="13df5-123">Kasutage lehel **Varude parameetrid** olevat vahekaarti **Kooslused**, et määrata kulujuhtimise parameetrid standardkuludele vastavate kahe parameetri määramiseks.</span><span class="sxs-lookup"><span data-stu-id="13df5-123">Use the **Bills of materials** tab on the **Inventory parameters** page to define two cost control parameters that are related to standard costs.</span></span> 

    -  <span data-ttu-id="13df5-124">Valige väljalt **Kulujaotus** suvand **Puudub** või **Alammoodul**.</span><span class="sxs-lookup"><span data-stu-id="13df5-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="13df5-125">Kui teete valiku **Alammoodul**, on kulude jaotamine*aktiivne*.</span><span class="sxs-lookup"><span data-stu-id="13df5-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="13df5-126">Aktiivse kulu jaotamine on standardkulu kaubad mitmetasemelises tootmisstruktuuris kulugruppide segmentimise arvutamiseks, säilitamiseks ja vaatamiseks kriitiline toiming.</span><span class="sxs-lookup"><span data-stu-id="13df5-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="13df5-127">Kui kulude jaotamine on aktiivne, saate kaubavaru, pooleliolevat tööd ja kulugrupi kohta müüdud kaupade kulu kinnitada ja analüüsida üksikul tasemel, mitmetasemeliselt või kogu vormingus.</span><span class="sxs-lookup"><span data-stu-id="13df5-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="13df5-128">Aktiivne kulude jaotamine tähendab seda, et toodetud kauba kulu aktiveerimine põhjustab kulugrupi segmentimise talletamise kauba kulukirjes.</span><span class="sxs-lookup"><span data-stu-id="13df5-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="13df5-129">Kui teete valiku **Puudub**, ei säilitada standardsete kuluüksuste kulugrupi segmentimist.</span><span class="sxs-lookup"><span data-stu-id="13df5-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="13df5-130">Teiste sõnadega, toodetud kauba standardkulu arvutatakse ja säilitatakse ühe summana ilma kulugrupi segmentimiseta.</span><span class="sxs-lookup"><span data-stu-id="13df5-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="13df5-131">Toodetud komponentide kulupanused koondatakse üheks summaks.</span><span class="sxs-lookup"><span data-stu-id="13df5-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="13df5-132">Tehke väljal **Standardi hälbed** valikud **Summeeritud** või **Kulugrupi kohta**.</span><span class="sxs-lookup"><span data-stu-id="13df5-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="13df5-133">Valik **Kulugrupi kohta** võimaldab tuvastada ostuhinna hälbeid ja tootmise hälbeid kulugruppide kaupa.</span><span class="sxs-lookup"><span data-stu-id="13df5-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="13df5-134">Samuti saate tuvastada nelja tüüpi tootmishälbeid: partii suuruse, koguse-, hinna- ja asendushälbeid.</span><span class="sxs-lookup"><span data-stu-id="13df5-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="13df5-135">Kui tegite valiku **Summeeritud**, ei saa te tuvastada hälbeid kulugrupi alusel ega nelja tüüpi tootmishälbeid.</span><span class="sxs-lookup"><span data-stu-id="13df5-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="13df5-136">Te saate vaadata vaid summeeritud tootmiskulude hälbeid.</span><span class="sxs-lookup"><span data-stu-id="13df5-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="13df5-137">Standardi erinevuspoliitika töötab kulujaotumise poliitikast sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="13df5-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="13df5-138">Teiste sõnadega saate valida kulude jaotumise poliitika üksuse **Puudub** kohta, samuti saate valida erinevused kulugrupi alusel, nii et kulugrupi tootmiskulude hälbed hõlmatakse ikkagi.</span><span class="sxs-lookup"><span data-stu-id="13df5-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="13df5-139">**5. Looge standardkulude kuluversioonid.**</span><span class="sxs-lookup"><span data-stu-id="13df5-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="13df5-140">Kasutage lehte **Kuluarvutuse versiooni seadistus**, et luua üks või mitu standardkulude kuluversiooni.</span><span class="sxs-lookup"><span data-stu-id="13df5-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="13df5-141">Iga kuluversioon peab olema määratud kulutüübiga **Standardkulud** ja võimaldama sisul kuluandmeid lisada.</span><span class="sxs-lookup"><span data-stu-id="13df5-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="13df5-142">**6. Valmistage standardkulude kasutamiseks ette olemasolev klient.**</span><span class="sxs-lookup"><span data-stu-id="13df5-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="13df5-143">Kliendid, kes soovivad oma olemasolevaid kaupu muuta standardkulu laomudeliks peavad kasutama lehte **Standardkulu teisendused**.</span><span class="sxs-lookup"><span data-stu-id="13df5-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="13df5-144">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="13df5-144">Related topics</span></span>
--------

[<span data-ttu-id="13df5-145">Standardomahinna teisendamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="13df5-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)


