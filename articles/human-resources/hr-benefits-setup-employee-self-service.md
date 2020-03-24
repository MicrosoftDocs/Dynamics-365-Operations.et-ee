---
title: Töövõtja iseteeninduse konfigureerimine
description: Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092656"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="da62f-103">Töövõtja iseteeninduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="da62f-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="da62f-104">Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.</span><span class="sxs-lookup"><span data-stu-id="da62f-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="da62f-105">Soodustuse plaani paanid juhivad kasutajad soodustuse plaanide juurde, millele nad saavad registreeruda.</span><span class="sxs-lookup"><span data-stu-id="da62f-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="da62f-106">Rollikeskuse paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="da62f-106">Set up a role center tile</span></span>

1. <span data-ttu-id="da62f-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="da62f-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="da62f-108">Valige vahekaart **Rollikeskuse paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da62f-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="da62f-109">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="da62f-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="da62f-110">Väli</span><span class="sxs-lookup"><span data-stu-id="da62f-110">Field</span></span> | <span data-ttu-id="da62f-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="da62f-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="da62f-112">Paani ID</span><span class="sxs-lookup"><span data-stu-id="da62f-112">Tile ID</span></span> | <span data-ttu-id="da62f-113">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="da62f-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="da62f-114">Paani sildi tekst</span><span class="sxs-lookup"><span data-stu-id="da62f-114">Tile label text</span></span> | <span data-ttu-id="da62f-115">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="da62f-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="da62f-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="da62f-116">Description</span></span> | <span data-ttu-id="da62f-117">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="da62f-117">A description of the tile.</span></span> |
   | <span data-ttu-id="da62f-118">Interneti-aadress</span><span class="sxs-lookup"><span data-stu-id="da62f-118">Internet address</span></span> | <span data-ttu-id="da62f-119">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="da62f-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="da62f-120">Paani suurus</span><span class="sxs-lookup"><span data-stu-id="da62f-120">Tile size</span></span> | <span data-ttu-id="da62f-121">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="da62f-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="da62f-122">Siht</span><span class="sxs-lookup"><span data-stu-id="da62f-122">Target</span></span> | <span data-ttu-id="da62f-123">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="da62f-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="da62f-124">Paani taustapilt</span><span class="sxs-lookup"><span data-stu-id="da62f-124">Tile background image</span></span> | <span data-ttu-id="da62f-125">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="da62f-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="da62f-126">Alusta</span><span class="sxs-lookup"><span data-stu-id="da62f-126">Start</span></span> | <span data-ttu-id="da62f-127">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="da62f-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="da62f-128">Lõpp</span><span class="sxs-lookup"><span data-stu-id="da62f-128">End</span></span> | <span data-ttu-id="da62f-129">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="da62f-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="da62f-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="da62f-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="da62f-131">Soodustuse plaanide paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="da62f-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="da62f-132">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="da62f-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="da62f-133">Valige vahekaart **Soodustuse plaanide paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da62f-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="da62f-134">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="da62f-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="da62f-135">Väli</span><span class="sxs-lookup"><span data-stu-id="da62f-135">Field</span></span> | <span data-ttu-id="da62f-136">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="da62f-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="da62f-137">Paani ID</span><span class="sxs-lookup"><span data-stu-id="da62f-137">Tile ID</span></span> | <span data-ttu-id="da62f-138">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="da62f-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="da62f-139">Paani sildi tekst</span><span class="sxs-lookup"><span data-stu-id="da62f-139">Tile label text</span></span> | <span data-ttu-id="da62f-140">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="da62f-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="da62f-141">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="da62f-141">Description</span></span> | <span data-ttu-id="da62f-142">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="da62f-142">A description of the tile.</span></span> |
   | <span data-ttu-id="da62f-143">Interneti-aadress</span><span class="sxs-lookup"><span data-stu-id="da62f-143">Internet address</span></span> | <span data-ttu-id="da62f-144">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="da62f-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="da62f-145">Paani suurus</span><span class="sxs-lookup"><span data-stu-id="da62f-145">Tile size</span></span> | <span data-ttu-id="da62f-146">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="da62f-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="da62f-147">Siht</span><span class="sxs-lookup"><span data-stu-id="da62f-147">Target</span></span> | <span data-ttu-id="da62f-148">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="da62f-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="da62f-149">Paani taustapilt</span><span class="sxs-lookup"><span data-stu-id="da62f-149">Tile background image</span></span> | <span data-ttu-id="da62f-150">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="da62f-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="da62f-151">Alusta</span><span class="sxs-lookup"><span data-stu-id="da62f-151">Start</span></span> | <span data-ttu-id="da62f-152">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="da62f-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="da62f-153">Lõpp</span><span class="sxs-lookup"><span data-stu-id="da62f-153">End</span></span> | <span data-ttu-id="da62f-154">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="da62f-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="da62f-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="da62f-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="da62f-156">Paindliku krediidiga plaani paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="da62f-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="da62f-157">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="da62f-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="da62f-158">Valige vahekaart **Paindliku krediidiga plaani paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da62f-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="da62f-159">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="da62f-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="da62f-160">Väli</span><span class="sxs-lookup"><span data-stu-id="da62f-160">Field</span></span> | <span data-ttu-id="da62f-161">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="da62f-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="da62f-162">Paani ID</span><span class="sxs-lookup"><span data-stu-id="da62f-162">Tile ID</span></span> | <span data-ttu-id="da62f-163">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="da62f-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="da62f-164">Paani sildi tekst</span><span class="sxs-lookup"><span data-stu-id="da62f-164">Tile label text</span></span> | <span data-ttu-id="da62f-165">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="da62f-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="da62f-166">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="da62f-166">Description</span></span> | <span data-ttu-id="da62f-167">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="da62f-167">A description of the tile.</span></span> |
   | <span data-ttu-id="da62f-168">Interneti-aadress</span><span class="sxs-lookup"><span data-stu-id="da62f-168">Internet address</span></span> | <span data-ttu-id="da62f-169">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="da62f-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="da62f-170">Paani suurus</span><span class="sxs-lookup"><span data-stu-id="da62f-170">Tile size</span></span> | <span data-ttu-id="da62f-171">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="da62f-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="da62f-172">Siht</span><span class="sxs-lookup"><span data-stu-id="da62f-172">Target</span></span> | <span data-ttu-id="da62f-173">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="da62f-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="da62f-174">Paani taustapilt</span><span class="sxs-lookup"><span data-stu-id="da62f-174">Tile background image</span></span> | <span data-ttu-id="da62f-175">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="da62f-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="da62f-176">Alusta</span><span class="sxs-lookup"><span data-stu-id="da62f-176">Start</span></span> | <span data-ttu-id="da62f-177">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="da62f-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="da62f-178">Lõpp</span><span class="sxs-lookup"><span data-stu-id="da62f-178">End</span></span> | <span data-ttu-id="da62f-179">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="da62f-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="da62f-180">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="da62f-180">Select **Save**.</span></span>
