---
title: Töö vabastuse olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Töö vabastuse olek.
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464448"
---
# <a name="job-exempt-status"></a><span data-ttu-id="ec999-103">Töö vabastuse olek</span><span class="sxs-lookup"><span data-stu-id="ec999-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ec999-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Töö vabastuse olek.</span><span class="sxs-lookup"><span data-stu-id="ec999-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ec999-105">Füüsiline nimi: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="ec999-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="ec999-106">Selles loetelus määratakse FLSA töö vabastuse oleku väärtuste suvandikomplekt.</span><span class="sxs-lookup"><span data-stu-id="ec999-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="ec999-107">See on esitatud olemasolevas suvandikomplektis cdm_jobexemptstatus.</span><span class="sxs-lookup"><span data-stu-id="ec999-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="ec999-108">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ec999-108">Value</span></span> | <span data-ttu-id="ec999-109">Silt</span><span class="sxs-lookup"><span data-stu-id="ec999-109">Label</span></span> | <span data-ttu-id="ec999-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ec999-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ec999-111">200000000</span><span class="sxs-lookup"><span data-stu-id="ec999-111">200000000</span></span> | <span data-ttu-id="ec999-112">Vabastus</span><span class="sxs-lookup"><span data-stu-id="ec999-112">Exempt</span></span> | <span data-ttu-id="ec999-113">Tööl on FLSA juhiste põhjal vabastatud olek.</span><span class="sxs-lookup"><span data-stu-id="ec999-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="ec999-114">200000001</span><span class="sxs-lookup"><span data-stu-id="ec999-114">200000001</span></span> | <span data-ttu-id="ec999-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="ec999-115">NonExempt</span></span> | <span data-ttu-id="ec999-116">Tööl on FLSA juhiste põhjal mittevabastatud olek.</span><span class="sxs-lookup"><span data-stu-id="ec999-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="ec999-117">200000002</span><span class="sxs-lookup"><span data-stu-id="ec999-117">200000002</span></span> | <span data-ttu-id="ec999-118">Ei rakendu</span><span class="sxs-lookup"><span data-stu-id="ec999-118">Does Not Apply</span></span> | <span data-ttu-id="ec999-119">FLSA oleku juhised ei rakendu tööle.</span><span class="sxs-lookup"><span data-stu-id="ec999-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ec999-120">Vt ka</span><span class="sxs-lookup"><span data-stu-id="ec999-120">See also</span></span>

[<span data-ttu-id="ec999-121">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="ec999-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ec999-122">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="ec999-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]