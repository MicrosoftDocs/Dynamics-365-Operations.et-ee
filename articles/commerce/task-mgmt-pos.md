---
title: Ülesannete haldus kassas
description: Selles teemas kirjeldatakse ülesannete haldust Microsoft Dynamics 365 Commerce’i kassarakenduses.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411736"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="858b7-103">Ülesannete haldus kassas</span><span class="sxs-lookup"><span data-stu-id="858b7-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="858b7-104">Selles teemas kirjeldatakse ülesannete haldust Microsoft Dynamics 365 Commerce’i kassarakenduses.</span><span class="sxs-lookup"><span data-stu-id="858b7-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="858b7-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="858b7-105">Overview</span></span>

<span data-ttu-id="858b7-106">Dynamics 365 Commerce’i kassarakenduses leiduvad ülesannete halduse funktsioonid, mis võimaldavad poe juhatajatel ja töötajatel hallata ülesandeid ja värskendada ülesande olekut.</span><span class="sxs-lookup"><span data-stu-id="858b7-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="858b7-107">Poe töötajad pääsevad tööülesannetele juurde kas valides kassa avalehel paani **Tööülesanded** või valides ülesannete teatised.</span><span class="sxs-lookup"><span data-stu-id="858b7-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="858b7-108">Vaikimisi viiakse poe töötajad vahekaardile **Minu ülesanded**, kus nad saavad vaadata neile määratud ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="858b7-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="858b7-109">Kuid nad saavad kergesti vahetada vahekaartidele **Tähtaja ületanud ülesanded**, **Avatud ülesanded** ja **Ülesannete loendid**.</span><span class="sxs-lookup"><span data-stu-id="858b7-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="858b7-110">Poe juhatajate ülesannete toimingud</span><span class="sxs-lookup"><span data-stu-id="858b7-110">Task operations for store managers</span></span>

<span data-ttu-id="858b7-111">Poe juhatajad saavad käsuriba nuppe kasutades teostada kassarakenduses järgmisi ülesande toiminguid.</span><span class="sxs-lookup"><span data-stu-id="858b7-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="858b7-112">**Määra** – määrake valitud ülesanded poe töötajale.</span><span class="sxs-lookup"><span data-stu-id="858b7-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="858b7-113">**Ülesande olek** – muutke valitud ülesannete olekut.</span><span class="sxs-lookup"><span data-stu-id="858b7-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="858b7-114">**Filtreeri** – vaikimisi kuvatakse ainult aktiivsed toimingud.</span><span class="sxs-lookup"><span data-stu-id="858b7-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="858b7-115">Samas filtreid rakendades saavad juhid kuvada kõik ülesanded, isegi lõpetatud või tühistatud ülesanded.</span><span class="sxs-lookup"><span data-stu-id="858b7-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="858b7-116">**Uus ülesanne** – looge ülesanne olemasolevase ülesande loendisse või looge ühekordne ülesanne.</span><span class="sxs-lookup"><span data-stu-id="858b7-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="858b7-117">Poe töötajad saavad käsuriba nuppe kasutades teostada kassarakenduses järgmisi ülesande toiminguid.</span><span class="sxs-lookup"><span data-stu-id="858b7-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="858b7-118">**Ülesande olek** – muutke valitud ülesannete olekut.</span><span class="sxs-lookup"><span data-stu-id="858b7-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="858b7-119">**Filtreeri** – vaikimisi kuvatakse ainult aktiivsed toimingud.</span><span class="sxs-lookup"><span data-stu-id="858b7-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="858b7-120">Samas filtreid rakendades saavad töötajad kuvada kõik ülesanded, isegi lõpetatud või tühistatud ülesanded.</span><span class="sxs-lookup"><span data-stu-id="858b7-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="858b7-121">Järgmine joonis näitab rakenduse Commerce kassarakenduse vahekaarti **Minu ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="858b7-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Vahekaart Minu ülesanded Commerce’i kassarakenduses](media/POS-task-management.png)

<span data-ttu-id="858b7-123">Järgmine illustratsioon näitab vahekaarti **Ülesandeloendid**.</span><span class="sxs-lookup"><span data-stu-id="858b7-123">The following illustration shows the **Task lists** tab.</span></span>

![Vahekaart Ülesandeloendid Commerce’i kassarakenduses](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="858b7-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="858b7-125">Additional resources</span></span>

[<span data-ttu-id="858b7-126">Ülesannete halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="858b7-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="858b7-127">Ülesannete halduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="858b7-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="858b7-128">Ülesandeloendite loomine ja ülesannete lisamine</span><span class="sxs-lookup"><span data-stu-id="858b7-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="858b7-129">Ülesandeloendite määramine poodidele või töötajatele</span><span class="sxs-lookup"><span data-stu-id="858b7-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
