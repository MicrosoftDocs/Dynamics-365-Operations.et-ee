---
title: Eemaldatud või aegunud platvormi funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087879"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="101d2-103">Eemaldatud või aegunud platvormi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="101d2-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="101d2-104">See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.</span><span class="sxs-lookup"><span data-stu-id="101d2-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="101d2-105">*Eemaldatud* funktsioon pole tootes enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="101d2-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="101d2-106">*Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.</span><span class="sxs-lookup"><span data-stu-id="101d2-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="101d2-107">See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta.</span><span class="sxs-lookup"><span data-stu-id="101d2-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="101d2-108">Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="101d2-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="101d2-109">Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="101d2-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="101d2-110">Platvormivärskendus update 32</span><span class="sxs-lookup"><span data-stu-id="101d2-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="101d2-111">Töövoo taotluse muutmise dialoogiboks ei sisalda enam kasutaja valiku ripploendit</span><span class="sxs-lookup"><span data-stu-id="101d2-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="101d2-112">**Aegumise/eemaldamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="101d2-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="101d2-113">See oli turvalisuse probleem, kuna muudatuse taotluse võis saata soovimatule kasutajale.</span><span class="sxs-lookup"><span data-stu-id="101d2-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="101d2-114">See oli ka kasutatavuse probleem, sest see sundis kasutajat määratlema, kes oli töövoo algataja, ja valida need käsitsi.</span><span class="sxs-lookup"><span data-stu-id="101d2-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="101d2-115">**Asendatud teise funktsiooniga?**</span><span class="sxs-lookup"><span data-stu-id="101d2-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="101d2-116">Ei</span><span class="sxs-lookup"><span data-stu-id="101d2-116">No</span></span> |
| <span data-ttu-id="101d2-117">**Mõjutatud tootealad**</span><span class="sxs-lookup"><span data-stu-id="101d2-117">**Product areas affected**</span></span>         | <span data-ttu-id="101d2-118">Töövoog</span><span class="sxs-lookup"><span data-stu-id="101d2-118">Workflow</span></span> |
| <span data-ttu-id="101d2-119">**Juurutamissuvand**</span><span class="sxs-lookup"><span data-stu-id="101d2-119">**Deployment option**</span></span>              | <span data-ttu-id="101d2-120">Kõik</span><span class="sxs-lookup"><span data-stu-id="101d2-120">All</span></span> |
| <span data-ttu-id="101d2-121">**Olek**</span><span class="sxs-lookup"><span data-stu-id="101d2-121">**Status**</span></span>                         | <span data-ttu-id="101d2-122">Kasutaja valiku ripploend eemaldati taotluse muudatuse dialoogiboksist platvormi värskenduses 32.</span><span class="sxs-lookup"><span data-stu-id="101d2-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="101d2-123">Taotluse muutmise taotlused saadetakse automaatselt algatajale, nagu see on ette nähtud.</span><span class="sxs-lookup"><span data-stu-id="101d2-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="101d2-124">Lisateavet selle funktsiooni kohta vt teemast [Tegevused töövoo kinnitusprotsessis](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="101d2-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="101d2-125">Varasemad teatised eemaldatud või aegunud funktsioonidest</span><span class="sxs-lookup"><span data-stu-id="101d2-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="101d2-126">Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="101d2-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

