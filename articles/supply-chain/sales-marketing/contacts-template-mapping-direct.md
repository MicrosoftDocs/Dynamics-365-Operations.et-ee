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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994040"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="4182b-103">Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="4182b-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="4182b-104">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="4182b-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="4182b-105">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse tabelites Kontakt (kontaktid) ja Kontakt (kliendid) sünkroonimiseks rakendusest Dynamics 365 Sales otse rakendusse Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4182b-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="4182b-106">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="4182b-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="4182b-107">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="4182b-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="4182b-108">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales.</span><span class="sxs-lookup"><span data-stu-id="4182b-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="4182b-109">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="4182b-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="4182b-110">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="4182b-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4182b-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="4182b-111">Templates and tasks</span></span>

<span data-ttu-id="4182b-112">Saadaolevatele mallidele juurdepääsemiseks avage [PowerAppsi administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="4182b-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="4182b-113">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="4182b-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4182b-114">Rakenduse Sales tabeli Kontaktid (kontaktid) sünkroonimiseks rakenduse Supply Chain Management tabelisse Kontaktid (kliendid) kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="4182b-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="4182b-115">**Mallide nimed andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="4182b-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="4182b-116">Kontaktid (Salesist Supply Chain Managementi) – otsene</span><span class="sxs-lookup"><span data-stu-id="4182b-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="4182b-117">Klientide kontaktid (Salesist Supply Chain Managementi) – otsene</span><span class="sxs-lookup"><span data-stu-id="4182b-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="4182b-118">**Ülesannete nimed andmete integratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="4182b-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="4182b-119">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="4182b-119">Contacts</span></span>
    - <span data-ttu-id="4182b-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="4182b-120">ContactToCustomer</span></span>

<span data-ttu-id="4182b-121">Enne kontakti sünkroonimist on nõutav järgmine sünkroonimisülesanne: kontod (Salesist Supply Chain Managementi)</span><span class="sxs-lookup"><span data-stu-id="4182b-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="4182b-122">Üksuste komplektid</span><span class="sxs-lookup"><span data-stu-id="4182b-122">Entity sets</span></span>

| <span data-ttu-id="4182b-123">Müük</span><span class="sxs-lookup"><span data-stu-id="4182b-123">Sales</span></span>    | <span data-ttu-id="4182b-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4182b-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="4182b-125">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="4182b-125">Contacts</span></span> | <span data-ttu-id="4182b-126">Dataverse’i kontaktid</span><span class="sxs-lookup"><span data-stu-id="4182b-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="4182b-127">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="4182b-127">Contacts</span></span> | <span data-ttu-id="4182b-128">Kliendid V2</span><span class="sxs-lookup"><span data-stu-id="4182b-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="4182b-129">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="4182b-129">Entity flow</span></span>

<span data-ttu-id="4182b-130">Kontakte hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4182b-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="4182b-131">Kontakt rakenduses Sales võib olla rakenduses Supply Chain Management kontakt või klient.</span><span class="sxs-lookup"><span data-stu-id="4182b-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="4182b-132">Selleks et välja uurida, kas rakenduse Sales kontakt tuleks sünkroonida rakendusega Supply Chain Management kontakti või kliendina, uurib süsteem rakenduses Sales kontakti järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="4182b-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="4182b-133">**Sünkroonimine kliendiga rakenduses Supply Chain Management:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Jah**</span><span class="sxs-lookup"><span data-stu-id="4182b-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="4182b-134">**Sünkroonimine kontaktiga rakenduses Supply Chain Management:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Ei** ja **Ettevõte** (peakonto/kontakt) osutab kontole (mitte kontaktile)</span><span class="sxs-lookup"><span data-stu-id="4182b-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4182b-135">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="4182b-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4182b-136">Kontaktile on lisatud uus veerg **On aktiivne klient**.</span><span class="sxs-lookup"><span data-stu-id="4182b-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="4182b-137">Seda veergu kasutatakse müügitegevusega kontaktide eristamiseks müügitellimuseta kontaktidest.</span><span class="sxs-lookup"><span data-stu-id="4182b-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="4182b-138">Suvandi **On aktiivne klient** sätteks on seatud **Jah** ainult kontaktide puhul, kellel on seotud pakkumisi, tellimusi või arveid.</span><span class="sxs-lookup"><span data-stu-id="4182b-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="4182b-139">Ainult need kontaktid sünkroonitakse rakendusega Supply Chain Management klientidena.</span><span class="sxs-lookup"><span data-stu-id="4182b-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="4182b-140">Kontaktile on lisatud uus veerg **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="4182b-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="4182b-141">See veerg näitab, kas kontakt on lingitud ettevõttega (peakonto/kontakt), mille tüüp on **Konto**.</span><span class="sxs-lookup"><span data-stu-id="4182b-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="4182b-142">Seda teavet kasutatakse kontaktide tuvastamiseks, kes tuleb sünkroonida rakendusega Supply Chain Management kontaktidena.</span><span class="sxs-lookup"><span data-stu-id="4182b-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="4182b-143">Kontaktile on lisatud uus veerg **Kontakti number**, et tagada integratsiooni jaoks loomulik ja kordumatu võti.</span><span class="sxs-lookup"><span data-stu-id="4182b-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="4182b-144">Kui uus kontakt on loodud, luuakse numbriseeria abil automaatselt väärtus **Kontakti number**.</span><span class="sxs-lookup"><span data-stu-id="4182b-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="4182b-145">Väärtus sisaldab sõnet **CON**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide.</span><span class="sxs-lookup"><span data-stu-id="4182b-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="4182b-146">Näide: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="4182b-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="4182b-147">Kui rakendusele Sales on lisatud integratsioonilahendus, seab täiendusskript veeru **Kontakti number** olemasolevatele kontaktidele, kasutades eespool mainitud numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="4182b-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="4182b-148">Täiendusskript seab ka veeru **On aktiivne klient** sätteks **Jah** kõigi müügitegevusega kontaktide puhul.</span><span class="sxs-lookup"><span data-stu-id="4182b-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="4182b-149">Rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4182b-149">In Supply Chain Management</span></span>

<span data-ttu-id="4182b-150">Kontaktid sildistatakse atribuuti **IsContactPersonExternallyMaintained** kasutades.</span><span class="sxs-lookup"><span data-stu-id="4182b-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="4182b-151">See atribuut näitab, et kõnealust kontakti hallatakse väliselt.</span><span class="sxs-lookup"><span data-stu-id="4182b-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="4182b-152">Sellisel juhul hallatakse väliselt hallatavaid kontakte rakenduses Müük.</span><span class="sxs-lookup"><span data-stu-id="4182b-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4182b-153">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="4182b-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="4182b-154">Kontakt kliendiga</span><span class="sxs-lookup"><span data-stu-id="4182b-154">Contact to customer</span></span>

- <span data-ttu-id="4182b-155">**CustomerGroup** on nõutav Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="4182b-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="4182b-156">Sünkroonimistõrgete vältimiseks saate määrata vastenduses vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="4182b-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="4182b-157">Sel juhul kasutatakse seda vaikeväärtust, kui veerg on rakenduses Sales tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="4182b-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="4182b-158">Malli vaikeväärtus on **10**.</span><span class="sxs-lookup"><span data-stu-id="4182b-158">The default template value is **10**.</span></span>

- <span data-ttu-id="4182b-159">Kui lisate järgmised vastendused, saate vähendada rakenduses Supply Chain Management nõutavate käsitsi värskenduste arvu.</span><span class="sxs-lookup"><span data-stu-id="4182b-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="4182b-160">Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.</span><span class="sxs-lookup"><span data-stu-id="4182b-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="4182b-161">**SiteId**: rakenduses Supply Chain Management saab toodetele määrata ka vaikesaidi.</span><span class="sxs-lookup"><span data-stu-id="4182b-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="4182b-162">Sait on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4182b-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="4182b-163">Malli väärtus atribuudile **SiteId** pole määratletud.</span><span class="sxs-lookup"><span data-stu-id="4182b-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="4182b-164">**WarehouseId**: rakenduses Supply Chain Management saab toodetele määrata ka vaikelao.</span><span class="sxs-lookup"><span data-stu-id="4182b-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="4182b-165">Ladu on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4182b-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="4182b-166">Malli väärtus atribuudile **WarehouseId** pole määratletud.</span><span class="sxs-lookup"><span data-stu-id="4182b-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="4182b-167">**LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4182b-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="4182b-168">Malli vaikeväärtus on **en-us**.</span><span class="sxs-lookup"><span data-stu-id="4182b-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4182b-169">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="4182b-169">Template mapping in Data integration</span></span>

<span data-ttu-id="4182b-170">Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="4182b-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="4182b-171">Vastendamine näitab, millise veeru teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4182b-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="4182b-172">Kontakt kontaktiga</span><span class="sxs-lookup"><span data-stu-id="4182b-172">Contact to contact</span></span>

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="4182b-174">Kontakt kliendiga</span><span class="sxs-lookup"><span data-stu-id="4182b-174">Contact to customer</span></span>

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="4182b-176">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="4182b-176">Related topics</span></span>

[<span data-ttu-id="4182b-177">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="4182b-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="4182b-178">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="4182b-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="4182b-179">Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="4182b-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="4182b-180">Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel</span><span class="sxs-lookup"><span data-stu-id="4182b-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="4182b-181">Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="4182b-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


