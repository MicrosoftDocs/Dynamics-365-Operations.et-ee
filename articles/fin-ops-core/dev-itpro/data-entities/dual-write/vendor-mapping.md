---
title: Integreeritud hankija koondandmed
description: Selles teemas kirjeldatakse hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019734"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="b2c5e-103">Integreeritud hankija koondandmed</span><span class="sxs-lookup"><span data-stu-id="b2c5e-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b2c5e-104">Termin *hankija* viitab tarnijariigi organisatsioonile või ainuomanikule, kes on tarneahela protsessi osa ja tarnib ettevõttele kaupu.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-104">The term *vendor* refers to a supplier organization or a sole proprietor that is part of the supply chain process, and that supplies goods for the business.</span></span> <span data-ttu-id="b2c5e-105">Kuigi *hankija* on loodud mõiste teenusekomplekti Finance and Operations rakendustes, pole teistes Dynamics 365 rakendustes mõistet hankija olemas.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-105">Although *vendor* is an established concept in Finance and Operations apps, a vendor concept doesn't exist in other Dynamics 365 apps.</span></span> <span data-ttu-id="b2c5e-106">Selle asemel on mõned ettevõtted olemi Konto üle koormanud nii kliendi- kui ka hankijateabega.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-106">Instead, some businesses overload the Account entity to store both customer information and vendor information.</span></span> <span data-ttu-id="b2c5e-107">Teised ettevõtted kasutavad kohandatud hankija mõistet.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-107">Other businesses use a custom vendor concept.</span></span> <span data-ttu-id="b2c5e-108">Common Data Service'i integratsioon toetab mõlemat lahendust.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-108">Common Data Service integration supports both these designs.</span></span> <span data-ttu-id="b2c5e-109">Seetõttu saate olenevalt oma äristsenaariumist lubada ühe neist lahendustest.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-109">Therefore, you can enable either of the designs, depending on your business scenario.</span></span>

<span data-ttu-id="b2c5e-110">Hankija andmete integreerimine Finance and Operationsi rakenduste ja teiste Dynamics 365 rakenduste vahel võimaldab teil hankida mitmeid koondandmeid.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-110">Integration of vendor data between Finance and Operations apps and other Dynamics 365 apps lets you multi-master the data.</span></span> <span data-ttu-id="b2c5e-111">Olenemata sellest, kust hankijaandmed pärinevad, on need integreeritud kulisside taga üle rakenduste piiride ja taristute erinevuste.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-111">Regardless of where the vendor data originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> 

### <a name="vendor-data-flow"></a><span data-ttu-id="b2c5e-112">Hankijaandmete voog</span><span class="sxs-lookup"><span data-stu-id="b2c5e-112">Vendor data flow</span></span>

<span data-ttu-id="b2c5e-113">Kui soovite kasutada hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite isoleerida hankijateabe klienditeabest, saate kasutada uut hankijalahendust.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-113">If you want to use other Dynamics 365 apps for vendor mastering, and you want to isolate vendor information from customer information, you can use the new vendor design.</span></span>

![Hankijaandmete voog](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="b2c5e-115">Kui soovite kasutada hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite hankijaandmete salvestamiseks jätkata olemi Konto kasutamist, saate kasutada uut, laiendatud hankijalahendust.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-115">If you want to use other Dynamics 365 apps for vendor mastering, and you want to continue to use the Account entity to store vendor information, you can use the new extended vendor design.</span></span> <span data-ttu-id="b2c5e-116">Selles lahenduses on hankija üksikasjadesse talletatud laiendatud hankijateave (nt hankijagrupp ja hankija sisestuse profiil).</span><span class="sxs-lookup"><span data-stu-id="b2c5e-116">In this design, extended vendor information, such as the vendor group and vendor posting profile, are stored in the vendor detail.</span></span>

![Hankijaandmete laiendatud voog](media/dual-write-vendor-detail.jpg)

<span data-ttu-id="b2c5e-118">Hankija kontaktteave meenutab kliendi kontaktteavet.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-118">Vendor contact information resembles customer contact information.</span></span> <span data-ttu-id="b2c5e-119">Kulisside taga talletatakse kontaktisiku teave ja tuuakse need samadest üksustest.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-119">Behind the scenes, the contact person's information is stored and retrieved from the same entities.</span></span>

## <a name="templates"></a><span data-ttu-id="b2c5e-120">Mallid</span><span class="sxs-lookup"><span data-stu-id="b2c5e-120">Templates</span></span>

<span data-ttu-id="b2c5e-121">Hankijaandmed sisaldavad kogu teavet hankija kohta (nt hankijagrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil).</span><span class="sxs-lookup"><span data-stu-id="b2c5e-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="b2c5e-122">Olemikaartide kogum toimib koos hankijaandmete suhtluse ajal, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-122">A collection of entity maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="b2c5e-123">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="b2c5e-123">Finance and Operations apps</span></span> | <span data-ttu-id="b2c5e-124">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="b2c5e-124">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="b2c5e-125">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b2c5e-125">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="b2c5e-126">Hankija V2</span><span class="sxs-lookup"><span data-stu-id="b2c5e-126">Vendor V2</span></span>               | <span data-ttu-id="b2c5e-127">Konto</span><span class="sxs-lookup"><span data-stu-id="b2c5e-127">Account</span></span> | <span data-ttu-id="b2c5e-128">Ettevõtted, mis kasutavad hankija teabe talletamiseks olemit Konto, saavad jätkata selle kasutamist samal viisil.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-128">Businesses that use the Account entity to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="b2c5e-129">Nad saavad Finance and Operationsi rakenduste integratsiooni tõttu kasutada ka konkreetseid hankijafunktsioone.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="b2c5e-130">Hankija V2</span><span class="sxs-lookup"><span data-stu-id="b2c5e-130">Vendor V2</span></span>               | <span data-ttu-id="b2c5e-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="b2c5e-131">Msdyn\_vendors</span></span> | <span data-ttu-id="b2c5e-132">Ettevõtted, mis kasutavad hankijate jaoks kohandatud lahendusi, saavad kasutada valmislahendusena hankija eeliseid, mis on Finance and Operationsi rakenduste integratsiooni tõttu juurutatud teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Common Data Service because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="b2c5e-133">Hankijagrupid</span><span class="sxs-lookup"><span data-stu-id="b2c5e-133">Vendor groups</span></span> | <span data-ttu-id="b2c5e-134">msdyn_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="b2c5e-134">msdyn_vendorgroups</span></span> | <span data-ttu-id="b2c5e-135">See mall sünkroonib hankijagrupi teabe.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="b2c5e-136">Tarnija makseviis</span><span class="sxs-lookup"><span data-stu-id="b2c5e-136">Vendor payment method</span></span> | <span data-ttu-id="b2c5e-137">msdyn_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="b2c5e-137">msdyn_vendorpaymentmethods</span></span> | <span data-ttu-id="b2c5e-138">See mall sünkroonib hankija makseviisi teabe.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="b2c5e-139">CDS-i kontaktid V2</span><span class="sxs-lookup"><span data-stu-id="b2c5e-139">CDS Contacts V2</span></span>             | <span data-ttu-id="b2c5e-140">kontaktid</span><span class="sxs-lookup"><span data-stu-id="b2c5e-140">contacts</span></span>                        | <span data-ttu-id="b2c5e-141">[Kontaktide](customer-mapping.md#cds-contacts-v2-to-contacts) mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="b2c5e-142">Maksegraafiku read</span><span class="sxs-lookup"><span data-stu-id="b2c5e-142">Payment schedule lines</span></span>      | <span data-ttu-id="b2c5e-143">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="b2c5e-143">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="b2c5e-144">[Maksegraafiku ridade](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) mall sünkroonib klientide ja hankijate viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="b2c5e-145">Maksegraafik</span><span class="sxs-lookup"><span data-stu-id="b2c5e-145">Payment schedule</span></span>            | <span data-ttu-id="b2c5e-146">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="b2c5e-146">msdyn_paymentschedules</span></span>          | <span data-ttu-id="b2c5e-147">[Maksegraafikute](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b2c5e-148">CDS V2 maksepäeva read</span><span class="sxs-lookup"><span data-stu-id="b2c5e-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="b2c5e-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="b2c5e-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="b2c5e-150">[Maksepäeva ridade](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) mall sünkroonib klientide ja hankijate maksepäeva ridade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="b2c5e-151">CDS-i maksepäevad</span><span class="sxs-lookup"><span data-stu-id="b2c5e-151">Payment days CDS</span></span>            | <span data-ttu-id="b2c5e-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="b2c5e-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="b2c5e-153">[Maksepäevade](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b2c5e-154">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="b2c5e-154">Terms of payment</span></span>            | <span data-ttu-id="b2c5e-155">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="b2c5e-155">msdyn_paymentterms</span></span>              | <span data-ttu-id="b2c5e-156">[Maksetingimuse](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="b2c5e-157">Nime liited</span><span class="sxs-lookup"><span data-stu-id="b2c5e-157">Name affixes</span></span>                | <span data-ttu-id="b2c5e-158">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="b2c5e-158">msdyn_nameaffixes</span></span>               | <span data-ttu-id="b2c5e-159">[Nimeliidete](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="b2c5e-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]