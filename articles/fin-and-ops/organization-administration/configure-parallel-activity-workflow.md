---
title: "Paralleeltegevuste konfigureerimine töövoos"
description: "Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 64cd387f8a6ab693d159cd659fca51fa6568ee39
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="26561-103">Paralleeltegevuste konfigureerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="26561-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26561-104">Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.</span><span class="sxs-lookup"><span data-stu-id="26561-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="26561-105">Paralleeltegevus koosneb töövoo harudes, mis töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="26561-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="26561-106">Paralleeltegevusele nime andmine</span><span class="sxs-lookup"><span data-stu-id="26561-106">Name a parallel activity</span></span>
<span data-ttu-id="26561-107">Paralleeltegevusele nime andmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="26561-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="26561-108">Paremklõpsake paralleeltegevust ja klõpsake valikut **Atribuudid** , et avada vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="26561-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="26561-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="26561-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="26561-110">Väljale **Nimi** sisestage paralleeltegevuse kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="26561-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="26561-111">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="26561-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="26561-112">Paralleeltegevuse harude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="26561-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="26561-113">Selle paralleeltegevuse harude lisamiseks ja konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="26561-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1. <span data-ttu-id="26561-114">Topeltklõpsake paralleeltegevust, et kuvada paralleeltegevuse harud.</span><span class="sxs-lookup"><span data-stu-id="26561-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="26561-115">Haru lisamiseks lohistage element **Haru** alalt **Töövoo elemendid** lõuendil olevasse sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="26561-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="26561-116">Järgmisel joonisel on kujutatud sisestuspunkt.![Sisestuspunkt](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="26561-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>

   |                                              <span data-ttu-id="26561-117"><strong>Märkus.</strong></span><span class="sxs-lookup"><span data-stu-id="26561-117"><strong>Note</strong></span></span>                                               |
   |------------------------------------------------------------------------------------------------------------------|
   | <span data-ttu-id="26561-118">Harude järjestus pole oluline, kuna kõik paralleeltegevuse harud töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="26561-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |


3. <span data-ttu-id="26561-119">Iga haru konfigureerimiseks vt jaotist [Paralleelharu konfigureerimine](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="26561-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






