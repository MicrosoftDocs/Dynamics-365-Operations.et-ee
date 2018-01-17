---
title: "Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: 534279eb0f139950a4bb568c8da04383b88e6db2
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="b6852-103">Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b6852-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b6852-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="b6852-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b6852-105">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="b6852-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b6852-106">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="b6852-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="b6852-107">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales.</span><span class="sxs-lookup"><span data-stu-id="b6852-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="b6852-108">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="b6852-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="b6852-109">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b6852-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b6852-110">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="b6852-110">Templates and tasks</span></span>

<span data-ttu-id="b6852-111">Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b6852-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b6852-112">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="b6852-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b6852-113">Müügiarvete päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="b6852-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="b6852-114">**Andmete integratsioon malli nimi:** müügiarved (rakendusest Fin and Ops rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="b6852-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b6852-115">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="b6852-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="b6852-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="b6852-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="b6852-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="b6852-117">SalesInvoiceLine</span></span>

<span data-ttu-id="b6852-118">Enne müügiarvete päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="b6852-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="b6852-119">Tooted (rakendusest Sales rakendusse Fin and Ops) – otse</span><span class="sxs-lookup"><span data-stu-id="b6852-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b6852-120">Kontod (rakendusest Sales rakendusse Fin and Ops) – otse (kui on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="b6852-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="b6852-121">Kontaktid (rakendusest Sales rakendusse Fin and Ops) – otse (kui on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="b6852-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="b6852-122">Müügitellimuse päis ja read (rakendusest Fin and Ops rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="b6852-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="b6852-123">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="b6852-123">Entity set</span></span>

| <span data-ttu-id="b6852-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b6852-124">Finance and Operations</span></span>                               | <span data-ttu-id="b6852-125">Müük</span><span class="sxs-lookup"><span data-stu-id="b6852-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="b6852-126">Väliselt hallatava kliendi müügiarve päised</span><span class="sxs-lookup"><span data-stu-id="b6852-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="b6852-127">Arved</span><span class="sxs-lookup"><span data-stu-id="b6852-127">Invoices</span></span>       |
| <span data-ttu-id="b6852-128">Väliselt hallatava kliendi müügiarve read</span><span class="sxs-lookup"><span data-stu-id="b6852-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="b6852-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="b6852-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b6852-130">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="b6852-130">Entity flow</span></span>

<span data-ttu-id="b6852-131">Müügiarved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="b6852-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="b6852-132">Müügiarve päises olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="b6852-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="b6852-133">Sales ei toeta maksuteavet päise tasandil.</span><span class="sxs-lookup"><span data-stu-id="b6852-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="b6852-134">Sünkroonimine hõlmab aga makse, mis on seotud rea tasemel tasudega.</span><span class="sxs-lookup"><span data-stu-id="b6852-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b6852-135">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="b6852-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="b6852-136">Väli **Arve number** lisati üksusesse **Arve** ja kuvatakse lehel.</span><span class="sxs-lookup"><span data-stu-id="b6852-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="b6852-137">Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Finance and Operationsis ja sünkroonitakse Salesiga.</span><span class="sxs-lookup"><span data-stu-id="b6852-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="b6852-138">Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Finance and Operationsist.</span><span class="sxs-lookup"><span data-stu-id="b6852-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="b6852-139">Väärtus **Müügitellimuse olek** asendatakse automaatselt olekuga **Arveldatud**, kui seotud arve Finance and Operationsist on Salesiga sünkroonitud.</span><span class="sxs-lookup"><span data-stu-id="b6852-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="b6852-140">Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks.</span><span class="sxs-lookup"><span data-stu-id="b6852-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="b6852-141">Seetõttu saab müügitellimuse omanik arvet vaadata.</span><span class="sxs-lookup"><span data-stu-id="b6852-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b6852-142">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="b6852-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="b6852-143">Enne müügiarvete sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="b6852-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="b6852-144">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="b6852-144">Setup in Sales</span></span>

<span data-ttu-id="b6852-145">Avage jaotis **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales** ja veenduge, et kasutusel oleks järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="b6852-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="b6852-146">Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b6852-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="b6852-147">Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.</span><span class="sxs-lookup"><span data-stu-id="b6852-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="b6852-148">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="b6852-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="b6852-149">Toiming SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="b6852-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="b6852-150">Veenduge, et atribuutide **InvoiceCountryRegionId** ja **BillingAddress\_Country** vahel oleks olemas nõutav vastendus.</span><span class="sxs-lookup"><span data-stu-id="b6852-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="b6852-151">Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni.</span><span class="sxs-lookup"><span data-stu-id="b6852-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="b6852-152">Hinnakiri on vajalik arvete koostamiseks rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="b6852-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="b6852-153">Värskendage üksuse **pricelevelid.name \[Hinnakirja nimi\]** väärtuskaarti hinnakirja alusel, mida kasutatakse rakenduses Sales valuuta kohta.</span><span class="sxs-lookup"><span data-stu-id="b6852-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="b6852-154">Saate ühe valuuta puhul kasutada vaikehinnakirja.</span><span class="sxs-lookup"><span data-stu-id="b6852-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="b6852-155">Kui teil on mitmes valuutas hinnakirju, saate kasutada väärtuskaarti.</span><span class="sxs-lookup"><span data-stu-id="b6852-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="b6852-156">Atribuudi **pricelevelid.name \[Hinnakirja nimi\]** malli väärtus on valuutal põhinev väärtuskaart, kus USA dollar = USA CRM-i teenus (näide).</span><span class="sxs-lookup"><span data-stu-id="b6852-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="b6852-157">Toiming SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="b6852-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="b6852-158">Veenduge, et atribuudi **Unit of measure** jaoks oleks olemas nõutav vastendus.</span><span class="sxs-lookup"><span data-stu-id="b6852-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="b6852-159">Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Finance and Operations olemas.</span><span class="sxs-lookup"><span data-stu-id="b6852-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="b6852-160">Üksuste **SalesUnitSymbol** ja **Quantity\_UOM** jaoks on määratletud väärtuskaardiga malli väärtus.</span><span class="sxs-lookup"><span data-stu-id="b6852-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b6852-161">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="b6852-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="b6852-162">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="b6852-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="b6852-163">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="b6852-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b6852-164">Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="b6852-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b6852-165">Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b6852-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="b6852-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="b6852-166">SalesInvoiceHeader</span></span>

![Malli vastendamine andmete integratsioonis](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="b6852-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="b6852-168">SalesInvoiceLine</span></span>

![Malli vastendamine andmete integratsioonis](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="b6852-170">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="b6852-170">Related topics</span></span>

[<span data-ttu-id="b6852-171">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="b6852-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b6852-172">Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="b6852-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b6852-173">Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="b6852-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="b6852-174">Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="b6852-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="b6852-175">Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b6852-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)







