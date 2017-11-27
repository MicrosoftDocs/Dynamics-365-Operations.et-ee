---
title: "Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuse päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="9dd4b-103">Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="9dd4b-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9dd4b-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuse päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="9dd4b-105">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="9dd4b-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="9dd4b-106">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="9dd4b-107">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="9dd4b-108">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="9dd4b-109">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="9dd4b-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9dd4b-110">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="9dd4b-110">Templates and tasks</span></span>

<span data-ttu-id="9dd4b-111">Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="9dd4b-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="9dd4b-112">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9dd4b-113">Müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="9dd4b-114">**Andmete integratsioon malli nimi:** Müügitellimused (rakendusest Fin and Ops rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="9dd4b-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="9dd4b-115">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="9dd4b-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="9dd4b-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="9dd4b-116">OrderHeader</span></span>
    - <span data-ttu-id="9dd4b-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="9dd4b-117">OrderLine</span></span>

<span data-ttu-id="9dd4b-118">Enne müügiarvete päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="9dd4b-119">Tooted (rakendusest Sales rakendusse Fin and Ops) – otse</span><span class="sxs-lookup"><span data-stu-id="9dd4b-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="9dd4b-120">Kontod (rakendusest Sales rakendusse Fin and Ops) – otse (kui on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="9dd4b-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="9dd4b-121">Kontaktid klientideks (rakendusest Sales rakendusse Fin and Ops) – otse (kui see on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="9dd4b-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="9dd4b-122">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="9dd4b-122">Entity set</span></span>

| <span data-ttu-id="9dd4b-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9dd4b-123">Finance and Operations</span></span>  | <span data-ttu-id="9dd4b-124">Müük</span><span class="sxs-lookup"><span data-stu-id="9dd4b-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="9dd4b-125">CDS-i müügitellimuste päised CDS</span><span class="sxs-lookup"><span data-stu-id="9dd4b-125">CDS sales order headers</span></span> | <span data-ttu-id="9dd4b-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="9dd4b-126">SalesOrders</span></span>       |
| <span data-ttu-id="9dd4b-127">CDS-i müügitellimuse read</span><span class="sxs-lookup"><span data-stu-id="9dd4b-127">CDS sales order lines</span></span>   | <span data-ttu-id="9dd4b-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="9dd4b-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="9dd4b-129">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="9dd4b-129">Entity flow</span></span>

<span data-ttu-id="9dd4b-130">Müügitellimused luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="9dd4b-131">Malli filtrid tagavad ainult asjakohaste müügitellimuste kaasamise sünkroonimisse.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="9dd4b-132">Müügitellimuse puhul peavad nii müügitellimuse esitanud klient kui ka arvelduse klient pärinema rakendusest Sales, et nad lisataks sünkroonimisse.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="9dd4b-133">Rakenduses Finance and Operations kasutatakse välju **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** andmeüksustes sünkroonimise jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="9dd4b-134">Rakenduses Finance and Operations olev müügitellimus tuleb kinnitada.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="9dd4b-135">Rakendusega Sales sünkroonitakse ainult kõrgema töötlemisolekuga kinnitatud müügitellimused, nt olekuga **Saadetud** või **Arveldatud**.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="9dd4b-136">Pärast müügitellimuse loomist või muutmist tuleb käitada pakett-töö **Müügi kogusummade arvutamine** rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="9dd4b-137">Rakendusega Sales sünkroonitakse vaid need müügitellimused, mille müügi kogusummad on arvutatud.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="9dd4b-138">Müügitellimuse päises olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="9dd4b-139">Sales ei toeta maksuteavet päise tasandil.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="9dd4b-140">Sünkroonimine hõlmab aga makse, mis on seotud rea tasemel tasudega.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9dd4b-141">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="9dd4b-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9dd4b-142">Üksusele **Tellimus** lisati uued väljad ja need kuvatakse järgmisel lehel.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="9dd4b-143">**Hallatakse väliselt**: seadke see valik väärtusele **Jah**, kui tellimus tuleb rakendusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="9dd4b-144">**Töötlemise olek**: sellel väljal kuvatakse tellimuse töötlemise olek rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="9dd4b-145">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="9dd4b-145">The following values are available:</span></span>

    - <span data-ttu-id="9dd4b-146">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="9dd4b-146">Active</span></span>
    - <span data-ttu-id="9dd4b-147">Kinnitatud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-147">Confirmed</span></span>
    - <span data-ttu-id="9dd4b-148">Saateleht</span><span class="sxs-lookup"><span data-stu-id="9dd4b-148">Packing Slip</span></span>
    - <span data-ttu-id="9dd4b-149">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-149">Invoiced</span></span>
    - <span data-ttu-id="9dd4b-150">Komplekteeritud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-150">Picked</span></span>
    - <span data-ttu-id="9dd4b-151">Osaliselt komplekteeritud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-151">Partially Picked</span></span>
    - <span data-ttu-id="9dd4b-152">Osaliselt pakitud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-152">Partially Packed</span></span>
    - <span data-ttu-id="9dd4b-153">Välja saadetud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-153">Shipped</span></span>
    - <span data-ttu-id="9dd4b-154">Osaliselt tarnitud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-154">Partially Shipped</span></span>
    - <span data-ttu-id="9dd4b-155">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-155">Partially Invoiced</span></span>
    - <span data-ttu-id="9dd4b-156">Tühistatud</span><span class="sxs-lookup"><span data-stu-id="9dd4b-156">Cancelled</span></span>

<span data-ttu-id="9dd4b-157">Sätet **Sisaldab ainult väliselt hallatavaid tooteid** kasutatakse teistes müügitellimuse stsenaariumides (näiteks rakendusest Sales rakendusse Finance and Operations sünkroonimisel), et jälgida, kas müügitellimus koosneb täielikult väliselt hallatavatest toodetest.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="9dd4b-158">Kui müügitellimus sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="9dd4b-159">See säte aitab tagada, et te ei püüaks sünkroonida müügitellimuse ridu, mis hõlmavad rakenduse Finance and Operations jaoks tundmatuid tooteid.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="9dd4b-160">Nupud **Arve koostamine**, **Tellimuse tühistamine**, **Ümberarvutamine**, **Toodete toomine** ja **Aadressi otsimine** lehel **Müügitellimus** on väliselt hallatavate tellimuste puhul peidetud, kuna arved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="9dd4b-161">Tellimuse lehte ei saa muuta, kuna müügitellimuse teave sünkroonitakse rakendusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="9dd4b-162">Müügitellimuse olek on ka edaspidi **Aktiivne**, et rakendusest Finance and Operations pärit muudatused saaksid liikuda rakenduses Sales olevasse müügitellimusse.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="9dd4b-163">Määrake selle käitumise juhtimiseks andmeintegratsiooni projektis vaikeväärtuse **Olekukood \[[Olek]\]** väärtuseks **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9dd4b-164">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="9dd4b-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="9dd4b-165">Enne müügitellimuste sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="9dd4b-166">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="9dd4b-166">Setup in Sales</span></span>

- <span data-ttu-id="9dd4b-167">Veenduge, et load oleks seadistatud töörühma jaoks, kuhu rakenduses Sales häälestatud ühendusest pärit kasutaja on määratud.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="9dd4b-168">Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="9dd4b-169">Kui töörühmal ei ole administraatorijuurdepääsu, ilmub andmete integratsioonis projekti käivitamisel veateade, mis annab teada, et peamine töörühm puudub.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="9dd4b-170">Valige jaotisest **Sätted** > **Turve** > **Töörühmad** asjakohane töörühm, valige käsk **Halda rolle** ja valige soovitud lubadega roll, näiteks **Süsteemiadministraator**.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="9dd4b-171">Avage jaotis **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales** ja veenduge, et kasutusel oleks järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="9dd4b-172">Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="9dd4b-173">Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="9dd4b-174">Seadistus rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9dd4b-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="9dd4b-175">Avage jaotis **Müük ja turundus** > **Perioodilised ülesanded** > **Müügi kogusummade arvutamine** ja seadistage töö pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="9dd4b-176">Valige suvandi **Müügitellimuste kogusummade arvutamine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="9dd4b-177">See toiming on oluline, kuna Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="9dd4b-178">Pakett-töö sagedus tuleks sobitada müügitellimuse sünkroonimise sagedusega.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="9dd4b-179">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="9dd4b-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="9dd4b-180">Ülesanne SalesHeader</span><span class="sxs-lookup"><span data-stu-id="9dd4b-180">SalesHeader task</span></span>

- <span data-ttu-id="9dd4b-181">Veenduge, et üksuste **InvoiceCountryRegionID** ja **BillingAddress\_Country** ning **DeliveryCountryRegionID** ja **DeliveryAddress\_Country** vahel oleks olemas vajalik vastendus.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="9dd4b-182">Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="9dd4b-183">Hinnakiri on vajalik tellimuste koostamiseks rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="9dd4b-184">Värskendage üksuse **pricelevelid.name \[Hinnakirja nimi\]** väärtuskaarti hinnakirja alusel, mida kasutatakse rakenduses Sales valuuta kohta.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="9dd4b-185">Saate ühe valuuta puhul kasutada vaikehinnakirja.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="9dd4b-186">Kui teil on mitmes valuutas hinnakirju, saate kasutada väärtuskaarti.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="9dd4b-187">Üksuse **pricelevelid.name \[Hinnakirja nimi\]** malli vaikeväärtus on **USA CRM-i teenus (näidis)**.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="9dd4b-188">Ülesanne SalesLine</span><span class="sxs-lookup"><span data-stu-id="9dd4b-188">SalesLine task</span></span>

- <span data-ttu-id="9dd4b-189">Veenduge, et üksuste **DeliveryCountryRegionId** ja **DeliveryAddress\_Country** vahel oleks olemas nõutav vastendamine.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="9dd4b-190">Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="9dd4b-191">Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Finance and Operations olemas.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="9dd4b-192">Üksuste **SalesUnitSymbol** ja **Quantity\_UOM** jaoks on määratletud väärtuskaardiga malli väärtus.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9dd4b-193">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="9dd4b-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="9dd4b-194">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="9dd4b-195">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="9dd4b-196">Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="9dd4b-197">Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd4b-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="9dd4b-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="9dd4b-198">OrderHeader</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="9dd4b-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="9dd4b-200">OrderLine</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="9dd4b-202">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="9dd4b-202">Related topics</span></span>

[<span data-ttu-id="9dd4b-203">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="9dd4b-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="9dd4b-204">Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="9dd4b-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="9dd4b-205">Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="9dd4b-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="9dd4b-206">Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="9dd4b-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="9dd4b-207">Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="9dd4b-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




