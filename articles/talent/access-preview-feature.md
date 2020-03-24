---
title: Funktsioonide haldamine
description: Selles teemas kirjeldatakse, kuidas administraator saab lubada eelvaatefunktsioone rakenduses Microsoft Dynamics 365 Talent, ja loetletakse funktsioone, mis on praegu eelvaate jaoks lubatud.
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
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124792"
---
# <a name="manage-features"></a><span data-ttu-id="451bb-103">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="451bb-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="451bb-104">Microsoft Dynamics 365 Human Resources pidevate inimkapitali juhtimisvõimaluste (HCM) levitamise osana tahame, et kliendid saaksid proovida uusi funktsioone niipea kui võimalik.</span><span class="sxs-lookup"><span data-stu-id="451bb-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="451bb-105">Administraatorid saavad näha ja kasutada eelvaatefunktsioone oma keskkondades.</span><span class="sxs-lookup"><span data-stu-id="451bb-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="451bb-106">Need funktsioonid on peaaegu valmis üldiseks kasutamiseks ja on läbinud põhjalikud kontrollid.</span><span class="sxs-lookup"><span data-stu-id="451bb-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="451bb-107">Eelvaatefunktsioonide puhul soovime saada täiendavat kasutajate tagasidet ja kinnitust, enne kui funktsioonid üldiselt kättesaadavaks teeme.</span><span class="sxs-lookup"><span data-stu-id="451bb-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="451bb-108">Selles teemas kirjeldatakse, kuidas saate lubada eelvaatefunktsioone, ja loetletakse funktsioone, mis on praegu eelvaatena saadaval.</span><span class="sxs-lookup"><span data-stu-id="451bb-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="451bb-109">Loendit värskendatakse, kui funktsioonid tehakse üldiselt kättesaadavaks ja/või lisatakse uusi eelvaatefunktsioone.</span><span class="sxs-lookup"><span data-stu-id="451bb-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="451bb-110">Uute eelvaatefunktsioonide kohta ei saadeta teatisi.</span><span class="sxs-lookup"><span data-stu-id="451bb-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="451bb-111">Kasutajad märkavad lihtsalt uusi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="451bb-111">Users will just start to see the features.</span></span> <span data-ttu-id="451bb-112">Lisateavet Talenti uute funktsioonide kohta vt teemast [Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent](./whats-new.md) ja [Dynamics 365 ja Power Platformi väljalaskemärkmed](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="451bb-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="451bb-113">Eelvaatefunktsioonide lubamine või keelamine</span><span class="sxs-lookup"><span data-stu-id="451bb-113">Enable or disable preview features</span></span>

<span data-ttu-id="451bb-114">Eelvaatefunktsioonidele ligipääsemiseks peate kõigepealt need oma keskkonnas lubama.</span><span class="sxs-lookup"><span data-stu-id="451bb-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="451bb-115">Eelvaatefunktsioonide lubamine või keelamine sõltub keskkonnast.</span><span class="sxs-lookup"><span data-stu-id="451bb-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="451bb-116">Kui lülitate sisse sätte **Eelvaatefunktsioonid**, siis lubate eelvaatefunktsioonid kõikidele teie organisatsiooni kasutajatele, kes on selles keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="451bb-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="451bb-117">Kui lülitate sätte välja, siis keelate eelvaatefunktsioonid ja teie kasutajatel pole nendele juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="451bb-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="451bb-118">Rakenduses Talent on eelvaatefunktsioonidel piiratud tugi.</span><span class="sxs-lookup"><span data-stu-id="451bb-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="451bb-119">Need võivad kasutada vähem privaatsus- ja turbemeetmeid ning pole hõlmatud rakenduse Talent teenindustaseme lepingus (SLA).</span><span class="sxs-lookup"><span data-stu-id="451bb-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="451bb-120">Eelvaatefunktsioone ei tohi kasutada isikuandmete (st igasugused andmed, mis võimaldavad isikut tuvastada) ega muude andmete töötlemiseks, millele kehtivad seaduste või regulatsioonide järgmise nõuded.</span><span class="sxs-lookup"><span data-stu-id="451bb-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="451bb-121">Attract</span><span class="sxs-lookup"><span data-stu-id="451bb-121">Attract</span></span>

1. <span data-ttu-id="451bb-122">Rakenduse Microsoft Dynamics 365 Talent: Attract sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="451bb-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="451bb-123">Valige ülemises parempoolses nurgas olevast menüüst **Seadistus** (hammasratta sümbol) suvand **Halduskeskus**.</span><span class="sxs-lookup"><span data-stu-id="451bb-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="451bb-124">Valige vahekaardi **Funktsioonide haldus** suvandi **Eelvaatefunktsioonid** kõrval olev suvand nii, et see muutuks siniseks ja sellel oleks tähis **Sees**.</span><span class="sxs-lookup"><span data-stu-id="451bb-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Eelvaatefunktsioonide lubamine rakenduses Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="451bb-126">Valige üksikud eelvaatefunktsioonid või tühistage valik.</span><span class="sxs-lookup"><span data-stu-id="451bb-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="451bb-127">Kui te ei tee midagi, on kõik saadaolevad eelvaatefunktsioonid lubatud.</span><span class="sxs-lookup"><span data-stu-id="451bb-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="451bb-128">Uute funktsioonide nägemiseks värskendage oma brauserit.</span><span class="sxs-lookup"><span data-stu-id="451bb-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="451bb-129">Sisselogitud kasutajad näevad uusi funktsioone, kui nad logivad uuesti sisse, või nad võivad uute funktsioonide kohe nägemiseks oma brauserit värskendada.</span><span class="sxs-lookup"><span data-stu-id="451bb-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="451bb-130">Mõne funktsiooni jaoks võib vaja minna lisakonfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="451bb-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="451bb-131">Seadistamise lõpetamiseks järgige linke eelvaatefunktsiooni kõrval.</span><span class="sxs-lookup"><span data-stu-id="451bb-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="451bb-132">Tagasiside</span><span class="sxs-lookup"><span data-stu-id="451bb-132">Feedback</span></span>

<span data-ttu-id="451bb-133">Ootame teie tagasisidet teie kogemuse kohta nende eelvaatefunktsioonidega.</span><span class="sxs-lookup"><span data-stu-id="451bb-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="451bb-134">Soovitame teil postitada tagasisidet nende või muude funktsioonide kasutamise kohta järgmistel saitidel.</span><span class="sxs-lookup"><span data-stu-id="451bb-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="451bb-135">[Kogukonna foorum](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – sellel saidil on mitmeid ressursse ning kasutajad saavad arutada kasutusjuhtumeid, küsida küsimusi ja otsida kogukonnalt abi.</span><span class="sxs-lookup"><span data-stu-id="451bb-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="451bb-136">Andke meile teada funktsioonidest, mida soovite tootes näha, või andke teada muudatustest, mida teie arvates oleks olemasolevates funktsioonides vaja.</span><span class="sxs-lookup"><span data-stu-id="451bb-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="451bb-137">Tooteideid pakkuge järgmistel saitidel.</span><span class="sxs-lookup"><span data-stu-id="451bb-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="451bb-138">Attracti ideed</span><span class="sxs-lookup"><span data-stu-id="451bb-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="451bb-139">Onboardi ideed</span><span class="sxs-lookup"><span data-stu-id="451bb-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="451bb-140">Ärge kindlasti kasutage tagasisides ega tootearvustustes isikuandmeid (igasugused andmed, mis võimaldavad isikut tuvastada).</span><span class="sxs-lookup"><span data-stu-id="451bb-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="451bb-141">Kogutud teavet võidakse põhjalikumalt analüüsida ja seda ei kasutata kohalduvate isikuandmete kaitse seaduste järgi taotluste täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="451bb-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="451bb-142">Isikuandmetele, mida kogutakse eraldi nende programmidega, kehtib [Microsofti privaatsusavaldus](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="451bb-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="451bb-143">Lisage see teema järjehoidjatesse ja kontrollige seda tihti, et olla kursis uusimate eelvaatefunktsioonidega, kui neid väljastame.</span><span class="sxs-lookup"><span data-stu-id="451bb-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="451bb-144">Vt ka</span><span class="sxs-lookup"><span data-stu-id="451bb-144">See also</span></span>

- [<span data-ttu-id="451bb-145">Talenti rakenduste proovimine või ostmine</span><span class="sxs-lookup"><span data-stu-id="451bb-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="451bb-146">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent?</span><span class="sxs-lookup"><span data-stu-id="451bb-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="451bb-147">Väljalaskeplaanid</span><span class="sxs-lookup"><span data-stu-id="451bb-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="451bb-148">Toe hankimine rakendusele Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="451bb-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
