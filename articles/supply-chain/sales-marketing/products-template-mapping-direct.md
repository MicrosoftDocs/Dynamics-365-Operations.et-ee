---
title: "Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: def88c291538e3ef278c51e4b87462782e222de2
ms.contentlocale: et-ee
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="7b4da-103">Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="7b4da-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7b4da-104">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="7b4da-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="7b4da-105">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="7b4da-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="7b4da-106">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="7b4da-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="7b4da-107">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="7b4da-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="7b4da-108">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales.</span><span class="sxs-lookup"><span data-stu-id="7b4da-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="7b4da-109">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="7b4da-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="7b4da-110">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="7b4da-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7b4da-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="7b4da-111">Templates and tasks</span></span>

<span data-ttu-id="7b4da-112">Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="7b4da-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="7b4da-113">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="7b4da-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7b4da-114">Toodete sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="7b4da-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="7b4da-115">**Andmete integratsioon malli nimi:** Tooted (rakendusest Fin and Ops rakendusse Sales) – otse</span><span class="sxs-lookup"><span data-stu-id="7b4da-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="7b4da-116">**Ülesande nimi andmete integratsiooni projektis:** Tooted</span><span class="sxs-lookup"><span data-stu-id="7b4da-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="7b4da-117">Enne toodete sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.</span><span class="sxs-lookup"><span data-stu-id="7b4da-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="7b4da-118">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="7b4da-118">Entity set</span></span>

| <span data-ttu-id="7b4da-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b4da-119">Finance and Operations</span></span>     | <span data-ttu-id="7b4da-120">Müük</span><span class="sxs-lookup"><span data-stu-id="7b4da-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="7b4da-121">Müüdavad väljastatud tooted</span><span class="sxs-lookup"><span data-stu-id="7b4da-121">Sellable released products</span></span> | <span data-ttu-id="7b4da-122">Tooted</span><span class="sxs-lookup"><span data-stu-id="7b4da-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="7b4da-123">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="7b4da-123">Entity flow</span></span>

<span data-ttu-id="7b4da-124">Tooteid hallatakse rakenduses Finance and Operations ja need sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="7b4da-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="7b4da-125">Andmeüksus **Müüdavad väljastatud tooted** rakenduses Finaces and Operations ekspordib ainult tooted, mille olek on *Müüdav*.</span><span class="sxs-lookup"><span data-stu-id="7b4da-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="7b4da-126">Müüdavad tooted hõlmavad müügitellimuses kasutamiseks vajalikku teavet.</span><span class="sxs-lookup"><span data-stu-id="7b4da-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="7b4da-127">Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud toode**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="7b4da-128">Tootenumbrit kasutatakse võtmena.</span><span class="sxs-lookup"><span data-stu-id="7b4da-128">The product number is used as a key.</span></span> <span data-ttu-id="7b4da-129">Kui tootevariandid sünkroonitakse rakendusega Sales, on igal tootevariandil seega individuaalne toote ID.</span><span class="sxs-lookup"><span data-stu-id="7b4da-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="7b4da-130">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="7b4da-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="7b4da-131">Rakenduses Sales lisatakse toodetele uus väli **On väliselt hallatav**, mis näitab, et kõnealust toodet hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="7b4da-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="7b4da-132">Vaikimisi seatakse rakendusse Sales importimise ajal selle väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="7b4da-133">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="7b4da-133">The following values are available:</span></span>

- <span data-ttu-id="7b4da-134">**Jah**: toode pärineb rakendusest Finance and Operations ja seda ei saa rakenduses Sales muuta.</span><span class="sxs-lookup"><span data-stu-id="7b4da-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="7b4da-135">**Ei**: toode sisestati otse rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="7b4da-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="7b4da-136">**(Tühi)**: toode oli rakenduses Sales olemas enne lahenduse Potentsiaalne klient sularahaks lubamist.</span><span class="sxs-lookup"><span data-stu-id="7b4da-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="7b4da-137">Väli **On väliselt hallatav** aitab tagada, et ainult väliselt hallatavate toodetega pakkumised ja müügitellimused sünkroonitakse rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7b4da-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="7b4da-138">Väliselt hallatavad tooted lisatakse automaatselt esimesse kehtivasse hinnakirja, millel on sama valuuta.</span><span class="sxs-lookup"><span data-stu-id="7b4da-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="7b4da-139">Hinnakirjad on korraldatud tähestikulises järjekorras nime alusel.</span><span class="sxs-lookup"><span data-stu-id="7b4da-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="7b4da-140">Toote müügihinda rakendusest Finance and Operations kasutatakse hinnakirja hinnana.</span><span class="sxs-lookup"><span data-stu-id="7b4da-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="7b4da-141">Seega peab rakenduses Sales olema hinnakiri iga toote müügivaluuta kohta rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7b4da-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="7b4da-142">Vabastatud müüdavate toodete valuutaks on määratud selle juriidilise isiku arvestusvaluuta, millest toode eksporditakse.</span><span class="sxs-lookup"><span data-stu-id="7b4da-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="7b4da-143">Toote sünkroonimine ei õnnestu, kui vastava valuutaga hinnakiri puudub.</span><span class="sxs-lookup"><span data-stu-id="7b4da-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="7b4da-144">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="7b4da-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="7b4da-145">Enne kui saate esimese sünkroonimise käivitada, peate olemasolevate toodete puhul rakenduses Finance and Operations täitma tabeli Eristatav toode.</span><span class="sxs-lookup"><span data-stu-id="7b4da-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="7b4da-146">Olemasolevaid tooteid ei sünkroonita, enne kui see töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="7b4da-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="7b4da-147">Kasutage rakenduses Finance and Operations otsingufunktsiooni, et otsida suvandit **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="7b4da-148">Valige töö käivitamiseks nupp **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="7b4da-149">Seda tööd tohib käitada ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="7b4da-149">This job must be run only one time.</span></span>

- <span data-ttu-id="7b4da-150">Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduse Finance and Operations ja rakenduse Sales vahel oleks üksuste **SalesUnitSymbol** ja **DefaultUnit (nimi)** vastenduses olemas.</span><span class="sxs-lookup"><span data-stu-id="7b4da-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="7b4da-151">Värskendage suvandi **Ühikugrupp** väärtuskaarti (**defaultuomscheduleid.name**), nii et see kattuks rakenduse Sales suvandiga **Ühikugrupid**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="7b4da-152">Malli vaikeväärtus on **Vaikeühik**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="7b4da-153">Veenduge, et kõigi toodete müügi mõõtühikud rakendusest Finance and Operations oleksid rakenduses Sales olemas.</span><span class="sxs-lookup"><span data-stu-id="7b4da-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="7b4da-154">Veenduge, et hinnakirjad oleksid rakenduses Sales olemas iga toote müügivaluuta kohta rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7b4da-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="7b4da-155">Rakenduses Sales tooteid luues võib nende olek olla **Mustand** või **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="7b4da-156">Käitumist saab juhtida rakenduse Sales jaotises **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales**.</span><span class="sxs-lookup"><span data-stu-id="7b4da-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="7b4da-157">Olekuga **Mustand** loodud tooted tuleb esmalt aktiveerida, enne kui neid saab pakkumistesse või müügitellimustesse lisada.</span><span class="sxs-lookup"><span data-stu-id="7b4da-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b4da-158">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="7b4da-158">Template mapping in Data integration</span></span>

<span data-ttu-id="7b4da-159">Järgmistel joonistel on toodud näide malli vastendusest andmete integreerimises.</span><span class="sxs-lookup"><span data-stu-id="7b4da-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="7b4da-160">Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7b4da-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Malli vastendamine andmeintegraatoris](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="7b4da-162">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="7b4da-162">Related topics</span></span>

[<span data-ttu-id="7b4da-163">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="7b4da-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="7b4da-164">Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="7b4da-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="7b4da-165">Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="7b4da-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="7b4da-166">Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="7b4da-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="7b4da-167">Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="7b4da-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




