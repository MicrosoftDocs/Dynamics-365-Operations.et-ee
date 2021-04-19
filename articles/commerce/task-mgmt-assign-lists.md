---
title: Ülesandeloendite määramine poodidele või töötajatele
description: Selles teemas kirjeldatakse, kuidas määrata rakenduses Microsoft Dynamics 365 Commerce poodidele või töötajatele ülesandeloendeid.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0c4f028367c894c54392963ffc4f6a0f0c04c03a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795257"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="1a950-103">Tööülesannete loendite määramine kauplustele või töötajatele</span><span class="sxs-lookup"><span data-stu-id="1a950-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a950-104">Selles teemas kirjeldatakse, kuidas määrata rakenduses Microsoft Dynamics 365 Commerce poodidele või töötajatele ülesandeloendeid.</span><span class="sxs-lookup"><span data-stu-id="1a950-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1a950-105">Rakenduse Dynamics 365 Commerce ülesannete haldus võimaldab teil määrata ülesandeloendeid erinevatele poodidele või töötajatele või poodide ja töötajate kombinatsioonile.</span><span class="sxs-lookup"><span data-stu-id="1a950-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="1a950-106">Näiteks võib 20 poe piirkondlik juht soovida määrata kõigile 20 poele ülesandeloendi **Pühadeaja ettevalmistus**.</span><span class="sxs-lookup"><span data-stu-id="1a950-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="1a950-107">Ülesandeloendi määramise protsessi käivitamine</span><span class="sxs-lookup"><span data-stu-id="1a950-107">Start the task list assignment process</span></span>

<span data-ttu-id="1a950-108">Ülesandeloendi määramise protsessi alustamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1a950-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="1a950-109">Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse administreerimine**.</span><span class="sxs-lookup"><span data-stu-id="1a950-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="1a950-110">Valige määramiseks ülesandeloend.</span><span class="sxs-lookup"><span data-stu-id="1a950-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="1a950-111">Valige suvand **Alusta protsessi**.</span><span class="sxs-lookup"><span data-stu-id="1a950-111">Select **Start process**.</span></span>
1. <span data-ttu-id="1a950-112">Dialoogiboksis **Käivita protsess** vahekaardil **Üldine** väljal **Protsessi nimi** sisestage nimi (näiteks **Ida piirkonna poed**).</span><span class="sxs-lookup"><span data-stu-id="1a950-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="1a950-113">Täpsustage kuupäev väljal **Sihtkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="1a950-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="1a950-114">Ülesandeloendi poodidele määramiseks kasutage vahekaardil **Poed** filtrit **Organisatsiooni hierarhia**, et otsida ja valida poed.</span><span class="sxs-lookup"><span data-stu-id="1a950-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="1a950-115">Ülesandeloendi töötajatele määramiseks otsige ja valige töötajad vahekaardil **Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="1a950-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="1a950-116">Protsessi alustamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a950-116">Select **OK** to start the process.</span></span> <span data-ttu-id="1a950-117">Ülesandeloend määratakse valitud poodidele või töötajatele.</span><span class="sxs-lookup"><span data-stu-id="1a950-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="1a950-118">Järgmisel joonisel on toodud näide, kuidas dialoogiboksis **Alusta protsessi** otsida ja valida poode.</span><span class="sxs-lookup"><span data-stu-id="1a950-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Poodide otsimine ja valimine dialoogiboksis Alusta protsessi](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="1a950-120">Korduva ülesandeloendi määramine</span><span class="sxs-lookup"><span data-stu-id="1a950-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="1a950-121">Jaemüüjal on mõnikord korduvad ülesanded, nagu „Neljapäevane sulgemise kontroll-loend” või „Kuu esimese päeva kontroll-loend”.</span><span class="sxs-lookup"><span data-stu-id="1a950-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="1a950-122">Seetõttu võivad nad soovida määrata korduva ülesandeloendi.</span><span class="sxs-lookup"><span data-stu-id="1a950-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="1a950-123">Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse administreerimine**.</span><span class="sxs-lookup"><span data-stu-id="1a950-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="1a950-124">Valige määramiseks ülesandeloend.</span><span class="sxs-lookup"><span data-stu-id="1a950-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="1a950-125">Valige suvand **Alusta protsessi**.</span><span class="sxs-lookup"><span data-stu-id="1a950-125">Select **Start process**.</span></span>
1. <span data-ttu-id="1a950-126">Dialoogiboksis **Alusta protsessi** vahekaardil **Üldine** väljal **Protsessi nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="1a950-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="1a950-127">Määrake suvand **Kordumine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1a950-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="1a950-128">Sisestage päevade arv väljale **Korduvuse sihtkuupäeva nihe päevades**.</span><span class="sxs-lookup"><span data-stu-id="1a950-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="1a950-129">Näiteks kui sisestate **4**, on sihtkuupäevaks kordumise kuupäev pluss neli päeva.</span><span class="sxs-lookup"><span data-stu-id="1a950-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="1a950-130">Vahekaardil **Käivita taustal** valige suvand **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="1a950-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="1a950-131">Sisestage dialoogiboksis **Korduse määratlemine** sageduse kriteeriumid ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a950-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="1a950-132">Järgmisel joonisel on toodud näidis, kuidas sisestada dialoogiboksi **Korduse määratlemine** sageduse kriteeriume.</span><span class="sxs-lookup"><span data-stu-id="1a950-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Sageduse kriteeriumite sisestamine dialoogiboksis Korduse määratlemine](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="1a950-134">Ülesandeloendi oleku jälgimine</span><span class="sxs-lookup"><span data-stu-id="1a950-134">Track task list status</span></span>

<span data-ttu-id="1a950-135">Kui olete piirkondlik juht või poe juhataja, võite tahta jälgida ülesandeloendite olekut, mis on mitmele poele või töötajale määratud.</span><span class="sxs-lookup"><span data-stu-id="1a950-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="1a950-136">Seejärel saate teha järeltegevusi poodide või töötajatega, kes neile määratud ülesandeid õigeaegselt ei täitnud.</span><span class="sxs-lookup"><span data-stu-id="1a950-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="1a950-137">Commerce’i kontor võimaldab teil vaadata ülesandeloendite olekut, ülesandeid uuesti märata või muuta ülesande olekut.</span><span class="sxs-lookup"><span data-stu-id="1a950-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="1a950-138">Kõikide ülesannete ülesandeloendi oleku jälgimiseks toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="1a950-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="1a950-139">Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse protsess**.</span><span class="sxs-lookup"><span data-stu-id="1a950-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="1a950-140">Erinevatele poodidele määratud kõikide ülesandeloendite oleku vaatamiseks valige vahekaart **Kõik ülesandeloendid**.</span><span class="sxs-lookup"><span data-stu-id="1a950-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="1a950-141">Kõikide teile määratud ülesannete ülesandeloendi oleku jälgimiseks toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="1a950-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="1a950-142">Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse protsess**.</span><span class="sxs-lookup"><span data-stu-id="1a950-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="1a950-143">Valige vahekaart **Minu ülesanded** või **Kõik ülesanded**, et vaadata või värskendada teile määratud ülesannete olekut.</span><span class="sxs-lookup"><span data-stu-id="1a950-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a950-144">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1a950-144">Additional resources</span></span>

[<span data-ttu-id="1a950-145">Ülesannete halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="1a950-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="1a950-146">Ülesannete halduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1a950-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="1a950-147">Ülesandeloendite loomine ja ülesannete lisamine</span><span class="sxs-lookup"><span data-stu-id="1a950-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="1a950-148">Ülesannete haldus kassas</span><span class="sxs-lookup"><span data-stu-id="1a950-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
