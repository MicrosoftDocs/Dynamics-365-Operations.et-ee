---
title: "Rakenduse Sales müügipakkumise päiste ja ridade vahetu sünkroonimine rakendusega Finance and Operations"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 77b15a51073bf923f09a4a0e83ee5b2642eec4af
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="5f5da-103">Rakenduse Sales müügipakkumise päiste ja ridade vahetu sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5f5da-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f5da-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="5f5da-105">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="5f5da-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="5f5da-106">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="5f5da-106">Template and tasks</span></span>

<span data-ttu-id="5f5da-107">Müügipakkumise päiste ja ridade vahetuks sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="5f5da-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="5f5da-108">**Andmete integratsioon malli nimi:** Müügipakkumised (rakendusest Sales rakendusse Fin and Ops) – otse</span><span class="sxs-lookup"><span data-stu-id="5f5da-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="5f5da-109">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="5f5da-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="5f5da-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5f5da-110">QuoteHeader</span></span>
    - <span data-ttu-id="5f5da-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5f5da-111">QuoteLine</span></span>

<span data-ttu-id="5f5da-112">Enne müügipakkumise päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="5f5da-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="5f5da-113">Tooted (rakendusest Sales rakendusse Fin and Ops) – otse</span><span class="sxs-lookup"><span data-stu-id="5f5da-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5f5da-114">Kontod (rakendusest Sales rakendusse Fin and Ops) – otse (kui on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="5f5da-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="5f5da-115">Kontaktid klientideks (rakendusest Sales rakendusse Fin and Ops) – otse (kui see on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="5f5da-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="5f5da-116">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="5f5da-116">Entity set</span></span>

| <span data-ttu-id="5f5da-117">Müük</span><span class="sxs-lookup"><span data-stu-id="5f5da-117">Sales</span></span>        | <span data-ttu-id="5f5da-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5f5da-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="5f5da-119">Tsitaadid</span><span class="sxs-lookup"><span data-stu-id="5f5da-119">Quotes</span></span>       | <span data-ttu-id="5f5da-120">CDS-i müügipakkumise päis</span><span class="sxs-lookup"><span data-stu-id="5f5da-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="5f5da-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="5f5da-121">QuoteDetails</span></span> | <span data-ttu-id="5f5da-122">CDS-i müügipakkumise read</span><span class="sxs-lookup"><span data-stu-id="5f5da-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="5f5da-123">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="5f5da-123">Entity flow</span></span>

<span data-ttu-id="5f5da-124">Müügipakkumised luuakse rakenduses Sales ja sünkroonitakse rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="5f5da-125">Müügipakkumised rakendusest Sales sünkroonitakse ainult juhul, kui täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="5f5da-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="5f5da-126">Kõiki müügipakkumises olevaid tooteid hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="5f5da-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="5f5da-127">Kui klõpsate käsku **Aktiveeri pakkumine**, muutub müügipakkumine aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="5f5da-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5f5da-128">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="5f5da-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5f5da-129">Pakkumise üksusele on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, et jälgida järjepidevalt, kas üksus **Müügipakkumine** sisaldab täielikult või väliselt hallatavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="5f5da-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="5f5da-130">Kui müügipakkumine sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="5f5da-131">See käitumine aitab tagada, et te ei püüa sünkroonida müügipakkumise ridu, mis hõlmavad rakenduse Finance and Operations jaoks tundmatuid tooteid.</span><span class="sxs-lookup"><span data-stu-id="5f5da-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="5f5da-132">Kõiki müügipakkumise tooteid ja ridu värskendatakse müügipakkumise päisest pärit teabega **Sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="5f5da-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="5f5da-133">See teave on saadaval üksuse **QuoteDetails** väljal **Pakkumine sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="5f5da-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="5f5da-134">Pakkumise tootele saab lisada allahindluse, mis sünkroonitakse rakendusega Finance ja Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="5f5da-135">Päise välju **Allahindlus**, **Tasud** ja **Maks** juhitakse seadistusega rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="5f5da-136">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="5f5da-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="5f5da-137">Praeguses kujunduses haldab ja reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="5f5da-138">Rakenduses Sales muudab lahendus järgmised väljad kirjutuskaitstuks, kuna väärtusi ei sünkroonita rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="5f5da-139">Müügipakkumise päise kirjutuskaitstud väljad: **Allahindluse %**, **Allahindlus** ja **Veose kogus**</span><span class="sxs-lookup"><span data-stu-id="5f5da-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="5f5da-140">Pakkumise toodete kirjutuskaitstud väljad: **Maks**</span><span class="sxs-lookup"><span data-stu-id="5f5da-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5f5da-141">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="5f5da-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="5f5da-142">Enne müügipakkumiste sünkroonimist on oluline värskendada järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="5f5da-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="5f5da-143">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="5f5da-143">Setup in Sales</span></span>

- <span data-ttu-id="5f5da-144">Veenduge, et load oleks seadistatud töörühma jaoks, kuhu rakenduses Sales häälestatud ühendusest pärit kasutaja on määratud.</span><span class="sxs-lookup"><span data-stu-id="5f5da-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="5f5da-145">Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte.</span><span class="sxs-lookup"><span data-stu-id="5f5da-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="5f5da-146">Kui töörühmal ei ole administraatorijuurdepääsu, ilmub andmete integratsioonis projekti käivitamisel veateade, mis annab teada, et peamine töörühm puudub.</span><span class="sxs-lookup"><span data-stu-id="5f5da-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="5f5da-147">Töörühma lubade seadistamiseks avage jaotis **Sätted** &gt; **Turve** &gt; **Töörühmad** ja valige vastav töörühm.</span><span class="sxs-lookup"><span data-stu-id="5f5da-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="5f5da-148">Valige **Rollide haldamine** ja seejärel valige roll, millel on soovitud load, nt **Süsteemiadministraator**.</span><span class="sxs-lookup"><span data-stu-id="5f5da-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="5f5da-149">Avage jaotis **Sätted** &gt; **Administreerimine** &gt; **Süsteemisätted** &gt; **Sales** ja veenduge, et kasutusel oleks järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="5f5da-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="5f5da-150">Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="5f5da-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="5f5da-151">Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.</span><span class="sxs-lookup"><span data-stu-id="5f5da-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="5f5da-152">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="5f5da-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="5f5da-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5f5da-153">QuoteHeader</span></span>

- <span data-ttu-id="5f5da-154">Veenduge, et atribuutide **Shipto\_country** – **DeliveryAddressCountryRegionISOCode** vahel oleks olemas nõutav vastendamine.</span><span class="sxs-lookup"><span data-stu-id="5f5da-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="5f5da-155">Väärtuste kaardil saate määratleda vaikeväärtuse, mida kasutatakse juhul, kui väärtus on tühi.</span><span class="sxs-lookup"><span data-stu-id="5f5da-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="5f5da-156">Jätke vasak pool tühjaks ja määrake paremal pool soovitud riik või regioon.</span><span class="sxs-lookup"><span data-stu-id="5f5da-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="5f5da-157">Nii ei pea riigisiseste tellimuste puhul riiki või regiooni sisestama.</span><span class="sxs-lookup"><span data-stu-id="5f5da-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="5f5da-158">Malli väärtus on väärtuskaart, kus on vastendatud mitu riiki või regiooni ja mille puhul tühja välja väärtus on **Ameerika Ühendriigid**.</span><span class="sxs-lookup"><span data-stu-id="5f5da-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="5f5da-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5f5da-159">QuoteLine</span></span>

- <span data-ttu-id="5f5da-160">Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Finance and Operations olemas.</span><span class="sxs-lookup"><span data-stu-id="5f5da-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="5f5da-161">Veenduge, et rakenduses Sales oleks nõutud ühikud määratletud.</span><span class="sxs-lookup"><span data-stu-id="5f5da-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="5f5da-162">Üksuste **oumid.name** ja **SalesUnitSymbol** jaoks on määratletud väärtuskaardiga malli väärtus.</span><span class="sxs-lookup"><span data-stu-id="5f5da-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="5f5da-163">Valikuline: saate lisada järgmised vastendused, et tagada pakkumise ridade importimine rakendusse Finance and Operations, kui kliendilt või tootelt vaiketeave puudub.</span><span class="sxs-lookup"><span data-stu-id="5f5da-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="5f5da-164">**SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="5f5da-165">Atribuudi **SiteId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="5f5da-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="5f5da-166">**WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="5f5da-167">Atribuudi **WarehouseId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="5f5da-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="5f5da-168">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="5f5da-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="5f5da-169">Välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keerulise seadistusega rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="5f5da-170">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="5f5da-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="5f5da-171">Praeguses kujunduses reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5da-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="5f5da-172">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="5f5da-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="5f5da-173">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="5f5da-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="5f5da-174">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="5f5da-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="5f5da-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5f5da-175">QuoteHeader</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="5f5da-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5f5da-177">QuoteLine</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="5f5da-179">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="5f5da-179">Related topics</span></span>

[<span data-ttu-id="5f5da-180">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="5f5da-180">Prospect to cash</span></span>](prospect-to-cash.md)


