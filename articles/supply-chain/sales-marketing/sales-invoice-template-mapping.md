---
title: "Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6db68236f512cc720e75c0d576ce4c49d6c87882
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="dd68e-103">Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="dd68e-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dd68e-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="dd68e-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="dd68e-105">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="dd68e-105">Templates and tasks</span></span>

<span data-ttu-id="dd68e-106">Müügiarvete päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="dd68e-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="dd68e-107">**Malli nimi andmete integratsioonis**</span><span class="sxs-lookup"><span data-stu-id="dd68e-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="dd68e-108">Müügiarved (Fin and Opsist Salesi)</span><span class="sxs-lookup"><span data-stu-id="dd68e-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="dd68e-109">**Ülesannete nimed andmete integratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="dd68e-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="dd68e-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="dd68e-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="dd68e-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="dd68e-111">SalesInvoiceLine</span></span>

<span data-ttu-id="dd68e-112">Enne Salesi müügiarve päise ja ridade sünkroonimist vajalikud sünkroonimistoimingud.</span><span class="sxs-lookup"><span data-stu-id="dd68e-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="dd68e-113">Tooted (Fin and Opsist Salesi)</span><span class="sxs-lookup"><span data-stu-id="dd68e-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="dd68e-114">Kontod (Salesist Fin and Opsi) (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="dd68e-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="dd68e-115">Kontaktid (Salesist Fin and Opsi) (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="dd68e-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="dd68e-116">Müügitellimuse päis ja read (Fin and Opsist Salesi)</span><span class="sxs-lookup"><span data-stu-id="dd68e-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="dd68e-117">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="dd68e-117">Entity set</span></span>

| <span data-ttu-id="dd68e-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd68e-118">Finance and Operations</span></span>                               | <span data-ttu-id="dd68e-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="dd68e-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="dd68e-120">Müük</span><span class="sxs-lookup"><span data-stu-id="dd68e-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="dd68e-121">Väliselt hallatava kliendi müügiarve päised</span><span class="sxs-lookup"><span data-stu-id="dd68e-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="dd68e-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="dd68e-122">SalesInvoice</span></span>     | <span data-ttu-id="dd68e-123">Arved</span><span class="sxs-lookup"><span data-stu-id="dd68e-123">Invoices</span></span>       |
| <span data-ttu-id="dd68e-124">Väliselt hallatava kliendi müügiarve read</span><span class="sxs-lookup"><span data-stu-id="dd68e-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="dd68e-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="dd68e-125">SalesInvoiceLine</span></span> | <span data-ttu-id="dd68e-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="dd68e-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="dd68e-127">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="dd68e-127">Entity flow</span></span>

<span data-ttu-id="dd68e-128">Müügiarved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="dd68e-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="dd68e-129">Jaotises **Müügiarve päis** olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="dd68e-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="dd68e-130">See on nii, kuna Sales ei toeta maksuteavet päise tasandil.</span><span class="sxs-lookup"><span data-stu-id="dd68e-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="dd68e-131">Rea tasandil tasudega seotud maksu arvestatakse.</span><span class="sxs-lookup"><span data-stu-id="dd68e-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="dd68e-132">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="dd68e-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="dd68e-133">**Arve numbri väli** lisatakse üksusele **Arve** ja kuvatakse lehel.</span><span class="sxs-lookup"><span data-stu-id="dd68e-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="dd68e-134">Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Finance and Operationsis ja sünkroonitakse Salesiga.</span><span class="sxs-lookup"><span data-stu-id="dd68e-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="dd68e-135">Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Finance and Operationsist.</span><span class="sxs-lookup"><span data-stu-id="dd68e-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="dd68e-136">**Müügitellimuse olek** muutub automaatselt olekuks **Arveldatud**, kui seotud arve Finance and Operationsist on Salesiga sünkroonitud.</span><span class="sxs-lookup"><span data-stu-id="dd68e-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="dd68e-137">Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks.</span><span class="sxs-lookup"><span data-stu-id="dd68e-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="dd68e-138">See annab müügitellimuse omanikule võimaluse arvet vaadata.</span><span class="sxs-lookup"><span data-stu-id="dd68e-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="dd68e-139">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="dd68e-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="dd68e-140">Enne müügiarvete sünkroonimist on oluline värskendada süsteeme järgmise sättega.</span><span class="sxs-lookup"><span data-stu-id="dd68e-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="dd68e-141">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="dd68e-141">Setup in Sales</span></span>

- <span data-ttu-id="dd68e-142">Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Kasuta süsteemi hinna arvutamise süsteemi** väärtuseks oleks määratud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="dd68e-143">Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Allahindluse arvutamise meetod** väärtuseks oleks määratud **Reaüksus**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="dd68e-144">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="dd68e-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="dd68e-145">Toiming SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="dd68e-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="dd68e-146">Värskendage väärtuse **CDS-i organisatsiooni ID** vastendus jaotises **Allikas** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="dd68e-147">Atribuudi **SalesOrder_Organization_OrganizationId** vaikemalli väärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="dd68e-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="dd68e-148">Atribuudi **Account_Organization_OrganizationId** malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="dd68e-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="dd68e-149">Atribuudi **Organization_OrganizationId** malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="dd68e-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="dd68e-150">Veenduge, et jaotise **Allikas** > **CDS atribuudile InvoiceCountryRegionId** ja **BillingAddress_Country** vahel oleks vajalik vastendus olemas.</span><span class="sxs-lookup"><span data-stu-id="dd68e-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="dd68e-151">Malli väärtus on **ValueMap** koos vastendatud riikide arvuga.</span><span class="sxs-lookup"><span data-stu-id="dd68e-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="dd68e-152">**Hinnakiri** on vajalik arvete koostamiseks rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="dd68e-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="dd68e-153">Värskendage parameetrit **ValueMap** jaotises **CDS** > **Üksuse pricelevelid.name [hinnakirja nimi] sihtkoht** väärtuseks **Hinnakiri**, mida kasutatakse jaotises Müük valuuta kohta.</span><span class="sxs-lookup"><span data-stu-id="dd68e-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="dd68e-154">Võite kasutada vaikeväärtust **Hinnakiri** ühe valuuta kohta või parameetrit **ValueMap**, kui teil on erinevates valuutades **hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="dd68e-155">Üksuse **pricelevelid.name [hinnakirja nimi]** malli väärtus on **ValueMap**, mis põhineb väärtusel **Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="dd68e-156">usd: USA CRM-i teenus (näidis).</span><span class="sxs-lookup"><span data-stu-id="dd68e-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="dd68e-157">Toiming SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="dd68e-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="dd68e-158">Veenduge, et vajalik vastendus oleks olemas, jaotises **Allikas** > **CDS mõõtühikuna**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="dd68e-159">Veenduge, et vajalik **ValueMap** parameetrile **SalesUnitSymbol** rakenduses Finance and Operations oleks olemas jaotises **Allikas** > **CDS-i vastendus**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="dd68e-160">Malli väärtus parameetriga **ValueMap** määratletakse üksusele **SalesUnitSymbol to Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="dd68e-161">Värskendage väärtuse **CDS-i organisatsiooni ID vastendus jaotises Allikas** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="dd68e-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="dd68e-162">Atribuudi **SalesInvoicer_Organization_OrganizationId** vaikemalli väärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="dd68e-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="dd68e-163">Atribuudi **Product_Organization_OrganizationId** malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="dd68e-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="dd68e-164">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="dd68e-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="dd68e-165">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="dd68e-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="dd68e-166">Nende väljade vastendamiseks on vaja seadistada väärtuskaart, mis põhineb nende organisatsioonide andmetel, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="dd68e-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="dd68e-167">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="dd68e-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="dd68e-172">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="dd68e-172">Related topics</span></span>

[<span data-ttu-id="dd68e-173">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="dd68e-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="dd68e-174">Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="dd68e-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="dd68e-175">Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="dd68e-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="dd68e-176">Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd68e-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="dd68e-177">Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="dd68e-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


