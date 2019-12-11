---
title: Tootesoovituste ülevaade
description: Selles teemas antakse üldist teavet tootesoovituste kohta. Tootesoovitused võimaldavad klientidel kergesti ja kiiresti leida tooteid, mida nad soovivad ja isegi tooteid, mida nad algselt ei kavatsenud osta.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770042"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="9e4e9-104">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="9e4e9-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9e4e9-105">Rakendust Microsoft Dynamics 365 Commerce saab kasutada tootesoovituste kuvamiseks e-kaubanduse veebisaidil ja kassa (POS) seadmes.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="9e4e9-106">Tootesoovitused on kaubad, millest klient võib huvitatud olla.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="9e4e9-107">Soovitused põhinevad teiste klientide ostude suundumustel võrgus ja kliendiga näost-näkku suhtlevates kauplustes.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="9e4e9-108">Tootesoovitused võimaldavad klientidel lihtsalt ja kiiresti leida tooteid, mida nad soovivad, kui neil on kogemus, mis neile hästi sobib.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="9e4e9-109">Ristmüüki ja ülesmüüki saab kasutada isegi selleks, et aidata klientidel leida täiendavaid tooteid, mida nad algselt ei kavatsenud osta.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="9e4e9-110">Kui soovitusi kasutatakse toote avastuse hõlbustamiseks, võivad need luua rohkem konversiooni võimalusi, aidata suurendada müügitulu ja aidata veelgi suurendada kliendi rahulolu ja hoidmist.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="9e4e9-111">Kaubanduses toetavad tootesoovitused suures osas Microsofti soovituste masinõppe tehnoloogiaid.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="9e4e9-112">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="9e4e9-112">Scenarios</span></span>

<span data-ttu-id="9e4e9-113">Tootesoovitused on saadaval järgmiste stsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="9e4e9-114">**E-kaubanduse lehe sirvimise või sihtlehe mis tahes kaupluse lehel:** kui kliendid või kaupluse kaastöötajad külastavad kaupluse lehte, võib soovituse mootor soovitada tooteid loendites **Uus**, **Enim müüdud** ja **Populaarsed**.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="9e4e9-115">**Lehel toote üksikasjad:** kui kliendid või kaupluse kaastöötajad külastavad lehte **Toote üksikasjad**, soovitab soovituse mootor lisakaupu, mida tõenäoliselt ka ostetakse.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="9e4e9-116">Need kaubad kuvatakse loendis **Inimestele meeldib ka**.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="9e4e9-117">**Kande või kassa lehel:** soovituse mootor pakub kaupu, mis põhinevad kogu ostukorvis olevate kaupade loendil.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="9e4e9-118">Need kaubad kuvatakse loendis **Sageli koos ostetud**.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="9e4e9-119">Soovitamise teenus</span><span class="sxs-lookup"><span data-stu-id="9e4e9-119">Recommendation service</span></span>

<span data-ttu-id="9e4e9-120">Tootesoovitused kasutavad soovituste masinõppe tehnoloogiaid järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="9e4e9-121">Andmed vormingus, mida soovitusteenus nõuab, ekstraheeritakse kaubanduse operatiivandmebaasist ja saadetakse olemi kauplusesse.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="9e4e9-122">Soovitusteenus kasutab andmeid soovitusmudelite koolitamiseks järgmiste loendite jaoks: **Inimestele meeldib ka**, **Sageli koos ostetud**, **Uus**, **Enim müüdud** ja **Populaarsed**.</span><span class="sxs-lookup"><span data-stu-id="9e4e9-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e4e9-123">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9e4e9-123">Additional resources</span></span>

[<span data-ttu-id="9e4e9-124">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="9e4e9-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9e4e9-125">Kureeritud tootesoovituste loendite loomine</span><span class="sxs-lookup"><span data-stu-id="9e4e9-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9e4e9-126">AI-ML-põhiste tootesoovituse tulemuste haldamine</span><span class="sxs-lookup"><span data-stu-id="9e4e9-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9e4e9-127">Tootesoovituste loendite lisamine lehtedele</span><span class="sxs-lookup"><span data-stu-id="9e4e9-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
