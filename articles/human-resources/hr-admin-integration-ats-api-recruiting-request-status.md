---
title: Värbamistaotluse olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.
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
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806038"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="107dc-103">Värbamistaotluse olek</span><span class="sxs-lookup"><span data-stu-id="107dc-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="107dc-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.</span><span class="sxs-lookup"><span data-stu-id="107dc-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="107dc-105">Füüsiline nimi: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="107dc-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="107dc-106">See loetelu annab kandidaatide värbamistaotluste oleku väärtuste suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="107dc-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="107dc-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="107dc-107">Value</span></span> | <span data-ttu-id="107dc-108">Silt</span><span class="sxs-lookup"><span data-stu-id="107dc-108">Label</span></span> | <span data-ttu-id="107dc-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="107dc-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="107dc-110">200000000</span><span class="sxs-lookup"><span data-stu-id="107dc-110">200000000</span></span> | <span data-ttu-id="107dc-111">Mustand</span><span class="sxs-lookup"><span data-stu-id="107dc-111">Draft</span></span> | <span data-ttu-id="107dc-112">Taotlus on mustandis ja ei ole valmis aktiivseks värbamiseks.</span><span class="sxs-lookup"><span data-stu-id="107dc-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="107dc-113">200000001</span><span class="sxs-lookup"><span data-stu-id="107dc-113">200000001</span></span> | <span data-ttu-id="107dc-114">Ülevaatamisel</span><span class="sxs-lookup"><span data-stu-id="107dc-114">In Review</span></span> | <span data-ttu-id="107dc-115">Taotlus on esitatud ja töövoog suunab selle kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="107dc-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="107dc-116">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="107dc-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="107dc-117">200000002</span><span class="sxs-lookup"><span data-stu-id="107dc-117">200000002</span></span> | <span data-ttu-id="107dc-118">Ootel</span><span class="sxs-lookup"><span data-stu-id="107dc-118">Pending</span></span> | <span data-ttu-id="107dc-119">Taotlus on töövoo tegevuse ootel.</span><span class="sxs-lookup"><span data-stu-id="107dc-119">The request is pending workflow action.</span></span> <span data-ttu-id="107dc-120">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="107dc-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="107dc-121">200000003</span><span class="sxs-lookup"><span data-stu-id="107dc-121">200000003</span></span> | <span data-ttu-id="107dc-122">Tühistatud</span><span class="sxs-lookup"><span data-stu-id="107dc-122">Canceled</span></span> | <span data-ttu-id="107dc-123">Taotlus on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="107dc-123">The request has been canceled.</span></span> <span data-ttu-id="107dc-124">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="107dc-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="107dc-125">200000004</span><span class="sxs-lookup"><span data-stu-id="107dc-125">200000004</span></span> | <span data-ttu-id="107dc-126">Keelatud</span><span class="sxs-lookup"><span data-stu-id="107dc-126">Denied</span></span> | <span data-ttu-id="107dc-127">Taotlusest keelduti.</span><span class="sxs-lookup"><span data-stu-id="107dc-127">The request has been denied.</span></span> <span data-ttu-id="107dc-128">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="107dc-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="107dc-129">200000005</span><span class="sxs-lookup"><span data-stu-id="107dc-129">200000005</span></span> | <span data-ttu-id="107dc-130">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="107dc-130">Active</span></span> | <span data-ttu-id="107dc-131">Mis tahes töövoog on lõpetatud ja kinnitatud ning taotlus on aktiivseks värbamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="107dc-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="107dc-132">200000006</span><span class="sxs-lookup"><span data-stu-id="107dc-132">200000006</span></span> | <span data-ttu-id="107dc-133">Suletud</span><span class="sxs-lookup"><span data-stu-id="107dc-133">Closed</span></span> | <span data-ttu-id="107dc-134">Värbamistaotlus on suletud.</span><span class="sxs-lookup"><span data-stu-id="107dc-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="107dc-135">Vt ka</span><span class="sxs-lookup"><span data-stu-id="107dc-135">See also</span></span>

[<span data-ttu-id="107dc-136">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="107dc-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="107dc-137">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="107dc-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]