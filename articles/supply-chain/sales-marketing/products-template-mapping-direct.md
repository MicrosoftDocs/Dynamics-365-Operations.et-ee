---
title: Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management otse rakendusse Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6ffd55585ff43f993876de6c669eb61e74a9fd79
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527310"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="1095f-103">Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="1095f-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="1095f-104">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="1095f-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="1095f-105">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management otse rakendusse Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="1095f-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="1095f-106">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="1095f-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="1095f-107">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="1095f-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="1095f-108">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales.</span><span class="sxs-lookup"><span data-stu-id="1095f-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="1095f-109">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="1095f-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="1095f-110">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="1095f-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1095f-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="1095f-111">Templates and tasks</span></span>

<span data-ttu-id="1095f-112">Saadaolevatele mallidele juurdepääsemiseks avage [Power Apps administreerimiskeskus](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="1095f-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="1095f-113">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="1095f-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1095f-114">Toodete sünkroonimiseks rakendusest Supply Chain Management rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="1095f-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="1095f-115">**Andmete integratsioon malli nimi:** Tooted (rakendusest Fin and Ops rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="1095f-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="1095f-116">**Ülesande nimi andmete integratsiooni projektis:** Tooted</span><span class="sxs-lookup"><span data-stu-id="1095f-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="1095f-117">Enne toodete sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.</span><span class="sxs-lookup"><span data-stu-id="1095f-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="1095f-118">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="1095f-118">Entity set</span></span>

| <span data-ttu-id="1095f-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1095f-119">Supply Chain Management</span></span>    | <span data-ttu-id="1095f-120">Müük</span><span class="sxs-lookup"><span data-stu-id="1095f-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="1095f-121">Müüdavad väljastatud tooted</span><span class="sxs-lookup"><span data-stu-id="1095f-121">Sellable released products</span></span> | <span data-ttu-id="1095f-122">Tooted</span><span class="sxs-lookup"><span data-stu-id="1095f-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="1095f-123">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="1095f-123">Entity flow</span></span>

<span data-ttu-id="1095f-124">Tooteid hallatakse rakenduses Supply Chain Management ja need sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="1095f-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="1095f-125">Andmeüksus **Müüdavad väljastatud tooted** rakenduses Supply Chain Management ekspordib ainult tooted, mille olek on *Müüdav*.</span><span class="sxs-lookup"><span data-stu-id="1095f-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="1095f-126">Müüdavad tooted hõlmavad müügitellimuses kasutamiseks vajalikku teavet.</span><span class="sxs-lookup"><span data-stu-id="1095f-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="1095f-127">Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud toode**.</span><span class="sxs-lookup"><span data-stu-id="1095f-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="1095f-128">Tootenumbrit kasutatakse võtmena.</span><span class="sxs-lookup"><span data-stu-id="1095f-128">The product number is used as a key.</span></span> <span data-ttu-id="1095f-129">Kui tootevariandid sünkroonitakse rakendusega Sales, on igal tootevariandil seega individuaalne toote ID.</span><span class="sxs-lookup"><span data-stu-id="1095f-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1095f-130">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="1095f-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="1095f-131">Rakenduses Sales lisatakse toodetele uus väli **On väliselt hallatav**, mis näitab, et kõnealust toodet hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="1095f-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="1095f-132">Vaikimisi seatakse rakendusse Sales importimise ajal selle väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1095f-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="1095f-133">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="1095f-133">The following values are available:</span></span>

- <span data-ttu-id="1095f-134">**Jah**: toode pärineb rakendusest Supply Chain Management ja seda ei saa rakenduses Sales muuta.</span><span class="sxs-lookup"><span data-stu-id="1095f-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="1095f-135">**Ei**: toode sisestati otse rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="1095f-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="1095f-136">**(Tühi)**: toode oli rakenduses Sales olemas enne lahenduse Potentsiaalne klient sularahaks lubamist.</span><span class="sxs-lookup"><span data-stu-id="1095f-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="1095f-137">Väli **On väliselt hallatav** aitab tagada, et ainult väliselt hallatavate toodetega pakkumised ja müügitellimused sünkroonitakse rakendusega upply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1095f-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="1095f-138">Väliselt hallatavad tooted lisatakse automaatselt esimesse kehtivasse hinnakirja, millel on sama valuuta.</span><span class="sxs-lookup"><span data-stu-id="1095f-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="1095f-139">Hinnakirjad on korraldatud tähestikulises järjekorras nime alusel.</span><span class="sxs-lookup"><span data-stu-id="1095f-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="1095f-140">Toote müügihinda rakendusest Supply Chain Management kasutatakse hinnakirja hinnana.</span><span class="sxs-lookup"><span data-stu-id="1095f-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="1095f-141">Seega peab rakenduses Sales olema hinnakiri iga toote müügivaluuta kohta rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1095f-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="1095f-142">Vabastatud müüdavate toodete valuutaks on määratud selle juriidilise isiku arvestusvaluuta, millest toode eksporditakse.</span><span class="sxs-lookup"><span data-stu-id="1095f-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="1095f-143">Toote sünkroonimine ei õnnestu, kui vastava valuutaga hinnakiri puudub.</span><span class="sxs-lookup"><span data-stu-id="1095f-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="1095f-144">Saate kontrollida integratsioonis kasutatud hinnakirja, vastendades andmeintegratsiooni projektis atribuudi pricelevelid.name [Vaikehinnakiri (nimi)].</span><span class="sxs-lookup"><span data-stu-id="1095f-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="1095f-145">Sisend peab olema väiketähtedes.</span><span class="sxs-lookup"><span data-stu-id="1095f-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="1095f-146">Näiteks oleksid rakenduses Sales hinnakirja „Standard” vaikeväärtused järgmised: Sihtväli: pricelevelid.name [Vaikehinnakiri (nimi)] ja vastenduse tüüp: [ { "transformType": "Vaikimisi", "defaultValue": "Standard" } ].</span><span class="sxs-lookup"><span data-stu-id="1095f-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1095f-147">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="1095f-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="1095f-148">Enne kui saate esimese sünkroonimise käivitada, peate olemasolevate toodete puhul rakenduses Supply Chain Management täitma tabeli Eristatav toode.</span><span class="sxs-lookup"><span data-stu-id="1095f-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="1095f-149">Olemasolevaid tooteid ei sünkroonita, enne kui see töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="1095f-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="1095f-150">Kasutage rakenduses Supply Chain Management otsingufunktsiooni, et otsida suvandit **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="1095f-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="1095f-151">Valige töö käivitamiseks nupp **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="1095f-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="1095f-152">Seda tööd tohib käitada ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="1095f-152">This job must be run only one time.</span></span>

- <span data-ttu-id="1095f-153">Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduse Supply Chain Management ja rakenduse Sales vahel oleks üksuste **SalesUnitSymbol** ja **DefaultUnit (nimi)** vastenduses olemas.</span><span class="sxs-lookup"><span data-stu-id="1095f-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="1095f-154">Värskendage suvandi **Ühikugrupp** väärtuskaarti (**defaultuomscheduleid.name**), nii et see kattuks rakenduse Sales suvandiga **Ühikugrupid**.</span><span class="sxs-lookup"><span data-stu-id="1095f-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="1095f-155">Malli vaikeväärtus on **Vaikeühik**.</span><span class="sxs-lookup"><span data-stu-id="1095f-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="1095f-156">Veenduge, et kõigi toodete müügi mõõtühikud rakendusest Supply Chain Management oleksid rakenduses Sales olemas.</span><span class="sxs-lookup"><span data-stu-id="1095f-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="1095f-157">Veenduge, et hinnakirjad oleksid rakenduses Sales olemas iga toote müügivaluuta kohta rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1095f-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="1095f-158">Rakenduses Sales tooteid luues võib nende olek olla **Mustand** või **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="1095f-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="1095f-159">Käitumist saab juhtida rakenduse Sales jaotises **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales**.</span><span class="sxs-lookup"><span data-stu-id="1095f-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="1095f-160">Olekuga **Mustand** loodud tooted tuleb esmalt aktiveerida, enne kui neid saab pakkumistesse või müügitellimustesse lisada.</span><span class="sxs-lookup"><span data-stu-id="1095f-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1095f-161">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="1095f-161">Template mapping in Data integration</span></span>

<span data-ttu-id="1095f-162">Järgmistel joonistel on toodud näide malli vastendusest andmete integreerimises.</span><span class="sxs-lookup"><span data-stu-id="1095f-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="1095f-163">Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1095f-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Malli vastendamine andmeintegraatoris](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="1095f-165">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="1095f-165">Related topics</span></span>

[<span data-ttu-id="1095f-166">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="1095f-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="1095f-167">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="1095f-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="1095f-168">Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="1095f-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="1095f-169">Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel</span><span class="sxs-lookup"><span data-stu-id="1095f-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="1095f-170">Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="1095f-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



