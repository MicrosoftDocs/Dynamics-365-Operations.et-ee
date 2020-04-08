---
title: Kindlatele hankekategooriatele hankijate kinnitamine
description: Selles teemas selgitatakse, kuidas kinnitada hankijaid konkreetsetele hanke kategooriatele Dynamics 365 Supply Chain Management.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
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
ms.openlocfilehash: 135b3a6bea2c0a8940550299504139551c9c3559
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147499"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="41a85-103">Kindlatele hankekategooriatele hankijate kinnitamine</span><span class="sxs-lookup"><span data-stu-id="41a85-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41a85-104">Selles teemas selgitatakse, kuidas kinnitada hankijaid konkreetsetele hanke kategooriatele Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="41a85-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="41a85-105">Ostutaotluse loomisel võib olla nõue valida heakskiidetud või eelistatud hankija, olenevalt sellest, kuidas ostupoliitikad on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="41a85-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="41a85-106">See protseduur näitab teile, kuidas määrata konkreetse hankekategooria puhul, et hankija on kinnitatud või eelistatud.</span><span class="sxs-lookup"><span data-stu-id="41a85-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="41a85-107">Seda ülesannet täidab tavaliselt hankespetsialist.</span><span class="sxs-lookup"><span data-stu-id="41a85-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="41a85-108">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="41a85-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="41a85-109">Navigeerimispaanil avage **Moodulid > Hanked > Hankijad > Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="41a85-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="41a85-110">Valige hankija, keda soovite kategooria puhul kinnitatud või eelistatud hankijaks määrata.</span><span class="sxs-lookup"><span data-stu-id="41a85-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="41a85-111">Valige toimingupaanil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="41a85-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="41a85-112">Valige **Kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="41a85-112">Select **Categories**.</span></span>
5. <span data-ttu-id="41a85-113">Valige **Lisa kategooria**.</span><span class="sxs-lookup"><span data-stu-id="41a85-113">Select **Add category**.</span></span>
6. <span data-ttu-id="41a85-114">Valige väljalt **Kategooria** **KONTORITARBED (KONTORITARBED)**.</span><span class="sxs-lookup"><span data-stu-id="41a85-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="41a85-115">Tehke väljal **Hankija kategooria olek** valik **Eelistatud**.</span><span class="sxs-lookup"><span data-stu-id="41a85-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="41a85-116">Kategooriale on võimalik määrata mitu eelistatud hankijat.</span><span class="sxs-lookup"><span data-stu-id="41a85-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="41a85-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="41a85-117">Select **Save**.</span></span>
9. <span data-ttu-id="41a85-118">Navigeerimispaanil avage **Moodulid > Hanked > Hanke kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="41a85-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="41a85-119">Valige puult **ETTEV. HANKEKATEGOORIAD \ KONTORITARBED**.</span><span class="sxs-lookup"><span data-stu-id="41a85-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="41a85-120">Laiendage jaotist **Hankijad**.</span><span class="sxs-lookup"><span data-stu-id="41a85-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="41a85-121">Kontrollige, kas valitud hankija on kuvatud eelistatud hankijana kategoorias Kontoritarbed.</span><span class="sxs-lookup"><span data-stu-id="41a85-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="41a85-122">Kui kasutate seda protseduuri tegevusjuhisena, võib olla vaja valida nuppu **Ava**, et oleks võimalik hankijate loendis alla kerida.</span><span class="sxs-lookup"><span data-stu-id="41a85-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="41a85-123">Sellel lehel saab ka eelistatud ja kinnitatud hankijaid lisada.</span><span class="sxs-lookup"><span data-stu-id="41a85-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="41a85-124">Puus laiendage **KONTORITARBED** ning valige **Käärid**.</span><span class="sxs-lookup"><span data-stu-id="41a85-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="41a85-125">Valige väljalt **Tuleta hankijad põhikategooriast:** väärtus **Ei**.</span><span class="sxs-lookup"><span data-stu-id="41a85-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="41a85-126">Valige väljalt **Tuleta hankijad põhikategooriast:** väärtus **Jah**.</span><span class="sxs-lookup"><span data-stu-id="41a85-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

