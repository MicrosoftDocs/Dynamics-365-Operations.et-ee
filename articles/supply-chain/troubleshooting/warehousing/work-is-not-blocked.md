---
title: Töö pole blokeeritud
description: Töö pole blokeeritud
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924200"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="0d139-103">Töö pole blokeeritud</span><span class="sxs-lookup"><span data-stu-id="0d139-103">Work isn't blocked</span></span>

<span data-ttu-id="0d139-104">Tõrkekood: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="0d139-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="0d139-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="0d139-105">Symptoms</span></span>

<span data-ttu-id="0d139-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="0d139-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0d139-107">Töö ID-ga %1 pole blokeeritud.</span><span class="sxs-lookup"><span data-stu-id="0d139-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="0d139-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="0d139-108">Cause</span></span>

<span data-ttu-id="0d139-109">**Blokeeritud voo** suvand on seatud väärtusele *Ei*.</span><span class="sxs-lookup"><span data-stu-id="0d139-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="0d139-110">Töö blokeeringut ei saa eemaldada, kuna see pole praegu blokeeritud.</span><span class="sxs-lookup"><span data-stu-id="0d139-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="0d139-111">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="0d139-111">Resolution</span></span>

 <span data-ttu-id="0d139-112">Ainult tööl, mille **Blokeeritud voo** suvand on seatud valikule *Jah* saab blokeeringu eemaldada.</span><span class="sxs-lookup"><span data-stu-id="0d139-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
