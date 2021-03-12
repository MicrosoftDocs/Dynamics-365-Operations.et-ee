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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ecee843b6c09c86b4e40ab34cc113e5a7e7c76f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977684"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="63cfa-103">Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="63cfa-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="63cfa-104">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="63cfa-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="63cfa-105">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management otse rakendusse Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="63cfa-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="63cfa-106">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="63cfa-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="63cfa-107">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="63cfa-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="63cfa-108">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales.</span><span class="sxs-lookup"><span data-stu-id="63cfa-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="63cfa-109">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="63cfa-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="63cfa-110">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="63cfa-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="63cfa-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="63cfa-111">Templates and tasks</span></span>

<span data-ttu-id="63cfa-112">Saadaolevatele mallidele juurdepääsemiseks avage [Power Apps administreerimiskeskus](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="63cfa-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="63cfa-113">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="63cfa-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="63cfa-114">Toodete sünkroonimiseks rakendusest Supply Chain Management rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="63cfa-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="63cfa-115">**Andmete integratsioon malli nimi:** Tooted (rakendusest Fin and Ops rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="63cfa-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="63cfa-116">**Ülesande nimi andmete integratsiooni projektis:** Tooted</span><span class="sxs-lookup"><span data-stu-id="63cfa-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="63cfa-117">Enne toodete sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.</span><span class="sxs-lookup"><span data-stu-id="63cfa-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="63cfa-118">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="63cfa-118">Entity set</span></span>

| <span data-ttu-id="63cfa-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="63cfa-119">Supply Chain Management</span></span>    | <span data-ttu-id="63cfa-120">Müük</span><span class="sxs-lookup"><span data-stu-id="63cfa-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="63cfa-121">Müüdavad väljastatud tooted</span><span class="sxs-lookup"><span data-stu-id="63cfa-121">Sellable released products</span></span> | <span data-ttu-id="63cfa-122">Tooted</span><span class="sxs-lookup"><span data-stu-id="63cfa-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="63cfa-123">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="63cfa-123">Entity flow</span></span>

<span data-ttu-id="63cfa-124">Tooteid hallatakse rakenduses Supply Chain Management ja need sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="63cfa-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="63cfa-125">Andmeüksus **Müüdavad väljastatud tooted** rakenduses Supply Chain Management ekspordib ainult tooted, mille olek on *Müüdav*.</span><span class="sxs-lookup"><span data-stu-id="63cfa-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="63cfa-126">Müüdavad tooted hõlmavad müügitellimuses kasutamiseks vajalikku teavet.</span><span class="sxs-lookup"><span data-stu-id="63cfa-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="63cfa-127">Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud toode**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="63cfa-128">Tootenumbrit kasutatakse võtmena.</span><span class="sxs-lookup"><span data-stu-id="63cfa-128">The product number is used as a key.</span></span> <span data-ttu-id="63cfa-129">Kui tootevariandid sünkroonitakse rakendusega Sales, on igal tootevariandil seega individuaalne toote ID.</span><span class="sxs-lookup"><span data-stu-id="63cfa-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="63cfa-130">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="63cfa-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="63cfa-131">Rakenduses Sales lisatakse toodetele uus väli **On väliselt hallatav**, mis näitab, et kõnealust toodet hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="63cfa-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="63cfa-132">Vaikimisi seatakse rakendusse Sales importimise ajal selle väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="63cfa-133">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="63cfa-133">The following values are available:</span></span>

- <span data-ttu-id="63cfa-134">**Jah**: toode pärineb rakendusest Supply Chain Management ja seda ei saa rakenduses Sales muuta.</span><span class="sxs-lookup"><span data-stu-id="63cfa-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="63cfa-135">**Ei**: toode sisestati otse rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="63cfa-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="63cfa-136">**(Tühi)**: toode oli rakenduses Sales olemas enne lahenduse Potentsiaalne klient sularahaks lubamist.</span><span class="sxs-lookup"><span data-stu-id="63cfa-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="63cfa-137">Väli **On väliselt hallatav** aitab tagada, et ainult väliselt hallatavate toodetega pakkumised ja müügitellimused sünkroonitakse rakendusega upply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63cfa-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="63cfa-138">Väliselt hallatavad tooted lisatakse automaatselt esimesse kehtivasse hinnakirja, millel on sama valuuta.</span><span class="sxs-lookup"><span data-stu-id="63cfa-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="63cfa-139">Hinnakirjad on korraldatud tähestikulises järjekorras nime alusel.</span><span class="sxs-lookup"><span data-stu-id="63cfa-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="63cfa-140">Toote müügihinda rakendusest Supply Chain Management kasutatakse hinnakirja hinnana.</span><span class="sxs-lookup"><span data-stu-id="63cfa-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="63cfa-141">Seega peab rakenduses Sales olema hinnakiri iga toote müügivaluuta kohta rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63cfa-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="63cfa-142">Vabastatud müüdavate toodete valuutaks on määratud selle juriidilise isiku arvestusvaluuta, millest toode eksporditakse.</span><span class="sxs-lookup"><span data-stu-id="63cfa-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="63cfa-143">Toote sünkroonimine ei õnnestu, kui vastava valuutaga hinnakiri puudub.</span><span class="sxs-lookup"><span data-stu-id="63cfa-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="63cfa-144">Saate kontrollida integratsioonis kasutatud hinnakirja, vastendades andmeintegratsiooni projektis atribuudi pricelevelid.name [Vaikehinnakiri (nimi)].</span><span class="sxs-lookup"><span data-stu-id="63cfa-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="63cfa-145">Sisend peab olema väiketähtedes.</span><span class="sxs-lookup"><span data-stu-id="63cfa-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="63cfa-146">Näiteks oleksid rakenduses Sales hinnakirja „Standard” vaikeväärtused järgmised: sihtväli: pricelevelid.name [Vaikehinnakiri (nimi)] ja vastenduse tüüp: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="63cfa-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="63cfa-147">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="63cfa-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="63cfa-148">Enne kui saate esimese sünkroonimise käivitada, peate olemasolevate toodete puhul rakenduses Supply Chain Management täitma tabeli Eristatav toode.</span><span class="sxs-lookup"><span data-stu-id="63cfa-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="63cfa-149">Olemasolevaid tooteid ei sünkroonita, enne kui see töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="63cfa-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="63cfa-150">Kasutage rakenduses Supply Chain Management otsingufunktsiooni, et otsida suvandit **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="63cfa-151">Valige töö käivitamiseks nupp **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="63cfa-152">Seda tööd tohib käitada ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="63cfa-152">This job must be run only one time.</span></span>

- <span data-ttu-id="63cfa-153">Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduse Supply Chain Management ja rakenduse Sales vahel oleks üksuste **SalesUnitSymbol** ja **DefaultUnit (nimi)** vastenduses olemas.</span><span class="sxs-lookup"><span data-stu-id="63cfa-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="63cfa-154">Värskendage suvandi **Ühikugrupp** väärtuskaarti (**defaultuomscheduleid.name**), nii et see kattuks rakenduse Sales suvandiga **Ühikugrupid**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="63cfa-155">Malli vaikeväärtus on **Vaikeühik**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="63cfa-156">Veenduge, et kõigi toodete müügi mõõtühikud rakendusest Supply Chain Management oleksid rakenduses Sales olemas.</span><span class="sxs-lookup"><span data-stu-id="63cfa-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="63cfa-157">Veenduge, et hinnakirjad oleksid rakenduses Sales olemas iga toote müügivaluuta kohta rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63cfa-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="63cfa-158">Rakenduses Sales tooteid luues võib nende olek olla **Mustand** või **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="63cfa-159">Käitumist saab juhtida rakenduse Sales jaotises **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales**.</span><span class="sxs-lookup"><span data-stu-id="63cfa-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="63cfa-160">Olekuga **Mustand** loodud tooted tuleb esmalt aktiveerida, enne kui neid saab pakkumistesse või müügitellimustesse lisada.</span><span class="sxs-lookup"><span data-stu-id="63cfa-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="63cfa-161">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="63cfa-161">Template mapping in Data integration</span></span>

<span data-ttu-id="63cfa-162">Järgmistel joonistel on toodud näide malli vastendusest andmete integreerimises.</span><span class="sxs-lookup"><span data-stu-id="63cfa-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="63cfa-163">Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63cfa-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Malli vastendamine andmeintegraatoris](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="63cfa-165">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="63cfa-165">Related topics</span></span>

[<span data-ttu-id="63cfa-166">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="63cfa-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="63cfa-167">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="63cfa-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="63cfa-168">Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="63cfa-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="63cfa-169">Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel</span><span class="sxs-lookup"><span data-stu-id="63cfa-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="63cfa-170">Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="63cfa-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



