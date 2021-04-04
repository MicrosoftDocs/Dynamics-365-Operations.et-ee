---
title: Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Dynamics 365 Sales otse rakendusega Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.openlocfilehash: a1cf4072cb873ebbf4e0e46f16771458e436bcac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243101"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="5338f-103">Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="5338f-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5338f-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Dynamics 365 Sales otse rakendusega Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="5338f-105">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="5338f-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5338f-106">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="5338f-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5338f-107">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="5338f-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="5338f-108">Andmeintegratsiooni funktsiooniga saadaolevad Prospect to cash mallid võimaldavad andmevahetust kontode, kontaktide, toodete, müügihindade, müügitellimuste ja müügiarvete kohta Supply Chain Managementi ja Salesi vahel.</span><span class="sxs-lookup"><span data-stu-id="5338f-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="5338f-109">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="5338f-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="5338f-110">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5338f-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="5338f-111">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="5338f-111">Template and tasks</span></span>

<span data-ttu-id="5338f-112">Müügipakkumise päiste ja ridade vahetuks sünkroonimiseks rakendusest Sales rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="5338f-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="5338f-113">**Andmete integratsioon malli nimi:** Müügipakkumised (rakendusest Sales rakendusse Supply Chain Management) – otse</span><span class="sxs-lookup"><span data-stu-id="5338f-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="5338f-114">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="5338f-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="5338f-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5338f-115">QuoteHeader</span></span>
    - <span data-ttu-id="5338f-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5338f-116">QuoteLine</span></span>

<span data-ttu-id="5338f-117">Enne müügipakkumise päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="5338f-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="5338f-118">Tooted (rakendusest Supply Chain Management rakendusse Sales) - otse</span><span class="sxs-lookup"><span data-stu-id="5338f-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="5338f-119">Kontod (rakendusest Sales rakendusse Supply Chain Management) - otse (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="5338f-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="5338f-120">Kontaktid klientidesse (Salesist Supply Chain Managementi) - otse (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="5338f-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="5338f-121">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="5338f-121">Entity set</span></span>

| <span data-ttu-id="5338f-122">Müük</span><span class="sxs-lookup"><span data-stu-id="5338f-122">Sales</span></span>        | <span data-ttu-id="5338f-123">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5338f-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="5338f-124">Tsitaadid</span><span class="sxs-lookup"><span data-stu-id="5338f-124">Quotes</span></span>       | <span data-ttu-id="5338f-125">Dataverse’i müügipakkumise päis</span><span class="sxs-lookup"><span data-stu-id="5338f-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="5338f-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="5338f-126">QuoteDetails</span></span> | <span data-ttu-id="5338f-127">Dataverse’i müügipakkumise read</span><span class="sxs-lookup"><span data-stu-id="5338f-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="5338f-128">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="5338f-128">Entity flow</span></span>

<span data-ttu-id="5338f-129">Müügiarved luuakse rakenduses Sales ja sünkroonitakse rakendusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="5338f-130">Müügipakkumised rakendusest Sales sünkroonitakse ainult juhul, kui täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="5338f-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="5338f-131">Kõiki müügipakkumises olevaid tooteid hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="5338f-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="5338f-132">Kui klõpsate käsku **Aktiveeri pakkumine**, muutub müügipakkumine aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="5338f-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5338f-133">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="5338f-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5338f-134">Pakkumise üksusele on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, et jälgida järjepidevalt, kas üksus **Müügipakkumine** sisaldab täielikult või väliselt hallatavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="5338f-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="5338f-135">Kui müügipakkumine sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="5338f-136">See käitumine aitab tagada, et te ei püüa sünkroonida müügipakkumise ridu, mis hõlmavad rakenduse Supply Chain Management jaoks tundmatuid tooteid.</span><span class="sxs-lookup"><span data-stu-id="5338f-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="5338f-137">Kõiki müügipakkumise tooteid ja ridu värskendatakse müügipakkumise päisest pärit teabega **Sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="5338f-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="5338f-138">See teave on saadaval üksuse **QuoteDetails** väljal **Pakkumine sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="5338f-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="5338f-139">Pakkumise tootele saab lisada allahindluse, mis sünkroonitakse rakendusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="5338f-140">Päise välju **Allahindlus**, **Tasud** ja **Maks** juhitakse seadistusega rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="5338f-141">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="5338f-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="5338f-142">Praeguses kujunduses haldab ja reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="5338f-143">Rakenduses Sales muudab lahendus järgmised väljad kirjutuskaitstuks, kuna väärtusi ei sünkroonita rakendusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="5338f-144">Müügipakkumise päise kirjutuskaitstud väljad: **Allahindluse %**, **Allahindlus** ja **Veose kogus**</span><span class="sxs-lookup"><span data-stu-id="5338f-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="5338f-145">Pakkumise toodete kirjutuskaitstud väljad: **Maks**</span><span class="sxs-lookup"><span data-stu-id="5338f-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5338f-146">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="5338f-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="5338f-147">Enne müügipakkumiste sünkroonimist on oluline värskendada järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="5338f-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="5338f-148">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="5338f-148">Setup in Sales</span></span>

- <span data-ttu-id="5338f-149">Veenduge, et load oleks seadistatud töörühma jaoks, kuhu rakenduses Sales häälestatud ühendusest pärit kasutaja on määratud.</span><span class="sxs-lookup"><span data-stu-id="5338f-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="5338f-150">Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte.</span><span class="sxs-lookup"><span data-stu-id="5338f-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="5338f-151">Kui töörühmal ei ole administraatorijuurdepääsu, ilmub andmete integratsioonis projekti käivitamisel veateade, mis annab teada, et peamine töörühm puudub.</span><span class="sxs-lookup"><span data-stu-id="5338f-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="5338f-152">Töörühma lubade seadistamiseks avage jaotis **Sätted** &gt; **Turve** &gt; **Töörühmad** ja valige vastav töörühm.</span><span class="sxs-lookup"><span data-stu-id="5338f-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="5338f-153">Valige **Rollide haldamine** ja seejärel valige roll, millel on soovitud load, nt **Süsteemiadministraator**.</span><span class="sxs-lookup"><span data-stu-id="5338f-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="5338f-154">Avage jaotis **Sätted** &gt; **Administreerimine** &gt; **Süsteemisätted** &gt; **Sales** ja veenduge, et kasutusel oleks järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="5338f-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="5338f-155">Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="5338f-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="5338f-156">Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.</span><span class="sxs-lookup"><span data-stu-id="5338f-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="5338f-157">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="5338f-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="5338f-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5338f-158">QuoteHeader</span></span>

- <span data-ttu-id="5338f-159">Veenduge, et atribuutide **Shipto\_country** – **DeliveryAddressCountryRegionISOCode** vahel oleks olemas nõutav vastendamine.</span><span class="sxs-lookup"><span data-stu-id="5338f-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="5338f-160">Väärtuste kaardil saate määratleda vaikeväärtuse, mida kasutatakse juhul, kui väärtus on tühi.</span><span class="sxs-lookup"><span data-stu-id="5338f-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="5338f-161">Jätke vasak pool tühjaks ja määrake paremal pool soovitud riik või regioon.</span><span class="sxs-lookup"><span data-stu-id="5338f-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="5338f-162">Nii ei pea riigisiseste tellimuste puhul riiki või regiooni sisestama.</span><span class="sxs-lookup"><span data-stu-id="5338f-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="5338f-163">Malli väärtus on väärtuskaart, kus on vastendatud mitu riiki või regiooni ja mille puhul tühja välja väärtus on **Ameerika Ühendriigid**.</span><span class="sxs-lookup"><span data-stu-id="5338f-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="5338f-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5338f-164">QuoteLine</span></span>

- <span data-ttu-id="5338f-165">Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Supply Chain Management olemas.</span><span class="sxs-lookup"><span data-stu-id="5338f-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="5338f-166">Veenduge, et rakenduses Sales oleks nõutud ühikud määratletud.</span><span class="sxs-lookup"><span data-stu-id="5338f-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="5338f-167">Üksuste **oumid.name** ja **SalesUnitSymbol** jaoks on määratletud väärtuskaardiga malli väärtus.</span><span class="sxs-lookup"><span data-stu-id="5338f-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="5338f-168">Valikuline: saate lisada järgmised vastendused, et tagada pakkumise ridade importimine rakendusse Supply Chain Management, kui kliendilt või tootelt vaiketeave puudub.</span><span class="sxs-lookup"><span data-stu-id="5338f-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="5338f-169">**SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="5338f-170">Atribuudi **SiteId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="5338f-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="5338f-171">**WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="5338f-172">Atribuudi **WarehouseId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="5338f-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="5338f-173">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="5338f-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="5338f-174">Päise välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keeruka seadistusega rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="5338f-175">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="5338f-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="5338f-176">Praeguses kujunduses reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5338f-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="5338f-177">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="5338f-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="5338f-178">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="5338f-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="5338f-179">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="5338f-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="5338f-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5338f-180">QuoteHeader</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="5338f-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5338f-182">QuoteLine</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="5338f-184">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="5338f-184">Related topics</span></span>

[<span data-ttu-id="5338f-185">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="5338f-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]