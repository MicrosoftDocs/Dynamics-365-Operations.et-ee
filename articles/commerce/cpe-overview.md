---
title: Commerce'i eelvaatekeskkonna ülevaade
description: See teema annab ülevaate rakenduse Microsoft Dynamics 365 Commerce eelvaatekeskkonnast.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906066"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="270a1-103">Commerce'i eelvaatekeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="270a1-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="270a1-104">See teema annab ülevaate rakenduse Microsoft Dynamics 365 Commerce eelvaatekeskkonnast.</span><span class="sxs-lookup"><span data-stu-id="270a1-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="270a1-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="270a1-105">Overview</span></span>

<span data-ttu-id="270a1-106">Commerce'i eelvaatekeskkond on valikuline lõpust lõppu Dynamics 365 Commerce'i eelvaatekeskkond, mis laseb potentsiaalsetel klientidel proovida Commerce toodet enne selle üldist vabastamist üldsusele.</span><span class="sxs-lookup"><span data-stu-id="270a1-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="270a1-107">Jättes kõrvale mõned väikesed piirangud, mis ei mõjuta funktsioone või praktilisust, pakub Commerce eelvaatekeskkond täielikku kauplemise kogemust ja seda saavad kasutada kliendid ja rakenduspartnerid, et hinnata toodet, anda tagasisidet ja teha sobivuse/vahe analüüs.</span><span class="sxs-lookup"><span data-stu-id="270a1-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="270a1-108">Commerce eelvaatekeskkonna piirangud</span><span class="sxs-lookup"><span data-stu-id="270a1-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="270a1-109">Kuigi Commerce eelvaatekeskkond pakub kõiki Commerce'i funktsioonide ja praktilisuste kogumit, on mõned väikesed piirangud:</span><span class="sxs-lookup"><span data-stu-id="270a1-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="270a1-110">Kuigi Commerce eelvaatekeskkonnas ei ole geograafilisi piiranguid, saab keskkonda komponente, nagu Retail Cloud Scale Unit (RCSU) ja e-kaubanduse rakendusi, ette valmistada ainult Ameerika Ühendriikides.</span><span class="sxs-lookup"><span data-stu-id="270a1-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="270a1-111">Commerce Preview keskkonnal on 30-päevase ajalimiit alates e-kaubanduse ettevalmistamise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="270a1-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="270a1-112">Commerce Preview keskkonda saab edukalt rakendada ja lähtestada ainult keskkonnas, mis kasutab demo topoloogiat, kus kõik keskkonna komponendid on kasutusele võetud ühe virtuaalarvuti (VM) abil.</span><span class="sxs-lookup"><span data-stu-id="270a1-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="270a1-113">Selle OneBox VM topoloogia peamine piirang on samaaegsete kasutajate arv, mida eelvaate keskkond saab toetada.</span><span class="sxs-lookup"><span data-stu-id="270a1-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="270a1-114">Commerce eelvaatekeskkonda saab hinnata ainult seni, kuni on olemas Commerce'i toote üldine kättesaadavus (GA).</span><span class="sxs-lookup"><span data-stu-id="270a1-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="270a1-115">Uued demo keskkonnad on saadaval pärast GA-d.</span><span class="sxs-lookup"><span data-stu-id="270a1-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="270a1-116">Alusta</span><span class="sxs-lookup"><span data-stu-id="270a1-116">Get started</span></span>

<span data-ttu-id="270a1-117">Commerce eelvaatekeskkonna ettevalmistamiseks vaadake teemat [Commerce eelvaatekeskkonna ettevalmistamiseks](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="270a1-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="270a1-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="270a1-118">Additional resources</span></span>

[<span data-ttu-id="270a1-119">Commerce'i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="270a1-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="270a1-120">Commerce'i eelvaatekeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="270a1-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="270a1-121">Commerce'i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="270a1-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="270a1-122">Commerce'i eelvaatekeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="270a1-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)