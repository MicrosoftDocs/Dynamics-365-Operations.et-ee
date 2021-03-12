---
title: Kanalipõhiste allahindluste määratlemine
description: Jaemüüjad määravad tihti erinevates kanalites erinevad allahindlused. Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 990c0d0b4b89420094dc86552b3e07717e5c7056
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991386"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="81e4e-104">Kanalipõhiste allahindluste määratlemine</span><span class="sxs-lookup"><span data-stu-id="81e4e-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81e4e-105">Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="81e4e-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="81e4e-106">Kanalipõhised allahindlused</span><span class="sxs-lookup"><span data-stu-id="81e4e-106">Channel-specific discounts</span></span>

<span data-ttu-id="81e4e-107">Jaemüüjad pakuvad sageli erinevates kanalites erinevaid allahindlusi.</span><span class="sxs-lookup"><span data-stu-id="81e4e-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="81e4e-108">Seda saab teha kohalike turutingimuste arvestamiseks või konkureerivate jaemüüjatega toime tulemiseks.</span><span class="sxs-lookup"><span data-stu-id="81e4e-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="81e4e-109">Commerce kasutab kanalipõhiste allahindluste määratlemiseks hinnagruppe.</span><span class="sxs-lookup"><span data-stu-id="81e4e-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="81e4e-110">Hinnagruppe saab määrata vähemalt ühele järgmisele üksusele: kanalid, kataloogid, alluvused ja püsikliendiprogrammid.</span><span class="sxs-lookup"><span data-stu-id="81e4e-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="81e4e-111">See artikkel käsitleb kanaleid, kuid samad mõisted kehtivad kataloogi allahindlustele, alluvuste allahindlustele ja püsikliendiallahindlustele.</span><span class="sxs-lookup"><span data-stu-id="81e4e-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="81e4e-112">Hinnagrupid</span><span class="sxs-lookup"><span data-stu-id="81e4e-112">Price groups</span></span>

<span data-ttu-id="81e4e-113">[![Hinnagrupid](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="81e4e-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="81e4e-114">Ülalolev joonis illustreerib seost kande võimalike üksuste vahel (kanal, kataloog, alluvus, klient, püsikliendikaart) ja mitmesuguseid allahindluse tüüpe, mida saab konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="81e4e-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="81e4e-115">Kõik kanded tehakse kanalis, seega on kanal kindlasti kandel olemas.</span><span class="sxs-lookup"><span data-stu-id="81e4e-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="81e4e-116">Ülejäänud üksused on valikulised.</span><span class="sxs-lookup"><span data-stu-id="81e4e-116">The remaining entities are optional.</span></span> <span data-ttu-id="81e4e-117">Igal koondandmete lehel on link seotud hinnagruppide lehele, kus saate vaadata ja lisada vajalikke hinnagruppe.</span><span class="sxs-lookup"><span data-stu-id="81e4e-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="81e4e-118">Hinnagruppi kasutatakse nelja tüüpi üksuste seostamiseks allahindluste, hinna korrigeerimiste ja kaubanduslepetega.</span><span class="sxs-lookup"><span data-stu-id="81e4e-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="81e4e-119">Soovitame plaanida strateegia, kuidas hinnagruppe nimetada, et neid korras hoida.</span><span class="sxs-lookup"><span data-stu-id="81e4e-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="81e4e-120">Üks võimalus on kasutada ees või järel tähte või numbrit, et erinevaid tüüpe eristada.</span><span class="sxs-lookup"><span data-stu-id="81e4e-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="81e4e-121">Näiteks 1-xxxxx kanali hinnagruppide puhul ja 2-xxxxx kataloogi hinnagruppide puhul.</span><span class="sxs-lookup"><span data-stu-id="81e4e-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="81e4e-122">Neli päringulehte keskenduvad igale kaubanduse üksusele, millega on seotud allahindlused.</span><span class="sxs-lookup"><span data-stu-id="81e4e-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="81e4e-123">**Kanali hinnagrupid** – sellel lehel on loend kanalitest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="81e4e-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="81e4e-124">**Kataloogi hinnagrupid** – sellel lehel on loend kataloogidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="81e4e-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="81e4e-125">**Püsikliendi hinnagrupid** – sellel lehel on loend püsikliendiprogrammidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="81e4e-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="81e4e-126">**Sidusettevõtete hinnagrupid** – sellel lehel on loend sidusettevõtetest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.</span><span class="sxs-lookup"><span data-stu-id="81e4e-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="81e4e-127">Kanali allahindluse seadistuse näide</span><span class="sxs-lookup"><span data-stu-id="81e4e-127">Example channel discount set up</span></span>

<span data-ttu-id="81e4e-128">Järgmine näide illustreerib kanali allahindluse seadistamiseks vajalikke toiminguid.</span><span class="sxs-lookup"><span data-stu-id="81e4e-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="81e4e-129">Selles näites on kanal nimega **Houston** ja loote uue allahindluse nimega **Tagasi-kooli.**</span><span class="sxs-lookup"><span data-stu-id="81e4e-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="81e4e-130">Kuna hinnakujunduse ja allahindluste strateegia hõlmab kanali allahindluste võimalust, luuakse kanali loomisel alati kanalipõhine hinnagrupp.</span><span class="sxs-lookup"><span data-stu-id="81e4e-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="81e4e-131">Teil on hinnagrupp **Houston-PG** ja see on määratud kanalile **Houston**.</span><span class="sxs-lookup"><span data-stu-id="81e4e-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="81e4e-132">Pärast uue allahindluse **Tagasi-kooli** loomist tuleb klõpsata valikut **Hinnagrupid** lehe **Allahindlus** ülemises osas.</span><span class="sxs-lookup"><span data-stu-id="81e4e-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="81e4e-133">Avaneb leht **Allahindluse hinnagrupid**.</span><span class="sxs-lookup"><span data-stu-id="81e4e-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="81e4e-134">Seejärel klõpsake nuppu **Uus** ja valige hinnagrupp **Houston-PG**.</span><span class="sxs-lookup"><span data-stu-id="81e4e-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="81e4e-135">Nüüd saate allahindluse lubada ja kanalisse suunata.</span><span class="sxs-lookup"><span data-stu-id="81e4e-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81e4e-136">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="81e4e-136">Additional resources</span></span>

[<span data-ttu-id="81e4e-137">Hinnakorrigeerimised ja allahindlused</span><span class="sxs-lookup"><span data-stu-id="81e4e-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
