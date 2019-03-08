---
title: URL-i avamine kassas
description: Selles teemas antakse ülevaade toote ja kliendi otsingufunktsiooni täiustustest rakenduses Microsoft Dynamics 365 for Retail.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "327086"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="64c40-103">URL-i avamine kassas</span><span class="sxs-lookup"><span data-stu-id="64c40-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64c40-104">Selles teemas kirjeldatakse, kuidas saate URL-i avamiseks konfigureerida nuppu jaemüügikassas.</span><span class="sxs-lookup"><span data-stu-id="64c40-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="64c40-105">See funktsioon ei vaja koodikohandust ja seda saab konfigureerida mittearendaja rollis.</span><span class="sxs-lookup"><span data-stu-id="64c40-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="64c40-106">See funktsioon on saadaval rakenduse Dynamics 365 for Finance and Operations versiooni 8.1.3 väljalaske (järk 8.1.227.10014) või uuema osana.</span><span class="sxs-lookup"><span data-stu-id="64c40-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="64c40-107">See funktsioon võimaldab nupu konfigureerimist kassas, kasutades URL-i avamiseks nupupaneeli koostajat.</span><span class="sxs-lookup"><span data-stu-id="64c40-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="64c40-108">Praegu toetatakse seda järgmistes konfiguratsioonides.</span><span class="sxs-lookup"><span data-stu-id="64c40-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="64c40-109">Ava uues aknas.</span><span class="sxs-lookup"><span data-stu-id="64c40-109">Open in new window.</span></span>
- <span data-ttu-id="64c40-110">Ava kassas.</span><span class="sxs-lookup"><span data-stu-id="64c40-110">Open within POS.</span></span>
- <span data-ttu-id="64c40-111">Ava omarakendus.</span><span class="sxs-lookup"><span data-stu-id="64c40-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="64c40-112">Ava uues aknas</span><span class="sxs-lookup"><span data-stu-id="64c40-112">Open in new window</span></span>

<span data-ttu-id="64c40-113">Selle konfiguratsioon määratleb, kas avada URL uues aknas või rakendusesiseselt.</span><span class="sxs-lookup"><span data-stu-id="64c40-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="64c40-114">Kui konfigureeritud on veebi URL-i avamine rakendusesiseselt, on kassa külgmine navigeerimispaan ja ülariba nähtavad ning kasutaja interaktsiooniks saadaval.</span><span class="sxs-lookup"><span data-stu-id="64c40-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="64c40-115">Kui konfigureeritud on uues aknas avamine, avaneb URL rakendusel Modern POS Windowsi jaoks uues aknas ja kõigil teistel kassaklientidel uuel brauseri vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="64c40-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="64c40-116">Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** on valitud.</span><span class="sxs-lookup"><span data-stu-id="64c40-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="64c40-117">Ava kassas</span><span class="sxs-lookup"><span data-stu-id="64c40-117">Open within POS</span></span>

<span data-ttu-id="64c40-118">Veebi URL-i avamist kassas toetatakse praegu ainult tänapäevase kassa jaoks operatsioonisüsteemis Windows.</span><span class="sxs-lookup"><span data-stu-id="64c40-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="64c40-119">Teistel klientidel on see võimalus arendamisel ja plaanitud välja anda tulevastes uuendustes.</span><span class="sxs-lookup"><span data-stu-id="64c40-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="64c40-120">Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** pole valitud.</span><span class="sxs-lookup"><span data-stu-id="64c40-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="64c40-121">Ava omarakendus</span><span class="sxs-lookup"><span data-stu-id="64c40-121">Open a native app</span></span>

<span data-ttu-id="64c40-122">See funktsioon võimaldab ka määrata mitteveebi URL-id omarakenduse avamiseks.</span><span class="sxs-lookup"><span data-stu-id="64c40-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="64c40-123">Näiteks saate täpsustada URL-protokolle nagu MailTo, SIP, IM või MSTEAMS, mida seejärel käsitlevad vastavad omarakendused hostiseadmes.</span><span class="sxs-lookup"><span data-stu-id="64c40-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="64c40-124">Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** on valitud.</span><span class="sxs-lookup"><span data-stu-id="64c40-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="64c40-125">Vt Windowsi arvutites protokolli vaikeseoste määramiseks jaotist [Rakenduse vaikeseoste eksport või import](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), kui seadistate arvutit funktsiooni Deployment Image Servicing and Management (DISM) kasutades.</span><span class="sxs-lookup"><span data-stu-id="64c40-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="64c40-126">Kui kasutate Windowsi arvutite haldamiseks tarkvara MDM, nagu Intune, vt jaotist [Poliitika konfigureerimisteenuse pakkuja – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="64c40-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="64c40-127">Kui olete kohandatud veebisaiti loov arendaja, vt jaotist [Vaikerakenduse kävitamine URI jaoks](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="64c40-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="64c40-128">Ava omarakendus sujuvalt</span><span class="sxs-lookup"><span data-stu-id="64c40-128">Open a native app seamlessly</span></span>

<span data-ttu-id="64c40-129">Windows, iOS ja Android võimaldavad samuti rakenduste sujuvamat avamist rakenduse protokolli seose alusel.</span><span class="sxs-lookup"><span data-stu-id="64c40-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="64c40-130">Kui rakendust pole veebibrauserist avamiseks juba konfigureeritud, võib selleks vaja minna arendajat.</span><span class="sxs-lookup"><span data-stu-id="64c40-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="64c40-131">Operatsioonisüsteemi Windows jaoks vt jaotist [Rakenduste lubamine veebisaitidele rakenduse URI ohjureid kasutades](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="64c40-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="64c40-132">Operatsioonisüsteemi iOS jaoks vt jaotist [Universaalsed lingid arendajatele](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="64c40-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="64c40-133">Androidi puhul vt teemat [Androidi rakenduste linkide käsitlemine](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="64c40-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="64c40-134">Klient</span><span class="sxs-lookup"><span data-stu-id="64c40-134">Client</span></span>                | <span data-ttu-id="64c40-135">Ava uues aknas</span><span class="sxs-lookup"><span data-stu-id="64c40-135">Open in new window</span></span> | <span data-ttu-id="64c40-136">Ava omarakendus</span><span class="sxs-lookup"><span data-stu-id="64c40-136">Open native app</span></span> | <span data-ttu-id="64c40-137">Ava kassas</span><span class="sxs-lookup"><span data-stu-id="64c40-137">Open within POS</span></span> | <span data-ttu-id="64c40-138">Üksikasjad</span><span class="sxs-lookup"><span data-stu-id="64c40-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="64c40-139">Windowsi tänapäevane kassa</span><span class="sxs-lookup"><span data-stu-id="64c40-139">Modern POS on Windows</span></span> | <span data-ttu-id="64c40-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="64c40-140">✓\*</span></span>                | <span data-ttu-id="64c40-141">✓</span><span class="sxs-lookup"><span data-stu-id="64c40-141">✓</span></span>               | <span data-ttu-id="64c40-142">✓</span><span class="sxs-lookup"><span data-stu-id="64c40-142">✓</span></span>              | <span data-ttu-id="64c40-143">\* Avaneb uues tänapäevase kassa aknas</span><span class="sxs-lookup"><span data-stu-id="64c40-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="64c40-144">Pilve kassa</span><span class="sxs-lookup"><span data-stu-id="64c40-144">Cloud POS</span></span>             | <span data-ttu-id="64c40-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="64c40-145">✓\*</span></span>                | <span data-ttu-id="64c40-146">✓</span><span class="sxs-lookup"><span data-stu-id="64c40-146">✓</span></span>               | <span data-ttu-id="64c40-147">X</span><span class="sxs-lookup"><span data-stu-id="64c40-147">X</span></span>              | <span data-ttu-id="64c40-148">\* Avaneb uuel brauseri vahekaardil</span><span class="sxs-lookup"><span data-stu-id="64c40-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="64c40-149">Tänapäevane kassa operatsioonisüsteemis iOS</span><span class="sxs-lookup"><span data-stu-id="64c40-149">Modern POS on iOS</span></span>     | <span data-ttu-id="64c40-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="64c40-150">✓\*</span></span>                | <span data-ttu-id="64c40-151">✓</span><span class="sxs-lookup"><span data-stu-id="64c40-151">✓</span></span>               | <span data-ttu-id="64c40-152">X</span><span class="sxs-lookup"><span data-stu-id="64c40-152">X</span></span>              | <span data-ttu-id="64c40-153">\* Avaneb uuel brauseri vahekaardil</span><span class="sxs-lookup"><span data-stu-id="64c40-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="64c40-154">Modern POS Androidis</span><span class="sxs-lookup"><span data-stu-id="64c40-154">Modern POS on Android</span></span> | <span data-ttu-id="64c40-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="64c40-155">✓\*</span></span>                | <span data-ttu-id="64c40-156">✓</span><span class="sxs-lookup"><span data-stu-id="64c40-156">✓</span></span>               | <span data-ttu-id="64c40-157">X</span><span class="sxs-lookup"><span data-stu-id="64c40-157">X</span></span>              | <span data-ttu-id="64c40-158">\* Avaneb uuel brauseri vahekaardil</span><span class="sxs-lookup"><span data-stu-id="64c40-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="64c40-159">Enne alustamist</span><span class="sxs-lookup"><span data-stu-id="64c40-159">Before you begin</span></span>

<span data-ttu-id="64c40-160">Enne alustamist vaadake üle konfigureerimine jaotises [Kassa ekraanipaigutused](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="64c40-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="64c40-161">URL-i avamine kassas</span><span class="sxs-lookup"><span data-stu-id="64c40-161">Open URL in POS</span></span>

<span data-ttu-id="64c40-162">URL-i konfigureerimiseks kassas avamise jaoks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="64c40-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="64c40-163">Minge peakontoris jaotisse **Jaemüük \> Kanali seadistus \> Kassa seadistus \> Kassa \> Kuvapaigutused**.</span><span class="sxs-lookup"><span data-stu-id="64c40-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="64c40-164">Valige **Nupupaneelid \> Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="64c40-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="64c40-165">Looge uus nupp.</span><span class="sxs-lookup"><span data-stu-id="64c40-165">Create a new button.</span></span>
4. <span data-ttu-id="64c40-166">Valige **Nupu** atribuudid.</span><span class="sxs-lookup"><span data-stu-id="64c40-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="64c40-167">Valige tegevuseks **Ava URL**.</span><span class="sxs-lookup"><span data-stu-id="64c40-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="64c40-168">Sisestage URL, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="64c40-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="64c40-169">Konfigureerige, kas URL uues aknas avada.</span><span class="sxs-lookup"><span data-stu-id="64c40-169">Configure whether to open the URL in a new window.</span></span>
