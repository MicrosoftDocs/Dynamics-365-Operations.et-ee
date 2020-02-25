---
title: Meiliteatiste profiili seadistamine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: feb28b9c801786f63282c4189d3eeb6d53ed07e1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003138"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="9a1e3-103">Meiliteatiste profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="9a1e3-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9a1e3-104">See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9a1e3-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9a1e3-105">Overview</span></span>

<span data-ttu-id="9a1e3-106">Enne kanalite loomist tuleb seadistada profiili, et tagada meiliteatiste saatmine erinevate sündmuste korral, nt tellimuse loomine, tellimuse tarne olek ja makse tõrge.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="9a1e3-107">Lisateavet meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span><span class="sxs-lookup"><span data-stu-id="9a1e3-107">For additional email configuration information, see [Configure and send email](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="9a1e3-108">Meiliteatiste profiili loomine</span><span class="sxs-lookup"><span data-stu-id="9a1e3-108">Create an email notification profile</span></span>

<span data-ttu-id="9a1e3-109">Meiliteatiste profiili loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="9a1e3-110">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Jaemüügi meiliteavituste profiil**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="9a1e3-111">Klõpsake toimingupaanil valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="9a1e3-112">Sisestage väljale **Meiliteatiste profiil** profiili tuvastamiseks nimi.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="9a1e3-113">Väljale **Kirjeldus** sisestage asjakohane kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="9a1e3-114">Määrake lüliti **Aktiivne** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="9a1e3-115">Loo e-kirja mall</span><span class="sxs-lookup"><span data-stu-id="9a1e3-115">Create an email template</span></span>

<span data-ttu-id="9a1e3-116">Enne kui meiliteavitusi luua saab, peate looma organisatsiooni meilimalli, mis sisaldab saatja meili andmeid ja meilimalli.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="9a1e3-117">Meilimalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="9a1e3-118">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Parameetrid \> Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="9a1e3-119">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9a1e3-120">Sisestage väljale **Meili ID** ID, mis aitab selle malli tuvastada.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="9a1e3-121">Sisestage väljale **Saatja nimi** saatja nimi.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="9a1e3-122">Sisestage väljale **Meili kirjeldus** tähenduslik kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="9a1e3-123">Sisestage väljale **Saatja meiliaadress** saatja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="9a1e3-124">Täitke jaotises **Üldine** kõik vajalikud valikulised andmed (nagu näiteks meili prioriteetsus).</span><span class="sxs-lookup"><span data-stu-id="9a1e3-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="9a1e3-125">Laiendage jaotist **Meilisõnumi sisu** ja valige malli sisu loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="9a1e3-126">Valige iga sisuüksuse jaoks keel ja sisestage meili teema rida.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="9a1e3-127">Kui meil on kehatekst, veenduge, et märgitud on märkeruut **On kehatekst**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="9a1e3-128">Valige toimingupaanil **Meilisõnum**, et sisestada meili kehatekstile mall.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="9a1e3-129">Järgmine pilt näitab mõningaid näiteid meilimalli sätetest.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-129">The following image shows some example email template settings.</span></span>

![E-kirja malli sätted.](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="9a1e3-131">Meilisündmuse loomine</span><span class="sxs-lookup"><span data-stu-id="9a1e3-131">Create an email event</span></span>

<span data-ttu-id="9a1e3-132">Meilisündmuse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="9a1e3-133">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Jaemüügi meiliteavituste profiil**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="9a1e3-134">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="9a1e3-135">Valige ripploendist **Meili ID** meilimall.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="9a1e3-136">Valige ripploendist sobiv **Meiliteatise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="9a1e3-137">Märkige ruut **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="9a1e3-138">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9a1e3-139">Järgmine pilt näitab mõningaid näiteid müügisündmuse teavituse sätetest.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-139">The following image shows some example retail event notification settings.</span></span>

![Jaemüügi sündmusest teavitamise sätted](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="9a1e3-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9a1e3-141">Additional resources</span></span>

[<span data-ttu-id="9a1e3-142">Meilisõnumi konfigureerimine ja saatmine</span><span class="sxs-lookup"><span data-stu-id="9a1e3-142">Configure and send email</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email)

[<span data-ttu-id="9a1e3-143">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="9a1e3-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9a1e3-144">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="9a1e3-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="9a1e3-145">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="9a1e3-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)