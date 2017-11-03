---
title: "Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega"
description: "Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="69e63-103">Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="69e63-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="69e63-104">Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="69e63-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="69e63-105">Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales (Sales) rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="69e63-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="69e63-106">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="69e63-106">Template and task</span></span>

<span data-ttu-id="69e63-107">Kontode sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="69e63-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="69e63-108">**Malli nimi:** Kontod (Salesist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="69e63-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="69e63-109">**Ülesande nimi projektis:** Kontod – Konto – Kliendid</span><span class="sxs-lookup"><span data-stu-id="69e63-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="69e63-110">Nõutavad sünkroonimisülesanded enne konto/kliendi sünkroonimist: pole</span><span class="sxs-lookup"><span data-stu-id="69e63-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="69e63-111">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="69e63-111">Entity set</span></span>

| <span data-ttu-id="69e63-112">Müük</span><span class="sxs-lookup"><span data-stu-id="69e63-112">Sales</span></span>    | <span data-ttu-id="69e63-113">CDS</span><span class="sxs-lookup"><span data-stu-id="69e63-113">CDS</span></span>     | <span data-ttu-id="69e63-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="69e63-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="69e63-115">Kontod</span><span class="sxs-lookup"><span data-stu-id="69e63-115">Accounts</span></span> | <span data-ttu-id="69e63-116">Konto</span><span class="sxs-lookup"><span data-stu-id="69e63-116">Account</span></span> | <span data-ttu-id="69e63-117">Kliendid</span><span class="sxs-lookup"><span data-stu-id="69e63-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="69e63-118">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="69e63-118">Entity flow</span></span>

<span data-ttu-id="69e63-119">Kontosid hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Finance and Operations klientidena.</span><span class="sxs-lookup"><span data-stu-id="69e63-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="69e63-120">Nende klientide atribuudi **On väliselt hallatav** sätteks on määratud **Jah**, et jälgida rakendusest Sales pärit kliente.</span><span class="sxs-lookup"><span data-stu-id="69e63-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="69e63-121">Arveldamise ajal kasutatakse seda teavet rakendusega Sales sünkroonitud arvete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="69e63-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="69e63-122">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="69e63-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="69e63-123">Väli **Konto number** on saadaval lehel **Konto**.</span><span class="sxs-lookup"><span data-stu-id="69e63-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="69e63-124">See on loomulik ja korduvatu võti, et toetada integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="69e63-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="69e63-125">Kliendisuhete halduse (CRM) lahenduse loomuliku võtme funktsioon võib mõjutada kliente, kes juba kasutavad välja **Konto number**, kuid ei kasuta iga konto puhul atribuudi **Konto number** kordumatuid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="69e63-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="69e63-126">Praegu ei toeta integratsioonilahendus seda juhtumit.</span><span class="sxs-lookup"><span data-stu-id="69e63-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="69e63-127">Kui uue konto loomisel ei ole atribuudi **Konto number** väärtust veel olemas, luuakse see automaatselt numbriseeriat kasutades.</span><span class="sxs-lookup"><span data-stu-id="69e63-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="69e63-128">Väärtus sisaldab sõnet **ACC**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide.</span><span class="sxs-lookup"><span data-stu-id="69e63-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="69e63-129">Näide: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="69e63-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="69e63-130">Kui rakendatakse integratsioonilahendust rakendusele Sales, seab täiendusskript välja **Konto number** olemasolevatele kontodele rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="69e63-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="69e63-131">Kui ühtki atribuudi **Konto number** väärtust ei ole, kasutatakse varem kirjeldatud numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="69e63-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="69e63-132">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="69e63-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="69e63-133">Atribuudi **CustomerGroupId** vastendus jaotisest **CDS &gt; Sihtkoht** tuleb värskendada rakenduses Finance and Operations kehtivale väärtusele.</span><span class="sxs-lookup"><span data-stu-id="69e63-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="69e63-134">Saate määrata vaikeväärtuse või määrata väärtuse väärtuskaardi abil.</span><span class="sxs-lookup"><span data-stu-id="69e63-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="69e63-135">Malli vaikeväärtus on **10**.</span><span class="sxs-lookup"><span data-stu-id="69e63-135">The default template value is **10**.</span></span>
- <span data-ttu-id="69e63-136">Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav.</span><span class="sxs-lookup"><span data-stu-id="69e63-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="69e63-137">Sünkroonimistõrgete vältimiseks saate määrata vastendusest **CDS &gt; Sihtkoht** vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="69e63-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="69e63-138">Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="69e63-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="69e63-139">Malli vaikeväärtus atribuudi **AddressCountryRegionISOCode** puhul on **USA**.</span><span class="sxs-lookup"><span data-stu-id="69e63-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="69e63-140">Atribuudi **DeliveryAddressCountryRegionISOCode** jaoks on malli vaikeväärtus **USA**.</span><span class="sxs-lookup"><span data-stu-id="69e63-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="69e63-141">Lisades järgmised vastendused vastendusest **CDS &gt; Sihtkoht**, saate vähendada rakenduses Finance and Operations nõutavate käsitsi värskenduste arvu.</span><span class="sxs-lookup"><span data-stu-id="69e63-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="69e63-142">Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.</span><span class="sxs-lookup"><span data-stu-id="69e63-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="69e63-143">**SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="69e63-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="69e63-144">Vaikesaidi võib võtta kas tootelt või kliendilt tellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="69e63-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="69e63-145">Atribuudi **SiteId** jaoks on malli vaikeväärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="69e63-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="69e63-146">**WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="69e63-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="69e63-147">Vaikelao võib võtta kas tootelt või kliendilt tellimuse päises rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="69e63-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="69e63-148">Atribuudi **WarehouseId** jaoks on malli vaikeväärtus **13**.</span><span class="sxs-lookup"><span data-stu-id="69e63-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="69e63-149">**LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="69e63-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="69e63-150">Vaikimisi kasutatakse kliendilt saadud tellimuse päises olevat keelt.</span><span class="sxs-lookup"><span data-stu-id="69e63-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="69e63-151">Malli vaikeväärtus atribuudi **LanguageId** puhul on **en-us**.</span><span class="sxs-lookup"><span data-stu-id="69e63-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="69e63-152">CDS-i organisatsiooni ID värskendamine (**Organization_OrganizationId**) vastenduses **Allikas &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="69e63-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="69e63-153">Malli vaikeväärtus on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="69e63-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="69e63-154">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="69e63-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="69e63-155">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="69e63-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="69e63-156">Nende väljade vastendamiseks peate seadistama väärtuste vastendamise.</span><span class="sxs-lookup"><span data-stu-id="69e63-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="69e63-157">Väärtuse vastendused on kohased neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="69e63-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="69e63-158">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="69e63-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Malli vastendamine andmeintegraatoris](./media/accounts-template-mapping-data-integrator-1.png)

![Malli vastendamine kontode puhul andmeintegraatoris](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="69e63-161">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="69e63-161">Related topics</span></span>

[<span data-ttu-id="69e63-162">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="69e63-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="69e63-163">Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="69e63-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="69e63-164">Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="69e63-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="69e63-165">Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="69e63-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="69e63-166">Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="69e63-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




