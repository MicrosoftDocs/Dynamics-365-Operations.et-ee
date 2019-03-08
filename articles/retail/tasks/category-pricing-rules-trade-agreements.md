---
title: " Kategooria hinnakujunduse reeglid, et luua kaubanduslepped"
description: Protseduur näitab, kuidas luua müügihinna kaubandusleppeid kategooria hinnakujunduse reegli abiga.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d252982cf1e4fa2f06646d0909e6f82d16f4cfc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355514"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="1dc60-103"> Kategooria hinnakujunduse reeglid, et luua kaubanduslepped</span><span class="sxs-lookup"><span data-stu-id="1dc60-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1dc60-104">Protseduur näitab, kuidas luua müügihinna kaubandusleppeid kategooria hinnakujunduse reegli abiga.</span><span class="sxs-lookup"><span data-stu-id="1dc60-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="1dc60-105">Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="1dc60-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="1dc60-106">See ülesanne on mõeldud jaemüügi tootejuhi rolli jaoks.</span><span class="sxs-lookup"><span data-stu-id="1dc60-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="1dc60-107">Klõpsake suvandit Hinnakujunduse ja allahindluste haldamine.</span><span class="sxs-lookup"><span data-stu-id="1dc60-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="1dc60-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1dc60-108">Click New.</span></span>
3. <span data-ttu-id="1dc60-109">Klõpsake suvandit Kategooria hinnareegel.</span><span class="sxs-lookup"><span data-stu-id="1dc60-109">Click Category price rule.</span></span>
4. <span data-ttu-id="1dc60-110">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1dc60-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="1dc60-111">Valige suvand väljal Konto kood.</span><span class="sxs-lookup"><span data-stu-id="1dc60-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="1dc60-112">Konto koodi, mille tüüp on „Grupp”, kasutatakse spetsiaalselt kanalite, püsikliendiprogrammide, kataloogide ja kuuluvuste jaoks mõeldud müügihinna kaubanduslepete häälestamiseks.</span><span class="sxs-lookup"><span data-stu-id="1dc60-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="1dc60-113">Valige või sisestage väärtus väljal Konto valik.</span><span class="sxs-lookup"><span data-stu-id="1dc60-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="1dc60-114">Valige või sisestage väärtus väljal Kategooria.</span><span class="sxs-lookup"><span data-stu-id="1dc60-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="1dc60-115">Sisestage number väljale Summa/protsent.</span><span class="sxs-lookup"><span data-stu-id="1dc60-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="1dc60-116">Valige või sisestage väärtus väljal Ümardamisversioon.</span><span class="sxs-lookup"><span data-stu-id="1dc60-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="1dc60-117">Klõpsake suvandit Kaubanduslepete loomine.</span><span class="sxs-lookup"><span data-stu-id="1dc60-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="1dc60-118">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="1dc60-118">Click Next.</span></span>
12. <span data-ttu-id="1dc60-119">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="1dc60-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="1dc60-120">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="1dc60-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="1dc60-121">Valige väljal Otsi järgmine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="1dc60-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="1dc60-122">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="1dc60-122">Click Next.</span></span>
16. <span data-ttu-id="1dc60-123">Klõpsake Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="1dc60-123">Click Finish.</span></span>
    * <span data-ttu-id="1dc60-124">See loob kaubandusleppe töölehe ja avab selle ülevaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="1dc60-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="1dc60-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1dc60-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1dc60-126">Kategooria hinnakujunduse reeglitest loodud kaubandusleppe töölehti ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="1dc60-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="1dc60-127">Enne sisestamist saate hinnad üle vaadata ja neid muuta.</span><span class="sxs-lookup"><span data-stu-id="1dc60-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="1dc60-128">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="1dc60-128">Click Edit.</span></span>
19. <span data-ttu-id="1dc60-129">Sisestage arv väljale Summa valuutas.</span><span class="sxs-lookup"><span data-stu-id="1dc60-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="1dc60-130">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="1dc60-130">Click Post.</span></span>
21. <span data-ttu-id="1dc60-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1dc60-131">Click OK.</span></span>
22. <span data-ttu-id="1dc60-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1dc60-132">Close the page.</span></span>
23. <span data-ttu-id="1dc60-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1dc60-133">Close the page.</span></span>
24. <span data-ttu-id="1dc60-134">Klõpsake vahekaarti Kategooria hinna reeglid.</span><span class="sxs-lookup"><span data-stu-id="1dc60-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="1dc60-135">Loend hõlmab kanalipõhiseid kategooria hinnakujunduse reeglid.</span><span class="sxs-lookup"><span data-stu-id="1dc60-135">Channel specific Category pricing rules will show in this list.</span></span>  

