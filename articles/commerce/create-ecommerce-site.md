---
title: E-kaubanduse saidi loomine
description: Selles teemas kirjeldatakse ülesandeid, mis on seotud uue e-kaubanduse saidi loomisega rakenduses Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945831"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="3c5f5-103">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3c5f5-104">Selles teemas kirjeldatakse ülesandeid, mis on seotud uue e-kaubanduse saidi loomisega rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3c5f5-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3c5f5-105">Overview</span></span>

<span data-ttu-id="3c5f5-106">Oma e-kaubanduse saidi arendamise alustamiseks peate kõigepealt looma saidi autorluse keskkonnas uue saidi.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="3c5f5-107">Enne uue saidi loomist peab olema rakenduses Dynamics 365 Retail loodud vähemalt üks veebipood.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="3c5f5-108">Saidi seadistamine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-108">Set up your site</span></span>

<span data-ttu-id="3c5f5-109">Oma saidi seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="3c5f5-110">Valige Microsofti teenuse Lifecycle Services (LCS) saidi autorluse keskkonna link.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="3c5f5-111">Valige saidi autorluse keskkonna avalehel suvand **Uus sait**.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="3c5f5-112">Sisestage dialoogiboksi **Uus sait** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="3c5f5-113">Väli</span><span class="sxs-lookup"><span data-stu-id="3c5f5-113">Field</span></span>                               | <span data-ttu-id="3c5f5-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3c5f5-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="3c5f5-115">Saidi nimi</span><span class="sxs-lookup"><span data-stu-id="3c5f5-115">Site name</span></span>                           | <span data-ttu-id="3c5f5-116">Sisestage kuvatav nimi, mida tuleks saidi autorluse keskkonnas teie saidi jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="3c5f5-117">See nimi on nähtav ainult autorluse keskkonnas ja seda ei kuvata klientidele.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="3c5f5-118">Saidi administraatori turberühm</span><span class="sxs-lookup"><span data-stu-id="3c5f5-118">Site administrator's security group</span></span> | <span data-ttu-id="3c5f5-119">Määrake Microsoft Azure Active Directory (Azure AD) turberühm, mis haldab kasutajaid, kellel on sellel saidil saidi administraatori roll.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="3c5f5-120">Vaikekanal (tootmisüksuse number)</span><span class="sxs-lookup"><span data-stu-id="3c5f5-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="3c5f5-121">Valige veebipood, mille jaoks see sait toimib fassaadina.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="3c5f5-122">Kui soovite, et teie e-kaubanduse sait toetaks mitut veebipoodi, peate pärast saidi seadistamist seostama poed oma saidiga suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="3c5f5-123">Vaikekeel</span><span class="sxs-lookup"><span data-stu-id="3c5f5-123">Default language</span></span>                            | <span data-ttu-id="3c5f5-124">Määrake selle veebipoe ja turu vaikekeel.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="3c5f5-125">Veebipood võib toetada mitut keelt.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-125">An online store can support multiple languages.</span></span> <span data-ttu-id="3c5f5-126">Kui soovite selle veebipoe või mõne muu veebipoe jaoks toetada mitut keelt, saate konfigureerida selle toe pärast saidi seadistamist suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="3c5f5-127">Domeen</span><span class="sxs-lookup"><span data-stu-id="3c5f5-127">Domain</span></span>                              | <span data-ttu-id="3c5f5-128">Valige domeeni nimi, mis toimib selle veebipoe jaoks domeenina.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="3c5f5-129">Kui te pole LCS-is ühtegi domeeni konfigureerinud, võite selle välja tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="3c5f5-130">Pärast domeeni LCS-is konfigureerimist peate lisama selle oma veebipoele suvandis **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="3c5f5-131">Tee</span><span class="sxs-lookup"><span data-stu-id="3c5f5-131">Path</span></span>                              | <span data-ttu-id="3c5f5-132">Kui teie sait toetab antud domeeninime puhul rohkem kui ühte keelt, kasutage tee välja, et luua selle domeeni ja keele kombinatsiooni jaoks kordumatu saidi URL.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="3c5f5-133">Kui keel, mille väljal **Vaikekeel** määrasite, on ainus selle domeeni jaoks toetatav keel või see on pärast saidi täiendavate keelte jaoks lokaliseerimist jätkuvalt vaikekeel, soovitame jätta selle välja tühjaks.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="3c5f5-134">Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="3c5f5-135">Saate kasutada ka lehe üleval vasakul ripploendit, et pääseda kategooriate põhjal eraldatud toodete juurde.</span><span class="sxs-lookup"><span data-stu-id="3c5f5-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c5f5-136">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3c5f5-136">Additional resources</span></span>

[<span data-ttu-id="3c5f5-137">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3c5f5-138">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3c5f5-139">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="3c5f5-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3c5f5-140">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3c5f5-141">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3c5f5-142">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3c5f5-143">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="3c5f5-143">Enable location-based store detection</span></span>](enable-store-detection.md)
