---
title: Tootesoovituste lisamine kassas
description: See teema kirjeldab toote soovituste kasutamist müügikohas (POS) seadmel.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48533596c5bdc73dd8c815166e7dde0ca2f3cb4d
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127809"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="3c3ec-103">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="3c3ec-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c3ec-104">Oma sisult on tootesoovitused ümberkujundamise ärirakendus, mis ulatub üle kõik kaubanduse ruumide, et luua rikkaid, kaasavaid ja kohandatud toote avastamise kogemusi.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="3c3ec-105">Selle funktsiooni juurutamiseks POS-is järgige juhiseid [soovituste lisamiseks oma POS-seadmetesse.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="3c3ec-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="3c3ec-106">Lisateavet toote soovituste funktsioonide kohta leiate [toote soovituste ülevaatest.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="3c3ec-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="3c3ec-107">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="3c3ec-107">Scenarios</span></span>

<span data-ttu-id="3c3ec-108">Tootesoovitused on aktiivsed järgmiste kassastsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="3c3ec-109">Need on saadaval pilvekassas või Modern POS-is (MPOS).</span><span class="sxs-lookup"><span data-stu-id="3c3ec-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="3c3ec-110">Lehel **Toote üksikasjad** toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="3c3ec-111">Kui poemüüja läheb varasemate kannete vaatamise käigus erinevate kanalite lõikes lehele **Toote üksikasjad**, soovitab soovituste mootor täiendavaid kaupu, mida tõenäoliselt koos ostetakse.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="3c3ec-112">[![Soovitused lehel Toote üksikasjad](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="3c3ec-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="3c3ec-113">Lehel **Kanne** toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="3c3ec-114">Soovituse mootor pakub kaupu kogu ostukorvis olevate kaupade loendi alusel, mis on sageli koos ostetud.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3c3ec-115">Soovituste kuvamiseks lehel **Kanne** peab jaemüüja muutma Dynamics 365 Commerceis ekraanipaigutust.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3c3ec-116">Juhtelement **Soovitused** tuleb paigutada lehele **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="3c3ec-117">[![Soovitused lehel Kanne](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="3c3ec-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="3c3ec-118">Commerce’i konfigureerimine kassasoovituste kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="3c3ec-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="3c3ec-119">Tootesoovituste seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="3c3ec-120">Veenduge, **et teie teenus on uuendatud 10.0.6 järgule.**</span><span class="sxs-lookup"><span data-stu-id="3c3ec-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="3c3ec-121">Järgige juhiseid, kuidas [lubada toote soovitusi](../commerce/enable-product-recommendations.md) oma ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="3c3ec-122">Valikuline: soovituste kuvamiseks kande ekraanil minge jaotisse **Ekraanipaigutus**, valige ekraanipaigutus, käivitage **Ekraanipaigutuse kujundaja** ja paigutage siis **soovituste juhtelement** vajalikku kohta.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="3c3ec-123">Avage **Kaubanduse parameetrid**, valige **Masinõpe** ja valige **Jah** jaotises **Luba kassasoovitused**.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="3c3ec-124">Soovituste nägemiseks kassal käivitage globaalne konfigureerimistöö **1110**.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="3c3ec-125">Kassa ekraanipaigutuse kujundajas tehtud muudatuste kajastamiseks käivitage kanali konfigureerimistöö **1070**.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="3c3ec-126">Tõrkeotsing, kui tootesoovitused on juba lubatud</span><span class="sxs-lookup"><span data-stu-id="3c3ec-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="3c3ec-127">Liikuge kohta **Commerce’o parameetrid** \> **Soovituste loendid** \> **Keela tootesoovitused** ja käivitage **Globaalne konfigureerimistöö \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="3c3ec-128">Kui olete oma kandekuvale lisanud **soovituste juhtelemendi**, kasutades **ekraanipaigutuse kujundajat**, eemaldage ka see.</span><span class="sxs-lookup"><span data-stu-id="3c3ec-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="3c3ec-129">Kui teil on lisaküsimusi, vaadake teemat [Tootesoovituste KKK](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="3c3ec-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c3ec-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3c3ec-130">Additional resources</span></span>

[<span data-ttu-id="3c3ec-131">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="3c3ec-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="3c3ec-132">ADLS-i lubamine Dynamics 365 Commerce keskkonnas</span><span class="sxs-lookup"><span data-stu-id="3c3ec-132">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="3c3ec-133">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="3c3ec-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="3c3ec-134">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="3c3ec-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="3c3ec-135">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="3c3ec-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="3c3ec-136">Soovitusloendite lisamine e-Kaubanduse saidile</span><span class="sxs-lookup"><span data-stu-id="3c3ec-136">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="3c3ec-137">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="3c3ec-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3c3ec-138">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="3c3ec-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="3c3ec-139">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="3c3ec-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="3c3ec-140">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="3c3ec-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="3c3ec-141">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="3c3ec-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
