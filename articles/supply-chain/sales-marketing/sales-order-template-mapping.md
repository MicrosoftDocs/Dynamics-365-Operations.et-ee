---
title: "Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 707efc97afc0679ed1fc22539789e98cbabcb581
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="97546-103">Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="97546-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="97546-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="97546-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="97546-105">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="97546-105">Template and tasks</span></span>

<span data-ttu-id="97546-106">Müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="97546-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="97546-107">**Malli nimi andmete integratsioonis**</span><span class="sxs-lookup"><span data-stu-id="97546-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="97546-108">Müügtellimused (Fin and Opsist Salesi)</span><span class="sxs-lookup"><span data-stu-id="97546-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="97546-109">**Ülesannete nimed andmete integratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="97546-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="97546-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="97546-110">OrderHeader</span></span>
    - <span data-ttu-id="97546-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="97546-111">OrderLine</span></span>

<span data-ttu-id="97546-112">Enne Salesi müügiarve päise ja ridade sünkroonimist vajalikud sünkroonimistoimingud.</span><span class="sxs-lookup"><span data-stu-id="97546-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="97546-113">Tooted (Fin and Opsist Salesi)</span><span class="sxs-lookup"><span data-stu-id="97546-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="97546-114">Kontod (Salesist Fin and Opsi) (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="97546-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="97546-115">Kontaktid klientideks (Salesist Fin and Opsi) (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="97546-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="97546-116">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="97546-116">Entity set</span></span>

| <span data-ttu-id="97546-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97546-117">Finance and Operations</span></span> |    <span data-ttu-id="97546-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="97546-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="97546-119">Müük</span><span class="sxs-lookup"><span data-stu-id="97546-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="97546-120">CDS-i müügitellimuste päised CDS</span><span class="sxs-lookup"><span data-stu-id="97546-120">CDS sales order headers</span></span>| <span data-ttu-id="97546-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="97546-121">SalesOrder</span></span>     | <span data-ttu-id="97546-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="97546-122">SalesOrders</span></span> |
| <span data-ttu-id="97546-123">CDS-i müügitellimuse read</span><span class="sxs-lookup"><span data-stu-id="97546-123">CDS sales order lines</span></span>  | <span data-ttu-id="97546-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="97546-124">SalesOrderLine</span></span> | <span data-ttu-id="97546-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="97546-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="97546-126">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="97546-126">Entity flow</span></span>

<span data-ttu-id="97546-127">Müügitellimused luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="97546-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="97546-128">Malli filtrid tagavad ainult asjakohaste müügitellimuste kaasamise sünkroonimisse.</span><span class="sxs-lookup"><span data-stu-id="97546-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="97546-129">Sünkroonimisse lisatakse nii tellimuse kui ka arvelduse klient rakenduse Sales müügitellimuselt.</span><span class="sxs-lookup"><span data-stu-id="97546-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="97546-130">Rakenduses Finance and Operations kasutatakse välju **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** andmeüksustes sünkroonimise jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="97546-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="97546-131">Üksuse **Müügitellimus** rakenduses Finance and Operations peab kinnitama.</span><span class="sxs-lookup"><span data-stu-id="97546-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="97546-132">Rakendusega Sales sünkroonitakse ainult kõrgema töötlemisolekuga kinnitatud müügitellimused, nt olekuga Saadetud või arveldatud.</span><span class="sxs-lookup"><span data-stu-id="97546-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="97546-133">Pärast müügitellimuse loomist või muutmist tuleb käivitada pakett-töö **Müügi kogusummade arvutamine** rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97546-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="97546-134">CDS-i ja Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud.</span><span class="sxs-lookup"><span data-stu-id="97546-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="97546-135">Jaotises **Müügitellimuse päis** olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="97546-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="97546-136">See on nii, kuna Sales ei toeta maksuteavet päise tasandil.</span><span class="sxs-lookup"><span data-stu-id="97546-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="97546-137">Rea tasandil tasudega seotud maksu arvestatakse.</span><span class="sxs-lookup"><span data-stu-id="97546-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="97546-138">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="97546-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="97546-139">Üksusele **Tellimus** lisatakse uued väljad ja need kuvatakse järgmisel lehel.</span><span class="sxs-lookup"><span data-stu-id="97546-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="97546-140">**Hallatakse väliselt** – seadke väärtusele **Jah**, kui tellimus rakendusest Finance and Operations tuleb.</span><span class="sxs-lookup"><span data-stu-id="97546-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="97546-141">**Töötlemise olek** – kasutatakse tellimuse töötlemise oleku kuvamiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97546-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="97546-142">Väärtused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="97546-142">Values are:</span></span>

    - <span data-ttu-id="97546-143">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="97546-143">Active</span></span>
    - <span data-ttu-id="97546-144">Kinnitatud</span><span class="sxs-lookup"><span data-stu-id="97546-144">Confirmed</span></span>
    - <span data-ttu-id="97546-145">Saateleht</span><span class="sxs-lookup"><span data-stu-id="97546-145">Packing Slip</span></span>
    - <span data-ttu-id="97546-146">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="97546-146">Invoiced</span></span>
    - <span data-ttu-id="97546-147">Komplekteeritud</span><span class="sxs-lookup"><span data-stu-id="97546-147">Picked</span></span>
    - <span data-ttu-id="97546-148">Osaliselt komplekteeritud</span><span class="sxs-lookup"><span data-stu-id="97546-148">Partially Picked</span></span>
    - <span data-ttu-id="97546-149">Osaliselt pakitud</span><span class="sxs-lookup"><span data-stu-id="97546-149">Partially Packed</span></span>
    - <span data-ttu-id="97546-150">Välja saadetud</span><span class="sxs-lookup"><span data-stu-id="97546-150">Shipped</span></span>
    - <span data-ttu-id="97546-151">Osaliselt tarnitud</span><span class="sxs-lookup"><span data-stu-id="97546-151">Partially Shipped</span></span>
    - <span data-ttu-id="97546-152">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="97546-152">Partially Invoiced</span></span>
    - <span data-ttu-id="97546-153">Tühistatud</span><span class="sxs-lookup"><span data-stu-id="97546-153">Cancelled</span></span>

<span data-ttu-id="97546-154">Sätet **Sisaldab ainult väliselt hallatavaid tooteid** kasutatakse teistes müügitellimuse stsenaariumides (rakendusest Sales rakendusse Finance and Operations sünkroonimisel), et jälgida, kas müügitellimus koosneb täielikult **väliselt hallatavatest toodetest**, millisel juhul tooteid hallatakse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97546-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="97546-155">See tagab, et te ei püüa sünkroonida müügitellimuse ridu toodetega, mis on rakendusele Finance and Operations tundmatud.</span><span class="sxs-lookup"><span data-stu-id="97546-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="97546-156">Nupud **Arve koostamine**, **Tellimuse tühistamine**, **Ümberarvutamine**, **Toodete toomine** ja **Aadressi otsimine** lehel **Müügitellimus** on väliselt hallatavate tellimuste puhul peidetud, kuna arved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="97546-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="97546-157">Tellimuse lehte ei saa redigeerida, müügitellimuse teave sünkroonitakse Finance and Operationsist.</span><span class="sxs-lookup"><span data-stu-id="97546-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="97546-158">**Müügitellimuse olek** jääb aktiivseks, et rakenduse Finance and Operations muudatused saaksid liikuda rakenduses Sales jaotisse **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="97546-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="97546-159">Seda juhitakse, määrates andmeintegratsiooni projektis vaikeväärtuse **Olekukood [olek]** väärtuseks **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="97546-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="97546-160">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="97546-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="97546-161">Enne müügitellimuste sünkroonimist on oluline värskendada süsteeme järgmise sättega.</span><span class="sxs-lookup"><span data-stu-id="97546-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="97546-162">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="97546-162">Setup in Sales</span></span>

- <span data-ttu-id="97546-163">Tagage meeskonnale load, millele kasutaja (teie rakenduse Sales jaotisest **Ühendusekomplekt**) on määratud.</span><span class="sxs-lookup"><span data-stu-id="97546-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="97546-164">Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte.</span><span class="sxs-lookup"><span data-stu-id="97546-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="97546-165">Ilma selleta saate tõrke, et peamine töörühm puudub, kui käivitate projekti andmete integraatorist.</span><span class="sxs-lookup"><span data-stu-id="97546-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="97546-166">Valige jaotisest **Sätted** > **Turve** > **Töörühmad** asjakohane töörühm, klõpsake valikut **Rollide haldamine** ja valige soovitud õigustega roll, nt Süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="97546-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="97546-167">Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Kasuta süsteemi hinna arvutamise süsteemi** väärtuseks oleks määratud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="97546-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="97546-168">Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Allahindluse arvutamise meetod** väärtuseks oleks määratud **Reaüksus**.</span><span class="sxs-lookup"><span data-stu-id="97546-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="97546-169">Seadistus rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97546-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="97546-170">Määrake **Müük ja turundus** > **Perioodilised ülesanded** > **Müügi kogusummade arvutamine** töötama pakett-tööna, nii et valiku **Müügitellimuste kogusummade arvutamine** väärtuseks on määratud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="97546-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="97546-171">See on oluline, kuna CDS-i ja Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud.</span><span class="sxs-lookup"><span data-stu-id="97546-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="97546-172">Pakett-töö sagedus tuleks sobitada müügitellimuse sünkroonimise sagedusega.</span><span class="sxs-lookup"><span data-stu-id="97546-172">The frequence of the batch job should be alligned with the frequence of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="97546-173">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="97546-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="97546-174">Ülesanne SalesHeader</span><span class="sxs-lookup"><span data-stu-id="97546-174">SalesHeader task</span></span>

- <span data-ttu-id="97546-175">Värskendage väärtuse **CDS-i organisatsiooni ID vastendus jaotises Allikas** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="97546-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="97546-176">Atribuudi **Account_Organization_OrganizationId** malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="97546-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="97546-177">Atribuudi **InvoiceAccount_Organization_OrganizationId** malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="97546-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="97546-178">Atribuudi **Organization_OrganizationId** malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="97546-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="97546-179">Veenduge, et oleks olemas vajalik vastendus atribuutide **Allikas** > **CDS atribuudile InvoiceCountryRegionId ja BillingAddress_Country** ning **DeliveryCountryRegionId ja DeliveryAddress_Country** vahel.</span><span class="sxs-lookup"><span data-stu-id="97546-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="97546-180">Malli väärtus on **ValueMap** koos vastendatud riikide arvuga.</span><span class="sxs-lookup"><span data-stu-id="97546-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="97546-181">**Hinnakiri** on vajalik tellimuste koostamiseks rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="97546-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="97546-182">Värskendage parameetrit **ValueMap** jaotises **CDS** > **Üksuse** **pricelevelid.name [hinnakirja nimi] sihtkoht** väärtuseks **Hinnakiri**, mida kasutatakse jaotises Müük valuuta kohta.</span><span class="sxs-lookup"><span data-stu-id="97546-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="97546-183">Võite kasutada vaikeväärtust **Hinnakiri** ühe valuuta kohta või parameetrit **ValueMap**, kui teil on erinevates valuutades **hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="97546-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="97546-184">Üksuse **pricelevelid.name [hinnakirja nimi]** malli vaikeväärtus on USA CRM-i teenus (näidis).</span><span class="sxs-lookup"><span data-stu-id="97546-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="97546-185">Ülesanne SalesLine</span><span class="sxs-lookup"><span data-stu-id="97546-185">SalesLine task</span></span>

- <span data-ttu-id="97546-186">Värskendage väärtuse **CDS-i organisatsiooni ID vastendus jaotises Allikas** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="97546-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="97546-187">Atribuudi **SalesOrder_Organization_OrganizationId** vaikemalli väärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="97546-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="97546-188">Atribuudi **Product_Organization_OrganizationId** malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="97546-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="97546-189">Veenduge, et jaotise **Allikas** > **CDS** atribuudile **DeliveryCountryRegionId** ja **DeliveryAddress_Country** vahel oleks vajalik vastendus olemas.</span><span class="sxs-lookup"><span data-stu-id="97546-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="97546-190">Malli väärtus on **ValueMap** koos vastendatud riikide arvuga.</span><span class="sxs-lookup"><span data-stu-id="97546-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="97546-191">Veenduge, et vajalik **ValueMap** parameetrile **SalesUnitSymbol** rakenduses Finance and Operations oleks olemas jaotises **Allikas** > **CDS-i vastendus**.</span><span class="sxs-lookup"><span data-stu-id="97546-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="97546-192">Malli väärtus parameetriga **ValueMap** määratletakse üksusele **SalesUnitSymbol to Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="97546-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="97546-193">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="97546-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="97546-194">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="97546-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="97546-195">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="97546-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="97546-196">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="97546-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="97546-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="97546-197">OrderHeader</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-1.png)

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="97546-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="97546-200">OrderLine</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-3.png)

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="97546-203">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="97546-203">Related topics</span></span>

[<span data-ttu-id="97546-204">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="97546-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="97546-205">Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="97546-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="97546-206">Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="97546-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="97546-207">Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97546-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="97546-208">Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="97546-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


