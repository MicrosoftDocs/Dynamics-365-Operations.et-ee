---
title: Domeenid teenuses Dynamics 365 Commerce
description: Selles teemas kirjeldatakse, kuidas käsitsetakse domeene teenuses Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: d855f2164e4ee0f0cdb220787eb96217523137e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010243"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="4bf0c-103">Domeenid teenuses Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4bf0c-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4bf0c-104">Selles teemas kirjeldatakse, kuidas käsitsetakse domeene teenuses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4bf0c-105">Domeenid on veebiaadressid, mida kasutatakse veebibrauseris teenuse Dynamics 365 Commerce saitidele navigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="4bf0c-106">Saate juhtida oma domeeni haldamist valitud domeeni nimeserveri (DNS) pakkuja abil.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="4bf0c-107">Domeenidele viidatakse teenuse Dynamics 365 Commerce saidiehitajas, et koordineerida seda, kuidas saidile pärast avaldamist juurde pääseb.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="4bf0c-108">Selles teemas antakse ülevaade sellest, kuidas domeene käsitletakse ja viidatakse kogu kaubanduse saidi arendamise ja käivitamise töötsükli jooksul.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="4bf0c-109">Hostinimede ettevalmistamine ja toetamine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-109">Provisioning and supported host names</span></span>

<span data-ttu-id="4bf0c-110">E-kaubanduse keskkonna ettevalmistamisel teenuses [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) kasutatakse juurutatud Commerce'i keskkonnaga seotud domeenide sisestamiseks e-kaubanduse ettevalmistamise kuval välja **Toetatud hostinimed**.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="4bf0c-111">Need domeenid on kliendile suunatud domeeninimede serveri (DNS) nimed, kus majutatakse e-kaubanduse veebisaite.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="4bf0c-112">Domeeni sisestamine selles etapis ei hakka domeeni liiklust teenusesse Dynamics 365 Commerce suunama.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="4bf0c-113">Domeeni liiklus marsruuditakse Commerce'i lõpp-punkti alles siis, kui DNS-i kirjet CNAME värskendatakse Commerce'i lõpp-punkti kasutamiseks domeeniga.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="4bf0c-114">Väljale **Toetatud hostinimed** saab sisestada mitu domeeni, eraldades need semikoolonitega.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="4bf0c-115">Järgmisel joonisel on kujutatud LCS-i e-kaubanduse ettevalmistamise ekraan, kus on esile tõstetud väli **Toetatud hostinimed**.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![LCS-i e-kaubanduse ettevalmistamise ekraan koos esiletõstetud väljaga **Toetatud hostinimed**](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="4bf0c-117">Kui ettevalmistamine on juba toimunud, saate luua hooldustaotluse lisadomeenide keskkonda lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="4bf0c-118">Teenusetaotluse loomiseks LCS-is tehke oma keskkonnas valikud **Tugi \> Toeprobleemid** ja valige **Edasta juhtum**.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="4bf0c-119">Commerce'i loodud URL-id</span><span class="sxs-lookup"><span data-stu-id="4bf0c-119">Commerce-generated URLs</span></span>

<span data-ttu-id="4bf0c-120">Dynamics 365 Commerce'i e-kaubanduse keskkonna ettevalmistamisel loob Commerce URL-i, mis on keskkonna tööaadress.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="4bf0c-121">Sellele URL-ile viidatakse LCS-is kuvatavas e-kaubanduse saidi lingis pärast keskkonna ettevalmistamist.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="4bf0c-122">Commerce'i loodud URL on vormingus `https://<e-commerce tenant name>.commerce.dynamics.com`, mille korral e-kaubanduse rentniku nimi on LCS-is Commerce'i keskkonna jaoks sisestatud nimi.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="4bf0c-123">Tootmissaidi hostinimesid saate kasutada ka liivakastikeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="4bf0c-124">See suvand on ideaalne kasutamiseks siis, kui kopeerite saidi liivakastikeskkonnast tootmisse.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="4bf0c-125">Saidi häälestus</span><span class="sxs-lookup"><span data-stu-id="4bf0c-125">Site setup</span></span>

<span data-ttu-id="4bf0c-126">Kui teie e-kaubanduse keskkond on ette valmistatud, peate seadistama oma saidi Commerce'i saidiehitajas saidi ja toimiva URL-i seostamiseks.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="4bf0c-127">Saidi esmakordsel seadistamisel saidiehitajas kuvatakse dialoogiboks **Saidi seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="4bf0c-128">Järgmisel illustratsioonil on kujutatud dialoogiboks **Saidi seadistamine** saidi „vaikimisi” jaoks, kui navigeerite saidile esmakordselt saidiehitaja kaudu.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![Dialoogiboks **Saidi seadistamine**](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="4bf0c-130">Väli **Vali domeen** võimaldab teil saidiehitajas seostada oma saidiga ühe toetatud hostinimedest, mida pakutakse teie saidi jaoks LCS-is.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="4bf0c-131">Välja **Tee** saab tühjaks jätta või lisada täiendava tee stringi, mis kajastub teie toimivas URL-is.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="4bf0c-132">Kui väli **Tee** on tühi, seostatakse saidiehitajas Commerce'i loodud URL seadistatava saidiga.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="4bf0c-133">Teed peavad olema kordumatud iga saidi/domeeni paari korral.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="4bf0c-134">Valitud saidil ja domeenis saab tühja teed kasutada ainult üks keskkonna sait või olla seostatud kordumatu tee stringiga.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="4bf0c-135">Saidi seadistamise ajal väljale **Tee** lisatud stringist saab Commerce'i loodud baas-URL-i alamtee, mida kasutatakse veebibrauseris saidile juurdepääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4bf0c-136">Tee on tuntud ka kui **Vastendatud tee**, kui lisada kanal saidiehitaja konfiguratsioonisektsiooni **Saidi sätted \> Kanalid**.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="4bf0c-137">Näiteks kui teil on saidiehitaja sait „fabrikam“ e-kaubanduse rentnikus nimega „xyz“ ja kui seadistate saidi tühja teega, pääsete veebibrauseris juurde avaldatud saidi sisule, avades otse Commerce'i loodud baas-URL-i.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="4bf0c-138">Kui olete sama saidi seadistamise ajal lisanud tee nimega „fabrikam”, pääsete veebibrauseri avaldatud saidi sisule juurde järgmise URL-i abil.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="4bf0c-139">Lehed ja URL-id</span><span class="sxs-lookup"><span data-stu-id="4bf0c-139">Pages and URLs</span></span>

<span data-ttu-id="4bf0c-140">Pärast seda, kui teie sait on seadistatud teega, tuginevad kõik saidiehitaja lehtedega seotud URL-id saidi toimivale URL-ile (Commerce'i loodud URL või Commerce'i loodud URL koos teega).</span><span class="sxs-lookup"><span data-stu-id="4bf0c-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="4bf0c-141">Uue URL-i loomine saidiehitajas (**URL-id /> +Uus**), valides lehe dialoogiboksi **Uus URL** loendist ja sisestades selle lehe URL-i tee, seostab selle URL-i valitud lehega.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="4bf0c-142">URL-i tee väärtus lisatakse saidi toimivale URL-ile lehele juurde pääsemiseks ja sel on silt `./<URL path>` saidiehitaja lehe **URL-id** URL-ide loendis.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="4bf0c-143">Järgmisel joonisel on kujutatud saidiehitaja dialoogiboks **Uus URL**, milles on esile tõstetud näidis-URL-i tee.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![Saidiehitaja dialoogiboks **Uus URL**](./media/Domains_PageSetup2a.png)

<span data-ttu-id="4bf0c-145">Järgmisel joonisel on kujutatud saidiehitaja leht **URL-id**, mille loendis on esile tõstetud URL.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![Kasutajavoo suvandi käitamine poliitika voos](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="4bf0c-147">Saidiehitaja domeenid</span><span class="sxs-lookup"><span data-stu-id="4bf0c-147">Domains in site builder</span></span>

<span data-ttu-id="4bf0c-148">Toetatud hostinime väärtused on saadaval, et neid saaks saidi seadistamisel domeeniga seostada.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="4bf0c-149">Toetatud hostinime väärtuse domeenina valimisel näete valitud domeeni, millele viidatakse saidiehitajas.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="4bf0c-150">See domeen on vaid viide Commerce'i keskkonnas ning selle domeeni reaalajas liiklust ei edastata veel teenusele Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4bf0c-151">Kui töötate saidiehitaja saitidega ja teil on seadistatud kaks saiti kahe erineva domeeniga, saate lisada oma toimivale URL-ile atribuudi **?domain=**, et pääseda brauseris juurde avaldatud saidi sisule.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="4bf0c-152">Näiteks keskkond „xyz” on ette valmistatud ning saidiehitajas on loodud ja seostatud kaks saiti: üks domeeniga `www.fabrikam.com` ja teine domeeniga `www.constoso.com`.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="4bf0c-153">Iga sait seadistati tühja tee abil.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="4bf0c-154">Nendele kahele saidile pääseb veebibrauseri kaudu juurde järgmiselt, kasutades atribuuti **?domain=**.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="4bf0c-155">Kui domeeni päringustringi ei pakuta keskkonnas, kus on mitu domeeni, kasutab Commerce esimest teie pakutavat domeeni.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="4bf0c-156">Näiteks kui saidi seadistamisel esitati esmalt tee „fabrikam”, võidakse kasutada URL-i `https://xyz.commerce.dynamics.com`, et pääseda juurde saidi `www.fabrikam.com` avaldatud sisule.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="4bf0c-157">Liikluse edastamine tootmisse</span><span class="sxs-lookup"><span data-stu-id="4bf0c-157">Traffic forwarding in production</span></span>

<span data-ttu-id="4bf0c-158">Mitme domeeni simuleerimiseks saate kasutada domeeni päringustringi parameetreid saidi commerce.dynamics.com lõpp-punktis.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="4bf0c-159">Kuid kui teil on vaja avaldada otse tootmisse, peate oma kohandatud domeeni liikluse edastama saidi `<e-commerce tenant name>.commerce.dynamics.com` lõpp-punkti.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="4bf0c-160">Saidi `<e-commerce tenant name>.commerce.dynamics.com` lõpp-punkt ei toeta kohandatud domeeni SSL-e, seega peate häälestama kohandatud domeenid, kasutades sisenemispunkti teenust või sisu edastamise võrku (CDN).</span><span class="sxs-lookup"><span data-stu-id="4bf0c-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="4bf0c-161">Kohandatud domeenide seadistamiseks sisenemispunkti teenuse või CDN-i abil on teil kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="4bf0c-162">Saate seadistada sisenemispunkti teenuse (nt Azure Front Door) eesserveri liikluse käsitlemiseks ja oma Commerce'i keskkonnaga ühenduse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="4bf0c-163">See tagab suurema kontrolli domeeni- ja serdihalduse ning täpsemate turbepoliitikate üle.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="4bf0c-164">Saate kasutada Commerce'i esitatud Azure'i sisenemispunkti eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="4bf0c-165">Selleks on vaja koordineerida tegevust teenuse Dynamics 365 Commerce töörühmaga domeeni kinnitamiseks ja teie tootmise domeeni SSL-i sertide hankimiseks.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="4bf0c-166">Lisateavet CDN-i teenuse otseseadistamise kohta leiate teemast [Sisu edastamise võrgu (CDN) toe lisamine](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="4bf0c-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="4bf0c-167">Commerce'i esitatud Azure'i sisenemispunkti eksemplari kasutamiseks peate looma CDN-i seadistusabi teenusetaotluse Commerce'i töörühma abil.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="4bf0c-168">Peate sisestama ettevõtte nime, tootmise domeeni, keskkonna ID ja tootmise e-kaubanduse rentniku nime.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="4bf0c-169">Peate kinnitama, kas tegemist on olemasoleva domeeniga (mida kasutatakse praegu aktiivse saidi jaoks) või uue domeeniga.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="4bf0c-170">Uue domeeni korral saab kinnitada domeeni ja hankida SSL-serdi ühe etapi abil.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="4bf0c-171">Olemasolevat veebisaiti teenindava domeeni korral on domeeni kinnitamise ja SSL-serdi loomiseks nõutav mitmeetapiline protsess.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="4bf0c-172">Sellel protsessil on seitsme tööpäeva teenusetaseme lepe (SLA) domeeni avaldamiseks, kuna see sisaldab mitut järjestikust etappi.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="4bf0c-173">Teenusetaotluse loomiseks LCS-is tehke oma keskkonnas valikud **Tugi \> Toeprobleemid** ja valige **Edasta juhtum**.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="4bf0c-174">SSL-iga kohandatud domeene toetatakse ainult töökeskkondades.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="4bf0c-175">Mitte-töökeskkondade (nt liivakasti ja kasutaja nõusoleku testimise (UAT)) korral kasutage avaldatud sisule veebibrauseri kaudu juurdepääsemiseks Commerce'i loodud URL-i.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="4bf0c-176">SSL-serdi protsess</span><span class="sxs-lookup"><span data-stu-id="4bf0c-176">SSL certificate process</span></span>

<span data-ttu-id="4bf0c-177">Kui teenusetaotlus on esitatud, kooskõlastab Commerce'i töörühm teiega järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="4bf0c-178">Uute domeenide korral.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-178">For new domains:</span></span>
- <span data-ttu-id="4bf0c-179">Commerce'i töörühm seadistab Azure'i sisenemispunkti teenuse eksemplari (Commerce'i hostitud).</span><span class="sxs-lookup"><span data-stu-id="4bf0c-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="4bf0c-180">Seejärel esitab Commerce'i töörühm kirje CNAME, et osutada teie kohandatud domeenile.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="4bf0c-181">Pärast kirje CNAME värskendamist saab Commerce'i hostitud Azure'i sisenemispunkti eksemplar kinnitada domeeni omandiõigust ja hankida SSL-serti.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="4bf0c-182">Olemasolevate/aktiivsete domeenide korral.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-182">For existing/active domains:</span></span>
- <span data-ttu-id="4bf0c-183">Commerce'i töörühm palub teil lisada kirje `afdverify.<custom-domain>` CNAME oma domeeni pakkumiseks DNS-i pakkujale.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="4bf0c-184">Kui see on lõpule viidud, lisab Commerce'i töörühm domeeni Azure'i sisenemispunkti eksemplari ja pakub täiendavaid DNS-i TXT-kirjeid, mis lisatakse domeeni DNS-i.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="4bf0c-185">Pärast TXT-kirjete lõpule viimist viib Commerce'i töörühm lõpule SSL-serti häälestava domeeni Azure'i sisenemispunkti värskendused.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="4bf0c-186">Tippdomeenid</span><span class="sxs-lookup"><span data-stu-id="4bf0c-186">Apex domains</span></span>

<span data-ttu-id="4bf0c-187">Commerce'i esitatud Azure'i sisenemispunkti eksemplar ei toeta tippdomeene (juurdomeene, mis ei sisalda alamdomeene).</span><span class="sxs-lookup"><span data-stu-id="4bf0c-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="4bf0c-188">Tippdomeenid vajavad probleemi lahendamiseks IP-aadressi ja Commerce'i Azure'i sisenemispunkti eksemplar on olemas ainult koos virtuaalsete lõpp-punktidega.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="4bf0c-189">Tippdomeeni kasutamiseks on teil kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="4bf0c-190">**Võimalus 1** – Saate kasutada oma DNS-i pakkujat, et suunata tippdomeen ümber "www"-domeeni.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="4bf0c-191">Näiteks suunab fabrikam.com ümber saidile `www.fabrikam.com`, kus `www.fabrikam.com` on kirje CNAME, mis osutab Commerce'i hostitud Azure'i sisenemispunkti eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="4bf0c-192">**Võimalus 2** – tippdomeeni majutamiseks saate ise seadistada CDN-i/sisenemispunkti eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="4bf0c-193">Kui kasutate Azure'i sisenemispunkti, peate samas tellimuses seadistama ka Azure'i DNS-i.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="4bf0c-194">Azure'i DNS-is majutatud tippdomeen võib osutada teie Azure'i sisenemispunktile pseudonüümi kirjena.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="4bf0c-195">See on ainus võimalus, sest tippdomeenid peavad alati osutama IP-aadressile.</span><span class="sxs-lookup"><span data-stu-id="4bf0c-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="4bf0c-196">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4bf0c-196">Additional resources</span></span>

  [<span data-ttu-id="4bf0c-197">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="4bf0c-198">Võrgupoe kanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="4bf0c-199">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="4bf0c-200">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="4bf0c-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="4bf0c-201">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="4bf0c-202">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="4bf0c-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="4bf0c-203">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="4bf0c-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="4bf0c-204">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="4bf0c-205">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="4bf0c-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="4bf0c-206">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="4bf0c-207">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="4bf0c-207">Enable location-based store detection</span></span>](enable-store-detection.md)
