---
title: Kuluobjektid
description: "Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d43ea6c0d80a1602f298bbbedb88dd8f7decca4e
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="cost-objects"></a><span data-ttu-id="0faa3-105">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="0faa3-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0faa3-106">Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse.</span><span class="sxs-lookup"><span data-stu-id="0faa3-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="0faa3-107">Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse.</span><span class="sxs-lookup"><span data-stu-id="0faa3-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="0faa3-108">Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid.</span><span class="sxs-lookup"><span data-stu-id="0faa3-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

<a name="cost-objects"></a><span data-ttu-id="0faa3-109">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="0faa3-109">Cost objects</span></span>
------------

<span data-ttu-id="0faa3-110">Lehel **Kuluobjektid** on loetletud kõik toote puhul registreeritud kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="0faa3-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="0faa3-111">Kuluobjektid määratletakse järgmistest allikatest pärinevate andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="0faa3-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="0faa3-112">Toode</span><span class="sxs-lookup"><span data-stu-id="0faa3-112">Product</span></span>
-   <span data-ttu-id="0faa3-113">Tootedimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="0faa3-113">Product dimension group</span></span>
-   <span data-ttu-id="0faa3-114">Laoala dimensiooni grupp</span><span class="sxs-lookup"><span data-stu-id="0faa3-114">Storage dimension group</span></span>
-   <span data-ttu-id="0faa3-115">Jälgimisdimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="0faa3-115">Tracking dimension group</span></span>

<span data-ttu-id="0faa3-116">**Märkus.** Kuluobjekt tähistab ainult kuluelementi tüübiga **Otsene materjalikulu**.</span><span class="sxs-lookup"><span data-stu-id="0faa3-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="0faa3-117">Kuluobjekt ja varuobjekt erinevad selle poolest, et kuluobjekt määratletakse finantsvarudele valitud varudimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="0faa3-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="0faa3-118">Näiteks on kaubal järgmine konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="0faa3-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="0faa3-119">**Laoala:** füüsilised varud = jah, finantsvarud = jah</span><span class="sxs-lookup"><span data-stu-id="0faa3-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="0faa3-120">**Ladu:** füüsilised varud = jah, finantsvarud = ei</span><span class="sxs-lookup"><span data-stu-id="0faa3-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="0faa3-121">**Partii number:** füüsilised varud = jah, finantsvarud = ei</span><span class="sxs-lookup"><span data-stu-id="0faa3-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="0faa3-122">Järgmine tabel näitab, milline on kuluobjekt ja milline on varuobjekt.</span><span class="sxs-lookup"><span data-stu-id="0faa3-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="0faa3-123">Objekti tüüp</span><span class="sxs-lookup"><span data-stu-id="0faa3-123">Object type</span></span>      | <span data-ttu-id="0faa3-124">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="0faa3-124">Item number</span></span> | <span data-ttu-id="0faa3-125">Laoala</span><span class="sxs-lookup"><span data-stu-id="0faa3-125">Site</span></span> | <span data-ttu-id="0faa3-126">Ladu</span><span class="sxs-lookup"><span data-stu-id="0faa3-126">Warehouse</span></span> | <span data-ttu-id="0faa3-127">Partii nr</span><span class="sxs-lookup"><span data-stu-id="0faa3-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="0faa3-128">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="0faa3-128">Cost object</span></span>      | <span data-ttu-id="0faa3-129">x</span><span class="sxs-lookup"><span data-stu-id="0faa3-129">x</span></span>           | <span data-ttu-id="0faa3-130">x</span><span class="sxs-lookup"><span data-stu-id="0faa3-130">x</span></span>    |           |           |
| <span data-ttu-id="0faa3-131">Varuobjekt</span><span class="sxs-lookup"><span data-stu-id="0faa3-131">Inventory object</span></span> | <span data-ttu-id="0faa3-132">x</span><span class="sxs-lookup"><span data-stu-id="0faa3-132">x</span></span>           | <span data-ttu-id="0faa3-133">x</span><span class="sxs-lookup"><span data-stu-id="0faa3-133">x</span></span>    |  <span data-ttu-id="0faa3-134">x</span><span class="sxs-lookup"><span data-stu-id="0faa3-134">x</span></span>        | <span data-ttu-id="0faa3-135">x</span><span class="sxs-lookup"><span data-stu-id="0faa3-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="0faa3-136">Kulude ja koguste kogunemine</span><span class="sxs-lookup"><span data-stu-id="0faa3-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="0faa3-137">Väärtus väljal **Väärtus** on järgmiste väärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="0faa3-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="0faa3-138">Füüsiline omahind</span><span class="sxs-lookup"><span data-stu-id="0faa3-138">Physical cost amount</span></span>
    -   <span data-ttu-id="0faa3-139">Finantsiline omahind</span><span class="sxs-lookup"><span data-stu-id="0faa3-139">Financial cost amount</span></span>
    -   <span data-ttu-id="0faa3-140">Korrigeerimised</span><span class="sxs-lookup"><span data-stu-id="0faa3-140">Adjustments</span></span>
-   <span data-ttu-id="0faa3-141">Väärtus väljal **Kogus** on järgmiste väärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="0faa3-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="0faa3-142">Saadud</span><span class="sxs-lookup"><span data-stu-id="0faa3-142">Received</span></span>
    -   <span data-ttu-id="0faa3-143">Maha arvatud</span><span class="sxs-lookup"><span data-stu-id="0faa3-143">Deducted</span></span>
    -   <span data-ttu-id="0faa3-144">Sisestatud kogus</span><span class="sxs-lookup"><span data-stu-id="0faa3-144">Posted quantity</span></span>
-   <span data-ttu-id="0faa3-145">Väli **Keskmine ühikukulu** on arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="0faa3-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="0faa3-146">Väärtuse arvutamiseks jagatakse väärtus **Väärtus** väärtusega **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="0faa3-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="0faa3-147">**Märkus.** Parameetril **Kaasa füüsiline väärtus** pole eelnevatele arvutustele mingit mõju.</span><span class="sxs-lookup"><span data-stu-id="0faa3-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="0faa3-148">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0faa3-148">See also</span></span>
--------

[<span data-ttu-id="0faa3-149">Tootedimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="0faa3-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="0faa3-150">Laoala dimensiooni grupp</span><span class="sxs-lookup"><span data-stu-id="0faa3-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="0faa3-151">Jälgimisdimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="0faa3-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="0faa3-152">Mis on uus või muudetud</span><span class="sxs-lookup"><span data-stu-id="0faa3-152">What's new or changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)

[<span data-ttu-id="0faa3-153">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="0faa3-153">Cost entries</span></span>](cost-entries.md)




