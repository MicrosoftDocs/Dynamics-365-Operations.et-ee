---
title: Meiliteatiste profiili seadistamine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555303"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="ec7d6-103">Meiliteatise profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="ec7d6-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec7d6-104">See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ec7d6-105">Kanalite loomisel saate seadistada meili teatise profiili.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="ec7d6-106">Sel viisil saab e-kirju saata klientidele erinevate kandesündmuste jaoks, nagu näiteks tellimuse loomine, tellimuse tarne olek ja makse nurjumine.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="ec7d6-107">Lisateavet meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ec7d6-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="ec7d6-108">Meiliteatiste profiili loomine</span><span class="sxs-lookup"><span data-stu-id="ec7d6-108">Create an email notification profile</span></span>

<span data-ttu-id="ec7d6-109">Meiliteatiste profiili loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="ec7d6-110">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Commerce’i meiliteavituse profiil**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="ec7d6-111">Klõpsake toimingupaanil valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="ec7d6-112">Sisestage väljale **Meiliteatiste profiil** profiili tuvastamiseks nimi.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="ec7d6-113">Väljale **Kirjeldus** sisestage asjakohane kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="ec7d6-114">Määrake lüliti **Aktiivne** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="ec7d6-115">Loo e-kirja mall</span><span class="sxs-lookup"><span data-stu-id="ec7d6-115">Create an email template</span></span>

<span data-ttu-id="ec7d6-116">Enne meiliteatise tüübi lubamist peate Cmmerce headquarters\`is looma organisatsiooni meilimalli.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="ec7d6-117">Mall määratleb iga keele puhul, mida soovite toetada, e-kirja teema, saatja, vaikekeele ja meili keha.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="ec7d6-118">Meilimalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="ec7d6-119">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Parameetrid \> Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="ec7d6-120">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ec7d6-121">Sisestage väljale **Meili ID** ID, mis aitab selle malli tuvastada.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="ec7d6-122">Sisestage väljale **Saatja nimi** saatja nimi.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="ec7d6-123">Sisestage väljale **Meili kirjeldus** tähenduslik kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="ec7d6-124">Sisestage väljale **Saatja meiliaadress** saatja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="ec7d6-125">Valige **Üldine** jaotises e-kirja malli jaoks vaikekeel.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="ec7d6-126">Vaikekeelt kasutatakse siis, kui määratud keele jaoks pole lokaliseeritud malli.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="ec7d6-127">Laiendage jaotist **Meilisõnumi sisu** ja valige malli sisu loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="ec7d6-128">Valige iga sisuüksuse jaoks keel ja sisestage meili teema rida.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="ec7d6-129">Kui meil on kehatekst, veenduge, et märgitud on märkeruut **On kehatekst**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="ec7d6-130">Valige toimingupaanil **Meilisõnum**, et sisestada meili kehatekstile mall.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="ec7d6-131">Järgmine pilt näitab mõningaid näiteid meilimalli sätetest.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-131">The following image shows some example email template settings.</span></span>

![E-kirja malli sätted.](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="ec7d6-133">Meilisündmuse loomine</span><span class="sxs-lookup"><span data-stu-id="ec7d6-133">Create an email event</span></span>

<span data-ttu-id="ec7d6-134">Meilisündmuse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="ec7d6-135">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Commerce’i meiliteavituse profiil**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="ec7d6-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="ec7d6-137">Valige ripploendist **Meili ID** meilimall.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="ec7d6-138">Valige ripploendist sobiv **Meiliteatise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="ec7d6-139">Märkige ruut **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="ec7d6-140">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ec7d6-141">Järgmine pilt näitab mõningaid näiteid sündmusest teavitamise sätetest.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-141">The following image shows some example event notification settings.</span></span>

![Sündmusest teavitamise sätted](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="ec7d6-143">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="ec7d6-143">Next steps</span></span>

<span data-ttu-id="ec7d6-144">Enne e-kirjade saatmist peate konfigureerima oma väljamineva e-posti teenuse ja seadistama pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="ec7d6-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="ec7d6-145">Lisateavet vt teemast [Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ec7d6-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="ec7d6-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ec7d6-146">Additional resources</span></span>

[<span data-ttu-id="ec7d6-147">Meilisõnumi konfigureerimine ja saatmine</span><span class="sxs-lookup"><span data-stu-id="ec7d6-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ec7d6-148">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="ec7d6-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ec7d6-149">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="ec7d6-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ec7d6-150">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="ec7d6-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
