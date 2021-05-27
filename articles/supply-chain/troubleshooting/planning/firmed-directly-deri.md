---
title: Otse tuletatud ja kindlad tellimused töödeldakse ülevaatuse töövooga
description: Otse tuletatud ja kindlad tellimused töödeldakse ülevaatuse töövooga.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026447"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="e28ff-103">Otse tuletatud ja kindlad tellimused töödeldakse ülevaatuse töövooga</span><span class="sxs-lookup"><span data-stu-id="e28ff-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="e28ff-104">KB number: 4612450</span><span class="sxs-lookup"><span data-stu-id="e28ff-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="e28ff-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="e28ff-105">Symptoms</span></span>

<span data-ttu-id="e28ff-106">Otse tuletatud ja kindlad tellimused töödeldakse *ülevaatuse* töövooga.</span><span class="sxs-lookup"><span data-stu-id="e28ff-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="e28ff-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="e28ff-107">Resolution</span></span>

<span data-ttu-id="e28ff-108">Kui juhtumi muudatuste jälgimine on lubatud, kuvatakse kindlad tuletatud tellimused (allhanke ostutellimused) olekuks *Ülevaatus*.</span><span class="sxs-lookup"><span data-stu-id="e28ff-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="e28ff-109">Seega, kui ostutellimus on tuletatud (allhanke ostutellimus), on see esitatud ainult töövoole.</span><span class="sxs-lookup"><span data-stu-id="e28ff-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="e28ff-110">Kui ostutellimus on kinnitatud kui plaanitud ostutellimus, kinnitatakse see automaatselt, kindlustamaks, et plaanimismootor ei looks uusi plaanitud tellimusi, kui ostutellimus on veel olekus *Mustand*.</span><span class="sxs-lookup"><span data-stu-id="e28ff-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
