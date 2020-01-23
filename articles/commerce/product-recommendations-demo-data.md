---
title: Tootesoovituste hankimine demoandmeid kasutades
description: Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi esimese järgu ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697930"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="5fb48-103">Tootesoovituste hankimine demoandmeid kasutades</span><span class="sxs-lookup"><span data-stu-id="5fb48-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="5fb48-104">Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi esimese järgu ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="5fb48-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="5fb48-105">Omnikanali tootesoovitused pakuvad komplekti toimetuslikult kureeritud või programmiliselt loodud toodete loendit.</span><span class="sxs-lookup"><span data-stu-id="5fb48-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="5fb48-106">Neid loendeid saab kasutada mitmes stsenaariumis, sõltuvalt ettevõtte vajadusest.</span><span class="sxs-lookup"><span data-stu-id="5fb48-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="5fb48-107">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5fb48-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="5fb48-108">Teise järgu ja kõrgemate rakenduse Dynamics 365 keskkondade tootesoovitused arvutatakse automaatselt kliendi andmetele tuginedes.</span><span class="sxs-lookup"><span data-stu-id="5fb48-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="5fb48-109">Tootesoovituste demoandmte kasutamine ei keela ühtegi tootesoovituste lahendust, mis on juba ette valmistatud keskkonnas ja mis tahes selle kasutusega seotud kulusid.</span><span class="sxs-lookup"><span data-stu-id="5fb48-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="5fb48-110">Esimese järgu keskkonna tootesoovitused põhinevad ainult CSV-failis talletatud staatilistel demoandmetel.</span><span class="sxs-lookup"><span data-stu-id="5fb48-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="5fb48-111">Tootesoovituste demoandmete lubamine keskkonnas</span><span class="sxs-lookup"><span data-stu-id="5fb48-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="5fb48-112">Tootesoovituste demoandmete lubamiseks peate juurutama rakenduse Dynamics 365 Commerce demolaienduse eelvaate vastavate keskkondadega.</span><span class="sxs-lookup"><span data-stu-id="5fb48-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="5fb48-113">See lubab automaatselt tootesoovituste demoandmed.</span><span class="sxs-lookup"><span data-stu-id="5fb48-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="5fb48-114">Vaikedemoandmed</span><span class="sxs-lookup"><span data-stu-id="5fb48-114">Default demo data</span></span>
<span data-ttu-id="5fb48-115">Igas Onebox tüüpi keskkonnas on eellaaditud tootesoovituste komplekti demoandmed, mis on salvestatud komaeraldatud reco_demo_data.csv faili, mis asub jaemüügiserveris.</span><span class="sxs-lookup"><span data-stu-id="5fb48-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Retail Server.</span></span>

<span data-ttu-id="5fb48-116">Need andmed on liigendatud järgmiste veergude alusel.</span><span class="sxs-lookup"><span data-stu-id="5fb48-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="5fb48-117">Veeru nimi</span><span class="sxs-lookup"><span data-stu-id="5fb48-117">Column name</span></span>         | <span data-ttu-id="5fb48-118">Kohustuslik</span><span class="sxs-lookup"><span data-stu-id="5fb48-118">Mandatory</span></span>          | <span data-ttu-id="5fb48-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5fb48-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="5fb48-120">Võimalikud väärtused</span><span class="sxs-lookup"><span data-stu-id="5fb48-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5fb48-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="5fb48-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="5fb48-123">Konkreetse tootesoovituse loenditüüp, mille demoandmefail loob.</span><span class="sxs-lookup"><span data-stu-id="5fb48-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="5fb48-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="5fb48-124">RecoBestSelling</span></span></li><li><span data-ttu-id="5fb48-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="5fb48-125">RecoNew</span></span></li><li><span data-ttu-id="5fb48-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="5fb48-126">RecoTrending</span></span></li><li><span data-ttu-id="5fb48-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="5fb48-127">RecoCart</span></span></li><li><span data-ttu-id="5fb48-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="5fb48-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="5fb48-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="5fb48-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="5fb48-131">Konkreetse tööüksuse number, mille puhul eeldatakse tootesoovituste esitamist.</span><span class="sxs-lookup"><span data-stu-id="5fb48-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="5fb48-132">Kategooria</span><span class="sxs-lookup"><span data-stu-id="5fb48-132">Category</span></span>            |                    |    <span data-ttu-id="5fb48-133">Kategooria, mille jaoks tuleks kindel loend tagastada.</span><span class="sxs-lookup"><span data-stu-id="5fb48-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="5fb48-134">Kui kategooriat pole määratud, on loend ainult navigeerimise hierarhia tipu jaoks.</span><span class="sxs-lookup"><span data-stu-id="5fb48-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="5fb48-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="5fb48-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="5fb48-136">Lähteväärtusi nõudvate loendite puhul (RecoPeopleAlsoBuy ja RecoCart) peaksid need loendid näitama lisatooteid.</span><span class="sxs-lookup"><span data-stu-id="5fb48-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="5fb48-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="5fb48-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="5fb48-139">Tulemusena tagastatakse üks või mitu toodet, mis eraldatakse ; abil.</span><span class="sxs-lookup"><span data-stu-id="5fb48-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="5fb48-140">Demoandmete kohandamine</span><span class="sxs-lookup"><span data-stu-id="5fb48-140">Customize demo data</span></span>
<span data-ttu-id="5fb48-141">Saate redigeerida vaikimisi demoandmeid mis tahes toote ja kategooria teabega, mis on seadistatud HQ-s.</span><span class="sxs-lookup"><span data-stu-id="5fb48-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="5fb48-142">Pärast CSV-faili värskendamist peegeldavad klientidele tagastatud tootesoovitused kohe muudatusi.</span><span class="sxs-lookup"><span data-stu-id="5fb48-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="5fb48-143">Laiend sisaldab andmefaili, mida nimetatakse RecoMockDataset.csv, mis võimaldab teil juhtida andmekogumit, mida kasutatakse proovisoovituste tulemuste mõjutamiseks.</span><span class="sxs-lookup"><span data-stu-id="5fb48-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="5fb48-144">Faili nime saab juhtida laienduse konfiguratsiooni kaudu, kasutades sätet **ext.Recommendations DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="5fb48-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="5fb48-145">See võimaldab teil omada mitu kogumit, mida saab hõlpsalt konfiguratsiooni kaudu vahetada.</span><span class="sxs-lookup"><span data-stu-id="5fb48-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="5fb48-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5fb48-146">Additional Resources</span></span>

[<span data-ttu-id="5fb48-147">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="5fb48-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="5fb48-148">Keskkonna planeerimine</span><span class="sxs-lookup"><span data-stu-id="5fb48-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)