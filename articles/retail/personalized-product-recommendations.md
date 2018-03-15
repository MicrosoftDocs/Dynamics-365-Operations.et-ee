---
title: "Isikupärastatud tootesoovituste ülevaade"
description: "See teema hõlmab teavet Dynamics 365 for Retaili tootesoovituste kohta, mida saab kassaseadmes kuvada."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 16bdf2176869e5822ddf8732c829b65f1e60632c
ms.openlocfilehash: ce91f675082a34bd5a1e88be7a7af6884dc47add
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="1b648-103">Isikupärastatud tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="1b648-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="1b648-104">Eemaldame tootesoovitusteenuse praeguse versiooni kuniks me seda funktsiooni parema algoritmi ja uuemate jaemüügile suunatud võimalustega täiustame.</span><span class="sxs-lookup"><span data-stu-id="1b648-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="1b648-105">Lisateavet vt teemast [Eemaldatud või aegunud funktsioonid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="1b648-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="1b648-106">Microsoft Dynamics 365 for Retailis saab tootesoovitused kuvada kassa (POS) seadmes.</span><span class="sxs-lookup"><span data-stu-id="1b648-106">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="1b648-107">Soovitused on kaubad, millest klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda.</span><span class="sxs-lookup"><span data-stu-id="1b648-107">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="1b648-108">Suurte kataloogidega jaemüüjate puhul aitavad soovitused kliendil tooteid avastada.</span><span class="sxs-lookup"><span data-stu-id="1b648-108">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="1b648-109">Näidates tooteid, mis on suunatud kliendi huvidele ja ostuharjumustele, võivad tootesoovitused aidata jaemüüjatel lisamüüki ning ristmüüki teha ja klienti hoida.</span><span class="sxs-lookup"><span data-stu-id="1b648-109">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="1b648-110">Rakenduses Dynamics 365 for Retail toimivad jaemüügi tootesoovitused kognitiivsete teenuste ja Microsoft Azure’i masinõppe abil.</span><span class="sxs-lookup"><span data-stu-id="1b648-110">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="1b648-111">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="1b648-111">Scenarios</span></span>
---------

<span data-ttu-id="1b648-112">Tootesoovitused on aktiivsed järgmiste kassastsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="1b648-112">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="1b648-113">Need on saadaval pilvekassas või Modern POS-is (MPOS).</span><span class="sxs-lookup"><span data-stu-id="1b648-113">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="1b648-114">Lehel **Toote üksikasjad** toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="1b648-114">On the **Product details** page:</span></span>

-   <span data-ttu-id="1b648-115">Kui poemüüja läheb varasemate kannete vaatamise käigus erinevate kanalite lõikes lehele **Toote üksikasjad**, soovitab soovituste mootor täiendavaid kaupu, mida tõenäoliselt koos ostetakse.</span><span class="sxs-lookup"><span data-stu-id="1b648-115">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="1b648-116">Kui poemüüja lisab kandele kliendi ja läheb siis lehele **Toote üksikasjad**, edastab soovituste mootor kliendi kannete ajaloo põhjal isikupärastatud soovitusi.</span><span class="sxs-lookup"><span data-stu-id="1b648-116">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="1b648-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="1b648-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="1b648-118">Lehel **Kanne** toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="1b648-118">On the **Transaction** page:</span></span>

-   <span data-ttu-id="1b648-119">Soovituste mootor soovitab kaupu kogu ostukorvis oleva kaupade loendi alusel.</span><span class="sxs-lookup"><span data-stu-id="1b648-119">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="1b648-120">Kui poemüüja lisab kandele kliendi, edastab soovituste mootor kliendi kannete ajaloo ja ostukorvis olevate kaupade põhjal isiklikke soovitusi.</span><span class="sxs-lookup"><span data-stu-id="1b648-120">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="1b648-121">Soovituste kuvamiseks lehel **Kanne** peab jaemüüja muutma Dynamics 365 for Retailis ekraani paigutust.</span><span class="sxs-lookup"><span data-stu-id="1b648-121">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="1b648-122">Juhtelement **Soovitused** tuleb paigutada lehele **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="1b648-122">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="1b648-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="1b648-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="1b648-124">Lehel **Kliendi üksikasjad** toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="1b648-124">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="1b648-125">Soovituste mootor soovitab kaupu kasutaja ID ja kliendi sooviloendis olevate kaupade alusel.</span><span class="sxs-lookup"><span data-stu-id="1b648-125">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="1b648-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="1b648-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="1b648-127">Microsoft Dynamics 365 for Retaili konfigureerimine kassasoovituste lubamiseks</span><span class="sxs-lookup"><span data-stu-id="1b648-127">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="1b648-128">Tootesoovituste seadistamiseks tuleb teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="1b648-128">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="1b648-129">Veenduge, et oleks valitud õige **juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="1b648-129">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="1b648-130">Avage jaotis **Üksuse kauplus**, valige **Jaekaubandus** ja seejärel klõpsake käsku **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="1b648-130">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="1b648-131">See kasutab teie tegevuse andmebaasis olevaid demoandmeid (või teie andmeid) ja teisaldab need üksuse kauplusesse.</span><span class="sxs-lookup"><span data-stu-id="1b648-131">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="1b648-132">Valikuline: soovituste kuvamiseks kande ekraanil minge jaotisse **Ekraanipaigutus**, valige ekraanipaigutus, käivitage **Ekraanipaigutuse kujundaja** ja paigutage siis **soovituste juhtelement** vajalikku kohta.</span><span class="sxs-lookup"><span data-stu-id="1b648-132">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="1b648-133">Avage **Retaili parameetrid**, valige **Masinõpe** ja valige **Jah** jaotisest **Luba kassasoovitused**.</span><span class="sxs-lookup"><span data-stu-id="1b648-133">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="1b648-134">Soovituste nägemiseks kassal käivitage globaalne konfigureerimistöö **1110**.</span><span class="sxs-lookup"><span data-stu-id="1b648-134">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="1b648-135">Kassa ekraanipaigutuse kujundajas tehtud muudatuste kajastamiseks käivitage kanali konfigureerimistöö **1070**.</span><span class="sxs-lookup"><span data-stu-id="1b648-135">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="1b648-136">[]()Kuidas see käib?</span><span class="sxs-lookup"><span data-stu-id="1b648-136">[]()How does it work?</span></span>
<span data-ttu-id="1b648-137">Valiku **Üksuse kauplus** värskendamisel toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1b648-137">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="1b648-138">Kognitiivsete teenuste nõutavas vormingus andmed ekstraktitakse Microsoft Dynamics 365 for Retaili tegevuse andmebaasist ja saadetakse üksuse kauplusse.</span><span class="sxs-lookup"><span data-stu-id="1b648-138">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="1b648-139">Azure Data Factory (ADF) kasutab neid andmeid andmete puhastamiseks Hive’i skriptide abil ADF-tegevuste käigus.</span><span class="sxs-lookup"><span data-stu-id="1b648-139">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="1b648-140">Puhastatud andmed salvestatakse bloobimällu.</span><span class="sxs-lookup"><span data-stu-id="1b648-140">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="1b648-141">Bloobimälust võetud andmeid kasutab kognitiivsete teenuste API soovitusmudeli väljaõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="1b648-141">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="1b648-142">Kui lülitate valiku **Luba soovitused** sisse ja käivitate konfigureerimistööd, siis toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1b648-142">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="1b648-143">API-st võetakse mudeli identimisteave ja ID ning need salvestatakse Dynamics 365 for Retaili tegevuse andmebaasi, AOS-i web.config-faili ja samuti jaemüügiserverisse.</span><span class="sxs-lookup"><span data-stu-id="1b648-143">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="1b648-144">CRT-le tehakse kättesaadavaks mudeli identimisteave ja ID, et saaks arvestada pilvekassa ja MPOS-i tootesoovituste kutseid veebirežiimis.</span><span class="sxs-lookup"><span data-stu-id="1b648-144">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="1b648-145">Vt ka</span><span class="sxs-lookup"><span data-stu-id="1b648-145">See also</span></span>
--------

[<span data-ttu-id="1b648-146">Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele</span><span class="sxs-lookup"><span data-stu-id="1b648-146">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




