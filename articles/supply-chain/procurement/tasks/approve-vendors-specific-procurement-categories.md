---
title: Kindlatele hankekategooriatele hankijate kinnitamine
description: Ostutaotluse loomisel võib olla nõue valida heakskiidetud või eelistatud hankija, olenevalt sellest, kuidas ostupoliitikad on seadistatud.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eec50e2e8f08fabb64f89c17159b97ba770026f8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836332"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="834ef-103">Kindlatele hankekategooriatele hankijate kinnitamine</span><span class="sxs-lookup"><span data-stu-id="834ef-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="834ef-104">Ostutaotluse loomisel võib olla nõue valida heakskiidetud või eelistatud hankija, olenevalt sellest, kuidas ostupoliitikad on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="834ef-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="834ef-105">See protseduur näitab teile, kuidas määrata konkreetse hankekategooria puhul, et hankija on kinnitatud või eelistatud.</span><span class="sxs-lookup"><span data-stu-id="834ef-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="834ef-106">Seda ülesannet täidab tavaliselt hankespetsialist.</span><span class="sxs-lookup"><span data-stu-id="834ef-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="834ef-107">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="834ef-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="834ef-108">Tehke valik Hanked > Hankijad > Kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="834ef-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="834ef-109">Valige hankija, keda soovite kategooria puhul kinnitatud või eelistatud hankijaks määrata.</span><span class="sxs-lookup"><span data-stu-id="834ef-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="834ef-110">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="834ef-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="834ef-111">Klõpsake valikut Kategooriad.</span><span class="sxs-lookup"><span data-stu-id="834ef-111">Click Categories.</span></span>
5. <span data-ttu-id="834ef-112">Klõpsake käsku Lisa kategooria.</span><span class="sxs-lookup"><span data-stu-id="834ef-112">Click Add category.</span></span>
6. <span data-ttu-id="834ef-113">Valige väljalt Kategooria KONTORITARBED (KONTORITARBED).</span><span class="sxs-lookup"><span data-stu-id="834ef-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="834ef-114">Tehke väljal Hankija kategooria olek valik Eelistatud.</span><span class="sxs-lookup"><span data-stu-id="834ef-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="834ef-115">Kategooriale on võimalik määrata mitu eelistatud hankijat.</span><span class="sxs-lookup"><span data-stu-id="834ef-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="834ef-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="834ef-116">Click Save.</span></span>
9. <span data-ttu-id="834ef-117">Tehke valik Hanked > Hankekategooriad.</span><span class="sxs-lookup"><span data-stu-id="834ef-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="834ef-118">Valige puult ETTEV. HANKEKATEGOORIAD \ KONTORITARBED.</span><span class="sxs-lookup"><span data-stu-id="834ef-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="834ef-119">Laiendage jaotist Hankijad.</span><span class="sxs-lookup"><span data-stu-id="834ef-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="834ef-120">Kontrollige, kas valitud hankija on kuvatud eelistatud hankijana kategoorias Kontoritarbed.</span><span class="sxs-lookup"><span data-stu-id="834ef-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="834ef-121">Kui kasutate seda protseduuri tegevusjuhisena, võib olla vaja klõpsata nuppu Ava, et oleks võimalik hankijate loendis alla kerida.</span><span class="sxs-lookup"><span data-stu-id="834ef-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="834ef-122">Sellel lehel saab ka eelistatud ja kinnitatud hankijaid lisada.</span><span class="sxs-lookup"><span data-stu-id="834ef-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="834ef-123">Laiendage puul valikut KONTORITARBED.</span><span class="sxs-lookup"><span data-stu-id="834ef-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="834ef-124">Tehke puul valik Käärid.</span><span class="sxs-lookup"><span data-stu-id="834ef-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="834ef-125">Valige väljalt Tuleta hankijad põhikategooriast: väärtus Ei.</span><span class="sxs-lookup"><span data-stu-id="834ef-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="834ef-126">Valige väljalt Tuleta hankijad põhikategooriast: väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="834ef-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

