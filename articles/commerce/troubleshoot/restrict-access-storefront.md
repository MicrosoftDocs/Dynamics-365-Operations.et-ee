---
title: Piirake katsetamise või arenduse ajal ligipääsu kauplusele
description: See teema kirjeldab, kuidas piirata juurdepääsu Microsoft Dynamics 365 Commerce sisemistele testimistele ja arendustele.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f5cba6b7ff3aa65441c932e72fa458bda0d0fc69
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801527"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="6cbf2-103">Piirake katsetamise või arenduse ajal ligipääsu kauplusele</span><span class="sxs-lookup"><span data-stu-id="6cbf2-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6cbf2-104">See teema kirjeldab, kuidas piirata juurdepääsu Microsoft Dynamics 365 Commerce sisemistele testimistele ja arendustele.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="6cbf2-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6cbf2-105">Description</span></span>

<span data-ttu-id="6cbf2-106">Sisetestimisel või aktiivsel arenduse ajal soovite võibolla piirata juurdepääsu oma saidile, et takistada väliskasutajatel pääseda juurde avaldatud siselao lehtedele.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="6cbf2-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="6cbf2-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="6cbf2-108">Azure AD B2C seadistamine standardsete kasutajavoogude abil</span><span class="sxs-lookup"><span data-stu-id="6cbf2-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="6cbf2-109">Teavet Azure Active Directory (Azure AD B2C) konfigureerimise kohta e-kaubanduse saidi jaoks vaata [B2C rentniku seadistamine Commerce\`s](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="6cbf2-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="6cbf2-110">Piira kasutaja juurdepääsu kaupluse lehtedele ja blokeeri uute kasutajate loomine</span><span class="sxs-lookup"><span data-stu-id="6cbf2-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="6cbf2-111">Rakenduse Commerce saidi koostajas kasutaja juurdepääsu piiramiseksfronte lehekülgedele, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6cbf2-112">Avage rakenduses oma sait.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-112">Go to your site.</span></span>
1. <span data-ttu-id="6cbf2-113">Valige **leheküljed** ja seejärel valige leht, mille kasutaja juurdepääsu piirata.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="6cbf2-114">Valige moodul või killupesa ja seejärel valige käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="6cbf2-115">Valige atribuutide paanil suvand **Nõuab sisselogimist?** ja valige suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="6cbf2-116">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-116">Select **Publish**.</span></span>

<span data-ttu-id="6cbf2-117">Uute kasutajate loomise blokeerimiseks Azure AD järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="6cbf2-118">Avage [Azure’i portaalis](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="6cbf2-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="6cbf2-119">Valige Azure AD B2C-rakendus, mille lõite oma saidi juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="6cbf2-120">Valige vasakpoolsel navigeerimispaanil suvand **Kasutaja voog**.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="6cbf2-121">Ülal **Kasutaja voog** lehel valige **Uus kasutajavoog**.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="6cbf2-122">Lehel **Valige kasutaja voo tüüp** valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="6cbf2-123">Lehe keskel valige **Logi sisse v2**.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="6cbf2-124">Seejärel järgige [Commerce'i B2C rentniku häälestamise samme](../set-up-b2c-tenant.md) voo konfigureerimiseks oma saidi standardse kasutajavoona Azure AD B2C jaoks testimise või arendamise ajal.</span><span class="sxs-lookup"><span data-stu-id="6cbf2-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6cbf2-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6cbf2-125">Additional resources</span></span>

[<span data-ttu-id="6cbf2-126">B2C-rentniku häälestus Commerce'is</span><span class="sxs-lookup"><span data-stu-id="6cbf2-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="6cbf2-127">Kohandatud lehtede häälestus kasutajate sisselogimise jaoks</span><span class="sxs-lookup"><span data-stu-id="6cbf2-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
