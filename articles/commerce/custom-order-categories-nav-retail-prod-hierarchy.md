---
title: Kaubastamisolemite sortimisjärjestuse muutmine
description: Selles teemas selgitatakse mõisteid, mis on seotud erinevate kaubastamisega seotud olemite kuvamisjärjestuse juhtimisega rakenduses Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 67807c53a6ffc6dd09cc6f0e48218e2ee2de559f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207771"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="1328e-103">Kaubastamisolemite sortimisjärjestuse muutmine</span><span class="sxs-lookup"><span data-stu-id="1328e-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1328e-104">Jaemüüjad peavad toodete avastamist esmaseks vahendiks klientidega suhtlemisel kõigis kanalites.</span><span class="sxs-lookup"><span data-stu-id="1328e-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="1328e-105">Erinevad funktsioonid aitavad klientidel tooteid hõlpsasti avastada.</span><span class="sxs-lookup"><span data-stu-id="1328e-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="1328e-106">Näiteks saavad nad sirvida kategooriaid, otsida ja filtreerida.</span><span class="sxs-lookup"><span data-stu-id="1328e-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="1328e-107">Selles teemas selgitatakse mõisteid, mis on seotud erinevate kaubastamisega seotud olemite kuvamisjärjestuse juhtimisega.</span><span class="sxs-lookup"><span data-stu-id="1328e-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="1328e-108">Samuti selgitatakse, kuidas muuta sortimisjärjestust.</span><span class="sxs-lookup"><span data-stu-id="1328e-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="1328e-109">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1328e-109">Overview</span></span>

<span data-ttu-id="1328e-110">Erinevate kaubastamisega seotud olemite sorteerimise tuge on täiustatud.</span><span class="sxs-lookup"><span data-stu-id="1328e-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="1328e-111">Tugi on nüüd paremini ühitatud olemasolevate kliendi stsenaariumitega, mis varem vajasid laiendusi juurutuspartneritelt.</span><span class="sxs-lookup"><span data-stu-id="1328e-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="1328e-112">Rakenduse Retail versioonides, mis on varasemad kui versioon 10.0.5, oli kategooriate sortimisjärjestus navigeerimise hierarhias tähestikuline.</span><span class="sxs-lookup"><span data-stu-id="1328e-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="1328e-113">Uus kohandatud sortimisjärjestuse funktsioon laseb kaubastamise juhtidel konfigureerida sortimisjärjestust erinevatele kaubastamisega seotud olemitele kõigi lõppkasutaja klientide hulgas.</span><span class="sxs-lookup"><span data-stu-id="1328e-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="1328e-114">Need kliendid hõlmavad nii peakontoreid ja kõnekeskuseid.</span><span class="sxs-lookup"><span data-stu-id="1328e-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="1328e-115">Kategooriate kuvamisjärjestuse konfigureerimine tootehierarhias</span><span class="sxs-lookup"><span data-stu-id="1328e-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="1328e-116">Enne selle protseduuri lõpetamist, peate installima demoandmed oma keskkonda.</span><span class="sxs-lookup"><span data-stu-id="1328e-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="1328e-117">Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kaubanduse tootehierarhia**.</span><span class="sxs-lookup"><span data-stu-id="1328e-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="1328e-118">Klõpsake **Redigeeri kategooriahierarhiat**.</span><span class="sxs-lookup"><span data-stu-id="1328e-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="1328e-119">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1328e-119">Click **Edit**.</span></span>
4. <span data-ttu-id="1328e-120">Puus laiendage **KÕIK \> Tegevussport**.</span><span class="sxs-lookup"><span data-stu-id="1328e-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="1328e-121">Puus laiendage **KÕIK \> Meeskonnasport**.</span><span class="sxs-lookup"><span data-stu-id="1328e-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="1328e-122">Väljale **Kuvamisjärjestus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="1328e-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="1328e-123">(Arv ei saa olla negatiivne.)</span><span class="sxs-lookup"><span data-stu-id="1328e-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="1328e-124">Korrake juhiseid 4–6 iga lisatava kategooria puhul, mille järjestust soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="1328e-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="1328e-125">Kanali navigeerimise hierarhia kuvamisjärjestus kajastub peakontoris kaubanduse tootehierarhias ja väljastatud toodetes kategooriate kaupa.</span><span class="sxs-lookup"><span data-stu-id="1328e-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Kohandatud tootehierarhia sorteerimine negatiivsete väärtustega](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Väljastatud tooted kategooriate kaupa tootehierarhia põhjal kohandatult sorteeritud](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="1328e-128">Kategooriate kuvamisjärjestuse konfigureerimine kanali navigeerimise hierarhias</span><span class="sxs-lookup"><span data-stu-id="1328e-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="1328e-129">Enne selle protseduuri lõpetamist, peate installima demoandmed oma keskkonda.</span><span class="sxs-lookup"><span data-stu-id="1328e-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="1328e-130">Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kanali navigeerimise kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="1328e-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="1328e-131">Valige loendis hierarhia **Moe navigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="1328e-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="1328e-132">Klõpsake **Redigeeri kategooriahierarhiat**.</span><span class="sxs-lookup"><span data-stu-id="1328e-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="1328e-133">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1328e-133">Click **Edit**.</span></span>
5. <span data-ttu-id="1328e-134">Puus valige **Mood \> Naiste rõivad \> Naiste kingad**.</span><span class="sxs-lookup"><span data-stu-id="1328e-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="1328e-135">Väljale **Kuvamisjärjestus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="1328e-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="1328e-136">Puus valige **Mood \> Naiste rõivad \> Pluusid**.</span><span class="sxs-lookup"><span data-stu-id="1328e-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="1328e-137">Samuti saate määratleda sortimisjärjestuse alamkategooriaid.</span><span class="sxs-lookup"><span data-stu-id="1328e-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="1328e-138">Puus valige **Mood \> Meeste rõivad \> Vabaaja särgid**.</span><span class="sxs-lookup"><span data-stu-id="1328e-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="1328e-139">Väljale **Kuvamisjärjestus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="1328e-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="1328e-140">Puus valige **Mood \> Meeste rõivad \> Mantlid & jakid**.</span><span class="sxs-lookup"><span data-stu-id="1328e-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="1328e-141">Väljale **Kuvamisjärjestus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="1328e-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="1328e-142">Korrake tegevust iga lisatava kategooria puhul, mille järjestust soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="1328e-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="1328e-143">Kategooriate kuvamisjärjestuse konfigureerimine kanali navigeerimise hierarhias kajastub peakontoris, kataloogis ja kanalites.</span><span class="sxs-lookup"><span data-stu-id="1328e-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Kohandatud sorteeritud kataloogi navigeerimise hierarhia](./media/ChannelNavCustomSorted.png)

![Kanali navigeerimise hierarhia põhjal kohandatud sorteeritud kataloogi navigeerimise hierarhia](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Müügikoht kohandatud sorteeritud kategooriatega](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="1328e-147">Kohandatud sortimisjärjestuse funktsioon on vaikimisi välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="1328e-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="1328e-148">Selle ja paljude teiste funktsiooni sisselülitamiseks vaadake teemat [Funktsioonide haldus](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="1328e-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]