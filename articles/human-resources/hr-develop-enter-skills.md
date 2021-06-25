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
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193973"
---
# <a name="enter-skills"></a><span data-ttu-id="278a4-103">Sisestage oskused</span><span class="sxs-lookup"><span data-stu-id="278a4-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="278a4-104">Saate sisestada töötajate, kandidaatide või kontaktisikute oodatavad oskused või tegelikud oskused rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="278a4-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="278a4-105">Oodatav oskus on oskus, mille isik kavatseb omandada.</span><span class="sxs-lookup"><span data-stu-id="278a4-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="278a4-106">Tegelik oskus on oskus, mis isikul praegu on.</span><span class="sxs-lookup"><span data-stu-id="278a4-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="278a4-107">Töövoo loomine oskuste automaatseks kinnitamiseks</span><span class="sxs-lookup"><span data-stu-id="278a4-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="278a4-108">Oskuste sisestamiseks ilma kinnitamist nõudmata peate oskuste automaatseks kinnitamiseks looma töövoo.</span><span class="sxs-lookup"><span data-stu-id="278a4-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="278a4-109">Töötajate sisestatud oskused vajavad alati juhi kinnitust.</span><span class="sxs-lookup"><span data-stu-id="278a4-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="278a4-110">See töövoog kinnitab automaatselt ainult juhtide sisestatud oskused oma töötajate nimel.</span><span class="sxs-lookup"><span data-stu-id="278a4-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="278a4-111">Tööruumis **Personalihaldus** valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="278a4-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="278a4-112">Jaotises **Seadistus** valige suvand **Inimressursside töövood**.</span><span class="sxs-lookup"><span data-stu-id="278a4-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="278a4-113">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="278a4-113">Select **New**.</span></span>

4. <span data-ttu-id="278a4-114">Valige **Loo töövoog** paanil väli **Töötaja oskused**.</span><span class="sxs-lookup"><span data-stu-id="278a4-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="278a4-115">[![Töötaja oskuste töövoo valimine](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="278a4-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="278a4-116">**Ava see fail?** dialoogiboksis valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="278a4-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="278a4-117">Kui teil palutakse, sisestage oma volitused.</span><span class="sxs-lookup"><span data-stu-id="278a4-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="278a4-118">Valige töövoo redaktoris **Kinnitage oskused** töövoo element ja lohistage see lõuendile.</span><span class="sxs-lookup"><span data-stu-id="278a4-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="278a4-119">[![Valige oskuste töövoo elemendi kinnitamine](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="278a4-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="278a4-120">Ühendage **Alusta** element **Kinnita oskused 1** elemendiga ja seejärel ühendage **Kinnita oskused 1** element elemendiga **Lõpp**.</span><span class="sxs-lookup"><span data-stu-id="278a4-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="278a4-121">Võimalik, et peate elemendi **Lõpp** vaatamiseks alla kerima.</span><span class="sxs-lookup"><span data-stu-id="278a4-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="278a4-122">Saate seda lohistada teiste elementideni lähemal.</span><span class="sxs-lookup"><span data-stu-id="278a4-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="278a4-123">[![Ühendage töövoo elemendid](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="278a4-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="278a4-124">Topeltklõpsake **1Kinnita oskused 1** töövoo element ja paremklõpsake **Samm 1** element.</span><span class="sxs-lookup"><span data-stu-id="278a4-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="278a4-125">Paremklõpsake **Samm 1** element ja valige suvand **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="278a4-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="278a4-126">**Atribuutide** aknas valige **Tingimus** vasakpoolsel navigeerimisribal.</span><span class="sxs-lookup"><span data-stu-id="278a4-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="278a4-127">Valige suvand **Käivita see samm üksnes siis, kui järgmine tingimus on täidetud**.</span><span class="sxs-lookup"><span data-stu-id="278a4-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="278a4-128">Valige **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="278a4-128">Select **Add condition**.</span></span> <span data-ttu-id="278a4-129">Pärast **Kus** käsku valige **Töötaja iseteenindusoskused** ja seejärel valige **Töötaja iseteenindusoskused. Isik**.</span><span class="sxs-lookup"><span data-stu-id="278a4-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="278a4-130">Pärast **on** valige **väli** ja seejärel valige **Kasutaja suhe isikuga. Isik**.</span><span class="sxs-lookup"><span data-stu-id="278a4-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="278a4-131">[![Määra tingimus](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="278a4-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="278a4-132">Valige **Määrang** vasaku käe navigeerimisribal.</span><span class="sxs-lookup"><span data-stu-id="278a4-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="278a4-133">Vahekaardil **Määrangu tüüp** valige **Hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="278a4-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="278a4-134">Valige **Hierarhia valik** vahekaardil **Hierarhia tüüp:** väärtus **Juhtimishierarhia**.</span><span class="sxs-lookup"><span data-stu-id="278a4-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="278a4-135">[![Määrake juhtimishierarhia](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="278a4-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="278a4-136">Valige **Sule** ja seejärel valige **Töövoog** lõuendi tööreas, siis valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="278a4-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="278a4-137">Lisateavet töövoogudega töötamise kohta vt teemast [Töövoosüsteemi ülevaade](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="278a4-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="278a4-138">Sisestage töötaja oskused</span><span class="sxs-lookup"><span data-stu-id="278a4-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="278a4-139">Vali töötaja.</span><span class="sxs-lookup"><span data-stu-id="278a4-139">Select a worker.</span></span>

2. <span data-ttu-id="278a4-140">Valige **Töötaja** lehel tegevusribalt **Isik** ja seejärel **Oskused**.</span><span class="sxs-lookup"><span data-stu-id="278a4-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="278a4-141">Täitke **Oskused** lehel iga oskuse jaoks järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="278a4-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="278a4-142">**Oskus**: Valige oskus.</span><span class="sxs-lookup"><span data-stu-id="278a4-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="278a4-143">**Taseme tüüp**: Valige **Tegelik** oskus töötaja olemaoslevale oskusele või **Soovitud** oskus töötaja oskuse jaoks, mida ta sihib.</span><span class="sxs-lookup"><span data-stu-id="278a4-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="278a4-144">**Tase**: Valige töötaja oskuse tase.</span><span class="sxs-lookup"><span data-stu-id="278a4-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="278a4-145">**Taseme kuupäev**: Valimiseks klõpsake kalendris kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="278a4-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="278a4-146">**Kontrollija**: Vajadusel valige loendist soovitud kontrollija.</span><span class="sxs-lookup"><span data-stu-id="278a4-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="278a4-147">Saate otsingut filtreerida.</span><span class="sxs-lookup"><span data-stu-id="278a4-147">You can filter your search.</span></span>
   - <span data-ttu-id="278a4-148">**Kogemuse aasta**: Sisestage kogemuse aasta.</span><span class="sxs-lookup"><span data-stu-id="278a4-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="278a4-149">**Kinnitatud**: Kui oskus on kinnitatud, märkige ruut.</span><span class="sxs-lookup"><span data-stu-id="278a4-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="278a4-150">**Kinnitaja**: Sisestage kinnitaja nimi.</span><span class="sxs-lookup"><span data-stu-id="278a4-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="278a4-151">Kui olete oskuste sisestamise lõpetanud, valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="278a4-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="278a4-152">Vt ka</span><span class="sxs-lookup"><span data-stu-id="278a4-152">See also</span></span>

[<span data-ttu-id="278a4-153">Oskuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="278a4-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="278a4-154">Oskuste kaardimine</span><span class="sxs-lookup"><span data-stu-id="278a4-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]