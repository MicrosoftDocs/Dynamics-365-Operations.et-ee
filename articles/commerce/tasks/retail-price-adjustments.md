---
title: " Jaemüügihindade korrigeerimine"
description: See protseduur juhendab teid kaubanduse hinna korrigeerimisel.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e6ce8ca1d9f63e7ddf6af897a6de5544e4edd9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802571"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="7c7ff-103"> Jaemüügihindade korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="7c7ff-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c7ff-104">See protseduur juhendab teid kaubanduse hinna korrigeerimisel.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="7c7ff-105">Hinna korrigeerimine saab kauba müügihinda otse muuta või muuta selle baasmüügihinda või kaubandusleppele vastavat hinda.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="7c7ff-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="7c7ff-107">Klõpsake suvandit Hinnakujunduse ja allahindluste haldamine.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="7c7ff-108">Klõpsake vahekaardil Hinna korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="7c7ff-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-109">Click New.</span></span>
    * <span data-ttu-id="7c7ff-110">Siin saate luua kõiki tavaliselt kasutatavaid hindade ja allahindluste reegleid, sh allahindlused, hinna korrigeerimised, kaubanduslepete kavad ja kategooriate hinnareeglid.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="7c7ff-111">Klõpsake valikut Hinna korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="7c7ff-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="7c7ff-113">Laiendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="7c7ff-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-114">Click Add.</span></span>
    * <span data-ttu-id="7c7ff-115">Selles näites sisestage väljale Toode 81126.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="7c7ff-116">Seejärel sisestage väljale Allahindluse protsent 10,0.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="7c7ff-117">Allahindluse protsendi tüüpi hinna korrigeerimine vähendab baasmüügihinda kaubandusleppele vastavat müügihinda.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="7c7ff-118">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-118">Click Add.</span></span>
    * <span data-ttu-id="7c7ff-119">Selles näites sisestage väljale Toode 81125.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="7c7ff-120">Seejärel tehke väljal Allahindluse meetod valik Sularaha allahindluse summa.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="7c7ff-121">Seejärel sisestage väljale Sularaha allahindluse summa väärtus 5,0.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="7c7ff-122">Sularaha allahindluse summa allahindlusetüüp on summa, mis võetakse maha baashinnast või kaubandusleppele vastavast hinnast.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="7c7ff-123">Klõpsake suvandit Hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-123">Click Price groups.</span></span>
    * <span data-ttu-id="7c7ff-124">Valige väljal Hinnagrupp RP-Houston.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="7c7ff-125">See seostab hinna korrigeerimise Houstoni kauplusega.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="7c7ff-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-126">Click Save.</span></span>
11. <span data-ttu-id="7c7ff-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-127">Close the page.</span></span>
12. <span data-ttu-id="7c7ff-128">Väljal Olek tehke valik Lubatud.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="7c7ff-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-129">Click Save.</span></span>
14. <span data-ttu-id="7c7ff-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-130">Close the page.</span></span>
15. <span data-ttu-id="7c7ff-131">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="7c7ff-131">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]