---
title: Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse üksuste Kontakt (kontaktid) ja Kontakt (kliendid) sünkroonimiseks rakendusest Dynamics 365 Sales rakendusse Dynamics 365 Supply Chain Management.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1a7f66797dea62a22d93ab105722bb26b4cf94e1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210107"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="c0711-103">Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="c0711-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c0711-104">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="c0711-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="c0711-105">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse üksuste Kontakt (kontaktid) ja Kontakt (kliendid) sünkroonimiseks rakendusest Dynamics 365 Sales otse rakendusse Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0711-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="c0711-106">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="c0711-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="c0711-107">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="c0711-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="c0711-108">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales.</span><span class="sxs-lookup"><span data-stu-id="c0711-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="c0711-109">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="c0711-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="c0711-110">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="c0711-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c0711-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="c0711-111">Templates and tasks</span></span>

<span data-ttu-id="c0711-112">Saadaolevatele mallidele juurdepääsemiseks avage [PowerAppsi administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="c0711-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="c0711-113">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="c0711-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c0711-114">Rakenduse Sales kontaktide (kontaktid) sünkroonimiseks rakenduse Supply Chain Management kontaktidega (kliendid)kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="c0711-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Supply Chain Management.</span></span>

- <span data-ttu-id="c0711-115">**Mallide nimed andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="c0711-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="c0711-116">Kontaktid (Salesist Supply Chain Managementi) – otsene</span><span class="sxs-lookup"><span data-stu-id="c0711-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="c0711-117">Klientide kontaktid (Salesist Supply Chain Managementi) – otsene</span><span class="sxs-lookup"><span data-stu-id="c0711-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="c0711-118">**Ülesannete nimed andmete integratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="c0711-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="c0711-119">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="c0711-119">Contacts</span></span>
    - <span data-ttu-id="c0711-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="c0711-120">ContactToCustomer</span></span>

<span data-ttu-id="c0711-121">Enne kontakti sünkroonimist on nõutav järgmine sünkroonimisülesanne: kontod (Salesist Supply Chain Managementi)</span><span class="sxs-lookup"><span data-stu-id="c0711-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="c0711-122">Üksuste komplektid</span><span class="sxs-lookup"><span data-stu-id="c0711-122">Entity sets</span></span>

| <span data-ttu-id="c0711-123">Müük</span><span class="sxs-lookup"><span data-stu-id="c0711-123">Sales</span></span>    | <span data-ttu-id="c0711-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c0711-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="c0711-125">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="c0711-125">Contacts</span></span> | <span data-ttu-id="c0711-126">CDS-i kontaktid</span><span class="sxs-lookup"><span data-stu-id="c0711-126">CDS Contacts</span></span>           |
| <span data-ttu-id="c0711-127">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="c0711-127">Contacts</span></span> | <span data-ttu-id="c0711-128">Kliendid V2</span><span class="sxs-lookup"><span data-stu-id="c0711-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="c0711-129">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="c0711-129">Entity flow</span></span>

<span data-ttu-id="c0711-130">Kontakte hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0711-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="c0711-131">Kontakt rakenduses Sales võib olla rakenduses Supply Chain Management kontakt või klient.</span><span class="sxs-lookup"><span data-stu-id="c0711-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="c0711-132">Selleks et välja uurida, kas rakenduse Sales kontakt tuleks sünkroonida rakendusega Supply Chain Management kontakti või kliendina, uurib süsteem rakenduses Sales kontakti järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="c0711-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="c0711-133">**Sünkroonimine kliendiga rakenduses Supply Chain Management:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Jah**</span><span class="sxs-lookup"><span data-stu-id="c0711-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="c0711-134">**Sünkroonimine kontaktiga rakenduses Supply Chain Management:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Ei** ja **Ettevõte** (peakonto/kontakt) osutab kontole (mitte kontaktile)</span><span class="sxs-lookup"><span data-stu-id="c0711-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c0711-135">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="c0711-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c0711-136">Kontaktile on lisatud uus väli **On aktiivne klient**.</span><span class="sxs-lookup"><span data-stu-id="c0711-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="c0711-137">Seda välja kasutatakse müügitegevusega kontaktide eristamiseks müügitellimuseta kontaktidest.</span><span class="sxs-lookup"><span data-stu-id="c0711-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="c0711-138">Suvandi **On aktiivne klient** sätteks on seatud **Jah** ainult kontaktide puhul, kellel on seotud pakkumisi, tellimusi või arveid.</span><span class="sxs-lookup"><span data-stu-id="c0711-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="c0711-139">Ainult need kontaktid sünkroonitakse rakendusega Supply Chain Management klientidena.</span><span class="sxs-lookup"><span data-stu-id="c0711-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="c0711-140">Kontaktile on lisatud uus väli **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="c0711-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="c0711-141">See väli näitab, kas kontakt on lingitud ettevõttega (peakonto/kontakt), mille tüüp on **Konto**.</span><span class="sxs-lookup"><span data-stu-id="c0711-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="c0711-142">Seda teavet kasutatakse kontaktide tuvastamiseks, kes tuleb sünkroonida rakendusega Supply Chain Management kontaktidena.</span><span class="sxs-lookup"><span data-stu-id="c0711-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="c0711-143">Kontaktile on lisatud uus väli **Kontakti number**, et tagada integratsiooni jaoks loomulik ja kordumatu võti.</span><span class="sxs-lookup"><span data-stu-id="c0711-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="c0711-144">Kui uus kontakt on loodud, luuakse numbriseeria abil automaatselt väärtus **Kontakti number**.</span><span class="sxs-lookup"><span data-stu-id="c0711-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="c0711-145">Väärtus sisaldab sõnet **CON**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide.</span><span class="sxs-lookup"><span data-stu-id="c0711-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="c0711-146">Näide: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="c0711-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="c0711-147">Kui rakendusele Sales on lisatud integratsioonilahendus, seab täiendusskript välja **Kontakti number** olemasolevatele kontaktidele, kasutades eespool mainitud numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="c0711-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="c0711-148">Täiendusskript seab ka välja **On aktiivne klient** sätteks **Jah** kõigi müügitegevusega kontaktide puhul.</span><span class="sxs-lookup"><span data-stu-id="c0711-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="c0711-149">Rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c0711-149">In Supply Chain Management</span></span>

<span data-ttu-id="c0711-150">Kontaktid sildistatakse atribuuti **IsContactPersonExternallyMaintained** kasutades.</span><span class="sxs-lookup"><span data-stu-id="c0711-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="c0711-151">See atribuut näitab, et kõnealust kontakti hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="c0711-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="c0711-152">Sellisel juhul hallatakse väliselt hallatavaid kontakte rakenduses Müük.</span><span class="sxs-lookup"><span data-stu-id="c0711-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c0711-153">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="c0711-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="c0711-154">Kontakt kliendiga</span><span class="sxs-lookup"><span data-stu-id="c0711-154">Contact to customer</span></span>

- <span data-ttu-id="c0711-155">**CustomerGroup** on nõutav Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="c0711-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="c0711-156">Sünkroonimistõrgete vältimiseks saate määrata vastenduses vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="c0711-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="c0711-157">Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="c0711-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="c0711-158">Malli vaikeväärtus on **10**.</span><span class="sxs-lookup"><span data-stu-id="c0711-158">The default template value is **10**.</span></span>

- <span data-ttu-id="c0711-159">Kui lisate järgmised vastendused, saate vähendada rakenduses Supply Chain Management nõutavate käsitsi värskenduste arvu.</span><span class="sxs-lookup"><span data-stu-id="c0711-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="c0711-160">Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.</span><span class="sxs-lookup"><span data-stu-id="c0711-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="c0711-161">**SiteId**: rakenduses Supply Chain Management saab toodetele määrata ka vaikesaidi.</span><span class="sxs-lookup"><span data-stu-id="c0711-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="c0711-162">Sait on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0711-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="c0711-163">Malli väärtus atribuudile **SiteId** pole määratletud.</span><span class="sxs-lookup"><span data-stu-id="c0711-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="c0711-164">**WarehouseId**: rakenduses Supply Chain Management saab toodetele määrata ka vaikelao.</span><span class="sxs-lookup"><span data-stu-id="c0711-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="c0711-165">Ladu on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0711-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="c0711-166">Malli väärtus atribuudile **WarehouseId** pole määratletud.</span><span class="sxs-lookup"><span data-stu-id="c0711-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="c0711-167">**LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0711-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="c0711-168">Malli vaikeväärtus on **en-us**.</span><span class="sxs-lookup"><span data-stu-id="c0711-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c0711-169">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="c0711-169">Template mapping in Data integration</span></span>

<span data-ttu-id="c0711-170">Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="c0711-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="c0711-171">Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0711-171">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="c0711-172">Kontakt kontaktiga</span><span class="sxs-lookup"><span data-stu-id="c0711-172">Contact to contact</span></span>

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="c0711-174">Kontakt kliendiga</span><span class="sxs-lookup"><span data-stu-id="c0711-174">Contact to customer</span></span>

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="c0711-176">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="c0711-176">Related topics</span></span>

[<span data-ttu-id="c0711-177">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="c0711-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="c0711-178">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="c0711-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="c0711-179">Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="c0711-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="c0711-180">Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel</span><span class="sxs-lookup"><span data-stu-id="c0711-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="c0711-181">Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="c0711-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


