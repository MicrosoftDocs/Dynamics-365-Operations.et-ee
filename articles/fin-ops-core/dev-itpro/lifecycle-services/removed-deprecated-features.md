---
title: Eemaldatud või aegunud funktsioonid teenuses Lifecycle Services (LCS)
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Microsoft Dynamicsi teenusest Lifecycle Services (LCS).
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885451"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="e924d-103">Eemaldatud või aegunud funktsioonid teenuses Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e924d-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e924d-104">See teema kirjeldab funktsioone, mis on Microsoft Dynamicsi teenusest Lifecycle Services (LCS) eemaldatud või aegunud.</span><span class="sxs-lookup"><span data-stu-id="e924d-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="e924d-105">*Eemaldatud* funktsioon pole teenuses enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="e924d-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="e924d-106">*Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.</span><span class="sxs-lookup"><span data-stu-id="e924d-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="e924d-107">See loend on esitatud nii, et saaksite oma plaanide tegemisel võtta neid eemaldusi ja aegumisi arvesse.</span><span class="sxs-lookup"><span data-stu-id="e924d-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="e924d-108">2019. aasta oktoobri teadaanded</span><span class="sxs-lookup"><span data-stu-id="e924d-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="e924d-109">Vooskeemide diagrammid äriprotsesside modelleerijas</span><span class="sxs-lookup"><span data-stu-id="e924d-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="e924d-110"><strong>Aegumise/eemaldamise põhjus</strong></span><span class="sxs-lookup"><span data-stu-id="e924d-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="e924d-111">Tühistame äriprotsesside modelleerijas vooskeemide diagrammide komponendi, kuna päranddisain põhjustas madalat kasutust.</span><span class="sxs-lookup"><span data-stu-id="e924d-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e924d-112"><strong>Asendatud teise funktsiooniga?</strong></span><span class="sxs-lookup"><span data-stu-id="e924d-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="e924d-113">Ei</span><span class="sxs-lookup"><span data-stu-id="e924d-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e924d-114"><strong>Mõjutatud alad</strong></span><span class="sxs-lookup"><span data-stu-id="e924d-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="e924d-115">Äriprotsesside modelleerija</span><span class="sxs-lookup"><span data-stu-id="e924d-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e924d-116"><strong>Olek</strong></span><span class="sxs-lookup"><span data-stu-id="e924d-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="e924d-117">Aegunud: vooskeemi diagrammide komponent eemaldatakse äriprotsesside modelleerijast 2020. aasta veebruari alguses.</span><span class="sxs-lookup"><span data-stu-id="e924d-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed by early February 2020.</span></span> <span data-ttu-id="e924d-118">Eemaldatakse järgmised funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="e924d-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="e924d-119">Olemasolevad vooskeemid ei ole vaatamiseks ega redigeerimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="e924d-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="e924d-120">Vooskeemi tegevusega seotud kuju atribuudid ei ole samuti saadaval, kuna kogu vahekaart <strong>Vooskeem</strong> eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="e924d-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="e924d-121">Need skeemid hõlmavad nii vaikimisi vooskeeme, mis on automaatselt loodud, kui ka kohandatud vooskeeme, mida on nende vaikimisi vooskeemide alusel muudetud.</span><span class="sxs-lookup"><span data-stu-id="e924d-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="e924d-122">Pärandi sobivuse / erinevuste analüüsi funktsioon ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="e924d-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="e924d-123">Seetõttu erinevuste loendit automaatselt ei looda ja see pole eksportimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="e924d-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="e924d-124"><strong>Märkus:</strong> see funktsioon oli varem aegunud ja asendatud Microsoft Azure DevOpsi integratsioonidega.</span><span class="sxs-lookup"><span data-stu-id="e924d-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="e924d-125">Vooskeemi versiooniajalugu ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="e924d-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
