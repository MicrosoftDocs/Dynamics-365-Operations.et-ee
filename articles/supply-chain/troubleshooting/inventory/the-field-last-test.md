---
title: Välja Viimase testimise kuupäev ei uuendata mitme kvaliteettellimuse loomisel
description: Välja Viimase testimise kuupäev ei uuendata mitme kvaliteettellimuse loomisel.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026450"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="e8202-103">Välja Viimase testimise kuupäev ei uuendata mitme kvaliteettellimuse loomisel</span><span class="sxs-lookup"><span data-stu-id="e8202-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="e8202-104">KB number: 4612803</span><span class="sxs-lookup"><span data-stu-id="e8202-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="e8202-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="e8202-105">Symptoms</span></span>

<span data-ttu-id="e8202-106">Välja **Viimase testimise** kuupäev ei uuendata mitme kvaliteettellimuse loomisel.</span><span class="sxs-lookup"><span data-stu-id="e8202-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="e8202-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="e8202-107">Resolution</span></span>

<span data-ttu-id="e8202-108">Süsteem käitub kavandatud viisil.</span><span class="sxs-lookup"><span data-stu-id="e8202-108">The system is behaving as designed.</span></span> <span data-ttu-id="e8202-109">Viimane testitud kuupäev ei ole seotud kvaliteettellimustega.</span><span class="sxs-lookup"><span data-stu-id="e8202-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="e8202-110">See säilitab kuupäeva, mil lõpetatud kaubad esimest korda osteti või toodeti.</span><span class="sxs-lookup"><span data-stu-id="e8202-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="e8202-111">Seda kuupäeva kasutatakse kõlblikkusaja nõuande kuupäeva arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="e8202-111">This date is used to calculate the shelf life advice date.</span></span>
