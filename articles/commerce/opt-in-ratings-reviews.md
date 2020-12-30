---
title: Hinnangute ja arvustuste kasutamise valimine
description: Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411682"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="29ea0-103">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="29ea0-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="29ea0-104">Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="29ea0-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="29ea0-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="29ea0-105">Overview</span></span>

<span data-ttu-id="29ea0-106">Hinnangute ja arvustuste lahendus on omnikanali lahendus, mille saate rakenduses Dynamics 365 Commerce teha kättesaadavaks, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="29ea0-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="29ea0-107">LCS on haldusportaal, mida jaemüüjad kasutavad oma keskkondade juhtimiseks alates ettevalmistusest kuni kasutusest eemaldamiseni.</span><span class="sxs-lookup"><span data-stu-id="29ea0-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="29ea0-108">Kui soovite oma Commerce’i veebisaidil kasutada hinnangute ja arvustuste lahendust, peate rakenduses Dynamics 365 Commerce e-kaubanduse saidi juurutamisel nõustuma hinnangute ja arvustustega.</span><span class="sxs-lookup"><span data-stu-id="29ea0-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="29ea0-109">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="29ea0-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="29ea0-110">Oma saidil hinnangute ja arvustuste kasutamisega nõustumiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="29ea0-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="29ea0-111">Järgige samme teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="29ea0-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="29ea0-112">Olles endiselt LCS-is, avage suvand **Jaemüügi juurutamise häälestus \> Muud sätted**.</span><span class="sxs-lookup"><span data-stu-id="29ea0-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="29ea0-113">Määrake suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="29ea0-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="29ea0-114">Sisestage väljale **AAD hinnangute ja arvustuse moderaatori turberühm (turberühma objekti ID)** Microsoft Azure Active Directory (Azure AD) turberühma ID, mis hõlmab hinnangute ja arvustuste moderaatoreid.</span><span class="sxs-lookup"><span data-stu-id="29ea0-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Hinnangute ja arvustuste kasutamise valimine](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="29ea0-116">Viige e-kaubanduse lähtestamise protsess lõpule.</span><span class="sxs-lookup"><span data-stu-id="29ea0-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="29ea0-117">Kui olete olemasolev rakenduse Dynamics 365 Commerce klient, kes on juba võtnud e-kaubanduse saidi kasutusele, ilma et oleks valinud hinnanguid ja arvustusi, ning nüüd soovite kasutada Dynamics 365 Commerce’i paketist hinnanguid ja arvustusi, esitage teenusetaotlus.</span><span class="sxs-lookup"><span data-stu-id="29ea0-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="29ea0-118">Teavet teenusetaotluse kasutamise kohta vt teemast [Teenusetaotluse esitamise protsess](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="29ea0-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="29ea0-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="29ea0-119">Additional resources</span></span>

[<span data-ttu-id="29ea0-120">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="29ea0-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="29ea0-121">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="29ea0-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="29ea0-122">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="29ea0-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="29ea0-123">Toote hinnangute sünkroonimine rakenduses Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="29ea0-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


