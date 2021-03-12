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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967721"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="30e76-104">Kuluarvutuse tase</span><span class="sxs-lookup"><span data-stu-id="30e76-104">Cost calculation level</span></span>

<span data-ttu-id="30e76-105">Koosluse (BOM) taseme puhul, mille nimi on **Kulu arvutamise tase**, ei arvestata arvutamisel ei tootmis- ega partiitellimusi.</span><span class="sxs-lookup"><span data-stu-id="30e76-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="30e76-106">Süsteem kasutab seda taset kuluarvutuse versioonides kulu arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="30e76-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="30e76-107">Protsessides, nagu ümberarvutamine ja lao sulgemine, kasutab süsteem hoopis koosluse taset **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="30e76-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="30e76-108">Järgmises lihtsas stsenaariumis on näha, mille poolest erinevad koosluse tase **Kulu arvutamise tase** ja koosluse tase **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="30e76-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="30e76-109">Teil on kolm toodet: A, B ja C. Toode C on toote B komponent ning toode B on toote A komponent.</span><span class="sxs-lookup"><span data-stu-id="30e76-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="30e76-110">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="30e76-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="30e76-111">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="30e76-111">**Product A:** 0</span></span>
    - <span data-ttu-id="30e76-112">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="30e76-112">**Product B:** 1</span></span>
    - <span data-ttu-id="30e76-113">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="30e76-113">**Product C:** 2</span></span>

- <span data-ttu-id="30e76-114">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="30e76-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="30e76-115">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="30e76-115">**Product A:** 0</span></span>
    - <span data-ttu-id="30e76-116">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="30e76-116">**Product B:** 1</span></span>
    - <span data-ttu-id="30e76-117">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="30e76-117">**Product C:** 2</span></span>

<span data-ttu-id="30e76-118">Seejärel luuakse tootmistellimus toote C jaoks ning toode A lisatakse tootmistellimuse kooslusesse.</span><span class="sxs-lookup"><span data-stu-id="30e76-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="30e76-119">Pärast tellimuse hindamist uuendatakse koosluse tasemed järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="30e76-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="30e76-120">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="30e76-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="30e76-121">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="30e76-121">**Product B:** 1</span></span>
    - <span data-ttu-id="30e76-122">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="30e76-122">**Product C:** 2</span></span>
    - <span data-ttu-id="30e76-123">**Toode A:** 3</span><span class="sxs-lookup"><span data-stu-id="30e76-123">**Product A:** 3</span></span>

- <span data-ttu-id="30e76-124">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="30e76-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="30e76-125">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="30e76-125">**Product A:** 0</span></span>
    - <span data-ttu-id="30e76-126">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="30e76-126">**Product B:** 1</span></span>
    - <span data-ttu-id="30e76-127">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="30e76-127">**Product C:** 2</span></span>

<span data-ttu-id="30e76-128">Selline käitumine tagab, et tootmistellimuse kooslustes tehtud muudatused ei mõjuta hilisemat kulu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="30e76-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
