---
title: "Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="b85f8-103">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="b85f8-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b85f8-104">Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="b85f8-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="b85f8-105">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="b85f8-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="b85f8-106">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="b85f8-106">Template and task</span></span>

<span data-ttu-id="b85f8-107">Toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) rakendusse Microsoft Dynamics 365 for Sales (Sales) kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="b85f8-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="b85f8-108">Malli nimi: Tooted (Fin and Opsist Salesi)</span><span class="sxs-lookup"><span data-stu-id="b85f8-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="b85f8-109">Ülesande nimi projektis: Tooted</span><span class="sxs-lookup"><span data-stu-id="b85f8-109">Name of task in project: Products</span></span>

<span data-ttu-id="b85f8-110">Nõutavad sünkroonimisülesanded enne toote sünkroonimist: pole</span><span class="sxs-lookup"><span data-stu-id="b85f8-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="b85f8-111">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="b85f8-111">Entity set</span></span>

| <span data-ttu-id="b85f8-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="b85f8-112">**Finance and Operations**</span></span> | <span data-ttu-id="b85f8-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="b85f8-113">**CDS**</span></span> | <span data-ttu-id="b85f8-114">**Müük**</span><span class="sxs-lookup"><span data-stu-id="b85f8-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="b85f8-115">Müüdavad väljastatud tooted</span><span class="sxs-lookup"><span data-stu-id="b85f8-115">Sellable released products</span></span> | <span data-ttu-id="b85f8-116">Toode</span><span class="sxs-lookup"><span data-stu-id="b85f8-116">Product</span></span> | <span data-ttu-id="b85f8-117">Tooted</span><span class="sxs-lookup"><span data-stu-id="b85f8-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="b85f8-118">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="b85f8-118">Entity flow</span></span>

<span data-ttu-id="b85f8-119">Tooteid hallatakse rakenduses Finance and Operations ja need sünkroonitakse rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="b85f8-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="b85f8-120">Andmeüksus **Müüdavad vabastatud tooted** rakenduses Finance and Operations ekspordib ainult müüdavaid tooteid, mis tähendab, et toodetel on teave, mis on nõutav müügitellimusel kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b85f8-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="b85f8-121">Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud toode**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="b85f8-122">Atribuuti **Toote number** kasutatakse võtmena, mis tähendab, et tootevariandid sünkroonitakse CDS-i ja Salesiga eraldi **toote ID-dega** iga **tootevariandi** kohta.</span><span class="sxs-lookup"><span data-stu-id="b85f8-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b85f8-123">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="b85f8-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b85f8-124">Rakenduses Sales lisatakse toodetele uus väli **On väliselt hallatav**, mis näitab, et kõnealust toodet hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="b85f8-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="b85f8-125">Vaikimisi seatakse rakendusse Sales importimise ajal selle väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="b85f8-126">**On väliselt hallatav = jah**: toode pärineb rakendusest Finance and Operations ega ole rakenduses Sales redigeeritav.</span><span class="sxs-lookup"><span data-stu-id="b85f8-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="b85f8-127">**On väliselt hallatav = ei**: toode sisestatakse otse rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="b85f8-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="b85f8-128">**On väliselt hallatav = tühi**: toode on rakenduses Sales olemas enne lahenduse Potentsiaalne klient sularahaks lubamist.</span><span class="sxs-lookup"><span data-stu-id="b85f8-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="b85f8-129">Välja **On väliselt hallatav** teavet kasutatakse tagamaks, et ainult **pakkumised** ja **müügitellimused** sättega **Väliselt hallatavad tooted** sünkroonitakse rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b85f8-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="b85f8-130">**Väliselt hallatavad toote** lisatakse automaatselt esimesse kehtivasse **hinnakirja**, millel on sama valuuta.</span><span class="sxs-lookup"><span data-stu-id="b85f8-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="b85f8-131">Pange tähele, et loend on korraldatud tähestikuliselt **nime** järgi.</span><span class="sxs-lookup"><span data-stu-id="b85f8-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="b85f8-132">Toote müügihinda rakendusest Finance and Operations kasutatakse **hinnakirja** hinnana.</span><span class="sxs-lookup"><span data-stu-id="b85f8-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="b85f8-133">See tähendab, et rakenduses Sales peab olema **hinnakiri** igale **toote müügivaluutale** rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b85f8-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="b85f8-134">Vabastatud müüdavate toodete valuutaks on määratud selle juriidilise isiku arvestusvaluuta, millest toode eksporditakse.</span><span class="sxs-lookup"><span data-stu-id="b85f8-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="b85f8-135">Toote sünkroonimine ei õnnestu ilma vastava valuutaga **hinnakirjata**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b85f8-136">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="b85f8-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="b85f8-137">Enne kui saate esimese sünkroonimise käivitada, peate olemasolevate toodete puhul rakenduses Finance and Operations asustama välja **Eristatava toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="b85f8-138">Olemasolevaid tooteid ei sünkroonita, enne kui see töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="b85f8-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="b85f8-139">Kasutage rakenduses Finance and Operations otsingufunktsiooni, et otsida suvandit **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="b85f8-140">Klõpsake töö käivitamiseks nuppu **Asusta eristuva toote tabel**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="b85f8-141">See töö tuleb käivitada ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="b85f8-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="b85f8-142">Veenduge, et vajalik **ValueMap** müügi **mõõtühikuks** (UOM) rakenduses Finance and Operations oleks vastenduses **Allikas -\> CDS-i vastenduse SalesUnitSymbol / DefaultSellingUnitOfMeasure** olemas.</span><span class="sxs-lookup"><span data-stu-id="b85f8-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="b85f8-143">Värskendage väärtust **CDS-i organisatsiooni ID Organization_OrganizationId** vastenduses **Allikas -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="b85f8-144">Malli vaikeväärtus on ORG001.</span><span class="sxs-lookup"><span data-stu-id="b85f8-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="b85f8-145">Värskendage väärtust **ValueMap** suvandis **Ühikurühm** (**defaultuomscheduleid.name**) vastenduses **CDS -\> Sihtkoht**, et see vastaks suvandile **Ühikurühmad** rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="b85f8-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="b85f8-146">Malli vaikeväärtus on **Vaikeühik**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="b85f8-147">Veenduge, et kõigi toodete müügi mõõtühikud rakendusest Finance and Operations oleksid rakenduses Sales olemas väärtusega **CDS-i märkeloendid**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="b85f8-148">Veenduge, et **hinnakirjad** oleksid rakenduses Sales olemas iga toote müügivaluuta kohta rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b85f8-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="b85f8-149">Tooteid saab müüa rakenduses Sales olekuga **Mustand** või **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="b85f8-150">Seda juhitakse rakenduse Sales menüü **Süsteemi sätted** jaotises **Müük**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="b85f8-151">Mustandina loodud tooted tuleb aktiveerida, enne kui need saab lisada **pakkumisele** või **müügitellimusele**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="b85f8-152">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="b85f8-152">Template mapping in data integrator</span></span>

<span data-ttu-id="b85f8-153">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="b85f8-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![malli vastendamine andmeintegraatoris](./media/products-template-mapping-data-integrator-1.png)

![malli vastendamine toodete puhul andmeintegraatoris](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="b85f8-156">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="b85f8-156">Related topics</span></span>

[<span data-ttu-id="b85f8-157">Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="b85f8-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="b85f8-158">Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="b85f8-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="b85f8-159">Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b85f8-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="b85f8-160">Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b85f8-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="b85f8-161">Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b85f8-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


