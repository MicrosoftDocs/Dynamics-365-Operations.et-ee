---
title: Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ning ridade sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fa2772db63332319c399999bd5f747b2ac729d9e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653271"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="22133-103">Rakenduse Finance and Operations müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="22133-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22133-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ning ridade sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="22133-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="22133-105">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="22133-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="22133-106">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="22133-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="22133-107">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales.</span><span class="sxs-lookup"><span data-stu-id="22133-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="22133-108">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="22133-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="22133-109">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="22133-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="22133-110">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="22133-110">Templates and tasks</span></span>

<span data-ttu-id="22133-111">Saadaolevatele mallidele juurdepääsemiseks avage [PowerAppsi administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="22133-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="22133-112">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="22133-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="22133-113">Müügiarve päiste ja ridade sünkroonimiseks rakendusest Supply Chain Management rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="22133-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="22133-114">**Andmete integratsioon malli nimi:** müügiarved (rakendusest Fin and Ops rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="22133-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="22133-115">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="22133-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="22133-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="22133-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="22133-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="22133-117">SalesInvoiceLine</span></span>

<span data-ttu-id="22133-118">Enne müügiarvete päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="22133-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="22133-119">Tooted (rakendusest Supply Chain Management rakendusse Sales) - otse</span><span class="sxs-lookup"><span data-stu-id="22133-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="22133-120">Kontod (rakendusest Sales rakendusse Supply Chain Management) - otse (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="22133-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="22133-121">Kontaktid (rakendusest Sales rakendusse Supply Chain Management) - otse (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="22133-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="22133-122">Müügitellimuse päis ja read (rakendusest Supply Chain Management rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="22133-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="22133-123">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="22133-123">Entity set</span></span>

| <span data-ttu-id="22133-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="22133-124">Supply Chain Management</span></span>                              | <span data-ttu-id="22133-125">Müük</span><span class="sxs-lookup"><span data-stu-id="22133-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="22133-126">Väliselt hallatava kliendi müügiarve päised</span><span class="sxs-lookup"><span data-stu-id="22133-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="22133-127">Arved</span><span class="sxs-lookup"><span data-stu-id="22133-127">Invoices</span></span>       |
| <span data-ttu-id="22133-128">Väliselt hallatava kliendi müügiarve read</span><span class="sxs-lookup"><span data-stu-id="22133-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="22133-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="22133-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="22133-130">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="22133-130">Entity flow</span></span>

<span data-ttu-id="22133-131">Müügiarved luuakse rakenduses Supply Chain Management ja sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="22133-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="22133-132">Müügiarve päises olevate tasudega seotud maksu ei arvestata praegu Supply Chain Managementi ja Salesi sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="22133-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="22133-133">Sales ei toeta maksuteavet päise tasandil.</span><span class="sxs-lookup"><span data-stu-id="22133-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="22133-134">Sünkroonimine hõlmab aga makse, mis on seotud rea tasemel tasudega.</span><span class="sxs-lookup"><span data-stu-id="22133-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="22133-135">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="22133-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="22133-136">Väli **Arve number** lisati üksusesse **Arve** ja kuvatakse lehel.</span><span class="sxs-lookup"><span data-stu-id="22133-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="22133-137">Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Supply Chain Managementis ja sünkroonitakse Salesiga.</span><span class="sxs-lookup"><span data-stu-id="22133-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="22133-138">Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Supply Chain Managementist.</span><span class="sxs-lookup"><span data-stu-id="22133-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="22133-139">Väärtus **Müügitellimuse olek** asendatakse automaatselt olekuga **Arveldatud**, kui seotud arve Supply Chain Managementist on Salesiga sünkroonitud.</span><span class="sxs-lookup"><span data-stu-id="22133-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="22133-140">Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks.</span><span class="sxs-lookup"><span data-stu-id="22133-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="22133-141">Seetõttu saab müügitellimuse omanik arvet vaadata.</span><span class="sxs-lookup"><span data-stu-id="22133-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="22133-142">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="22133-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="22133-143">Enne müügiarvete sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="22133-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="22133-144">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="22133-144">Setup in Sales</span></span>

<span data-ttu-id="22133-145">Avage jaotis **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales** ja veenduge, et kasutusel oleks järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="22133-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="22133-146">Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="22133-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="22133-147">Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.</span><span class="sxs-lookup"><span data-stu-id="22133-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="22133-148">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="22133-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="22133-149">Toiming SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="22133-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="22133-150">Veenduge, et atribuutide **InvoiceCountryRegionId** ja **BillingAddress\_Country** vahel oleks olemas nõutav vastendus.</span><span class="sxs-lookup"><span data-stu-id="22133-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="22133-151">Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni.</span><span class="sxs-lookup"><span data-stu-id="22133-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="22133-152">Hinnakiri on vajalik arvete koostamiseks rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="22133-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="22133-153">Värskendage üksuse **pricelevelid.name \[Hinnakirja nimi\]** väärtuskaarti hinnakirja alusel, mida kasutatakse rakenduses Sales valuuta kohta.</span><span class="sxs-lookup"><span data-stu-id="22133-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="22133-154">Saate ühe valuuta puhul kasutada vaikehinnakirja.</span><span class="sxs-lookup"><span data-stu-id="22133-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="22133-155">Kui teil on mitmes valuutas hinnakirju, saate kasutada väärtuskaarti.</span><span class="sxs-lookup"><span data-stu-id="22133-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="22133-156">Atribuudi **pricelevelid.name \[Hinnakirja nimi\]** malli väärtus on valuutal põhinev väärtuskaart, kus USA dollar = USA CRM-i teenus (näide).</span><span class="sxs-lookup"><span data-stu-id="22133-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="22133-157">Toiming SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="22133-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="22133-158">Veenduge, et atribuudi **Mõõtühik** jaoks oleks olemas nõutav vastendus.</span><span class="sxs-lookup"><span data-stu-id="22133-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="22133-159">Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Supply Chain Management olemas.</span><span class="sxs-lookup"><span data-stu-id="22133-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="22133-160">Üksuste **SalesUnitSymbol** ja **Quantity\_UOM** jaoks on määratletud väärtuskaardiga malli väärtus.</span><span class="sxs-lookup"><span data-stu-id="22133-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="22133-161">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="22133-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="22133-162">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="22133-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="22133-163">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="22133-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="22133-164">Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="22133-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="22133-165">Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="22133-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="22133-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="22133-166">SalesInvoiceHeader</span></span>

![Malli vastendamine andmete integratsioonis](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="22133-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="22133-168">SalesInvoiceLine</span></span>

![Malli vastendamine andmete integratsioonis](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="22133-170">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="22133-170">Related topics</span></span>

[<span data-ttu-id="22133-171">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="22133-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="22133-172">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="22133-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="22133-173">Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="22133-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="22133-174">Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="22133-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="22133-175">Rakenduse Supply Chain Management müügitellimuse päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="22133-175">Synchronize sales order headers and lines directly from Supply Chain Management to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)
