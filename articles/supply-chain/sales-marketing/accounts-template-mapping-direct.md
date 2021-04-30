---
title: Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks rakendusest Dynamics 365 Sales rakendusse Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fff9171966045e9dad5f2c70087a568cfa075e43
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908128"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="aa81d-103">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="aa81d-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="aa81d-104">Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="aa81d-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="aa81d-105">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks otse rakendusest Dynamics 365 Sales rakendusse Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="aa81d-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="aa81d-106">Andmevoog lahenduses Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="aa81d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="aa81d-107">Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="aa81d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="aa81d-108">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales.</span><span class="sxs-lookup"><span data-stu-id="aa81d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="aa81d-109">Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="aa81d-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="aa81d-110">[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="aa81d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="aa81d-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="aa81d-111">Templates and tasks</span></span>

<span data-ttu-id="aa81d-112">Saadaolevatele mallidele juurdepääsemiseks avage [Power Apps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="aa81d-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="aa81d-113">Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="aa81d-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="aa81d-114">Kontode sünkroonimiseks rakendusest Sales rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="aa81d-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="aa81d-115">**Andmete integratsioon malli nimi:** Kontod (rakendusest Sales rakendusse Fin and Ops) – otse</span><span class="sxs-lookup"><span data-stu-id="aa81d-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="aa81d-116">**Ülesande nimi projektis:** Kontod – Kliendid</span><span class="sxs-lookup"><span data-stu-id="aa81d-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="aa81d-117">Enne konto/kliendi sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.</span><span class="sxs-lookup"><span data-stu-id="aa81d-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="aa81d-118">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="aa81d-118">Entity set</span></span>

| <span data-ttu-id="aa81d-119">Müük</span><span class="sxs-lookup"><span data-stu-id="aa81d-119">Sales</span></span>    | <span data-ttu-id="aa81d-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="aa81d-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="aa81d-121">Kontod</span><span class="sxs-lookup"><span data-stu-id="aa81d-121">Accounts</span></span> | <span data-ttu-id="aa81d-122">Kliendid V2</span><span class="sxs-lookup"><span data-stu-id="aa81d-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="aa81d-123">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="aa81d-123">Entity flow</span></span>

<span data-ttu-id="aa81d-124">Kontosid hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Supply Chain Management klientidena.</span><span class="sxs-lookup"><span data-stu-id="aa81d-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="aa81d-125">Nende klientide atribuudi **On väliselt hallatav** sätteks on määratud **Jah**, et jälgida rakendusest Sales pärit kliente.</span><span class="sxs-lookup"><span data-stu-id="aa81d-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="aa81d-126">Arveldamise ajal kasutatakse seda teavet rakendusega Sales sünkroonitud arvete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="aa81d-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="aa81d-127">Lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="aa81d-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="aa81d-128">Veerg **Konto number** on saadaval lehel **Konto**.</span><span class="sxs-lookup"><span data-stu-id="aa81d-128">The **Account Number** column is available on the **Account** page.</span></span> <span data-ttu-id="aa81d-129">See on loomulik ja kordumatu võti, et toetada integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="aa81d-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="aa81d-130">Kliendisuhete halduse (CRM) lahenduse loomuliku võtme funktsioon võib mõjutada kliente, kes juba kasutavad veergu **Konto number**, kuid ei kasuta iga konto puhul atribuudi **Konto number** kordumatuid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="aa81d-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** column, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="aa81d-131">Praegu ei toeta integratsioonilahendus seda juhtumit.</span><span class="sxs-lookup"><span data-stu-id="aa81d-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="aa81d-132">Kui uue konto loomisel ei ole atribuudi **Konto number** väärtust veel olemas, luuakse see automaatselt numbriseeriat kasutades.</span><span class="sxs-lookup"><span data-stu-id="aa81d-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="aa81d-133">Väärtus sisaldab sõnet **ACC**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide.</span><span class="sxs-lookup"><span data-stu-id="aa81d-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="aa81d-134">Näide: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="aa81d-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="aa81d-135">Kui rakendatakse integratsioonilahendust rakendusele Sales, seab täiendusskript veeru **Konto number** olemasolevatele kontodele rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="aa81d-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** column for existing accounts in Sales.</span></span> <span data-ttu-id="aa81d-136">Kui ühtki atribuudi **Konto number** väärtust ei ole, kasutatakse varem mainitud numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="aa81d-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="aa81d-137">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="aa81d-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="aa81d-138">Atribuudi **CustomerGroupId** vastendust tuleb värskendada rakenduses Supply Chain Management kehtivale väärtusele.</span><span class="sxs-lookup"><span data-stu-id="aa81d-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="aa81d-139">Saate määrata vaikeväärtuse või määrata väärtuse väärtuskaardi abil.</span><span class="sxs-lookup"><span data-stu-id="aa81d-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="aa81d-140">Malli vaikeväärtus on **10**.</span><span class="sxs-lookup"><span data-stu-id="aa81d-140">The default template value is **10**.</span></span>

- <span data-ttu-id="aa81d-141">Kui lisate järgmised vastendused, saate vähendada rakenduses Supply Chain Management nõutavate käsitsi värskenduste arvu.</span><span class="sxs-lookup"><span data-stu-id="aa81d-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="aa81d-142">Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.</span><span class="sxs-lookup"><span data-stu-id="aa81d-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="aa81d-143">**SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="aa81d-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="aa81d-144">Vaikesaidi võib võtta kas tootelt või kliendilt tellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="aa81d-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="aa81d-145">Malli vaikeväärtus on **1**.</span><span class="sxs-lookup"><span data-stu-id="aa81d-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="aa81d-146">**WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="aa81d-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="aa81d-147">Vaikelao võib võtta kas tootelt või kliendilt tellimuse päises rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="aa81d-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="aa81d-148">Malli vaikeväärtus on **13**.</span><span class="sxs-lookup"><span data-stu-id="aa81d-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="aa81d-149">**LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="aa81d-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="aa81d-150">Vaikimisi kasutatakse kliendilt saadud tellimuse päises olevat keelt.</span><span class="sxs-lookup"><span data-stu-id="aa81d-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="aa81d-151">Malli vaikeväärtus on **en-us**.</span><span class="sxs-lookup"><span data-stu-id="aa81d-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="aa81d-152">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="aa81d-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="aa81d-153">Veerud **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa.</span><span class="sxs-lookup"><span data-stu-id="aa81d-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't included in the default mappings.</span></span> <span data-ttu-id="aa81d-154">Nende veergude vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel tabelit sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="aa81d-154">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synchronized between.</span></span>

<span data-ttu-id="aa81d-155">Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="aa81d-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="aa81d-156">Vastendamine näitab, millise veeru teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="aa81d-156">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

![Malli vastendamine andmete integratsioonis](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="aa81d-158">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="aa81d-158">Related topics</span></span>


[<span data-ttu-id="aa81d-159">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="aa81d-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="aa81d-160">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="aa81d-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="aa81d-161">Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="aa81d-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="aa81d-162">Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel</span><span class="sxs-lookup"><span data-stu-id="aa81d-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="aa81d-163">Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="aa81d-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]