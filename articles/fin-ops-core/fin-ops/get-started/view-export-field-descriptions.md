---
title: Väljade kirjelduste vaatamine ja eksportimine
description: Selles artiklis kirjeldatakse, kuidas vaadata väljade kirjeldusi ja kuidas kasutada väljade kirjelduste lehte kirjelduste eksportimiseks.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 974f99632738cfc6eec5ff85965f4e9f9608a8b5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177470"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="047d6-103">Väljade kirjelduste vaatamine ja eksportimine</span><span class="sxs-lookup"><span data-stu-id="047d6-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="047d6-104">Selles artiklis kirjeldatakse, kuidas vaadata väljade kirjeldusi ja kuidas kasutada väljade kirjelduste lehte kirjelduste eksportimiseks.</span><span class="sxs-lookup"><span data-stu-id="047d6-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="047d6-105">Mõnedel keerukamatel väljadel on välja kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="047d6-105">Some of the more complex fields have field descriptions.</span></span> <span data-ttu-id="047d6-106">Need kirjeldused kuvatakse, kui liigute välja kohale.</span><span class="sxs-lookup"><span data-stu-id="047d6-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="047d6-107">Väljade kirjeldusi saab vaadata ja eksportida ka lehel **Väljade kirjeldused**.</span><span class="sxs-lookup"><span data-stu-id="047d6-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="047d6-108">Kõigil lehekülgedel ei ole väljade kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="047d6-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="047d6-109">Soovime pakkuda kirjeldusi ainult keerukamate väljade jaoks, mitte nende väljade jaoks, mille kasutamine on ilmselge.</span><span class="sxs-lookup"><span data-stu-id="047d6-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="047d6-110">Seetõttu pole mõnel lehel väljade kirjeldusi, mõnel lehel on mõned kirjeldused ja mõnel keerukamal lehel (nt paljudel parameetrilehtedel) on palju kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="047d6-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="047d6-111">Kui teil on juurdepääs arenduskeskkonnale, saate lisada uusi väljade kirjeldusi ja kohandada olemasolevaid kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="047d6-111">If you have access to the development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="047d6-112">Näiteks saate lisada välja kirjeldusele ettevõttepõhist teavet.</span><span class="sxs-lookup"><span data-stu-id="047d6-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="047d6-113">Lisateavet leiate jaotisest [Välja spikri kohandamine](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="047d6-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="047d6-114">Väljakirjelduste vaatamine kasutajaliideses</span><span class="sxs-lookup"><span data-stu-id="047d6-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="047d6-115">Välja kirjelduse vaatamiseks liikuge välja kohale.</span><span class="sxs-lookup"><span data-stu-id="047d6-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="047d6-116">Kui kirjeldus puudub, näete välja kohale liikudes välja nime.</span><span class="sxs-lookup"><span data-stu-id="047d6-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="047d6-117">Dynamics AX-i versioonis 7.0 (veebruar 2016) saab väljakirjeldusi vaadata ainult lehel **Väljade kirjeldused**.</span><span class="sxs-lookup"><span data-stu-id="047d6-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="047d6-118">Järgmisel joonisel on näha väljakirjeldus, mis kuvatakse, kui liigute välja **Lukusta kaubad inventuuri ajaks** kohale.</span><span class="sxs-lookup"><span data-stu-id="047d6-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="047d6-119">[![Väljakirjelduse näide](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="047d6-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="047d6-120">Kasutage lehte Väljade kirjeldused väljaspikri vaatamiseks ja eksportimiseks</span><span class="sxs-lookup"><span data-stu-id="047d6-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="047d6-121">Leht **Väljade kirjeldused** võimaldab väljade kirjeldusi vaadata ja eksportida.</span><span class="sxs-lookup"><span data-stu-id="047d6-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="047d6-122">Saate korraga vaadata ühe lehe jaoks saadaolevaid kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="047d6-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="047d6-123">Vaadake lehe kirjeldusi</span><span class="sxs-lookup"><span data-stu-id="047d6-123">View the descriptions for a page</span></span>

<span data-ttu-id="047d6-124">Lehe kirjelduste vaatamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="047d6-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="047d6-125">Sisestage väljale **Lehe valimine** lehe nimi.</span><span class="sxs-lookup"><span data-stu-id="047d6-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="047d6-126">Teise võimalusena klõpsake noolt kõigi lehtede loendi avamiseks ja seejärel sirvige või filtreerige loendit.</span><span class="sxs-lookup"><span data-stu-id="047d6-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="047d6-127">Saate kasutada kasutajaliideses kuvatavat lehe nime (nt **Kliendid**) või lehe koodnime (AOT-nime), mis on kättesaadav lehele paremklõpsates (nt **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="047d6-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="047d6-128">Teavet mitmesuguste võimaluste kohta lehtede loendi filtreerimiseks leiate selle artikli edasisest osast „Lehe otsimine”.</span><span class="sxs-lookup"><span data-stu-id="047d6-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="047d6-129">Kui määrate valiku **Kaasa ilma kirjelduseta väljad** väärtuseks **Jah**, kuvatakse kõik lehe väljad, olenemata sellest, kas neil on kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="047d6-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="047d6-130">Ekspordi lehe kirjeldused</span><span class="sxs-lookup"><span data-stu-id="047d6-130">Export the descriptions for a page</span></span>

<span data-ttu-id="047d6-131">Kirjelduste eksportimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="047d6-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="047d6-132">Valige leht väljalt **Lehe valimine**.</span><span class="sxs-lookup"><span data-stu-id="047d6-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="047d6-133">Klõpsake paremas ülanurgas nuppu **Ava Microsoft Office’is** ja siis klõpsake suvandit **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="047d6-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="047d6-134">Lehe otsimine</span><span class="sxs-lookup"><span data-stu-id="047d6-134">Searching for a page</span></span>

<span data-ttu-id="047d6-135">Lehe otsimiseks väljal **Lehe valimine** on mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="047d6-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="047d6-136">Paljudel juhtudel tuleb klõpsata noolt väljal **Lehe valimine**, et avada ripploend ja valida siis filtreeritud lehtede loendist.</span><span class="sxs-lookup"><span data-stu-id="047d6-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="047d6-137">Sisestage nime osa ning avage siis ripploend, et filtreeritud lehtede loendist valida.</span><span class="sxs-lookup"><span data-stu-id="047d6-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="047d6-138">Avage ripploend ja klõpsake siis pealkirja **Lehe nimi** loendi ülaosas või pealkirja **Lehe AOT-nimi**.</span><span class="sxs-lookup"><span data-stu-id="047d6-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="047d6-139">Avaneb dialoogiboks, kus saate kasutada täpsema filtreerimise valikuid, nt **Lehe nimi algab tähega**.</span><span class="sxs-lookup"><span data-stu-id="047d6-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="047d6-140">Sisestage lehe täisnimi</span><span class="sxs-lookup"><span data-stu-id="047d6-140">Type the full name of the page.</span></span> <span data-ttu-id="047d6-141">Selle valiku kasutamisel tasub avada ripploend ja vaadata, mida see veel sisaldab, ka siis, kui väljade kirjeldused on nähtavad.</span><span class="sxs-lookup"><span data-stu-id="047d6-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="047d6-142">Kui nimele on üks täpne vaste, näidatakse selle lehe väljade kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="047d6-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="047d6-143">Kui on mitu täpset vastet, ei kuvata ühtegi kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="047d6-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="047d6-144">Peate ripploendi avama ja valima soovitud lehe.</span><span class="sxs-lookup"><span data-stu-id="047d6-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="047d6-145">Kui sisestatud lehe nimi on osa teise lehe nimest, näete oma lehe kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="047d6-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="047d6-146">Kuid kui avate ripploendi, siis näete veel lehti, mis seda nime sisaldavad.</span><span class="sxs-lookup"><span data-stu-id="047d6-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="047d6-147">Näiteks ei kuvata ühtegi kirjeldust, kui sisestate sõna **Inventuur** väljale **Lehe valimine**.</span><span class="sxs-lookup"><span data-stu-id="047d6-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="047d6-148">Avate ripploendi ja näete, et on olemas kaks lehte nimega **Inventuur** ja mitu lehte, mille nimes on sõna „inventuur”.</span><span class="sxs-lookup"><span data-stu-id="047d6-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="047d6-149">Kui valite lehe, mille AOT-nimi on **InventJournalCount**, kuvatakse selle lehe väljade kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="047d6-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="047d6-150">Kui aga ripploendi uuesti avate, näete, et loend sisaldab nüüd kõiki lehti, mille AOT-nime osa on „InventJournalCount”.</span><span class="sxs-lookup"><span data-stu-id="047d6-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="047d6-151">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="047d6-151">Troubleshooting</span></span>

<span data-ttu-id="047d6-152">Selles jaotises on teave, mis on abiks veaotsingul probleemide osas, millega võite väljade kirjelduste kasutamisel kokku puutuda.</span><span class="sxs-lookup"><span data-stu-id="047d6-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="047d6-153">Ma ei leia välja kirjeldust</span><span class="sxs-lookup"><span data-stu-id="047d6-153">I can't find a field description</span></span>

<span data-ttu-id="047d6-154">Praegu on käimas kirjelduste lisamise toiming keerulisematele väljadele.</span><span class="sxs-lookup"><span data-stu-id="047d6-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="047d6-155">Kui vajate konkreetse välja puhul abi, andke meile sellest teada, lisades sellele teemale kommentaari.</span><span class="sxs-lookup"><span data-stu-id="047d6-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="047d6-156">Välja kirjeldusest ei ole abi</span><span class="sxs-lookup"><span data-stu-id="047d6-156">The field description isn't helpful</span></span>

<span data-ttu-id="047d6-157">Andke meile sellest teada, lisades sellele teemale kommentaari.</span><span class="sxs-lookup"><span data-stu-id="047d6-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="047d6-158">Võimaluse korral kirjeldage lisateavet, mida vajate.</span><span class="sxs-lookup"><span data-stu-id="047d6-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="047d6-159">Ma ei leia lehelt Väljade kirjeldused välja.</span><span class="sxs-lookup"><span data-stu-id="047d6-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="047d6-160">Kõigi väljade kuvamiseks lehel määrake valiku **Kaasa ilma kirjelduseta väljad** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="047d6-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="047d6-161">Klõpsake välja **Lehe valimine** kontrollimiseks, kas olete õige lehe valinud.</span><span class="sxs-lookup"><span data-stu-id="047d6-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="047d6-162">Kui sisestatud nimi on osa teise välja nimest, siis valisite võib-olla lehe, millel on pikem nimi.</span><span class="sxs-lookup"><span data-stu-id="047d6-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="047d6-163">Ma ei leia lehelt Väljade kirjeldused lehte.</span><span class="sxs-lookup"><span data-stu-id="047d6-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="047d6-164">Teavet mitmesuguste võimaluste kohta lehtede otsimiseks leiate selle artikli varasemast osast „Lehtede otsimine”.</span><span class="sxs-lookup"><span data-stu-id="047d6-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="047d6-165">Kui sisestasite lehe täpse nime, ei pruugi väljade kirjeldusi näha olla, kui sama nimi on mitmel lehel.</span><span class="sxs-lookup"><span data-stu-id="047d6-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="047d6-166">Klõpsake noolt väljal **Lehe valimine**, et avada saadaolevate lehtede filtreeritud loend.</span><span class="sxs-lookup"><span data-stu-id="047d6-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="047d6-167">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="047d6-167">Additional resources</span></span>

[<span data-ttu-id="047d6-168">Väljaspikri kohandamine</span><span class="sxs-lookup"><span data-stu-id="047d6-168">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)
