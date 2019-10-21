---
title: Omnikanali tootesoovituste demoandmed
description: Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi Tier-1 ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225817"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="b68dd-103">Omnikanali tootesoovituste demoandmed</span><span class="sxs-lookup"><span data-stu-id="b68dd-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="b68dd-104">Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi Tier-1 ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="b68dd-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="b68dd-105">Omnikanali tootesoovitused pakuvad keeleliselt või programmiliselt loodud tellitud toodete loendit.</span><span class="sxs-lookup"><span data-stu-id="b68dd-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="b68dd-106">Neid loendeid saab kasutada mitmes stsenaariumis, sõltuvalt ettevõtte vajadusest.</span><span class="sxs-lookup"><span data-stu-id="b68dd-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="b68dd-107">Lisateavet toote soovituste funktsioonide kohta leiate [Tootesoovituste](product-recommendaitons-overview.md) ülevaatest.</span><span class="sxs-lookup"><span data-stu-id="b68dd-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="b68dd-108">Tier-2 ja kõrgema Dynamics Environmentsi tootesoovitused arvutatakse automaatselt kliendi andmetele tuginedes.</span><span class="sxs-lookup"><span data-stu-id="b68dd-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="b68dd-109">Tootesoovituste demoandmte kasutamine ei keela ühtegi tootesoovituste lahendust, mis on juba ette valmistatud keskkonnas ja mis tahes selle kasutusega seotud kulusid.</span><span class="sxs-lookup"><span data-stu-id="b68dd-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="b68dd-110">Tier-1 keskkonna tootesoovitused põhinevad ainult CSV-failis talletatud staatilistel demoandmetel.</span><span class="sxs-lookup"><span data-stu-id="b68dd-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="b68dd-111">Tootesoovituste demoandmete lubamine keskkonnas</span><span class="sxs-lookup"><span data-stu-id="b68dd-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="b68dd-112">Kliendid peavad kasutama **Dynamics 365 CommerceEelvaate demolaiendust** vastavale keskkonnale, mis võimaldab automaatselt tootesoovituste demoandmed.</span><span class="sxs-lookup"><span data-stu-id="b68dd-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="b68dd-113">Vaikedemoandmed</span><span class="sxs-lookup"><span data-stu-id="b68dd-113">Default demo data</span></span>
<span data-ttu-id="b68dd-114">Igas Onebox tüüpi keskkonnas on eellaaditud tootesoovituste komplekti demoandmed, mis on salvestatud komaeraldatud **reco_demo_data.csv** faili, mis asub samas kaustas kui see dokument jaemüügiserveris.</span><span class="sxs-lookup"><span data-stu-id="b68dd-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="b68dd-115">Need andmed on liigendatud järgmiste veergude alusel.</span><span class="sxs-lookup"><span data-stu-id="b68dd-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="b68dd-116">Veeru nimi</span><span class="sxs-lookup"><span data-stu-id="b68dd-116">Column name</span></span>         | <span data-ttu-id="b68dd-117">Kohustuslik</span><span class="sxs-lookup"><span data-stu-id="b68dd-117">Mandatory</span></span>          | <span data-ttu-id="b68dd-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b68dd-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="b68dd-119">Võimalikud väärtused</span><span class="sxs-lookup"><span data-stu-id="b68dd-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b68dd-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="b68dd-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="b68dd-122">Konkreetse tootesoovituse loenditüüp, mida demoandmefail loob.</span><span class="sxs-lookup"><span data-stu-id="b68dd-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="b68dd-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="b68dd-123">RecoBestSelling</span></span></li><li><span data-ttu-id="b68dd-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="b68dd-124">RecoNew</span></span></li><li><span data-ttu-id="b68dd-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="b68dd-125">RecoTrending</span></span></li><li><span data-ttu-id="b68dd-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="b68dd-126">RecoCart</span></span></li><li><span data-ttu-id="b68dd-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="b68dd-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="b68dd-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="b68dd-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="b68dd-130">Konkreetse tööüksuse number, mille puhul eeldatakse tootesoovituste esitamist.</span><span class="sxs-lookup"><span data-stu-id="b68dd-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="b68dd-131">Kategooria</span><span class="sxs-lookup"><span data-stu-id="b68dd-131">Category</span></span>            |                    |    <span data-ttu-id="b68dd-132">Kategooria, mille jaoks tuleks kindel loend tagastada.</span><span class="sxs-lookup"><span data-stu-id="b68dd-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="b68dd-133">Kui kategooriat pole määratud, on loend ainult navigeerimise hierarhia jaoks.</span><span class="sxs-lookup"><span data-stu-id="b68dd-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="b68dd-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="b68dd-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="b68dd-135">Seemneid nõudvate loendite puhul (RecoPeopleAlsoBuy ja RecoCart) peaksid need loendid näitama lisatooteid.</span><span class="sxs-lookup"><span data-stu-id="b68dd-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="b68dd-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="b68dd-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="b68dd-138">Tulemusena tagastatakse üks või mitu toodet, mis eraldatakse **;** abil.</span><span class="sxs-lookup"><span data-stu-id="b68dd-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="b68dd-139">Demoandmete kohandamine</span><span class="sxs-lookup"><span data-stu-id="b68dd-139">Customize demo data</span></span>
<span data-ttu-id="b68dd-140">Kliendid saavad redigeerida vaikimisi demoandmeid mis tahes toote ja kategooria teabega, mis on seadistatud HQ-s.</span><span class="sxs-lookup"><span data-stu-id="b68dd-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="b68dd-141">Pärast CSV uuendamist peegeldavad klientidele tagastatud tootesoovitused kohe muudatusi.</span><span class="sxs-lookup"><span data-stu-id="b68dd-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="b68dd-142">Laiend sisaldab andmefaili, mida nimetatakse RecoMockDataset.csv, mis võimaldab kliendil juhtida andmekogumit, mida kasutatakse proovisoovituste tulemuste mõjutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b68dd-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="b68dd-143">Faili nime saab juhtida laienduse konfiguratsiooni kaudu, kasutades sätet **ext.Recommendations DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="b68dd-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="b68dd-144">See võimaldab klientidel omada mitu kogumit, mida saab hõlpsalt konfiguratsiooni kaudu vahetada.</span><span class="sxs-lookup"><span data-stu-id="b68dd-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="b68dd-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b68dd-145">Additional resources</span></span>

[<span data-ttu-id="b68dd-146">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b68dd-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="b68dd-147">Keskkonna planeerimine</span><span class="sxs-lookup"><span data-stu-id="b68dd-147">Environment planning</span></span>](environment-planning.md)
