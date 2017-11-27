---
title: "Osaline asukoha tsükliline inventuur"
description: "Tsüklilise inventuuri plaanid juhivad tegelikke inventuuritoimingud. Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0e0f9d81f4d5943a89d8ac87776e05acb32cb8d9
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="84c80-104">Osaline asukoha tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="84c80-104">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="84c80-105">Tsüklilise inventuuri plaanid juhivad tegelikke inventuuritoimingud.</span><span class="sxs-lookup"><span data-stu-id="84c80-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="84c80-106">Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante.</span><span class="sxs-lookup"><span data-stu-id="84c80-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="84c80-107">Tsüklilise inventuuri plaanide abil inventuuritöö loomisel saate juhtida tegelikke inventuuritoiminguid.</span><span class="sxs-lookup"><span data-stu-id="84c80-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="84c80-108">Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante.</span><span class="sxs-lookup"><span data-stu-id="84c80-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="84c80-109">Konkreetseid tooteid filtreerides saab laojuht vähendada ülevaatamise üldkulusid, vältida konsolideerimisvigu ja säästa aega.</span><span class="sxs-lookup"><span data-stu-id="84c80-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="84c80-110">Osalise asukoha tsüklilise inventuuri konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="84c80-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="84c80-111">Kui kasutate inventuuritoimingute jaoks lao tööprotsessi, luuakse iga asukoha jaoks tööpäis.</span><span class="sxs-lookup"><span data-stu-id="84c80-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="84c80-112">Kui määratlete tsüklilise inventuuri plaani, võite kasutada päringut **Vali asukohad** loodava tsüklilise inventuuri töö piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="84c80-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="84c80-113">Tsüklilise inventuuri plaani jaoks toodete valimisel saate valida nii toote kui ka tootevariandi päringuid, et täpsustada, mida loendatakse.</span><span class="sxs-lookup"><span data-stu-id="84c80-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="84c80-114">Tsüklilise inventuuri plaaniga saab seostada **töömalli** määramiseks, kuidas tsüklilise inventuuri töö tuleks luua.</span><span class="sxs-lookup"><span data-stu-id="84c80-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="84c80-115">Inventuuritoimingute töömallile viidatakse otse tsüklilise inventuuri plaanist.</span><span class="sxs-lookup"><span data-stu-id="84c80-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="84c80-116">Töömalli üksikasjade määratlemisel võite kasutada valikut **Töörea jaotused** määramiseks, kas inventuuritöö read tuleks rühmitada kaubakoodi või tootevariandi koodi alusel.</span><span class="sxs-lookup"><span data-stu-id="84c80-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="84c80-117">See seadistus on vajalik ainult juhul, kui soovite loendada asukohas vaba kaubavaru ainult teatud toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="84c80-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="84c80-118">Loodavatel tsüklilise inventuuri töö ridadel on siin määratud teabetase ja juhendatud inventuuritoiming toimub selle taseme põhjal.</span><span class="sxs-lookup"><span data-stu-id="84c80-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="84c80-119">Kui seostate tsüklilise inventuuri plaanid töömallidega, kasutades valikut **Tööridade jaotused**, valitakse loodavale tsüklilise inventuuri tööle väli **Osaline tsükliline inventuur** ja töömalli definitsiooni põhjal luuakse mitu tsüklilise inventuuri töö rida.</span><span class="sxs-lookup"><span data-stu-id="84c80-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="84c80-120">Enne osalise tsüklilise inventuuri töö töötlemist peab tegema tsüklilise inventuuri seadistamise käigus mobiilse seadme menüüelemendile vähemalt valiku **Kuva kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="84c80-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="84c80-121">Laooperaatoril palutakse registreerida ainult inventuuriridadega seotud inventuuriteave (kaubakoodid ja tootedimensioonid).</span><span class="sxs-lookup"><span data-stu-id="84c80-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="84c80-122">Kõiki muid vabu kaubavarusid eiratakse selle inventuuriprotsessi puhul.</span><span class="sxs-lookup"><span data-stu-id="84c80-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="84c80-123">Osalise tsüklilise inventuuri protsessi puhul ei uuendata asukoha kuupäeva/kellaaega **Viimane tsükliline inventuur**.</span><span class="sxs-lookup"><span data-stu-id="84c80-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="84c80-124">Näide</span><span class="sxs-lookup"><span data-stu-id="84c80-124">Example</span></span>
<span data-ttu-id="84c80-125">Selle näite puhul tuleb laos 61 loendada ainult kaup koodiga A0001.</span><span class="sxs-lookup"><span data-stu-id="84c80-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="84c80-126">Tsüklilisele inventuurile luuakse uus töömall.</span><span class="sxs-lookup"><span data-stu-id="84c80-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="84c80-127">Inventuuri tööridade rühmitamiseks kaubakoodi alusel kasutatakse valikut **Töörea jaotused**.</span><span class="sxs-lookup"><span data-stu-id="84c80-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="84c80-128">Seega on loodaval tsüklilise inventuuri tööl read kaubakoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="84c80-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="84c80-129">Võite rühmitada read ka tootevariandi numbri järgi.</span><span class="sxs-lookup"><span data-stu-id="84c80-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="84c80-130">Luuakse uus tsüklilise inventuuri plaan, mis viitab äsja loodud töömallile.</span><span class="sxs-lookup"><span data-stu-id="84c80-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="84c80-131">Tsüklilise inventuuri plaan sisaldab kõiki asukohti laos 61 (päring **Vali asukohad**), kus on kaubakoodi A0001 varud.</span><span class="sxs-lookup"><span data-stu-id="84c80-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="84c80-132">Konkreetsete toodete valik on määratletud jaotises **Tsüklilise inventuuri tootevalikud**.</span><span class="sxs-lookup"><span data-stu-id="84c80-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="84c80-133">Tsüklilise inventuuri plaanidele saab valida tooteid, määrates välja **Tühjad asukohad** olekuks **Välista tühjad**.</span><span class="sxs-lookup"><span data-stu-id="84c80-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="84c80-134">Tsüklilise inventuuri plaani töötlemisel luuakse kaubakoodile A0001 osaline tsüklilise inventuuri töö.</span><span class="sxs-lookup"><span data-stu-id="84c80-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="84c80-135">Tegeliku inventuuriprotsessi saab juhendatud tsüklilise inventuuri puhul läbida mobiilse seadme menüüelemendi abil.</span><span class="sxs-lookup"><span data-stu-id="84c80-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="84c80-136">Vt ka</span><span class="sxs-lookup"><span data-stu-id="84c80-136">See also</span></span>
--------

[<span data-ttu-id="84c80-137">Tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="84c80-137">Cycle counting</span></span>](cycle-counting.md)


