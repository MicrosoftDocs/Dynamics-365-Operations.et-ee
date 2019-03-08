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
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308433"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="7fb4e-103">Paralleeltegevuste konfigureerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="7fb4e-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fb4e-104">Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="7fb4e-105">Paralleeltegevus koosneb töövoo harudes, mis töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="7fb4e-106">Paralleeltegevusele nime andmine</span><span class="sxs-lookup"><span data-stu-id="7fb4e-106">Name a parallel activity</span></span>

<span data-ttu-id="7fb4e-107">Paralleeltegevusele nime andmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="7fb4e-108">Paremklõpsake paralleeltegevust ja klõpsake valikut **Atribuudid** , et avada vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="7fb4e-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="7fb4e-110">Väljale **Nimi** sisestage paralleeltegevuse kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="7fb4e-111">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="7fb4e-112">Paralleeltegevuse harude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7fb4e-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="7fb4e-113">Selle paralleeltegevuse harude lisamiseks ja konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="7fb4e-114">Topeltklõpsake paralleeltegevust, et kuvada paralleeltegevuse harud.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="7fb4e-115">Haru lisamiseks lohistage element **Haru** alalt **Töövoo elemendid** lõuendil olevasse sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="7fb4e-116">Järgmisel joonisel on kujutatud sisestuspunkt.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-116">The following figure shows an insertion point.</span></span>

    ![Sisestuspunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="7fb4e-118">Harude järjestus pole oluline, kuna kõik paralleeltegevuse harud töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="7fb4e-119">Iga haru konfigureerimiseks vt jaotist [Paralleelharu konfigureerimine](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="7fb4e-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>
