---
title: Tootmistulemuste Power BI sisu
description: "See teema kirjeldab, mida hõlmab tootmistulemuste Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: sericks
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1945d137b337508a1850e3e679a60487aecb6b84
ms.openlocfilehash: fa93249d2dba0e6f72d394daa6a125f29a062594
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="production-performance-power-bi-content"></a>Tootmistulemuste Power BI sisu

[!include[banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **tootmistulemuste** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Tootmistulemuste** Power BI sisu on mõeldud tootmisjuhtidele või nendele inimestele organisatsioonis, kes vastutavad tootmise juhtimise eest.

Lisatud aruanded võimaldavad kasutada Power BI-d tootmistoimingute tulemusi: õigeaegset läbiviimist, kvaliteeti ja kulu. Aruannetes kasutatakse tootmistellimuste ja partiitellimuste kandeandmeid ning antakse nii koondvaade ettevõtteülestest tootmismõõdikutest kui ka mõõdikute jaotus toote ja ressursi kaupa.

Power BI sisu tõstab esile organisatsiooni võime toota õigeaegselt ja täies mahus. Tulevasi tulemusi prognoositakse tootmisplaanide põhjal. Põhjalikud aruanded annavad üksikasjalikke ülevaateid tootmisega tekitatud tootedefektidest ning ka ressursside ja toimingute defektimääradest.

See Power BI sisu võimaldab analüüsida ka tootmiskulude hälbeid. Tootmiskulude hälbed arvutatakse erinevusena eeldatava ja realiseeritud kulu vahel. Tootmiskulude hälbed arvutatakse siis, kui tootmistellimused või partiitellimused saavutavad oleku **Lõpetatud**.

**Tootmistellimuse** Power BI sisu hõlmab tootmistellimustest ja partiitellimustest pärinevaid andmeid. Aruanded ei sisalda andmeid, mis on seotud kanban-tootmistega.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 2017. aasta juuli värskendust, siis kuvatakse **tootmistulemuste** Power BI sisu lehel **Tootmistulemused** (**Tootmise juhtimine** > **Päringud ja aruanded** > **Tootmistulemuste analüüs** > **Tootmistulemused**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad mõõdikud

**Tootmistulemuste** Power BI sisaldab aruandelehtede kogumit. Iga leht koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena.

Järgmises tabelis antakse ülevaade sisalduvatest visualiseeringutest.

| Aruandeleht                                | Diagrammid                                               | Paanid |
|--------------------------------------------|------------------------------------------------------|-------|
| Tootmise jõudlus                     | <ul><li>Tootmiste arv kuupäeva järgi</li><li>Tootmiste arv toote ja kaubagrupi järgi</li><li>Plaanitud tootmiste arv kuupäeva järgi</li><li>10 viimast toodet õigeaegsuse ja täielikkuse alusel</li></ul> | <ul><li>Tellimusi kokku</li><li>Õigeaegsuse ja täielikkuse %</li><li>Mittetäielike %</li><li>Ennetähtaegsete %</li><li>Hilinenute %</li></ul> |
| Defektid toodete kaupa                         | <ul><li>Defektsete määr (ppm) kuupäeva järgi</li><li>Defektsete määr (ppm) toote ja kaubagrupi järgi</li><li>Toodetud kogus kuupäeva järgi</li><li>10 parimat toodet efektiivsusmäära järgi</li></ul> | <ul><li>Defektsete määr (ppm)</li><li>Vigane kogus</li><li>Lõplik kogus</li></ul> |
| Defektide trend toodete kaupa                   | Defektimäär (ppm) toodetud koguse järgi | Defektimäär (ppm) |
| Defektid ressursi alusel                        | <ul><li>Defektimäär (ppm) kuupäeva järgi</li><li>Defektimäär (ppm) ressursi ja laoala järgi</li><li>Defektimäär (ppm) toimingu järgi</li><li>10 parimat ressurssi defektimäära järgi</li></ul> | Vigane kogus |
| Defektide trend ressursi järgi                  | Defektimäär (ppm) töödeldud koguse järgi | |
| Tootmiskulude hälbed tööülesandele kulude jagamisel | <ul><li>Tootmiskulude hälve kuupäeva ja kulugrupi tüübi järgi</li><li>Tootmiskulude hälve laoala ja kulugrupi tüübi järgi</li><li>10 peamist soovimatu tootehälbega toodet</li><li>10 peamist soovimatu tootehälbega toodet ressursi järgi</li></ul> | <ul><li>Realiseeritud kulu</li><li>Tootmiskulude hälve</li><li>Tootmiskulude hälbe %</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI sisu laiendamine
Kasutades teenuses Microsoft Dynamics Lifecycle Services (LCS) olevaid sisupakette, saate pakkuda suurepäraseid analüüsivõimalusi inimestele, kes rakendusse Microsoft Dynamics 365 sisse ei logi. Neid sisupakette saab muuta nii, et need sisaldaksid teisi aruandeid või visuaale, ja avaldada siis sisupaketid analüüsimiseks Power BI.com-i rentnikus.

Power BI sisu **Tootmistulemused** leiate LCS-i ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Laadige kindlasti alla **tootmistulemuste** Power BI sisu, mis kehtib teie kasutatava Dynamics 365 versiooni puhul.

> [!NOTE]
> Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operationsi versiooni 1611, siis on selle Power BI sisu eeltingimus KB 4011327. Pärast LCS-i sisselogimist pääsete teabebaasiartiklile juurde aadressil https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

**Tootmistulemuste** Power BI sisu aruandelehtede jaoks kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Üksuse kaupluse kohta lisateabe saamiseks vt jaotist [Power BI integreerimine üksuse kauplusega](power-bi-integration-entity-store.md).

Järgmises tabelis on näidatud peamised koondmõõdikud, mida kasutatakse Power BI sisu alusena.

| Üksus                   | Peamised koondmõõtmised  | Finance and Operationsi andmeallikas | Väli              |
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
| Tootmiskulude hälve, %   | SUM('Production variance'[Production variance]) / SUM('Production variance'[Estimated cost]) |
| Kõik plaanitud tellimused       | COUNTROWS('Planned production order') |
| Varajane                    | COUNTROWS(FILTER('Planned production order', 'Planned production order'[Scheduled end date] \< 'Planned production order'[Requirement date])) |
| Hilja                     | COUNTROWS(FILTER('Planned production order', 'Planned production order'[Scheduled end date] \> 'Planned production order'[Requirement date])) |
| Õigeaegne                  | COUNTROWS(FILTER('Planned production order', 'Planned production order'[Scheduled end date] = 'Planned production order'[Requirement date])) |
| Õigeaegsete %                | IF ( 'Planned production order'[On-time] \<\> 0, 'Planned production order'[On-time], IF ('Planned production order'[All planned orders] \<\> 0, 0, BLANK()) ) / 'Planned production order'[All planned orders] |
| Valmis                | COUNTROWS(FILTER('Production order', 'Production order'[Is RAF'ed] = TRUE)) |
| Defektsete määr (ppm)     | IF( 'Production order'[Total quantity] = 0, BLANK(), (SUM('Production order'[Defective quantity]) / 'Production order'[Total quantity]) \* 1000000) |
| Viivitusega tootmise määr  | 'Production order'[Late \#] / 'Production order'[Completed] |
| Ennetähtaegne ja täielik          | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = TRUE && 'Production order'[Is early] = TRUE)) |
| Ennetähtaegsed \#                 | COUNTROWS(FILTER('Production order', 'Production order'[Is early] = TRUE)) |
| Ennetähtaegsete %                  | IFERROR( IF('Production order'[Early \#] \<\> 0, 'Production order'[Early \#], IF('Production order'[Total orders] = 0, BLANK(), 0)) / 'Production order'[Total orders], BLANK()) |
| Mittetäielik               | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = FALSE && 'Production order'[Is RAF'ed] = TRUE)) |
| Mittetäielike %             | IFERROR( IF('Production order'[Incomplete] \<\> 0, 'Production order'[Incomplete], IF('Production order'[Total orders] = 0, BLANK(), 0)) / 'Production order'[Total orders], BLANK()) |
| On hilinenud               | 'Production order'[Is RAF'ed] = TRUE && 'Production order'[Delayed value] = 1 |
| On ennetähtaegne                 | 'Production order'[Is RAF'ed] = TRUE && 'Production order'[Days delayed] \< 0 |
| On täielik               | 'Production order'[Good quantity] \>= 'Production order'[Scheduled quantity] |
| On RAF'ed                | 'Production order'[Production status value] = 5 \|\| 'Production order'[Production status value] = 7 |
| Hilinenud ja täielik           | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = TRUE && 'Production order'[Is delayed] = TRUE)) |
| Hilinenud \#                  | COUNTROWS(FILTER('Production order', 'Production order'[Is delayed] = TRUE)) |
| Hilinenute %                   | IFERROR( IF('Production order'[Late \#] \<\> 0, 'Production order'[Late \#], IF('Production order'[Total orders] = 0, BLANK(), 0)) / 'Production order'[Total orders], BLANK()) |
| Õigeaegsed ja täielikud        | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = TRUE && 'Production order'[Is delayed] = FALSE && 'Production order'[Is early] = FALSE)) |
| Õigeaegsuse ja täielikkuse %      | IFERROR( IF('Production order'[On-time & in full] \<\> 0, 'Production order'[On-time & in full], IF('Production order'[Completed] = 0, BLANK(), 0)) / 'Production order'[Completed], BLANK()) |
| Tellimusi kokku             | COUNTROWS('Production order') |
| Lõplik kogus           | SUM('Production order'[Good quantity]) + SUM('Production order'[Defective quantity]) |
| Defektimäär (ppm)        | IF( 'Route transactions'[Processed quantity] = 0, BLANK(), (SUM('Route transactions'[Defective quantity]) / 'Route transactions'[Processed quantity]) \* 1000000) |
| Kombineeritud defektimäär (ppm) | IF( 'Route transactions'[Total mixed quantity] = 0, BLANK(), (SUM('Route transactions'[Defective quantity]) / 'Route transactions'[Total mixed quantity]) \* 1000000) |
| Töödeldud kogus       | SUM('Route transactions'[Good quantity]) + SUM('Route transactions'[Defective quantity]) |
| Kombineeritud kogus kokku     | SUM('Production order'[Good quantity]) + SUM('Route transactions'[Defective quantity]) |

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

## <a name="additional-resources"></a>Lisaressursid

Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

- [Andmeüksused](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities)
- [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI paanide lisamine tööruumidele](/dynamics365/unified-operations/dev-itpro/analytics/configure-power-bi-integration)

