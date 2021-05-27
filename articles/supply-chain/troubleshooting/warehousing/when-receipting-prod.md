---
title: Ühele kviitungile prinditakse mitme tööpäise jaoks ainult üks silt
description: Ühele kviitungile prinditakse mitme tööpäise jaoks ainult üks silt.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026438"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="55cb7-103">Ühele kviitungile prinditakse mitme tööpäise jaoks ainult üks silt</span><span class="sxs-lookup"><span data-stu-id="55cb7-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="55cb7-104">KB number: 4614667</span><span class="sxs-lookup"><span data-stu-id="55cb7-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="55cb7-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="55cb7-105">Symptoms</span></span>

<span data-ttu-id="55cb7-106">Mitu tööpäist luuakse samale sihtlitsentsiplaadile osana ühest laorakenduse vastuvõtusündmusest.</span><span class="sxs-lookup"><span data-stu-id="55cb7-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="55cb7-107">Toote saabumisel prinditakse siiski ainult üks litsentsiplaadi silt.</span><span class="sxs-lookup"><span data-stu-id="55cb7-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="55cb7-108">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="55cb7-108">Resolution</span></span>

<span data-ttu-id="55cb7-109">Süsteem käitub kavandatud viisil.</span><span class="sxs-lookup"><span data-stu-id="55cb7-109">The system is behaving as designed.</span></span>

<span data-ttu-id="55cb7-110">Praeguses kujunduses luuakse alati üks litsentsiplaadi silt, sõltumata töö päise ja töörea kombinatsioonide arvust.</span><span class="sxs-lookup"><span data-stu-id="55cb7-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="55cb7-111">Loodud silt sisaldab teavet ainult ühe kombinatsiooni kohta.</span><span class="sxs-lookup"><span data-stu-id="55cb7-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="55cb7-112">Selle probleemi lahendamiseks veenduge, et töö päise loomine on alati vastendatud ainult ühe sihtlitsentsiplaadiga.</span><span class="sxs-lookup"><span data-stu-id="55cb7-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
