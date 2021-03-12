---
title: Uue kaubandusleppe loomine
description: See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e49793fc7f6b3f37bafae05770d4b23d24171329
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974881"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="c9fd8-103">Uue kaubandusleppe loomine</span><span class="sxs-lookup"><span data-stu-id="c9fd8-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9fd8-104">See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="c9fd8-105">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c9fd8-106">Kui kasutate oma andmeid, peate enne selle juhendi käivitamist veenduma, et oleks olemas kaubandusleppe tööleht, kus suvandi Vaikeseos sätteks on valitud „Hind (müük)”.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="c9fd8-107">Uue kaubandusleppe töölehe loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="c9fd8-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="c9fd8-108">Avage **Navigatsioonipaan > Moodulid > Müük ja turundus > Hinnad ja allahindlused > Kaubandusleppe töölehed**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="c9fd8-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-109">Click **New**.</span></span>
3. <span data-ttu-id="c9fd8-110">Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c9fd8-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c9fd8-112">Klõpsake paanil **Toimingupaan** suvandit **Read**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="c9fd8-113">Valige väljal **Konto kood** suvand "Tabel".</span><span class="sxs-lookup"><span data-stu-id="c9fd8-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="c9fd8-114">Selles näites värskendate hinda teatud kliendi puhul, mis tähendab, et peate valima suvandi Tabel.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="c9fd8-115">Kui värskendasite toote hinnakirja, siis valige suvand "Kõik", et uus hind kehtiks kõikide klientide jaoks.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="c9fd8-116">Kui määrasite erinevatele kliendisektoritele erinevad hinnad, siis valige suvand Grupp.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="c9fd8-117">Suvandi Grupp valimiseks peate seadistama kliendi hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="c9fd8-118">Klõpsake väljal **Konto valik** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c9fd8-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="c9fd8-120">Valige väljal **Kaubakood** suvand "Tabel".</span><span class="sxs-lookup"><span data-stu-id="c9fd8-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="c9fd8-121">Kui sisestate kaubandusleppe, mille tüüp on Hind (müük), peate valima väljal **Kaubakood** ainult suvandi "Tabel".</span><span class="sxs-lookup"><span data-stu-id="c9fd8-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="c9fd8-122">Põhjuseks on see, et hind on absoluutväärtus ning ei saa olla kõigi toodete või tootegrupi puhul olla sama.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="c9fd8-123">Klõpsake väljal **Kauba seos** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="c9fd8-124">Valige loendist toode, mille soovite leppesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="c9fd8-125">Märkige üles, millise toote valisite.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="c9fd8-126">Sisestage miinimumkogus väljale **Alates**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="c9fd8-127">Kui klient peab tellima miinimumkoguse, enne kui kvalifitseerub uue hinna saamiseks, peate määrama selle koguse siin.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="c9fd8-128">Sisestage väärtus väljale **Kuni**, et määrata maksimaalne kogus, üle mille leppe hind ei kehti.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="c9fd8-129">Kui pakute hindu ja allahindlusi mitme kogusekatkestuse põhjal, määrake iga koguserühm miinimum- ja maksimumkoguse paarina vastavalt väljadel **Alates** ja **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="c9fd8-130">Sisestage hind väljale **Summa valuutas**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="c9fd8-131">Sisestage jaotise **Üksikasjad** väljale **Alguskuupäev** kuupäev, millest alates see lepe kehtib.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="c9fd8-132">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-132">Click **Save**.</span></span>
16. <span data-ttu-id="c9fd8-133">Klõpsake valikut **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-133">Click **Validate**.</span></span>
17. <span data-ttu-id="c9fd8-134">Klõpsake **Kinnita valitud read**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="c9fd8-135">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-135">Click **OK**.</span></span>
19. <span data-ttu-id="c9fd8-136">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-136">Click **Post**.</span></span>
20. <span data-ttu-id="c9fd8-137">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="c9fd8-138">Toote kaubanduslepete kuvamine</span><span class="sxs-lookup"><span data-stu-id="c9fd8-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="c9fd8-139">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="c9fd8-140">Leidke ja valige loendist toode, mille hinda äsja värskendasite.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="c9fd8-141">Klõpsake paanil **Tegevuspaan** nuppu **Müük**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="c9fd8-142">Klõpsake **Kuva kaubanduslepped**.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="c9fd8-143">Vaadake üle äsjaloodud hinna kaubandusleppe üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="c9fd8-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9fd8-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c9fd8-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="c9fd8-146">Tehniline ülevaade</span><span class="sxs-lookup"><span data-stu-id="c9fd8-146">Whitepaper</span></span>
<span data-ttu-id="c9fd8-147">Lisateabe saamiseks laadige alla järgmine tehniline ülevaade (kirjutatud versiooni AX2012 toetamiseks, kuid kehtib ka rakendusele Dynamics 365 Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="c9fd8-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>
- [<span data-ttu-id="c9fd8-148">Kaubanduslepped</span><span class="sxs-lookup"><span data-stu-id="c9fd8-148">Trade agreements</span></span>](https://mbs.microsoft.com/files/public/CS/AX2012R3/TradeagreementsinAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="c9fd8-149">Kogukonna ajaveebid</span><span class="sxs-lookup"><span data-stu-id="c9fd8-149">Community blogs</span></span>
- [<span data-ttu-id="c9fd8-150">Müügihinnad rakenduses Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c9fd8-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
