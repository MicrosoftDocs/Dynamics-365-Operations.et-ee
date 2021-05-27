---
title: Väljastatud tooted V2 üksuse abil ei saa kaupa importida
description: Üksust Released kasutades välja antud tooted V2 ei saa importida.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026431"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="7d86e-103">Väljastatud tooted V2 üksuse abil ei saa kaupa importida</span><span class="sxs-lookup"><span data-stu-id="7d86e-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="7d86e-104">KB number: 4611825</span><span class="sxs-lookup"><span data-stu-id="7d86e-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="7d86e-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="7d86e-105">Symptoms</span></span>

<span data-ttu-id="7d86e-106">Kui proovite kaupa importida, kasutades üksust *Väljastatud tooted V2* saate tõrketeate, mis sarnaneb järgmise näitega:</span><span class="sxs-lookup"><span data-stu-id="7d86e-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="7d86e-107">Kirjeid ei saa luua rakenduses Items – jälgides dimensioonigruppe (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="7d86e-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="7d86e-108">Kauba number: 2040663, partii.</span><span class="sxs-lookup"><span data-stu-id="7d86e-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="7d86e-109">Kirje on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="7d86e-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="7d86e-110">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="7d86e-110">Resolution</span></span>

<span data-ttu-id="7d86e-111">Uute väljastatud toodete importimiseks peate *Väljastatud toote loomise V2* üksuse kasutama üksuse *Väljastatud tooted V2* asemel.</span><span class="sxs-lookup"><span data-stu-id="7d86e-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
