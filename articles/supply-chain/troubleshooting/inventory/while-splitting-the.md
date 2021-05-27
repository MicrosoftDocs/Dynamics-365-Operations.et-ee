---
title: Tegeliku kaalu koguse jaotamisel kasutatakse nimikoguse asemel miinimumkogust
description: Tegeliku kaaluga koguse tükeldamisel partiiks kasutab välja Komplekteeritud kogus kaubale määratud miinimumkogust, mitte nominaalkogust.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026448"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="6394c-103">Tegeliku kaalu koguse jaotamisel kasutatakse nimikoguse asemel miinimumkogust</span><span class="sxs-lookup"><span data-stu-id="6394c-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="6394c-104">KB-number: 4612073</span><span class="sxs-lookup"><span data-stu-id="6394c-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="6394c-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="6394c-105">Symptoms</span></span>

<span data-ttu-id="6394c-106">Tegeliku kaaluga koguse tükeldamisel partiiks kasutab välja **Komplekteeritud kogus** kaubale määratud miinimumkogust, mitte nominaalkogust.</span><span class="sxs-lookup"><span data-stu-id="6394c-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="6394c-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="6394c-107">Resolution</span></span>

<span data-ttu-id="6394c-108">Süsteem käitub kavandatud viisil.</span><span class="sxs-lookup"><span data-stu-id="6394c-108">The system is behaving as designed.</span></span> <span data-ttu-id="6394c-109">Süsteem kasutab komplekteerimiseks iga kauba minimaalse koguse seadistust.</span><span class="sxs-lookup"><span data-stu-id="6394c-109">The system uses each item's minimum quantity setup for picking.</span></span>
