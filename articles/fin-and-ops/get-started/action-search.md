---
title: Tegevuse otsing
description: Selles artiklis kirjeldatakse tegevuse otsingu funktsiooni rakenduses Microsoft Dynamics 365 for Finance and Operations. Tegevuste otsing aitab teil leida ka käitada lehel tegevusi.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 960c715c487fbda5d93630327f07380e6d8fbd3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547027"
---
# <a name="action-search"></a><span data-ttu-id="ffa17-104">Tegevuse otsing</span><span class="sxs-lookup"><span data-stu-id="ffa17-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffa17-105">Selles artiklis kirjeldatakse tegevuse otsingu funktsiooni rakenduses Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ffa17-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ffa17-106">Tegevuste otsing aitab teil leida ka käitada lehel tegevusi.</span><span class="sxs-lookup"><span data-stu-id="ffa17-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="ffa17-107">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="ffa17-107">Introduction</span></span>

<span data-ttu-id="ffa17-108">Rakenduses Microsoft Dynamics 365 for Finance and Operations olevad lehed kuvavad käsklusi peamiselt toimingupaanidel – nii standardsel toimingupaanil, mis kuvatakse lehe ülaosas, kui ka tööriistaribadel, mis kuvatakse lehe erinevates jaotistes.</span><span class="sxs-lookup"><span data-stu-id="ffa17-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="ffa17-109">Varasemates versioonides võimaldas klahvinäpunäidete funktsioon teil toimingupaani mis tahes nupule kiiresti juurde pääseda, vajutades Alt-klahvi ja seejärel tähejada.</span><span class="sxs-lookup"><span data-stu-id="ffa17-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="ffa17-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="ffa17-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="ffa17-111">Finance and Operationsi praeguses versioonis pole klahvinäpunäited aga enam saadaval, kuid need on asendatud tegevuse otsimise funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="ffa17-111">However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="ffa17-112">See uus funktsioon võimaldab kiiret otsingut ja nupu käivitamist mis tahes nähtavalt tegevuspaanilt.</span><span class="sxs-lookup"><span data-stu-id="ffa17-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="ffa17-113">Tegevus otsingu kasutamine</span><span class="sxs-lookup"><span data-stu-id="ffa17-113">Using action search</span></span>

<span data-ttu-id="ffa17-114">Tegevuse otsingu funktsiooni kasutamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ffa17-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="ffa17-115">Klõpsake tegevuspaani välja **tegevuse otsing**.</span><span class="sxs-lookup"><span data-stu-id="ffa17-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="ffa17-116">(Väli **Tegevuse otsing** sisaldab suurendusklaasi ikooni.)</span><span class="sxs-lookup"><span data-stu-id="ffa17-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="ffa17-117">Tippige osaliselt või täielikult nupu nimi, mille soovite käivitada.</span><span class="sxs-lookup"><span data-stu-id="ffa17-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="ffa17-118">Saate otsimiseks kasutada ka nupu „tees” olevaid sõnu,</span><span class="sxs-lookup"><span data-stu-id="ffa17-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="ffa17-119">(Lisateavet vt selle artikli järgmisest teemast.) Tavaliselt ilmub nupp tulemuste loendi lähedale pärast kahe kuni nelja tähemärgi tippimist.</span><span class="sxs-lookup"><span data-stu-id="ffa17-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="ffa17-120">Otsige nupp tulemuste loendist üles ja käivitage see (kasutades hiirt ja klaviatuuri).</span><span class="sxs-lookup"><span data-stu-id="ffa17-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="ffa17-121">Pärast nupu käivitamist naaseb fookus lehe viimasesse asukohta ja saate tööd jätkata.</span><span class="sxs-lookup"><span data-stu-id="ffa17-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="ffa17-122">[![tegevuse-otsinguväli](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="ffa17-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="ffa17-123">Saate tegevuste otsingu käivitada ka, vajutades klahve Ctrl+/ või Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="ffa17-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="ffa17-124">Vajutage uuesti kiirklahvi, et fookus naaseks teie viimasele lehe asukohale.</span><span class="sxs-lookup"><span data-stu-id="ffa17-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="ffa17-125">Tulemuste loendi mõistmine</span><span class="sxs-lookup"><span data-stu-id="ffa17-125">Understanding the results list</span></span>

<span data-ttu-id="ffa17-126">Sageli peate Finance and Operationsis teadma nupu otstarbe mõistmiseks nii nupu asukohta kui ka konteksti.</span><span class="sxs-lookup"><span data-stu-id="ffa17-126">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="ffa17-127">Seetõttu kuvatakse tulemuste loendis iga üksuse puhul lisateave, et saaksite täpselt aru, millised nupud loendis kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="ffa17-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="ffa17-128">Eriti kuvatakse nupu tee.</span><span class="sxs-lookup"><span data-stu-id="ffa17-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="ffa17-129">Tee võib vajaduse korral hõlmata järgmiste kasutajaliidese elementide silte.</span><span class="sxs-lookup"><span data-stu-id="ffa17-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="ffa17-130">Toimingupaani vahekaart</span><span class="sxs-lookup"><span data-stu-id="ffa17-130">Action Pane tab</span></span>
- <span data-ttu-id="ffa17-131">Nupu grupp</span><span class="sxs-lookup"><span data-stu-id="ffa17-131">Button group</span></span>
- <span data-ttu-id="ffa17-132">Menüünupp (kui nupp on menüünupu sees)</span><span class="sxs-lookup"><span data-stu-id="ffa17-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="ffa17-133">Menüü eraldaja (kui nupp on menüünupu sees nimega grupis)</span><span class="sxs-lookup"><span data-stu-id="ffa17-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="ffa17-134">Grupp või vahekaart lehel (näiteks kiirkaardi nimi)</span><span class="sxs-lookup"><span data-stu-id="ffa17-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="ffa17-135">Tippisite väljale **Tegevuse otsing** näiteks tähed **kog** ja uurite nüüd tulemuste loendit.</span><span class="sxs-lookup"><span data-stu-id="ffa17-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="ffa17-136">Esimene kirje (nupp **Kogusummad**) on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="ffa17-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="ffa17-137">Kuvatakse ka nupu tee **Müügitellimus** &gt; **Vaade**.</span><span class="sxs-lookup"><span data-stu-id="ffa17-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="ffa17-138">Tee osa **Müügitellimus** vastab tegumiriba vahekaardile **Müügitellimus** ja tee osa **Vaade** vastab selle vahekaardi rühmale **Vaade**. Samamoodi annab nupu **Koguallahindlus** tee (**Müü** &gt; **Arvuta**) teile teada, et see nupp asub tegumiriba vahekaardi **Müü** grupis **Arvuta**.</span><span class="sxs-lookup"><span data-stu-id="ffa17-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="ffa17-139">Seetõttu aitab see teave teil täpselt aru saada, milline nupp tegevuseotsinguga käivitatakse (kui valite selle nupu tulemuste loendist).</span><span class="sxs-lookup"><span data-stu-id="ffa17-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="ffa17-140">[![tegevuste-otsinguväli-koos-andmetega](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="ffa17-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="ffa17-141">Eelmises näites näitas tegevuse otsing tulemusi standardselt toimingupaanilt lehe ülaosas.</span><span class="sxs-lookup"><span data-stu-id="ffa17-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="ffa17-142">Kuid tegevuse otsing näitab ka tulemusi nähtamatutelt tööriistaribadelt, mis asuvad lehe muudes kohtades.</span><span class="sxs-lookup"><span data-stu-id="ffa17-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="ffa17-143">Näiteks otsite nuppu **Vaba kaubavaru**, mis asub kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="ffa17-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ffa17-144">Sellisel juhul teavitab nupu tee tulemuste loendis (**Müügitellimuse read** &gt; **Varud** &gt; **Vaade**), et see nupp asub kiirkaardil **Müügitellimuse read** menüünupu **Varud** päise **Vaade** all.</span><span class="sxs-lookup"><span data-stu-id="ffa17-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="ffa17-145">[![vaba-kaubavaru](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="ffa17-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="ffa17-146">Tegevuse otsing vs navigeerimisotsing</span><span class="sxs-lookup"><span data-stu-id="ffa17-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="ffa17-147">Kui tegevuseotsing on mõeldud tegevuste otsimiseks ja käivitamiseks lehel, siis lehtede otsimiseks ja neil navigeerimiseks on Finance and Operationsis eraldi otsingumehhanism.</span><span class="sxs-lookup"><span data-stu-id="ffa17-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="ffa17-148">Lisateavet selle funktsiooni kohta vt artiklist [Navigeerimisotsing](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="ffa17-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>