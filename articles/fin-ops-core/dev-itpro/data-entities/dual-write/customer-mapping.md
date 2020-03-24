---
title: Integreeritud klientide koond
description: Selles teemas kirjeldatakse kliendiandmete integreerimist rakenduse Finance and Operations ja teenuse Common Data Service vahel.
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
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124585"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="e278a-103">Integreeritud kliendi koondandmed</span><span class="sxs-lookup"><span data-stu-id="e278a-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="e278a-104">Kliendikirjete loomine mitmes rakenduses on tavaline.</span><span class="sxs-lookup"><span data-stu-id="e278a-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="e278a-105">Näiteks võib müügitegevus tuua ärikliendi kirjeid rakenduse Sales kaudu ja e-kaubandus või jaemüük võivad tuua kliendikirjeid rakenduse Finance and Operations kaudu.</span><span class="sxs-lookup"><span data-stu-id="e278a-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="e278a-106">Olenemata sellest, kust kliendikirje pärineb, on see integreeritud kulisside taga üle rakenduste piiride ja taristute erinevuste.</span><span class="sxs-lookup"><span data-stu-id="e278a-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="e278a-107">Integreeritud klientide loomine aitab käsitleda mitut loodud stsenaariumi ja annab põhjaliku kliendivaate Dynamics 365 rakenduse komplektile.</span><span class="sxs-lookup"><span data-stu-id="e278a-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="e278a-108">Kliendiandmete voog</span><span class="sxs-lookup"><span data-stu-id="e278a-108">Customer data flow</span></span>

<span data-ttu-id="e278a-109">*Klient* on rakendustes täpselt määratletud mõiste.</span><span class="sxs-lookup"><span data-stu-id="e278a-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="e278a-110">Seetõttu hõlmab kliendiandmete integreerimine lihtsalt kliendikontseptsiooni ühtlustamist kahe rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="e278a-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="e278a-111">Järgmine illustratsioon näitab kliendiandmete voogu.</span><span class="sxs-lookup"><span data-stu-id="e278a-111">The following illustration shows the customer data flow.</span></span>

![Kliendiandmete voog](media/dual-write-customer-data-flow.png)

<span data-ttu-id="e278a-113">Kliente saab laias laastus liigitada kahte tüüpi: äri-/organisatsioonikliendid ning tarbijad/lõppkasutajad.</span><span class="sxs-lookup"><span data-stu-id="e278a-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="e278a-114">Neid kahte tüüpi kliente talletatakse ja käsitletakse rakendustes Finance and Operations ja Common Data Service erinevalt.</span><span class="sxs-lookup"><span data-stu-id="e278a-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="e278a-115">Rakenduses Finance and Operations luuakse nii äri-/organisatsioonikliendid kui ka tarbijad/lõppkasutajad ühed tabelis nimetusega **CustTable** (CustomerCustomerV3Entity) ja neid liigitatakse atribuudi **Type** järgi.</span><span class="sxs-lookup"><span data-stu-id="e278a-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="e278a-116">(Kui atribuudiks **Tüüp** on määratud **Organisatsioon**, on klient äri-/organisatsiooniklient ja kui atribuudiks **Tüüp** on määratud **Isik**, on klient tarbija/lõppkasutaja.) Esmase kontaktisiku teavet töödeldakse olemi SMMContactPersonEntity kaudu.</span><span class="sxs-lookup"><span data-stu-id="e278a-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="e278a-117">Rakenduses Common Data Service luuakse äri-/organisatsioonikliendid olemis Konto ja tuvastatakse klientidena, kui atribuudiks **Seose tüüp** on määratud **Klient**.</span><span class="sxs-lookup"><span data-stu-id="e278a-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="e278a-118">Nii tarbijaid/lõppkasutajaid kui ka kontaktisikut esindab olem Kontakt.</span><span class="sxs-lookup"><span data-stu-id="e278a-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="e278a-119">Et tagada tarbija/lõppkasutaja ja kontaktisiku selge eristamine, on olemil**Kontakt** loogikalipp nimega **Müüdav**.</span><span class="sxs-lookup"><span data-stu-id="e278a-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="e278a-120">Kui **Müüdav** on **Tõene**, on kontakt tarbija/lõppkasutaja ja selle kontakt jaoks saab luua pakkumisi ja tellimusi.</span><span class="sxs-lookup"><span data-stu-id="e278a-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="e278a-121">Kui **Müüdav** on **Väär**, on kontakt vaid kliendi esmane kontaktisik.</span><span class="sxs-lookup"><span data-stu-id="e278a-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="e278a-122">Kui mittemüüdav kontakt osaleb pakkumise või tellimuse toimingus, on atribuudiks **Müüdav** määratud **Tõene**, et märkida kontakt lipuga müüdava kontaktina.</span><span class="sxs-lookup"><span data-stu-id="e278a-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="e278a-123">Kontakt, kes on saanud müüdavaks kontaktiks, jääb müüdavaks kontaktiks.</span><span class="sxs-lookup"><span data-stu-id="e278a-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="e278a-124">Mallid</span><span class="sxs-lookup"><span data-stu-id="e278a-124">Templates</span></span>

<span data-ttu-id="e278a-125">Kliendiandmed sisaldavad kogu teavet kliendi kohta (nt. kliendigrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil ja püsikliendi olek).</span><span class="sxs-lookup"><span data-stu-id="e278a-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="e278a-126">Olemikaartide kogum toimib koos kliendiandmete suhtluse ajal, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="e278a-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="e278a-127">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="e278a-127">Finance and Operations apps</span></span> | <span data-ttu-id="e278a-128">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="e278a-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="e278a-129">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e278a-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="e278a-130">CDS-i kontaktid V2</span><span class="sxs-lookup"><span data-stu-id="e278a-130">CDS Contacts V2</span></span>             | <span data-ttu-id="e278a-131">kontaktid</span><span class="sxs-lookup"><span data-stu-id="e278a-131">contacts</span></span>                        | <span data-ttu-id="e278a-132">See mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="e278a-133">Kliendigrupid</span><span class="sxs-lookup"><span data-stu-id="e278a-133">Customer groups</span></span>             | <span data-ttu-id="e278a-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="e278a-134">msdyn_customergroups</span></span>            | <span data-ttu-id="e278a-135">See mall sünkroonib kliendigrupi teabe.</span><span class="sxs-lookup"><span data-stu-id="e278a-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="e278a-136">Kliendi makseviis</span><span class="sxs-lookup"><span data-stu-id="e278a-136">Customer payment method</span></span>     | <span data-ttu-id="e278a-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="e278a-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="e278a-138">See mall sünkroonib kliendi makseviisi teabe.</span><span class="sxs-lookup"><span data-stu-id="e278a-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="e278a-139">Kliendid V3</span><span class="sxs-lookup"><span data-stu-id="e278a-139">Customers V3</span></span>                | <span data-ttu-id="e278a-140">kontod</span><span class="sxs-lookup"><span data-stu-id="e278a-140">accounts</span></span>                        | <span data-ttu-id="e278a-141">See mall sünkroonib äri-ja organisatsiooniklientide kliendi koondteabe.</span><span class="sxs-lookup"><span data-stu-id="e278a-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="e278a-142">Kliendid V3</span><span class="sxs-lookup"><span data-stu-id="e278a-142">Customers V3</span></span>                | <span data-ttu-id="e278a-143">kontaktid</span><span class="sxs-lookup"><span data-stu-id="e278a-143">contacts</span></span>                        | <span data-ttu-id="e278a-144">See mall sünkroonib tarbijate ja lõppkasutajate kliendi koondandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="e278a-145">Kliendikaart</span><span class="sxs-lookup"><span data-stu-id="e278a-145">Loyalty card</span></span>                | <span data-ttu-id="e278a-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="e278a-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="e278a-147">See mall sünkroonib kliendikaardi teabe.</span><span class="sxs-lookup"><span data-stu-id="e278a-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="e278a-148">Nime liited</span><span class="sxs-lookup"><span data-stu-id="e278a-148">Name affixes</span></span>                | <span data-ttu-id="e278a-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="e278a-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="e278a-150">See mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e278a-151">CDS V2 maksepäeva read</span><span class="sxs-lookup"><span data-stu-id="e278a-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="e278a-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="e278a-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="e278a-153">See mall sünkroonib nii klientide kui ka hankijate maksepäeva ridade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e278a-154">CDS-i maksepäevad</span><span class="sxs-lookup"><span data-stu-id="e278a-154">Payment days CDS</span></span>            | <span data-ttu-id="e278a-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="e278a-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="e278a-156">See mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e278a-157">Maksegraafiku read</span><span class="sxs-lookup"><span data-stu-id="e278a-157">Payment schedule lines</span></span>      | <span data-ttu-id="e278a-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="e278a-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="e278a-159">Sünkroonib nii klientide kui ka hankijate maksegraafiku ridade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e278a-160">Maksegraafik</span><span class="sxs-lookup"><span data-stu-id="e278a-160">Payment schedule</span></span>            | <span data-ttu-id="e278a-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="e278a-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="e278a-162">See mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e278a-163">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="e278a-163">Terms of payment</span></span>            | <span data-ttu-id="e278a-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="e278a-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="e278a-165">See mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="e278a-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
