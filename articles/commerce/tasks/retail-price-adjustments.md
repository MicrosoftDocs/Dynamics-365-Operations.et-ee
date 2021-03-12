---
title: " Jaemüügihindade korrigeerimine"
description: See protseduur juhendab teid kaubanduse hinna korrigeerimisel.
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7443f69473c0aad478d47f80f284b1156bad9c24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962981"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="39a6c-103"> Jaemüügihindade korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="39a6c-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39a6c-104">See protseduur juhendab teid kaubanduse hinna korrigeerimisel.</span><span class="sxs-lookup"><span data-stu-id="39a6c-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="39a6c-105">Hinna korrigeerimine saab kauba müügihinda otse muuta või muuta selle baasmüügihinda või kaubandusleppele vastavat hinda.</span><span class="sxs-lookup"><span data-stu-id="39a6c-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="39a6c-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="39a6c-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="39a6c-107">Klõpsake suvandit Hinnakujunduse ja allahindluste haldamine.</span><span class="sxs-lookup"><span data-stu-id="39a6c-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="39a6c-108">Klõpsake vahekaardil Hinna korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="39a6c-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="39a6c-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="39a6c-109">Click New.</span></span>
    * <span data-ttu-id="39a6c-110">Siin saate luua kõiki tavaliselt kasutatavaid hindade ja allahindluste reegleid, sh allahindlused, hinna korrigeerimised, kaubanduslepete kavad ja kategooriate hinnareeglid.</span><span class="sxs-lookup"><span data-stu-id="39a6c-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="39a6c-111">Klõpsake valikut Hinna korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="39a6c-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="39a6c-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="39a6c-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="39a6c-113">Laiendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="39a6c-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="39a6c-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="39a6c-114">Click Add.</span></span>
    * <span data-ttu-id="39a6c-115">Selles näites sisestage väljale Toode 81126.</span><span class="sxs-lookup"><span data-stu-id="39a6c-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="39a6c-116">Seejärel sisestage väljale Allahindluse protsent 10,0.</span><span class="sxs-lookup"><span data-stu-id="39a6c-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="39a6c-117">Allahindluse protsendi tüüpi hinna korrigeerimine vähendab baasmüügihinda kaubandusleppele vastavat müügihinda.</span><span class="sxs-lookup"><span data-stu-id="39a6c-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="39a6c-118">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="39a6c-118">Click Add.</span></span>
    * <span data-ttu-id="39a6c-119">Selles näites sisestage väljale Toode 81125.</span><span class="sxs-lookup"><span data-stu-id="39a6c-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="39a6c-120">Seejärel tehke väljal Allahindluse meetod valik Sularaha allahindluse summa.</span><span class="sxs-lookup"><span data-stu-id="39a6c-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="39a6c-121">Seejärel sisestage väljale Sularaha allahindluse summa väärtus 5,0.</span><span class="sxs-lookup"><span data-stu-id="39a6c-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="39a6c-122">Sularaha allahindluse summa allahindlusetüüp on summa, mis võetakse maha baashinnast või kaubandusleppele vastavast hinnast.</span><span class="sxs-lookup"><span data-stu-id="39a6c-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="39a6c-123">Klõpsake suvandit Hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="39a6c-123">Click Price groups.</span></span>
    * <span data-ttu-id="39a6c-124">Valige väljal Hinnagrupp RP-Houston.</span><span class="sxs-lookup"><span data-stu-id="39a6c-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="39a6c-125">See seostab hinna korrigeerimise Houstoni kauplusega.</span><span class="sxs-lookup"><span data-stu-id="39a6c-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="39a6c-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="39a6c-126">Click Save.</span></span>
11. <span data-ttu-id="39a6c-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="39a6c-127">Close the page.</span></span>
12. <span data-ttu-id="39a6c-128">Väljal Olek tehke valik Lubatud.</span><span class="sxs-lookup"><span data-stu-id="39a6c-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="39a6c-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="39a6c-129">Click Save.</span></span>
14. <span data-ttu-id="39a6c-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="39a6c-130">Close the page.</span></span>
15. <span data-ttu-id="39a6c-131">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="39a6c-131">Refresh the page.</span></span>

