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
# <a name="omni-channel-product-recommendations-demo-data"></a>Omnikanali tootesoovituste demoandmed

Selle dokumendi eesmärk on anda juhiseid, kuidas võimendada omnikanali tootesoovitusi Tier-1 ühe kasti keskkondades, kasutades eeltäidetud, kohandatavaid demoandmeid.

Omnikanali tootesoovitused pakuvad keeleliselt või programmiliselt loodud tellitud toodete loendit. Neid loendeid saab kasutada mitmes stsenaariumis, sõltuvalt ettevõtte vajadusest. Lisateavet toote soovituste funktsioonide kohta leiate [Tootesoovituste](product-recommendaitons-overview.md) ülevaatest.

Tier-2 ja kõrgema Dynamics Environmentsi tootesoovitused arvutatakse automaatselt kliendi andmetele tuginedes.
Tootesoovituste demoandmte kasutamine ei keela ühtegi tootesoovituste lahendust, mis on juba ette valmistatud keskkonnas ja mis tahes selle kasutusega seotud kulusid.

Tier-1 keskkonna tootesoovitused põhinevad ainult CSV-failis talletatud staatilistel demoandmetel.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Tootesoovituste demoandmete lubamine keskkonnas

Kliendid peavad kasutama **Dynamics 365 CommerceEelvaate demolaiendust** vastavale keskkonnale, mis võimaldab automaatselt tootesoovituste demoandmed.

## <a name="default-demo-data"></a>Vaikedemoandmed
Igas Onebox tüüpi keskkonnas on eellaaditud tootesoovituste komplekti demoandmed, mis on salvestatud komaeraldatud **reco_demo_data.csv** faili, mis asub samas kaustas kui see dokument jaemüügiserveris.

Need andmed on liigendatud järgmiste veergude alusel.

| Veeru nimi         | Kohustuslik          | Kirjeldus                                                                                                                                 | Võimalikud väärtused                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkreetse tootesoovituse loenditüüp, mida demoandmefail loob.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Konkreetse tööüksuse number, mille puhul eeldatakse tootesoovituste esitamist.                                        |                                                                              |
| Kategooria            |                    |    Kategooria, mille jaoks tuleks kindel loend tagastada. Kui kategooriat pole määratud, on loend ainult navigeerimise hierarhia jaoks.    |                                                                              |
| SeedItemId          |                    |    Seemneid nõudvate loendite puhul (RecoPeopleAlsoBuy ja RecoCart) peaksid need loendid näitama lisatooteid.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Tulemusena tagastatakse üks või mitu toodet, mis eraldatakse **;** abil.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Demoandmete kohandamine
Kliendid saavad redigeerida vaikimisi demoandmeid mis tahes toote ja kategooria teabega, mis on seadistatud HQ-s. Pärast CSV uuendamist peegeldavad klientidele tagastatud tootesoovitused kohe muudatusi.

Laiend sisaldab andmefaili, mida nimetatakse RecoMockDataset.csv, mis võimaldab kliendil juhtida andmekogumit, mida kasutatakse proovisoovituste tulemuste mõjutamiseks. Faili nime saab juhtida laienduse konfiguratsiooni kaudu, kasutades sätet **ext.Recommendations DemoFilePath**. See võimaldab klientidel omada mitu kogumit, mida saab hõlpsalt konfiguratsiooni kaudu vahetada.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations-overview.md)

[Keskkonna planeerimine](environment-planning.md)
