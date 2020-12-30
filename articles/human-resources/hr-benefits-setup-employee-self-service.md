---
title: Töövõtja iseteeninduse konfigureerimine
description: Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: d1534e37e83e22dd9860de54165c062935db3798
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418204"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="9a3dc-103">Töövõtja iseteeninduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9a3dc-103">Configure employee self service</span></span>

<span data-ttu-id="9a3dc-104">Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="9a3dc-105">Soodustuse plaani paanid juhivad kasutajad soodustuse plaanide juurde, millele nad saavad registreeruda.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="9a3dc-106">Soodustuse plaanide paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="9a3dc-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="9a3dc-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="9a3dc-108">Valige vahekaart **Soodustuse plaanide paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="9a3dc-109">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9a3dc-110">Väli</span><span class="sxs-lookup"><span data-stu-id="9a3dc-110">Field</span></span> | <span data-ttu-id="9a3dc-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9a3dc-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9a3dc-112">**Paani ID**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-112">**Tile ID**</span></span> | <span data-ttu-id="9a3dc-113">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="9a3dc-114">**Paani sildi tekst**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-114">**Tile label text**</span></span> | <span data-ttu-id="9a3dc-115">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="9a3dc-116">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-116">**Description**</span></span> | <span data-ttu-id="9a3dc-117">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-117">A description of the tile.</span></span> |
   | <span data-ttu-id="9a3dc-118">**Interneti-aadress**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-118">**Internet address**</span></span> | <span data-ttu-id="9a3dc-119">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="9a3dc-120">**Paani suurus**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-120">**Tile size**</span></span> | <span data-ttu-id="9a3dc-121">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="9a3dc-122">**Siht**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-122">**Target**</span></span> | <span data-ttu-id="9a3dc-123">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="9a3dc-124">**Paani taustapilt**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-124">**Tile background image**</span></span> | <span data-ttu-id="9a3dc-125">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="9a3dc-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="9a3dc-126">**Alusta**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-126">**Start**</span></span> | <span data-ttu-id="9a3dc-127">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="9a3dc-128">**Lõpp**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-128">**End**</span></span> | <span data-ttu-id="9a3dc-129">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="9a3dc-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="9a3dc-131">Paindliku krediidiga plaani paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="9a3dc-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="9a3dc-132">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="9a3dc-133">Valige vahekaart **Paindliku krediidiga plaani paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="9a3dc-134">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9a3dc-135">Väli</span><span class="sxs-lookup"><span data-stu-id="9a3dc-135">Field</span></span> | <span data-ttu-id="9a3dc-136">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9a3dc-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9a3dc-137">**Paani ID**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-137">**Tile ID**</span></span> | <span data-ttu-id="9a3dc-138">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="9a3dc-139">**Paani sildi tekst**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-139">**Tile label text**</span></span> | <span data-ttu-id="9a3dc-140">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="9a3dc-141">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-141">**Description**</span></span> | <span data-ttu-id="9a3dc-142">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-142">A description of the tile.</span></span> |
   | <span data-ttu-id="9a3dc-143">**Interneti-aadress**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-143">**Internet address**</span></span> | <span data-ttu-id="9a3dc-144">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="9a3dc-145">**Paani suurus**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-145">**Tile size**</span></span> | <span data-ttu-id="9a3dc-146">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="9a3dc-147">**Siht**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-147">**Target**</span></span> | <span data-ttu-id="9a3dc-148">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="9a3dc-149">**Paani taustapilt**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-149">**Tile background image**</span></span> | <span data-ttu-id="9a3dc-150">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="9a3dc-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="9a3dc-151">**Alusta**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-151">**Start**</span></span> | <span data-ttu-id="9a3dc-152">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="9a3dc-153">**Lõpp**</span><span class="sxs-lookup"><span data-stu-id="9a3dc-153">**End**</span></span> | <span data-ttu-id="9a3dc-154">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="9a3dc-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9a3dc-155">Select **Save**.</span></span>
