---
title: Hooldustoimingud
description: Kasutage hooldustoiminguid hooldustellimuse käigus täidetava ülesande kirjeldamiseks. Seda teavet näevad nii tehnikud kui ka kliendid.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2538a7b4a4c13a299afb37dd336f2f5d6f36a23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549836"
---
# <a name="service-tasks"></a><span data-ttu-id="b8836-104">Hooldustoimingud</span><span class="sxs-lookup"><span data-stu-id="b8836-104">Service tasks</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8836-105">Kasutage hooldustoiminguid hooldustellimuse käigus täidetava ülesande kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="b8836-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="b8836-106">Seda teavet näevad nii tehnikud kui ka kliendid.</span><span class="sxs-lookup"><span data-stu-id="b8836-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="b8836-107">Hooldustoimingute loomine toimub lehel **Hooldustoimingud** ning te seostate hooldustoimingud kindla hooldusleppe või hooldustellimusega, luues hooldustoimingu seose.</span><span class="sxs-lookup"><span data-stu-id="b8836-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="b8836-108">Iga kord, kui loote hooldustoimingu seose, saate luua järgmise.</span><span class="sxs-lookup"><span data-stu-id="b8836-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="b8836-109">Sisemärkused ülesande kohta, nagu detailsed tehnilised nõudmised ülesandele, mida tehnikul on vaja teada.</span><span class="sxs-lookup"><span data-stu-id="b8836-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="b8836-110">Välised märkused, mida klient näeb.</span><span class="sxs-lookup"><span data-stu-id="b8836-110">External notes that the customer can see.</span></span> <span data-ttu-id="b8836-111">Need võivad anda töös oleva ülesande kohta vähem tehnilise selgituse vastavalt kokkuleppele kliendi ja hooldusettevõtte vahel.</span><span class="sxs-lookup"><span data-stu-id="b8836-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="b8836-112">Kui olete loonud hooldustoimingu seose hooldustoimingu ja hooldustellimuse vahel, saate täpsustada seda hooldustoimingut, kui loote hooldustellimusele või hooldusleppele ridu.</span><span class="sxs-lookup"><span data-stu-id="b8836-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="b8836-113">Kui loote hooldustellimusi hooldusleppe põhjal, siis saate kasutada hooldustoiminguid, mis on määratud igale hooldusleppe reale hooldustellimuse ridade grupeerimiseks hooldustellimustesse.</span><span class="sxs-lookup"><span data-stu-id="b8836-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="b8836-114">Hooldustoimingute loomine</span><span class="sxs-lookup"><span data-stu-id="b8836-114">Create a service task</span></span>

1. <span data-ttu-id="b8836-115">Klõpsake valikul **Hooldushaldus** \> **Häälestus** \> **Hooldustoimingud**.</span><span class="sxs-lookup"><span data-stu-id="b8836-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="b8836-116">Looge uus rida.</span><span class="sxs-lookup"><span data-stu-id="b8836-116">Create a new line.</span></span>
3. <span data-ttu-id="b8836-117">Sisestage teenuse ID ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b8836-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="b8836-118">Näide</span><span class="sxs-lookup"><span data-stu-id="b8836-118">Example</span></span>

<span data-ttu-id="b8836-119">Tehnikul on vaja täita kaks tööülesannet käigukasti juures (teenusobjekt GB-1234) kliendi asukohas.</span><span class="sxs-lookup"><span data-stu-id="b8836-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="b8836-120">Kliendile luuakse hoolduslepe ja tööülesannetega seostatakse mitu kannet.</span><span class="sxs-lookup"><span data-stu-id="b8836-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="b8836-121">Hoolduslepe ja leppe read kahe tööülesande kohta on järgmised.</span><span class="sxs-lookup"><span data-stu-id="b8836-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="b8836-122">Hoolduslepe</span><span class="sxs-lookup"><span data-stu-id="b8836-122">Service agreement</span></span>

| <span data-ttu-id="b8836-123">Projekt</span><span class="sxs-lookup"><span data-stu-id="b8836-123">Project</span></span> | <span data-ttu-id="b8836-124">Hoolduslepe</span><span class="sxs-lookup"><span data-stu-id="b8836-124">Service agreement</span></span> | <span data-ttu-id="b8836-125">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b8836-125">Description</span></span>                                  | <span data-ttu-id="b8836-126">Grupeeri</span><span class="sxs-lookup"><span data-stu-id="b8836-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="b8836-127">9012</span><span class="sxs-lookup"><span data-stu-id="b8836-127">9012</span></span>    | <span data-ttu-id="b8836-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="b8836-128">000008\_001</span></span>       | <span data-ttu-id="b8836-129">Kontroll ja rutiinne asendamine – GB-1234</span><span class="sxs-lookup"><span data-stu-id="b8836-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="b8836-130">Preemia</span><span class="sxs-lookup"><span data-stu-id="b8836-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="b8836-131">Hooldusleppe read</span><span class="sxs-lookup"><span data-stu-id="b8836-131">Service agreement lines</span></span>

| <span data-ttu-id="b8836-132">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b8836-132">Description</span></span>             | <span data-ttu-id="b8836-133">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="b8836-133">Transaction type</span></span> | <span data-ttu-id="b8836-134">Teenuse objekt</span><span class="sxs-lookup"><span data-stu-id="b8836-134">Service object</span></span> | <span data-ttu-id="b8836-135">Hooldustoiming</span><span class="sxs-lookup"><span data-stu-id="b8836-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="b8836-136">Kontrollimine ja puhastamine</span><span class="sxs-lookup"><span data-stu-id="b8836-136">Inspection and cleaning</span></span> | <span data-ttu-id="b8836-137">Tund</span><span class="sxs-lookup"><span data-stu-id="b8836-137">Hour</span></span>             | <span data-ttu-id="b8836-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="b8836-138">GB-1234</span></span>        | <span data-ttu-id="b8836-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-139">I/C - GB1234</span></span> |
| <span data-ttu-id="b8836-140">Reisimine</span><span class="sxs-lookup"><span data-stu-id="b8836-140">Travel</span></span>                  | <span data-ttu-id="b8836-141">Expense</span><span class="sxs-lookup"><span data-stu-id="b8836-141">Expense</span></span>          | <span data-ttu-id="b8836-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="b8836-142">GB-1234</span></span>        | <span data-ttu-id="b8836-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-143">I/C - GB1234</span></span> |
| <span data-ttu-id="b8836-144">Materjalid</span><span class="sxs-lookup"><span data-stu-id="b8836-144">Materials</span></span>               | <span data-ttu-id="b8836-145">Kaup</span><span class="sxs-lookup"><span data-stu-id="b8836-145">Item</span></span>             | <span data-ttu-id="b8836-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="b8836-146">GB-1234</span></span>        | <span data-ttu-id="b8836-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-147">I/C - GB1234</span></span> |
| <span data-ttu-id="b8836-148">Rutiinne asendamine</span><span class="sxs-lookup"><span data-stu-id="b8836-148">Routine replacement</span></span>     | <span data-ttu-id="b8836-149">Tund</span><span class="sxs-lookup"><span data-stu-id="b8836-149">Hour</span></span>             | <span data-ttu-id="b8836-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="b8836-150">GB-1234</span></span>        | <span data-ttu-id="b8836-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-151">RR - GB1234</span></span>  |
| <span data-ttu-id="b8836-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="b8836-152">GR-1</span></span>                    | <span data-ttu-id="b8836-153">Kaup</span><span class="sxs-lookup"><span data-stu-id="b8836-153">Item</span></span>             | <span data-ttu-id="b8836-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="b8836-154">GB-1234</span></span>        | <span data-ttu-id="b8836-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-155">RR - GB1234</span></span>  |
| <span data-ttu-id="b8836-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="b8836-156">GR-5</span></span>                    | <span data-ttu-id="b8836-157">Kaup</span><span class="sxs-lookup"><span data-stu-id="b8836-157">Item</span></span>             | <span data-ttu-id="b8836-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="b8836-158">GB-1234</span></span>        | <span data-ttu-id="b8836-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-159">RR - GB1234</span></span>  |

<span data-ttu-id="b8836-160">Kahe tööülesande hooldusleppe ridadele on lisatud kaks hooldustoimingut.</span><span class="sxs-lookup"><span data-stu-id="b8836-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="b8836-161">Hooldustoimingud määravad kanded, mis iga tööülesande alla kuuluvad.</span><span class="sxs-lookup"><span data-stu-id="b8836-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="b8836-162">Esimesel juhul näitab hooldustoiming I/C - GB1234 kõiki hooldusleppe ridu, mis on seotud objekti GB-1234 kontrollimise ja puhastamisega.</span><span class="sxs-lookup"><span data-stu-id="b8836-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="b8836-163">Teisel juhul näitab hooldustoiming RR - GB1234 kõiki hooldusleppe ridu, mis on seotud rutiinse asendamisega.</span><span class="sxs-lookup"><span data-stu-id="b8836-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="b8836-164">Hooldustoimingu seosed, mis ühendavad hooldustoiminguid kindla leppega, on järgmised.</span><span class="sxs-lookup"><span data-stu-id="b8836-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="b8836-165">teenustoimingud</span><span class="sxs-lookup"><span data-stu-id="b8836-165">Service tasks</span></span>

| <span data-ttu-id="b8836-166">teenustoiming</span><span class="sxs-lookup"><span data-stu-id="b8836-166">Service task</span></span> | <span data-ttu-id="b8836-167">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b8836-167">Description</span></span>                             | <span data-ttu-id="b8836-168">sisemärkus</span><span class="sxs-lookup"><span data-stu-id="b8836-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="b8836-169">väline märkus</span><span class="sxs-lookup"><span data-stu-id="b8836-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="b8836-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-170">I/C - GB1234</span></span> | <span data-ttu-id="b8836-171">Käigukasti GB-1234 kontrollimine</span><span class="sxs-lookup"><span data-stu-id="b8836-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="b8836-172">Käigukasti GB-1234 visuaalne ja mehaaniline kontrollimine ja puhastamine</span><span class="sxs-lookup"><span data-stu-id="b8836-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="b8836-173">Käigukasti rutiinne kontrollimine</span><span class="sxs-lookup"><span data-stu-id="b8836-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="b8836-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="b8836-174">RR - GB1234</span></span>  | <span data-ttu-id="b8836-175">GB-1234 osade rutiinne asendamine</span><span class="sxs-lookup"><span data-stu-id="b8836-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="b8836-176">Rutiinse teenuse käigus GR-1 ja GR-5 komponentide asendamine (enne 2002. aastat valmistatud käigukastide puhul asendatakse ka GR-2 komponent)</span><span class="sxs-lookup"><span data-stu-id="b8836-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="b8836-177">Rutiinne osade asendamine</span><span class="sxs-lookup"><span data-stu-id="b8836-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="b8836-178">Hooldustellimuste grupeerimine</span><span class="sxs-lookup"><span data-stu-id="b8836-178">Group service orders</span></span>

<span data-ttu-id="b8836-179">Kui loote automaatselt hooldustellimusi, siis saate kasutada hooldustoimingut grupeerimise kriteeriumina.</span><span class="sxs-lookup"><span data-stu-id="b8836-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="b8836-180">Hooldustoimingute grupeerimiseks määrake hooldusleppes, et hooldusleppel põhinevad hooldustellimused tuleb grupeerida hooldustoimingu ID järgi, mis on nende esmane grupeerimiskriteerium.</span><span class="sxs-lookup"><span data-stu-id="b8836-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="b8836-181">**Grupeerimine hooldustoimingute kaupa**</span><span class="sxs-lookup"><span data-stu-id="b8836-181">**Group by service task**</span></span>

1. <span data-ttu-id="b8836-182">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="b8836-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="b8836-183">Vahekaardil **Häälestus** valige väljal **Hooldustellimuste ühendamine** valik **Hooldustoimingu alusel**.</span><span class="sxs-lookup"><span data-stu-id="b8836-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


