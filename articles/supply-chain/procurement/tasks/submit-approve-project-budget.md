---
title: Projekti eelarve esitamine ja kinnitamine
description: See protseduur näitab, kuidas luua ja esitada projekti eelarvet.
author: RichardLuan
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72ac6705ef8584ef41980a1cc9490227538de365
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222845"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="1542c-103">Projekti eelarve esitamine ja kinnitamine</span><span class="sxs-lookup"><span data-stu-id="1542c-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1542c-104">See protseduur näitab, kuidas luua ja esitada projekti eelarvet.</span><span class="sxs-lookup"><span data-stu-id="1542c-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="1542c-105">Projekti eelarve loomisel saate sisestada projekti hinnangulised tulud ja kulud ning kasutada seejärel neid tegelike projektikannete juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="1542c-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="1542c-106">Projekti eelarve koostamisel tuleb kõik algsed eelarved ja revisjonid kinnitamiseks projekti töövoogu saata.</span><span class="sxs-lookup"><span data-stu-id="1542c-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="1542c-107">Töövoog annab suurema kontrolli protsessi üle ja loob muudatuste ajaloo kirje.</span><span class="sxs-lookup"><span data-stu-id="1542c-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="1542c-108">See ülesande loodi USSI andmekogumit kasutades.</span><span class="sxs-lookup"><span data-stu-id="1542c-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="1542c-109">Avage **Navigeerimispaneelil** **Moodulid > Projektijuhtimine ja raamatupidamine > Projektid > Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="1542c-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="1542c-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1542c-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1542c-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1542c-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1542c-112">Klõpsake **Toimingupaanil** valikut **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="1542c-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="1542c-113">Klõpsake nuppu **Projekti eelarve**.</span><span class="sxs-lookup"><span data-stu-id="1542c-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="1542c-114">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="1542c-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="1542c-115">Laiendage kiirkaarti **Maksumus**.</span><span class="sxs-lookup"><span data-stu-id="1542c-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="1542c-116">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1542c-116">Click **New**.</span></span>
9. <span data-ttu-id="1542c-117">Valige suvand väljal **Kande tüüp**.</span><span class="sxs-lookup"><span data-stu-id="1542c-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="1542c-118">Väljale **Kategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1542c-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="1542c-119">Sisestage number väljale **Algne eelarve**.</span><span class="sxs-lookup"><span data-stu-id="1542c-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="1542c-120">Laiendage kiirkaarti **Tulud**.</span><span class="sxs-lookup"><span data-stu-id="1542c-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="1542c-121">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1542c-121">Click **New**.</span></span>
14. <span data-ttu-id="1542c-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1542c-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="1542c-123">Valige suvand väljal **Kande tüüp**.</span><span class="sxs-lookup"><span data-stu-id="1542c-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="1542c-124">Väljale **Kategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1542c-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="1542c-125">Sisestage number väljale **Algne eelarve**.</span><span class="sxs-lookup"><span data-stu-id="1542c-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="1542c-126">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1542c-126">Click **Save**.</span></span>
19. <span data-ttu-id="1542c-127">Klõpsake nuppu **Töövoog**.</span><span class="sxs-lookup"><span data-stu-id="1542c-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="1542c-128">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="1542c-128">Click **Submit**.</span></span>
21. <span data-ttu-id="1542c-129">Sisestage väärtus väljale **Kommentaar**.</span><span class="sxs-lookup"><span data-stu-id="1542c-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="1542c-130">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="1542c-130">Click **Submit**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]