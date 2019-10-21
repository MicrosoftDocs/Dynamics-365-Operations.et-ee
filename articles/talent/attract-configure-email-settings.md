---
title: Meilisätete konfigureerimine rakenduses Microsoft Dynamics 365 Talent – Attract
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 Talent - Attract saadetud e-posti sätteid.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008658"
---
# <a name="configure-email-settings"></a><span data-ttu-id="ef8de-103">Meilisätete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ef8de-103">Configure email settings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ef8de-104">Teie kaubamärk loob usalduse ja aitab teil luua suhteid kandidaatidega, enne kui nad isegi teie vabadele töökohtadele kandideerivad.</span><span class="sxs-lookup"><span data-stu-id="ef8de-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="ef8de-105">Positiivne kaubamärgi taju meelitab parimaid talente ja suurendab olemasolevate töötajate lojaalsust.</span><span class="sxs-lookup"><span data-stu-id="ef8de-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="ef8de-106">Microsoft Dynamics 365 Talent: Attract võimaldab teil konfigureerida e-kirju nii, et need peegeldavad teie ettevõtte kaubamärki.</span><span class="sxs-lookup"><span data-stu-id="ef8de-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="ef8de-107">Seetõttu saate pakkuda töökoha kandidaatidele järjepideva kogemuse, kui nad läbi kandideerimisprotsessi edenevad.</span><span class="sxs-lookup"><span data-stu-id="ef8de-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="ef8de-108">Attract võimaldab teil teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="ef8de-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="ef8de-109">Konfigureerige e-posti sätted nii, et kasutatakse teie ettevõtte Microsoft Exchange'i e-posti teenuse kontot.</span><span class="sxs-lookup"><span data-stu-id="ef8de-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="ef8de-110">Sel viisil teavad kandidaadid, et meilid tulevad teie ettevõttest.</span><span class="sxs-lookup"><span data-stu-id="ef8de-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="ef8de-111">Näiteks saate konfigureerida sätteid nii, et kandidaadid saavad e-kirju aadressilt `recruiting@contoso.com`, mitte `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="ef8de-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="ef8de-112">Loogu kogu meilisuhtlusele ühtne tootjakohanduse, määrates kõigile meilimallidele üldine päis ja jalus.</span><span class="sxs-lookup"><span data-stu-id="ef8de-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="ef8de-113">Attracti häälestamiseks, nii et see kasutaks meilide saatmiseks teie ettevõtte meiliteenuse kontot, vajate tervikliku värbamise lisandmoodulit.</span><span class="sxs-lookup"><span data-stu-id="ef8de-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="ef8de-114">E-posti teenuse konto ühendamine</span><span class="sxs-lookup"><span data-stu-id="ef8de-114">Connect an email service account</span></span>

<span data-ttu-id="ef8de-115">Ühendades oma ettevõtte meiliteenuse konto, saate luua kaubamärgiga e-posti kogemuse oma kandidaatidele.</span><span class="sxs-lookup"><span data-stu-id="ef8de-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="ef8de-116">Kui te oma ettevõtte kontot ei ühenda, kasutab Attract vaikimisi Microsofti kaubamängiga meiliteenuste kontot.</span><span class="sxs-lookup"><span data-stu-id="ef8de-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="ef8de-117">Valige lehe paremast ülanurgast hammasratta sümbol **Sätted** ja seejärel valige **Halduskeskus**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="ef8de-118">Vahekaardil **Meilisätted** valige jaotises **Meiliteenuste kontod** suvand **Ühenda ettevõtte konto**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Oma ettevõtte meiliteenuse konto ühendamine Attractis](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="ef8de-120">Lisateavet ühiskasutatava meilikonto loomise kohta vt teemast [Ühiskasutatavad postkastid rakenduses Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="ef8de-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="ef8de-121">Logige Microsofti sisselogimise aknas sisse, kasutades oma ettevõtte mandaate.</span><span class="sxs-lookup"><span data-stu-id="ef8de-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="ef8de-122">Kui te ei ole veel meiliteenuse kontot seadistanud või kui soovite lisada uue, valige käsk **Lisa uus teenusekonto**ja sisestage seejärel oma e-posti andmed.</span><span class="sxs-lookup"><span data-stu-id="ef8de-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="ef8de-123">Kui olete juba selle meiliteenuse konto seadistanud, mida soovite kasutada, valige see.</span><span class="sxs-lookup"><span data-stu-id="ef8de-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="ef8de-124">Kui teie meiliteenuse konto on edukalt konfigureeritud, kuvatakse see jaotises **Meiliteenuse kontod**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="ef8de-125">E-posti teenuse konto eemaldamine</span><span class="sxs-lookup"><span data-stu-id="ef8de-125">Disconnect an email service account</span></span>

<span data-ttu-id="ef8de-126">Kui soovite lõpetada oma ettevõtte domeeni kasutamise Attracti meiiteenuses, saate meiliteenuse konto eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ef8de-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="ef8de-127">Valige lehe paremast ülanurgast hammasratta sümbol **Sätted** ja seejärel valige **Halduskeskus**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="ef8de-128">Valige vahekaardil **Meilisätted** jaotises **Meiliteenuste kontod** nupp **Veel** (kolm vertikaalset punkti) selle meiliteenuste konto kõrval, mida soovite eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ef8de-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="ef8de-129">Valige **Eemalda meilikonto**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-129">Select **Disconnect email account**.</span></span>

    ![Oma ettevõtte meiliteenuse konto eemaldamine](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="ef8de-131">Kui teil palutakse toiming kinnitada, valige **Katkesta ühendus**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Oma ettevõtte meiliteenuse konto eemaldamise kinnitamine](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="ef8de-133">Kui te ei ühenda erinevat meiliteenuste kontot, saadetakse Attractist saadetud meilid vaikimisi kasutades Microsofti kaubamärgiga meiliteenuste kontot.</span><span class="sxs-lookup"><span data-stu-id="ef8de-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="ef8de-134">E-kirja malli sätete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ef8de-134">Configure email template settings</span></span>

<span data-ttu-id="ef8de-135">Saate laadida üles pilti oma ettevõtte logost või muid andmeid oma meilide kohandatud päise jaoks.</span><span class="sxs-lookup"><span data-stu-id="ef8de-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="ef8de-136">Saate anda meili jaluses ka linke oma privaatsuspoliitikale ja kasutustingimustele.</span><span class="sxs-lookup"><span data-stu-id="ef8de-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="ef8de-137">Peate järgima oma riigi või piirkonna kohaldatavaid seadusi ja samuti selle riigi või piirkonna seadusi, mille alla kuulub meili saaja.</span><span class="sxs-lookup"><span data-stu-id="ef8de-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="ef8de-138">Need seadused hõlmavad rämpsposti vastaseid reegleid.</span><span class="sxs-lookup"><span data-stu-id="ef8de-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="ef8de-139">Valige lehe paremast ülanurgast hammasratta sümbol **Sätted** ja seejärel valige **Halduskeskus**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="ef8de-140">Lohistage vahekaardil **Meilisätted** jaotises **E-kirja malli sätted** oma meilide päises kasutada soovitud pilt pildiaknasse või sirvige vastava faili leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="ef8de-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="ef8de-141">Olemasoleva pildi asendamiseks peate esmalt valima selle kõrval suvandi **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="ef8de-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="ef8de-142">Pilt peab olema JPEG, JPG, PNG või SVG fail.</span><span class="sxs-lookup"><span data-stu-id="ef8de-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="ef8de-143">Piltide soovituslik suurus on vahemikus 25 – 800 pikslit (laius) ja 25 – 150 pikslit (kõrgus).</span><span class="sxs-lookup"><span data-stu-id="ef8de-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="ef8de-144">Päise maksimaalne failimaht on 1 megabaiti (MB).</span><span class="sxs-lookup"><span data-stu-id="ef8de-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Teie ettevõtte e-posti päise jaoks pildi lisamine](./media/attract-admin-email-header.png)

3. <span data-ttu-id="ef8de-146">Andke jaotises **Teie suhtlusele kohaldatav privaatsuspoliitika** link teie ettevõtte privaatsuspoliitikale.</span><span class="sxs-lookup"><span data-stu-id="ef8de-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="ef8de-147">Andke jaotises **Teie suhtlusele kohaldatavad tingimused** link teie ettevõtte kasutustingimustele.</span><span class="sxs-lookup"><span data-stu-id="ef8de-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Oma ettevõtte privaatsuspoliitika ja kasutustingimuste linkide lisamine e-posti jalusele](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="ef8de-149">Valige **Salvesta**, et salvestada e-kirja malli sätted.</span><span class="sxs-lookup"><span data-stu-id="ef8de-149">Select **Save** to save your email template settings.</span></span>
