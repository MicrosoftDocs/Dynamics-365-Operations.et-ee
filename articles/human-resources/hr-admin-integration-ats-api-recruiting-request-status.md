---
title: Värbamistaotluse olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464642"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="fa444-103">Värbamistaotluse olek</span><span class="sxs-lookup"><span data-stu-id="fa444-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fa444-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.</span><span class="sxs-lookup"><span data-stu-id="fa444-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="fa444-105">Füüsiline nimi: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="fa444-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="fa444-106">See loetelu annab kandidaatide värbamistaotluste oleku väärtuste suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="fa444-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="fa444-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="fa444-107">Value</span></span> | <span data-ttu-id="fa444-108">Silt</span><span class="sxs-lookup"><span data-stu-id="fa444-108">Label</span></span> | <span data-ttu-id="fa444-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fa444-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fa444-110">200000000</span><span class="sxs-lookup"><span data-stu-id="fa444-110">200000000</span></span> | <span data-ttu-id="fa444-111">Mustand</span><span class="sxs-lookup"><span data-stu-id="fa444-111">Draft</span></span> | <span data-ttu-id="fa444-112">Taotlus on mustandis ja ei ole valmis aktiivseks värbamiseks.</span><span class="sxs-lookup"><span data-stu-id="fa444-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="fa444-113">200000001</span><span class="sxs-lookup"><span data-stu-id="fa444-113">200000001</span></span> | <span data-ttu-id="fa444-114">Ülevaatamisel</span><span class="sxs-lookup"><span data-stu-id="fa444-114">In Review</span></span> | <span data-ttu-id="fa444-115">Taotlus on esitatud ja töövoog suunab selle kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="fa444-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="fa444-116">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="fa444-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="fa444-117">200000002</span><span class="sxs-lookup"><span data-stu-id="fa444-117">200000002</span></span> | <span data-ttu-id="fa444-118">Ootel</span><span class="sxs-lookup"><span data-stu-id="fa444-118">Pending</span></span> | <span data-ttu-id="fa444-119">Taotlus on töövoo tegevuse ootel.</span><span class="sxs-lookup"><span data-stu-id="fa444-119">The request is pending workflow action.</span></span> <span data-ttu-id="fa444-120">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="fa444-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="fa444-121">200000003</span><span class="sxs-lookup"><span data-stu-id="fa444-121">200000003</span></span> | <span data-ttu-id="fa444-122">Tühistatud</span><span class="sxs-lookup"><span data-stu-id="fa444-122">Canceled</span></span> | <span data-ttu-id="fa444-123">Taotlus on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="fa444-123">The request has been canceled.</span></span> <span data-ttu-id="fa444-124">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="fa444-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="fa444-125">200000004</span><span class="sxs-lookup"><span data-stu-id="fa444-125">200000004</span></span> | <span data-ttu-id="fa444-126">Keelatud</span><span class="sxs-lookup"><span data-stu-id="fa444-126">Denied</span></span> | <span data-ttu-id="fa444-127">Taotlusest keelduti.</span><span class="sxs-lookup"><span data-stu-id="fa444-127">The request has been denied.</span></span> <span data-ttu-id="fa444-128">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="fa444-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="fa444-129">200000005</span><span class="sxs-lookup"><span data-stu-id="fa444-129">200000005</span></span> | <span data-ttu-id="fa444-130">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="fa444-130">Active</span></span> | <span data-ttu-id="fa444-131">Mis tahes töövoog on lõpetatud ja kinnitatud ning taotlus on aktiivseks värbamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="fa444-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="fa444-132">200000006</span><span class="sxs-lookup"><span data-stu-id="fa444-132">200000006</span></span> | <span data-ttu-id="fa444-133">Suletud</span><span class="sxs-lookup"><span data-stu-id="fa444-133">Closed</span></span> | <span data-ttu-id="fa444-134">Värbamistaotlus on suletud.</span><span class="sxs-lookup"><span data-stu-id="fa444-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fa444-135">Vt ka</span><span class="sxs-lookup"><span data-stu-id="fa444-135">See also</span></span>

[<span data-ttu-id="fa444-136">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="fa444-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="fa444-137">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="fa444-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]