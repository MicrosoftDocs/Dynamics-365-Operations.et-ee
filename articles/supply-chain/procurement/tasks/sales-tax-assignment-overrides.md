---
title: Käibemaksu määramine ja tühistamised
description: See protseduur näitab, kuidas kaubanduse kanalitele käibemaksugruppe määrata.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c6e1de5046a3ce5d896ba3686a28d6d474d4268
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020724"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="2cae9-103">Käibemaksu määramine ja tühistamised</span><span class="sxs-lookup"><span data-stu-id="2cae9-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2cae9-104">See protseduur näitab, kuidas kaubanduse kanalitele käibemaksugruppe määrata.</span><span class="sxs-lookup"><span data-stu-id="2cae9-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="2cae9-105">Samuti näitab see uue käibemaksu tühistamise loomise protsessi ja selle määramist olemasolevale käibemaksu tühistamise grupile.</span><span class="sxs-lookup"><span data-stu-id="2cae9-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="2cae9-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="2cae9-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2cae9-107">Minge jaotisse Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused.</span><span class="sxs-lookup"><span data-stu-id="2cae9-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="2cae9-108">Klõpsake loendis kanali ID linki „Houston”.</span><span class="sxs-lookup"><span data-stu-id="2cae9-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="2cae9-109">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="2cae9-109">Click Edit.</span></span>
    * <span data-ttu-id="2cae9-110">Väljal Käibemaksugrupp on praeguse ettevõtte käibemaksugruppide loend.</span><span class="sxs-lookup"><span data-stu-id="2cae9-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="2cae9-111">Praegu määratud grupp on üldine käibemaksugrupp Texas.</span><span class="sxs-lookup"><span data-stu-id="2cae9-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="2cae9-112">On ka käibemaksugrupid "Washington" ja "Washington, Kingi maakond."</span><span class="sxs-lookup"><span data-stu-id="2cae9-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="2cae9-113">Käibemaksugruppidesse saate kaasata mitme omavalitsuse asjakohased maksud.</span><span class="sxs-lookup"><span data-stu-id="2cae9-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="2cae9-114">Väljal Käibemaksu tühistamine saab käibemaksu tühistamise gruppe kanaliga vastendada.</span><span class="sxs-lookup"><span data-stu-id="2cae9-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="2cae9-115">Käibemaksu tühistamise gruppe saab kasutada mitme kaupluse puhul toimivate käibemaksu tühistamiste grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="2cae9-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="2cae9-116">Selle asemel, et määrata käibemaksu tühistamisi ükshaaval, saab luua grupi ja määrata selle aja säästmiseks otse kanalitele.</span><span class="sxs-lookup"><span data-stu-id="2cae9-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="2cae9-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2cae9-117">Click Save.</span></span>
5. <span data-ttu-id="2cae9-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2cae9-118">Close the page.</span></span>
6. <span data-ttu-id="2cae9-119">Avage Jaemüük ja kaubandus > Kanali seadistus > Käibemaksud > Käibemaksu tühistamised.</span><span class="sxs-lookup"><span data-stu-id="2cae9-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="2cae9-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2cae9-120">Click New.</span></span>
8. <span data-ttu-id="2cae9-121">Sisestage väljale Käibemaksu tühistamine oma uue tühistamise nimi.</span><span class="sxs-lookup"><span data-stu-id="2cae9-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="2cae9-122">Sisestage tühistamise kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="2cae9-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="2cae9-123">Määrake olekuks Luba.</span><span class="sxs-lookup"><span data-stu-id="2cae9-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="2cae9-124">Laiendage või ahendage jaotist Tühistamine.</span><span class="sxs-lookup"><span data-stu-id="2cae9-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="2cae9-125">Valige suvand väljalt Tüüp.</span><span class="sxs-lookup"><span data-stu-id="2cae9-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="2cae9-126">Kauba käibemaksugruppe saab kasutada konkreetsete gruppi kuuluvate kaupade maksude alistamiseks.</span><span class="sxs-lookup"><span data-stu-id="2cae9-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="2cae9-127">Näiteks toidukaupu maksustatakse tavaliselt tarbekaupadest erinevalt ja neil on tõenäoliselt oma käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="2cae9-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="2cae9-128">Käibemaksugrupid on konkreetsele kanalile rakendatavad maksude grupid.</span><span class="sxs-lookup"><span data-stu-id="2cae9-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="2cae9-129">Näiteks kui kanal teeb nii jaemüüki kui ka ettevõtetevahelist müüki, võidakse kasutada erinevaid kaupade käibemaksugruppe.</span><span class="sxs-lookup"><span data-stu-id="2cae9-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="2cae9-130">Kõik kohaldatavad maksud vastendatakse käibemaksugrupiga.</span><span class="sxs-lookup"><span data-stu-id="2cae9-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="2cae9-131">Nüüd saate teha käibemaksu tühistamise loomiseks maksude kohta valikuid Algväärtus ja Sihtväärtus või Maksugrupist ja Maksugrupiks.</span><span class="sxs-lookup"><span data-stu-id="2cae9-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="2cae9-132">Väli Algväärtus tähistab tühistatavat maksu või maksugruppi.</span><span class="sxs-lookup"><span data-stu-id="2cae9-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="2cae9-133">Kauba käibemaksugrupi järgi tühistamine annab teistsuguseid valikuid kui käibemaksugrupi järgi tühistamine.</span><span class="sxs-lookup"><span data-stu-id="2cae9-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="2cae9-134">Käibemaksu tühistamised saab seadistada nii, et maksud tühistatakse kõigil kannetel või konkreetsetel kande ridadel.</span><span class="sxs-lookup"><span data-stu-id="2cae9-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="2cae9-135">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2cae9-135">Click Save.</span></span>
14. <span data-ttu-id="2cae9-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2cae9-136">Close the page.</span></span>
15. <span data-ttu-id="2cae9-137">Avage Jaemüük ja kaubandus > Kanali seadistus > Käibemaksud > Käibemaksu tühistamise grupid.</span><span class="sxs-lookup"><span data-stu-id="2cae9-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="2cae9-138">Selles etapis määrate äsja loodud käibemaksu alistamise Houstoni kanalile määratud käibemaksu alistamise grupile.</span><span class="sxs-lookup"><span data-stu-id="2cae9-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="2cae9-139">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="2cae9-139">Click Edit.</span></span>
17. <span data-ttu-id="2cae9-140">Laiendage või ahendage jaotist Häälestus.</span><span class="sxs-lookup"><span data-stu-id="2cae9-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="2cae9-141">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="2cae9-141">Click Add.</span></span>
19. <span data-ttu-id="2cae9-142">Klõpsake väljal Käibemaksu tühistamine otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="2cae9-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="2cae9-143">Valige loendist eelnevalt loodud käibemaksu tühistamine.</span><span class="sxs-lookup"><span data-stu-id="2cae9-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="2cae9-144">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2cae9-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="2cae9-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2cae9-145">Click Save.</span></span>

