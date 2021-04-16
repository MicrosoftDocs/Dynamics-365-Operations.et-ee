---
title: Erandite uurimine või lahendamine
description: Hankija arvepoliitikad käivitatakse, kui sisestate hankija arve leheküljel Hankija arve ja avate lehekülje Hankija arve poliitika rikkumised.
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abc8dc112ab577ddcbd208f898a8d4e487bc2998
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827766"
---
# <a name="research-or-resolve-exceptions"></a><span data-ttu-id="e2582-103">Erandite uurimine või lahendamine</span><span class="sxs-lookup"><span data-stu-id="e2582-103">Research or resolve exceptions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2582-104">Hankija arvepoliitikad käivitatakse, kui sisestate hankija arve leheküljel Hankija arve ja avate lehekülje Hankija arve poliitika rikkumised.</span><span class="sxs-lookup"><span data-stu-id="e2582-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="e2582-105">Hankija arve töövoogu saate konfigureerida ka selliselt, et hankija arve poliitikad käivitatakse iga kord, kui sisestate arve töövoogu.</span><span class="sxs-lookup"><span data-stu-id="e2582-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="e2582-106">Hankija arvepoliitikad ei kehti arvetele, mis on loodud arveregistris või arve töölehel.</span><span class="sxs-lookup"><span data-stu-id="e2582-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="e2582-107">Arvete võrdlemise kinnitamisel ei kasutata hankija arvepoliitikaid, vaid selle sätted määratakse leheküljel Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e2582-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="e2582-108">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="e2582-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="e2582-109">Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli.</span><span class="sxs-lookup"><span data-stu-id="e2582-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="e2582-110">Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine.</span><span class="sxs-lookup"><span data-stu-id="e2582-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="e2582-111">Hankija arve poliitikate loomise ettevalmistus</span><span class="sxs-lookup"><span data-stu-id="e2582-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="e2582-112">Avage Ostureskontro > Seadistus > Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e2582-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="e2582-113">Klõpsake vahekaarti Arve kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="e2582-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="e2582-114">Märkige või tühjendage ruut Arve päise oleku automaatne värskendus.</span><span class="sxs-lookup"><span data-stu-id="e2582-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="e2582-115">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e2582-115">Click OK.</span></span>
5. <span data-ttu-id="e2582-116">Valige suvand väljal Lahknevustega arvete sisestamine.</span><span class="sxs-lookup"><span data-stu-id="e2582-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="e2582-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2582-117">Close the page.</span></span>
7. <span data-ttu-id="e2582-118">Avage Ostureskontro > Poliitika seadistus > Hankija arvepoliitikad.</span><span class="sxs-lookup"><span data-stu-id="e2582-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="e2582-119">Klõpsake valikut Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e2582-119">Click Parameters.</span></span>
9. <span data-ttu-id="e2582-120">Klõpsake btnAdd.</span><span class="sxs-lookup"><span data-stu-id="e2582-120">Click btnAdd.</span></span>
10. <span data-ttu-id="e2582-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2582-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="e2582-122">Hankija arvete poliitika reegli tüüpide loomine</span><span class="sxs-lookup"><span data-stu-id="e2582-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="e2582-123">Avage Ostureskontro > Poliitika seadistus > Hankija arve poliitikareegli tüübid.</span><span class="sxs-lookup"><span data-stu-id="e2582-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="e2582-124">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e2582-124">Click New.</span></span>
3. <span data-ttu-id="e2582-125">Sisestage väärtus väljale Reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="e2582-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="e2582-126">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2582-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e2582-127">Klõpsake väljal Päringu nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e2582-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e2582-128">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e2582-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e2582-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e2582-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e2582-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e2582-130">Click Save.</span></span>
9. <span data-ttu-id="e2582-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2582-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="e2582-132">Hankija arvepoliitika määratlemine</span><span class="sxs-lookup"><span data-stu-id="e2582-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="e2582-133">Avage Ostureskontro > Poliitika seadistus > Hankija arvepoliitikad.</span><span class="sxs-lookup"><span data-stu-id="e2582-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="e2582-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e2582-134">Click New.</span></span>
3. <span data-ttu-id="e2582-135">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e2582-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e2582-136">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2582-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e2582-137">Laiendage või ahendage jaotist Poliitika organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="e2582-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="e2582-138">Valige puul Contoso Entertainment System USA.</span><span class="sxs-lookup"><span data-stu-id="e2582-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="e2582-139">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e2582-139">Click Add.</span></span>
8. <span data-ttu-id="e2582-140">Laiendage või ahendage jaotist Poliitika reeglid.</span><span class="sxs-lookup"><span data-stu-id="e2582-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="e2582-141">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="e2582-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="e2582-142">Sisestage väärtus väljale Poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="e2582-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="e2582-143">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="e2582-143">Click Filter.</span></span>
12. <span data-ttu-id="e2582-144">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e2582-144">Click Add.</span></span>
13. <span data-ttu-id="e2582-145">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e2582-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e2582-146">Klõpsake väljal Tabel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e2582-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="e2582-147">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e2582-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="e2582-148">Klõpsake väljal Tuletatud tabel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e2582-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="e2582-149">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e2582-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="e2582-150">Klõpsake väljal Väli otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e2582-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="e2582-151">Sisestage väärtus väljale Väli.</span><span class="sxs-lookup"><span data-stu-id="e2582-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="e2582-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2582-152">Close the page.</span></span>
21. <span data-ttu-id="e2582-153">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="e2582-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="e2582-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e2582-154">Click OK.</span></span>
23. <span data-ttu-id="e2582-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e2582-155">Click OK.</span></span>
24. <span data-ttu-id="e2582-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2582-156">Close the page.</span></span>
25. <span data-ttu-id="e2582-157">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2582-157">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]