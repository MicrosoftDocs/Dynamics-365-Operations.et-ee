---
title: Pilvepõhise otsingu ülevaade
description: See teema annab rakenduse Microsoft Dynamics 365 Commerce pilvepõhise otsingu ülevaate.
author: ashishmsft
manager: annbe
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00a3de2515cea341f7529b8cb6cb2caae5e33d22
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527439"
---
# <a name="cloud-powered-search-overview"></a><span data-ttu-id="a7173-103">Pilvepõhise otsingu ülevaade</span><span class="sxs-lookup"><span data-stu-id="a7173-103">Cloud-powered search overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a7173-104">See teema annab rakenduse Microsoft Dynamics 365 Commerce pilvepõhise otsingu ülevaate.</span><span class="sxs-lookup"><span data-stu-id="a7173-104">This topic gives an overview of cloud-powered search in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a7173-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a7173-105">Overview</span></span>

<span data-ttu-id="a7173-106">Toote tuvastatavus aitab tagada, et kliendid saavad kategooriaid sirvides, otsides ja filtreerides tooteid kiiresti ja hõlpsalt leida.</span><span class="sxs-lookup"><span data-stu-id="a7173-106">Product discoverability helps guarantee that customers can quickly and easily find products by browsing categories, searching, and filtering.</span></span> <span data-ttu-id="a7173-107">Jaemüüjad peavad toodete avastamist esmaseks vahendiks klientidega suhtlemisel kõigis kanalites.</span><span class="sxs-lookup"><span data-stu-id="a7173-107">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span>

<span data-ttu-id="a7173-108">Kliendid on harjunud veebiotsingu mootorite peaaegu hetkelise reaktsiooniajaga, keeruliste e-kaubanduse veebisaitidega, sotsiaalsete rakendustega, otsingusõna tippimisel automaatselt ilmuvate soovitustega, mitmetahulise navigeerimisega ja esiletõstmisega.</span><span class="sxs-lookup"><span data-stu-id="a7173-108">Customers are accustomed to the nearly instantaneous response times of web search engines, sophisticated e-Commerce websites, social apps, automatic suggestions that appear as they type search terms, faceted navigation, and highlighting.</span></span> <span data-ttu-id="a7173-109">Kui kliendid ei leia ühest e-kaubanduse poest otsitavat toodet piisavalt kiiresti, siis nad ei kõhkle, et minna erinevasse e-kaupluse poodi.</span><span class="sxs-lookup"><span data-stu-id="a7173-109">If customers can't find the product that they are looking for quickly enough in one e-Commerce store, they won't hesitate to go to a different e-Commerce store.</span></span>

<span data-ttu-id="a7173-110">Rakenduse Dynamics 365 Commerce pilvepõhine toote tuvastamine aitab jaemüüjatel jätkuvalt suurendada kliendi kinnipidamise ja teisendamise määrasid kõikide kanalite üleselt, nii e-kaubanduse kanalites kui ka kassa kanalites.</span><span class="sxs-lookup"><span data-stu-id="a7173-110">The cloud-powered product discoverability in Dynamics 365 Commerce helps retailers continue to increase consumer retention and conversion rates across all channels, both e-Commerce channels and point of sale (POS) channels.</span></span>

<span data-ttu-id="a7173-111">Rakenduse Dynamics 365 Commerce otsingul on parandatud võimalused, et aidata jaemüüjatel saavutada parem toodete tuvastatavus.</span><span class="sxs-lookup"><span data-stu-id="a7173-111">The Dynamics 365 Commerce search experience has improved capabilities to help retailers achieve better product discoverability.</span></span> <span data-ttu-id="a7173-112">Samal ajal pakuvad need võimalused e-kaubanduse liikluse jaoks vajalikku skaleeritavust ja jõudlust.</span><span class="sxs-lookup"><span data-stu-id="a7173-112">At the same time, these capabilities deliver the scalability and performance that are required for e-Commerce traffic.</span></span>

## <a name="browse-and-search"></a><span data-ttu-id="a7173-113">Sirvimine ja otsing</span><span class="sxs-lookup"><span data-stu-id="a7173-113">Browse and search</span></span>

<span data-ttu-id="a7173-114">Otsingu asjakohasus ja jõudlus on omnikanali kogemuse põhitegurid, kuna toote tuvastamine sõltub peamiselt teabe toomise ja sisu navigeerimise otsingu funktsioonidest.</span><span class="sxs-lookup"><span data-stu-id="a7173-114">Search relevance and performance are key factors in the omnichannel experience, because product discovery relies primarily on search functionality for information retrieval and content navigation.</span></span> <span data-ttu-id="a7173-115">Efektiivne ja tõhus sirvimis- ja otsingukogemus aitavad teisendamist suurendada.</span><span class="sxs-lookup"><span data-stu-id="a7173-115">An effective and efficient browse and search experience helps increase conversion.</span></span>

<span data-ttu-id="a7173-116">Järgmisel illustratsioonil on toodud tüüpiline sirvimis- ja otsingufunktsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="a7173-116">The following illustration shows an example of typical browse and search functionality.</span></span>

![Sihtlehe otsing](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a><span data-ttu-id="a7173-118">Mitmetahuline navigeerimine ja valiku kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="a7173-118">Faceted navigation and choice summary</span></span> 

<span data-ttu-id="a7173-119">Mitmetahuline navigeerimine aitab klientidel hõlpsamini sisu sirvida, võimaldades neil filtreerida piiritlusatribuutidega, mis on lingitud terminikomplekti mõistetega.</span><span class="sxs-lookup"><span data-stu-id="a7173-119">Faceted navigation helps customers more easily browse for content by letting them filter on refiners that are linked to terms in a term set.</span></span> <span data-ttu-id="a7173-120">Kui klient on valinud ja rakendanud piiritlusatribuudid, kuvatakse valikute kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="a7173-120">After a customer has selected and applied refiners, a summary of the choices is shown.</span></span> 

<span data-ttu-id="a7173-121">Mitmetahulist navigeerimist kasutades saate konfigureerida erinevad piiritlusatribuudid erinevatele terminikomplekti mõistetele, ilma et peaksite täiendavaid lehti looma.</span><span class="sxs-lookup"><span data-stu-id="a7173-121">By using faceted navigation, you can configure different refiners for different terms in a term set, without having to create additional pages.</span></span> 

<span data-ttu-id="a7173-122">Järgmisel joonisel on kujutatud näide, kus otsingus kasutatakse mitmetahulist navigeerimist.</span><span class="sxs-lookup"><span data-stu-id="a7173-122">The following illustration shows an example where faceted navigation is used in a search.</span></span>

![Valikute kokkuvõte](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a><span data-ttu-id="a7173-124">Kõikehõlmavad automaatsed soovitused</span><span class="sxs-lookup"><span data-stu-id="a7173-124">Immersive autosuggest</span></span>

<span data-ttu-id="a7173-125">Praegused automaatse soovituse funktsioonid näitavad ainult märksõnu, mis käivitavad vastava märksõna otsingu.</span><span class="sxs-lookup"><span data-stu-id="a7173-125">Current autosuggest functionality just shows keywords that trigger a search for the matching keyword.</span></span> <span data-ttu-id="a7173-126">Rakenduse Dynamics 365 Commerce uute täiustuste abil saavad kliendid sageli tuvastada lingid toodetele enne, kui nad on tippimise lõpetanud.</span><span class="sxs-lookup"><span data-stu-id="a7173-126">Because of new enhancements in Dynamics 365 Commerce, customers can often discover links to products before they have finished typing.</span></span>

<span data-ttu-id="a7173-127">Dynamics 365 Commerce toetab ka erinevate kategooriate märksõnade vasteid.</span><span class="sxs-lookup"><span data-stu-id="a7173-127">Dynamics 365 Commerce also supports functionality for keyword matches in various categories.</span></span> <span data-ttu-id="a7173-128">See funktsioon võimaldab klientidel näha kattuvate märksõnade arvu kategooriate lõikes ja käivitada märksõnade otsimise teistes kategooriates.</span><span class="sxs-lookup"><span data-stu-id="a7173-128">This functionality lets customers see the number of matching keywords across categories and trigger a search for a keyword in other categories.</span></span>

<span data-ttu-id="a7173-129">Järgmisel joonisel on kujutatud näide, kus kasutatakse kõikehõlmavaid automaatseid soovitusi.</span><span class="sxs-lookup"><span data-stu-id="a7173-129">The following illustration shows an example where immersive autosuggest is being used.</span></span>

![kõikehõlmavad automaatsed soovitused](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a><span data-ttu-id="a7173-131">Tüüp</span><span class="sxs-lookup"><span data-stu-id="a7173-131">Sort</span></span>

<span data-ttu-id="a7173-132">Rakenduse Dynamics 365 Commerce täiustatud sortimine võimaldab klientidel sortida, otsida ja sirvida otsingutulemusi ning täpsustada neid kriteeriumite põhjal, nagu hind, toote nimi ja tootenumber.</span><span class="sxs-lookup"><span data-stu-id="a7173-132">Enhanced sorting in Dynamics 365 Commerce lets customers sort, search, and browse search results, and refine them by criteria such as price, product name, and product number.</span></span> <span data-ttu-id="a7173-133">Kliendid saavad lisaks sorteerida tulemusi selle põhjal, kas toode on uus, suurima läbimüügiga või hiljuti lisatud.</span><span class="sxs-lookup"><span data-stu-id="a7173-133">Customers can also sort results based on whether a product is new, top-selling, or recently added.</span></span>

>[!NOTE]
><span data-ttu-id="a7173-134">Need pilvepõhised otsinguvõimalused on saadaval alates versioonist 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="a7173-134">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="a7173-135">Veenduge, et jaotises **Kaubanduse parameetrid > konfiguratsiooniparameetrid** on kirje ProductSearch.UseAzureSearch väärtuseks määratud „tõene”.</span><span class="sxs-lookup"><span data-stu-id="a7173-135">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="a7173-136">![Pilvepõhise otsingu konfiguratsiooniparameetrid](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="a7173-136">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7173-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a7173-137">Additional resources</span></span>

[<span data-ttu-id="a7173-138">Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="a7173-138">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="a7173-139">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="a7173-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)
