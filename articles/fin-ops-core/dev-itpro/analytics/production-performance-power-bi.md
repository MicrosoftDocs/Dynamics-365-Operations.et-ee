---
title: Tootmisjõudluse Power BI sisu
description: See artikkel kirjeldab, mida sisaldub tootmise jõudluse sisus Power BI.
author: AndersGirke
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.search.form: ProductionPerformancePowerBI
ms.openlocfilehash: e1b8afcc3d1b64c6828e4081b41a74d3b76731bc
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205729"
---
# <a name="production-performance-power-bi-content"></a>Tootmisjõudluse Power BI sisu

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, mida sisaldub tootmise **jõudluse sisus** Microsoft Power BI. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Tootmisjõudluse** Power BI sisu on mõeldud tootmisjuhtidele või nendele inimestele organisatsioonis, kes vastutavad tootmise juhtimise eest.

Lisatud aruanded võimaldavad kasutada Power BI-d tootmistoimingute tulemusi: õigeaegset läbiviimist, kvaliteeti ja kulu. Aruannetes kasutatakse tootmistellimuste ja partiitellimuste kandeandmeid ning antakse nii koondvaade ettevõtteülestest tootmismõõdikutest kui ka mõõdikute jaotus toote ja ressursi kaupa.

Power BI sisu tõstab esile organisatsiooni võime toota õigeaegselt ja täies mahus. Tulevasi tulemusi prognoositakse tootmisplaanide põhjal. Põhjalikud aruanded annavad üksikasjalikke ülevaateid tootmisega tekitatud tootedefektidest ning ka ressursside ja toimingute defektimääradest.

See Power BI sisu võimaldab analüüsida ka tootmiskulude hälbeid. Tootmiskulude hälbed arvutatakse erinevusena eeldatava ja realiseeritud kulu vahel. Tootmiskulude hälbed arvutatakse siis, kui tootmistellimused või partiitellimused saavutavad oleku **Lõpetatud**.

**Tootmisjõudluse** Power BI sisu hõlmab tootmistellimustest ja partiitellimustest pärinevaid andmeid. Aruanded ei sisalda andmeid, mis on seotud kanban-tootmistega.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Tootmisjõudluse** Power BI sisu kuvatakse lehel **Tootmise jõudlus** (**Tootmise juhtimine** \> **Päringud ja aruanded** \> **Tootmisjõudluse analüüs** \> **Tootmisjõudlus**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad mõõdikud

**Tootmisjõudluse** Power BI sisu sisaldab aruandelehtede kogumit. Iga leht koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena.

Järgmises tabelis antakse ülevaade sisalduvatest visualiseeringutest.

| Aruandeleht                                | Diagrammid | Paanid |
|--------------------------------------------|--------|-------|
| Tootmise jõudlus                     | <ul><li>Tootmiste arv kuupäeva järgi</li><li>Tootmiste arv toote ja kaubagrupi järgi</li><li>Plaanitud tootmiste arv kuupäeva järgi</li><li>10 viimast toodet õigeaegsuse ja täielikkuse alusel</li></ul> | <ul><li>Tellimusi kokku</li><li>Õigeaegsuse ja täielikkuse %</li><li>Mittetäielike %</li><li>Ennetähtaegsete %</li><li>Hilinenute %</li></ul> |
| Defektid toodete kaupa                         | <ul><li>Defektsete määr (ppm) kuupäeva järgi</li><li>Defektsete määr (ppm) toote ja kaubagrupi järgi</li><li>Toodetud kogus kuupäeva järgi</li><li>10 parimat toodet efektiivsusmäära järgi</li></ul> | <ul><li>Defektsete määr (ppm)</li><li>Vigane kogus</li><li>Lõplik kogus</li></ul> |
| Defektide trend toodete kaupa                   | Defektimäär (ppm) toodetud koguse järgi | Defektimäär (ppm) |
| Defektid ressursi alusel                        | <ul><li>Defektimäär (ppm) kuupäeva järgi</li><li>Defektimäär (ppm) ressursi ja laoala järgi</li><li>Defektimäär (ppm) toimingu järgi</li><li>10 parimat ressurssi defektimäära järgi</li></ul> | Vigane kogus |
| Defektide trend ressursi järgi                  | Defektimäär (ppm) töödeldud koguse järgi | |
| Tootmiskulude hälbed tööülesandele kulude jagamisel | <ul><li>Tootmiskulude hälve kuupäeva ja kulugrupi tüübi järgi</li><li>Tootmiskulude hälve laoala ja kulugrupi tüübi järgi</li><li>10 peamist soovimatu tootehälbega toodet</li><li>10 peamist soovimatu tootehälbega toodet ressursi järgi</li></ul> | <ul><li>Realiseeritud kulu</li><li>Tootmiskulude hälve</li><li>Tootmiskulude hälbe %</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

**Tootmisjõudluse** Power BI sisu aruandelehtede jaoks kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet üksuse kaupluse kohta vt teemast [Power BI integreerimine üksuse kauplusega](power-bi-integration-entity-store.md).

Järgmises tabelis on näidatud peamised koondmõõdikud, mida kasutatakse Power BI sisu alusena.

| Üksus                   | Peamised koondmõõtmised  | Finantside ja toimingute rakenduste andmeallikas | Väli              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Järgmine tabel näitab, kuidas kasutatakse peamisi koondmõõtmisi mitme arvutatud meetme loomiseks sisu andmekogumis.

| Mõõt                  | Meetme arvutamise viis |
|--------------------------|-------------------------------|
| Tootmiskulude hälve, %   | SUM('Production variance'\[Production variance\]) / SUM('Production variance'\[Estimated cost\]) |
| Kõik plaanitud tellimused       | COUNTROWS('Planned production order') |
| Varajane                    | COUNTROWS(FILTER('Planned production order', 'Planned production order'\[Scheduled end date\] \< 'Planned production order'\[Requirement date\])) |
| Hilja                     | COUNTROWS(FILTER('Planned production order', 'Planned production order'\[Scheduled end date\] \> 'Planned production order'\[Requirement date\])) |
| Õigeaegne                  | COUNTROWS(FILTER('Planned production order', 'Planned production order'\[Scheduled end date\] = 'Planned production order'\[Requirement date\])) |
| Õigeaegsete %                | IF ( 'Planned production order'\[On-time\] \<\> 0, 'Planned production order'\[On-time\], IF ('Planned production order'\[All planned orders\] \<\> 0, 0, BLANK()) ) / 'Planned production order'\[All planned orders\] |
| Valmis                | COUNTROWS(FILTER('Production order', 'Production order'\[Is RAF'ed\] = TRUE)) |
| Defektsete määr (ppm)     | IF( 'Production order'\[Total quantity\] = 0, BLANK(), (SUM('Production order'\[Defective quantity\]) / 'Production order'\[Total quantity\]) \* 1000000) |
| Viivitusega tootmise määr  | 'Production order'\[Late \#\] / 'Production order'\[Completed\] |
| Ennetähtaegne ja täielik          | COUNTROWS(FILTER('Production order', 'Production order'\[Is in full\] = TRUE && 'Production order'\[Is early\] = TRUE)) |
| Ennetähtaegsed \#                 | COUNTROWS(FILTER('Production order', 'Production order'\[Is early\] = TRUE)) |
| Ennetähtaegsete %                  | IFERROR( IF('Production order'\[Early \#\] \<\> 0, 'Production order'\[Early \#\], IF('Production order'\[Total orders\] = 0, BLANK(), 0)) / 'Production order'\[Total orders\], BLANK()) |
| Lõpetamata               | COUNTROWS(FILTER('Production order', 'Production order'\[Is in full\] = FALSE && 'Production order'\[Is RAF'ed\] = TRUE)) |
| Mittetäielike %             | IFERROR( IF('Production order'\[Incomplete\] \<\> 0, 'Production order'\[Incomplete\], IF('Production order'\[Total orders\] = 0, BLANK(), 0)) / 'Production order'\[Total orders\], BLANK()) |
| On hilinenud               | 'Production order'\[Is RAF'ed\] = TRUE && 'Production order'\[Delayed value\] = 1 |
| On ennetähtaegne                 | 'Production order'\[Is RAF'ed\] = TRUE && 'Production order'\[Days delayed\] \< 0 |
| On täielik               | 'Production order'\[Good quantity\] \>= 'Production order'\[Scheduled quantity\] |
| On RAF'ed                | 'Production order'\[Production status value\] = 5 \|\| 'Production order'\[Production status value\] = 7 |
| Hilinenud ja täielik           | COUNTROWS(FILTER('Production order', 'Production order'\[Is in full\] = TRUE && 'Production order'\[Is delayed\] = TRUE)) |
| Hilinenud \#                  | COUNTROWS(FILTER('Production order', 'Production order'\[Is delayed\] = TRUE)) |
| Hilinenute %                   | IFERROR( IF('Production order'\[Late \#\] \<\> 0, 'Production order'\[Late \#\], IF('Production order'\[Total orders\] = 0, BLANK(), 0)) / 'Production order'\[Total orders\], BLANK()) |
| Õigeaegsed ja täielikud        | COUNTROWS(FILTER('Production order', 'Production order'\[Is in full\] = TRUE && 'Production order'\[Is delayed\] = FALSE && 'Production order'\[Is early\] = FALSE)) |
| Õigeaegsuse ja täielikkuse %      | IFERROR( IF('Production order'\[On-time & in full\] \<\> 0, 'Production order'\[On-time & in full\], IF('Production order'\[Completed\] = 0, BLANK(), 0)) / 'Production order'\[Completed\], BLANK()) |
| Tellimusi kokku             | COUNTROWS('Production order') |
| Lõplik kogus           | SUM('Production order'\[Good quantity\]) + SUM('Production order'\[Defective quantity\]) |
| Defektimäär (ppm)        | IF( 'Route transactions'\[Processed quantity\] = 0, BLANK(), (SUM('Route transactions'\[Defective quantity\]) / 'Route transactions'\[Processed quantity\]) \* 1000000) |
| Kombineeritud defektimäär (ppm) | IF( 'Route transactions'\[Total mixed quantity\] = 0, BLANK(), (SUM('Route transactions'\[Defective quantity\]) / 'Route transactions'\[Total mixed quantity\]) \* 1000000) |
| Töödeldud kogus       | SUM('Route transactions'\[Good quantity\]) + SUM('Route transactions'\[Defective quantity\]) |
| Kombineeritud kogus kokku     | SUM('Production order'\[Good quantity\]) + SUM('Route transactions'\[Defective quantity\]) |

Järgmises tabelis olevaid põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.

| Üksus                    | Atribuutide näited                                        |
|---------------------------|---------------------------------------------------------------|
| Lõppkuupäev kinnitatud | Lõpetamise (RAF) kuupäeva, kuu ja aasta tasakaalustus                 |
| Lõppkuupäev                | Lõpetatud kuu tasakaalustus ja kuu                                  |
| Vajaduse kuupäev          | Vajaduse kuupäeva kuu tasakaalustus ja vajaduse kuupäev            |
| Protsessikande kuupäev    | Protsessikande kuu tasakaalustus ja kuupäev                       |
| Saidid                     | Laoalade ID, laoala nimi, riik ja linn                          |
| Üksused                  | ID ja nimi                                                   |
| Ressursid                 | Ressursi ID, ressursi nimi, ressursitüüp ja ressursigrupp |
| Tooted                  | Tootenumber, toote nimi, kauba ID ja kaubagrupp         |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
