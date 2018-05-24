---
title: "Kuluobjekti kontrollijate pääsuõiguste määratlemine"
description: "See teema käsitleb kuluobjekti kontrollijate pääsuõigusi."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1cac3c3b724dda4ab39a65aa5221eda427767eb8
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="7ea79-103">Kuluobjekti kontrollija pääsuõigused</span><span class="sxs-lookup"><span data-stu-id="7ea79-103">Access rights of a cost object controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ea79-104">Tööruum **Kulude juhtimine** on keskne punkt, kus juhid saavad oma kuluobjektide toimivust vaadata.</span><span class="sxs-lookup"><span data-stu-id="7ea79-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="7ea79-105">See tööruum laseb juhtidel tarbida kuluarvestuse andmeid, isegi kui nad ei ole kuluarvestajad.</span><span class="sxs-lookup"><span data-stu-id="7ea79-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="7ea79-106">Turvalisuse huvides peaks juhtidel olema lubatud näha ainult neid kuluarvestuse andmeid, mis on seotud konkreetsete kuluobjektidega, mille eest nad vastutavad.</span><span class="sxs-lookup"><span data-stu-id="7ea79-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="7ea79-107">Kuluarvestuses on neli kordumatut rolli.</span><span class="sxs-lookup"><span data-stu-id="7ea79-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="7ea79-108">Rolli nimi</span><span class="sxs-lookup"><span data-stu-id="7ea79-108">Role name</span></span>               | <span data-ttu-id="7ea79-109">Litsents</span><span class="sxs-lookup"><span data-stu-id="7ea79-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="7ea79-110">Kuluarvestuse haldur</span><span class="sxs-lookup"><span data-stu-id="7ea79-110">Cost accounting manager</span></span> | <span data-ttu-id="7ea79-111">Tegevus</span><span class="sxs-lookup"><span data-stu-id="7ea79-111">Activity</span></span>     |
| <span data-ttu-id="7ea79-112">Kuluarvestaja</span><span class="sxs-lookup"><span data-stu-id="7ea79-112">Cost accountant</span></span>         | <span data-ttu-id="7ea79-113">Operations</span><span class="sxs-lookup"><span data-stu-id="7ea79-113">Operations</span></span>   |
| <span data-ttu-id="7ea79-114">Kuluarvestuse ametnik</span><span class="sxs-lookup"><span data-stu-id="7ea79-114">Cost accountant clerk</span></span>   | <span data-ttu-id="7ea79-115">Operations</span><span class="sxs-lookup"><span data-stu-id="7ea79-115">Operations</span></span>   |
| <span data-ttu-id="7ea79-116">Kuluobjekti kontroller</span><span class="sxs-lookup"><span data-stu-id="7ea79-116">Cost object controller</span></span>  | <span data-ttu-id="7ea79-117">Töörühma liikmed</span><span class="sxs-lookup"><span data-stu-id="7ea79-117">Team members</span></span> |

<span data-ttu-id="7ea79-118">Selles teemas selgitatakse, kuidas määrata juhile **kuluobjekti kontrollija** rolli.</span><span class="sxs-lookup"><span data-stu-id="7ea79-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="7ea79-119">Kui juhile on määratud **kuluobjekti kontrollija** roll, saab juht teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="7ea79-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="7ea79-120">Avage (kliendis) tööruum **Kulude juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="7ea79-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="7ea79-121">Saate minna süvitsi ja teil on vaatamiseks juurdepääs lehtedele, mis toetavad süvitsimineku kogemust.</span><span class="sxs-lookup"><span data-stu-id="7ea79-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="7ea79-122">Avage (mobiilirakenduses) tööruum **Kulude juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="7ea79-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="7ea79-123">Roll **Kuluobjekti kontrollija** ei kontrolli seda, millistele kuluobjektidele on kasutajal juurdepääs ja milliste andmeid ta vaadata saab.</span><span class="sxs-lookup"><span data-stu-id="7ea79-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="7ea79-124">Rea tasemel turvalisus tagatakse dimensioonihierarhiate ja juurdepääsuloendi hierarhia kaudu.</span><span class="sxs-lookup"><span data-stu-id="7ea79-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="7ea79-125">Pääsuõiguste andmine</span><span class="sxs-lookup"><span data-stu-id="7ea79-125">Grant access rights</span></span>
<span data-ttu-id="7ea79-126">Järgmine näide on selle kohta, milline dimensioonihierarhia välja võib näha.</span><span class="sxs-lookup"><span data-stu-id="7ea79-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="7ea79-127">**Dimensioonihierarhia üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="7ea79-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="7ea79-128">Dimensioonihierarhia nimi</span><span class="sxs-lookup"><span data-stu-id="7ea79-128">Dimension hierarchy name</span></span> | <span data-ttu-id="7ea79-129">Dimensioon</span><span class="sxs-lookup"><span data-stu-id="7ea79-129">Dimension</span></span>    | <span data-ttu-id="7ea79-130">Dimensiooni hierarhia tüübi nimi</span><span class="sxs-lookup"><span data-stu-id="7ea79-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="7ea79-131">Juurdepääsuloendi hierarhia</span><span class="sxs-lookup"><span data-stu-id="7ea79-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="7ea79-132">Organisatsioon</span><span class="sxs-lookup"><span data-stu-id="7ea79-132">Organization</span></span>             | <span data-ttu-id="7ea79-133">Kulukeskused</span><span class="sxs-lookup"><span data-stu-id="7ea79-133">Cost centers</span></span> | <span data-ttu-id="7ea79-134">Dimensiooni klassifitseerimishierarhia</span><span class="sxs-lookup"><span data-stu-id="7ea79-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="7ea79-135">**Jah**</span><span class="sxs-lookup"><span data-stu-id="7ea79-135">**Yes**</span></span>               |

<span data-ttu-id="7ea79-136">Võite kasutada hierarhiakujundajas kiirkaarti **Kasutajad** vähemalt ühe kasutaja ID sisestamiseks igasse sõlme.</span><span class="sxs-lookup"><span data-stu-id="7ea79-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="7ea79-137">Kasutajad</span><span class="sxs-lookup"><span data-stu-id="7ea79-137">Users</span></span>            | <span data-ttu-id="7ea79-138">Dimensiooniliikmete vahemikud</span><span class="sxs-lookup"><span data-stu-id="7ea79-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="7ea79-139">**Sõlmed**</span><span class="sxs-lookup"><span data-stu-id="7ea79-139">**Nodes**</span></span>                         | <span data-ttu-id="7ea79-140">**Kasutaja ID**</span><span class="sxs-lookup"><span data-stu-id="7ea79-140">**User ID**</span></span>      | <span data-ttu-id="7ea79-141">**Lähtedimensiooni liige**</span><span class="sxs-lookup"><span data-stu-id="7ea79-141">**From dimension member**</span></span> | <span data-ttu-id="7ea79-142">**Sihtdimensiooni liige**</span><span class="sxs-lookup"><span data-stu-id="7ea79-142">**To dimension member**</span></span> |
| <span data-ttu-id="7ea79-143">Organisatsioon</span><span class="sxs-lookup"><span data-stu-id="7ea79-143">Organization</span></span>                      | <span data-ttu-id="7ea79-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="7ea79-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="7ea79-145">&nbsp;&nbsp;Administraator</span><span class="sxs-lookup"><span data-stu-id="7ea79-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="7ea79-146">aprill</span><span class="sxs-lookup"><span data-stu-id="7ea79-146">April</span></span>            |                           |                         |
| <span data-ttu-id="7ea79-147">&nbsp;&nbsp;&nbsp;&nbsp;Finantsid</span><span class="sxs-lookup"><span data-stu-id="7ea79-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="7ea79-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="7ea79-148">Alicia</span></span>           | <span data-ttu-id="7ea79-149">CC002</span><span class="sxs-lookup"><span data-stu-id="7ea79-149">CC002</span></span>                     | <span data-ttu-id="7ea79-150">CC003</span><span class="sxs-lookup"><span data-stu-id="7ea79-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="7ea79-151">CC007</span><span class="sxs-lookup"><span data-stu-id="7ea79-151">CC007</span></span>                     | <span data-ttu-id="7ea79-152">CC007</span><span class="sxs-lookup"><span data-stu-id="7ea79-152">CC007</span></span>                   |
| <span data-ttu-id="7ea79-153">&nbsp;&nbsp;&nbsp;&nbsp;Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="7ea79-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="7ea79-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="7ea79-154">Arnie</span></span>            | <span data-ttu-id="7ea79-155">CC001</span><span class="sxs-lookup"><span data-stu-id="7ea79-155">CC001</span></span>                     | <span data-ttu-id="7ea79-156">CC001</span><span class="sxs-lookup"><span data-stu-id="7ea79-156">CC001</span></span>                   |
| <span data-ttu-id="7ea79-157">&nbsp;&nbsp;Tootmine</span><span class="sxs-lookup"><span data-stu-id="7ea79-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="7ea79-158">David</span><span class="sxs-lookup"><span data-stu-id="7ea79-158">David</span></span>            |                           |                         |
| <span data-ttu-id="7ea79-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakendamine</span><span class="sxs-lookup"><span data-stu-id="7ea79-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="7ea79-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="7ea79-160">Ellen</span></span>            | <span data-ttu-id="7ea79-161">CC005</span><span class="sxs-lookup"><span data-stu-id="7ea79-161">CC005</span></span>                     | <span data-ttu-id="7ea79-162">CC005</span><span class="sxs-lookup"><span data-stu-id="7ea79-162">CC005</span></span>                   |
| <span data-ttu-id="7ea79-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembler</span><span class="sxs-lookup"><span data-stu-id="7ea79-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="7ea79-164">Chris</span><span class="sxs-lookup"><span data-stu-id="7ea79-164">Chris</span></span>            | <span data-ttu-id="7ea79-165">CC006</span><span class="sxs-lookup"><span data-stu-id="7ea79-165">CC006</span></span>                     | <span data-ttu-id="7ea79-166">CC006</span><span class="sxs-lookup"><span data-stu-id="7ea79-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="7ea79-167">Kuluarvestajad tuleks määrata hierarhia ülemisele tasandile, et nad näeksid kuluarvestuses kõiki kirjeid.</span><span class="sxs-lookup"><span data-stu-id="7ea79-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="7ea79-168">Enne, kui juurdepääsuloendi hierarhiat ja selle turbesätteid rakendada saab, tuleb valiku **Luba kuvamise juurdepääs kuluobjekti dimensiooniliikmete jaoks** väärtuseks määrata **Jah** vahekaardil **Üldine** lehel **Kuluarvestuse parameetrid** (**Kuluarvestus** > **Seadistus** > **Parameetrid**).</span><span class="sxs-lookup"><span data-stu-id="7ea79-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="7ea79-169">Juurdepääsuloendi hierarhia sätteid kasutatakse järgmistel aladel kuvatavate andmete juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="7ea79-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="7ea79-170">**Kulude juhtimise** tööruum (kliendis):</span><span class="sxs-lookup"><span data-stu-id="7ea79-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="7ea79-171">Süvitsiminekuks kasutatavatel lehtedel olevad andmed</span><span class="sxs-lookup"><span data-stu-id="7ea79-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="7ea79-172">**Kulude juhtimise** tööruum (mobiilirakenduses):</span><span class="sxs-lookup"><span data-stu-id="7ea79-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="7ea79-173">Saldod kaartidel</span><span class="sxs-lookup"><span data-stu-id="7ea79-173">Balances in cards</span></span>

- <span data-ttu-id="7ea79-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="7ea79-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="7ea79-175">Power BI visualisatsioonidel kuvatavad andmed</span><span class="sxs-lookup"><span data-stu-id="7ea79-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="7ea79-176">Andmete Power BI visualisatsioonid, mis on manustatud rakenduse Microsoft Dynamics 365 for Finance and Operationsi klienti</span><span class="sxs-lookup"><span data-stu-id="7ea79-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="7ea79-177">Enne kui juurdepääsuloendi hierarhia saab Power BI-s olevaid andmeid mõjutada, tuleb juurdepääsuloendi hierarhia ja rea tasemel turve Power BI-s siduda.</span><span class="sxs-lookup"><span data-stu-id="7ea79-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="7ea79-178">Lisateavet leiate teemast [Kuluarvestuse sisupaketi jaoks turbe seadistamine](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="7ea79-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="7ea79-179">Selles teemas näidatakse eeltingimusi, mis peavad olema täidetud enne **kulude juhtimise** tööruumi kasutamist.</span><span class="sxs-lookup"><span data-stu-id="7ea79-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="7ea79-180">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7ea79-180">Additional resources</span></span>

- [<span data-ttu-id="7ea79-181">Kulujuhtimise tööruum</span><span class="sxs-lookup"><span data-stu-id="7ea79-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="7ea79-182">Dimensioonihierarhia</span><span class="sxs-lookup"><span data-stu-id="7ea79-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="7ea79-183">Kuluarvestuse sisupaketi turbe seadistamine</span><span class="sxs-lookup"><span data-stu-id="7ea79-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

