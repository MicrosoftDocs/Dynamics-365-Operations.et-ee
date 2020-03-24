---
title: E-kaubanduse saidi loomine
description: See teema kirjeldab vajalikke etappe ja teavet uue e-kaubanduse saidi loomiseks Dynamics 365 Commerce'i saidiehitajas.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096770"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="a2f56-103">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="a2f56-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a2f56-104">See teema kirjeldab vajalikke etappe ja teavet uue e-kaubanduse saidi loomiseks Dynamics 365 Commerce'i saidiehitajas.</span><span class="sxs-lookup"><span data-stu-id="a2f56-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="a2f56-105">Enne oma e-kaubanduse saidi arendamise alustamiseks peate kõigepealt looma saidiehitajas uue saidi.</span><span class="sxs-lookup"><span data-stu-id="a2f56-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="a2f56-106">Oma e-kaubanduse saidi arendamise alustamiseks peate kõigepealt looma saidi autorluse keskkonnas uue saidi.</span><span class="sxs-lookup"><span data-stu-id="a2f56-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="a2f56-107">Enne uue saidi loomist peab olema rakenduses Commerce loodud vähemalt üks veebipood.</span><span class="sxs-lookup"><span data-stu-id="a2f56-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="a2f56-108">Saidi seadistamine</span><span class="sxs-lookup"><span data-stu-id="a2f56-108">Set up your site</span></span>

<span data-ttu-id="a2f56-109">Oma saidi seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a2f56-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="a2f56-110">Avage saidiehitaja keskkond.</span><span class="sxs-lookup"><span data-stu-id="a2f56-110">Open the site builder environment.</span></span> <span data-ttu-id="a2f56-111">Saidiehitaja lingi leiate Commerce'i keskkonna funktsioonide lehel Microsoft Lifecycle Services (LCS) alt.</span><span class="sxs-lookup"><span data-stu-id="a2f56-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="a2f56-112">Valige saidi autorluse keskkonna avalehel suvand **Uus sait**.</span><span class="sxs-lookup"><span data-stu-id="a2f56-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="a2f56-113">Sisestage dialoogiboksi **Uus sait** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="a2f56-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="a2f56-114">Väli</span><span class="sxs-lookup"><span data-stu-id="a2f56-114">Field</span></span>                               | <span data-ttu-id="a2f56-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a2f56-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="a2f56-116">Saidi nimi</span><span class="sxs-lookup"><span data-stu-id="a2f56-116">Site name</span></span>                           | <span data-ttu-id="a2f56-117">Sisestage kuvatav nimi, mida tuleks saidi autorluse keskkonnas teie saidi jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="a2f56-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="a2f56-118">See nimi on nähtav ainult autorluse keskkonnas ja seda ei kuvata klientidele.</span><span class="sxs-lookup"><span data-stu-id="a2f56-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="a2f56-119">Saidi administraatori turberühm</span><span class="sxs-lookup"><span data-stu-id="a2f56-119">Site administrator's security group</span></span> | <span data-ttu-id="a2f56-120">Määrake Microsoft Azure Active Directory (Azure AD) turberühm, mis haldab kasutajaid, kellel on sellel saidil saidi administraatori roll.</span><span class="sxs-lookup"><span data-stu-id="a2f56-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="a2f56-121">Vaikekanal (tootmisüksuse number)</span><span class="sxs-lookup"><span data-stu-id="a2f56-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="a2f56-122">Valige veebipood, mille jaoks see sait toimib fassaadina.</span><span class="sxs-lookup"><span data-stu-id="a2f56-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="a2f56-123">Kui soovite, et teie e-kaubanduse sait toetaks mitut veebipoodi, peate pärast saidi seadistamist seostama poed oma saidiga suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="a2f56-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="a2f56-124">Vaikekeel</span><span class="sxs-lookup"><span data-stu-id="a2f56-124">Default language</span></span>                            | <span data-ttu-id="a2f56-125">Määrake selle veebipoe ja turu vaikekeel.</span><span class="sxs-lookup"><span data-stu-id="a2f56-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="a2f56-126">Veebipood võib toetada mitut keelt.</span><span class="sxs-lookup"><span data-stu-id="a2f56-126">An online store can support multiple languages.</span></span> <span data-ttu-id="a2f56-127">Kui soovite selle veebipoe või mõne muu veebipoe jaoks toetada mitut keelt, saate konfigureerida selle toe pärast saidi seadistamist suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="a2f56-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="a2f56-128">Domeen</span><span class="sxs-lookup"><span data-stu-id="a2f56-128">Domain</span></span>                              | <span data-ttu-id="a2f56-129">Valige domeeni nimi, mis toimib selle veebipoe jaoks domeenina.</span><span class="sxs-lookup"><span data-stu-id="a2f56-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="a2f56-130">Kui te pole LCS-is ühtegi domeeni konfigureerinud, võite selle välja tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="a2f56-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="a2f56-131">Pärast domeeni LCS-is konfigureerimist peate lisama selle oma veebipoele suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="a2f56-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="a2f56-132">Tee</span><span class="sxs-lookup"><span data-stu-id="a2f56-132">Path</span></span>                              | <span data-ttu-id="a2f56-133">Kui teie sait toetab antud domeeninime puhul rohkem kui ühte keelt, kasutage tee välja, et luua selle domeeni ja keele kombinatsiooni jaoks kordumatu saidi URL.</span><span class="sxs-lookup"><span data-stu-id="a2f56-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="a2f56-134">Kui keel, mille väljal **Vaikekeel** määrasite, on ainus selle domeeni jaoks toetatav keel või see on pärast saidi täiendavate keelte jaoks lokaliseerimist jätkuvalt vaikekeel, soovitame jätta selle välja tühjaks.</span><span class="sxs-lookup"><span data-stu-id="a2f56-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="a2f56-135">Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut.</span><span class="sxs-lookup"><span data-stu-id="a2f56-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="a2f56-136">Saate kasutada ka lehe üleval vasakul ripploendit, et pääseda kategooriate põhjal eraldatud toodete juurde.</span><span class="sxs-lookup"><span data-stu-id="a2f56-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2f56-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a2f56-137">Additional resources</span></span>

[<span data-ttu-id="a2f56-138">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a2f56-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a2f56-139">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="a2f56-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a2f56-140">Võrgupoe kanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="a2f56-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="a2f56-141">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="a2f56-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a2f56-142">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="a2f56-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a2f56-143">URL-i hulgiümbersuunamiste üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="a2f56-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a2f56-144">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="a2f56-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a2f56-145">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="a2f56-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a2f56-146">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="a2f56-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a2f56-147">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="a2f56-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a2f56-148">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="a2f56-148">Enable location-based store detection</span></span>](enable-store-detection.md)
