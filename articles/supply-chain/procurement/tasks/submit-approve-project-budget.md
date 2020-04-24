---
title: Projekti eelarve esitamine ja kinnitamine
description: See protseduur näitab, kuidas luua ja esitada projekti eelarvet.
author: mkirknel
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14683554c45db72061ecbbf4a528656df3132692
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207439"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="ffac7-103">Projekti eelarve esitamine ja kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ffac7-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffac7-104">See protseduur näitab, kuidas luua ja esitada projekti eelarvet.</span><span class="sxs-lookup"><span data-stu-id="ffac7-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="ffac7-105">Projekti eelarve loomisel saate sisestada projekti hinnangulised tulud ja kulud ning kasutada seejärel neid tegelike projektikannete juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="ffac7-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="ffac7-106">Projekti eelarve koostamisel tuleb kõik algsed eelarved ja revisjonid kinnitamiseks projekti töövoogu saata.</span><span class="sxs-lookup"><span data-stu-id="ffac7-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="ffac7-107">Töövoog annab suurema kontrolli protsessi üle ja loob muudatuste ajaloo kirje.</span><span class="sxs-lookup"><span data-stu-id="ffac7-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="ffac7-108">See ülesande loodi USSI andmekogumit kasutades.</span><span class="sxs-lookup"><span data-stu-id="ffac7-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="ffac7-109">Avage **Navigeerimispaneelil** **Moodulid > Projektijuhtimine ja raamatupidamine > Projektid > Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="ffac7-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ffac7-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ffac7-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ffac7-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ffac7-112">Klõpsake **Toimingupaanil** valikut **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="ffac7-113">Klõpsake nuppu **Projekti eelarve**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="ffac7-114">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="ffac7-115">Laiendage kiirkaarti **Maksumus**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="ffac7-116">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-116">Click **New**.</span></span>
9. <span data-ttu-id="ffac7-117">Valige suvand väljal **Kande tüüp**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="ffac7-118">Väljale **Kategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="ffac7-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="ffac7-119">Sisestage number väljale **Algne eelarve**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="ffac7-120">Laiendage kiirkaarti **Tulud**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="ffac7-121">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-121">Click **New**.</span></span>
14. <span data-ttu-id="ffac7-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ffac7-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="ffac7-123">Valige suvand väljal **Kande tüüp**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="ffac7-124">Väljale **Kategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="ffac7-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="ffac7-125">Sisestage number väljale **Algne eelarve**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="ffac7-126">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-126">Click **Save**.</span></span>
19. <span data-ttu-id="ffac7-127">Klõpsake nuppu **Töövoog**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="ffac7-128">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-128">Click **Submit**.</span></span>
21. <span data-ttu-id="ffac7-129">Sisestage väärtus väljale **Kommentaar**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="ffac7-130">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="ffac7-130">Click **Submit**.</span></span>

