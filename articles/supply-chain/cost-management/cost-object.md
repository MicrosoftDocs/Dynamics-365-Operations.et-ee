---
title: Kuluobjektid
description: Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e590322c75cfb2ad21236af56656061037a4b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426399"
---
# <a name="cost-objects"></a><span data-ttu-id="b4f84-105">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="b4f84-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4f84-106">Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse.</span><span class="sxs-lookup"><span data-stu-id="b4f84-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="b4f84-107">Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse.</span><span class="sxs-lookup"><span data-stu-id="b4f84-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="b4f84-108">Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid.</span><span class="sxs-lookup"><span data-stu-id="b4f84-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="b4f84-109">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="b4f84-109">Cost objects</span></span>

<span data-ttu-id="b4f84-110">Lehel **Kuluobjektid** on loetletud kõik toote puhul registreeritud kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="b4f84-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="b4f84-111">Kuluobjektid määratletakse järgmistest allikatest pärinevate andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="b4f84-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="b4f84-112">Toode</span><span class="sxs-lookup"><span data-stu-id="b4f84-112">Product</span></span>
-   <span data-ttu-id="b4f84-113">Tootedimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="b4f84-113">Product dimension group</span></span>
-   <span data-ttu-id="b4f84-114">Laoala dimensiooni grupp</span><span class="sxs-lookup"><span data-stu-id="b4f84-114">Storage dimension group</span></span>
-   <span data-ttu-id="b4f84-115">Jälgimisdimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="b4f84-115">Tracking dimension group</span></span>

<span data-ttu-id="b4f84-116">**Märkus.** Kuluobjekt tähistab ainult kuluelementi tüübiga **Otsene materjalikulu**.</span><span class="sxs-lookup"><span data-stu-id="b4f84-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="b4f84-117">Kuluobjekt ja varuobjekt erinevad selle poolest, et kuluobjekt määratletakse finantsvarudele valitud varudimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="b4f84-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="b4f84-118">Näiteks on kaubal järgmine konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="b4f84-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="b4f84-119">**Laoala:** füüsilised varud = jah, finantsvarud = jah</span><span class="sxs-lookup"><span data-stu-id="b4f84-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="b4f84-120">**Ladu:** füüsilised varud = jah, finantsvarud = ei</span><span class="sxs-lookup"><span data-stu-id="b4f84-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="b4f84-121">**Partii number:** füüsilised varud = jah, finantsvarud = ei</span><span class="sxs-lookup"><span data-stu-id="b4f84-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="b4f84-122">Järgmine tabel näitab, milline on kuluobjekt ja milline on varuobjekt.</span><span class="sxs-lookup"><span data-stu-id="b4f84-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="b4f84-123">Objekti tüüp</span><span class="sxs-lookup"><span data-stu-id="b4f84-123">Object type</span></span>      | <span data-ttu-id="b4f84-124">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="b4f84-124">Item number</span></span> | <span data-ttu-id="b4f84-125">Laoala</span><span class="sxs-lookup"><span data-stu-id="b4f84-125">Site</span></span> | <span data-ttu-id="b4f84-126">Ladu</span><span class="sxs-lookup"><span data-stu-id="b4f84-126">Warehouse</span></span> | <span data-ttu-id="b4f84-127">Partii nr</span><span class="sxs-lookup"><span data-stu-id="b4f84-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="b4f84-128">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b4f84-128">Cost object</span></span>      | <span data-ttu-id="b4f84-129">x</span><span class="sxs-lookup"><span data-stu-id="b4f84-129">x</span></span>           | <span data-ttu-id="b4f84-130">x</span><span class="sxs-lookup"><span data-stu-id="b4f84-130">x</span></span>    |           |           |
| <span data-ttu-id="b4f84-131">Varuobjekt</span><span class="sxs-lookup"><span data-stu-id="b4f84-131">Inventory object</span></span> | <span data-ttu-id="b4f84-132">x</span><span class="sxs-lookup"><span data-stu-id="b4f84-132">x</span></span>           | <span data-ttu-id="b4f84-133">x</span><span class="sxs-lookup"><span data-stu-id="b4f84-133">x</span></span>    |  <span data-ttu-id="b4f84-134">x</span><span class="sxs-lookup"><span data-stu-id="b4f84-134">x</span></span>        | <span data-ttu-id="b4f84-135">x</span><span class="sxs-lookup"><span data-stu-id="b4f84-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="b4f84-136">Kulude ja koguste kogunemine</span><span class="sxs-lookup"><span data-stu-id="b4f84-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="b4f84-137">Väärtus väljal **Väärtus** on järgmiste väärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="b4f84-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="b4f84-138">Füüsiline omahind</span><span class="sxs-lookup"><span data-stu-id="b4f84-138">Physical cost amount</span></span>
    -   <span data-ttu-id="b4f84-139">Finantsiline omahind</span><span class="sxs-lookup"><span data-stu-id="b4f84-139">Financial cost amount</span></span>
    -   <span data-ttu-id="b4f84-140">Korrigeerimised</span><span class="sxs-lookup"><span data-stu-id="b4f84-140">Adjustments</span></span>
-   <span data-ttu-id="b4f84-141">Väärtus väljal **Kogus** on järgmiste väärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="b4f84-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="b4f84-142">Saadud</span><span class="sxs-lookup"><span data-stu-id="b4f84-142">Received</span></span>
    -   <span data-ttu-id="b4f84-143">Maha arvatud</span><span class="sxs-lookup"><span data-stu-id="b4f84-143">Deducted</span></span>
    -   <span data-ttu-id="b4f84-144">Sisestatud kogus</span><span class="sxs-lookup"><span data-stu-id="b4f84-144">Posted quantity</span></span>
-   <span data-ttu-id="b4f84-145">Väli **Keskmine ühikukulu** on arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="b4f84-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="b4f84-146">Väärtuse arvutamiseks jagatakse väärtus **Väärtus** väärtusega **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="b4f84-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="b4f84-147">**Märkus.** Parameetril **Kaasa füüsiline väärtus** pole eelnevatele arvutustele mingit mõju.</span><span class="sxs-lookup"><span data-stu-id="b4f84-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b4f84-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b4f84-148">Additional resources</span></span>
--------

[<span data-ttu-id="b4f84-149">Tootedimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="b4f84-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="b4f84-150">Laoala dimensiooni grupp</span><span class="sxs-lookup"><span data-stu-id="b4f84-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="b4f84-151">Jälgimisdimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="b4f84-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="b4f84-152">Mis on uus või muudetud</span><span class="sxs-lookup"><span data-stu-id="b4f84-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="b4f84-153">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b4f84-153">Cost entries</span></span>](cost-entries.md)



