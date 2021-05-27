---
title: Kaudsed kulud protsessiaruandes sisaldab kustutatud tootmist
description: Protsessi kaudsete kulude aruanne sisaldab teavet tootmistellimuste kohta, mis on osaliselt töödeldud ja hiljem kustutatud.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026440"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="c828d-103">Kaudsed kulud protsessiaruandes sisaldab kustutatud tootmist</span><span class="sxs-lookup"><span data-stu-id="c828d-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="c828d-104">KB number: 4612748</span><span class="sxs-lookup"><span data-stu-id="c828d-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="c828d-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c828d-105">Symptoms</span></span>

<span data-ttu-id="c828d-106">**Protsessi kaudsete kulude aruanne** sisaldab teavet tootmistellimuste kohta, mis on osaliselt töödeldud ja hiljem kustutatud.</span><span class="sxs-lookup"><span data-stu-id="c828d-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="c828d-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="c828d-107">Resolution</span></span>

<span data-ttu-id="c828d-108">Tootmistellimuse tühistamisel tühistate ka selle tootmistellimuse kõik kanded.</span><span class="sxs-lookup"><span data-stu-id="c828d-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="c828d-109">Kui kustutate tootmistellimuse, jäävad alles alammooduli tabelid ja pearaamat ning kõik sellega seotud kanded.</span><span class="sxs-lookup"><span data-stu-id="c828d-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="c828d-110">Aruannetes kuvatakse tehingud alamraamatu tabelites.</span><span class="sxs-lookup"><span data-stu-id="c828d-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="c828d-111">Kindla tootmistellimuse netoväärtus peaks olema 0.00.</span><span class="sxs-lookup"><span data-stu-id="c828d-111">For the specific production order, the net value should be 0.00.</span></span>
