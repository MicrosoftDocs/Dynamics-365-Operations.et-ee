---
title: Dynamics 365 Commerce'i saidi seostamine võrgukanaliga
description: See teema selgitab, kuidas siduda oma rakenduse Microsoft Dynamics 365 Commerce saiti ühe või mitme võrgupoega.
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7ceef55bac11ae8a1f7d9dafbddc45d67b836504
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797301"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="5b6e8-103">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="5b6e8-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b6e8-104">See teema selgitab, kuidas siduda oma rakenduse Microsoft Dynamics 365 Commerce saiti ühe või mitme võrgupoega.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="5b6e8-105">Kui olete Dynamics 365 Commerce'i e-kaubanduse keskkonna Microsoft Dynamics Lifecycle Servicesi (LCS) portaali kasutades ette valmistanud, olete valmis looma oma esimest e-kaubanduse veebisaiti.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="5b6e8-106">Algse saidi loomise osana seostate saidi eelnevalt loodud võrgupoega.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="5b6e8-107">See samm seob saidi veebikanaliga ja võimaldab saidil kuvada navigeerimise hierarhiat, tooteid, kategooriaid, hindu, tarnevõimalusi ja kõike muud, mille veebipoes määratlete.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="5b6e8-108">LCS-is uue saidi loomiseks ja sellega veebipoe seostamiseks valige saidi autorluse keskkonna link.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="5b6e8-109">Seejärel valige saidi autorluse keskkonna lehel suvand **Uus sait**.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="5b6e8-110">Dialoogiaknas **Uus sait** peate sisestama oma saidi kohta mõned põhiandmed.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="5b6e8-111">Esitatava teabe täielikku selgitust vaadake artiklist [Uue e-kaubanduse saidi loomine](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="5b6e8-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="5b6e8-112">Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="5b6e8-113">Saate kasutada ka leheküljel üleval vasakul ripploendit, et pääseda toodete juurde kategooriate põhjal.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b6e8-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5b6e8-114">Additional resources</span></span>

[<span data-ttu-id="5b6e8-115">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5b6e8-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5b6e8-116">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="5b6e8-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="5b6e8-117">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="5b6e8-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5b6e8-118">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="5b6e8-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="5b6e8-119">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="5b6e8-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="5b6e8-120">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="5b6e8-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="5b6e8-121">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="5b6e8-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5b6e8-122">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="5b6e8-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="5b6e8-123">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="5b6e8-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="5b6e8-124">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="5b6e8-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]