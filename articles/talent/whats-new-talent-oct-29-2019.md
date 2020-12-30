---
title: Mis on Dynamics 365 Talent-is uut või mida on muudetud (29. oktoober 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529680"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="227dc-103">Mis on Dynamics 365 Talent-is uut või mida on muudetud (29. oktoober 2019)</span><span class="sxs-lookup"><span data-stu-id="227dc-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="227dc-104">Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="227dc-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="227dc-105">Muutused Attractis</span><span class="sxs-lookup"><span data-stu-id="227dc-105">Changes in Attract</span></span>

<span data-ttu-id="227dc-106">See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="227dc-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="227dc-107">Muutused Onboardis</span><span class="sxs-lookup"><span data-stu-id="227dc-107">Changes in Onboard</span></span>

<span data-ttu-id="227dc-108">See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="227dc-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="227dc-109">Core HR-i muudatused</span><span class="sxs-lookup"><span data-stu-id="227dc-109">Changes in Core HR</span></span>

<span data-ttu-id="227dc-110">Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="227dc-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="227dc-111">Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="227dc-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="227dc-112">Ilma rollideta osapoolte kustutamine peaks vaikimisi olema sees (371233)</span><span class="sxs-lookup"><span data-stu-id="227dc-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="227dc-113">Talentis uut keskkonda ette valmistades on suvand **Ilma eksisteerivate rollideta osapoolte kustutamine** vaikimisi sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="227dc-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="227dc-114">Töötaja kustutamisel ei eemaldata töötajaga seotud osapoolt, välja arvatud juhul, kui see säte on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="227dc-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="227dc-115">See muudatus piirab globaalses aadressiraamatus kattuvaid kirjeid, kui peate töötajaid importima, muutma või uuesti importima.</span><span class="sxs-lookup"><span data-stu-id="227dc-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="227dc-116">Puhkusetaotluste mustandeid ja tühistusi peaks olema võimalik Common Data Service’is kustutada (376999)</span><span class="sxs-lookup"><span data-stu-id="227dc-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="227dc-117">Selle muudatusega saate nüüd kustutada puhkusetaotlusi, mille olek on Common Data Service’is **Mustand** või **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="227dc-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="227dc-118">Täiendavaid kohandatud väljade loendi väärtuseid ei kajastata Common Data Service’is pärast rakendusnupu vajutamist kohandatud väljade vormil (379599)</span><span class="sxs-lookup"><span data-stu-id="227dc-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="227dc-119">Kui lisate uue loendi väärtused olemasolevale kohandatud väljale, mis on juba Common Data Service’iga sünkroonitud, on need nüüd Common Data Service’is saadaval pärast muudatuste rakendamist vormil **Kohandatud väljad**.</span><span class="sxs-lookup"><span data-stu-id="227dc-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="227dc-120">Värbamise kontroll-loendi rakendamine juriidilistele isikutele, kui eksisteerib rohkem kui üks töösuhe (371270)</span><span class="sxs-lookup"><span data-stu-id="227dc-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="227dc-121">Selle nädala väljaandes saate rakendada kontroll-loendeid töötajatele, kellel on suvandis **Töötaja vorm > Kontroll-loendid** rohkem kui üks töösuhe.</span><span class="sxs-lookup"><span data-stu-id="227dc-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="227dc-122">Soodustuste avatud registreerimise eelvaatefunktsioon on eemaldatud</span><span class="sxs-lookup"><span data-stu-id="227dc-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="227dc-123">Kooskõlas meie teadaandega ajaveebipostituses [Core HR-i strateegilised investeeringud parandavad tegevuse tõhusust](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence), eemaldas Microsoft avalikust eelversioonist soodustuste avatud registreerimise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="227dc-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="227dc-124">Tulevikus antakse välja uued funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="227dc-124">New functionality will be released in the future.</span></span> <span data-ttu-id="227dc-125">Soodustuste avatud registreerimise funktsiooni tootmisest kasutamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="227dc-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="227dc-126">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="227dc-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="227dc-127">Jõudluse ülevaadete printimine</span><span class="sxs-lookup"><span data-stu-id="227dc-127">Print performance reviews</span></span>

<span data-ttu-id="227dc-128">Vt [Jõudluse ülevaadete printimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews), rakenduse Dynamics 365 2019. aasta väljalaskevoo plaanis 2.</span><span class="sxs-lookup"><span data-stu-id="227dc-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="227dc-129">Funktsioonihalduse tööruum</span><span class="sxs-lookup"><span data-stu-id="227dc-129">Feature management workspace</span></span>

<span data-ttu-id="227dc-130">Igale väljalaskele lisatakse funktsioone ja nende uuendusi.</span><span class="sxs-lookup"><span data-stu-id="227dc-130">Features are added and updated in every release.</span></span> <span data-ttu-id="227dc-131">Funktsioonihalduskeskkond pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit.</span><span class="sxs-lookup"><span data-stu-id="227dc-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="227dc-132">Vaikimisi on uued funktsioonid välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="227dc-132">By default, new features are turned off.</span></span> <span data-ttu-id="227dc-133">Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="227dc-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="227dc-134">Lisateavet tulevaste funktsioonihaldusega seotud muudatuste kohta vt teemast [Funktsioonihalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="227dc-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
