---
title: Käibemaksu määramine ja tühistamised
description: See protseduur näitab, kuidas jaemüügikanalitele käibemaksugruppe määrata.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f08829bccbaea6fb70563e553f9042300b4d5ea9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837994"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="d1ac1-103">Käibemaksu määramine ja tühistamised</span><span class="sxs-lookup"><span data-stu-id="d1ac1-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1ac1-104">See protseduur näitab, kuidas jaemüügikanalitele käibemaksugruppe määrata.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="d1ac1-105">Samuti näitab see uue käibemaksu tühistamise loomise protsessi ja selle määramist olemasolevale käibemaksu tühistamise grupile.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="d1ac1-106">Selle protseduuri puhul</span><span class="sxs-lookup"><span data-stu-id="d1ac1-106">This procedure</span></span>

<span data-ttu-id="d1ac1-107">kasutatakse demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d1ac1-108">Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="d1ac1-109">Klõpsake loendis jaemüügikanali ID linki Houston.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="d1ac1-110">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-110">Click Edit.</span></span>
    * <span data-ttu-id="d1ac1-111">Väljal Käibemaksugrupp on praeguse ettevõtte käibemaksugruppide loend.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="d1ac1-112">Praegu määratud grupp on üldine käibemaksugrupp Texas.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="d1ac1-113">On ka käibemaksugrupid "Washington" ja "Washington, Kingi maakond."</span><span class="sxs-lookup"><span data-stu-id="d1ac1-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="d1ac1-114">Käibemaksugruppidesse saate kaasata mitme omavalitsuse asjakohased maksud.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="d1ac1-115">Väljal Käibemaksu tühistamine saab käibemaksu tühistamise gruppe kanaliga vastendada.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="d1ac1-116">Käibemaksu tühistamise gruppe saab kasutada mitme kaupluse puhul toimivate käibemaksu tühistamiste grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="d1ac1-117">Selle asemel, et määrata käibemaksu tühistamisi ükshaaval, saab luua grupi ja määrata selle aja säästmiseks otse kanalitele.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="d1ac1-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-118">Click Save.</span></span>
5. <span data-ttu-id="d1ac1-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-119">Close the page.</span></span>
6. <span data-ttu-id="d1ac1-120">Avage Jaemüük ja kaubandus > Kanali seadistus > Käibemaksud > Käibemaksu tühistamised.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="d1ac1-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-121">Click New.</span></span>
8. <span data-ttu-id="d1ac1-122">Sisestage väljale Käibemaksu tühistamine oma uue tühistamise nimi.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="d1ac1-123">Sisestage tühistamise kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="d1ac1-124">Määrake olekuks Luba.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="d1ac1-125">Laiendage või ahendage jaotist Tühistamine.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="d1ac1-126">Valige suvand väljalt Tüüp.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="d1ac1-127">Kauba käibemaksugruppe saab kasutada konkreetsete gruppi kuuluvate kaupade maksude alistamiseks.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="d1ac1-128">Näiteks toidukaupu maksustatakse tavaliselt tarbekaupadest erinevalt ja neil on tõenäoliselt oma käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="d1ac1-129">Käibemaksugrupid on konkreetsele kanalile rakendatavad maksude grupid.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="d1ac1-130">Näiteks kui kanal teeb nii jaemüüki kui ka ettevõtetevahelist müüki, võidakse kasutada erinevaid kaupade käibemaksugruppe.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="d1ac1-131">Kõik kohaldatavad maksud vastendatakse käibemaksugrupiga.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="d1ac1-132">Nüüd saate teha käibemaksu tühistamise loomiseks maksude kohta valikuid Algväärtus ja Sihtväärtus või Maksugrupist ja Maksugrupiks.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="d1ac1-133">Väli Algväärtus tähistab tühistatavat maksu või maksugruppi.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="d1ac1-134">Kauba käibemaksugrupi järgi tühistamine annab teistsuguseid valikuid kui käibemaksugrupi järgi tühistamine.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="d1ac1-135">Käibemaksu tühistamised saab seadistada nii, et maksud tühistatakse kõigil kannetel või konkreetsetel kande ridadel.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="d1ac1-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-136">Click Save.</span></span>
14. <span data-ttu-id="d1ac1-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-137">Close the page.</span></span>
15. <span data-ttu-id="d1ac1-138">Avage Jaemüük ja kaubandus > Kanali seadistus > Käibemaksud > Käibemaksu tühistamise grupid.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="d1ac1-139">Selles etapis määrate äsja loodud käibemaksu alistamise Houstoni kanalile määratud käibemaksu alistamise grupile.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="d1ac1-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-140">Click Edit.</span></span>
17. <span data-ttu-id="d1ac1-141">Laiendage või ahendage jaotist Häälestus.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="d1ac1-142">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-142">Click Add.</span></span>
19. <span data-ttu-id="d1ac1-143">Klõpsake väljal Käibemaksu tühistamine otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="d1ac1-144">Valige loendist eelnevalt loodud käibemaksu tühistamine.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="d1ac1-145">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="d1ac1-146">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-146">Click Save.</span></span>

