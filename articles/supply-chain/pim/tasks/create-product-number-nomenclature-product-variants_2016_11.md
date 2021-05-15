---
title: Tootenumbri nomenklatuuri loomine konfigureeritud tootevariantide jaoks
description: See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921007"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="d02ad-103">Tootenumbri nomenklatuuri loomine konfigureeritud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="d02ad-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d02ad-104">See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada.</span><span class="sxs-lookup"><span data-stu-id="d02ad-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="d02ad-105">See protseduur näitab ka, kuidas toote konfiguratsioonimudeli komponendile konfiguratsiooni nomenklatuuri koostada.</span><span class="sxs-lookup"><span data-stu-id="d02ad-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="d02ad-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d02ad-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d02ad-107">Uus tootenumbri nomenklatuur määratakse D0004 tooteetalonile.</span><span class="sxs-lookup"><span data-stu-id="d02ad-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="d02ad-108">Enamasti teeb selle toimingu toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="d02ad-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="d02ad-109">Tootenumbri nomenklatuuri loomine</span><span class="sxs-lookup"><span data-stu-id="d02ad-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="d02ad-110">Avage **Tooteteabe haldus \> Seadistamine \> Tootenomenklatuurid**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="d02ad-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-111">Select **New**.</span></span>
1. <span data-ttu-id="d02ad-112">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="d02ad-113">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="d02ad-114">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-114">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-115">Valige **Tooteetaloni koondnumber**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="d02ad-116">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-116">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-117">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="d02ad-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-119">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="d02ad-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d02ad-120">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-120">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-121">Valige **Konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="d02ad-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d02ad-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="d02ad-123">Tootenumbri nomenklatuuri määramine tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="d02ad-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="d02ad-124">Avage **Tooteteabe haldus \> Tooted \> Tooteetalonid**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="d02ad-125">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="d02ad-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d02ad-126">Näiteks saate filtreerida välja **Tootenumber** väärtuse D järgi.</span><span class="sxs-lookup"><span data-stu-id="d02ad-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="d02ad-127">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="d02ad-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="d02ad-128">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-128">Select **Edit**.</span></span>
1. <span data-ttu-id="d02ad-129">Valige väärtus *Jah* väljal **Kasuta nomenklatuuri**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="d02ad-130">Väljale **Tootevariandi numbri nomenklatuur** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="d02ad-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="d02ad-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d02ad-131">Close the page.</span></span>
1. <span data-ttu-id="d02ad-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d02ad-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="d02ad-133">Nomenklatuuri loomine toote konfiguratsioonimudeli komponendile</span><span class="sxs-lookup"><span data-stu-id="d02ad-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="d02ad-134">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="d02ad-135">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d02ad-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="d02ad-136">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="d02ad-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="d02ad-137">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-137">Select **Edit**.</span></span>
1. <span data-ttu-id="d02ad-138">Tehke väljal *Kasuta konfiguratsiooni nomenklatuur* valik **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="d02ad-139">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-139">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-140">Valige **Atribuudi väärtus**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d02ad-141">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-142">Valige või sisestage väärtus väljal **Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d02ad-143">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-143">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-144">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="d02ad-145">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-146">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="d02ad-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d02ad-147">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-147">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-148">Valige **Atribuudi väärtus**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d02ad-149">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-150">Valige või sisestage väärtus väljal **Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d02ad-151">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-151">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-152">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="d02ad-153">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-154">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="d02ad-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d02ad-155">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-155">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-156">Valige **Atribuudi väärtus**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d02ad-157">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-158">Valige või sisestage väärtus väljal **Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d02ad-159">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-159">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-160">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="d02ad-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-162">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="d02ad-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d02ad-163">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-163">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-164">Valige **Atribuudi väärtus**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d02ad-165">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-166">Valige või sisestage väärtus väljal **Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d02ad-167">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-167">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-168">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="d02ad-169">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-170">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="d02ad-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d02ad-171">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-171">Select **Add**.</span></span>
1. <span data-ttu-id="d02ad-172">Valige **Numbriseeria väärtus**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="d02ad-173">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d02ad-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d02ad-174">Sisestage või valige väärtus väljal **Numbriseeria**.</span><span class="sxs-lookup"><span data-stu-id="d02ad-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="d02ad-175">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d02ad-175">Close the page.</span></span>
1. <span data-ttu-id="d02ad-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d02ad-176">Close the page.</span></span>
1. <span data-ttu-id="d02ad-177">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d02ad-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]