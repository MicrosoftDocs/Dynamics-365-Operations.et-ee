---
title: URL-i avamine kassas
description: Selles teemas antakse ülevaade toote ja kliendi otsingufunktsiooni täiustustest rakenduses Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193199"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="cc00a-103">URL-i avamine kassas</span><span class="sxs-lookup"><span data-stu-id="cc00a-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc00a-104">Selles teemas kirjeldatakse, kuidas saate URL-i avamiseks konfigureerida Dynamics 365 Commerce nuppu jaemüügikassas.</span><span class="sxs-lookup"><span data-stu-id="cc00a-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="cc00a-105">See funktsioon ei vaja koodikohandust ja seda saab konfigureerida mittearendaja rollis.</span><span class="sxs-lookup"><span data-stu-id="cc00a-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="cc00a-106">See funktsioon võimaldab nupu konfigureerimist kassas, kasutades URL-i avamiseks nupupaneeli koostajat.</span><span class="sxs-lookup"><span data-stu-id="cc00a-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="cc00a-107">Praegu toetatakse seda järgmistes konfiguratsioonides.</span><span class="sxs-lookup"><span data-stu-id="cc00a-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="cc00a-108">Ava uues aknas.</span><span class="sxs-lookup"><span data-stu-id="cc00a-108">Open in new window.</span></span>
- <span data-ttu-id="cc00a-109">Ava kassas.</span><span class="sxs-lookup"><span data-stu-id="cc00a-109">Open within POS.</span></span>
- <span data-ttu-id="cc00a-110">Ava omarakendus.</span><span class="sxs-lookup"><span data-stu-id="cc00a-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="cc00a-111">Ava uues aknas</span><span class="sxs-lookup"><span data-stu-id="cc00a-111">Open in new window</span></span>

<span data-ttu-id="cc00a-112">Selle konfiguratsioon määratleb, kas avada URL uues aknas või rakendusesiseselt.</span><span class="sxs-lookup"><span data-stu-id="cc00a-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="cc00a-113">Kui konfigureeritud on veebi URL-i avamine rakendusesiseselt, on kassa külgmine navigeerimispaan ja ülariba nähtavad ning kasutaja interaktsiooniks saadaval.</span><span class="sxs-lookup"><span data-stu-id="cc00a-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="cc00a-114">Kui konfigureeritud on uues aknas avamine, avaneb URL rakendusel Modern POS Windowsi jaoks uues aknas ja kõigil teistel kassaklientidel uuel brauseri vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="cc00a-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="cc00a-115">Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** on valitud.</span><span class="sxs-lookup"><span data-stu-id="cc00a-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="cc00a-116">Ava kassas</span><span class="sxs-lookup"><span data-stu-id="cc00a-116">Open within POS</span></span>

<span data-ttu-id="cc00a-117">Veebi URL-i avamist kassas toetatakse praegu ainult tänapäevase kassa jaoks operatsioonisüsteemis Windows.</span><span class="sxs-lookup"><span data-stu-id="cc00a-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="cc00a-118">Teistel klientidel on see võimalus arendamisel ja plaanitud välja anda tulevastes uuendustes.</span><span class="sxs-lookup"><span data-stu-id="cc00a-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="cc00a-119">Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** pole valitud.</span><span class="sxs-lookup"><span data-stu-id="cc00a-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="cc00a-120">Ava omarakendus</span><span class="sxs-lookup"><span data-stu-id="cc00a-120">Open a native app</span></span>

<span data-ttu-id="cc00a-121">See funktsioon võimaldab ka määrata mitteveebi URL-id omarakenduse avamiseks.</span><span class="sxs-lookup"><span data-stu-id="cc00a-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="cc00a-122">Näiteks saate täpsustada URL-protokolle nagu MailTo, SIP, IM või MSTEAMS, mida seejärel käsitlevad vastavad omarakendused hostiseadmes.</span><span class="sxs-lookup"><span data-stu-id="cc00a-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="cc00a-123">Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** on valitud.</span><span class="sxs-lookup"><span data-stu-id="cc00a-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="cc00a-124">Vt Windowsi arvutites protokolli vaikeseoste määramiseks jaotist [Rakenduse vaikeseoste eksport või import](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), kui seadistate arvutit funktsiooni Deployment Image Servicing and Management (DISM) kasutades.</span><span class="sxs-lookup"><span data-stu-id="cc00a-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="cc00a-125">Kui kasutate Windowsi arvutite haldamiseks tarkvara MDM, nagu Intune, vt jaotist [Poliitika konfigureerimisteenuse pakkuja – ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="cc00a-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="cc00a-126">Kui olete kohandatud veebisaiti loov arendaja, vt jaotist [Vaikerakenduse kävitamine URI jaoks](/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="cc00a-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="cc00a-127">Ava omarakendus sujuvalt</span><span class="sxs-lookup"><span data-stu-id="cc00a-127">Open a native app seamlessly</span></span>

<span data-ttu-id="cc00a-128">Windows, iOS ja Android võimaldavad samuti rakenduste sujuvamat avamist rakenduse protokolli seose alusel.</span><span class="sxs-lookup"><span data-stu-id="cc00a-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="cc00a-129">Kui rakendust pole veebibrauserist avamiseks juba konfigureeritud, võib selleks vaja minna arendajat.</span><span class="sxs-lookup"><span data-stu-id="cc00a-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="cc00a-130">Operatsioonisüsteemi Windows jaoks vt jaotist [Rakenduste lubamine veebisaitidele rakenduse URI ohjureid kasutades](/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="cc00a-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="cc00a-131">Operatsioonisüsteemi iOS jaoks vt jaotist [Universaalsed lingid arendajatele](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="cc00a-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="cc00a-132">Androidi puhul vt teemat [Androidi rakenduste linkide käsitlemine](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="cc00a-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="cc00a-133">Klient</span><span class="sxs-lookup"><span data-stu-id="cc00a-133">Client</span></span>                | <span data-ttu-id="cc00a-134">Ava uues aknas</span><span class="sxs-lookup"><span data-stu-id="cc00a-134">Open in new window</span></span> | <span data-ttu-id="cc00a-135">Ava omarakendus</span><span class="sxs-lookup"><span data-stu-id="cc00a-135">Open native app</span></span> | <span data-ttu-id="cc00a-136">Ava kassas</span><span class="sxs-lookup"><span data-stu-id="cc00a-136">Open within POS</span></span> | <span data-ttu-id="cc00a-137">Üksikasjad</span><span class="sxs-lookup"><span data-stu-id="cc00a-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="cc00a-138">Windowsi tänapäevane kassa</span><span class="sxs-lookup"><span data-stu-id="cc00a-138">Modern POS on Windows</span></span> | <span data-ttu-id="cc00a-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc00a-139">✓\*</span></span>                | <span data-ttu-id="cc00a-140">✓</span><span class="sxs-lookup"><span data-stu-id="cc00a-140">✓</span></span>               | <span data-ttu-id="cc00a-141">✓</span><span class="sxs-lookup"><span data-stu-id="cc00a-141">✓</span></span>              | <span data-ttu-id="cc00a-142">\* Avaneb uues tänapäevase kassa aknas</span><span class="sxs-lookup"><span data-stu-id="cc00a-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="cc00a-143">Pilve kassa</span><span class="sxs-lookup"><span data-stu-id="cc00a-143">Cloud POS</span></span>             | <span data-ttu-id="cc00a-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc00a-144">✓\*</span></span>                | <span data-ttu-id="cc00a-145">✓</span><span class="sxs-lookup"><span data-stu-id="cc00a-145">✓</span></span>               | <span data-ttu-id="cc00a-146">X</span><span class="sxs-lookup"><span data-stu-id="cc00a-146">X</span></span>              | <span data-ttu-id="cc00a-147">\* Avaneb uuel brauseri vahekaardil</span><span class="sxs-lookup"><span data-stu-id="cc00a-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="cc00a-148">Tänapäevane kassa operatsioonisüsteemis iOS</span><span class="sxs-lookup"><span data-stu-id="cc00a-148">Modern POS on iOS</span></span>     | <span data-ttu-id="cc00a-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc00a-149">✓\*</span></span>                | <span data-ttu-id="cc00a-150">✓</span><span class="sxs-lookup"><span data-stu-id="cc00a-150">✓</span></span>               | <span data-ttu-id="cc00a-151">X</span><span class="sxs-lookup"><span data-stu-id="cc00a-151">X</span></span>              | <span data-ttu-id="cc00a-152">\* Avaneb uuel brauseri vahekaardil</span><span class="sxs-lookup"><span data-stu-id="cc00a-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="cc00a-153">Modern POS Androidis</span><span class="sxs-lookup"><span data-stu-id="cc00a-153">Modern POS on Android</span></span> | <span data-ttu-id="cc00a-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="cc00a-154">✓\*</span></span>                | <span data-ttu-id="cc00a-155">✓</span><span class="sxs-lookup"><span data-stu-id="cc00a-155">✓</span></span>               | <span data-ttu-id="cc00a-156">X</span><span class="sxs-lookup"><span data-stu-id="cc00a-156">X</span></span>              | <span data-ttu-id="cc00a-157">\* Avaneb uuel brauseri vahekaardil</span><span class="sxs-lookup"><span data-stu-id="cc00a-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="cc00a-158">Enne alustamist</span><span class="sxs-lookup"><span data-stu-id="cc00a-158">Before you begin</span></span>

<span data-ttu-id="cc00a-159">Enne alustamist vaadake üle konfigureerimine jaotises [Kassa ekraanipaigutused](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="cc00a-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="cc00a-160">URL-i avamine kassas</span><span class="sxs-lookup"><span data-stu-id="cc00a-160">Open URL in POS</span></span>

<span data-ttu-id="cc00a-161">URL-i konfigureerimiseks kassas avamise jaoks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cc00a-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="cc00a-162">Minge peakontoris jaotisse **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Kuvapaigutused**.</span><span class="sxs-lookup"><span data-stu-id="cc00a-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="cc00a-163">Valige **Nupupaneelid \> Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="cc00a-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="cc00a-164">Looge uus nupp.</span><span class="sxs-lookup"><span data-stu-id="cc00a-164">Create a new button.</span></span>
4. <span data-ttu-id="cc00a-165">Valige **Nupu** atribuudid.</span><span class="sxs-lookup"><span data-stu-id="cc00a-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="cc00a-166">Valige tegevuseks **Ava URL**.</span><span class="sxs-lookup"><span data-stu-id="cc00a-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="cc00a-167">Sisestage URL, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="cc00a-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="cc00a-168">Konfigureerige, kas URL uues aknas avada.</span><span class="sxs-lookup"><span data-stu-id="cc00a-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
