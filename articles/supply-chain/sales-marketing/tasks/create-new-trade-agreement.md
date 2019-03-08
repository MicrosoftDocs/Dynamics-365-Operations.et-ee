---
title: Uue kaubandusleppe loomine
description: See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "323498"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="05799-103">Uue kaubandusleppe loomine</span><span class="sxs-lookup"><span data-stu-id="05799-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05799-104">See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud.</span><span class="sxs-lookup"><span data-stu-id="05799-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="05799-105">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="05799-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="05799-106">Kui kasutate oma andmeid, peate enne selle juhendi käivitamist veenduma, et oleks olemas kaubandusleppe tööleht, kus suvandi Vaikeseos sätteks on valitud Hind (müük).</span><span class="sxs-lookup"><span data-stu-id="05799-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="05799-107">Uue kaubandusleppe töölehe loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="05799-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="05799-108">Avage Müük ja turundus > Hinnad ja allahindlused > Kaubandusleppe töölehed.</span><span class="sxs-lookup"><span data-stu-id="05799-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="05799-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="05799-109">Click New.</span></span>
3. <span data-ttu-id="05799-110">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="05799-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="05799-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="05799-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="05799-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="05799-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="05799-113">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="05799-113">Click Lines.</span></span>
7. <span data-ttu-id="05799-114">Valige väljal Konto kood suvand Tabel.</span><span class="sxs-lookup"><span data-stu-id="05799-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="05799-115">Selles näites värskendate hinda teatud kliendi puhul, mis tähendab, et peate valima suvandi Tabel.</span><span class="sxs-lookup"><span data-stu-id="05799-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="05799-116">Kui värskendasite toote hinnakirja, siis valige suvand Kõik, et uus hind kehtiks kõikide klientide jaoks.</span><span class="sxs-lookup"><span data-stu-id="05799-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="05799-117">Kui määrasite erinevatele kliendisektoritele erinevad hinnad, siis valige suvand Grupp.</span><span class="sxs-lookup"><span data-stu-id="05799-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="05799-118">Suvandi Grupp valimiseks peate seadistama kliendi hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="05799-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="05799-119">Klõpsake väljal Konto valik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="05799-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="05799-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="05799-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="05799-121">Valige väljal Kaubakood suvand Tabel.</span><span class="sxs-lookup"><span data-stu-id="05799-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="05799-122">Kui sisestate kaubandusleppe, mille tüüp on Hind (müük), peate valima kaubakoodi väljal ainult suvandi Tabel.</span><span class="sxs-lookup"><span data-stu-id="05799-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="05799-123">Põhjuseks on see, et hind on absoluutväärtus ning ei saa olla kõigi toodete või tootegrupi puhul olla sama.</span><span class="sxs-lookup"><span data-stu-id="05799-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="05799-124">Klõpsake väljal Kauba seos otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="05799-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="05799-125">Valige loendist toode, mille soovite leppesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="05799-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="05799-126">Märkige üles, millise toote valisite.</span><span class="sxs-lookup"><span data-stu-id="05799-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="05799-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="05799-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="05799-128">Sisestage miinimumkogus väljale Alates.</span><span class="sxs-lookup"><span data-stu-id="05799-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="05799-129">Kui klient peab tellima miinimumkoguse, enne kui kvalifitseerub uue hinna saamiseks, peate määrama selle koguse siin.</span><span class="sxs-lookup"><span data-stu-id="05799-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="05799-130">Sisestage väärtus väljale Kuni, et määrata maksimaalne kogus, üle mille leppe hind ei kehti.</span><span class="sxs-lookup"><span data-stu-id="05799-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="05799-131">Kui pakute hindu ja allahindlusi mitme kogusekatkestuse põhjal, määrake iga koguserühm miinimum- ja maksimumkoguse paarina vastavalt väljadel Alates ja Kuni.</span><span class="sxs-lookup"><span data-stu-id="05799-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="05799-132">Sisestage hind väljale Summa valuutas.</span><span class="sxs-lookup"><span data-stu-id="05799-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="05799-133">Sisestage väljale Alates kuupäev, millest alates see lepe kehtib.</span><span class="sxs-lookup"><span data-stu-id="05799-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="05799-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="05799-134">Click Save.</span></span>
18. <span data-ttu-id="05799-135">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="05799-135">Click Validate.</span></span>
19. <span data-ttu-id="05799-136">Klõpsake suvandit Kinnita valitud read.</span><span class="sxs-lookup"><span data-stu-id="05799-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="05799-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="05799-137">Click OK.</span></span>
21. <span data-ttu-id="05799-138">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="05799-138">Click Post.</span></span>
22. <span data-ttu-id="05799-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="05799-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="05799-140">Toote kaubanduslepete kuvamine</span><span class="sxs-lookup"><span data-stu-id="05799-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="05799-141">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="05799-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="05799-142">Leidke ja valige loendist toode, mille hinda äsja värskendasite.</span><span class="sxs-lookup"><span data-stu-id="05799-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="05799-143">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="05799-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="05799-144">Klõpsake suvandit Kuva kaubanduslepped.</span><span class="sxs-lookup"><span data-stu-id="05799-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="05799-145">Vaadake üle äsjaloodud hinna kaubandusleppe üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="05799-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="05799-146">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="05799-146">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05799-147">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="05799-147">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="05799-148">Kogukonna ajaveebid</span><span class="sxs-lookup"><span data-stu-id="05799-148">Community blogs</span></span>
- [<span data-ttu-id="05799-149">Müügihinnad rakenduses Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="05799-149">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
