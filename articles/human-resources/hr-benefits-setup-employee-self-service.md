---
title: Töövõtja iseteeninduse konfigureerimine
description: Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797931"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="e9ce7-103">Töövõtja iseteeninduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e9ce7-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9ce7-104">Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="e9ce7-105">Soodustuse plaani paanid juhivad kasutajad soodustuse plaanide juurde, millele nad saavad registreeruda.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="e9ce7-106">Soodustuse plaanide paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="e9ce7-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="e9ce7-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="e9ce7-108">Valige vahekaart **Soodustuse plaanide paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="e9ce7-109">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e9ce7-110">Väli</span><span class="sxs-lookup"><span data-stu-id="e9ce7-110">Field</span></span> | <span data-ttu-id="e9ce7-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e9ce7-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e9ce7-112">**Paani ID**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-112">**Tile ID**</span></span> | <span data-ttu-id="e9ce7-113">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="e9ce7-114">**Paani sildi tekst**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-114">**Tile label text**</span></span> | <span data-ttu-id="e9ce7-115">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="e9ce7-116">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-116">**Description**</span></span> | <span data-ttu-id="e9ce7-117">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-117">A description of the tile.</span></span> |
   | <span data-ttu-id="e9ce7-118">**Interneti-aadress**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-118">**Internet address**</span></span> | <span data-ttu-id="e9ce7-119">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="e9ce7-120">**Paani suurus**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-120">**Tile size**</span></span> | <span data-ttu-id="e9ce7-121">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="e9ce7-122">**Siht**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-122">**Target**</span></span> | <span data-ttu-id="e9ce7-123">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="e9ce7-124">**Paani taustapilt**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-124">**Tile background image**</span></span> | <span data-ttu-id="e9ce7-125">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="e9ce7-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="e9ce7-126">**Alusta**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-126">**Start**</span></span> | <span data-ttu-id="e9ce7-127">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="e9ce7-128">**Lõpp**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-128">**End**</span></span> | <span data-ttu-id="e9ce7-129">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="e9ce7-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="e9ce7-131">Paindliku krediidiga plaani paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="e9ce7-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="e9ce7-132">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="e9ce7-133">Valige vahekaart **Paindliku krediidiga plaani paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="e9ce7-134">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e9ce7-135">Väli</span><span class="sxs-lookup"><span data-stu-id="e9ce7-135">Field</span></span> | <span data-ttu-id="e9ce7-136">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e9ce7-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e9ce7-137">**Paani ID**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-137">**Tile ID**</span></span> | <span data-ttu-id="e9ce7-138">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="e9ce7-139">**Paani sildi tekst**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-139">**Tile label text**</span></span> | <span data-ttu-id="e9ce7-140">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="e9ce7-141">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-141">**Description**</span></span> | <span data-ttu-id="e9ce7-142">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-142">A description of the tile.</span></span> |
   | <span data-ttu-id="e9ce7-143">**Interneti-aadress**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-143">**Internet address**</span></span> | <span data-ttu-id="e9ce7-144">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="e9ce7-145">**Paani suurus**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-145">**Tile size**</span></span> | <span data-ttu-id="e9ce7-146">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="e9ce7-147">**Siht**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-147">**Target**</span></span> | <span data-ttu-id="e9ce7-148">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="e9ce7-149">**Paani taustapilt**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-149">**Tile background image**</span></span> | <span data-ttu-id="e9ce7-150">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="e9ce7-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="e9ce7-151">**Alusta**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-151">**Start**</span></span> | <span data-ttu-id="e9ce7-152">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="e9ce7-153">**Lõpp**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-153">**End**</span></span> | <span data-ttu-id="e9ce7-154">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="e9ce7-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]