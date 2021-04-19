---
title: Ülesandehaldus kassas
description: Selles teemas kirjeldatakse ülesannete haldust Microsoft Dynamics 365 Commerce kassarakenduses (POS).
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
ms.openlocfilehash: 38ee9db94b3b222e8c0ce5d0883f47bd5d3e7d22
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796918"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="12d78-103">Ülesandehaldus kassas</span><span class="sxs-lookup"><span data-stu-id="12d78-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12d78-104">Selles teemas kirjeldatakse ülesannete haldust Microsoft Dynamics 365 Commerce kassarakenduses (POS).</span><span class="sxs-lookup"><span data-stu-id="12d78-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="12d78-105">Dynamics 365 Commerce’i kassarakenduses leiduvad ülesannete halduse funktsioonid, mis võimaldavad poe juhatajatel ja töötajatel hallata ülesandeid ja värskendada ülesande olekut.</span><span class="sxs-lookup"><span data-stu-id="12d78-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="12d78-106">Poe töötajad pääsevad tööülesannetele juurde kas valides kassa avalehel paani **Tööülesanded** või valides ülesannete teatised.</span><span class="sxs-lookup"><span data-stu-id="12d78-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="12d78-107">Vaikimisi viiakse poe töötajad vahekaardile **Minu ülesanded**, kus nad saavad vaadata neile määratud ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="12d78-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="12d78-108">Kuid nad saavad kergesti vahetada vahekaartidele **Tähtaja ületanud ülesanded**, **Avatud ülesanded** ja **Ülesannete loendid**.</span><span class="sxs-lookup"><span data-stu-id="12d78-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="12d78-109">Poe juhatajate ülesannete toimingud</span><span class="sxs-lookup"><span data-stu-id="12d78-109">Task operations for store managers</span></span>

<span data-ttu-id="12d78-110">Poe juhatajad saavad käsuriba nuppe kasutades teostada kassarakenduses järgmisi ülesande toiminguid.</span><span class="sxs-lookup"><span data-stu-id="12d78-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="12d78-111">**Määra** – määrake valitud ülesanded poe töötajale.</span><span class="sxs-lookup"><span data-stu-id="12d78-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="12d78-112">**Ülesande olek** – muutke valitud ülesannete olekut.</span><span class="sxs-lookup"><span data-stu-id="12d78-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="12d78-113">**Filtreeri** – vaikimisi kuvatakse ainult aktiivsed toimingud.</span><span class="sxs-lookup"><span data-stu-id="12d78-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="12d78-114">Samas filtreid rakendades saavad juhid kuvada kõik ülesanded, isegi lõpetatud või tühistatud ülesanded.</span><span class="sxs-lookup"><span data-stu-id="12d78-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="12d78-115">**Uus ülesanne** – looge ülesanne olemasolevase ülesande loendisse või looge ühekordne ülesanne.</span><span class="sxs-lookup"><span data-stu-id="12d78-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="12d78-116">Poe töötajad saavad käsuriba nuppe kasutades teostada kassarakenduses järgmisi ülesande toiminguid.</span><span class="sxs-lookup"><span data-stu-id="12d78-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="12d78-117">**Ülesande olek** – muutke valitud ülesannete olekut.</span><span class="sxs-lookup"><span data-stu-id="12d78-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="12d78-118">**Filtreeri** – vaikimisi kuvatakse ainult aktiivsed toimingud.</span><span class="sxs-lookup"><span data-stu-id="12d78-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="12d78-119">Samas filtreid rakendades saavad töötajad kuvada kõik ülesanded, isegi lõpetatud või tühistatud ülesanded.</span><span class="sxs-lookup"><span data-stu-id="12d78-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="12d78-120">Järgmine joonis näitab rakenduse Commerce kassarakenduse vahekaarti **Minu ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="12d78-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Vahekaart Minu ülesanded Commerce’i kassarakenduses](media/POS-task-management.png)

<span data-ttu-id="12d78-122">Järgmine illustratsioon näitab vahekaarti **Ülesandeloendid**.</span><span class="sxs-lookup"><span data-stu-id="12d78-122">The following illustration shows the **Task lists** tab.</span></span>

![Vahekaart Ülesandeloendid Commerce’i kassarakenduses](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="12d78-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="12d78-124">Additional resources</span></span>

[<span data-ttu-id="12d78-125">Ülesannete halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="12d78-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="12d78-126">Ülesannete halduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="12d78-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="12d78-127">Ülesandeloendite loomine ja ülesannete lisamine</span><span class="sxs-lookup"><span data-stu-id="12d78-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="12d78-128">Ülesandeloendite määramine poodidele või töötajatele</span><span class="sxs-lookup"><span data-stu-id="12d78-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
