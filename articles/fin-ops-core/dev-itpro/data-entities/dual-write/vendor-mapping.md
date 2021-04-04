---
title: Integreeritud hankija koondandmed
description: Selles teemas kirjeldatakse hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Dataverse vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 272962b58d8d654c2640a51ef2dbdcd1b05cf8c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560309"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="9ffed-103">Integreeritud hankija koondandmed</span><span class="sxs-lookup"><span data-stu-id="9ffed-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="9ffed-104">Termin *hankija* viitab tarnijariigi organisatsioonile või ainuomanikule, kes tarnib ettevõttele kaupu või teenuseid.</span><span class="sxs-lookup"><span data-stu-id="9ffed-104">The term *vendor* refers to a supplier organization, or a sole proprietor who supplies goods or services to a business.</span></span> <span data-ttu-id="9ffed-105">Kuigi *hankija* on loodud mõiste teenusekomplektis Microsoft Dynamics 365 Supply Chain Management, pole teistes Dynamics 365 mudeljuhitud rakendustes mõistet hankija olemas.</span><span class="sxs-lookup"><span data-stu-id="9ffed-105">Although *vendor* is an established concept in Microsoft Dynamics 365 Supply Chain Management, no vendor concept exists in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="9ffed-106">Kuid hankija teabe talletamiseks saate ülekoormata tabeli **Konto/kontakt**.</span><span class="sxs-lookup"><span data-stu-id="9ffed-106">However, you can overload the **Account/Contact** table to store vendor information.</span></span> <span data-ttu-id="9ffed-107">Integreeritud hankija koondandmed tutvustavad Dynamics 365 mudeljuhitud rakendustes selgesõnalist hankija mõistet.</span><span class="sxs-lookup"><span data-stu-id="9ffed-107">The integrated vendor master introduces an explicit vendor concept in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="9ffed-108">Saate kasutada kas uut hankija kujundust või talletada hankija andmeid tabelis **Konto/kontakt**.</span><span class="sxs-lookup"><span data-stu-id="9ffed-108">You can either use the new vendor design or store vendor data in the **Account/Contact** table.</span></span> <span data-ttu-id="9ffed-109">Topeltkirjutus toetab mõlemat lähenemist.</span><span class="sxs-lookup"><span data-stu-id="9ffed-109">Dual-write supports both approaches.</span></span>

<span data-ttu-id="9ffed-110">Mõlemas lähenemisviisis on hankija andmed integreeritud Dynamics 365 Supply Chain Managementi, Dynamics 365 Salesi, Dynamics 365 Field Service'i ja Power Appsi portaalide vahel.</span><span class="sxs-lookup"><span data-stu-id="9ffed-110">In both approaches, the vendor data is integrated between Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, and Power Apps portals.</span></span> <span data-ttu-id="9ffed-111">Supply Chain Managementis on andmed saadaval töövoogudele (nt ostutaotlused ja ostutellimused).</span><span class="sxs-lookup"><span data-stu-id="9ffed-111">In Supply Chain Management, the data is available for workflows such as purchase requisitions and purchase orders.</span></span>

## <a name="vendor-data-flow"></a><span data-ttu-id="9ffed-112">Hankijaandmete voog</span><span class="sxs-lookup"><span data-stu-id="9ffed-112">Vendor data flow</span></span>

<span data-ttu-id="9ffed-113">Kui te ei soovi talletada hankija andmeid Dataverse’i tabelis **Konto/kontakt**, saate kasutada uut hankija kujundust.</span><span class="sxs-lookup"><span data-stu-id="9ffed-113">If you don't want to store vendor data in the **Account/Contact** table in Dataverse, you can use the new vendor design.</span></span>

![Hankijaandmete voog](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="9ffed-115">Kui soovite jätkata hankija andmete talletamist tabelis **Konto/kontakt**, saate kasutada laiendatud hankija kujundust.</span><span class="sxs-lookup"><span data-stu-id="9ffed-115">If you want to continue to store vendor data in the **Account/Contact** table, you can use the extended vendor design.</span></span> <span data-ttu-id="9ffed-116">Laiendatud hankija kujunduse kasutamiseks peate konfigureerima hankija töövood topeltkirjutuse lahendusepaketis.</span><span class="sxs-lookup"><span data-stu-id="9ffed-116">To use the extended vendor design, you must configure the vendor workflows in the dual-write solution package.</span></span> <span data-ttu-id="9ffed-117">Lisateavet vaadake teemast [Hankija kujunduste vahel vahetamine](vendor-switch.md).</span><span class="sxs-lookup"><span data-stu-id="9ffed-117">For more information, see [Switch between vendor designs](vendor-switch.md).</span></span>

![Hankijaandmete laiendatud voog](media/dual-write-vendor-detail.jpg)

> [!TIP]
> <span data-ttu-id="9ffed-119">Kui kasutate iseteeninduse hankijate Power Appsi portaale, võib hankija teave liikuda otse Finance and Operationsi rakendustesse.</span><span class="sxs-lookup"><span data-stu-id="9ffed-119">If you're using Power Apps portals for self-service vendors, the vendor information can flow directly to Finance and Operations apps.</span></span>

## <a name="templates"></a><span data-ttu-id="9ffed-120">Mallid</span><span class="sxs-lookup"><span data-stu-id="9ffed-120">Templates</span></span>

<span data-ttu-id="9ffed-121">Hankijaandmed sisaldavad kogu teavet hankija kohta (nt hankijagrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil).</span><span class="sxs-lookup"><span data-stu-id="9ffed-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="9ffed-122">Tabeli kaartide kogum toimib koos hankijaandmete suhtluse ajal, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="9ffed-122">A collection of table maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="9ffed-123">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="9ffed-123">Finance and Operations apps</span></span> | <span data-ttu-id="9ffed-124">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="9ffed-124">Other Dynamics 365 apps</span></span>     | <span data-ttu-id="9ffed-125">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9ffed-125">Description</span></span>
----------------------------|-----------------------------|------------
<span data-ttu-id="9ffed-126">Hankija V2</span><span class="sxs-lookup"><span data-stu-id="9ffed-126">Vendor V2</span></span>                   | <span data-ttu-id="9ffed-127">Konto</span><span class="sxs-lookup"><span data-stu-id="9ffed-127">Account</span></span>                     | <span data-ttu-id="9ffed-128">Ettevõtted, mis kasutavad hankija teabe talletamiseks tabelit Konto, saavad jätkata selle kasutamist samal viisil.</span><span class="sxs-lookup"><span data-stu-id="9ffed-128">Businesses that use the Account table to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="9ffed-129">Nad saavad Finance and Operationsi rakenduste integratsiooni tõttu kasutada ka konkreetseid hankijafunktsioone.</span><span class="sxs-lookup"><span data-stu-id="9ffed-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="9ffed-130">Hankija V2</span><span class="sxs-lookup"><span data-stu-id="9ffed-130">Vendor V2</span></span>                   | <span data-ttu-id="9ffed-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="9ffed-131">Msdyn\_vendors</span></span>              | <span data-ttu-id="9ffed-132">Ettevõtted, mis kasutavad hankijate jaoks kohandatud lahendusi, saavad kasutada valmislahendusena hankija eeliseid, mis on Finance and Operationsi rakenduste integratsiooni tõttu juurutatud teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9ffed-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Dataverse because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="9ffed-133">Hankijagrupid</span><span class="sxs-lookup"><span data-stu-id="9ffed-133">Vendor groups</span></span>               | <span data-ttu-id="9ffed-134">msdyn\_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="9ffed-134">msdyn\_vendorgroups</span></span>         | <span data-ttu-id="9ffed-135">See mall sünkroonib hankijagrupi teabe.</span><span class="sxs-lookup"><span data-stu-id="9ffed-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="9ffed-136">Tarnija makseviis</span><span class="sxs-lookup"><span data-stu-id="9ffed-136">Vendor payment method</span></span>       | <span data-ttu-id="9ffed-137">msdyn\_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="9ffed-137">msdyn\_vendorpaymentmethods</span></span> | <span data-ttu-id="9ffed-138">See mall sünkroonib hankija makseviisi teabe.</span><span class="sxs-lookup"><span data-stu-id="9ffed-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="9ffed-139">CDS-i kontaktid V2</span><span class="sxs-lookup"><span data-stu-id="9ffed-139">CDS Contacts V2</span></span>             | <span data-ttu-id="9ffed-140">kontaktid</span><span class="sxs-lookup"><span data-stu-id="9ffed-140">contacts</span></span>                    | <span data-ttu-id="9ffed-141">[Kontaktide](customer-mapping.md#cds-contacts-v2-to-contacts) mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="9ffed-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="9ffed-142">Maksegraafiku read</span><span class="sxs-lookup"><span data-stu-id="9ffed-142">Payment schedule lines</span></span>      | <span data-ttu-id="9ffed-143">msdyn\_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="9ffed-143">msdyn\_paymentschedulelines</span></span> | <span data-ttu-id="9ffed-144">[Maksegraafiku ridade](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) mall sünkroonib klientide ja hankijate viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="9ffed-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="9ffed-145">Maksegraafik</span><span class="sxs-lookup"><span data-stu-id="9ffed-145">Payment schedule</span></span>            | <span data-ttu-id="9ffed-146">msdyn\_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="9ffed-146">msdyn\_paymentschedules</span></span>     | <span data-ttu-id="9ffed-147">[Maksegraafikute](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="9ffed-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="9ffed-148">CDS V2 maksepäeva read</span><span class="sxs-lookup"><span data-stu-id="9ffed-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="9ffed-149">msdyn\_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="9ffed-149">msdyn\_paymentdaylines</span></span>      | <span data-ttu-id="9ffed-150">[Maksepäeva ridade](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) mall sünkroonib klientide ja hankijate maksepäeva ridade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="9ffed-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="9ffed-151">CDS-i maksepäevad</span><span class="sxs-lookup"><span data-stu-id="9ffed-151">Payment days CDS</span></span>            | <span data-ttu-id="9ffed-152">msdyn\_paymentdays</span><span class="sxs-lookup"><span data-stu-id="9ffed-152">msdyn\_paymentdays</span></span>          | <span data-ttu-id="9ffed-153">[Maksepäevade](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="9ffed-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="9ffed-154">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="9ffed-154">Terms of payment</span></span>            | <span data-ttu-id="9ffed-155">msdyn\_paymentterms</span><span class="sxs-lookup"><span data-stu-id="9ffed-155">msdyn\_paymentterms</span></span>         | <span data-ttu-id="9ffed-156">[Maksetingimuse](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="9ffed-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="9ffed-157">Nime liited</span><span class="sxs-lookup"><span data-stu-id="9ffed-157">Name affixes</span></span>                | <span data-ttu-id="9ffed-158">msdyn\_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="9ffed-158">msdyn\_nameaffixes</span></span>          | <span data-ttu-id="9ffed-159">[Nimeliidete](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="9ffed-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]