---
title: Lõpuleviimise olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Lõpuleviimise olek.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468199"
---
# <a name="completion-status"></a><span data-ttu-id="52232-103">Lõpuleviimise olek</span><span class="sxs-lookup"><span data-stu-id="52232-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="52232-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Lõpuleviimise olek.</span><span class="sxs-lookup"><span data-stu-id="52232-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="52232-105">Füüsiline nimi: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="52232-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="52232-106">See loetelu annab kandidaatide skriiningute oleku väärtuste suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="52232-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="52232-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="52232-107">Value</span></span> | <span data-ttu-id="52232-108">Silt</span><span class="sxs-lookup"><span data-stu-id="52232-108">Label</span></span> | <span data-ttu-id="52232-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="52232-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="52232-110">200000000</span><span class="sxs-lookup"><span data-stu-id="52232-110">200000000</span></span> | <span data-ttu-id="52232-111">Lõpetamata</span><span class="sxs-lookup"><span data-stu-id="52232-111">Not Complete</span></span> | <span data-ttu-id="52232-112">Kandidaat ei ole skriiningut veel lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="52232-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="52232-113">200000001</span><span class="sxs-lookup"><span data-stu-id="52232-113">200000001</span></span> | <span data-ttu-id="52232-114">Edasta</span><span class="sxs-lookup"><span data-stu-id="52232-114">Pass</span></span> | <span data-ttu-id="52232-115">Kandidaat on skriiningu läbinud.</span><span class="sxs-lookup"><span data-stu-id="52232-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="52232-116">200000002</span><span class="sxs-lookup"><span data-stu-id="52232-116">200000002</span></span> | <span data-ttu-id="52232-117">Nurjumine</span><span class="sxs-lookup"><span data-stu-id="52232-117">Fail</span></span> | <span data-ttu-id="52232-118">Kandidaat on skriiningu läbikukkunud.</span><span class="sxs-lookup"><span data-stu-id="52232-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="52232-119">Vt ka</span><span class="sxs-lookup"><span data-stu-id="52232-119">See also</span></span>

[<span data-ttu-id="52232-120">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="52232-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="52232-121">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="52232-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]