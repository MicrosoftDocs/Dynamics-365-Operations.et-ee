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
ms.openlocfilehash: 6abac72b7530dc7b82c8e95faebdce791cf7dbd1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003230"
---
# <a name="get-product-recommendations-using-demo-data"></a>Tootesoovituste hankimine demoandmeid kasutades
Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi esimese järgu ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.

Omnikanali tootesoovitused pakuvad komplekti toimetuslikult kureeritud või programmiliselt loodud toodete loendit. Neid loendeid saab kasutada mitmes stsenaariumis, sõltuvalt ettevõtte vajadusest. Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).

Teise järgu ja kõrgemate rakenduse Dynamics 365 keskkondade tootesoovitused arvutatakse automaatselt kliendi andmetele tuginedes. Tootesoovituste demoandmte kasutamine ei keela ühtegi tootesoovituste lahendust, mis on juba ette valmistatud keskkonnas ja mis tahes selle kasutusega seotud kulusid.

Esimese järgu keskkonna tootesoovitused põhinevad ainult CSV-failis talletatud staatilistel demoandmetel.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Tootesoovituste demoandmete lubamine keskkonnas
Tootesoovituste demoandmete lubamiseks peate juurutama rakenduse Dynamics 365 Commerce demolaienduse eelvaate vastavate keskkondadega. See lubab automaatselt tootesoovituste demoandmed.

## <a name="default-demo-data"></a>Vaikedemoandmed
Igas Oneboxi tüüpi keskkonnas on eellaaditud tootesoovituste komplekti demoandmed, mis on salvestatud komaeraldatud reco_demo_data.csv faili, mis asub Commerce’i skaala üksuses.

Need andmed on liigendatud järgmiste veergude alusel.

| Veeru nimi         | Kohustuslik          | Kirjeldus                                                                                                                                 | Võimalikud väärtused                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkreetse tootesoovituse loenditüüp, mille demoandmefail loob.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Konkreetse tööüksuse number, mille puhul eeldatakse tootesoovituste esitamist.                                        |                                                                              |
| Kategooria            |                    |    Kategooria, mille jaoks tuleks kindel loend tagastada. Kui kategooriat pole määratud, on loend ainult navigeerimise hierarhia tipu jaoks.    |                                                                              |
| SeedItemId          |                    |    Lähteväärtusi nõudvate loendite puhul (RecoPeopleAlsoBuy ja RecoCart) peaksid need loendid näitama lisatooteid.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Tulemusena tagastatakse üks või mitu toodet, mis eraldatakse ; abil.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Demoandmete kohandamine
Saate redigeerida vaikimisi demoandmeid mis tahes toote ja kategooria teabega, mis on seadistatud HQ-s. Pärast CSV-faili värskendamist peegeldavad klientidele tagastatud tootesoovitused kohe muudatusi.

Laiend sisaldab andmefaili, mida nimetatakse RecoMockDataset.csv, mis võimaldab teil juhtida andmekogumit, mida kasutatakse proovisoovituste tulemuste mõjutamiseks. Faili nime saab juhtida laienduse konfiguratsiooni kaudu, kasutades sätet **ext.Recommendations DemoFilePath**. See võimaldab teil omada mitu kogumit, mida saab hõlpsalt konfiguratsiooni kaudu vahetada.


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Keskkonna planeerimine](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
