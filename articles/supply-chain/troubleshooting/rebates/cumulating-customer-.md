---
title: Kliendi tagasimaksete kumuleerimine kauba tagasimaksegruppide abil nurjub
description: Kui kasutate kliendi tagasimakseleppeid kombinatsioonis kauba tagasimaksegruppidega, arvutatakse tagasimaksed, kuid kumuleerimine nurjub.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026429"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="c714a-103">Kliendi tagasimaksete kumuleerimine kauba tagasimaksegruppide abil nurjub</span><span class="sxs-lookup"><span data-stu-id="c714a-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="c714a-104">KB number: 4611372</span><span class="sxs-lookup"><span data-stu-id="c714a-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="c714a-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c714a-105">Symptoms</span></span>

<span data-ttu-id="c714a-106">Kui kasutate kliendi tagasimakseleppeid (*summa* tüüp) kombinatsioonis kauba tagasimaksegruppidega, arvutatakse tagasimaksed, kuid kumuleerimine nurjub.</span><span class="sxs-lookup"><span data-stu-id="c714a-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="c714a-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="c714a-107">Resolution</span></span>

<span data-ttu-id="c714a-108">Süsteem käitub kavandatud viisil.</span><span class="sxs-lookup"><span data-stu-id="c714a-108">The system is behaving as designed.</span></span> <span data-ttu-id="c714a-109">Kaubagrupid grupeerivad ainult sama lävitingimusega kaubad.</span><span class="sxs-lookup"><span data-stu-id="c714a-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="c714a-110">Tagasimakse tingimus (lävi) seatakse iga kauba summa suhtes, mitte iga kaubagrupi kauba kumuleeritud summa suhtes.</span><span class="sxs-lookup"><span data-stu-id="c714a-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
