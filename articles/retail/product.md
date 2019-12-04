---
title: Tootesoovitused müügikohas
description: See teema kirjeldab toote soovituste kasutamist müügikohas (POS) seadmel.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: 98c84e987c40adf136d0240117f7b0f119bf2f59
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811113"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="148b1-103">Tootesoovitused müügikohas</span><span class="sxs-lookup"><span data-stu-id="148b1-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="148b1-104">Oma sisult on toote soovitused ümberkujundamise ärirakendus, mis ulatub üle kõik jaemüügi ruumide, et luua rikkaid, kaasavaid ja kohandatud toote avastamise kogemusi.</span><span class="sxs-lookup"><span data-stu-id="148b1-104">At its core, product Recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="148b1-105">Selle funktsiooni juurutamiseks POS-is järgige juhiseid [soovituste lisamiseks oma POS-seadmetesse.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="148b1-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="148b1-106">Lisateavet toote soovituste funktsioonide kohta leiate [toote soovituste ülevaatest.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="148b1-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="148b1-107">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="148b1-107">Scenarios</span></span>

<span data-ttu-id="148b1-108">Tootesoovitused on aktiivsed järgmiste kassastsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="148b1-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="148b1-109">Need on saadaval pilvekassas või Modern POS-is (MPOS).</span><span class="sxs-lookup"><span data-stu-id="148b1-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="148b1-110">Lehel **Toote üksikasjad** toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="148b1-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="148b1-111">Kui poemüüja läheb varasemate kannete vaatamise käigus erinevate kanalite lõikes lehele **Toote üksikasjad**, soovitab soovituste mootor täiendavaid kaupu, mida tõenäoliselt koos ostetakse.</span><span class="sxs-lookup"><span data-stu-id="148b1-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="148b1-112">[![Soovitused lehel Toote üksikasjad](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="148b1-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="148b1-113">Lehel **Kanne** toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="148b1-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="148b1-114">Soovituse mootor pakub kaupu kogu ostukorvis olevate kaupade loendi alusel, mis on sageli koos ostetud.</span><span class="sxs-lookup"><span data-stu-id="148b1-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="148b1-115">Soovituste kuvamiseks lehel **Kanne** peab jaemüüja muutma Dynamics 365 for Retailis ekraanipaigutust.</span><span class="sxs-lookup"><span data-stu-id="148b1-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="148b1-116">Juhtelement **Soovitused** tuleb paigutada lehele **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="148b1-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="148b1-117">[![Soovitused lehel Kanne](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="148b1-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a><span data-ttu-id="148b1-118">Dynamics 365 Retaili konfigureerimine kassasoovituste kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="148b1-118">Configure Dynamics 365 Retail to enable POS recommendations</span></span>

<span data-ttu-id="148b1-119">Tootesoovituste seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="148b1-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="148b1-120">Veenduge, **et teie teenus on uuendatud 10.0.6 järgule.**</span><span class="sxs-lookup"><span data-stu-id="148b1-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="148b1-121">Järgige juhiseid, kuidas [lubada toote soovitusi](../commerce/enable-product-recommendations.md) oma ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="148b1-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="148b1-122">Valikuline: soovituste kuvamiseks kande ekraanil minge jaotisse **Ekraanipaigutus**, valige ekraanipaigutus, käivitage **Ekraanipaigutuse kujundaja** ja paigutage siis **soovituste juhtelement** vajalikku kohta.</span><span class="sxs-lookup"><span data-stu-id="148b1-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="148b1-123">Avage **Retaili parameetrid**, valige **Masinõpe** ja valige **Jah** jaotisest **Luba kassasoovitused**.</span><span class="sxs-lookup"><span data-stu-id="148b1-123">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="148b1-124">Soovituste nägemiseks kassal käivitage globaalne konfigureerimistöö **1110**.</span><span class="sxs-lookup"><span data-stu-id="148b1-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="148b1-125">Kassa ekraanipaigutuse kujundajas tehtud muudatuste kajastamiseks käivitage kanali konfigureerimistöö **1070**.</span><span class="sxs-lookup"><span data-stu-id="148b1-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="148b1-126">Tõrkeotsing, kui tootesoovitused on juba lubatud</span><span class="sxs-lookup"><span data-stu-id="148b1-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="148b1-127">Liikuge kohta **Jaemüügi parameetrid** \> **Soovituste loendid** \> **Keela tootesoovitused** ja käivitage **Globaalne konfigureerimistöö \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="148b1-127">Navigate to **Retail Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="148b1-128">Kui olete oma kandekuvale lisanud **soovituste juhtelemendi**, kasutades **ekraanipaigutuse kujundajat**, eemaldage ka see.</span><span class="sxs-lookup"><span data-stu-id="148b1-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="148b1-129">Kui teil on lisaküsimusi, vaadake teemat [Tootesoovituste KKK](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="148b1-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="148b1-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="148b1-130">Additional resources</span></span>

[<span data-ttu-id="148b1-131">Soovituste juhtelemendi lisamine kassaseadmete kandekuvale</span><span class="sxs-lookup"><span data-stu-id="148b1-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="148b1-132">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="148b1-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="148b1-133">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="148b1-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 