---
title: Värbamistaotluse olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059180"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="05ecd-103">Värbamistaotluse olek</span><span class="sxs-lookup"><span data-stu-id="05ecd-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="05ecd-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.</span><span class="sxs-lookup"><span data-stu-id="05ecd-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="05ecd-105">Füüsiline nimi: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="05ecd-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="05ecd-106">See loetelu annab kandidaatide värbamistaotluste oleku väärtuste suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="05ecd-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="05ecd-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="05ecd-107">Value</span></span> | <span data-ttu-id="05ecd-108">Silt</span><span class="sxs-lookup"><span data-stu-id="05ecd-108">Label</span></span> | <span data-ttu-id="05ecd-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="05ecd-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="05ecd-110">200000000</span><span class="sxs-lookup"><span data-stu-id="05ecd-110">200000000</span></span> | <span data-ttu-id="05ecd-111">Mustand</span><span class="sxs-lookup"><span data-stu-id="05ecd-111">Draft</span></span> | <span data-ttu-id="05ecd-112">Taotlus on mustandis ja ei ole valmis aktiivseks värbamiseks.</span><span class="sxs-lookup"><span data-stu-id="05ecd-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="05ecd-113">200000001</span><span class="sxs-lookup"><span data-stu-id="05ecd-113">200000001</span></span> | <span data-ttu-id="05ecd-114">Ülevaatamisel</span><span class="sxs-lookup"><span data-stu-id="05ecd-114">In Review</span></span> | <span data-ttu-id="05ecd-115">Taotlus on esitatud ja töövoog suunab selle kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="05ecd-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="05ecd-116">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="05ecd-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="05ecd-117">200000002</span><span class="sxs-lookup"><span data-stu-id="05ecd-117">200000002</span></span> | <span data-ttu-id="05ecd-118">Ootel</span><span class="sxs-lookup"><span data-stu-id="05ecd-118">Pending</span></span> | <span data-ttu-id="05ecd-119">Taotlus on töövoo tegevuse ootel.</span><span class="sxs-lookup"><span data-stu-id="05ecd-119">The request is pending workflow action.</span></span> <span data-ttu-id="05ecd-120">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="05ecd-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="05ecd-121">200000003</span><span class="sxs-lookup"><span data-stu-id="05ecd-121">200000003</span></span> | <span data-ttu-id="05ecd-122">Tühistatud</span><span class="sxs-lookup"><span data-stu-id="05ecd-122">Canceled</span></span> | <span data-ttu-id="05ecd-123">Taotlus on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="05ecd-123">The request has been canceled.</span></span> <span data-ttu-id="05ecd-124">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="05ecd-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="05ecd-125">200000004</span><span class="sxs-lookup"><span data-stu-id="05ecd-125">200000004</span></span> | <span data-ttu-id="05ecd-126">Keelatud</span><span class="sxs-lookup"><span data-stu-id="05ecd-126">Denied</span></span> | <span data-ttu-id="05ecd-127">Taotlusest keelduti.</span><span class="sxs-lookup"><span data-stu-id="05ecd-127">The request has been denied.</span></span> <span data-ttu-id="05ecd-128">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="05ecd-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="05ecd-129">200000005</span><span class="sxs-lookup"><span data-stu-id="05ecd-129">200000005</span></span> | <span data-ttu-id="05ecd-130">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="05ecd-130">Active</span></span> | <span data-ttu-id="05ecd-131">Mis tahes töövoog on lõpetatud ja kinnitatud ning taotlus on aktiivseks värbamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="05ecd-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="05ecd-132">200000006</span><span class="sxs-lookup"><span data-stu-id="05ecd-132">200000006</span></span> | <span data-ttu-id="05ecd-133">Suletud</span><span class="sxs-lookup"><span data-stu-id="05ecd-133">Closed</span></span> | <span data-ttu-id="05ecd-134">Värbamistaotlus on suletud.</span><span class="sxs-lookup"><span data-stu-id="05ecd-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="05ecd-135">Vt ka</span><span class="sxs-lookup"><span data-stu-id="05ecd-135">See also</span></span>

[<span data-ttu-id="05ecd-136">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="05ecd-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="05ecd-137">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="05ecd-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]