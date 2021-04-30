---
title: Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel
description: See teema kirjeldab, kuidas sünkroonida ülesannete haldust Microsoft Teams ja Dynamics 365 Commerce müügikoha vahel.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b4a9ad561e3bff67720a08d6e4184a81e01f734
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908265"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="61f86-103">Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel</span><span class="sxs-lookup"><span data-stu-id="61f86-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61f86-104">See teema kirjeldab, kuidas sünkroonida ülesannete haldust Microsoft Teams ja Dynamics 365 Commerce müügikoha vahel.</span><span class="sxs-lookup"><span data-stu-id="61f86-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="61f86-105">Teams'i integreerimise üks peamisi eesmärke on võimaldada kassarakenduse ja Teams-i ülesannete halduse sünkroonimist.</span><span class="sxs-lookup"><span data-stu-id="61f86-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="61f86-106">Nii saavad poe töötajad ülesannete haldamiseks kasutada kas POS-rakendust või Teamsit ega pea rakendusi vahetama.</span><span class="sxs-lookup"><span data-stu-id="61f86-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="61f86-107">Kuna Plannerit kasutatakse Teamsi ülesannete hoidlana, peab olema seos Teamsi ja Dynamics 365 Commerce vahel.</span><span class="sxs-lookup"><span data-stu-id="61f86-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="61f86-108">Selle lingi loomiseks kasutatakse konkreetse poe meeskonna kindlat plaani ID-d.</span><span class="sxs-lookup"><span data-stu-id="61f86-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="61f86-109">Järgmised protseduurid näitavad, kuidas seadistada POS- ja Teams-rakenduste vahel ülesannete haldamise sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="61f86-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="61f86-110">Katseülesande loendi avaldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="61f86-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="61f86-111">Järgmine protseduur eeldab, et teie kauplusemeeskonnad kasutavad Microsoft Teams esmakordselt ülesandehalduse integreerimist Commerce'iga.</span><span class="sxs-lookup"><span data-stu-id="61f86-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="61f86-112">Katseülesannete loendi avaldamiseks Teamis järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="61f86-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="61f86-113">Logige Teami suhtlushaldurina sisse.</span><span class="sxs-lookup"><span data-stu-id="61f86-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="61f86-114">Tavaliselt on kommunikatsioonijuhid kasutajad, kellel on Commerce'i **piirkonnajuhi** roll.</span><span class="sxs-lookup"><span data-stu-id="61f86-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="61f86-115">Valige vasakul navigeerimispaanil **Planner ülesanded** alusel.</span><span class="sxs-lookup"><span data-stu-id="61f86-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="61f86-116">Vahekaardil **Avaldatud loendid** valige all vasakul **Uus loend** ja nimetage uus loend **Testülesannete loend**.</span><span class="sxs-lookup"><span data-stu-id="61f86-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="61f86-117">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="61f86-117">Select **Create**.</span></span> <span data-ttu-id="61f86-118">Uus loend kuvatakse jaotises **Mustandid**.</span><span class="sxs-lookup"><span data-stu-id="61f86-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="61f86-119">**Ülesande pealkirja** all andke esimesele ülesandele pealkiri **Teams integreerimise testimine**.</span><span class="sxs-lookup"><span data-stu-id="61f86-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="61f86-120">Seejärel valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="61f86-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="61f86-121">Valige loendist **Mustandid** ülesandeloend.</span><span class="sxs-lookup"><span data-stu-id="61f86-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="61f86-122">Seejärel valige ülemises parempoolses nurgas  **Avalda** .</span><span class="sxs-lookup"><span data-stu-id="61f86-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="61f86-123">Dialoogiboksis **Valige, kes avaldab**, valige meeskonnad, kes peaksid vastu võtma testülesannete loendi.</span><span class="sxs-lookup"><span data-stu-id="61f86-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="61f86-124">Avaldamisplaani läbivaatamiseks klõpsake nuppu **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="61f86-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="61f86-125">Kui peate muudatusi tegema, valige suvand  **Tagasi**.</span><span class="sxs-lookup"><span data-stu-id="61f86-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="61f86-126">Valige käsk **Jätkamiseks kinnita** ja valige valige käsk **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="61f86-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="61f86-127">Kui avaldamine on lõpule viidud, ilmub **avaldatud loendite** vahekaardi ülaosas teade, kui teie ülesannete loend on edukalt kohale toimetatud.</span><span class="sxs-lookup"><span data-stu-id="61f86-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="61f86-128">Lisateavet vt [Avalda ülesannete loendid, et luua ja jälgida organisatsiooni tööd](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="61f86-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="61f86-129">Kassa ja Teams linkimine ülesannete haldamiseks</span><span class="sxs-lookup"><span data-stu-id="61f86-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="61f86-130">Kassa ja Microsoft Teams rakenduste linkimiseks Commerce peakontori ülesandehalduse jaoks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="61f86-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="61f86-131">Minge **Retail ja Commerce \> Ülesandehaldus \>Ülesannete integreerimine rakendusega Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="61f86-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="61f86-132">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="61f86-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="61f86-133">Määrake suvandi **Luba ülesandehalduse integratsioon** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="61f86-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="61f86-134">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="61f86-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="61f86-135">Tegumiribal valige **Ülesandehalduse seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="61f86-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="61f86-136">Peaksite saama teatise, mis näitab, et luuakse partiitöö nimega **Teamsi ettevalmistamine**.</span><span class="sxs-lookup"><span data-stu-id="61f86-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="61f86-137">Minge **Süsteemihaldus \> Päringud \> Partiitööd** ja leidke viimane töö, mille kirjeldus on **Teamsi ettevalmistamine**.</span><span class="sxs-lookup"><span data-stu-id="61f86-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="61f86-138">Oodake, kuni töö on lõpuni viidud.</span><span class="sxs-lookup"><span data-stu-id="61f86-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="61f86-139">Käitage **CDX-töö 1070**, et avaldada plaani ID ja talletada viited jaemüügiserveris.</span><span class="sxs-lookup"><span data-stu-id="61f86-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61f86-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="61f86-140">Additional resources</span></span>

[<span data-ttu-id="61f86-141">Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="61f86-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="61f86-142">Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="61f86-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="61f86-143">Microsoft Teams sätted rakendusest Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="61f86-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="61f86-144">Kasutaja rollide haldamine rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="61f86-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="61f86-145">Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="61f86-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="61f86-146">Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK</span><span class="sxs-lookup"><span data-stu-id="61f86-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
