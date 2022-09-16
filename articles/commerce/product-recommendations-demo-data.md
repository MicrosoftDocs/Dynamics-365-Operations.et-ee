---
title: Soovituste loomine demoandmetega
description: See artikkel annab juhiseid selle kohta, kuidas võimendada menüü-kanali tootesoovitusi Tier-1 ühe boksi keskkondades, kasutades eelasustatavaid, kohandatavaid demoandmeid.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7e3df414b3c16c28b6f5ca04f765d91c1312ada4
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459964"
---
# <a name="create-recommendations-with-demo-data"></a>Soovituste loomine demoandmetega

[!include [banner](includes/banner.md)]

See artikkel annab juhiseid selle kohta, kuidas võimendada menüü-kanali tootesoovitusi Tier-1 ühe boksi keskkondades, kasutades eelasustatavaid, kohandatavaid demoandmeid.

Omnikanali tootesoovitused pakuvad komplekti toimetuslikult kureeritud või programmiliselt loodud toodete loendit. Neid loendeid saab kasutada mitmes stsenaariumis, sõltuvalt ettevõtte vajadusest. Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).

Teise järgu ja kõrgemate rakenduse Dynamics 365 keskkondade tootesoovitused arvutatakse automaatselt kliendi andmetele tuginedes. Tootesoovituste demoandmte kasutamine ei keela ühtegi tootesoovituste lahendust, mis on juba ette valmistatud keskkonnas ja mis tahes selle kasutusega seotud kulusid.

Esimese järgu keskkonna tootesoovitused põhinevad ainult CSV-failis talletatud staatilistel demoandmetel.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Tootesoovituste demoandmete lubamine keskkonnas
Tootesoovituste demoandmete lubamiseks peate juurutama rakenduse Dynamics 365 Commerce demolaienduse eelvaate vastavate keskkondadega. See lubab automaatselt tootesoovituste demoandmed.

## <a name="default-demo-data"></a>Vaikedemoandmed
Igas OneBoxi tüüpi keskkonnas on eellaaditud tootesoovituste komplekti demoandmed, mis on salvestatud komaeraldatud „reco_demo_data.csv” faili, mis asub Commerce Scale Unitis.

Need andmed on liigendatud järgmiste veergude alusel.

| Veeru nimi         | Kohustuslik          | Kirjeldus                                                                                                                                 | Võimalikud väärtused                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkreetse tootesoovituse loenditüüp, mille demoandmefail loob.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li><li>Vali uuesti</li><li>RecoSimilarVisual</li><li>RecoSimilarTextual</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Konkreetse tööüksuse number, mille puhul eeldatakse tootesoovituste esitamist.                                        |                                                                              |
| Kategooria            |                    |    Kategooria, mille jaoks tuleks kindel loend tagastada. Kui kategooriat pole määratud, on loend ainult navigeerimise hierarhia tipu jaoks.    |                                                                              |
| SeedItemId          |                    |    Lähteväärtusi nõudvate loendite puhul (RecoPeopleAlsoBuy ja RecoCart) peaksid need loendid näitama lisatooteid.            |                                                                              |
| CustomerId          |                    |    Loenditele, mis nõuavad kliendi identifikaatorit (RecoPicks).  Vaikimisi väärtus 0 rakendub kõigile klientidele.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Tulemusena tagastatakse üks või mitu toodet, mis eraldatakse ; abil.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Demoandmete kohandamine
Saate redigeerida vaikimisi demoandmeid mis tahes toote ja kategooria teabega, mis on seadistatud HQ-s. Pärast CSV-faili värskendamist peegeldavad klientidele tagastatud tootesoovitused kohe muudatusi.

Laiend sisaldab andmefaili, mida nimetatakse RecoMockDataset.csv, mis võimaldab teil juhtida andmekogumit, mida kasutatakse proovisoovituste tulemuste mõjutamiseks. Faili nime saab juhtida laienduse konfiguratsiooni kaudu, kasutades sätet **ext.Recommendations DemoFilePath**. See võimaldab teil omada mitu kogumit, mida saab hõlpsalt konfiguratsiooni kaudu vahetada.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
