---
title: Töö üksikasjade API
description: See teema annab üksikasjad ja näidispäringu Töö üksiksasjade olemi kohta rakenduses Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f15282bf72340cb1a832ff3264361472d0a6c70
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881965"
---
# <a name="job-detail-api"></a><span data-ttu-id="0ddab-103">Töö üksikasjade API</span><span class="sxs-lookup"><span data-stu-id="0ddab-103">Job detail API</span></span>

<span data-ttu-id="0ddab-104">See teema annab üksikasjad ja näidispäringu Töö üksiksasjade olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0ddab-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="0ddab-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="0ddab-105">Properties</span></span>

| <span data-ttu-id="0ddab-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="0ddab-106">Property</span></span><br><span data-ttu-id="0ddab-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="0ddab-107">**Physical name**</span></span><br><span data-ttu-id="0ddab-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="0ddab-108">**_Type_**</span></span> | <span data-ttu-id="0ddab-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="0ddab-109">Use</span></span> | <span data-ttu-id="0ddab-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0ddab-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0ddab-111">**Töö ID**</span><span class="sxs-lookup"><span data-stu-id="0ddab-111">**Job ID**</span></span><br><span data-ttu-id="0ddab-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="0ddab-112">mshr_jobid</span></span><br><span data-ttu-id="0ddab-113">*String*</span><span class="sxs-lookup"><span data-stu-id="0ddab-113">*String*</span></span> | <span data-ttu-id="0ddab-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0ddab-114">Read-only</span></span><br><span data-ttu-id="0ddab-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0ddab-115">Required</span></span> | <span data-ttu-id="0ddab-116">Töö kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="0ddab-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="0ddab-117">**Turuhinna madal künnis**</span><span class="sxs-lookup"><span data-stu-id="0ddab-117">**Market price low threshold**</span></span><br><span data-ttu-id="0ddab-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="0ddab-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="0ddab-119">*Kümnendkoht*</span><span class="sxs-lookup"><span data-stu-id="0ddab-119">*Decimal*</span></span> | | <span data-ttu-id="0ddab-120">Süsteemi loodud GUID-väärtus ametikoha kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="0ddab-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
