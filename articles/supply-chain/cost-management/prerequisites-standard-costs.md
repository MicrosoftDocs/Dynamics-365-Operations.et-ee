---
title: Standardkulude eeltingimuste ülevaade
description: Selles teemas kirjeldatakse standardkulude kasutamise põhisamme.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9333bda96ceae378ab74892534db13761038a06c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967354"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="b9c98-103">Standardkulude eeltingimuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b9c98-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9c98-104">Selles teemas kirjeldatakse standardkulude kasutamise põhisamme.</span><span class="sxs-lookup"><span data-stu-id="b9c98-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="b9c98-105">Järgmised etapid sõltuvad ettevõtte toimingutest.</span><span class="sxs-lookup"><span data-stu-id="b9c98-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="b9c98-106">Näiteks erinevad need mittetöötleva keskkonna, protsesse mittekasutava töötleva keskkonna ja protsesse kasutava töötleva keskkonna puhul.</span><span class="sxs-lookup"><span data-stu-id="b9c98-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="b9c98-107">Standardkulude seadistamiseks läbige järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="b9c98-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="b9c98-108">**1. Looge standardkuludele kauba mudeligrupp.**</span><span class="sxs-lookup"><span data-stu-id="b9c98-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="b9c98-109">Kasutage lehte **Kauba mudeligrupid** standardkuludele uue grupi loomiseks ja määrake üksuse **Standardkulu** laomudel.</span><span class="sxs-lookup"><span data-stu-id="b9c98-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="b9c98-110">Kauba mudeligrupi identifikaator peab olema selgitav, nt **Std kulud**.</span><span class="sxs-lookup"><span data-stu-id="b9c98-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="b9c98-111">Märkige ruudud näitamaks, et grupp peaks lubama finantsilist negatiivset laovaru ning sisestama füüsilisi ja finantsilisi laovarusid.</span><span class="sxs-lookup"><span data-stu-id="b9c98-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="b9c98-112">See standardkulugrupp määratakse kaupadele.</span><span class="sxs-lookup"><span data-stu-id="b9c98-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="b9c98-113">**2. Määrake pearaamatukontod, mis vastavad standardkulu erinevustele.**</span><span class="sxs-lookup"><span data-stu-id="b9c98-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b9c98-114">Kasutage lehte **Kontoplaan** standardkulude erinevustele vastavate pearaamatukontode määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b9c98-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b9c98-115">Need pearaamatukontod peavad olema määratud enne, kui need lehele **Sisestamine** määratakse.</span><span class="sxs-lookup"><span data-stu-id="b9c98-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="b9c98-116">Pearaamatukontod võivad kajastada kaubagruppe ja kulugruppe.</span><span class="sxs-lookup"><span data-stu-id="b9c98-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="b9c98-117">**3. Määrake pearaamatukontod kaubasisestustele, mis vastavad standardkulu erinevustele.**</span><span class="sxs-lookup"><span data-stu-id="b9c98-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b9c98-118">Kasutage lehte **Sisestamine** standardkulu erinevustele vastavate pearaamatukontode määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b9c98-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b9c98-119">Te saate erinevuste pearaamatukontod määrata kauba (või kaubagrupi) ja kulugrupi (või kulugrupi tüübi) alusel või et pearaamatukonto kohanduks kõigile kaupadele ja kulugruppidele.</span><span class="sxs-lookup"><span data-stu-id="b9c98-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="b9c98-120">Need valikud vastavad kulusuhetele tabelites, gruppides ja mõlemas.</span><span class="sxs-lookup"><span data-stu-id="b9c98-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="b9c98-121">Enne kauba sisestusreeglite määratlemist lubage lehel **Kandekombinatsioonid** kulusuhted (tabelites, gruppides ja mõlemas).</span><span class="sxs-lookup"><span data-stu-id="b9c98-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="b9c98-122">**4. Määrake standardkuludele vastavad laoparameetrid.**</span><span class="sxs-lookup"><span data-stu-id="b9c98-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="b9c98-123">Kasutage lehel **Laoarvestuse poliitikate häälestus > Parameetrid** olevat vahekaarti **Laoarvestus**, et määrata kulujuhtimise parameetrid standardkuludele vastavate kahe parameetri määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b9c98-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="b9c98-124">Valige väljalt **Kulujaotus** suvand **Puudub** või **Alammoodul**.</span><span class="sxs-lookup"><span data-stu-id="b9c98-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="b9c98-125">Kui teete valiku **Alammoodul**, on kulude jaotamine *aktiivne*.</span><span class="sxs-lookup"><span data-stu-id="b9c98-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="b9c98-126">Aktiivse kulu jaotamine on standardkulu kaubad mitmetasemelises tootmisstruktuuris kulugruppide segmentimise arvutamiseks, säilitamiseks ja vaatamiseks kriitiline toiming.</span><span class="sxs-lookup"><span data-stu-id="b9c98-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="b9c98-127">Kui kulude jaotamine on aktiivne, saate kaubavaru, pooleliolevat tööd ja kulugrupi kohta müüdud kaupade kulu kinnitada ja analüüsida üksikul tasemel, mitmetasemeliselt või kogu vormingus.</span><span class="sxs-lookup"><span data-stu-id="b9c98-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="b9c98-128">Aktiivne kulude jaotamine tähendab seda, et toodetud kauba kulu aktiveerimine põhjustab kulugrupi segmentimise talletamise kauba kulukirjes.</span><span class="sxs-lookup"><span data-stu-id="b9c98-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="b9c98-129">Kui teete valiku **Puudub**, ei säilitada standardsete kuluüksuste kulugrupi segmentimist.</span><span class="sxs-lookup"><span data-stu-id="b9c98-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="b9c98-130">Teiste sõnadega, toodetud kauba standardkulu arvutatakse ja säilitatakse ühe summana ilma kulugrupi segmentimiseta.</span><span class="sxs-lookup"><span data-stu-id="b9c98-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="b9c98-131">Toodetud komponentide kulupanused koondatakse üheks summaks.</span><span class="sxs-lookup"><span data-stu-id="b9c98-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="b9c98-132">Tehke väljal **Standardi hälbed** valikud **Summeeritud** või **Kulugrupi kohta**.</span><span class="sxs-lookup"><span data-stu-id="b9c98-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="b9c98-133">Valik **Kulugrupi kohta** võimaldab tuvastada ostuhinna hälbeid ja tootmise hälbeid kulugruppide kaupa.</span><span class="sxs-lookup"><span data-stu-id="b9c98-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="b9c98-134">Samuti saate tuvastada nelja tüüpi tootmishälbeid: partii suuruse, koguse-, hinna- ja asendushälbeid.</span><span class="sxs-lookup"><span data-stu-id="b9c98-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="b9c98-135">Kui tegite valiku **Summeeritud**, ei saa te tuvastada hälbeid kulugrupi alusel ega nelja tüüpi tootmishälbeid.</span><span class="sxs-lookup"><span data-stu-id="b9c98-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="b9c98-136">Te saate vaadata vaid summeeritud tootmiskulude hälbeid.</span><span class="sxs-lookup"><span data-stu-id="b9c98-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="b9c98-137">Standardi erinevuspoliitika töötab kulujaotumise poliitikast sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="b9c98-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="b9c98-138">Teiste sõnadega saate valida kulude jaotumise poliitika üksuse **Puudub** kohta, samuti saate valida erinevused kulugrupi alusel, nii et kulugrupi tootmiskulude hälbed hõlmatakse ikkagi.</span><span class="sxs-lookup"><span data-stu-id="b9c98-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="b9c98-139">**5. Looge standardkulude kuluversioonid.**</span><span class="sxs-lookup"><span data-stu-id="b9c98-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="b9c98-140">Kasutage lehte **Kuluarvutuse versiooni seadistus**, et luua üks või mitu standardkulude kuluversiooni.</span><span class="sxs-lookup"><span data-stu-id="b9c98-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="b9c98-141">Iga kuluversioon peab olema määratud kulutüübiga **Standardkulud** ja võimaldama sisul kuluandmeid lisada.</span><span class="sxs-lookup"><span data-stu-id="b9c98-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="b9c98-142">**6. Valmistage standardkulude kasutamiseks ette olemasolev klient.**</span><span class="sxs-lookup"><span data-stu-id="b9c98-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="b9c98-143">Kliendid, kes soovivad oma olemasolevaid kaupu muuta standardkulu laomudeliks peavad kasutama lehte **Standardkulu teisendused**.</span><span class="sxs-lookup"><span data-stu-id="b9c98-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="b9c98-144">Seotud teemad</span><span class="sxs-lookup"><span data-stu-id="b9c98-144">Related topics</span></span>
--------

[<span data-ttu-id="b9c98-145">Standardomahinna teisendamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="b9c98-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="b9c98-146">Ajaveebid</span><span class="sxs-lookup"><span data-stu-id="b9c98-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="b9c98-147">Kogukonna ajaveebid</span><span class="sxs-lookup"><span data-stu-id="b9c98-147">Community blogs</span></span>

- [<span data-ttu-id="b9c98-148">Otseste materjalikulude standardkulude seadistamine rakenduses Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b9c98-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="b9c98-149">Standardsed otsesed tööjõukulud rakenduses Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b9c98-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
