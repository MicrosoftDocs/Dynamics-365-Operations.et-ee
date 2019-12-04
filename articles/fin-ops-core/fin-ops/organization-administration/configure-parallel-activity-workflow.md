---
title: Paralleeltegevuste konfigureerimine töövoos
description: Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14b4410a0bd177159817cd5116a5a0d959992ad5
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812405"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="f7cee-103">Paralleeltegevuste konfigureerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="f7cee-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7cee-104">Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.</span><span class="sxs-lookup"><span data-stu-id="f7cee-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="f7cee-105">Paralleeltegevus koosneb töövoo harudes, mis töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="f7cee-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="f7cee-106">Paralleeltegevusele nime andmine</span><span class="sxs-lookup"><span data-stu-id="f7cee-106">Name a parallel activity</span></span>

<span data-ttu-id="f7cee-107">Paralleeltegevusele nime andmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f7cee-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="f7cee-108">Paremklõpsake paralleeltegevust ja klõpsake valikut **Atribuudid** , et avada vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="f7cee-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="f7cee-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="f7cee-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="f7cee-110">Väljale **Nimi** sisestage paralleeltegevuse kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="f7cee-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="f7cee-111">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="f7cee-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="f7cee-112">Paralleeltegevuse harude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f7cee-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="f7cee-113">Selle paralleeltegevuse harude lisamiseks ja konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f7cee-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="f7cee-114">Topeltklõpsake paralleeltegevust, et kuvada paralleeltegevuse harud.</span><span class="sxs-lookup"><span data-stu-id="f7cee-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="f7cee-115">Haru lisamiseks lohistage element **Haru** alalt **Töövoo elemendid** lõuendil olevasse sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="f7cee-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="f7cee-116">Järgmisel joonisel on kujutatud sisestuspunkt.</span><span class="sxs-lookup"><span data-stu-id="f7cee-116">The following figure shows an insertion point.</span></span>

    ![Sisestuspunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="f7cee-118">Harude järjestus pole oluline, kuna kõik paralleeltegevuse harud töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="f7cee-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="f7cee-119">Iga haru konfigureerimiseks vaadake jaotist [Töövoo paralleelsete harude konfigureerimine](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f7cee-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
