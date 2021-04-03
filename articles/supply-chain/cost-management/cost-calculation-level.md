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
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251022"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="cf010-104">Kuluarvutuse tase</span><span class="sxs-lookup"><span data-stu-id="cf010-104">Cost calculation level</span></span>

<span data-ttu-id="cf010-105">Koosluse (BOM) taseme puhul, mille nimi on **Kulu arvutamise tase**, ei arvestata arvutamisel ei tootmis- ega partiitellimusi.</span><span class="sxs-lookup"><span data-stu-id="cf010-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="cf010-106">Süsteem kasutab seda taset kuluarvutuse versioonides kulu arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="cf010-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="cf010-107">Protsessides, nagu ümberarvutamine ja lao sulgemine, kasutab süsteem hoopis koosluse taset **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="cf010-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="cf010-108">Järgmises lihtsas stsenaariumis on näha, mille poolest erinevad koosluse tase **Kulu arvutamise tase** ja koosluse tase **Kuluarvutuse tase**.</span><span class="sxs-lookup"><span data-stu-id="cf010-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="cf010-109">Teil on kolm toodet: A, B ja C. Toode C on toote B komponent ning toode B on toote A komponent.</span><span class="sxs-lookup"><span data-stu-id="cf010-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="cf010-110">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="cf010-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="cf010-111">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="cf010-111">**Product A:** 0</span></span>
    - <span data-ttu-id="cf010-112">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="cf010-112">**Product B:** 1</span></span>
    - <span data-ttu-id="cf010-113">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="cf010-113">**Product C:** 2</span></span>

- <span data-ttu-id="cf010-114">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="cf010-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="cf010-115">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="cf010-115">**Product A:** 0</span></span>
    - <span data-ttu-id="cf010-116">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="cf010-116">**Product B:** 1</span></span>
    - <span data-ttu-id="cf010-117">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="cf010-117">**Product C:** 2</span></span>

<span data-ttu-id="cf010-118">Seejärel luuakse tootmistellimus toote C jaoks ning toode A lisatakse tootmistellimuse kooslusesse.</span><span class="sxs-lookup"><span data-stu-id="cf010-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="cf010-119">Pärast tellimuse hindamist uuendatakse koosluse tasemed järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="cf010-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="cf010-120">**Kuluarvutuse tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="cf010-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="cf010-121">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="cf010-121">**Product B:** 1</span></span>
    - <span data-ttu-id="cf010-122">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="cf010-122">**Product C:** 2</span></span>
    - <span data-ttu-id="cf010-123">**Toode A:** 3</span><span class="sxs-lookup"><span data-stu-id="cf010-123">**Product A:** 3</span></span>

- <span data-ttu-id="cf010-124">**Kulu arvutamise tase** määrab järgmised koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="cf010-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="cf010-125">**Toode A:** 0</span><span class="sxs-lookup"><span data-stu-id="cf010-125">**Product A:** 0</span></span>
    - <span data-ttu-id="cf010-126">**Toode B:** 1</span><span class="sxs-lookup"><span data-stu-id="cf010-126">**Product B:** 1</span></span>
    - <span data-ttu-id="cf010-127">**Toode C:** 2</span><span class="sxs-lookup"><span data-stu-id="cf010-127">**Product C:** 2</span></span>

<span data-ttu-id="cf010-128">Selline käitumine tagab, et tootmistellimuse kooslustes tehtud muudatused ei mõjuta hilisemat kulu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="cf010-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]