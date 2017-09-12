---
title: "Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations"
description: "Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="3f6d8-103">Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3f6d8-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="3f6d8-104">Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="3f6d8-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="3f6d8-105">Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales (Sales) rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="3f6d8-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="3f6d8-106">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="3f6d8-106">Template and tasks</span></span>

<span data-ttu-id="3f6d8-107">Müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="3f6d8-108">**Malli nimi:** Müügipakkumised (Salesist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="3f6d8-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="3f6d8-109">**Ülesannete nimed projektis:**</span><span class="sxs-lookup"><span data-stu-id="3f6d8-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="3f6d8-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="3f6d8-110">QuoteHeader</span></span>
    - <span data-ttu-id="3f6d8-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="3f6d8-111">QuoteLine</span></span>

<span data-ttu-id="3f6d8-112">Enne müügipakkumise päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="3f6d8-113">Tooted</span><span class="sxs-lookup"><span data-stu-id="3f6d8-113">Products</span></span>
- <span data-ttu-id="3f6d8-114">Kontod (kui on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="3f6d8-114">Accounts (if used)</span></span>
- <span data-ttu-id="3f6d8-115">Kontaktid (kui on kasutusel)</span><span class="sxs-lookup"><span data-stu-id="3f6d8-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="3f6d8-116">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="3f6d8-116">Entity set</span></span>

| <span data-ttu-id="3f6d8-117">Müük</span><span class="sxs-lookup"><span data-stu-id="3f6d8-117">Sales</span></span>        | <span data-ttu-id="3f6d8-118">CDS</span><span class="sxs-lookup"><span data-stu-id="3f6d8-118">CDS</span></span>           | <span data-ttu-id="3f6d8-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3f6d8-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="3f6d8-120">Tsitaadid</span><span class="sxs-lookup"><span data-stu-id="3f6d8-120">Quotes</span></span>       | <span data-ttu-id="3f6d8-121">Pakkumine</span><span class="sxs-lookup"><span data-stu-id="3f6d8-121">Quotation</span></span>     | <span data-ttu-id="3f6d8-122">Müügipakkumise päised</span><span class="sxs-lookup"><span data-stu-id="3f6d8-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="3f6d8-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="3f6d8-123">QuoteDetails</span></span> | <span data-ttu-id="3f6d8-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="3f6d8-124">QuotationLine</span></span> | <span data-ttu-id="3f6d8-125">CDS-i müügipakkumise read</span><span class="sxs-lookup"><span data-stu-id="3f6d8-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3f6d8-126">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="3f6d8-126">Entity flow</span></span>

<span data-ttu-id="3f6d8-127">Müügipakkumised luuakse rakenduses Sales ja sünkroonitakse rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="3f6d8-128">Müügipakkumised rakendusest Sales sünkroonitakse ainult juhul, kui täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="3f6d8-129">Kõiki müügipakkumise ridadel olevaid tooteid hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="3f6d8-130">Müügipakkumine on aktiivne või aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3f6d8-131">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="3f6d8-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="3f6d8-132">Pakkumise üksusele on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, et jälgida järjepidevalt, kas müügipakkumine sisaldab täielikult või väliselt hallatavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="3f6d8-133">Kui müügipakkumine sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="3f6d8-134">See käitumine aitab tagada, et te ei püüa sünkroonida müügipakkumise ridu toodetega, mis on rakendusele Finance and Operations tundmatud.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="3f6d8-135">Kõiki tooteid ja ridu pakkumises värskendatakse pakkumise päisest pärit teabega **Sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="3f6d8-136">See teave on leitav pakkumise reaüksuse väljalt **Pakkumine sisaldab ainult väliselt hallatavaid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="3f6d8-137">Välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keerulise seadistusega rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="3f6d8-138">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="3f6d8-139">Praeguses kujunduses haldab ja reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="3f6d8-140">Rakenduses Sales muudab lahendus järgmised väljad kirjutuskaitstuks, kuna väärtusi ei sünkroonita rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="3f6d8-141">**Müügipakkumise päise kirjutuskaitstud väljad:** Allahindluse %, Allahindlus, Veose kogus</span><span class="sxs-lookup"><span data-stu-id="3f6d8-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="3f6d8-142">**Müügipakkumise ridade kirjutuskaitstud väljad:** Maks</span><span class="sxs-lookup"><span data-stu-id="3f6d8-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3f6d8-143">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="3f6d8-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="3f6d8-144">Enne müügipakkumiste sünkroonimist minge rakenduses Sales jaotisse **Sätted** &gt; **Haldus** &gt; **Süsteemi sätted** &gt; **Müük** ja veenduge, et välja **Allahindluse arvutamise meetod** sätteks oleks valitud **Ühiku kohta**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="3f6d8-145">See säte aitab tagada, et reaüksuse allahindlus rakendusest Sales vastab sättele rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="3f6d8-146">Muidu ei ole allahindlus rakenduses Finance and Operations õige, kuna Finance and Operations loeb allahindlust allahindlusena ühiku kohta, isegi kui see oli rakenduses Sales allahindlus rea kohta.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="3f6d8-147">Minge rakenduses Finance and Operations jaotisse **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="3f6d8-148">Valige vahekaardil **Numbriseeria** müügipakkumiste numbriseeria ja klõpsake siis nuppu **Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="3f6d8-149">Seejärel seadke jaotises **Üldine seadistus** välja **Käsitsi** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="3f6d8-150">Minge rakenduses Finance and Operations jaotisse **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="3f6d8-151">Seejärel seadke vahekaardil **Saadetised** välja **Tarnekuupäeva juhtimine** sätteks **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="3f6d8-152">See säte aitab vältida müügipakkumiste puhul sünkroonimise nurjumist.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="3f6d8-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="3f6d8-153">QuoteHeader</span></span>

- <span data-ttu-id="3f6d8-154">Väli **Nõutud tarnekuupäev** on rakenduses Finance and Operations nõutav ning sünkroonimine nurjub, kui see väli on jäetud tühjaks.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="3f6d8-155">Selle probleemi vältimiseks võetakse juhul, kui väli on tühi, vaikekuupäev valikust **Allikas &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="3f6d8-156">Kuupäev tuleb värskendada eelistatud väärtusele.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="3f6d8-157">Praegu ei saa tänase kuupäeva tähistamiseks sisestada väärtust, nagu **Täna**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="3f6d8-158">Peate sisestama kindla kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-158">You must enter a specific date.</span></span> <span data-ttu-id="3f6d8-159">Malli vaikeväärtus suvandi **Nõutav tarnekuupäev** puhul on **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="3f6d8-160">Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="3f6d8-161">Selleks et vältida sünkroonimistõrkeid, saate määrata vaikeväärtuse, mida kasutatakse, kui see väli on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="3f6d8-162">See vaikeväärtus on kasulik ka seetõttu, et kohalike aadresside puhul ei peate väljale **Riik, piirkond** väärtust käsitsi sisestama.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="3f6d8-163">Atribuudi **DeliveryAddressCountryRegionISOCode** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="3f6d8-164">Värskendage välja **CDS Organization ID** vastendust jaotises **Allikas &gt; CDS**, nii et see vastaks valikule **CDS-i organisatsioon** organisatsiooniüksuses.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="3f6d8-165">Malli vaikeväärtus atribuudi **Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="3f6d8-166">Malli vaikeväärtus atribuudi **Account_Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="3f6d8-167">Malli vaikeväärtus atribuudi **InvoiceAccount_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="3f6d8-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="3f6d8-168">QuoteLine</span></span>

- <span data-ttu-id="3f6d8-169">Värskendage välja **CDS Organization ID** vastendust jaotises **Allikas &gt; CDS**, nii et see vastaks valikule **CDS-i organisatsioon** organisatsiooniüksuses.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="3f6d8-170">Malli vaikeväärtus atribuudi **Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="3f6d8-171">Malli vaikeväärtus atribuudi **Product_Organization_Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="3f6d8-172">Malli vaikeväärtus atribuudi **Quotation_Organization_Organization_OrganizationId** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="3f6d8-173">Väli **Nõutud tarnekuupäev** on rakenduses Finance and Operations nõutav ning sünkroonimine nurjub, kui see väli on jäetud tühjaks.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="3f6d8-174">Selle probleemi vältimiseks võetakse juhul, kui väli on tühi, vaikekuupäev valikust **Allikas &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="3f6d8-175">Kuupäev tuleb värskendada eelistatud väärtusele.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="3f6d8-176">Praegu ei saa tänase kuupäeva tähistamiseks sisestada väärtust, nagu **Täna**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="3f6d8-177">Peate sisestama kindla kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-177">You must enter a specific date.</span></span> <span data-ttu-id="3f6d8-178">Malli vaikeväärtus suvandi **Nõutav tarnekuupäev** puhul on **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="3f6d8-179">Saate lisada jaotisest **CDS &gt; Sihtkoht** järgmised vastendused, et tagada pakkumise ridade importimine rakendusse Finance and Operations, kui kliendilt või tootelt vaiketeave puudub.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="3f6d8-180">**SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="3f6d8-181">Atribuudi **SiteId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="3f6d8-182">**WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="3f6d8-183">Atribuudi **WarehouseId** jaoks malli vaikeväärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="3f6d8-184">Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduses Finance and Operations oleks jaotise **CDS &gt; Sihtkoht** vastenduses suvandi **Quantity_UOM** puhul atribuudile **SALESUNITSYMBOL** olemas.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="3f6d8-185">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="3f6d8-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="3f6d8-186">Välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keerulise seadistusega rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="3f6d8-187">See seadistus ei toeta praegu integratsiooni vastendamist.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="3f6d8-188">Praeguses kujunduses reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="3f6d8-189">Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="3f6d8-190">Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="3f6d8-191">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="3f6d8-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="3f6d8-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="3f6d8-192">QuoteHeader</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="3f6d8-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="3f6d8-195">QuoteLine</span></span>

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="3f6d8-198">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="3f6d8-198">Related topics</span></span>

[<span data-ttu-id="3f6d8-199">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="3f6d8-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="3f6d8-200">Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="3f6d8-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="3f6d8-201">Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="3f6d8-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



