---
title: E-kaubanduse saidi loomine
description: See teema kirjeldab vajalikke etappe ja teavet uue e-kaubanduse saidi loomiseks Dynamics 365 Commerce'i saidiehitajas.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
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
ms.openlocfilehash: 7d552f29fd8f52b512a7c21b36b0a814cac50646
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517180"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="ce2c8-103">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce2c8-104">See teema kirjeldab vajalikke etappe ja teavet uue e-kaubanduse saidi loomiseks Dynamics 365 Commerce'i saidiehitajas.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="ce2c8-105">Kui litsentsite Dynamics 365 Commerce'i võimalusi, valmistatakse saidiehitaja ette koos alustussaidiga, mida saate kasutada oma saidi alusena.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="ce2c8-106">Kui aga soovite alustada nullist või luua teise saidi, tuleb teil luua uus sait saidi autorluse keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="ce2c8-107">Saidi seadistamine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-107">Set up your site</span></span>

<span data-ttu-id="ce2c8-108">Oma saidi seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="ce2c8-109">Avage saidiehitaja keskkond.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-109">Open the site builder environment.</span></span> <span data-ttu-id="ce2c8-110">Saidiehitaja lingi leiate Commerce'i keskkonna funktsioonide lehel Microsoft Lifecycle Services (LCS) alt.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="ce2c8-111">Valige saidi autorluse keskkonna avalehel suvand **Uus sait**.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="ce2c8-112">Sisestage dialoogiboksi **Uus sait** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="ce2c8-113">Väli</span><span class="sxs-lookup"><span data-stu-id="ce2c8-113">Field</span></span>                               | <span data-ttu-id="ce2c8-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ce2c8-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="ce2c8-115">Saidi nimi</span><span class="sxs-lookup"><span data-stu-id="ce2c8-115">Site name</span></span>                           | <span data-ttu-id="ce2c8-116">Sisestage kuvatav nimi, mida tuleks saidi autorluse keskkonnas teie saidi jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="ce2c8-117">See nimi on nähtav ainult autorluse keskkonnas ja seda ei kuvata klientidele.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="ce2c8-118">Saidi administraatori turberühm</span><span class="sxs-lookup"><span data-stu-id="ce2c8-118">Site administrator's security group</span></span> | <span data-ttu-id="ce2c8-119">Määrake Microsoft Azure Active Directory (Azure AD) turberühm, mis haldab kasutajaid, kellel on sellel saidil saidi administraatori roll.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="ce2c8-120">Vaikekanal (tootmisüksuse number)</span><span class="sxs-lookup"><span data-stu-id="ce2c8-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="ce2c8-121">Valige veebipood, mille jaoks see sait toimib fassaadina.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="ce2c8-122">Kui soovite, et teie e-kaubanduse sait toetaks mitut veebipoodi, peate pärast saidi seadistamist seostama poed oma saidiga jaotises **Saidi sätted** .</span><span class="sxs-lookup"><span data-stu-id="ce2c8-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="ce2c8-123">Vaikekeel</span><span class="sxs-lookup"><span data-stu-id="ce2c8-123">Default language</span></span>                            | <span data-ttu-id="ce2c8-124">Määrake selle veebipoe ja turu vaikekeel.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="ce2c8-125">Veebipood võib toetada mitut keelt.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-125">An online store can support multiple languages.</span></span> <span data-ttu-id="ce2c8-126">Kui soovite selle veebipoe või mõne muu veebipoe jaoks toetada mitut keelt, saate konfigureerida selle toe pärast saidi seadistamist suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="ce2c8-127">Domeen</span><span class="sxs-lookup"><span data-stu-id="ce2c8-127">Domain</span></span>                              | <span data-ttu-id="ce2c8-128">Valige domeeni nimi, mis toimib selle veebipoe jaoks domeenina.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="ce2c8-129">Kui te pole LCS-is ühtegi domeeni konfigureerinud, võite selle välja tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="ce2c8-130">Pärast domeeni LCS-is konfigureerimist peate lisama selle oma veebipoele suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="ce2c8-131">Tee</span><span class="sxs-lookup"><span data-stu-id="ce2c8-131">Path</span></span>                              | <span data-ttu-id="ce2c8-132">Kui teie sait toetab antud domeeninime puhul rohkem kui ühte keelt, kasutage tee välja, et luua selle domeeni ja keele kombinatsiooni jaoks kordumatu saidi URL.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="ce2c8-133">Kui keel, mille väljal **Vaikekeel** määrasite, on ainus selle domeeni jaoks toetatav keel või see on pärast saidi täiendavate keelte jaoks lokaliseerimist jätkuvalt vaikekeel, soovitame jätta selle välja tühjaks.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="ce2c8-134">Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="ce2c8-135">Saate kasutada ka lehe üleval vasakul ripploendit, et pääseda kategooriate põhjal eraldatud toodete juurde.</span><span class="sxs-lookup"><span data-stu-id="ce2c8-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce2c8-136">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ce2c8-136">Additional resources</span></span>

[<span data-ttu-id="ce2c8-137">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ce2c8-138">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ce2c8-139">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="ce2c8-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ce2c8-140">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ce2c8-141">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="ce2c8-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="ce2c8-142">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="ce2c8-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="ce2c8-143">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ce2c8-144">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="ce2c8-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ce2c8-145">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ce2c8-146">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="ce2c8-146">Enable location-based store detection</span></span>](enable-store-detection.md)
