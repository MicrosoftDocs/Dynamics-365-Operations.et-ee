---
title: Hinnangute ja arvustuste ülevaade
description: See teema hõlmab hinnanguid ja arvustusi rakenduses Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 45a6710a10fe3d33457c1327c8fc339c9ad0082a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698184"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="b2f17-103">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b2f17-103">Ratings and reviews overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b2f17-104">See teema hõlmab hinnanguid ja arvustusi rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2f17-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b2f17-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b2f17-105">Overview</span></span>

<span data-ttu-id="b2f17-106">Hinnangud ja arvustused on olulised e-kaubanduse klientidele, kes soovivad teada, kuidas teised kliendid toodet hindavad.</span><span class="sxs-lookup"><span data-stu-id="b2f17-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="b2f17-107">Samuti võivad need aidata tarbijatel teha ostuotsuseid.</span><span class="sxs-lookup"><span data-stu-id="b2f17-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="b2f17-108">Rakenduses Dynamics 365 Commerce võimaldab hinnangute ja arvustuste lahendus jaemüüjatel jäädvustada tootearvustusi ja hinnanguid klientidelt.</span><span class="sxs-lookup"><span data-stu-id="b2f17-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="b2f17-109">Seejärel saavad jaemüüjad kuvada keskmised hinnangud ja vaadata üle oma e-kaubanduse veebisaidil olevat teavet.</span><span class="sxs-lookup"><span data-stu-id="b2f17-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="b2f17-110">Keskmise hinnangu teave kuvatakse kassas (POS) ja kõnekeskuse kanalites.</span><span class="sxs-lookup"><span data-stu-id="b2f17-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="b2f17-111">Seetõttu saavad müügiassistendid seda kasutada, et aidata kasutajatel otsuseid teha.</span><span class="sxs-lookup"><span data-stu-id="b2f17-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="b2f17-112">Hinnangud ja arvustused võivad olla ka tagasiside mehhanism, mida jaemüüjad saavad kasutada toote kvaliteedi parandamiseks ja seetõttu müügi suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b2f17-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="b2f17-113">Hinnangute ja arvustuste funktsioon rakenduses Dynamics 365 Commerce on omnikanali lahendus ja on algupäraselt saadaval platvormi osana.</span><span class="sxs-lookup"><span data-stu-id="b2f17-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="b2f17-114">Hinnangute ja arvustuste lahendus on üles ehitatud teenusele Microsoft Azure, mis pakub suurt mastaapsust ja usaldusväärsust.</span><span class="sxs-lookup"><span data-stu-id="b2f17-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="b2f17-115">Järgmine illustratsioon näitab, kuidas hinnangute ja arvustuste lahendus töötab rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2f17-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Hinnangud ja arvustused rakenduses Dynamics 365 for Commerce](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="b2f17-117">Hinnangute ja arvustuste lahendus rakenduses Dynamics 365 Commerce kasutab teenust Azure Cognitive Services, et pakkuda ebasündsate sõnade automaatset modereerimist 40 keeles.</span><span class="sxs-lookup"><span data-stu-id="b2f17-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="b2f17-118">Kuna inimeste heakskiitu ei nõuta, vähendatakse modereerimise kulusid.</span><span class="sxs-lookup"><span data-stu-id="b2f17-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="b2f17-119">Süsteem pakub ka moderaatori tööriistu, mida saab kasutada klientide murede, tagasiside ja mahavõtmise taotluste rahuldamiseks ja kasutajatelt saadud andmetega seotud taotluste käsitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b2f17-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="b2f17-120">Hinnangute ja arvustuste lahendus pakub vidinaid, mis näitavad hinnangu kokkuvõtteid toodete loendites, otsingutulemustes, toote üksikasjade lehel ja muudes kohtades.</span><span class="sxs-lookup"><span data-stu-id="b2f17-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="b2f17-121">Vidinad näitavad täielikku arvustuste loendit ja pakuvad ka sortimise ja filtreerimise suvandeid.</span><span class="sxs-lookup"><span data-stu-id="b2f17-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="b2f17-122">Hinnangute ja arvustuste lahendus pakub ka ärianalüüsi (BI) malli, mis sisaldab mõõdikute kogumit, et anda ülevaated hinnangutest ja arvustustest.</span><span class="sxs-lookup"><span data-stu-id="b2f17-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="b2f17-123">Hinnanguid ja arvustusi saab eksportida edasise analüüsi jaoks.</span><span class="sxs-lookup"><span data-stu-id="b2f17-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2f17-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b2f17-124">Additional resources</span></span>

[<span data-ttu-id="b2f17-125">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="b2f17-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="b2f17-126">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="b2f17-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="b2f17-127">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b2f17-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="b2f17-128">Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="b2f17-128">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)