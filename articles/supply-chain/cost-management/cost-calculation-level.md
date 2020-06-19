---
title: Kuluarvutuse tase
description: Selles teemas kirjeldatakse koosluse (BOM) taset, mille nimi on kuluarvutuse tase. See koosluse tase ei arvesta arvutamisel ei tootmis- ega partiitellimusi.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410942"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="681a8-104">Kuluarvutuse tase</span><span class="sxs-lookup"><span data-stu-id="681a8-104">Cost calculation level</span></span>

<span data-ttu-id="681a8-105">Koosluse (BOM) taseme puhul, mille nimi on **Kulu arvutamise tase**, ei arvestata arvutamisel ei tootmis- ega partiitellimusi.</span><span class="sxs-lookup"><span data-stu-id="681a8-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="681a8-106">Süsteem kasutab seda taset kuluarvutuse versioonides kulu arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="681a8-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="681a8-107">Protsessides, nagu ümberarvutamine ja lao sulgemine, kasutab süsteem hoopis koosluse taset **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="681a8-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="681a8-108">Järgmises lihtsas stsenaariumis on näha, mille poolest erinevad koosluse tase **Kulu arvutamise tase** ja koosluse tase **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="681a8-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="681a8-109">Teil on kolm toodet: A, B ja C. Toode C on toote B komponent ning toode B on toote A komponent.</span><span class="sxs-lookup"><span data-stu-id="681a8-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="681a8-110">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="681a8-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="681a8-111">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="681a8-111">**Product A:** 0</span></span>
    - <span data-ttu-id="681a8-112">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="681a8-112">**Product B:** 1</span></span>
    - <span data-ttu-id="681a8-113">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="681a8-113">**Product C:** 2</span></span>

- <span data-ttu-id="681a8-114">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="681a8-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="681a8-115">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="681a8-115">**Product A:** 0</span></span>
    - <span data-ttu-id="681a8-116">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="681a8-116">**Product B:** 1</span></span>
    - <span data-ttu-id="681a8-117">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="681a8-117">**Product C:** 2</span></span>

<span data-ttu-id="681a8-118">Seejärel luuakse tootmistellimus toote C jaoks ning toode A lisatakse tootmistellimuse kooslusesse.</span><span class="sxs-lookup"><span data-stu-id="681a8-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="681a8-119">Pärast tellimuse hindamist uuendatakse koosluse tasemed järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="681a8-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="681a8-120">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="681a8-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="681a8-121">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="681a8-121">**Product B:** 1</span></span>
    - <span data-ttu-id="681a8-122">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="681a8-122">**Product C:** 2</span></span>
    - <span data-ttu-id="681a8-123">**Toode A:** 3</span><span class="sxs-lookup"><span data-stu-id="681a8-123">**Product A:** 3</span></span>

- <span data-ttu-id="681a8-124">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="681a8-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="681a8-125">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="681a8-125">**Product A:** 0</span></span>
    - <span data-ttu-id="681a8-126">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="681a8-126">**Product B:** 1</span></span>
    - <span data-ttu-id="681a8-127">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="681a8-127">**Product C:** 2</span></span>

<span data-ttu-id="681a8-128">Selline käitumine tagab, et tootmistellimuse kooslustes tehtud muudatused ei mõjuta hilisemat kulu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="681a8-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
