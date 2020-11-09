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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 36716c302d86bc5715798bf4cf4899f666d0872c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997450"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="ad33e-103">Integreeritud kliendi koondandmed</span><span class="sxs-lookup"><span data-stu-id="ad33e-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="ad33e-104">Kliendiandmeid saab luua rohkem kui ühes Dynamics 365 rakenduses.</span><span class="sxs-lookup"><span data-stu-id="ad33e-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="ad33e-105">Näiteks kliendikirje võib pärineda Dynamics 365 Salesi müügitegevusest (mudeljuhitud Dynamics 365 rakendus) või Dynamics 365 Commerce'i jaemüügi tegevusest (Finance and Operationsi rakendus).</span><span class="sxs-lookup"><span data-stu-id="ad33e-105">For example, a customer record can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a record can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="ad33e-106">Olenemata sellest, kust kliendiandmed pärinevad, on see integreeritud kulisside taga.</span><span class="sxs-lookup"><span data-stu-id="ad33e-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="ad33e-107">Integreeritud kliendi koondandmed annavad teile paindlikkuse luua kliendiandmeid kõigis Dynamics 365 rakendustes ja põhjaliku ülevaate kliendi kohta Dynamics 365 rakenduse komplektis.</span><span class="sxs-lookup"><span data-stu-id="ad33e-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="ad33e-108">Kliendiandmete voog</span><span class="sxs-lookup"><span data-stu-id="ad33e-108">Customer data flow</span></span>

<span data-ttu-id="ad33e-109">*Klient* on rakendustes täpselt määratletud mõiste.</span><span class="sxs-lookup"><span data-stu-id="ad33e-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="ad33e-110">Seetõttu hõlmab kliendiandmete integreerimine lihtsalt kliendikontseptsiooni ühtlustamist kahe rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="ad33e-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="ad33e-111">Järgmine illustratsioon näitab kliendiandmete voogu.</span><span class="sxs-lookup"><span data-stu-id="ad33e-111">The following illustration shows the customer data flow.</span></span>

![Kliendiandmete voog](media/dual-write-customer-data-flow.png)

<span data-ttu-id="ad33e-113">Kliente saab laias laastus liigitada kahte tüüpi: äri-/organisatsioonikliendid ning tarbijad/lõppkasutajad.</span><span class="sxs-lookup"><span data-stu-id="ad33e-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="ad33e-114">Neid kahte tüüpi kliente talletatakse ja käsitletakse rakendustes Finance and Operations ja Common Data Service erinevalt.</span><span class="sxs-lookup"><span data-stu-id="ad33e-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="ad33e-115">Rakenduses Finance and Operations luuakse nii äri-/organisatsioonikliendid kui ka tarbijad/lõppkasutajad ühed tabelis nimetusega **CustTable** (CustCustomerV3Entity) ja neid liigitatakse atribuudi **Tüüp** järgi.</span><span class="sxs-lookup"><span data-stu-id="ad33e-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="ad33e-116">(Kui atribuudiks **Tüüp** on määratud **Organisatsioon** , on klient äri-/organisatsiooniklient ja kui atribuudiks **Tüüp** on määratud **Isik** , on klient tarbija/lõppkasutaja.) Esmase kontaktisiku teavet töödeldakse olemi SMMContactPersonEntity kaudu.</span><span class="sxs-lookup"><span data-stu-id="ad33e-116">(If **Type** is set to **Organization** , the customer is a commercial/organizational customer, and if **Type** is set to **Person** , the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="ad33e-117">Rakenduses Common Data Service luuakse äri-/organisatsioonikliendid olemis Konto ja tuvastatakse klientidena, kui atribuudiks **Seose tüüp** on määratud **Klient**.</span><span class="sxs-lookup"><span data-stu-id="ad33e-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="ad33e-118">Nii tarbijaid/lõppkasutajaid kui ka kontaktisikut esindab olem Kontakt.</span><span class="sxs-lookup"><span data-stu-id="ad33e-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="ad33e-119">Et tagada tarbija/lõppkasutaja ja kontaktisiku selge eristamine, on olemil **Kontakt** loogikalipp nimega **Müüdav**.</span><span class="sxs-lookup"><span data-stu-id="ad33e-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="ad33e-120">Kui **Müüdav** on **Tõene** , on kontakt tarbija/lõppkasutaja ja selle kontakt jaoks saab luua pakkumisi ja tellimusi.</span><span class="sxs-lookup"><span data-stu-id="ad33e-120">When **Sellable** is **True** , the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="ad33e-121">Kui **Müüdav** on **Väär** , on kontakt vaid kliendi esmane kontaktisik.</span><span class="sxs-lookup"><span data-stu-id="ad33e-121">When **Sellable** is **False** , the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="ad33e-122">Kui mittemüüdav kontakt osaleb pakkumise või tellimuse toimingus, on atribuudiks **Müüdav** määratud **Tõene** , et märkida kontakt lipuga müüdava kontaktina.</span><span class="sxs-lookup"><span data-stu-id="ad33e-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="ad33e-123">Kontakt, kes on saanud müüdavaks kontaktiks, jääb müüdavaks kontaktiks.</span><span class="sxs-lookup"><span data-stu-id="ad33e-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="ad33e-124">Mallid</span><span class="sxs-lookup"><span data-stu-id="ad33e-124">Templates</span></span>

<span data-ttu-id="ad33e-125">Kliendiandmed sisaldavad kogu teavet kliendi kohta (nt. kliendigrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil ja püsikliendi olek).</span><span class="sxs-lookup"><span data-stu-id="ad33e-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="ad33e-126">Olemikaartide kogum toimib koos kliendiandmete suhtluse ajal, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="ad33e-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="ad33e-127">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="ad33e-127">Finance and Operations apps</span></span> | <span data-ttu-id="ad33e-128">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="ad33e-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="ad33e-129">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad33e-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="ad33e-130">CDS-i kontaktid V2</span><span class="sxs-lookup"><span data-stu-id="ad33e-130">CDS Contacts V2</span></span>             | <span data-ttu-id="ad33e-131">kontaktid</span><span class="sxs-lookup"><span data-stu-id="ad33e-131">contacts</span></span>                        | <span data-ttu-id="ad33e-132">See mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="ad33e-133">Kliendigrupid</span><span class="sxs-lookup"><span data-stu-id="ad33e-133">Customer groups</span></span>             | <span data-ttu-id="ad33e-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="ad33e-134">msdyn_customergroups</span></span>            | <span data-ttu-id="ad33e-135">See mall sünkroonib kliendigrupi teabe.</span><span class="sxs-lookup"><span data-stu-id="ad33e-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="ad33e-136">Kliendi makseviis</span><span class="sxs-lookup"><span data-stu-id="ad33e-136">Customer payment method</span></span>     | <span data-ttu-id="ad33e-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="ad33e-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="ad33e-138">See mall sünkroonib kliendi makseviisi teabe.</span><span class="sxs-lookup"><span data-stu-id="ad33e-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="ad33e-139">Kliendid V3</span><span class="sxs-lookup"><span data-stu-id="ad33e-139">Customers V3</span></span>                | <span data-ttu-id="ad33e-140">kontod</span><span class="sxs-lookup"><span data-stu-id="ad33e-140">accounts</span></span>                        | <span data-ttu-id="ad33e-141">See mall sünkroonib äri-ja organisatsiooniklientide kliendi koondteabe.</span><span class="sxs-lookup"><span data-stu-id="ad33e-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="ad33e-142">Kliendid V3</span><span class="sxs-lookup"><span data-stu-id="ad33e-142">Customers V3</span></span>                | <span data-ttu-id="ad33e-143">kontaktid</span><span class="sxs-lookup"><span data-stu-id="ad33e-143">contacts</span></span>                        | <span data-ttu-id="ad33e-144">See mall sünkroonib tarbijate ja lõppkasutajate kliendi koondandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="ad33e-145">Nime liited</span><span class="sxs-lookup"><span data-stu-id="ad33e-145">Name affixes</span></span>                | <span data-ttu-id="ad33e-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="ad33e-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="ad33e-147">See mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="ad33e-148">CDS V2 maksepäeva read</span><span class="sxs-lookup"><span data-stu-id="ad33e-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="ad33e-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="ad33e-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="ad33e-150">See mall sünkroonib nii klientide kui ka hankijate maksepäeva ridade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="ad33e-151">CDS-i maksepäevad</span><span class="sxs-lookup"><span data-stu-id="ad33e-151">Payment days CDS</span></span>            | <span data-ttu-id="ad33e-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="ad33e-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="ad33e-153">See mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="ad33e-154">Maksegraafiku read</span><span class="sxs-lookup"><span data-stu-id="ad33e-154">Payment schedule lines</span></span>      | <span data-ttu-id="ad33e-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="ad33e-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="ad33e-156">Sünkroonib nii klientide kui ka hankijate maksegraafiku ridade viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="ad33e-157">Maksegraafik</span><span class="sxs-lookup"><span data-stu-id="ad33e-157">Payment schedule</span></span>            | <span data-ttu-id="ad33e-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="ad33e-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="ad33e-159">See mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="ad33e-160">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="ad33e-160">Terms of payment</span></span>            | <span data-ttu-id="ad33e-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="ad33e-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="ad33e-162">See mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.</span><span class="sxs-lookup"><span data-stu-id="ad33e-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
