---
title: "Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontakti (kontaktid) ja kontakti (kliendid) sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="801d7-103">Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="801d7-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="801d7-104">Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="801d7-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="801d7-105">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontakti (kontaktid) üksuste ja kontakti (kliendid) sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales (Sales) rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="801d7-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="801d7-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="801d7-106">Templates and tasks</span></span>

<span data-ttu-id="801d7-107">Kontakti (kontaktid) sünkroonimiseks rakendusest Sales kontaktiga (kliendid) rakenduses Finance and Operations kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="801d7-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="801d7-108">**Mallide nimed:**</span><span class="sxs-lookup"><span data-stu-id="801d7-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="801d7-109">Kontaktid kontaktiga (Salesist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="801d7-109">Contacts to Contact (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="801d7-110">Kontaktid kliendiga (Salesist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="801d7-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="801d7-111">**Ülesannete nimed projektis:**</span><span class="sxs-lookup"><span data-stu-id="801d7-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="801d7-112">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="801d7-112">Contacts</span></span>
    - <span data-ttu-id="801d7-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="801d7-113">ContactToCustomer</span></span>

<span data-ttu-id="801d7-114">Enne kontakti sünkroonimist on nõutav järgmine sünkroonimisülesanne: kontod (Salesist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="801d7-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="801d7-115">Üksuste komplektid</span><span class="sxs-lookup"><span data-stu-id="801d7-115">Entity sets</span></span>

| <span data-ttu-id="801d7-116">Müük</span><span class="sxs-lookup"><span data-stu-id="801d7-116">Sales</span></span>    | <span data-ttu-id="801d7-117">CDS</span><span class="sxs-lookup"><span data-stu-id="801d7-117">CDS</span></span>     | <span data-ttu-id="801d7-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="801d7-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="801d7-119">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="801d7-119">Contacts</span></span> | <span data-ttu-id="801d7-120">Kontakt</span><span class="sxs-lookup"><span data-stu-id="801d7-120">Contact</span></span> | <span data-ttu-id="801d7-121">CDS-i kontaktid</span><span class="sxs-lookup"><span data-stu-id="801d7-121">CDS Contacts</span></span>           |
| <span data-ttu-id="801d7-122">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="801d7-122">Contacts</span></span> | <span data-ttu-id="801d7-123">Konto</span><span class="sxs-lookup"><span data-stu-id="801d7-123">Account</span></span> | <span data-ttu-id="801d7-124">Kliendid V2</span><span class="sxs-lookup"><span data-stu-id="801d7-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="801d7-125">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="801d7-125">Entity flow</span></span>

<span data-ttu-id="801d7-126">Kontakte hallatakse rakenduses Sales ning sünkroonitakse teenuse Common Data Service (CDS) ja rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="801d7-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="801d7-127">Kontakt rakenduses Sales saab kontaktiks CDS-is ja rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="801d7-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="801d7-128">Teise võimalusena saab see kontoks CDS-is ja kliendiks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="801d7-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="801d7-129">Selleks et määrata, kas kontakt tuleb võtta rakendusest Sales sünkroonimiseks CDS-i ja rakendusega Finance and Operations (näiteks kontaktid rakenduses Sales &gt; kontakt teenuses CDS &gt; kontaktid rakenduses Finance and Operations), vaatab süsteem rakenduse Sales kontakti puhul järgmisi atribuute:</span><span class="sxs-lookup"><span data-stu-id="801d7-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="801d7-130">**Sünkroonimine kontoga CDS-is ja kliendiga rakenduses Finance and Operations:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Jah**</span><span class="sxs-lookup"><span data-stu-id="801d7-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="801d7-131">**Sünkroonimine kontaktiga CDS-is ja kontaktiga rakenduses Finance and Operations:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Ei** ja **Ettevõte** (Peakonto/kontakt) osutab kontole (mitte kontaktile)</span><span class="sxs-lookup"><span data-stu-id="801d7-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="801d7-132">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="801d7-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="801d7-133">Kontaktile on lisatud uus väli **On aktiivne klient**.</span><span class="sxs-lookup"><span data-stu-id="801d7-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="801d7-134">Seda välja kasutatakse müügitegevusega kontaktide eristamiseks müügitellimuseta kontaktidest.</span><span class="sxs-lookup"><span data-stu-id="801d7-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="801d7-135">Suvandi **On aktiivne klient** sätteks on seatud **Jah** ainult kontaktide puhul, kellel on seotud pakkumisi, tellimusi või arveid.</span><span class="sxs-lookup"><span data-stu-id="801d7-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="801d7-136">Ainult need kontaktid sünkroonitakse rakendusega Finance and Operations klientidena.</span><span class="sxs-lookup"><span data-stu-id="801d7-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="801d7-137">Kontaktile on lisatud uus väli **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="801d7-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="801d7-138">Selle väljaga näidatakse, kas kontakt on lingitud ettevõttega (peakonto/kontakt), mille tüüp on **Konto**.</span><span class="sxs-lookup"><span data-stu-id="801d7-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="801d7-139">Seda teavet kasutatakse kontaktide tuvastamiseks, kes tuleb sünkroonida rakendusega Finance and Operations kontaktidena.</span><span class="sxs-lookup"><span data-stu-id="801d7-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="801d7-140">Kontaktile on lisatud uus väli **Kontakti number**, et tagada integratsiooni jaoks loomulik ja kordumatu võti.</span><span class="sxs-lookup"><span data-stu-id="801d7-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="801d7-141">Kui uus kontakt on loodud, luuakse numbriseeria abil automaatselt väärtus **Kontakti number**.</span><span class="sxs-lookup"><span data-stu-id="801d7-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="801d7-142">Väärtus sisaldab sõnet **CON**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide.</span><span class="sxs-lookup"><span data-stu-id="801d7-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="801d7-143">Näide: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="801d7-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="801d7-144">Kui rakendusele Sales on lisatud integratsioonilahendus, seab täiendusskript välja **Kontakti number** olemasolevatele kontaktidele, kasutades eespool kirjeldatud numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="801d7-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="801d7-145">Täiendusskript seab ka välja **On aktiivne klient** sätteks **Jah** kõigi müügitegevusega kontaktide puhul.</span><span class="sxs-lookup"><span data-stu-id="801d7-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="801d7-146">Rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="801d7-146">In Finance and Operations</span></span> 

<span data-ttu-id="801d7-147">Kontaktid sildistatakse atribuuti **IsContactPersonExternallyMaintained** kasutades.</span><span class="sxs-lookup"><span data-stu-id="801d7-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="801d7-148">See atribuut näitab, et kõnealust kontakti hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="801d7-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="801d7-149">Sellisel juhul hallatakse väliselt hallatavaid kontakte rakenduses Müük.</span><span class="sxs-lookup"><span data-stu-id="801d7-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="801d7-150">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="801d7-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="801d7-151">Kontakt kontaktiga</span><span class="sxs-lookup"><span data-stu-id="801d7-151">Contact to Contact</span></span>

- <span data-ttu-id="801d7-152">Värskendage välja **CDS-i organisatsiooni ID** vastenduses **Allikas &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="801d7-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="801d7-153">Malli vaikeväärtus atribuudi **Organization_OrganizationId [organisatsiooni ID]** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="801d7-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="801d7-154">Malli vaikeväärtus atribuudi **PrimaryAccount_Organization_OrganizationId [organisatsiooni ID]** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="801d7-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="801d7-155">Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav.</span><span class="sxs-lookup"><span data-stu-id="801d7-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="801d7-156">Sünkroonimistõrgete vältimiseks saate määrata vastenduses **CDS &gt; Toimingud** vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="801d7-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="801d7-157">Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="801d7-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="801d7-158">Atribuudi **PrimaryAddressCountryRegionISOCode** jaoks on malli vaikeväärtus **USA**.</span><span class="sxs-lookup"><span data-stu-id="801d7-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="801d7-159">Veenduge, et järgmise välja väärtus oleks rakenduses Finance and Operations olemas.</span><span class="sxs-lookup"><span data-stu-id="801d7-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="801d7-160">Kui teave pole rakenduses Finance and Operations nõutav, saate vastenduse vastendusest **CDS &gt; Sihtkoht** eemaldada.</span><span class="sxs-lookup"><span data-stu-id="801d7-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="801d7-161">**Välja nimi rakenduses Finance and Operations:** Otsus</span><span class="sxs-lookup"><span data-stu-id="801d7-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="801d7-162">**Vastendamine:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="801d7-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="801d7-163">Kontakt kliendiga</span><span class="sxs-lookup"><span data-stu-id="801d7-163">Contact to Customer</span></span>

- <span data-ttu-id="801d7-164">Värskendage välja **CDS-i organisatsiooni ID** vastenduses **Allikas &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="801d7-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="801d7-165">Malli vaikeväärtus atribuudi **Organization_OrganizationId [organisatsiooni ID]** puhul on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="801d7-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="801d7-166">Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav.</span><span class="sxs-lookup"><span data-stu-id="801d7-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="801d7-167">Sünkroonimistõrgete vältimiseks saate määrata vastenduses **CDS &gt; Sihtkoht** vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="801d7-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="801d7-168">Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="801d7-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="801d7-169">Atribuudi **PrimaryAddressCountryRegionISOCode** jaoks on malli vaikeväärtus **USA**.</span><span class="sxs-lookup"><span data-stu-id="801d7-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="801d7-170">Väli **CustomerGroup** on rakenduses Finance and Operations nõutav.</span><span class="sxs-lookup"><span data-stu-id="801d7-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="801d7-171">Sünkroonimistõrgete vältimiseks saate määrata vastenduses **CDS &gt; Sihtkoht** vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="801d7-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="801d7-172">Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="801d7-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="801d7-173">Atribuudi **CustomerGroupId** jaoks on malli vaikeväärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="801d7-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="801d7-174">Lisades järgmised vastendused vastendusest **CDS &gt; Sihtkoht**, saate vähendada rakenduses Finance and Operations olevate käsitsi värskenduste arvu.</span><span class="sxs-lookup"><span data-stu-id="801d7-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="801d7-175">Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.</span><span class="sxs-lookup"><span data-stu-id="801d7-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="801d7-176">**SiteId** – rakenduses Finance and Operations saab toodetele määrata ka vaikesaidi.</span><span class="sxs-lookup"><span data-stu-id="801d7-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="801d7-177">Sait on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="801d7-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="801d7-178">Malli väärtus atribuudile **SiteId** pole määratletud.</span><span class="sxs-lookup"><span data-stu-id="801d7-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="801d7-179">**WarehouseId** – rakenduses Finance and Operations saab toodetele määrata ka vaikelao.</span><span class="sxs-lookup"><span data-stu-id="801d7-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="801d7-180">Ladu on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="801d7-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="801d7-181">Malli väärtus atribuudile **WarehouseId** pole määratletud.</span><span class="sxs-lookup"><span data-stu-id="801d7-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="801d7-182">**LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="801d7-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="801d7-183">Malli vaikeväärtus atribuudi **LanguageId** puhul on **en-us**.</span><span class="sxs-lookup"><span data-stu-id="801d7-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="801d7-184">Malli vastendamine andmeintegraatoris</span><span class="sxs-lookup"><span data-stu-id="801d7-184">Template mapping in data integrator</span></span>

<span data-ttu-id="801d7-185">Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.</span><span class="sxs-lookup"><span data-stu-id="801d7-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="801d7-186">Kontakt kontaktiga</span><span class="sxs-lookup"><span data-stu-id="801d7-186">Contact to Contact</span></span>

![Malli vastendamine andmeintegraatoris](./media/contacts-template-mapping-data-integrator-1.png)

![Malli vastendamine kontaktide puhul andmeintegraatoris](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="801d7-189">Kontakt kliendiga</span><span class="sxs-lookup"><span data-stu-id="801d7-189">Contact to Customer</span></span>

![Malli vastendamine andmeintegraatoris](./media/contacts-template-mapping-data-integrator-3.png)

![Malli vastendamine kontaktide puhul andmeintegraatoris](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="801d7-192">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="801d7-192">Related topics</span></span>

[<span data-ttu-id="801d7-193">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="801d7-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="801d7-194">Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega</span><span class="sxs-lookup"><span data-stu-id="801d7-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="801d7-195">Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="801d7-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

