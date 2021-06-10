---
title: Oskuste kaardimine
description: Saate luua oskuste kaardistamise otsingu, et leida kvalifitseeritud isik rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076587"
---
# <a name="map-skills"></a><span data-ttu-id="48d13-103">Oskuste kaardimine</span><span class="sxs-lookup"><span data-stu-id="48d13-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="48d13-104">Saate luua oskuste kaardistamise otsingu, et leida kvalifitseeritud isik rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="48d13-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="48d13-105">Oskuste kaardistamise otsingud tagastavad kriteeriumeid, mille sisestate järgmist teavet otsides:</span><span class="sxs-lookup"><span data-stu-id="48d13-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="48d13-106">Oskused</span><span class="sxs-lookup"><span data-stu-id="48d13-106">Skills</span></span>
- <span data-ttu-id="48d13-107">Haridus</span><span class="sxs-lookup"><span data-stu-id="48d13-107">Education</span></span>
- <span data-ttu-id="48d13-108">Serdid</span><span class="sxs-lookup"><span data-stu-id="48d13-108">Certificates</span></span>
- <span data-ttu-id="48d13-109">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="48d13-109">Positions</span></span>
- <span data-ttu-id="48d13-110">Projektikogemus</span><span class="sxs-lookup"><span data-stu-id="48d13-110">Project experience</span></span>

<span data-ttu-id="48d13-111">Näiteks võite leida oma organisatsioonis inimesed, kes on oma CPA välja teeninud.</span><span class="sxs-lookup"><span data-stu-id="48d13-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="48d13-112">Oskuste kaardistamise profiilid võimaldavad leida praegused töötajad või kandidaadid, kellel on kvalifikatsioonid, mis vastavad otseselt ärivajadustele.</span><span class="sxs-lookup"><span data-stu-id="48d13-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="48d13-113">Oskuste kaardistamise tulemuste loendis saab kuvada või oskuste profiilile lisada vaid need töötajad, kandidaadid ja kontaktisikud, kes on lisatud oskuste kaardistamise otsingusse.</span><span class="sxs-lookup"><span data-stu-id="48d13-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="48d13-114">Isiku kaasamiseks oskuste kaardistamise otsingutesse määrake **Kaasa oskuste kaardistamisse** järgmistel lehtedel valik **Jah**:</span><span class="sxs-lookup"><span data-stu-id="48d13-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="48d13-115">Töötaja</span><span class="sxs-lookup"><span data-stu-id="48d13-115">Worker</span></span><br>
> - <span data-ttu-id="48d13-116">Töötaja</span><span class="sxs-lookup"><span data-stu-id="48d13-116">Employee</span></span><br>
> - <span data-ttu-id="48d13-117">Kandidaat</span><span class="sxs-lookup"><span data-stu-id="48d13-117">Applicant</span></span><br>
> - <span data-ttu-id="48d13-118">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="48d13-118">Contacts</span></span><br>

<span data-ttu-id="48d13-119">Oskuste kaardistamise loomiseks minge **Töötaja areng > Lingid > Oskuste kaardistamine**.</span><span class="sxs-lookup"><span data-stu-id="48d13-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="48d13-120">Oskuste kaardistamise profiili loomiseks minge **Töötaja areng > Lingid > Oskuste kaardistamise profiilid**.</span><span class="sxs-lookup"><span data-stu-id="48d13-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="48d13-121">Oskuste vahe analüüs ja oskuste profiili analüüs</span><span class="sxs-lookup"><span data-stu-id="48d13-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="48d13-122">Saate luua oskuste profiili analüüsi, et vaadata isiku pädevuste loendit.</span><span class="sxs-lookup"><span data-stu-id="48d13-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="48d13-123">Oskuste vahe analüüsiga saate võrrelda isiku oskusi ja töö jaoks vajalikke oskusi.</span><span class="sxs-lookup"><span data-stu-id="48d13-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="48d13-124">Vaheanalüüsi loomiseks minge jaotisesse **Töötaja areng > Lingid > Oskuste vaheanalüüsi töö – isik**.</span><span class="sxs-lookup"><span data-stu-id="48d13-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="48d13-125">Oskuste kaardistamise profiili loomiseks minge **Töötaja areng > Lingid > Oskuste profiili analüüsid**.</span><span class="sxs-lookup"><span data-stu-id="48d13-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="48d13-126">Vt ka</span><span class="sxs-lookup"><span data-stu-id="48d13-126">See also</span></span>

[<span data-ttu-id="48d13-127">Oskuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="48d13-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="48d13-128">Sisestage oskused</span><span class="sxs-lookup"><span data-stu-id="48d13-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]