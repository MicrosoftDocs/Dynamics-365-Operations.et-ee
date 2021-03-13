---
title: Töövõtja iseteeninduse konfigureerimine
description: Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 32981812eac3c08e1409fe5470b550e421f5d6c9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112222"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="c6d46-103">Töövõtja iseteeninduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c6d46-103">Configure employee self service</span></span>

<span data-ttu-id="c6d46-104">Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.</span><span class="sxs-lookup"><span data-stu-id="c6d46-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="c6d46-105">Soodustuse plaani paanid juhivad kasutajad soodustuse plaanide juurde, millele nad saavad registreeruda.</span><span class="sxs-lookup"><span data-stu-id="c6d46-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="c6d46-106">Soodustuse plaanide paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="c6d46-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="c6d46-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c6d46-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="c6d46-108">Valige vahekaart **Soodustuse plaanide paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c6d46-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="c6d46-109">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="c6d46-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c6d46-110">Väli</span><span class="sxs-lookup"><span data-stu-id="c6d46-110">Field</span></span> | <span data-ttu-id="c6d46-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c6d46-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c6d46-112">**Paani ID**</span><span class="sxs-lookup"><span data-stu-id="c6d46-112">**Tile ID**</span></span> | <span data-ttu-id="c6d46-113">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="c6d46-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="c6d46-114">**Paani sildi tekst**</span><span class="sxs-lookup"><span data-stu-id="c6d46-114">**Tile label text**</span></span> | <span data-ttu-id="c6d46-115">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="c6d46-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="c6d46-116">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="c6d46-116">**Description**</span></span> | <span data-ttu-id="c6d46-117">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c6d46-117">A description of the tile.</span></span> |
   | <span data-ttu-id="c6d46-118">**Interneti-aadress**</span><span class="sxs-lookup"><span data-stu-id="c6d46-118">**Internet address**</span></span> | <span data-ttu-id="c6d46-119">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="c6d46-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="c6d46-120">**Paani suurus**</span><span class="sxs-lookup"><span data-stu-id="c6d46-120">**Tile size**</span></span> | <span data-ttu-id="c6d46-121">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="c6d46-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="c6d46-122">**Siht**</span><span class="sxs-lookup"><span data-stu-id="c6d46-122">**Target**</span></span> | <span data-ttu-id="c6d46-123">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="c6d46-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="c6d46-124">**Paani taustapilt**</span><span class="sxs-lookup"><span data-stu-id="c6d46-124">**Tile background image**</span></span> | <span data-ttu-id="c6d46-125">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="c6d46-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="c6d46-126">**Alusta**</span><span class="sxs-lookup"><span data-stu-id="c6d46-126">**Start**</span></span> | <span data-ttu-id="c6d46-127">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c6d46-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="c6d46-128">**Lõpp**</span><span class="sxs-lookup"><span data-stu-id="c6d46-128">**End**</span></span> | <span data-ttu-id="c6d46-129">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c6d46-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="c6d46-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c6d46-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="c6d46-131">Paindliku krediidiga plaani paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="c6d46-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="c6d46-132">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c6d46-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="c6d46-133">Valige vahekaart **Paindliku krediidiga plaani paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c6d46-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="c6d46-134">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="c6d46-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c6d46-135">Väli</span><span class="sxs-lookup"><span data-stu-id="c6d46-135">Field</span></span> | <span data-ttu-id="c6d46-136">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c6d46-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c6d46-137">**Paani ID**</span><span class="sxs-lookup"><span data-stu-id="c6d46-137">**Tile ID**</span></span> | <span data-ttu-id="c6d46-138">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="c6d46-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="c6d46-139">**Paani sildi tekst**</span><span class="sxs-lookup"><span data-stu-id="c6d46-139">**Tile label text**</span></span> | <span data-ttu-id="c6d46-140">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="c6d46-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="c6d46-141">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="c6d46-141">**Description**</span></span> | <span data-ttu-id="c6d46-142">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c6d46-142">A description of the tile.</span></span> |
   | <span data-ttu-id="c6d46-143">**Interneti-aadress**</span><span class="sxs-lookup"><span data-stu-id="c6d46-143">**Internet address**</span></span> | <span data-ttu-id="c6d46-144">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="c6d46-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="c6d46-145">**Paani suurus**</span><span class="sxs-lookup"><span data-stu-id="c6d46-145">**Tile size**</span></span> | <span data-ttu-id="c6d46-146">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="c6d46-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="c6d46-147">**Siht**</span><span class="sxs-lookup"><span data-stu-id="c6d46-147">**Target**</span></span> | <span data-ttu-id="c6d46-148">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="c6d46-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="c6d46-149">**Paani taustapilt**</span><span class="sxs-lookup"><span data-stu-id="c6d46-149">**Tile background image**</span></span> | <span data-ttu-id="c6d46-150">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="c6d46-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="c6d46-151">**Alusta**</span><span class="sxs-lookup"><span data-stu-id="c6d46-151">**Start**</span></span> | <span data-ttu-id="c6d46-152">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c6d46-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="c6d46-153">**Lõpp**</span><span class="sxs-lookup"><span data-stu-id="c6d46-153">**End**</span></span> | <span data-ttu-id="c6d46-154">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c6d46-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="c6d46-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c6d46-155">Select **Save**.</span></span>
