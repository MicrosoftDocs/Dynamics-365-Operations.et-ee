---
title: E-kaubanduse saidi ülevaade
description: Selles teemas antakse ülevaade e-kaubanduse saitide toest rakenduses Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53bce671d6aca35335a3b3ef557a94fa60da1edc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251183"
---
# <a name="e-commerce-site-overview"></a><span data-ttu-id="7f950-103">E-kaubanduse saidi ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-103">E-commerce site overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f950-104">Selles teemas antakse ülevaade e-kaubanduse saitide toest rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f950-104">This topic provides an overview of the support for e-commerce sites in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="7f950-105">See sisaldab teavet selle kohta, kuidas e-kaubanduse võrgupoode lähtestatakse ja hallatakse rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7f950-105">It includes information about how e-commerce online stores are initialized and managed in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7f950-106">See sisaldab ka linke lisateabele võrgupoodide ja e-kaubanduse saidi häälestamise ja konfigureerimise kohta.</span><span class="sxs-lookup"><span data-stu-id="7f950-106">It also provides links to more information about online stores, and about how to set up and configure an e-commerce site.</span></span> <span data-ttu-id="7f950-107">Kuigi see teema hõlmab paljusid põhitõdesid, ei hõlma see kõike, mis on vajalik tootmise e-kaubanduse saidi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="7f950-107">Although this topic covers many of the basics, it doesn't cover everything that is required to set up a production e-commerce site.</span></span> <span data-ttu-id="7f950-108">Täpsemad teemad leiate Dynamics 365 Commerce'i dokumentatsioonist.</span><span class="sxs-lookup"><span data-stu-id="7f950-108">More advanced topics can be found in the Dynamics 365 Commerce documentation.</span></span>

## <a name="online-store-channel"></a><span data-ttu-id="7f950-109">Võrgupoe kanal</span><span class="sxs-lookup"><span data-stu-id="7f950-109">Online store channel</span></span>

<span data-ttu-id="7f950-110">Enne oma saidi loomist teenuses Dynamics 365 Commerce, peab olema häälestatud vähemalt üks võrgupoe kanal.</span><span class="sxs-lookup"><span data-stu-id="7f950-110">Before you can build your site in Dynamics 365 Commerce, at least one online store channel must be set up.</span></span> <span data-ttu-id="7f950-111">Lisateavet leiate teemast [Võrgukanali häälestamine](channel-setup-online.md).</span><span class="sxs-lookup"><span data-stu-id="7f950-111">For more information, see [Set up an online channel](channel-setup-online.md).</span></span> 

<span data-ttu-id="7f950-112">Teenuses Dynamics 365 Commerce kasutate võrgupoe kanalit toodete, hindade, keelte, makseviiside, tarneviiside, täitmise keskuste ja teiste võrgukogemuse aspektide loomiseks, mis peaksid olema klientidele kättesaadavad.</span><span class="sxs-lookup"><span data-stu-id="7f950-112">In Dynamics 365 Commerce, you use an online store channel to establish the products, pricing, languages, payment methods, delivery modes, fulfillment centers, and other aspects of the online experience that should be available to your customers.</span></span>

<span data-ttu-id="7f950-113">Enne teenuse Dynamics 365 Commerce kasutamise alustamist peab olema seadistatud ainult üks võrgupoe kanal.</span><span class="sxs-lookup"><span data-stu-id="7f950-113">Only one online store channel has to be set up before you can get started with Dynamics 365 Commerce.</span></span> <span data-ttu-id="7f950-114">Samas võib üks e-kaubanduse sait pakkuda mitme võrgupoe võrgukogemust.</span><span class="sxs-lookup"><span data-stu-id="7f950-114">However, a single e-commerce site can provide the online experience for multiple online stores.</span></span> <span data-ttu-id="7f950-115">Näiteks kui erinevate geograafiliste piirkondade toetamiseks on seadistatud mitu võrgupoodi, saab kasutada ühte e-kaubanduse lehtede komplekti, et pakkuda iga poe poolt määratletud ainulaadset kogemust.</span><span class="sxs-lookup"><span data-stu-id="7f950-115">For example, if multiple online stores are set up to support different geographical regions, a single set of e-commerce pages can be used to provide the unique experiences that are defined by each store.</span></span> <span data-ttu-id="7f950-116">Lisateavet selle kohta, kuidas konfigureerida saiti mitme e-poe toetamiseks, leiate teemast [Veebisaidi seostamine kanaliga](associate-site-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="7f950-116">For more information about how to configure a site to support multiple online stores, see [Associate an online site with a channel](associate-site-online-store.md).</span></span>

<span data-ttu-id="7f950-117">Pärast e-poe seadistamist saab selle seostada teenuse Dynamics 365 Commerce saidiga, mis esitatakse teie e-poe fassaadina.</span><span class="sxs-lookup"><span data-stu-id="7f950-117">After an online store is set up, it can be associated with the Dynamics 365 Commerce site that will serve as your online storefront.</span></span> <span data-ttu-id="7f950-118">Lisateavet e-poodide ja nende seadistamise kohta leiate teemast [E-poodide seadistamine](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).</span><span class="sxs-lookup"><span data-stu-id="7f950-118">For more information about online stores and how to set them up, see [Set up online stores](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).</span></span>

## <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="7f950-119">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="7f950-119">Deploy a new e-commerce tenant</span></span>

<span data-ttu-id="7f950-120">E-kaubanduse saidi lähtestamisel küsitakse teilt domeeninime.</span><span class="sxs-lookup"><span data-stu-id="7f950-120">During initialization of an e-commerce site, you're prompted for a domain name.</span></span> <span data-ttu-id="7f950-121">Lisateavet Domeenide kohta Commerce'is leiate teemast [Domeeninime](configure-your-domain-name.md) ja domeenide konfigureerimine [rakenduses Dynamics 365 Commerce](domains-commerce.md).</span><span class="sxs-lookup"><span data-stu-id="7f950-121">For more information about domains in Commerce, see [Configure your domain name](configure-your-domain-name.md) and [Domains in Dynamics 365 Commerce](domains-commerce.md).</span></span> <span data-ttu-id="7f950-122">Uue e-kaubanduse rentniku juurutamiseks [Microsoft Dynamics Lifecycle Servicesi (LCS-i) abil](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) järgige teemas [Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md) toodud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="7f950-122">To deploy a new e-commerce tenant by using [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), follow the steps in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="7f950-123">Pärast seda, kui teie e-kaubanduse rentnik on LCS-is häälestatud, antakse Commerce'i saidiehitaja link.</span><span class="sxs-lookup"><span data-stu-id="7f950-123">After your e-commerce tenant is set up in LCS, a link to Commerce site builder will be provided.</span></span> <span data-ttu-id="7f950-124">Seejärel saate kasutada Commerce'i saidiehitajat oma e-kaubanduse saitide lähtestamiseks ja konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="7f950-124">You can then use Commerce site builder to initialize and configure your e-commerce sites.</span></span>

## <a name="initialize-your-e-commerce-site"></a><span data-ttu-id="7f950-125">E-kaubanduse saidi lähtestamine</span><span class="sxs-lookup"><span data-stu-id="7f950-125">Initialize your e-commerce site</span></span>

<span data-ttu-id="7f950-126">Kui käivitate Commerce'i saidiehitaja LCS-i kaudu, kuvatakse leht **Saidid**.</span><span class="sxs-lookup"><span data-stu-id="7f950-126">When you start Commerce site builder from LCS, the **Sites** page appears.</span></span> <span data-ttu-id="7f950-127">Sellel lehel on kaks eelkonfigureeritud saiti, **Vaikimisi** ja **Fabrikam**, nagu on näidatud järgmisel joonisel toodud näites.</span><span class="sxs-lookup"><span data-stu-id="7f950-127">This page includes two preconfigured sites, **default** and **fabrikam**, as shown in the example in the following illustration.</span></span>

![Saitide leht Commerce'i saidiehitajas](media/e-commerce-site-01.png)

<span data-ttu-id="7f950-129">Kui valite ühe neist saitidest, palutakse teil valida domeeni nimi, võrgupoe vaikekanal, valitud kanali toetatud keel ja tee.</span><span class="sxs-lookup"><span data-stu-id="7f950-129">When you select one of these sites, you're prompted to select a domain name, a default online store channel, a supported language for the selected channel, and a path.</span></span> <span data-ttu-id="7f950-130">Kui kasutatakse ainult ühte kanalit, võite tee tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="7f950-130">If only one channel is used, you can leave the path blank.</span></span> <span data-ttu-id="7f950-131">Rohkem võrgupoe kanaleid või keeli saab hiljem konfigureerida Commerce'i saidiehitajas.</span><span class="sxs-lookup"><span data-stu-id="7f950-131">More online store channels or languages can be configured later in Commerce site builder.</span></span> <span data-ttu-id="7f950-132">Iga täiendav kanal või keel nõuab kordumatut teed.</span><span class="sxs-lookup"><span data-stu-id="7f950-132">Each additional channel or language will require a unique path.</span></span> <span data-ttu-id="7f950-133">Oletagem näiteks, et teil on kaks võrgukanalit, mis on seotud ühe saidiga ja saidi domeeninimi on `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="7f950-133">For example, you have two online channels that are associated with a single site, and the domain name for the site is `www.fabrikam.com`.</span></span> <span data-ttu-id="7f950-134">Sel juhul võib ühe kanali tee olla vaikeväärtus, millel puudub tee (`https://www.fabrikam.com`) ja teise kanali saab määrata uuele teele, näiteks **Sait2**, mille URL on `https://www.fabrikam.com/site2`.</span><span class="sxs-lookup"><span data-stu-id="7f950-134">In this case, the path for one channel can be the default value that has no path (`https://www.fabrikam.com`), and the second channel can be set to a new path, such as **site2**, that will have the URL `https://www.fabrikam.com/site2`.</span></span> <span data-ttu-id="7f950-135">Järgmisel joonisel on näide saidi lähtestamise dialoogiboksist Commerce'i saidikoosturis.</span><span class="sxs-lookup"><span data-stu-id="7f950-135">The following illustration shows an example of a site initialization dialog box in Commerce site builder.</span></span>

![Saidi lähtestamise dialoogiboks Commerce'i saidikoosturis](media/e-commerce-site-02.png)

<span data-ttu-id="7f950-137">Lehel **Saidid** on ka nupp **Uus sait**.</span><span class="sxs-lookup"><span data-stu-id="7f950-137">The **Sites** page also includes a **New site** button.</span></span> <span data-ttu-id="7f950-138">Selle nupu valimisel kuvatav dialoogiboks sarnaneb saidi lähtestamise dialoogiboksiga, kuid seda kasutatakse uue saidi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="7f950-138">The dialog box that appears when you select this button resembles the site initialization dialog box, but it's used to create a new site.</span></span> <span data-ttu-id="7f950-139">Uued saidid on tühjad.</span><span class="sxs-lookup"><span data-stu-id="7f950-139">New sites are blank.</span></span> <span data-ttu-id="7f950-140">Need ei sisalda samu vaikemalle, fragmente, lehti ega pilte, mis on saidil **Vaikimisi** ja **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="7f950-140">They don't include the same default templates, fragments, pages, and images that are provided with the **default** and **fabrikam** sites.</span></span> <span data-ttu-id="7f950-141">Kuid vastavalt vajadusele saate avada tugiteenusepileti, et taotleda vaikesisu koopia lisamist uuele tühjale saidile.</span><span class="sxs-lookup"><span data-stu-id="7f950-141">However, as you require, you can open a support ticket to request that a copy of the default content be added to a new blank site.</span></span> <span data-ttu-id="7f950-142">Lisateavet leiate teemast [E-kaubanduse saidi loomine](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="7f950-142">For more information, see [Create an e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="7f950-143">Pärast uue saidi lähtestamist kuvatakse Commerce'i saidikoosturi leht **Avaleht**.</span><span class="sxs-lookup"><span data-stu-id="7f950-143">After a new site is initialized, the Commerce site builder **Home** page appears.</span></span> <span data-ttu-id="7f950-144">See leht sisaldab linke levinud toimingutele ja juhendsisule, nagu on näidatud järgmisel joonisel toodud näitel.</span><span class="sxs-lookup"><span data-stu-id="7f950-144">This page includes links to common actions and guidance content, as shown in the example in the following illustration.</span></span>

![Lingid Commerce'i saidiehitaja avalehel](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a><span data-ttu-id="7f950-146">Võrgupoe kanalite muutmine või võrgupoe kanalite lisamine e-kaubanduse saidile</span><span class="sxs-lookup"><span data-stu-id="7f950-146">Modify online store channels or add online store channels to an e-commerce site</span></span>

<span data-ttu-id="7f950-147">Pärast e-kaubanduse saidi loomist saate sellega seostatud kanalit muuta, järgides teemas [E-kaubanduse saidi seostamine võrgukanaliga](associate-site-online-store.md) toodud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="7f950-147">After an e-commerce site is created, you can change the channel that it's associated with by following the steps in [Associate an e-commerce site with an online channel](associate-site-online-store.md).</span></span> <span data-ttu-id="7f950-148">Järgmisel joonisel toodud näide näitab, kuidas kanali tootmisüksuse numbrit (OUN-i) saab muuta lehel **Kanalid** (**Saidi sätted \> Kanalid**).</span><span class="sxs-lookup"><span data-stu-id="7f950-148">The example in the following illustration shows how a channel operating unit number (OUN) can be changed on the **Channels** page (**Site settings \> Channels**).</span></span> <span data-ttu-id="7f950-149">Kui olete muudatuse tegemise lõpetanud, valige kindlasti nupp **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="7f950-149">After you've finished making a change, be sure to select **Save and publish**.</span></span> <span data-ttu-id="7f950-150">Sel viisil tagate muudatuse avaldamise.</span><span class="sxs-lookup"><span data-stu-id="7f950-150">In this way, you ensure that the change is published.</span></span>

![Kanalite leht Commerce'i saidiehitajas](media/e-commerce-site-04.png)

<span data-ttu-id="7f950-152">Uute kanalite lisamiseks valige nupp **Lisa kanal**.</span><span class="sxs-lookup"><span data-stu-id="7f950-152">You can add new channels by selecting **Add a channel**.</span></span> <span data-ttu-id="7f950-153">Kanalile uute keelte lisamiseks valige kanal ja seejärel valige kuvatavas kanalidialoogiboksis käsk **Lisa lokaat**.</span><span class="sxs-lookup"><span data-stu-id="7f950-153">To add new languages to a channel, select the channel, and then select **Add a locale** in the channel dialog box that appears.</span></span> <span data-ttu-id="7f950-154">Enne, kui lokaate dialoogiboksis kuvada saab, peavad need olema Commerce'i peakontori võrgupoe kanali jaoks eelkonfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="7f950-154">Before locales can appear in the dialog box, they must be preconfigured for the online store channel in Commerce headquarters.</span></span>

![Kanali dialoogiboks Commerce'i saidiehitajas](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a><span data-ttu-id="7f950-156">Azure B2C rentniku häälestamine</span><span class="sxs-lookup"><span data-stu-id="7f950-156">Set up an Azure B2C tenant</span></span>

<span data-ttu-id="7f950-157">Dynamics 365 Commerce kasutab teenust Azure Active Directory (Azure AD) ettevõtja ja tarbija (B2C) vahelist teavet kasutaja mandaadi ja autentimise voogude toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="7f950-157">Dynamics 365 Commerce uses Azure Active Directory (Azure AD) business-to-consumer (B2C) to support user credential and authentication flows.</span></span> <span data-ttu-id="7f950-158">Lisateavet Azure B2C rentniku häälestamise kohta leiate teemast [B2C rentniku häälestamine Commerce'is](set-up-b2c-tenant.md), [Kohandatud lehtede häälestus kasutajate sisselogimise jaoks](custom-pages-user-logins.md) ja [Mitme jaekaubandusrentniku konfigureerimine Commerce'i keskkonnas](configure-multi-b2c-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="7f950-158">For information about how to set up your Azure B2C tenant, see [Set up a B2C tenant in Commerce](set-up-b2c-tenant.md), [Set up custom pages for user sign-ins](custom-pages-user-logins.md), and [Configure multiple B2C tenants in a Commerce environment](configure-multi-b2c-tenants.md).</span></span>

## <a name="overview-of-the-default-site-pages"></a><span data-ttu-id="7f950-159">Saidi vaikelehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-159">Overview of the default site pages</span></span>

<span data-ttu-id="7f950-160">Saidil **Vaikimisi** ja **Fabrikam** on eelkonfigureeritud mallid, fragmendid ja lehed, mis aitavad teil alustada.</span><span class="sxs-lookup"><span data-stu-id="7f950-160">The **default** and **fabrikam** sites include preconfigured templates, fragments, and pages to help you get started.</span></span> <span data-ttu-id="7f950-161">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="7f950-161">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7f950-162">Avalehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-162">Home page overview</span></span>](quick-tour-home-page.md)
- [<span data-ttu-id="7f950-163">Toote üksikasjade lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-163">Product details page overview</span></span>](quick-tour-pdp.md)
- [<span data-ttu-id="7f950-164">Ostukorvi ja väljaregistreerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-164">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)
- [<span data-ttu-id="7f950-165">Kontohalduse lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-165">Account management pages overview</span></span>](quick-tour-account-management.md)

## <a name="manage-site-settings"></a><span data-ttu-id="7f950-166">Saidisätete haldamine</span><span class="sxs-lookup"><span data-stu-id="7f950-166">Manage site settings</span></span>

<span data-ttu-id="7f950-167">Saidi sätete haldamise kohta lisateabe saamiseks vaadake järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="7f950-167">For information about how to manage your site settings, see the following topics:</span></span>

- [<span data-ttu-id="7f950-168">E-kaubanduse kasutajate ja rollide haldamine</span><span class="sxs-lookup"><span data-stu-id="7f950-168">Manage e-commerce users and roles</span></span>](manage-ecommerce-users-roles.md)
- [<span data-ttu-id="7f950-169">Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused</span><span class="sxs-lookup"><span data-stu-id="7f950-169">Search engine optimization (SEO) considerations for your site</span></span>](/search-engine-optimization-considerations.md)
- [<span data-ttu-id="7f950-170">Sisu turbepoliitika (CSP) haldamine</span><span class="sxs-lookup"><span data-stu-id="7f950-170">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
- [<span data-ttu-id="7f950-171">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="7f950-171">Select a site theme</span></span>](select-site-theme.md)

## <a name="manage-site-content"></a><span data-ttu-id="7f950-172">Saidi sisu haldamine</span><span class="sxs-lookup"><span data-stu-id="7f950-172">Manage site content</span></span>

<span data-ttu-id="7f950-173">Saidi sisu haldamise kohta lisateabe saamiseks vaadake järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="7f950-173">For information about how to manage site content, see the following topics:</span></span>

- [<span data-ttu-id="7f950-174">Lehemudeli sõnastik</span><span class="sxs-lookup"><span data-stu-id="7f950-174">Page model glossary</span></span>](page-elements-overview.md)
- [<span data-ttu-id="7f950-175">Dokumendi olekud ja töötsükkel</span><span class="sxs-lookup"><span data-stu-id="7f950-175">Document states and lifecycle</span></span>](document-states-overview.md)
- [<span data-ttu-id="7f950-176">Mallid ja paigutus</span><span class="sxs-lookup"><span data-stu-id="7f950-176">Templates and layout</span></span>](templates-layouts-overview.md)
- [<span data-ttu-id="7f950-177">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="7f950-177">Work with fragments</span></span>](work-with-fragments.md)
- [<span data-ttu-id="7f950-178">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="7f950-178">Work with modules</span></span>](work-with-modules.md)
- [<span data-ttu-id="7f950-179">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-179">Digital asset management overview</span></span>](dam-overview.md)
- [<span data-ttu-id="7f950-180">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="7f950-180">Module library overview</span></span>](starter-kit-overview.md)

## <a name="additional-resources"></a><span data-ttu-id="7f950-181">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7f950-181">Additional resources</span></span>

[<span data-ttu-id="7f950-182">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="7f950-182">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7f950-183">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="7f950-183">Deploy a new e-commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7f950-184">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="7f950-184">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7f950-185">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7f950-185">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7f950-186">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="7f950-186">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7f950-187">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="7f950-187">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="7f950-188">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="7f950-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]