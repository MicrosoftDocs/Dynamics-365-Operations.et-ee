---
title: Võrgupoe kanali häälestamine
description: See artikkel annab teavet kaupluste veebipoodide kanalite kohta ja kuidas neid rakenduses Dynamics 365 Commerce seadistada.
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096890"
---
# <a name="set-up-an-online-store-channel"></a><span data-ttu-id="401f0-103">Võrgupoe kanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="401f0-103">Set up an online store channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="401f0-104">See artikkel annab teavet kaupluste veebipoodide kanalite kohta ja kuidas neid rakenduses Dynamics 365 Commerce seadistada.</span><span class="sxs-lookup"><span data-stu-id="401f0-104">This article provides information about online store channels and how to set them up in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="401f0-105">Commerce toetab mitut jaemüügikanalit.</span><span class="sxs-lookup"><span data-stu-id="401f0-105">Commerce supports multiple retail channels.</span></span> <span data-ttu-id="401f0-106">Need kanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks).</span><span class="sxs-lookup"><span data-stu-id="401f0-106">These channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="401f0-107">Võrgupoed annavad jaemüüjale kohaloleku võrgus, nii et tema kliendid saavad lisaks jaekauplusest osta tooteid ka võrgupoest.</span><span class="sxs-lookup"><span data-stu-id="401f0-107">Online stores give an online presence to a retailer, so that customers can purchase products from the retailer's online store in addition to its retail stores.</span></span> <span data-ttu-id="401f0-108">Kui kliendid ostavad tooteid võrgupoest, saab need tooted neile tarnida või võivad nad tooted kätte saada kohalikust kauplusest.</span><span class="sxs-lookup"><span data-stu-id="401f0-108">If customers purchase products from the online store, those products can be shipped to them, or the customers can pick the products up at a local store.</span></span> 

<span data-ttu-id="401f0-109">Võrgupoe saate luua Commerce’i kliendis.</span><span class="sxs-lookup"><span data-stu-id="401f0-109">You create an online store in the Commerce client.</span></span> <span data-ttu-id="401f0-110">Seejärel avaldatakse võrgupood kolmanda poole võrgupoele, mis on integreeritud Commerce’iga.</span><span class="sxs-lookup"><span data-stu-id="401f0-110">This online store is then published to a third-party online store that is integrated with Commerce.</span></span> <span data-ttu-id="401f0-111">Muu osapoole võrgupood toimib võrgupoe fassaadina (kasutajaliidesena) ning võimaldab teil valida kliendihaldussüsteemi (CMS) ja kasutajaliidese võimalusi.</span><span class="sxs-lookup"><span data-stu-id="401f0-111">The third-party online store serves as the storefront (UI) for the online store, and gives you a choice of customer management system (CMS) and UI capabilities.</span></span> <span data-ttu-id="401f0-112">Mitu seda tüüpi integratsiooni on saadaval.</span><span class="sxs-lookup"><span data-stu-id="401f0-112">Several integrations of this type are available.</span></span> 

<span data-ttu-id="401f0-113">Atribuudid, mida saate võrgupoe jaoks määratleda, juhivad võrgupoe toimimist.</span><span class="sxs-lookup"><span data-stu-id="401f0-113">The properties that you define for the online store control the behavior of the online store.</span></span> <span data-ttu-id="401f0-114">Näiteks määratlete navigeerimiskategooria hierarhia ja määrate selle võrgupoele.</span><span class="sxs-lookup"><span data-stu-id="401f0-114">For example, you define the navigation category hierarchy and assign it to the online store.</span></span> <span data-ttu-id="401f0-115">Võrgupoe avaldamisel muu osapoole võrgupoele kuvatakse navigeerimiskategooria hierarhia kaupluse võrguversioonis.</span><span class="sxs-lookup"><span data-stu-id="401f0-115">When you publish the online store to the third-party online store, the navigation category hierarchy appears in the online version of the store.</span></span> <span data-ttu-id="401f0-116">Ostjad kasutavad navigeerimiskategooria hierarhiat võrgupoe sisu sirvimiseks ja toodete otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="401f0-116">Shoppers then use the navigation category hierarchy to browse the online store and search for products.</span></span> 

<span data-ttu-id="401f0-117">Võrgupoe loomiseks peate seadistama komponendid, mis võimaldavad kaupluse jaoks kannete töötlemist.</span><span class="sxs-lookup"><span data-stu-id="401f0-117">To create an online store, you must set up the components that enable transactions to be processed for the store.</span></span> <span data-ttu-id="401f0-118">Näiteks tuleb lisada sortimentid, rakendada atribuudid ning seadistada makseviisid ja tarneviisid.</span><span class="sxs-lookup"><span data-stu-id="401f0-118">For example, you must add assortments, apply attributes, and set up payment methods and shipping methods.</span></span> <span data-ttu-id="401f0-119">Samuti saate määrata hindu, kampaaniaid, allahindlusi, kaubandusleppeid ja võrgupoes kehtivaid tarnetingimusi.</span><span class="sxs-lookup"><span data-stu-id="401f0-119">You can also define prices, promotions, discounts, trade agreements, and shipping terms that are specific to the online store.</span></span> 

<span data-ttu-id="401f0-120">Pärast võrgupoe avaldamist muu poole võrgupoele saate võrgupoe jaoks luua tootekatalooge.</span><span class="sxs-lookup"><span data-stu-id="401f0-120">After you publish the online store to the third-party online store, you can create product catalogs for the online store.</span></span> <span data-ttu-id="401f0-121">Kataloogi toodetest saavad võrgupoe tooteloendid.</span><span class="sxs-lookup"><span data-stu-id="401f0-121">The products in the catalog become product listings in the online store.</span></span> <span data-ttu-id="401f0-122">Kui klient ostab võrgupoest tooteid, värskendatakse ja sünkroonitakse saadaolevad varud klientrakenduses.</span><span class="sxs-lookup"><span data-stu-id="401f0-122">When a shopper purchases products from the online store, the available inventory is updated and synchronized in the client.</span></span> <span data-ttu-id="401f0-123">Samuti luuakse ostude kohta müügitellimused ning saadetakse tellimuse täitmiseks ja töötlemiseks klientrakendusse.</span><span class="sxs-lookup"><span data-stu-id="401f0-123">Additionally, sales orders are generated for the purchases, and are sent to the client for order fulfillment and processing.</span></span>

## <a name="set-up-an-online-store"></a><span data-ttu-id="401f0-124">Võrgupoe seadistamine</span><span class="sxs-lookup"><span data-stu-id="401f0-124">Set up an online store</span></span>

<span data-ttu-id="401f0-125">Võrgupoe seadistamiseks täitke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="401f0-125">To set up an online store, you must complete the following tasks.</span></span>

1. <span data-ttu-id="401f0-126">Looge võrgupood.</span><span class="sxs-lookup"><span data-stu-id="401f0-126">Create the online store.</span></span>
2. <span data-ttu-id="401f0-127">Lisage võrgupood sobivatesse organisatsiooni hierarhiatesse.</span><span class="sxs-lookup"><span data-stu-id="401f0-127">Add the online store to the appropriate organization hierarchies.</span></span>
3. <span data-ttu-id="401f0-128">Lisage sortimendid, mis sisaldavad võrgupoes saadavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="401f0-128">Add assortments that include the products that are available in the online store.</span></span>
4. <span data-ttu-id="401f0-129">Määrake või looge võrgupoe jaoks hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="401f0-129">Assign or create price groups for the online store.</span></span>
5. <span data-ttu-id="401f0-130">Seadistage tarneviisid, mis on võrgupoe jaoks saadaval.</span><span class="sxs-lookup"><span data-stu-id="401f0-130">Set up the modes of delivery that are available for the online store.</span></span>
6. <span data-ttu-id="401f0-131">Määrake võrgupoes kehtivad makseviisid.</span><span class="sxs-lookup"><span data-stu-id="401f0-131">Assign the payment methods that are accepted by the online store.</span></span>
7. <span data-ttu-id="401f0-132">Kui võimaldate toodete tellimist veebis ja kauba kättesaamist kohalikust kauplusest, määrake võrgupoele kaupluselokaatori grupid.</span><span class="sxs-lookup"><span data-stu-id="401f0-132">If you allow shoppers to order products online and then pick them up at a local store, assign store locator groups to the online store.</span></span>
8. <span data-ttu-id="401f0-133">Määrake võrgupoele kanalite, toodete ja müügitellimuste atribuudid.</span><span class="sxs-lookup"><span data-stu-id="401f0-133">Assign attributes for channels, products, and sales orders to the online store.</span></span> <span data-ttu-id="401f0-134">Kanali atribuudid kehtivad kogu võrgupoele, toote atribuudid kehtivad võrgupoes pakutavatele toodetele ja müügitellimuse atribuudid kehtivad võrgupoes loodud müügitellimustele.</span><span class="sxs-lookup"><span data-stu-id="401f0-134">Channel attributes apply to the whole online store, product attributes apply to the products that are offered in the online store, and sales order attributes apply to the sales orders that are generated from the online store.</span></span>
9. <span data-ttu-id="401f0-135">Vastendage atribuudid, et määratleda omadused, mis määravad, kuidas need atribuudid võrgupoes toimivad.</span><span class="sxs-lookup"><span data-stu-id="401f0-135">Map attributes to define the properties that determine how those attributes behave in the online store.</span></span> <span data-ttu-id="401f0-136">Näiteks saab atribuudid määratleda kas nõutavaks või otsitavaks.</span><span class="sxs-lookup"><span data-stu-id="401f0-136">For example, attributes can be defined as required or searchable.</span></span>
10. <span data-ttu-id="401f0-137">Avaldage võrgupood, et luua poe struktuur oma valitud muu osapoole võrgupoes.</span><span class="sxs-lookup"><span data-stu-id="401f0-137">Publish the online store to generate the store structure on your choice of third-party online store.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="401f0-138">Tähtis! Enne võrgupoe avaldamist peate seadistama selle jaotusasukoha.</span><span class="sxs-lookup"><span data-stu-id="401f0-138">Before you publish the online store, you must set up a distribution location for it.</span></span>

## <a name="commerce-channel-navigation-hierarchies"></a><span data-ttu-id="401f0-139">Commerce’i navigeerimishierarhiad</span><span class="sxs-lookup"><span data-stu-id="401f0-139">Commerce channel navigation hierarchies</span></span>

<span data-ttu-id="401f0-140">Enne võrgupoe loomist peate määrama kaubanduskanali navigeerimishierarhia, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="401f0-140">Before you create an online store, you must define the commerce channel navigation hierarchy that you want to use for it.</span></span> <span data-ttu-id="401f0-141">Kanali navigeerimishierarhia tähistab kategooriahierarhiat, mis kuvatakse võrgupoes pärast poe avaldamist.</span><span class="sxs-lookup"><span data-stu-id="401f0-141">The channel navigation hierarchy represents the category hierarchy that is displayed in the online store after the store is published.</span></span> <span data-ttu-id="401f0-142">Võrgupoe tootekataloogide avaldamisel vastendatakse kataloogis olevad tooted kanali navigeerimishierarhia kategooriatega.</span><span class="sxs-lookup"><span data-stu-id="401f0-142">When you publish product catalogs to the online store, the products in the catalog are mapped to the categories in the channel navigation hierarchy.</span></span> <span data-ttu-id="401f0-143">Seejärel kasutavad ostjad hierarhiat võrgupoes navigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="401f0-143">Shoppers then use the hierarchy to navigate in the online store.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="401f0-144">Organisatsiooni hierarhiad</span><span class="sxs-lookup"><span data-stu-id="401f0-144">Organization hierarchies</span></span>

<span data-ttu-id="401f0-145">Organisatsiooni hierarhiaid kasutatakse kaubanduskanalite struktureerimiseks ja seoste tähistamiseks ettevõtet moodustavate organisatsioonide vahel.</span><span class="sxs-lookup"><span data-stu-id="401f0-145">Organization hierarchies are used to structure commerce channels and to represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="401f0-146">Võrgupoodide seadistamisel saate neid organisatsiooni hierarhiasse lisada.</span><span class="sxs-lookup"><span data-stu-id="401f0-146">When you set up online stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="401f0-147">Poed jagavad seejärel sortimentide, täiendamise ja aruandluse jaoks kasutatavaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="401f0-147">The stores then share the data that is used for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="401f0-148">Organisatsiooni hierarhia loomisel peate määrama sellele eesmärgi.</span><span class="sxs-lookup"><span data-stu-id="401f0-148">When you create an organization hierarchy, you assign a purpose to it.</span></span> <span data-ttu-id="401f0-149">Eesmärk näitab, kuidas hierarhiat ettevõtte struktuuris kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="401f0-149">The purpose indicates how the hierarchy is used in the business structure.</span></span> <span data-ttu-id="401f0-150">Saate poe toimingute jaoks luua ühe organisatsiooni hierarhia ja kasutada seda sortimentide, täiendamise ja aruannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="401f0-150">You can create one organization hierarchy for your store operations, and use that hierarchy for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="401f0-151">Teise võimalusena saate iga eesmärgi jaoks luua eraldi organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="401f0-151">Alternatively, you can create a separate organization hierarchy for each purpose.</span></span> <span data-ttu-id="401f0-152">Samuti saate luua mitu sama eesmärgiga hierarhiat ja määrata igale neist eraldi kanali.</span><span class="sxs-lookup"><span data-stu-id="401f0-152">You can also create multiple hierarchies that have the same purpose, and assign a separate channel to each one.</span></span> <span data-ttu-id="401f0-153">Kui kavatsete avaldada võrgupoes tootekataloogid, peaksite võrgupoe lisama vähemalt sortimendi organisatsioonihierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="401f0-153">If you plan to publish product catalogs to the online store, you should, at a minimum, add the online store to an organization hierarchy for assortments.</span></span> <span data-ttu-id="401f0-154">Kataloogis olevad tooted on valitud võrgupoele määratud sortimentidest.</span><span class="sxs-lookup"><span data-stu-id="401f0-154">The products in a catalog are selected from the assortments that are assigned to the online store.</span></span> <span data-ttu-id="401f0-155">Kataloogi avaldamisel võrdleb avaldamisprotsess võrgupoele määratud sortimendi ja kataloogi kaasatud toodete kehtivuskuupäevi, et kindlaks teha, milliseid tooteid võrgupoes kättesaadavaks muuta.</span><span class="sxs-lookup"><span data-stu-id="401f0-155">When the catalog is published, the publishing process compares the effective dates for the assortment that is assigned to the online store with the products that are included in the catalog to determine which products to make available in the online store.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="401f0-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="401f0-156">Additional resources</span></span>

[<span data-ttu-id="401f0-157">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="401f0-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="401f0-158">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="401f0-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="401f0-159">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="401f0-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="401f0-160">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="401f0-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="401f0-161">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="401f0-161">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="401f0-162">URL-i hulgiümbersuunamiste üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="401f0-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="401f0-163">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="401f0-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="401f0-164">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="401f0-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="401f0-165">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="401f0-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="401f0-166">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="401f0-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="401f0-167">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="401f0-167">Enable location-based store detection</span></span>](enable-store-detection.md)
