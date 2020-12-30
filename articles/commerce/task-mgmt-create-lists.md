---
title: Ülesandeloendite loomine ja ülesannete lisamine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce luua ülesandeloendeid ja lisada neile ülesandeid.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1cab31784db9f3242dce20e98762088436a5a8f8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411737"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="974c7-103">Ülesandeloendite loomine ja ülesannete lisamine</span><span class="sxs-lookup"><span data-stu-id="974c7-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="974c7-104">Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce luua ülesandeloendeid ja lisada neile ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="974c7-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="974c7-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="974c7-105">Overview</span></span>

<span data-ttu-id="974c7-106">*Ülesanne* määratleb kindla töö või tegevuse, mille keegi peab täitma määratud tähtajal või enne seda.</span><span class="sxs-lookup"><span data-stu-id="974c7-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="974c7-107">Rakenduses Dynamics 365 Commerce võib ülesanne sisaldada üksikasjalikke juhiseid ja teavet kontaktisiku kohta.</span><span class="sxs-lookup"><span data-stu-id="974c7-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="974c7-108">See võib sisaldada ka linke kontori toimingutele kassatoimingutele või saidi lehtedele, et aidata parandada produktiivsust ja pakkuda konteksti, mida ülesande omanik ülesande tõhusaks täitmiseks vajab.</span><span class="sxs-lookup"><span data-stu-id="974c7-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="974c7-109">*Ülesandeloend* on ülesannete kogum, mis tuleb äriprotsessi osana täita.</span><span class="sxs-lookup"><span data-stu-id="974c7-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="974c7-110">Näiteks võib olemas olla ülesandeloend, mille uus töötaja peab sisseelamise ajal lõpetama, ülesandeloend õhtustes vahetustes töötvatele kassapidajatele või ülesandeloend, mis tuleb lõpule viia, et valmistada pood ette eelseisvaks pühadeajaks.</span><span class="sxs-lookup"><span data-stu-id="974c7-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="974c7-111">Rakenduses Commerce saab igale kauplusele või töötajale määrata iga loendi, millel on sihtkuupäev, ja selle saab konfigureerida korduvaks.</span><span class="sxs-lookup"><span data-stu-id="974c7-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="974c7-112">Nii juhid kui ka töötajad saavad luua rakenduse Commerce kontoris ülesandeloendeid ja seejärel määrata need poodide komplektile.</span><span class="sxs-lookup"><span data-stu-id="974c7-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="974c7-113">Ülesandeloendi loomine</span><span class="sxs-lookup"><span data-stu-id="974c7-113">Create a task list</span></span>

<span data-ttu-id="974c7-114">Ülesandeloendi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="974c7-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="974c7-115">Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse administreerimine**.</span><span class="sxs-lookup"><span data-stu-id="974c7-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="974c7-116">Valige suvand **Uus** ja seejärel sisestage väärtused väljadele **Nimi**, **Kirjeldus** ja **Omanik**.</span><span class="sxs-lookup"><span data-stu-id="974c7-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="974c7-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="974c7-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="974c7-118">Ülesandeloendisse ülesannete lisamine</span><span class="sxs-lookup"><span data-stu-id="974c7-118">Add tasks to a task list</span></span>

<span data-ttu-id="974c7-119">Ülesandeloendisse ülesannete lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="974c7-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="974c7-120">Olemasoleva ülesandeloendi kiirkaardil **Ülesanded** valige ülesande lisamiseks suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="974c7-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="974c7-121">Sisestage olemi nimi dialoogiboksis **Loo uus ülesanne** väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="974c7-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="974c7-122">Sisestage positiivne või negatiivne täisarvuline väärtus väljale **Tähtajaliste andmete nihe sihtkuupäevast alates**.</span><span class="sxs-lookup"><span data-stu-id="974c7-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="974c7-123">Näiteks sisestage **–2**, kui ülesanne tuleb lõpetada kaks päeva enne ülesandeloendi tähtaega.</span><span class="sxs-lookup"><span data-stu-id="974c7-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="974c7-124">Sisestage üksikasjalised juhised väljale **Märkmed**.</span><span class="sxs-lookup"><span data-stu-id="974c7-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="974c7-125">Väljale **Kontaktisik** sisestage valdkonna asjatundja nimi, kellega ülesanne omanik saab abi saamiseks ühendust võtta.</span><span class="sxs-lookup"><span data-stu-id="974c7-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="974c7-126">Sisestage väljale **Ülesande link** ülesande olemuse põhjal link.</span><span class="sxs-lookup"><span data-stu-id="974c7-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="974c7-127">Ehkki saate kasutada välja **Määratud:**, et määrata ülesanded kellelegi, kui ülesandeloendit loote, soovitame ülesandeloendi loomise ajal ülesannete määramist vältida.</span><span class="sxs-lookup"><span data-stu-id="974c7-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="974c7-128">Selle asemel määrake ülesanded pärast seda, kui loend on üksikute poodide jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="974c7-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="974c7-129">Töötaja tootlikkuse parandamist ülesannete linkide kasutamine</span><span class="sxs-lookup"><span data-stu-id="974c7-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="974c7-130">Rakendus Commerce võimaldab teil linkida ülesanded konkreetsete kassatoimingutega, nagu müügiaruande käitamine, uue töötaja juhendamiseks veebipõhise õppevideo vaatamine või kontoritoimingute tegemine.</span><span class="sxs-lookup"><span data-stu-id="974c7-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="974c7-131">See funktsioon aitab ülesannete omanikel saada teavet, mis on ülesande tõhusaks täitmiseks vaja.</span><span class="sxs-lookup"><span data-stu-id="974c7-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="974c7-132">Ülesande linkide lisamiseks ülesande loomise ajal toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="974c7-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="974c7-133">Olemasoleva ülesandeloendi kiirkaardil **Ülesanded** valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="974c7-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="974c7-134">Dialoogiboksis **Redigeeri ülesannet** väljal **Ülesande link** valige üks või mitu järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="974c7-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="974c7-135">Valige suvand **Menüü-üksus**, et konfigureerida kontori toiming, nagu „Tootekomplektid”.</span><span class="sxs-lookup"><span data-stu-id="974c7-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="974c7-136">Valige suvand **Kassatoiming**, et konfigureerida kassatoiming, näiteks „Müügiaruanded”.</span><span class="sxs-lookup"><span data-stu-id="974c7-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="974c7-137">Valige absoluutse URL-i konfigureerimiseks suvand **URL**.</span><span class="sxs-lookup"><span data-stu-id="974c7-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="974c7-138">Järgmisel joonisel on näidatud ülesande linkide valimine dialoogiboksis **Redigeeri ülesannet**.</span><span class="sxs-lookup"><span data-stu-id="974c7-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Ülesande linkide valimine dialoogiboksis Redigeeri ülesannet](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="974c7-140">Kassatoimingu konfigureerimine, et selle saaks ülesandega linkida</span><span class="sxs-lookup"><span data-stu-id="974c7-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="974c7-141">Kassatoimingu konfigureerimine, et selle saaks ülesandega linkida, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="974c7-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="974c7-142">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Kassatoimingud**.</span><span class="sxs-lookup"><span data-stu-id="974c7-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="974c7-143">Valige käsk **Redigeer**, leidke kassatoiming ja märkige seejärel selle märkeruut **Luba ülesande haldus**.</span><span class="sxs-lookup"><span data-stu-id="974c7-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="974c7-144">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="974c7-144">Additional resources</span></span>

[<span data-ttu-id="974c7-145">Ülesannete halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="974c7-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="974c7-146">Ülesannete halduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="974c7-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="974c7-147">Ülesandeloendite määramine poodidele või töötajatele</span><span class="sxs-lookup"><span data-stu-id="974c7-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="974c7-148">Ülesannete haldus kassas</span><span class="sxs-lookup"><span data-stu-id="974c7-148">Task management in POS</span></span>](task-mgmt-POS.md)
