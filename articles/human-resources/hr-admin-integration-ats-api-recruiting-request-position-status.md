---
title: Värbamistaotluse ametikoha olek
description: Selles teemas kirjeldatakse värbamisetaotluse ametikoha oleku suvandikomplekti rakenduses Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789728"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="1bd34-103">Värbamistaotluse ametikoha olek</span><span class="sxs-lookup"><span data-stu-id="1bd34-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1bd34-104">Selles teemas kirjeldatakse värbamisetaotluse ametikoha oleku suvandikomplekti rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1bd34-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1bd34-105">Füüsiline nimi: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="1bd34-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="1bd34-106">See loetelu annab olemis RecruitingRequestPosition iga värbamistaotluse ametikoha väärtuste oleku suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="1bd34-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="1bd34-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="1bd34-107">Value</span></span> | <span data-ttu-id="1bd34-108">Silt</span><span class="sxs-lookup"><span data-stu-id="1bd34-108">Label</span></span> | <span data-ttu-id="1bd34-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1bd34-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1bd34-110">200000000</span><span class="sxs-lookup"><span data-stu-id="1bd34-110">200000000</span></span> | <span data-ttu-id="1bd34-111">Avamine</span><span class="sxs-lookup"><span data-stu-id="1bd34-111">Open</span></span> | <span data-ttu-id="1bd34-112">Värbamistaotluse ametikoht on värbamiseks vaba.</span><span class="sxs-lookup"><span data-stu-id="1bd34-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="1bd34-113">See ei näita, et ametikohale puuduksid hetkel aktiivesd ametikoha määramised.</span><span class="sxs-lookup"><span data-stu-id="1bd34-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="1bd34-114">Värbamise ajal võib ametikohal töötaja olla.</span><span class="sxs-lookup"><span data-stu-id="1bd34-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="1bd34-115">See näitab ainult seda, et ametikoht on värbamistaotluse kontekstis värbamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="1bd34-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="1bd34-116">200000001</span><span class="sxs-lookup"><span data-stu-id="1bd34-116">200000001</span></span> | <span data-ttu-id="1bd34-117">Täidetud</span><span class="sxs-lookup"><span data-stu-id="1bd34-117">Filled</span></span> | <span data-ttu-id="1bd34-118">Töötaja on ametikohale määramiseks valitud.</span><span class="sxs-lookup"><span data-stu-id="1bd34-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="1bd34-119">200000002</span><span class="sxs-lookup"><span data-stu-id="1bd34-119">200000002</span></span> | <span data-ttu-id="1bd34-120">Tühistatud</span><span class="sxs-lookup"><span data-stu-id="1bd34-120">Canceled</span></span> | <span data-ttu-id="1bd34-121">Taotlus sellele ametikohale värbamiseks on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="1bd34-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1bd34-122">Vt ka</span><span class="sxs-lookup"><span data-stu-id="1bd34-122">See also</span></span>

[<span data-ttu-id="1bd34-123">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="1bd34-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="1bd34-124">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="1bd34-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]