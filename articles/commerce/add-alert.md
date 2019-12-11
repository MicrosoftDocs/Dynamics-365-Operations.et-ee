---
title: Teatise moodul
description: See teema hõlmab teatise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785348"
---
# <a name="alert-module"></a><span data-ttu-id="8b252-103">Teatise moodul</span><span class="sxs-lookup"><span data-stu-id="8b252-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8b252-104">See teema hõlmab teatise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="8b252-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8b252-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="8b252-105">Overview</span></span>

<span data-ttu-id="8b252-106">Teatise moodulit kasutatakse lehel olevate sisemiste teabesõnumite kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="8b252-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="8b252-107">Teatise moodulid toetavad tekstsõnumit ja linki.</span><span class="sxs-lookup"><span data-stu-id="8b252-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="8b252-108">Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="8b252-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="8b252-109">Teatise moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="8b252-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="8b252-110">E-kaubanduse teatise moodulite näited</span><span class="sxs-lookup"><span data-stu-id="8b252-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="8b252-111">Teatise mooduleid saab kasutada saidi päises, et näidata saidiüleseid kampaaniaid või sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="8b252-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="8b252-112">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="8b252-112">Here are some examples:</span></span>

<span data-ttu-id="8b252-113">„Iga-aastane allahindlus lõppeb 10 päeva pärast”</span><span class="sxs-lookup"><span data-stu-id="8b252-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="8b252-114">„Suured allahindlused tagasi kooli kampaania ajal.</span><span class="sxs-lookup"><span data-stu-id="8b252-114">"Save big with back to school sale.</span></span> <span data-ttu-id="8b252-115">Ostke kohe.”</span><span class="sxs-lookup"><span data-stu-id="8b252-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="8b252-116">Teatise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="8b252-116">Alert module properties</span></span>

| <span data-ttu-id="8b252-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="8b252-117">Property name</span></span>  | <span data-ttu-id="8b252-118">Väärtus</span><span class="sxs-lookup"><span data-stu-id="8b252-118">Value</span></span>                              | <span data-ttu-id="8b252-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8b252-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="8b252-120">Tekst</span><span class="sxs-lookup"><span data-stu-id="8b252-120">Text</span></span>           | <span data-ttu-id="8b252-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="8b252-121">Text</span></span>                               | <span data-ttu-id="8b252-122">Teatise moodulis ilmuv tekstsõnum.</span><span class="sxs-lookup"><span data-stu-id="8b252-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="8b252-123">Teksti joondus</span><span class="sxs-lookup"><span data-stu-id="8b252-123">Text alignment</span></span> | <span data-ttu-id="8b252-124">**Paremal**, **Vasakul** või **Keskel**</span><span class="sxs-lookup"><span data-stu-id="8b252-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="8b252-125">Väärtus, mis määratleb, kuidas tekst on teatise moodulis joondatud.</span><span class="sxs-lookup"><span data-stu-id="8b252-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="8b252-126">Unusta teatis</span><span class="sxs-lookup"><span data-stu-id="8b252-126">Dismiss alert</span></span>  | <span data-ttu-id="8b252-127">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="8b252-127">**True** or **False**</span></span>              | <span data-ttu-id="8b252-128">Kui väärtuseks on seatud **Tõene**, Saab klient teatise lõpetada.</span><span class="sxs-lookup"><span data-stu-id="8b252-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="8b252-129">Seos</span><span class="sxs-lookup"><span data-stu-id="8b252-129">Link</span></span>           | <span data-ttu-id="8b252-130">URL</span><span class="sxs-lookup"><span data-stu-id="8b252-130">URL</span></span>                                | <span data-ttu-id="8b252-131">Valikulise lingi URL.</span><span class="sxs-lookup"><span data-stu-id="8b252-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="8b252-132">Lehele teatise mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="8b252-132">Add an alert module to a page</span></span> 

<span data-ttu-id="8b252-133">Lehele teatise mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8b252-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8b252-134">Looge lehe mall nimega **teatise mall**.</span><span class="sxs-lookup"><span data-stu-id="8b252-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="8b252-135">Lisage vaikelehe pessa **Peamine** teatise moodul.</span><span class="sxs-lookup"><span data-stu-id="8b252-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="8b252-136">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8b252-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="8b252-137">Kasutage äsja loodud teatise malli, et luua leht, mille nimi on **teatise leht**.</span><span class="sxs-lookup"><span data-stu-id="8b252-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="8b252-138">Lisage uue lehe pessa **Peamine** teatise moodul.</span><span class="sxs-lookup"><span data-stu-id="8b252-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="8b252-139">Sisestage teatise mooduli sätetes teatise tekst.</span><span class="sxs-lookup"><span data-stu-id="8b252-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="8b252-140">Kui soovite teatise moodulit veelgi kohandada, võite redigeerida teisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="8b252-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="8b252-141">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="8b252-141">Save and preview the page.</span></span> <span data-ttu-id="8b252-142">Lehe ülaosas peaksite nägema teatist teie lisatud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="8b252-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="8b252-143">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8b252-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="8b252-144">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8b252-144">Additional resources</span></span>

[<span data-ttu-id="8b252-145">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="8b252-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8b252-146">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="8b252-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="8b252-147">Sisurikas plokimoodul</span><span class="sxs-lookup"><span data-stu-id="8b252-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="8b252-148">Sisupaigutuse moodul</span><span class="sxs-lookup"><span data-stu-id="8b252-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="8b252-149">Funktsioonimoodul</span><span class="sxs-lookup"><span data-stu-id="8b252-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="8b252-150">Pannoomoodul</span><span class="sxs-lookup"><span data-stu-id="8b252-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="8b252-151">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="8b252-151">Video player module</span></span>](add-video-player.md)
