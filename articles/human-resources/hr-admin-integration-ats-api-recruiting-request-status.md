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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125950"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="a09f6-103">Värbamistaotluse olek</span><span class="sxs-lookup"><span data-stu-id="a09f6-103">Recruiting request status</span></span>

<span data-ttu-id="a09f6-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.</span><span class="sxs-lookup"><span data-stu-id="a09f6-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a09f6-105">Füüsiline nimi: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="a09f6-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="a09f6-106">See loetelu annab kandidaatide värbamistaotluste oleku väärtuste suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="a09f6-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="a09f6-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="a09f6-107">Value</span></span> | <span data-ttu-id="a09f6-108">Silt</span><span class="sxs-lookup"><span data-stu-id="a09f6-108">Label</span></span> | <span data-ttu-id="a09f6-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a09f6-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a09f6-110">200000000</span><span class="sxs-lookup"><span data-stu-id="a09f6-110">200000000</span></span> | <span data-ttu-id="a09f6-111">Mustand</span><span class="sxs-lookup"><span data-stu-id="a09f6-111">Draft</span></span> | <span data-ttu-id="a09f6-112">Taotlus on mustandis ja ei ole valmis aktiivseks värbamiseks.</span><span class="sxs-lookup"><span data-stu-id="a09f6-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="a09f6-113">200000001</span><span class="sxs-lookup"><span data-stu-id="a09f6-113">200000001</span></span> | <span data-ttu-id="a09f6-114">Ülevaatamisel</span><span class="sxs-lookup"><span data-stu-id="a09f6-114">In Review</span></span> | <span data-ttu-id="a09f6-115">Taotlus on esitatud ja töövoog suunab selle kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="a09f6-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="a09f6-116">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="a09f6-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a09f6-117">200000002</span><span class="sxs-lookup"><span data-stu-id="a09f6-117">200000002</span></span> | <span data-ttu-id="a09f6-118">Ootel</span><span class="sxs-lookup"><span data-stu-id="a09f6-118">Pending</span></span> | <span data-ttu-id="a09f6-119">Taotlus on töövoo tegevuse ootel.</span><span class="sxs-lookup"><span data-stu-id="a09f6-119">The request is pending workflow action.</span></span> <span data-ttu-id="a09f6-120">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="a09f6-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a09f6-121">200000003</span><span class="sxs-lookup"><span data-stu-id="a09f6-121">200000003</span></span> | <span data-ttu-id="a09f6-122">Tühistatud</span><span class="sxs-lookup"><span data-stu-id="a09f6-122">Canceled</span></span> | <span data-ttu-id="a09f6-123">Taotlus on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="a09f6-123">The request has been canceled.</span></span> <span data-ttu-id="a09f6-124">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="a09f6-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a09f6-125">200000004</span><span class="sxs-lookup"><span data-stu-id="a09f6-125">200000004</span></span> | <span data-ttu-id="a09f6-126">Keelatud</span><span class="sxs-lookup"><span data-stu-id="a09f6-126">Denied</span></span> | <span data-ttu-id="a09f6-127">Taotlusest keelduti.</span><span class="sxs-lookup"><span data-stu-id="a09f6-127">The request has been denied.</span></span> <span data-ttu-id="a09f6-128">Saadaval ainult siis, kui töövoog on lubatud.</span><span class="sxs-lookup"><span data-stu-id="a09f6-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a09f6-129">200000005</span><span class="sxs-lookup"><span data-stu-id="a09f6-129">200000005</span></span> | <span data-ttu-id="a09f6-130">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="a09f6-130">Active</span></span> | <span data-ttu-id="a09f6-131">Mis tahes töövoog on lõpetatud ja kinnitatud ning taotlus on aktiivseks värbamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="a09f6-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="a09f6-132">200000006</span><span class="sxs-lookup"><span data-stu-id="a09f6-132">200000006</span></span> | <span data-ttu-id="a09f6-133">Suletud</span><span class="sxs-lookup"><span data-stu-id="a09f6-133">Closed</span></span> | <span data-ttu-id="a09f6-134">Värbamistaotlus on suletud.</span><span class="sxs-lookup"><span data-stu-id="a09f6-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a09f6-135">Vt ka</span><span class="sxs-lookup"><span data-stu-id="a09f6-135">See also</span></span>

[<span data-ttu-id="a09f6-136">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="a09f6-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a09f6-137">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="a09f6-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
