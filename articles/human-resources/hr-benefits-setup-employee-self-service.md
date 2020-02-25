---
title: Töövõtja iseteeninduse konfigureerimine
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008761"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="14355-102">Töövõtja iseteeninduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="14355-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="14355-103">Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.</span><span class="sxs-lookup"><span data-stu-id="14355-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="14355-104">Soodustuse plaani paanid juhivad kasutajad soodustuse plaanide juurde, millele nad saavad registreeruda.</span><span class="sxs-lookup"><span data-stu-id="14355-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="14355-105">Rollikeskuse paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="14355-105">Set up a role center tile</span></span>

1. <span data-ttu-id="14355-106">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="14355-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="14355-107">Valige vahekaart **Rollikeskuse paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14355-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="14355-108">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="14355-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="14355-109">Väli</span><span class="sxs-lookup"><span data-stu-id="14355-109">Field</span></span> | <span data-ttu-id="14355-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14355-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="14355-111">Paani ID</span><span class="sxs-lookup"><span data-stu-id="14355-111">Tile ID</span></span> | <span data-ttu-id="14355-112">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="14355-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="14355-113">Paani sildi tekst</span><span class="sxs-lookup"><span data-stu-id="14355-113">Tile label text</span></span> | <span data-ttu-id="14355-114">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="14355-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="14355-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14355-115">Description</span></span> | <span data-ttu-id="14355-116">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="14355-116">A description of the tile.</span></span> |
   | <span data-ttu-id="14355-117">Interneti-aadress</span><span class="sxs-lookup"><span data-stu-id="14355-117">Internet address</span></span> | <span data-ttu-id="14355-118">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="14355-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="14355-119">Paani suurus</span><span class="sxs-lookup"><span data-stu-id="14355-119">Tile size</span></span> | <span data-ttu-id="14355-120">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="14355-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="14355-121">Siht</span><span class="sxs-lookup"><span data-stu-id="14355-121">Target</span></span> | <span data-ttu-id="14355-122">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="14355-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="14355-123">Paani taustapilt</span><span class="sxs-lookup"><span data-stu-id="14355-123">Tile background image</span></span> | <span data-ttu-id="14355-124">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="14355-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="14355-125">Alusta</span><span class="sxs-lookup"><span data-stu-id="14355-125">Start</span></span> | <span data-ttu-id="14355-126">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="14355-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="14355-127">Lõpp</span><span class="sxs-lookup"><span data-stu-id="14355-127">End</span></span> | <span data-ttu-id="14355-128">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="14355-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="14355-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14355-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="14355-130">Soodustuse plaanide paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="14355-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="14355-131">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="14355-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="14355-132">Valige vahekaart **Soodustuse plaanide paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14355-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="14355-133">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="14355-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="14355-134">Väli</span><span class="sxs-lookup"><span data-stu-id="14355-134">Field</span></span> | <span data-ttu-id="14355-135">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14355-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="14355-136">Paani ID</span><span class="sxs-lookup"><span data-stu-id="14355-136">Tile ID</span></span> | <span data-ttu-id="14355-137">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="14355-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="14355-138">Paani sildi tekst</span><span class="sxs-lookup"><span data-stu-id="14355-138">Tile label text</span></span> | <span data-ttu-id="14355-139">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="14355-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="14355-140">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14355-140">Description</span></span> | <span data-ttu-id="14355-141">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="14355-141">A description of the tile.</span></span> |
   | <span data-ttu-id="14355-142">Interneti-aadress</span><span class="sxs-lookup"><span data-stu-id="14355-142">Internet address</span></span> | <span data-ttu-id="14355-143">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="14355-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="14355-144">Paani suurus</span><span class="sxs-lookup"><span data-stu-id="14355-144">Tile size</span></span> | <span data-ttu-id="14355-145">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="14355-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="14355-146">Siht</span><span class="sxs-lookup"><span data-stu-id="14355-146">Target</span></span> | <span data-ttu-id="14355-147">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="14355-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="14355-148">Paani taustapilt</span><span class="sxs-lookup"><span data-stu-id="14355-148">Tile background image</span></span> | <span data-ttu-id="14355-149">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="14355-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="14355-150">Alusta</span><span class="sxs-lookup"><span data-stu-id="14355-150">Start</span></span> | <span data-ttu-id="14355-151">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="14355-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="14355-152">Lõpp</span><span class="sxs-lookup"><span data-stu-id="14355-152">End</span></span> | <span data-ttu-id="14355-153">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="14355-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="14355-154">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14355-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="14355-155">Paindliku krediidiga plaani paani häälestamine</span><span class="sxs-lookup"><span data-stu-id="14355-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="14355-156">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="14355-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="14355-157">Valige vahekaart **Paindliku krediidiga plaani paani seadistamine** ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14355-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="14355-158">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="14355-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="14355-159">Väli</span><span class="sxs-lookup"><span data-stu-id="14355-159">Field</span></span> | <span data-ttu-id="14355-160">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14355-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="14355-161">Paani ID</span><span class="sxs-lookup"><span data-stu-id="14355-161">Tile ID</span></span> | <span data-ttu-id="14355-162">Paani kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="14355-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="14355-163">Paani sildi tekst</span><span class="sxs-lookup"><span data-stu-id="14355-163">Tile label text</span></span> | <span data-ttu-id="14355-164">Iseteeninduses paani jaoks kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="14355-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="14355-165">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14355-165">Description</span></span> | <span data-ttu-id="14355-166">Paani kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="14355-166">A description of the tile.</span></span> |
   | <span data-ttu-id="14355-167">Interneti-aadress</span><span class="sxs-lookup"><span data-stu-id="14355-167">Internet address</span></span> | <span data-ttu-id="14355-168">Sisestage töövõtja iseteeninduse lehe URL.</span><span class="sxs-lookup"><span data-stu-id="14355-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="14355-169">Paani suurus</span><span class="sxs-lookup"><span data-stu-id="14355-169">Tile size</span></span> | <span data-ttu-id="14355-170">Paani suurus: väike, keskmine või suur.</span><span class="sxs-lookup"><span data-stu-id="14355-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="14355-171">Siht</span><span class="sxs-lookup"><span data-stu-id="14355-171">Target</span></span> | <span data-ttu-id="14355-172">Määrab, kas leht peaks avanema uues aknas või praeguses aknas.</span><span class="sxs-lookup"><span data-stu-id="14355-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="14355-173">Paani taustapilt</span><span class="sxs-lookup"><span data-stu-id="14355-173">Tile background image</span></span> | <span data-ttu-id="14355-174">Paani jaoks kasutatava kujutise URL (valikuline).</span><span class="sxs-lookup"><span data-stu-id="14355-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="14355-175">Alusta</span><span class="sxs-lookup"><span data-stu-id="14355-175">Start</span></span> | <span data-ttu-id="14355-176">Paani saadaval olemise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="14355-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="14355-177">Lõpp</span><span class="sxs-lookup"><span data-stu-id="14355-177">End</span></span> | <span data-ttu-id="14355-178">Paani saadaval olemise lõpukuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="14355-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="14355-179">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14355-179">Select **Save**.</span></span>
