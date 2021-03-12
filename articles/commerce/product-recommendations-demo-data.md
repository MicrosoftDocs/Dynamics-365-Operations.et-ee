---
title: Soovituste loomine demoandmetega
description: Selle teema eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi esimese järgu ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7ccb0b6c5aace0fc76c6886299fba7369abed860
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972357"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="c2e7b-103">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="c2e7b-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c2e7b-104">Selle teema eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi esimese järgu ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="c2e7b-105">Omnikanali tootesoovitused pakuvad komplekti toimetuslikult kureeritud või programmiliselt loodud toodete loendit.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="c2e7b-106">Neid loendeid saab kasutada mitmes stsenaariumis, sõltuvalt ettevõtte vajadusest.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="c2e7b-107">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c2e7b-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="c2e7b-108">Teise järgu ja kõrgemate rakenduse Dynamics 365 keskkondade tootesoovitused arvutatakse automaatselt kliendi andmetele tuginedes.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="c2e7b-109">Tootesoovituste demoandmte kasutamine ei keela ühtegi tootesoovituste lahendust, mis on juba ette valmistatud keskkonnas ja mis tahes selle kasutusega seotud kulusid.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="c2e7b-110">Esimese järgu keskkonna tootesoovitused põhinevad ainult CSV-failis talletatud staatilistel demoandmetel.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="c2e7b-111">Tootesoovituste demoandmete lubamine keskkonnas</span><span class="sxs-lookup"><span data-stu-id="c2e7b-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="c2e7b-112">Tootesoovituste demoandmete lubamiseks peate juurutama rakenduse Dynamics 365 Commerce demolaienduse eelvaate vastavate keskkondadega.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="c2e7b-113">See lubab automaatselt tootesoovituste demoandmed.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="c2e7b-114">Vaikedemoandmed</span><span class="sxs-lookup"><span data-stu-id="c2e7b-114">Default demo data</span></span>
<span data-ttu-id="c2e7b-115">Igas OneBoxi tüüpi keskkonnas on eellaaditud tootesoovituste komplekti demoandmed, mis on salvestatud komaeraldatud „reco_demo_data.csv” faili, mis asub Commerce Scale Unitis.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="c2e7b-116">Need andmed on liigendatud järgmiste veergude alusel.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="c2e7b-117">Veeru nimi</span><span class="sxs-lookup"><span data-stu-id="c2e7b-117">Column name</span></span>         | <span data-ttu-id="c2e7b-118">Kohustuslik</span><span class="sxs-lookup"><span data-stu-id="c2e7b-118">Mandatory</span></span>          | <span data-ttu-id="c2e7b-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c2e7b-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="c2e7b-120">Võimalikud väärtused</span><span class="sxs-lookup"><span data-stu-id="c2e7b-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c2e7b-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="c2e7b-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="c2e7b-123">Konkreetse tootesoovituse loenditüüp, mille demoandmefail loob.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="c2e7b-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="c2e7b-124">RecoBestSelling</span></span></li><li><span data-ttu-id="c2e7b-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="c2e7b-125">RecoNew</span></span></li><li><span data-ttu-id="c2e7b-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="c2e7b-126">RecoTrending</span></span></li><li><span data-ttu-id="c2e7b-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="c2e7b-127">RecoCart</span></span></li><li><span data-ttu-id="c2e7b-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="c2e7b-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="c2e7b-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="c2e7b-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="c2e7b-131">Konkreetse tööüksuse number, mille puhul eeldatakse tootesoovituste esitamist.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="c2e7b-132">Kategooria</span><span class="sxs-lookup"><span data-stu-id="c2e7b-132">Category</span></span>            |                    |    <span data-ttu-id="c2e7b-133">Kategooria, mille jaoks tuleks kindel loend tagastada.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="c2e7b-134">Kui kategooriat pole määratud, on loend ainult navigeerimise hierarhia tipu jaoks.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="c2e7b-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="c2e7b-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="c2e7b-136">Lähteväärtusi nõudvate loendite puhul (RecoPeopleAlsoBuy ja RecoCart) peaksid need loendid näitama lisatooteid.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="c2e7b-137">CustomerId</span><span class="sxs-lookup"><span data-stu-id="c2e7b-137">CustomerId</span></span>          |                    |    <span data-ttu-id="c2e7b-138">Loenditele, mis nõuavad kliendi identifikaatorit (RecoPicks).</span><span class="sxs-lookup"><span data-stu-id="c2e7b-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="c2e7b-139">Vaikimisi väärtus 0 rakendub kõigile klientidele.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="c2e7b-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="c2e7b-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="c2e7b-142">Tulemusena tagastatakse üks või mitu toodet, mis eraldatakse ; abil.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="c2e7b-143">Demoandmete kohandamine</span><span class="sxs-lookup"><span data-stu-id="c2e7b-143">Customize demo data</span></span>
<span data-ttu-id="c2e7b-144">Saate redigeerida vaikimisi demoandmeid mis tahes toote ja kategooria teabega, mis on seadistatud HQ-s.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="c2e7b-145">Pärast CSV-faili värskendamist peegeldavad klientidele tagastatud tootesoovitused kohe muudatusi.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="c2e7b-146">Laiend sisaldab andmefaili, mida nimetatakse RecoMockDataset.csv, mis võimaldab teil juhtida andmekogumit, mida kasutatakse proovisoovituste tulemuste mõjutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="c2e7b-147">Faili nime saab juhtida laienduse konfiguratsiooni kaudu, kasutades sätet **ext.Recommendations DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="c2e7b-148">See võimaldab teil omada mitu kogumit, mida saab hõlpsalt konfiguratsiooni kaudu vahetada.</span><span class="sxs-lookup"><span data-stu-id="c2e7b-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="c2e7b-149">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c2e7b-149">Additional resources</span></span>

[<span data-ttu-id="c2e7b-150">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="c2e7b-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c2e7b-151">Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="c2e7b-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="c2e7b-152">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="c2e7b-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c2e7b-153">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="c2e7b-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="c2e7b-154">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="c2e7b-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="c2e7b-155">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="c2e7b-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="c2e7b-156">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="c2e7b-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="c2e7b-157">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="c2e7b-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="c2e7b-158">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="c2e7b-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c2e7b-159">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="c2e7b-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c2e7b-160">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="c2e7b-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
