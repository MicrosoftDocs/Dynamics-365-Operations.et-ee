---
title: Eemaldatud või aegunud funktsioonid teenuses Lifecycle Services (LCS)
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Microsoft Dynamicsi teenusest Lifecycle Services (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: abf7a1a0a75ac3098efeeab3df65481999b69acc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687874"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="94ce5-103">Eemaldatud või aegunud funktsioonid teenuses Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="94ce5-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="94ce5-104">See teema kirjeldab funktsioone, mis on Microsoft Dynamicsi teenusest Lifecycle Services (LCS) eemaldatud või aegunud.</span><span class="sxs-lookup"><span data-stu-id="94ce5-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="94ce5-105">*Eemaldatud* funktsioon pole teenuses enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="94ce5-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="94ce5-106">*Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.</span><span class="sxs-lookup"><span data-stu-id="94ce5-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="94ce5-107">See loend on esitatud nii, et saaksite oma plaanide tegemisel võtta neid eemaldusi ja aegumisi arvesse.</span><span class="sxs-lookup"><span data-stu-id="94ce5-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="94ce5-108">2019. aasta oktoobri teadaanded</span><span class="sxs-lookup"><span data-stu-id="94ce5-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="94ce5-109">Vooskeemide diagrammid äriprotsesside modelleerijas</span><span class="sxs-lookup"><span data-stu-id="94ce5-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="94ce5-110"><strong>Aegumise/eemaldamise põhjus</strong></span><span class="sxs-lookup"><span data-stu-id="94ce5-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="94ce5-111">Tühistame äriprotsesside modelleerijas vooskeemide diagrammide komponendi, kuna päranddisain põhjustas madalat kasutust.</span><span class="sxs-lookup"><span data-stu-id="94ce5-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ce5-112"><strong>Asendatud teise funktsiooniga?</strong></span><span class="sxs-lookup"><span data-stu-id="94ce5-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="94ce5-113">Ei</span><span class="sxs-lookup"><span data-stu-id="94ce5-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ce5-114"><strong>Mõjutatud alad</strong></span><span class="sxs-lookup"><span data-stu-id="94ce5-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="94ce5-115">Äriprotsesside modelleerija</span><span class="sxs-lookup"><span data-stu-id="94ce5-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94ce5-116"><strong>Olek</strong></span><span class="sxs-lookup"><span data-stu-id="94ce5-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="94ce5-117">Aegunud: vooskeemi diagrammide komponent eemaldatakse äriprotsesside modelleerijast 2020. aastal.</span><span class="sxs-lookup"><span data-stu-id="94ce5-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="94ce5-118">Saadaval pole järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="94ce5-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="94ce5-119">Kõik vooskeemid on kirjutuskaitstud ja pole redigeerimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="94ce5-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="94ce5-120">Vooskeemi tegevusega seotud kuju atribuudid ei ole samuti saadaval.</span><span class="sxs-lookup"><span data-stu-id="94ce5-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="94ce5-121">Need skeemid hõlmavad nii vaikimisi vooskeeme, mis on automaatselt loodud, kui ka kohandatud vooskeeme, mida on nende vaikimisi vooskeemide alusel muudetud.</span><span class="sxs-lookup"><span data-stu-id="94ce5-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="94ce5-122">Protsessisammud on kirjutuskaitstud ja pole redigeerimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="94ce5-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="94ce5-123">Pärandi sobivuse / erinevuste analüüsi funktsioon ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="94ce5-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="94ce5-124">Seetõttu erinevuste loendit automaatselt ei looda ja see pole eksportimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="94ce5-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="94ce5-125"><strong>Märkus:</strong> see funktsioon oli varem aegunud ja asendatud Microsoft Azure DevOpsi integratsioonidega.</span><span class="sxs-lookup"><span data-stu-id="94ce5-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="94ce5-126">Vooskeemi versiooniajalugu ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="94ce5-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
