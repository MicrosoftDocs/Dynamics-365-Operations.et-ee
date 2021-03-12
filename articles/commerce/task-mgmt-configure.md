---
title: Ülesannete halduse konfigureerimine
description: Selles teemas kirjeldatakse, kuidas konfigureerida ülesannete halduse funktsioone rakenduses Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e880305d02fd9f10464fe3f65a2774a44da258c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006231"
---
# <a name="configure-task-management"></a><span data-ttu-id="6288a-103">Ülesannete halduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6288a-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6288a-104">Selles teemas kirjeldatakse, kuidas konfigureerida ülesannete halduse funktsioone rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6288a-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6288a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="6288a-105">Overview</span></span>

<span data-ttu-id="6288a-106">Enne kui rakenduse Dynamics 365 Commerce juhatajad ja töötajad saavad Commerce’is ülesande haldamise funktsioone kasutada, tuleb ülesannete haldus konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="6288a-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="6288a-107">Konfiguratsiooni etapid hõlmavad juhatajatele ja töötajatele lubade andmist, kassa klientidele lubade andmist, kassa teavituste seadistamist ja kassarakenduse avalehel paani **Ülesanded** konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="6288a-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="6288a-108">Poe juhatajate lubade konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6288a-108">Configure permissions for store managers</span></span>

<span data-ttu-id="6288a-109">Konkreetse poe iga töötaja saab vaadata kõiki sellele poele määratud ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="6288a-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="6288a-110">Samuti saavad nad värskendada neile määratud ülesannete olekut.</span><span class="sxs-lookup"><span data-stu-id="6288a-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="6288a-111">Samas peab isikutel, nagu poe juhatajad, olema ülesande halduri load, et hallata poele määratud ülesandeid ja luua ühekordseid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="6288a-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="6288a-112">Poe juhatajate ülesannete halduse lubade konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6288a-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="6288a-113">Avage **Jaemüük ja kaubandus \> Töötajad \> Loagrupid**.</span><span class="sxs-lookup"><span data-stu-id="6288a-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="6288a-114">Valige konkreetne loagrupp (nt **Juhataja**) ja seejärel valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6288a-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="6288a-115">Kiirkaardil **Load** määrake suvand **Luba ülesannete haldus** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6288a-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="6288a-116">Kiirkaardil **Teatised** lisage toiming **Ülesannete haldus** ja sisestage väärtus väljale **Kuvamisjärjestus**.</span><span class="sxs-lookup"><span data-stu-id="6288a-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="6288a-117">Näiteks sisestage **2**, kui toimingul **Tellimuse täitmise** on juba suvandi **Kuvamisjärjestus** jaoks väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="6288a-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="6288a-118">Kui mitte-juhist isikul peab omama kassa ülesannete halduse õiguseid, saate isikule anda load.</span><span class="sxs-lookup"><span data-stu-id="6288a-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="6288a-119">Teise võimalusena saate luua uue õiguste grupi mitte-juhtidele ja seada suvand **Luba ülesannete haldamine** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6288a-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="6288a-120">Järgmisel joonisel on näidatud, kuidas konfigureerida poe juhatajate ülesannete halduse lubasid.</span><span class="sxs-lookup"><span data-stu-id="6288a-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Poe juhatajate ülesannete halduse lubade konfigureerimine](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="6288a-122">Töötajate lubade konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6288a-122">Configure permissions for employees</span></span>

<span data-ttu-id="6288a-123">Töötajatel peavad olema õigused ülesannete loendite loomiseks, määramise kriteeriumide haldamiseks ja ülesannete loendi kordumise konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6288a-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="6288a-124">Nende lubade konfigureerimiseks määrate töötajad rollile **Jaemüügi ülesannete haldur**.</span><span class="sxs-lookup"><span data-stu-id="6288a-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="6288a-125">Töötaja lubade konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6288a-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="6288a-126">Avage **Jaemüük ja kaubandus \> Töötajad \> Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="6288a-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="6288a-127">Valige töötaja.</span><span class="sxs-lookup"><span data-stu-id="6288a-127">Select an employee.</span></span>
1. <span data-ttu-id="6288a-128">Kiirkaardil **Kasutaja rollid** valige suvand **Määra rollid**.</span><span class="sxs-lookup"><span data-stu-id="6288a-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="6288a-129">Dialoogiboksis **Määra kasutajale rollid** valige roll **Jaemüügi ülesannete haldur** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="6288a-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="6288a-130">Kassa klientidele lubade jaotamine</span><span class="sxs-lookup"><span data-stu-id="6288a-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="6288a-131">Enne kui töötajad saavad kassa kliente kasutada, peavad load olema nende klientide vahel jaotatud ja sünkroonitud.</span><span class="sxs-lookup"><span data-stu-id="6288a-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="6288a-132">Kassa klientidele lubade jaotamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6288a-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="6288a-133">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="6288a-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="6288a-134">Valige jaotusgraafik **1060** (**Personal**) ja seejärel valige käsk **Käita kohe**.</span><span class="sxs-lookup"><span data-stu-id="6288a-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="6288a-135">Valige jaotusgraafik **1070** (**Kanali konfiguratsioon**) ja seejärel valige käsk **Käita kohe**.</span><span class="sxs-lookup"><span data-stu-id="6288a-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="6288a-136">Ülesannete jaoks kassa teatiste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6288a-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="6288a-137">Ülesannete haldus peab olema konfigureeritud nii, et teatised oleksid kassarakenduses saadaval.</span><span class="sxs-lookup"><span data-stu-id="6288a-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="6288a-138">Ülesannete jaoks kassa teatiste konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6288a-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="6288a-139">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Kassatoimingud**.</span><span class="sxs-lookup"><span data-stu-id="6288a-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="6288a-140">Leidke toiming **1400** (**Ülesannete haldus**) ja valige selle joaks märkeruut **Luba teatised**.</span><span class="sxs-lookup"><span data-stu-id="6288a-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="6288a-141">Järgmisel joonisel on kujutatud toiming **Ülesannete haldus** lehel **Kassa toimingud**.</span><span class="sxs-lookup"><span data-stu-id="6288a-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Ülesannete halduse toiming kassa toimingute lehel](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="6288a-143">Lisateavet kassa teatiste konfigureerimise kohta vt teemast [Kassa tellimuse teatiste kuvamine](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="6288a-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="6288a-144">Paani Ülesanded konfigureerimine kassarakenduse avalehel</span><span class="sxs-lookup"><span data-stu-id="6288a-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="6288a-145">Enne kassarakenduse avalehel paani **Ülesanded** konfigureerimist, vt teemast [Kassa ekraanipaigutused](pos-screen-layouts.md) teavet selle kohta, kuidas konfigureerida ja lisada kassa ekraanipaigutusse uusi nuppe.</span><span class="sxs-lookup"><span data-stu-id="6288a-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="6288a-146">Kassarakenduse avalehel paani **Ülesanded** konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6288a-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="6288a-147">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Ekraanipaigutused**.</span><span class="sxs-lookup"><span data-stu-id="6288a-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="6288a-148">Valige ekraanipaigutus, valige paigutuse suurus ja valige nupupaneel.</span><span class="sxs-lookup"><span data-stu-id="6288a-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="6288a-149">Kiirkaardil **Nupupaneelid** valige suvand **Kujundaja**, et redigeerida valitud nupupaneeli.</span><span class="sxs-lookup"><span data-stu-id="6288a-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="6288a-150">Lisage paan **Ülesanded** avalehe vastavale jaotisele.</span><span class="sxs-lookup"><span data-stu-id="6288a-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="6288a-151">Järgmisel joonisel on näidatud paani **Ülesanded** näide kassa avalehel.</span><span class="sxs-lookup"><span data-stu-id="6288a-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Ülesannete paan kassa avalehel](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="6288a-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6288a-153">Additional resources</span></span>

[<span data-ttu-id="6288a-154">Ülesannete halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="6288a-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="6288a-155">Ülesandeloendite loomine ja ülesannete lisamine</span><span class="sxs-lookup"><span data-stu-id="6288a-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="6288a-156">Ülesandeloendite määramine poodidele või töötajatele</span><span class="sxs-lookup"><span data-stu-id="6288a-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="6288a-157">Ülesannete haldus kassas</span><span class="sxs-lookup"><span data-stu-id="6288a-157">Task management in POS</span></span>](task-mgmt-POS.md)
