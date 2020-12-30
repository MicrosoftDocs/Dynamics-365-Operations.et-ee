---
title: Koorma koostamise töölaud
description: Selles teemas kirjeldatakse, kuidas töötada koorma koostamise töölauaga.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 429a8bac5491a342ecbc8b67c59c71715a4b0889
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646381"
---
# <a name="load-building-workbench"></a><span data-ttu-id="593ea-103">Koorma koostamise töölaud</span><span class="sxs-lookup"><span data-stu-id="593ea-103">Load building workbench</span></span>

<span data-ttu-id="593ea-104">Koorma koostamise töölaud võimaldab teil koormate loomisel rakendada koorma koostamise strateegiaid.</span><span class="sxs-lookup"><span data-stu-id="593ea-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="593ea-105">Koorma koostamise strateegia loomine</span><span class="sxs-lookup"><span data-stu-id="593ea-105">Create a load building strategy</span></span>

<span data-ttu-id="593ea-106">Koorma koostamise strateegiad saate kasutada koormate automaatseks koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="593ea-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="593ea-107">See võimalus võib olla kasulik järgmistes olukordades.</span><span class="sxs-lookup"><span data-stu-id="593ea-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="593ea-108">Kui saadate regulaarselt kindlaid tooteid, aitavad koormastrateegiad säästa aega, sest te ei pea iga kord sama koormat koostama.</span><span class="sxs-lookup"><span data-stu-id="593ea-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="593ea-109">Kui soovite tõhususe maksimeerimiseks välistada poolikud koormad, võivad koormastrateegiad aidata koormaid võimalikult palju täita.</span><span class="sxs-lookup"><span data-stu-id="593ea-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="593ea-110">Koorma koostamise strateegia klass nimega `TMSLoadBuildingVolumeStrategy` annab koorma koostamise strateegia nimega *Mahupõhine koorma koostamise strateegia*.</span><span class="sxs-lookup"><span data-stu-id="593ea-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="593ea-111">See strateegia võimaldab kasutada koorma mallil kõrguse ja kaalu kohta määratud maksimumväärtusi või alistada sätted, sisestades uusi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="593ea-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="593ea-112">See strateegia on ainus valmiskujul strateegia.</span><span class="sxs-lookup"><span data-stu-id="593ea-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="593ea-113">(Võib-olla soovite siiski ka kohandatud strateegiaid kasutada.)</span><span class="sxs-lookup"><span data-stu-id="593ea-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="593ea-114">Valmiskujul strateegiat *Mahupõhine koorma koostamise strateegia* kasutamiseks valige koorem lehe **Koorma koostamise töölaud** väljal **Koorma koostamise strateegia** (**Transpordihaldus &gt; Planeerimine &gt; Koorma koostamise töölaud**).</span><span class="sxs-lookup"><span data-stu-id="593ea-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="593ea-115">Koorma koostamise strateegia loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="593ea-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="593ea-116">Valige **Transpordihaldus &gt; Häälestus &gt; Koorma koostamine &gt; Koorma koostamise strateegiad**.</span><span class="sxs-lookup"><span data-stu-id="593ea-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="593ea-117">Tehle toimingupaanil valik **Loo klassiloend**, et veenduda, kas teil on kõigi saadaolevate klasside uusimad versioonid.</span><span class="sxs-lookup"><span data-stu-id="593ea-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="593ea-118">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="593ea-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="593ea-119">Sisestage strateegiale kordumatu nimi, valige koorma koostamise strateegia klass ja sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="593ea-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="593ea-120">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="593ea-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="593ea-121">Valige toimingupaanil **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="593ea-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="593ea-122">Tehke lehel **Koorma koostamise strateegia parameetrid** loendis valik **Mahuhulk** ja sisestage siis väljale **Väärtus** koorma kogu mahuhulga protsent, mida tuleks uuele koorma koostamise strateegiale rakendada.</span><span class="sxs-lookup"><span data-stu-id="593ea-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="593ea-123">Tehke loendis valik **Kaaluhulk** ja sisestage siis väljale **Väärtus** koorma kogu kaaluhulga protsent, mida tuleks uuele koorma koostamise strateegiale rakendada.</span><span class="sxs-lookup"><span data-stu-id="593ea-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="593ea-124">Sulgege leht **Koorma koostamise strateegia parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="593ea-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="593ea-125">Sulgege leht **Koorma koostamise strateegiad**.</span><span class="sxs-lookup"><span data-stu-id="593ea-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="593ea-126">Nüüd saate koorma koostamise mallile määrata koorma koostamise strateegia.</span><span class="sxs-lookup"><span data-stu-id="593ea-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="593ea-127">Võite seda kasutada ka koorma planeerimise töölaual.</span><span class="sxs-lookup"><span data-stu-id="593ea-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="593ea-128">Koorma koostamise strateegia kasutamine koorma koostamise töölaual</span><span class="sxs-lookup"><span data-stu-id="593ea-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="593ea-129">Valige **Transpordihaldus &gt; Planeerimine &gt; Koorma koostamise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="593ea-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="593ea-130">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="593ea-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="593ea-131">Valige strateegia väljal **Koorma koostamise strateegia**.</span><span class="sxs-lookup"><span data-stu-id="593ea-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="593ea-132">Kui olete määranud koorma koostamise malli ja määranud sellele koorma koostmaise strateegia, valige toimingupaanilpaani vahekaardil **Mallide haldamine** käsk **Rakenda mall**.</span><span class="sxs-lookup"><span data-stu-id="593ea-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="593ea-133">Seejärel valige rippmenüü dialoogiaknas **Koorma koostamise malli rakendamine** mall väljal **Koorma koostamise malli nimi**.</span><span class="sxs-lookup"><span data-stu-id="593ea-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="593ea-134">Kiirkaardil **Koormamallide järjestus** valige [koormamall](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="593ea-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="593ea-135">Töölaud proovib koormat sobitada seda tüüpi konteineritega siin määratud järjestuses.</span><span class="sxs-lookup"><span data-stu-id="593ea-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="593ea-136">Tavaliselt tuleks loendi algusesse panna väikseimad konteinerid, et esimesena valitaks kindlasti väikseim võimalik konteiner.</span><span class="sxs-lookup"><span data-stu-id="593ea-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="593ea-137">Tehke toimingupaanil valik **Soovita koormaid**.</span><span class="sxs-lookup"><span data-stu-id="593ea-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="593ea-138">Vaadake üle pakutud koormad ja pakutud koormaread.</span><span class="sxs-lookup"><span data-stu-id="593ea-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="593ea-139">Tehke toimingupaanil valik **Loo koormad**, et luua kiirkaardi **Pakutud koormaread** lähtedokumentide ridadel põhinevad koormad.</span><span class="sxs-lookup"><span data-stu-id="593ea-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="593ea-140">Sulgege leht **Koorma koostamise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="593ea-140">Close the **Load building workbench** page.</span></span>
