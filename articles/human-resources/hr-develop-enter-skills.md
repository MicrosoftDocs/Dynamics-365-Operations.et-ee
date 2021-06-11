---
title: Sisestage oskused
description: Tööd ja haldurid saavad oskuseid sisestada rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076588"
---
# <a name="enter-skills"></a><span data-ttu-id="63c3c-103">Sisestage oskused</span><span class="sxs-lookup"><span data-stu-id="63c3c-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="63c3c-104">Saate sisestada töötajate, kandidaatide või kontaktisikute oodatavad oskused või tegelikud oskused rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63c3c-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="63c3c-105">Oodatav oskus on oskus, mille isik kavatseb omandada.</span><span class="sxs-lookup"><span data-stu-id="63c3c-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="63c3c-106">Tegelik oskus on oskus, mis isikul praegu on.</span><span class="sxs-lookup"><span data-stu-id="63c3c-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="63c3c-107">Töövoo loomine oskuste automaatseks kinnitamiseks</span><span class="sxs-lookup"><span data-stu-id="63c3c-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="63c3c-108">Oskuste sisestamiseks ilma kinnitamist nõudmata peate oskuste automaatseks kinnitamiseks looma töövoo.</span><span class="sxs-lookup"><span data-stu-id="63c3c-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="63c3c-109">Töötajate sisestatud oskused vajavad alati juhi kinnitust.</span><span class="sxs-lookup"><span data-stu-id="63c3c-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="63c3c-110">See töövoog kinnitab automaatselt ainult juhtide sisestatud oskused oma töötajate nimel.</span><span class="sxs-lookup"><span data-stu-id="63c3c-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="63c3c-111">Tööruumis **Personalihaldus** valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="63c3c-112">Jaotises **Seadistus** valige suvand **Inimressursside töövood**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="63c3c-113">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-113">Select **New**.</span></span>

4. <span data-ttu-id="63c3c-114">Valige **Loo töövoog** paanil väli **Töötaja oskused**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="63c3c-115">[![Töötaja oskuste töövoo valimine](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="63c3c-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="63c3c-116">**Ava see fail?** dialoogiboksis valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="63c3c-117">Kui teil palutakse, sisestage oma volitused.</span><span class="sxs-lookup"><span data-stu-id="63c3c-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="63c3c-118">Valige töövoo redaktoris **Kinnitage oskused** töövoo element ja lohistage see lõuendile.</span><span class="sxs-lookup"><span data-stu-id="63c3c-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="63c3c-119">[![Valige oskuste töövoo elemendi kinnitamine](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="63c3c-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="63c3c-120">Ühendage **Alusta** element **Kinnita oskused 1** elemendiga ja seejärel ühendage **Kinnita oskused 1** element elemendiga **Lõpp**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="63c3c-121">Võimalik, et peate elemendi **Lõpp** vaatamiseks alla kerima.</span><span class="sxs-lookup"><span data-stu-id="63c3c-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="63c3c-122">Saate seda lohistada teiste elementideni lähemal.</span><span class="sxs-lookup"><span data-stu-id="63c3c-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="63c3c-123">[![Ühendage töövoo elemendid](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="63c3c-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="63c3c-124">Topeltklõpsake **1Kinnita oskused 1** töövoo element ja paremklõpsake **Samm 1** element.</span><span class="sxs-lookup"><span data-stu-id="63c3c-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="63c3c-125">Paremklõpsake **Samm 1** element ja valige suvand **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="63c3c-126">**Atribuutide** aknas valige **Tingimus** vasakpoolsel navigeerimisribal.</span><span class="sxs-lookup"><span data-stu-id="63c3c-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="63c3c-127">Valige suvand **Käivita see samm üksnes siis, kui järgmine tingimus on täidetud**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="63c3c-128">Valige **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-128">Select **Add condition**.</span></span> <span data-ttu-id="63c3c-129">Pärast **Kus** käsku valige **Töötaja iseteenindusoskused** ja seejärel valige **Töötaja iseteenindusoskused. Isik**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="63c3c-130">Pärast **on** valige **väli** ja seejärel valige **Kasutaja suhe isikuga. Isik**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="63c3c-131">[![Määra tingimus](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="63c3c-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="63c3c-132">Valige **Määrang** vasaku käe navigeerimisribal.</span><span class="sxs-lookup"><span data-stu-id="63c3c-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="63c3c-133">Vahekaardil **Määrangu tüüp** valige **Hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="63c3c-134">Valige **Hierarhia valik** vahekaardil **Hierarhia tüüp:** väärtus **Juhtimishierarhia**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="63c3c-135">[![Määrake juhtimishierarhia](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="63c3c-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="63c3c-136">Valige **Sule** ja seejärel valige **Töövoog** lõuendi tööreas, siis valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="63c3c-137">Lisateavet töövoogudega töötamise kohta vt teemast [Töövoosüsteemi ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="63c3c-137">For more information about creating workflows, see [Workflow system overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="63c3c-138">Sisestage töötaja oskused</span><span class="sxs-lookup"><span data-stu-id="63c3c-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="63c3c-139">Vali töötaja.</span><span class="sxs-lookup"><span data-stu-id="63c3c-139">Select a worker.</span></span>

2. <span data-ttu-id="63c3c-140">Valige **Töötaja** lehel tegevusribalt **Isik** ja seejärel **Oskused**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="63c3c-141">Täitke **Oskused** lehel iga oskuse jaoks järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="63c3c-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="63c3c-142">**Oskus**: Valige oskus.</span><span class="sxs-lookup"><span data-stu-id="63c3c-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="63c3c-143">**Taseme tüüp**: Valige **Tegelik** oskus töötaja olemaoslevale oskusele või **Soovitud** oskus töötaja oskuse jaoks, mida ta sihib.</span><span class="sxs-lookup"><span data-stu-id="63c3c-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="63c3c-144">**Tase**: Valige töötaja oskuse tase.</span><span class="sxs-lookup"><span data-stu-id="63c3c-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="63c3c-145">**Taseme kuupäev**: Valimiseks klõpsake kalendris kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="63c3c-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="63c3c-146">**Kontrollija**: Vajadusel valige loendist soovitud kontrollija.</span><span class="sxs-lookup"><span data-stu-id="63c3c-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="63c3c-147">Saate otsingut filtreerida.</span><span class="sxs-lookup"><span data-stu-id="63c3c-147">You can filter your search.</span></span>
   - <span data-ttu-id="63c3c-148">**Kogemuse aasta**: Sisestage kogemuse aasta.</span><span class="sxs-lookup"><span data-stu-id="63c3c-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="63c3c-149">**Kinnitatud**: Kui oskus on kinnitatud, märkige ruut.</span><span class="sxs-lookup"><span data-stu-id="63c3c-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="63c3c-150">**Kinnitaja**: Sisestage kinnitaja nimi.</span><span class="sxs-lookup"><span data-stu-id="63c3c-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="63c3c-151">Kui olete oskuste sisestamise lõpetanud, valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="63c3c-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="63c3c-152">Vt ka</span><span class="sxs-lookup"><span data-stu-id="63c3c-152">See also</span></span>

[<span data-ttu-id="63c3c-153">Oskuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="63c3c-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="63c3c-154">Oskuste kaardimine</span><span class="sxs-lookup"><span data-stu-id="63c3c-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]