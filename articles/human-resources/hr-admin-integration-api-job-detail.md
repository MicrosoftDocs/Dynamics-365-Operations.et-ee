---
title: Töö üksikasjade API
description: See teema annab üksikasjad ja näidispäringu Töö üksiksasjade olemi kohta rakenduses Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 562b9f505311b6cfe505a76fc5c0a384eb641936
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054760"
---
# <a name="job-detail-api"></a><span data-ttu-id="3adbe-103">Töö üksikasjade API</span><span class="sxs-lookup"><span data-stu-id="3adbe-103">Job detail API</span></span>

<span data-ttu-id="3adbe-104">See teema annab üksikasjad ja näidispäringu Töö üksiksasjade olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3adbe-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="3adbe-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="3adbe-105">Properties</span></span>

| <span data-ttu-id="3adbe-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="3adbe-106">Property</span></span><br><span data-ttu-id="3adbe-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="3adbe-107">**Physical name**</span></span><br><span data-ttu-id="3adbe-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="3adbe-108">**_Type_**</span></span> | <span data-ttu-id="3adbe-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="3adbe-109">Use</span></span> | <span data-ttu-id="3adbe-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3adbe-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3adbe-111">**Töö ID**</span><span class="sxs-lookup"><span data-stu-id="3adbe-111">**Job ID**</span></span><br><span data-ttu-id="3adbe-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="3adbe-112">mshr_jobid</span></span><br><span data-ttu-id="3adbe-113">*String*</span><span class="sxs-lookup"><span data-stu-id="3adbe-113">*String*</span></span> | <span data-ttu-id="3adbe-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3adbe-114">Read-only</span></span><br><span data-ttu-id="3adbe-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3adbe-115">Required</span></span> | <span data-ttu-id="3adbe-116">Töö kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="3adbe-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="3adbe-117">**Turuhinna madal künnis**</span><span class="sxs-lookup"><span data-stu-id="3adbe-117">**Market price low threshold**</span></span><br><span data-ttu-id="3adbe-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="3adbe-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="3adbe-119">*Kümnendkoht*</span><span class="sxs-lookup"><span data-stu-id="3adbe-119">*Decimal*</span></span> | | <span data-ttu-id="3adbe-120">Süsteemi loodud GUID-väärtus ametikoha kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="3adbe-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
