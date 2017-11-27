---
title: "Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations"
description: "Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="10b21-103">Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10b21-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="10b21-104">Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="10b21-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="10b21-105">Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales (Sales) rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="10b21-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="10b21-106">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="10b21-106">Template and tasks</span></span>

<span data-ttu-id="10b21-107">Müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="10b21-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="10b21-108">**Malli nimi:** Müügipakkumised (Salesist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="10b21-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="10b21-109">**Ülesannete nimed projektis:**</span><span class="sxs-lookup"><span data-stu-id="10b21-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="10b21-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="10b21-110">QuoteHeader</span></span>
    - <span data-ttu-id="10b21-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="10b21-111">QuoteLine</span></span>

<span data-ttu-id="10b21-112">Enne müügipakkumise päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="10b21-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="10b21-113">Tooted (Fin and Opsist Salesi)</span><span class="sxs-lookup"><span data-stu-id="10b21-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="10b21-114">Kontod (Salesist Fin and Opsi) (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="10b21-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="10b21-115">Kontaktid klientideks (Salesist Fin and Opsi) (kui kasutatakse)</span><span class="sxs-lookup"><span data-stu-id="10b21-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="10b21-116">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="10b21-116">Entity set</span></span>

| <span data-ttu-id="10b21-117">Müük</span><span class="sxs-lookup"><span data-stu-id="10b21-117">Sales</span></span>        | <span data-ttu-id="10b21-118">CDS</span><span class="sxs-lookup"><span data-stu-id="10b21-118">CDS</span></span>           | <span data-ttu-id="10b21-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10b21-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="10b21-120">Tsitaadid</span><span class="sxs-lookup"><span data-stu-id="10b21-120">Quotes</span></span>       | <span data-ttu-id="10b21-121">Pakkumine</span><span class="sxs-lookup"><span data-stu-id="10b21-121">Quotation</span></span>     | <span data-ttu-id="10b21-122">Müügipakkumise päised</span><span class="sxs-lookup"><span data-stu-id="10b21-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="10b21-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="10b21-123">QuoteDetails</span></span> | <span data-ttu-id="10b21-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="10b21-124">QuotationLine</span></span> | <span data-ttu-id="10b21-125">CDS-i müügipakkumise read</span><span class="sxs-lookup"><span data-stu-id="10b21-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="10b21-126">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="10b21-126">Entity flow</span></span>

<span data-ttu-id="10b21-127">Müügipakkumised luuakse rakenduses Sales ja sünkroonitakse rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="10b21-128">Müügipakkumised rakendusest Sales sünkroonitakse ainult juhul, kui täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="10b21-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="10b21-129">Kõiki müügipakkumise ridadel olevaid tooteid hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="10b21-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="10b21-130">Müügipakkumine on aktiivne või aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="10b21-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="10b21-131">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="10b21-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="10b21-132">Pakkumise üksusele on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, et jälgida järjepidevalt, kas müügipakkumine sisaldab täielikult või väliselt hallatavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="10b21-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="10b21-133">Kui müügipakkumine sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="10b21-134">See käitumine aitab tagada, et te ei püüa sünkroonida müügipakkumise ridu toodetega, mis on rakendusele Finance and Operations tundmatud.</span><span class="sxs-lookup"><span data-stu-id="10b21-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="10b21-135">Kõiki tooteid ja ridu pakkumises värskendatakse pakkumise päisest pärit teabega **Sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="10b21-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="10b21-136">See teave on leitav pakkumise reaüksuse väljalt **Pakkumine sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="10b21-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="10b21-137">Välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keerulise seadistusega rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="10b21-138">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="10b21-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="10b21-139">Praeguses kujunduses haldab ja reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="10b21-140">Rakenduses Sales muudab lahendus järgmised väljad kirjutuskaitstuks, kuna väärtusi ei sünkroonita rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="10b21-141">**Müügipakkumise päise kirjutuskaitstud väljad:** Allahindluse %, Allahindlus, Veose kogus</span><span class="sxs-lookup"><span data-stu-id="10b21-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="10b21-142">**Müügipakkumise ridade kirjutuskaitstud väljad:** Maks</span><span class="sxs-lookup"><span data-stu-id="10b21-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="10b21-143">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="10b21-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="10b21-144">Enne müügitellimuste sünkroonimist on oluline värskendada süsteeme järgmise sättega.</span><span class="sxs-lookup"><span data-stu-id="10b21-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="10b21-145">Seadistus rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="10b21-145">Setup in Sales</span></span>

- <span data-ttu-id="10b21-146">Avage **Sätted** &gt; **Haldus** &gt; **Süsteemi sätted** &gt; **Müük** ja veenduge, et välja **Allahindluse arvutamise meetod** sätteks oleks valitud **Ühiku kohta**.</span><span class="sxs-lookup"><span data-stu-id="10b21-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="10b21-147">See säte aitab tagada, et reaüksuse allahindlus rakendusest Sales vastab sättele rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="10b21-148">Muidu ei ole allahindlus rakenduses Finance and Operations õige, kuna Finance and Operations loeb allahindlust allahindlusena ühiku kohta, isegi kui see oli rakenduses Sales allahindlus rea kohta.</span><span class="sxs-lookup"><span data-stu-id="10b21-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="10b21-149">Seadistus rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10b21-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="10b21-150">Avage **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="10b21-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="10b21-151">Valige vahekaardil **Numbriseeria** müügipakkumiste numbriseeria ja klõpsake siis nuppu **Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="10b21-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="10b21-152">Seejärel seadke jaotises **Üldine seadistus** välja **Käsitsi** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="10b21-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="10b21-153">Avage **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="10b21-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="10b21-154">Seejärel seadke vahekaardil **Saadetised** välja **Tarnekuupäeva juhtimine** sätteks **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="10b21-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="10b21-155">See säte aitab vältida müügipakkumiste puhul sünkroonimise nurjumist.</span><span class="sxs-lookup"><span data-stu-id="10b21-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="10b21-156">Seadistus andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="10b21-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="10b21-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="10b21-157">QuoteHeader</span></span>

- <span data-ttu-id="10b21-158">Väli **Nõutud tarnekuupäev** on rakenduses Finance and Operations nõutav ning sünkroonimine nurjub, kui see väli on jäetud tühjaks.</span><span class="sxs-lookup"><span data-stu-id="10b21-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="10b21-159">Selle probleemi vältimiseks võetakse juhul, kui väli on tühi, vaikekuupäev valikust **Allikas &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="10b21-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="10b21-160">Kuupäev tuleb värskendada eelistatud väärtusele.</span><span class="sxs-lookup"><span data-stu-id="10b21-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="10b21-161">Praegu ei saa tänase kuupäeva tähistamiseks sisestada väärtust, nagu **Täna**.</span><span class="sxs-lookup"><span data-stu-id="10b21-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="10b21-162">Peate sisestama kindla kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="10b21-162">You must enter a specific date.</span></span> <span data-ttu-id="10b21-163">Malli vaikeväärtus suvandi **Nõutav tarnekuupäev** puhul on **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="10b21-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="10b21-164">Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav.</span><span class="sxs-lookup"><span data-stu-id="10b21-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="10b21-165">Selleks et vältida sünkroonimistõrkeid, saate määrata vaikeväärtuse, mida kasutatakse, kui see väli on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="10b21-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="10b21-166">See vaikeväärtus on kasulik ka seetõttu, et kohalike aadresside puhul ei peate väljale **Riik, piirkond** väärtust käsitsi sisestama.</span><span class="sxs-lookup"><span data-stu-id="10b21-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="10b21-167">Atribuudi **DeliveryAddressCountryRegionISOCode** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="10b21-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="10b21-168">Värskendage välja **CDS Organization ID** vastendust jaotises **Allikas &gt; CDS**, nii et see vastaks valikule **CDS-i organisatsioon** organisatsiooniüksuses.</span><span class="sxs-lookup"><span data-stu-id="10b21-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="10b21-169">Malli vaikeväärtus atribuudi **Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="10b21-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="10b21-170">Malli vaikeväärtus atribuudi **Account_Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="10b21-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="10b21-171">Malli vaikeväärtus atribuudi **InvoiceAccount_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="10b21-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="10b21-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="10b21-172">QuoteLine</span></span>

- <span data-ttu-id="10b21-173">Värskendage välja **CDS Organization ID** vastendust jaotises **Allikas &gt; CDS**, nii et see vastaks valikule **CDS-i organisatsioon** organisatsiooniüksuses.</span><span class="sxs-lookup"><span data-stu-id="10b21-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="10b21-174">Malli vaikeväärtus atribuudi **Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="10b21-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="10b21-175">Malli vaikeväärtus atribuudi **Product_Organization_Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="10b21-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="10b21-176">Malli vaikeväärtus atribuudi **Quotation_Organization_Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="10b21-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="10b21-177">Väli **Nõutud tarnekuupäev** on rakenduses Finance and Operations nõutav ning sünkroonimine nurjub, kui see väli on jäetud tühjaks.</span><span class="sxs-lookup"><span data-stu-id="10b21-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="10b21-178">Selle probleemi vältimiseks võetakse juhul, kui väli on tühi, vaikekuupäev valikust **Allikas &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="10b21-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="10b21-179">Kuupäev tuleb värskendada eelistatud väärtusele.</span><span class="sxs-lookup"><span data-stu-id="10b21-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="10b21-180">Praegu ei saa tänase kuupäeva tähistamiseks sisestada väärtust, nagu **Täna**.</span><span class="sxs-lookup"><span data-stu-id="10b21-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="10b21-181">Peate sisestama kindla kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="10b21-181">You must enter a specific date.</span></span> <span data-ttu-id="10b21-182">Malli vaikeväärtus suvandi **Nõutav tarnekuupäev** puhul on **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="10b21-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="10b21-183">Saate lisada jaotisest **CDS &gt; Sihtkoht** järgmised vastendused, et tagada pakkumise ridade importimine rakendusse Finance and Operations, kui kliendilt või tootelt vaiketeave puudub.</span><span class="sxs-lookup"><span data-stu-id="10b21-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="10b21-184">**SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="10b21-185">Atribuudi **SiteId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="10b21-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="10b21-186">**WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="10b21-187">Atribuudi **WarehouseId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="10b21-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="10b21-188">Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduses Finance and Operations oleks jaotise **CDS &gt; Sihtkoht** vastenduses suvandi **Quantity_UOM** puhul atribuudile **SALESUNITSYMBOL** olemas.</span><span class="sxs-lookup"><span data-stu-id="10b21-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="10b21-189">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="10b21-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="10b21-190">Välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keerulise seadistusega rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="10b21-191">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="10b21-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="10b21-192">Praeguses kujunduses reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10b21-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="10b21-193">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="10b21-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="10b21-194">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="10b21-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="10b21-195">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="10b21-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="10b21-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="10b21-196">QuoteHeader</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="10b21-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="10b21-199">QuoteLine</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="10b21-202">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="10b21-202">Related topics</span></span>

[<span data-ttu-id="10b21-203">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="10b21-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="10b21-204">Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="10b21-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="10b21-205">Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="10b21-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



