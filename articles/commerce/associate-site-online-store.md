---
title: Dynamics 365 Commerce'i saidi seostamine võrgukanaliga
description: See teema selgitab, kuidas siduda oma rakenduse Microsoft Dynamics 365 Commerce saiti ühe või mitme võrgupoega.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb39b54e45e387067720dcbc5d9ccffbf8bf08b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211518"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="da7a9-103">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="da7a9-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da7a9-104">See teema selgitab, kuidas siduda oma rakenduse Microsoft Dynamics 365 Commerce saiti ühe või mitme võrgupoega.</span><span class="sxs-lookup"><span data-stu-id="da7a9-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="da7a9-105">Kui olete Dynamics 365 Commerce'i e-kaubanduse keskkonna Microsoft Dynamics Lifecycle Servicesi (LCS) portaali kasutades ette valmistanud, olete valmis looma oma esimest e-kaubanduse veebisaiti.</span><span class="sxs-lookup"><span data-stu-id="da7a9-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="da7a9-106">Algse saidi loomise osana seostate saidi eelnevalt loodud võrgupoega.</span><span class="sxs-lookup"><span data-stu-id="da7a9-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="da7a9-107">See samm seob saidi veebikanaliga ja võimaldab saidil kuvada navigeerimise hierarhiat, tooteid, kategooriaid, hindu, tarnevõimalusi ja kõike muud, mille veebipoes määratlete.</span><span class="sxs-lookup"><span data-stu-id="da7a9-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="da7a9-108">LCS-is uue saidi loomiseks ja sellega veebipoe seostamiseks valige saidi autorluse keskkonna link.</span><span class="sxs-lookup"><span data-stu-id="da7a9-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="da7a9-109">Seejärel valige saidi autorluse keskkonna lehel suvand **Uus sait**.</span><span class="sxs-lookup"><span data-stu-id="da7a9-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="da7a9-110">Dialoogiaknas **Uus sait** peate sisestama oma saidi kohta mõned põhiandmed.</span><span class="sxs-lookup"><span data-stu-id="da7a9-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="da7a9-111">Esitatava teabe täielikku selgitust vaadake artiklist [Uue e-kaubanduse saidi loomine](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="da7a9-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="da7a9-112">Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut.</span><span class="sxs-lookup"><span data-stu-id="da7a9-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="da7a9-113">Saate kasutada ka leheküljel üleval vasakul ripploendit, et pääseda toodete juurde kategooriate põhjal.</span><span class="sxs-lookup"><span data-stu-id="da7a9-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da7a9-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="da7a9-114">Additional resources</span></span>

[<span data-ttu-id="da7a9-115">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="da7a9-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="da7a9-116">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="da7a9-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="da7a9-117">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="da7a9-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="da7a9-118">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="da7a9-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="da7a9-119">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="da7a9-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="da7a9-120">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="da7a9-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="da7a9-121">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="da7a9-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="da7a9-122">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="da7a9-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="da7a9-123">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="da7a9-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="da7a9-124">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="da7a9-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]