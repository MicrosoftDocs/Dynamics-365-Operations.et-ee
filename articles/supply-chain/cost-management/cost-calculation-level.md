---
title: Kuluarvutuse tase
description: Selles teemas kirjeldatakse koosluse (BOM) taset, mille nimi on kuluarvutuse tase. See koosluse tase ei arvesta arvutamisel ei tootmis- ega partiitellimusi.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839483"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="e99a5-104">Kuluarvutuse tase</span><span class="sxs-lookup"><span data-stu-id="e99a5-104">Cost calculation level</span></span>

<span data-ttu-id="e99a5-105">Koosluse (BOM) taseme puhul, mille nimi on **Kulu arvutamise tase**, ei arvestata arvutamisel ei tootmis- ega partiitellimusi.</span><span class="sxs-lookup"><span data-stu-id="e99a5-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="e99a5-106">Süsteem kasutab seda taset kuluarvutuse versioonides kulu arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="e99a5-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="e99a5-107">Protsessides, nagu ümberarvutamine ja lao sulgemine, kasutab süsteem hoopis koosluse taset **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="e99a5-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="e99a5-108">Järgmises lihtsas stsenaariumis on näha, mille poolest erinevad koosluse tase **Kulu arvutamise tase** ja koosluse tase **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="e99a5-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="e99a5-109">Teil on kolm toodet: A, B ja C. Toode C on toote B komponent ning toode B on toote A komponent.</span><span class="sxs-lookup"><span data-stu-id="e99a5-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="e99a5-110">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="e99a5-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="e99a5-111">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="e99a5-111">**Product A:** 0</span></span>
    - <span data-ttu-id="e99a5-112">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="e99a5-112">**Product B:** 1</span></span>
    - <span data-ttu-id="e99a5-113">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="e99a5-113">**Product C:** 2</span></span>

- <span data-ttu-id="e99a5-114">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="e99a5-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="e99a5-115">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="e99a5-115">**Product A:** 0</span></span>
    - <span data-ttu-id="e99a5-116">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="e99a5-116">**Product B:** 1</span></span>
    - <span data-ttu-id="e99a5-117">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="e99a5-117">**Product C:** 2</span></span>

<span data-ttu-id="e99a5-118">Seejärel luuakse tootmistellimus toote C jaoks ning toode A lisatakse tootmistellimuse kooslusesse.</span><span class="sxs-lookup"><span data-stu-id="e99a5-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="e99a5-119">Pärast tellimuse hindamist uuendatakse koosluse tasemed järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="e99a5-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="e99a5-120">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="e99a5-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="e99a5-121">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="e99a5-121">**Product B:** 1</span></span>
    - <span data-ttu-id="e99a5-122">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="e99a5-122">**Product C:** 2</span></span>
    - <span data-ttu-id="e99a5-123">**Toode A:** 3</span><span class="sxs-lookup"><span data-stu-id="e99a5-123">**Product A:** 3</span></span>

- <span data-ttu-id="e99a5-124">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="e99a5-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="e99a5-125">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="e99a5-125">**Product A:** 0</span></span>
    - <span data-ttu-id="e99a5-126">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="e99a5-126">**Product B:** 1</span></span>
    - <span data-ttu-id="e99a5-127">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="e99a5-127">**Product C:** 2</span></span>

<span data-ttu-id="e99a5-128">Selline käitumine tagab, et tootmistellimuse kooslustes tehtud muudatused ei mõjuta hilisemat kulu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="e99a5-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]