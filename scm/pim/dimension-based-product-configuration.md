---
title: "Dimensioonipõhine tootekonfiguratsioon"
description: "Dimensioonipõhine toote konfigureerimine tähistab lihtsat lahendust mitme tootevariandi loomiseks ühest tooteetalonist ja selle kooslusest."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 89f01401f1d937a72ae7e59b784cf034b48aaf1f
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="04c3c-103">Dimensioonipõhine tootekonfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="04c3c-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="04c3c-104">Dimensioonipõhine toote konfigureerimine tähistab lihtsat lahendust mitme tootevariandi loomiseks ühest tooteetalonist ja selle kooslusest.</span><span class="sxs-lookup"><span data-stu-id="04c3c-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="04c3c-105">Dimensioonipõhine tootekonfiguratsioon on üks kolmest integreeritud tootekonfiguratsiooni tehnoloogiatest.</span><span class="sxs-lookup"><span data-stu-id="04c3c-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="04c3c-106">Kaks ülejäänud tehnoloogiat on eelmääratletud variandid ja piirangupõhine konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="04c3c-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="04c3c-107">Kõik kolm tehnoloogiat kasutavad lähtepunktina tooteetaloni ja võimaldavad kasutajal luua ühele tooteetalonile palju tootevariante.</span><span class="sxs-lookup"><span data-stu-id="04c3c-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="04c3c-108">Põhimõisted</span><span class="sxs-lookup"><span data-stu-id="04c3c-108">Key concepts</span></span>
<span data-ttu-id="04c3c-109">Dimensioonipõhise tootekonfiguratsiooni aluseks on järgmised põhimõisteid.</span><span class="sxs-lookup"><span data-stu-id="04c3c-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="04c3c-110">Tooteetalonid</span><span class="sxs-lookup"><span data-stu-id="04c3c-110">Product masters</span></span>
-   <span data-ttu-id="04c3c-111">Konfiguratsiooni tootedimensioon</span><span class="sxs-lookup"><span data-stu-id="04c3c-111">Configuration product dimension</span></span>
-   <span data-ttu-id="04c3c-112">Konfiguratsioonigrupid</span><span class="sxs-lookup"><span data-stu-id="04c3c-112">Configuration groups</span></span>
-   <span data-ttu-id="04c3c-113">Kooslus</span><span class="sxs-lookup"><span data-stu-id="04c3c-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="04c3c-114">Konfigureerimisprotsess</span><span class="sxs-lookup"><span data-stu-id="04c3c-114">Configuration route</span></span>
-   <span data-ttu-id="04c3c-115">Konfiguratsioonireeglid</span><span class="sxs-lookup"><span data-stu-id="04c3c-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="04c3c-116">Tooteetalonid</span><span class="sxs-lookup"><span data-stu-id="04c3c-116">Product masters</span></span>

<span data-ttu-id="04c3c-117">Tooteetalon on igasuguse toote konfiguratsiooniprotsessi lähtepunkt.</span><span class="sxs-lookup"><span data-stu-id="04c3c-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="04c3c-118">Toote dimensioonipõhise konfiguratsiooni puhul on vaja selle konkreetse konfiguratsioonitehnoloogiaga tooteetaloni ja toote dimensioonigruppi, mis sisaldab konfiguratsiooni tootedimensiooni.</span><span class="sxs-lookup"><span data-stu-id="04c3c-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="04c3c-119">Konfiguratsiooni tootedimensioon</span><span class="sxs-lookup"><span data-stu-id="04c3c-119">Configuration product dimension</span></span>

<span data-ttu-id="04c3c-120">Konfiguratsiooni tootedimensiooni kasutatakse tooteetalonide tootevariantide tuvastamiseks dimensioonipõhise konfiguratsioonitehnoloogiaga.</span><span class="sxs-lookup"><span data-stu-id="04c3c-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="04c3c-121">Konfiguratsiooni dimensiooni väärtuse sisestab kasutaja ja see peaks aitama tuvastada üksikuid tootevariante.</span><span class="sxs-lookup"><span data-stu-id="04c3c-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="04c3c-122">Konfiguratsioonigrupid</span><span class="sxs-lookup"><span data-stu-id="04c3c-122">Configuration groups</span></span>

<span data-ttu-id="04c3c-123">Konfiguratsioonigrupid määratletakse keskhoidlas ja neid saab kasutada kõigi dimensioonipõhiste toote konfiguratsioonimudelite jaoks.</span><span class="sxs-lookup"><span data-stu-id="04c3c-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="04c3c-124">Konfiguratsioonigrupid on seotud üksikute koosluse ridadega ja need hoiavad koos üksteist välistavate ridade gruppi.</span><span class="sxs-lookup"><span data-stu-id="04c3c-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="04c3c-125">See tähendab, et ühe tootevariandi puhul saab valida grupist ainult ühe rea.</span><span class="sxs-lookup"><span data-stu-id="04c3c-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="04c3c-126">Kooslus</span><span class="sxs-lookup"><span data-stu-id="04c3c-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="04c3c-127">Kooslus tähistab dimensioonipõhise tootekonfiguratsiooni koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="04c3c-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="04c3c-128">See peab sisaldama kõik tootevariandis kasutatavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="04c3c-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="04c3c-129">Iga koosluse rida võib viidata konfiguratsioonigrupile.</span><span class="sxs-lookup"><span data-stu-id="04c3c-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="04c3c-130">Kui rida ei viita konfiguratsioonigrupile, lisatakse see kõigile tootevariantidele.</span><span class="sxs-lookup"><span data-stu-id="04c3c-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="04c3c-131">Konfigureerimisprotsess</span><span class="sxs-lookup"><span data-stu-id="04c3c-131">Configuration route</span></span>

<span data-ttu-id="04c3c-132">Konfiguratsiooniprotsess määrab konfiguratsioonigruppide järjestuse, nagu need kasutajale toote konfiguratsiooniprotsessis kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="04c3c-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="04c3c-133">Konfiguratsioonireeglid</span><span class="sxs-lookup"><span data-stu-id="04c3c-133">Configuration rules</span></span>

<span data-ttu-id="04c3c-134">Konfiguratsioonireeglid kajastavad mehhanismi, mis tagab, et ühes koosluse konfiguratsioonigrupis sisalduv toode lisab toote sama koosluse konfiguratsioonigruppi või arvab selle sealt välja.</span><span class="sxs-lookup"><span data-stu-id="04c3c-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="04c3c-135">Toote modelleerimisprotsess</span><span class="sxs-lookup"><span data-stu-id="04c3c-135">Product modeling process</span></span>
<span data-ttu-id="04c3c-136">Dimensioonipõhise toote tootemudeli koostamise loomulik protsess algab vastavate konfiguratsioonigruppide määratlemisest.</span><span class="sxs-lookup"><span data-stu-id="04c3c-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="04c3c-137">On oluline tagada, et kõik tooted, mida koosluses kasutatakse, on väljastatud ettevõttele, millele tootemudel on koostatud.</span><span class="sxs-lookup"><span data-stu-id="04c3c-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="04c3c-138">Kui need koosteüksused on paigas, saab kasutaja luua koosluse ja määrata konfiguratsioonigrupid kõigile vastavatele koosluse ridadele.</span><span class="sxs-lookup"><span data-stu-id="04c3c-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="04c3c-139">Kui kooslus on valmis, saab määratleda konfigureerimisprotsessi konfiguratsioonigruppide õigesse järjekorda paigutamiseks.</span><span class="sxs-lookup"><span data-stu-id="04c3c-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="04c3c-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimensioonipõhine-toote-modelleerimisprotsess](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimensioonipõhine-toote-modelleerimisprotsess\[/caption\] Kui on olemas teatud erinevatest konfiguratsioonigruppidest pärinevaid tooteid, mida tuleb või mida ei tohi koos kasutada, saate koostada konfigureerimisreeglid, mis need tooteseosed jõustavad.</span><span class="sxs-lookup"><span data-stu-id="04c3c-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimension-based product modeling process\[/caption\] If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="04c3c-141">Kui kooslus on seotud koosluse versiooni kaudu dimensioonipõhise tooteetaloniga ja mõlemad on kinnitatud ning aktiveeritud, saate luua tootekonfiguratsioone ja sisestada igale konfiguratsioonile nime.</span><span class="sxs-lookup"><span data-stu-id="04c3c-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="04c3c-142">Konfiguratsioonid saab määratleda enne ühegi kande loomist või seda saab teha siis, kui ilmneb vajadus teatud konfiguratsiooni järele.</span><span class="sxs-lookup"><span data-stu-id="04c3c-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="04c3c-143">Soovituslik kasutamine</span><span class="sxs-lookup"><span data-stu-id="04c3c-143">Suggested use</span></span>

<span data-ttu-id="04c3c-144">Dimensioonipõhist konfiguratsioonitehnoloogiat saab kõige paremini kasutada piiratud varieeritavusega toodete puhul ja standardsete tootedimensioonide suurus, värv, stiil ja konfiguratsioon ei sobi konkreetse tootevarianti tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="04c3c-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="04c3c-145">Näiteks võib olla jalgratas raami kõrguse, ratta suuruse, pidurite tüüpide ja erinevate käikudega.</span><span class="sxs-lookup"><span data-stu-id="04c3c-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>




