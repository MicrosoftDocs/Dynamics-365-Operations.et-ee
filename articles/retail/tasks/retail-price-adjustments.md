---
title: " Jaemüügihindade korrigeerimine"
description: See protseduur juhendab jaemüügi hinna korrigeerimisel.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9427d3955e5442e301c416e2960e071ca5d85a3c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "366301"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="cbf40-103"> Jaemüügihindade korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="cbf40-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cbf40-104">See protseduur juhendab jaemüügi hinna korrigeerimisel.</span><span class="sxs-lookup"><span data-stu-id="cbf40-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="cbf40-105">Jaemüügi hinna korrigeerimine saab kauba müügihinda otse muuta või muuta selle baasmüügihinda või kaubandusleppele vastavat hinda.</span><span class="sxs-lookup"><span data-stu-id="cbf40-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="cbf40-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="cbf40-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="cbf40-107">Klõpsake suvandit Hinnakujunduse ja allahindluste haldamine.</span><span class="sxs-lookup"><span data-stu-id="cbf40-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="cbf40-108">Klõpsake vahekaardil Hinna korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="cbf40-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="cbf40-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cbf40-109">Click New.</span></span>
    * <span data-ttu-id="cbf40-110">Siin saate luua kõiki tavaliselt kasutatavaid hindade ja allahindluste reegleid, sh jaemüügi allahindlusi, hinna korrigeerimisi, kaubanduslepete kavasid ja kategooriate hinnareegleid.</span><span class="sxs-lookup"><span data-stu-id="cbf40-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="cbf40-111">Klõpsake valikut Hinna korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="cbf40-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="cbf40-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="cbf40-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="cbf40-113">Laiendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="cbf40-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="cbf40-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cbf40-114">Click Add.</span></span>
    * <span data-ttu-id="cbf40-115">Selles näites sisestage väljale Toode 81126.</span><span class="sxs-lookup"><span data-stu-id="cbf40-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="cbf40-116">Seejärel sisestage väljale Allahindluse protsent 10,0.</span><span class="sxs-lookup"><span data-stu-id="cbf40-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="cbf40-117">Allahindluse protsendi tüüpi hinna korrigeerimine vähendab baasmüügihinda kaubandusleppele vastavat müügihinda.</span><span class="sxs-lookup"><span data-stu-id="cbf40-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="cbf40-118">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cbf40-118">Click Add.</span></span>
    * <span data-ttu-id="cbf40-119">Selles näites sisestage väljale Toode 81125.</span><span class="sxs-lookup"><span data-stu-id="cbf40-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="cbf40-120">Seejärel tehke väljal Allahindluse meetod valik Sularaha allahindluse summa.</span><span class="sxs-lookup"><span data-stu-id="cbf40-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="cbf40-121">Seejärel sisestage väljale Sularaha allahindluse summa väärtus 5,0.</span><span class="sxs-lookup"><span data-stu-id="cbf40-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="cbf40-122">Sularaha allahindluse summa allahindlusetüüp on summa, mis võetakse maha baashinnast või kaubandusleppele vastavast hinnast.</span><span class="sxs-lookup"><span data-stu-id="cbf40-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="cbf40-123">Klõpsake suvandit Hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="cbf40-123">Click Price groups.</span></span>
    * <span data-ttu-id="cbf40-124">Valige väljal Hinnagrupp RP-Houston.</span><span class="sxs-lookup"><span data-stu-id="cbf40-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="cbf40-125">See seostab hinna korrigeerimise Houstoni kauplusega.</span><span class="sxs-lookup"><span data-stu-id="cbf40-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="cbf40-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cbf40-126">Click Save.</span></span>
11. <span data-ttu-id="cbf40-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cbf40-127">Close the page.</span></span>
12. <span data-ttu-id="cbf40-128">Väljal Olek tehke valik Lubatud.</span><span class="sxs-lookup"><span data-stu-id="cbf40-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="cbf40-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cbf40-129">Click Save.</span></span>
14. <span data-ttu-id="cbf40-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cbf40-130">Close the page.</span></span>
15. <span data-ttu-id="cbf40-131">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="cbf40-131">Refresh the page.</span></span>

