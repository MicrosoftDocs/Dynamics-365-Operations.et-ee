---
title: "Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega"
description: "See teema selgitab, kuidas võrrelda loodud elektroonilise aruandluse aruannete tulemusi aruande alusväärtustega."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega

[!include[banner](../includes/banner.md)]

Saate jälgida väljaminevaid elektroonilisi dokumente loovate elektroonilise aruandluse vormingute tulemusi. Kui jälje loomine on sisse lülitatud (elektrooniline aruandlus kasutab parameetrit **Käita silumisrežiimis**), luuakse elektroonilise aruandluse vormingu täitmislogis uus jälituskirje iga kord, kui elektroonilise aruandluse aruannet käitatakse. Igasse loodud jälge salvestatakse järgmised üksikasjad.

- Kõik valideerimisreeglitega loodud hoiatused
- Kõik valideerimisreeglitega loodud tõrked 
- Kõik jälituskirje manustena salvestatud loodud failid

Saate salvestada mis tahes elektroonilise aruandluse vormingu puhul eraldi rakenduse alusfailid. Faile loetakse alusfailideks, kui need kirjeldavad käitatud aruannete oodatud tulemusi. Kui alusfail on saadaval elektroonilise aruandluse vormingu puhul, mis käitati, kui jälje loomine oli sisse lülitatud, salvestab jälg peale eespool nimetatud üksikasjade ka loodud elektroonilise dokumendi ja alusfaili võrdluse tulemuse. Saate ühe klõpsuga tuua loodud elektroonilise dokumendi ja selle alusfaili ühe zip-failina. Seejärel saate teha üksikasjaliku võrdluse, kasutades välist tööriista, nt Windiff.

Saate jälge hinnata, et analüüsida, kas loodud elektroonilised dokumendid sisaldavad oodatud sisu. Nüüd saate teha selle hindamise kasutaja vastuvõtu testimise (UAT) keskkonnas, kui koodi alus on muutunud (näiteks kui läksite üle rakenduse uuele eksemplarile, installisite kiirparanduspakette või juurutasite koodimuudatusi). Sel moel saate kindel olla, et hindamine ei mõjuta kasutatud elektroonilise aruandluse aruannete täitmist. Paljude elektroonilise aruandluse aruannete puhul saab hindamist teha järelevalveta režiimis.

Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusejuhiseid **Elektrooniline aruandlus, aruannete loomine ja tulemuste võrdlemine (1. osa)** ning **Elektrooniline aruandlus: aruannete loomine ja tulemuste võrdlemine (2. osa)**, mis on osa äriprotsessist **7.5.4.3 IT-teenuste/-lahenduste testimine (10679)** ja mille saab alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684). Need tegevusejuhised selgitavad teile elektroonilise aruandluse konfigureerimise protsessi alusfailide kasutamiseks loodud elektrooniliste dokumentide hindamiseks.

