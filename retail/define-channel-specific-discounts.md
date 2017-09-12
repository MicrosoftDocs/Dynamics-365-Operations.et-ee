---
title: "Kanalipõhiste allahindluste määratlemine"
description: "Jaemüüjad määravad tihti erinevates kanalites erinevad allahindlused. Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a0286ab72d7fa6b40228dfdcabde00bee9995d74
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="ba6ea-104">Kanalipõhiste allahindluste määratlemine</span><span class="sxs-lookup"><span data-stu-id="ba6ea-104">Define channel-specific discounts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ba6ea-105">Jaemüüjad määravad tihti erinevates kanalites erinevad allahindlused.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="ba6ea-106">Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span> 

<a name="channel-specific-discounts"></a><span data-ttu-id="ba6ea-107">Kanalipõhised allahindlused</span><span class="sxs-lookup"><span data-stu-id="ba6ea-107">Channel-specific discounts</span></span>
--------------------------

<span data-ttu-id="ba6ea-108">Jaemüüjad pakuvad sageli erinevates kanalites erinevaid allahindlusi.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="ba6ea-109">Seda saab teha kohalike turutingimuste arvestamiseks või konkureerivate jaemüüjatega toime tulemiseks.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="ba6ea-110">Microsoft Dynamics 365 for Retail kasutab kanalipõhiste allahindluste määratlemiseks hinnagruppe.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="ba6ea-111">Hinnagruppe saab määrata vähemalt ühele järgmisele üksusele: kanalid, kataloogid, alluvused ja püsikliendiprogrammid.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="ba6ea-112">See artikkel käsitleb kanaleid, kuid samad mõisted kehtivad kataloogi allahindlustele, alluvuste allahindlustele ja püsikliendiallahindlustele.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="ba6ea-113">Hinnagrupid</span><span class="sxs-lookup"><span data-stu-id="ba6ea-113">Price groups</span></span>

<span data-ttu-id="ba6ea-114">[![Hinnagrupid](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="ba6ea-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="ba6ea-115">Ülalolev joonis illustreerib seost kande võimalike üksuste vahel (kanal, kataloog, alluvus, klient, püsikliendikaart) ja mitmesuguseid allahindluse tüüpe, mida saab konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="ba6ea-116">Kõik kanded tehakse kanalis, seega on kanal kindlasti kandel olemas.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="ba6ea-117">Ülejäänud üksused on valikulised.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-117">The remaining entities are optional.</span></span> <span data-ttu-id="ba6ea-118">Igal koondandmete lehel on link seotud hinnagruppide lehele, kus saate vaadata ja lisada vajalikke hinnagruppe.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="ba6ea-119">Hinnagruppi kasutatakse nelja tüüpi üksuste seostamiseks allahindluste, hinna korrigeerimiste ja kaubanduslepetega.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="ba6ea-120">Soovitame plaanida strateegia, kuidas hinnagruppe nimetada, et neid korras hoida.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="ba6ea-121">Üks võimalus on kasutada ees või järel tähte või numbrit, et erinevaid tüüpe eristada.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="ba6ea-122">Näiteks 1-xxxxx kanali hinnagruppide puhul ja 2-xxxxx kataloogi hinnagruppide puhul.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="ba6ea-123">Neli päringulehte keskenduvad igale jaemüügiüksusele, millega on seotud allahindlused.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

-   <span data-ttu-id="ba6ea-124">**Jaemüügikanali hinnagrupid**– sellel lehel on loend kanalitest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-124">**Retail channel price groups** - This page shows a list of channels and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="ba6ea-125">**Kataloogi hinnagrupid**– sellel lehel on loend kataloogidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-125">**Catalog price groups** - This page shows a list of catalogs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="ba6ea-126">**Püsikliendi hinnagrupid**– sellel lehel on loend püsikliendiprogrammidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-126">**Loyalty price groups** - This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="ba6ea-127">**Sidusettevõtete hinnagrupid**– sellel lehel on loend sidusettevõtetest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-127">**Affiliation price groups** - This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="ba6ea-128">Kanali allahindluse seadistuse näide</span><span class="sxs-lookup"><span data-stu-id="ba6ea-128">Example channel discount set up</span></span>
<span data-ttu-id="ba6ea-129">Järgmine näide illustreerib kanali allahindluse seadistamiseks vajalikke toiminguid.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1.  <span data-ttu-id="ba6ea-130">Selles näites on kanal nimega **Houston** ja loote uue allahindluse nimega **Tagasi-kooli.**</span><span class="sxs-lookup"><span data-stu-id="ba6ea-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School.**</span></span>
2.  <span data-ttu-id="ba6ea-131">Kuna hinnakujunduse ja allahindluste strateegia hõlmab kanali allahindluste võimalust, luuakse kanali loomisel alati kanalipõhine hinnagrupp.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3.  <span data-ttu-id="ba6ea-132">Teil on hinnagrupp **Houston-PG** ja see on määratud kanalile **Houston**.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4.  <span data-ttu-id="ba6ea-133">Pärast uue allahindluse **Tagasi-kooli** loomist tuleb klõpsata valikut **Hinnagrupid** lehe **Allahindlus** ülemises osas.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="ba6ea-134">Avaneb leht **Allahindluse hinnagrupid**.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="ba6ea-135">Seejärel klõpsake nuppu **Uus** ja valige hinnagrupp **Houston-PG**.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5.  <span data-ttu-id="ba6ea-136">Nüüd saate allahindluse lubada ja kanalisse suunata.</span><span class="sxs-lookup"><span data-stu-id="ba6ea-136">Now you can enable the discount and push it to the channel.</span></span>

 

<a name="see-also"></a><span data-ttu-id="ba6ea-137">Vt ka</span><span class="sxs-lookup"><span data-stu-id="ba6ea-137">See also</span></span>
--------

[<span data-ttu-id="ba6ea-138">Hinnakorrigeerimised ja allahindlused</span><span class="sxs-lookup"><span data-stu-id="ba6ea-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)




