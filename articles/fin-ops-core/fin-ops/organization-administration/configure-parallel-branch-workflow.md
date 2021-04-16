---
title: Paralleelharude konfigureerimine töövoos
description: Paralleelharu konfigureerimiseks viige töövooredaktoris lõpule järgmised protseduurid.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b5270660f0dbe4351f0088787468a563d2f36cf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747803"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="93c3a-103">Paralleelharude konfigureerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="93c3a-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93c3a-104">Paralleelharu konfigureerimiseks viige töövooredaktoris lõpule järgmised protseduurid.</span><span class="sxs-lookup"><span data-stu-id="93c3a-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="93c3a-105">Paralleelharu on peamiselt töövoog, mida käitatakse ematöövoo kontekstis.</span><span class="sxs-lookup"><span data-stu-id="93c3a-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="93c3a-106">Haru nimetamine</span><span class="sxs-lookup"><span data-stu-id="93c3a-106">Name a branch</span></span>

<span data-ttu-id="93c3a-107">Sisestage paralleelharule nimi järgmisi juhiseid järgides.</span><span class="sxs-lookup"><span data-stu-id="93c3a-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="93c3a-108">Paremklõpsake paralleelharu ja seejärel klõpsake valikut **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="93c3a-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="93c3a-109">Kuvatakse vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="93c3a-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="93c3a-110">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="93c3a-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="93c3a-111">Väljale **Nimi** sisestage paralleelharu kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="93c3a-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="93c3a-112">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="93c3a-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="93c3a-113">Haru elementide kujundamine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="93c3a-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="93c3a-114">Järgige neid juhiseid, et kujundada ja konfigureerida paralleelharu elemendid.</span><span class="sxs-lookup"><span data-stu-id="93c3a-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="93c3a-115">Topeltklõpsake paralleelharu.</span><span class="sxs-lookup"><span data-stu-id="93c3a-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="93c3a-116">Lohistage töövoo elemendid lõuendile ja konfigureerige seejärel elemendid, nii nagu teeksite seda mis tahes muu töövoo loomiseks.</span><span class="sxs-lookup"><span data-stu-id="93c3a-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="93c3a-117">Lisateavet leiate teemast [Töövoogude loomise ülevaade](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="93c3a-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93c3a-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="93c3a-118">Additional resources</span></span>

[<span data-ttu-id="93c3a-119">Töövoogude loomise ülevaade</span><span class="sxs-lookup"><span data-stu-id="93c3a-119">Create workflows overview</span></span>](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]