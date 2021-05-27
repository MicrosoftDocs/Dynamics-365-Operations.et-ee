---
title: Alustatud karantiinitellimuse kogust tellimuse jagamisel ei värskendata
description: Kui loote karantiinitellimuse ja proovite seda tükeldada, ei uuendata tellimuse kogust järelejäänud tükeldatud koguseks.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026452"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="93968-103">Alustatud karantiinitellimuse kogust tellimuse jagamisel ei värskendata</span><span class="sxs-lookup"><span data-stu-id="93968-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="93968-104">KB number: 4613113</span><span class="sxs-lookup"><span data-stu-id="93968-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="93968-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="93968-105">Symptoms</span></span>

<span data-ttu-id="93968-106">Kui loote karantiinitellimuse ja proovite seda tükeldada, ei uuendata tellimuse kogust pärast jagamist järelejäänud koguseks.</span><span class="sxs-lookup"><span data-stu-id="93968-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="93968-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="93968-107">Resolution</span></span>

<span data-ttu-id="93968-108">Süsteem ei muuda karantiinikorralduse algset kogust, tagamaks, et saate jälgida selle vahelao orderi jaoks loodud algset kogust.</span><span class="sxs-lookup"><span data-stu-id="93968-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="93968-109">Süsteem jälgib siiski karantiinitellimusest jagatud kogust.</span><span class="sxs-lookup"><span data-stu-id="93968-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="93968-110">Selleks jälituse jaoks kasutab see andmebaasi välja nimega `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="93968-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="93968-111">Kuid seda välja ei kuvata kasutajaliideses (UI).</span><span class="sxs-lookup"><span data-stu-id="93968-111">However, this field isn't visible in the user interface (UI).</span></span>
