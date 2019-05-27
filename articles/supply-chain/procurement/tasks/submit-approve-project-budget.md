---
title: Projekti eelarve esitamine ja kinnitamine
description: See protseduur näitab, kuidas luua ja esitada projekti eelarvet.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569841"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="9b1a8-103">Projekti eelarve esitamine ja kinnitamine</span><span class="sxs-lookup"><span data-stu-id="9b1a8-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b1a8-104">See protseduur näitab, kuidas luua ja esitada projekti eelarvet.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="9b1a8-105">Projekti eelarve loomisel saate sisestada projekti hinnangulised tulud ja kulud ning kasutada seejärel neid tegelike projektikannete juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="9b1a8-106">Projekti eelarve koostamisel tuleb kõik algsed eelarved ja revisjonid kinnitamiseks projekti töövoogu saata.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="9b1a8-107">Töövoog annab suurema kontrolli protsessi üle ja loob muudatuste ajaloo kirje.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="9b1a8-108">See ülesande loodi USSI andmekogumit kasutades.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="9b1a8-109">Avage Projektihaldus ja -arvestus > Projektid > Kõik projektid.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="9b1a8-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9b1a8-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9b1a8-112">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="9b1a8-113">Klõpsake nuppu Projekti eelarve.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-113">Click Project budget.</span></span>
6. <span data-ttu-id="9b1a8-114">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="9b1a8-115">Laiendage jaotist Kulu</span><span class="sxs-lookup"><span data-stu-id="9b1a8-115">Expand the Cost section</span></span>
8. <span data-ttu-id="9b1a8-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-116">Click New.</span></span>
9. <span data-ttu-id="9b1a8-117">Valige suvand väljal Kande tüüp.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="9b1a8-118">Valige või sisestage väärtus väljal Kategooria.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="9b1a8-119">Sisestage number väljale Algne eelarve.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="9b1a8-120">Laiendage jaotist Tulud.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="9b1a8-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-121">Click New.</span></span>
14. <span data-ttu-id="9b1a8-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="9b1a8-123">Valige suvand väljal Kande tüüp.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="9b1a8-124">Valige või sisestage väärtus väljal Kategooria.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="9b1a8-125">Sisestage number väljale Algne eelarve.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="9b1a8-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-126">Click Save.</span></span>
19. <span data-ttu-id="9b1a8-127">Klõpsake nuppu Töövoog.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-127">Click Workflow.</span></span>
20. <span data-ttu-id="9b1a8-128">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-128">Click Submit.</span></span>
21. <span data-ttu-id="9b1a8-129">Sisestage väärtus väljale Kommentaar.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="9b1a8-130">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="9b1a8-130">Click Submit.</span></span>

