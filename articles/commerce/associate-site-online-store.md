---
title: E-kaubanduse saidi seostamine võrgukanaliga
description: See teema selgitab, kuidas siduda oma rakenduse Microsoft Dynamics 365 Commerce saiti ühe või mitme võrgupoega.
author: stuharg
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: bicyclingfool
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62d3c168967bd680b3ded56e627730324f2a5ec6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945578"
---
# <a name="associate-an-e-commerce-site-with-an-online-channel"></a><span data-ttu-id="fdb57-103">E-kaubanduse saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="fdb57-103">Associate an e-Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fdb57-104">See teema selgitab, kuidas siduda oma rakenduse Microsoft Dynamics 365 Commerce saiti ühe või mitme võrgupoega.</span><span class="sxs-lookup"><span data-stu-id="fdb57-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="fdb57-105">Kui olete e-kaubanduse Microsoft Dynamicsi teenust Lifecycle Services (LCS) kasutades ette valmistanud, olete valmis looma oma esimese e-kaubanduse veebisaidi.</span><span class="sxs-lookup"><span data-stu-id="fdb57-105">After you've provisioned e-Commerce by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-Commerce website.</span></span> <span data-ttu-id="fdb57-106">Algse saidi loomise osana seostate saidi eelnevalt loodud võrgupoega.</span><span class="sxs-lookup"><span data-stu-id="fdb57-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="fdb57-107">See samm seob saidi veebikanaliga ja võimaldab saidil kuvada navigeerimise hierarhiat, tooteid, kategooriaid, hindu, tarnevõimalusi ja kõike muud, mille veebipoes määratlete.</span><span class="sxs-lookup"><span data-stu-id="fdb57-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="fdb57-108">LCS-is uue saidi loomiseks ja sellega veebipoe seostamiseks valige saidi autorluse keskkonna link.</span><span class="sxs-lookup"><span data-stu-id="fdb57-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="fdb57-109">Seejärel valige saidi autorluse keskkonna lehel suvand **Uus sait**.</span><span class="sxs-lookup"><span data-stu-id="fdb57-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="fdb57-110">Dialoogiaknas **Uus sait** peate sisestama oma saidi kohta mõned põhiandmed.</span><span class="sxs-lookup"><span data-stu-id="fdb57-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="fdb57-111">Esitatava teabe täielikku selgitust vaadake teemast [Uue e-kaubanduse saidi loomine](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="fdb57-111">For a complete explanation of the information that you must provide, see [Create a new e-Commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="fdb57-112">Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut.</span><span class="sxs-lookup"><span data-stu-id="fdb57-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="fdb57-113">Saate kasutada ka leheküljel üleval vasakul ripploendit, et pääseda toodete juurde kategooriate põhjal.</span><span class="sxs-lookup"><span data-stu-id="fdb57-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdb57-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fdb57-114">Additional resources</span></span>

[<span data-ttu-id="fdb57-115">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fdb57-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fdb57-116">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="fdb57-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="fdb57-117">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="fdb57-117">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="fdb57-118">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="fdb57-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="fdb57-119">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="fdb57-119">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fdb57-120">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="fdb57-120">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fdb57-121">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="fdb57-121">Enable location-based store detection</span></span>](enable-store-detection.md)
