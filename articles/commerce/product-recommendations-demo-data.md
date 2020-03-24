---
title: Soovituste loomine demoandmetega
description: Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi esimese järgu ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2e790d78b4d5216822ffda3a3895feb674876bd8
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127832"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="d5a8d-103">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="d5a8d-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5a8d-104">Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi esimese järgu ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="d5a8d-105">Omnikanali tootesoovitused pakuvad komplekti toimetuslikult kureeritud või programmiliselt loodud toodete loendit.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="d5a8d-106">Neid loendeid saab kasutada mitmes stsenaariumis, sõltuvalt ettevõtte vajadusest.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="d5a8d-107">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d5a8d-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="d5a8d-108">Teise järgu ja kõrgemate rakenduse Dynamics 365 keskkondade tootesoovitused arvutatakse automaatselt kliendi andmetele tuginedes.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="d5a8d-109">Tootesoovituste demoandmte kasutamine ei keela ühtegi tootesoovituste lahendust, mis on juba ette valmistatud keskkonnas ja mis tahes selle kasutusega seotud kulusid.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="d5a8d-110">Esimese järgu keskkonna tootesoovitused põhinevad ainult CSV-failis talletatud staatilistel demoandmetel.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="d5a8d-111">Tootesoovituste demoandmete lubamine keskkonnas</span><span class="sxs-lookup"><span data-stu-id="d5a8d-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="d5a8d-112">Tootesoovituste demoandmete lubamiseks peate juurutama rakenduse Dynamics 365 Commerce demolaienduse eelvaate vastavate keskkondadega.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="d5a8d-113">See lubab automaatselt tootesoovituste demoandmed.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="d5a8d-114">Vaikedemoandmed</span><span class="sxs-lookup"><span data-stu-id="d5a8d-114">Default demo data</span></span>
<span data-ttu-id="d5a8d-115">Igas Oneboxi tüüpi keskkonnas on eellaaditud tootesoovituste komplekti demoandmed, mis on salvestatud komaeraldatud „reco_demo_data.csv” faili, mis asub Commerce Scale Unitis.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="d5a8d-116">Need andmed on liigendatud järgmiste veergude alusel.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="d5a8d-117">Veeru nimi</span><span class="sxs-lookup"><span data-stu-id="d5a8d-117">Column name</span></span>         | <span data-ttu-id="d5a8d-118">Kohustuslik</span><span class="sxs-lookup"><span data-stu-id="d5a8d-118">Mandatory</span></span>          | <span data-ttu-id="d5a8d-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d5a8d-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="d5a8d-120">Võimalikud väärtused</span><span class="sxs-lookup"><span data-stu-id="d5a8d-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d5a8d-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="d5a8d-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="d5a8d-123">Konkreetse tootesoovituse loenditüüp, mille demoandmefail loob.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="d5a8d-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="d5a8d-124">RecoBestSelling</span></span></li><li><span data-ttu-id="d5a8d-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="d5a8d-125">RecoNew</span></span></li><li><span data-ttu-id="d5a8d-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="d5a8d-126">RecoTrending</span></span></li><li><span data-ttu-id="d5a8d-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="d5a8d-127">RecoCart</span></span></li><li><span data-ttu-id="d5a8d-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="d5a8d-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="d5a8d-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="d5a8d-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="d5a8d-131">Konkreetse tööüksuse number, mille puhul eeldatakse tootesoovituste esitamist.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="d5a8d-132">Kategooria</span><span class="sxs-lookup"><span data-stu-id="d5a8d-132">Category</span></span>            |                    |    <span data-ttu-id="d5a8d-133">Kategooria, mille jaoks tuleks kindel loend tagastada.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="d5a8d-134">Kui kategooriat pole määratud, on loend ainult navigeerimise hierarhia tipu jaoks.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="d5a8d-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="d5a8d-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="d5a8d-136">Lähteväärtusi nõudvate loendite puhul (RecoPeopleAlsoBuy ja RecoCart) peaksid need loendid näitama lisatooteid.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="d5a8d-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d5a8d-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="d5a8d-139">Tulemusena tagastatakse üks või mitu toodet, mis eraldatakse ; abil.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-139">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="d5a8d-140">Demoandmete kohandamine</span><span class="sxs-lookup"><span data-stu-id="d5a8d-140">Customize demo data</span></span>
<span data-ttu-id="d5a8d-141">Saate redigeerida vaikimisi demoandmeid mis tahes toote ja kategooria teabega, mis on seadistatud HQ-s.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="d5a8d-142">Pärast CSV-faili värskendamist peegeldavad klientidele tagastatud tootesoovitused kohe muudatusi.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="d5a8d-143">Laiend sisaldab andmefaili, mida nimetatakse RecoMockDataset.csv, mis võimaldab teil juhtida andmekogumit, mida kasutatakse proovisoovituste tulemuste mõjutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="d5a8d-144">Faili nime saab juhtida laienduse konfiguratsiooni kaudu, kasutades sätet **ext.Recommendations DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="d5a8d-145">See võimaldab teil omada mitu kogumit, mida saab hõlpsalt konfiguratsiooni kaudu vahetada.</span><span class="sxs-lookup"><span data-stu-id="d5a8d-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="d5a8d-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d5a8d-146">Additional Resources</span></span>

[<span data-ttu-id="d5a8d-147">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="d5a8d-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d5a8d-148">ADLS-i lubamine Dynamics 365 Commerce keskkonnas</span><span class="sxs-lookup"><span data-stu-id="d5a8d-148">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d5a8d-149">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="d5a8d-149">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d5a8d-150">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="d5a8d-150">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d5a8d-151">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="d5a8d-151">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d5a8d-152">Soovitusloendite lisamine e-Kaubanduse saidile</span><span class="sxs-lookup"><span data-stu-id="d5a8d-152">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="d5a8d-153">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="d5a8d-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d5a8d-154">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="d5a8d-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d5a8d-155">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="d5a8d-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d5a8d-156">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="d5a8d-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d5a8d-157">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="d5a8d-157">Product recommendations FAQ</span></span>](faq-recommendations.md)
