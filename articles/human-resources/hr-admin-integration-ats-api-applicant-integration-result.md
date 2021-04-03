---
title: Kandidaadi integratsiooni tulemus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti kandidaadi integreerimise tulemus.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467549"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="0d444-103">Kandidaadi integratsiooni tulemus</span><span class="sxs-lookup"><span data-stu-id="0d444-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0d444-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti kandidaadi integreerimise tulemus.</span><span class="sxs-lookup"><span data-stu-id="0d444-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0d444-105">Füüsiline nimi: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="0d444-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="0d444-106">See loetelu annab kandidaadi kirjele oleku.</span><span class="sxs-lookup"><span data-stu-id="0d444-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="0d444-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="0d444-107">Value</span></span> | <span data-ttu-id="0d444-108">Silt</span><span class="sxs-lookup"><span data-stu-id="0d444-108">Label</span></span> | <span data-ttu-id="0d444-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0d444-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0d444-110">200000000</span><span class="sxs-lookup"><span data-stu-id="0d444-110">200000000</span></span> | <span data-ttu-id="0d444-111">Töötlemata</span><span class="sxs-lookup"><span data-stu-id="0d444-111">Not processed</span></span> | <span data-ttu-id="0d444-112">Kandidaat on endiselt kaalumisel.</span><span class="sxs-lookup"><span data-stu-id="0d444-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="0d444-113">200000001</span><span class="sxs-lookup"><span data-stu-id="0d444-113">200000001</span></span> | <span data-ttu-id="0d444-114">Palgatud</span><span class="sxs-lookup"><span data-stu-id="0d444-114">Hired</span></span> | <span data-ttu-id="0d444-115">Kandidaat on palgatud.</span><span class="sxs-lookup"><span data-stu-id="0d444-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="0d444-116">200000002</span><span class="sxs-lookup"><span data-stu-id="0d444-116">200000002</span></span> | <span data-ttu-id="0d444-117">Palkamata</span><span class="sxs-lookup"><span data-stu-id="0d444-117">Not hired</span></span> | <span data-ttu-id="0d444-118">Otsustati kandidaati mitte palgata.</span><span class="sxs-lookup"><span data-stu-id="0d444-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="0d444-119">200000003</span><span class="sxs-lookup"><span data-stu-id="0d444-119">200000003</span></span> | <span data-ttu-id="0d444-120">Lõpetatud</span><span class="sxs-lookup"><span data-stu-id="0d444-120">Dismissed</span></span> | <span data-ttu-id="0d444-121">Kandidaat jäeti kaalumiselt välja.</span><span class="sxs-lookup"><span data-stu-id="0d444-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0d444-122">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0d444-122">See also</span></span>

[<span data-ttu-id="0d444-123">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="0d444-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0d444-124">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="0d444-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]