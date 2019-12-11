---
title: Hinnangute ja arvustuste kasutamise valimine
description: Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.
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
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697976"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="f6b4e-103">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="f6b4e-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f6b4e-104">Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="f6b4e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="f6b4e-105">Overview</span></span>

<span data-ttu-id="f6b4e-106">Hinnangute ja arvustuste lahendus on omnikanali lahendus, mille saate rakenduses Dynamics 365 Commerce teha kättesaadavaks, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f6b4e-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="f6b4e-107">LCS on haldusportaal, mida jaemüüjad kasutavad oma keskkondade juhtimiseks alates ettevalmistusest kuni kasutusest eemaldamiseni.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="f6b4e-108">Kui soovite oma Commerce’i veebisaidil kasutada hinnanguid ja arvustusi, peate nendega esmalt nõustuma.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="f6b4e-109">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="f6b4e-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="f6b4e-110">Oma saidil hinnangute ja arvustuste kasutamisega nõustumiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="f6b4e-111">Järgige samme teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="f6b4e-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="f6b4e-112">Olles endiselt LCS-is, avage suvand **Jaemüügi juurutamise häälestus \> Muud sätted**.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="f6b4e-113">Määrake suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="f6b4e-114">Sisestage väljale **AAD hinnangute ja arvustuse moderaatori turberühm (turberühma objekti ID)** Microsoft Azure Active Directory (Azure AD) turberühma ID, mis hõlmab hinnangute ja arvustuste moderaatoreid.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Hinnangute ja arvustuste kasutamise valimine](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="f6b4e-116">Viige e-kaubanduse lähtestamise protsess lõpule.</span><span class="sxs-lookup"><span data-stu-id="f6b4e-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6b4e-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f6b4e-117">Additional resources</span></span>

[<span data-ttu-id="f6b4e-118">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="f6b4e-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="f6b4e-119">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="f6b4e-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="f6b4e-120">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f6b4e-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="f6b4e-121">Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="f6b4e-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
