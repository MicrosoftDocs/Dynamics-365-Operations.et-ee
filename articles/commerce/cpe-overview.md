---
title: Dynamics 365 Commerce'i hindamiskeskkonna ülevaade
description: See teema annab ülevaate rakenduse Microsoft Dynamics 365 Commerce hindamiskeskkonnast.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e08c2f327771d7731b836840006d63b6ecb7dfc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000946"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="1b5a2-103">Dynamics 365 Commerce'i hindamiskeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="1b5a2-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b5a2-104">See teema annab ülevaate rakenduse Microsoft Dynamics 365 Commerce hindamiskeskkonnast.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="1b5a2-105">Commerce'i hindamiskeskkonnad pole üldiselt kättesaadavad ja antakse partneritele ning klientidele taotluse alusel.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="1b5a2-106">Lisateabe saamiseks pöörduge oma Microsofti partneri kontakti poole.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="1b5a2-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1b5a2-107">Overview</span></span>

<span data-ttu-id="1b5a2-108">Commerce'i hindamiskeskkond on valikuline täielik Dynamics 365 Commerce'i keskkond, mis võimaldab partneritel ja potentsiaalsetel klientidel proovida Commerce'i toodet.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="1b5a2-109">Hindamiskeskkonnad on osaliselt eelkonfigureeritud, et vähendada nõutavaid ettevalmistuse järgseid etappe.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="1b5a2-110">Jättes kõrvale mõned väikesed piirangud, mis ei mõjuta funktsioone või praktilisust, pakub Commerce'i hindamiskeskkond täielikku kauplemise kogemust ja seda saavad kasutada kliendid ja rakenduspartnerid, et hinnata toodet, anda tagasisidet ja teha sobivuse/vahe analüüs.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="1b5a2-111">Commerce'i hindamiskeskkonna piirangud</span><span class="sxs-lookup"><span data-stu-id="1b5a2-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="1b5a2-112">Kuigi Commerce'i hindamiskeskkond pakub kõiki Commerce'i funktsioonide ja praktilisuste kogumit, on mõned väikesed piirangud:</span><span class="sxs-lookup"><span data-stu-id="1b5a2-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="1b5a2-113">Kuigi Commerce'i hindamiskeskkonnas ei ole geograafilisi piiranguid, tuleks keskkonda komponente, nagu Retail Cloud Scale Unit (RCSU) ja e-kaubanduse rakendusi, ette valmistada ainult Ameerika Ühendriikides.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="1b5a2-114">Commerce'i hindamiskeskkonnal on 30-päevane ajapiirang alates e-kaubanduse ettevalmistamise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="1b5a2-115">Commerce'i hindamiskeskkonda saab edukalt rakendada ja lähtestada ainult keskkonnas, mis kasutab demo topoloogiat, kus kõik keskkonna komponendid on kasutusele võetud ühe pilve majutatud virtuaalarvuti (VM) abil.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="1b5a2-116">Selle topoloogia peamine piirang on samaaegsete kasutajate arv, mida keskkond saab toetada.</span><span class="sxs-lookup"><span data-stu-id="1b5a2-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="1b5a2-117">Alusta</span><span class="sxs-lookup"><span data-stu-id="1b5a2-117">Get started</span></span>

<span data-ttu-id="1b5a2-118">Commerce'i hindamiskeskkonna ettevalmistamiseks vaadake teemat [Commerce'i hindamiskeskkonna ettevalmistamine](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="1b5a2-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b5a2-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1b5a2-119">Additional resources</span></span>

[<span data-ttu-id="1b5a2-120">Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="1b5a2-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="1b5a2-121">Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1b5a2-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="1b5a2-122">BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="1b5a2-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="1b5a2-123">Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1b5a2-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="1b5a2-124">Dynamics 365 Commerce'i hindamiskeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="1b5a2-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
