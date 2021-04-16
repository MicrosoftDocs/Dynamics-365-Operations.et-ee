---
title: Paralleeltegevuste konfigureerimine töövoos
description: Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1a47857cbe65c00ad678b2b0372c642abf01b41
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747827"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="264e1-103">Paralleeltegevuste konfigureerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="264e1-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="264e1-104">Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.</span><span class="sxs-lookup"><span data-stu-id="264e1-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="264e1-105">Paralleeltegevus koosneb töövoo harudes, mis töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="264e1-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="264e1-106">Paralleeltegevusele nime andmine</span><span class="sxs-lookup"><span data-stu-id="264e1-106">Name a parallel activity</span></span>

<span data-ttu-id="264e1-107">Paralleeltegevusele nime andmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="264e1-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="264e1-108">Paremklõpsake paralleeltegevust ja klõpsake valikut **Atribuudid** , et avada vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="264e1-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="264e1-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="264e1-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="264e1-110">Väljale **Nimi** sisestage paralleeltegevuse kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="264e1-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="264e1-111">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="264e1-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="264e1-112">Paralleeltegevuse harude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="264e1-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="264e1-113">Selle paralleeltegevuse harude lisamiseks ja konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="264e1-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="264e1-114">Topeltklõpsake paralleeltegevust, et kuvada paralleeltegevuse harud.</span><span class="sxs-lookup"><span data-stu-id="264e1-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="264e1-115">Haru lisamiseks lohistage element **Haru** alalt **Töövoo elemendid** lõuendil olevasse sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="264e1-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="264e1-116">Järgmisel joonisel on kujutatud sisestuspunkt.</span><span class="sxs-lookup"><span data-stu-id="264e1-116">The following figure shows an insertion point.</span></span>

    ![Sisestuspunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="264e1-118">Harude järjestus pole oluline, kuna kõik paralleeltegevuse harud töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="264e1-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="264e1-119">Iga haru konfigureerimiseks vaadake jaotist [Töövoo paralleelsete harude konfigureerimine](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="264e1-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]