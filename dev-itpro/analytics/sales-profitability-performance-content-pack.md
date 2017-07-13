---
title: "Müügi ja tulususe tulemuste Power BI sisu"
description: "See teema kirjeldab, mida hõlmab müügi ja tulususe jõudluse Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 16fef86e330a392ddd888fcb46060c3e1efa87c5
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Müügi ja tulususe tulemuste Power BI sisu

[!include[banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **müügi ja tulususe jõudluse** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Müügi ja tulususe jõudluse** Power BI sisu loodi selleks, et müügijuhid saaksid jälgida peamisi müügimõõdikuid: tulu, brutokasumit ja kasumimarginaale. Selles kasutatakse müügikannete andmeid ning antakse koondvaade kogu ettevõtte müüginumbritest ja müügitulemuste jaotusest klientide ning toodete kohta.

Aruanded toovad esile tulu muutused ja kasumi kasvu aja jooksul. Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi klientide ja toodete positiivsetest ning negatiivsetest trendidest. Lisaks võrreldakse diagrammidel erinevate tootekategooriate tulu ja kasumlikkust ning kliendigruppe omavahel. Tänu sellele saavad kategooria- ja piirkonnajuhid tuvastada mahajääjaid ja liidreid. Lõpuks loob põhjalik aruanne graafiku eraldi kliendi tulu ja kasumimarginaali võrdlusega. Seega on kliendihalduritel andmetepõhine alus, mille abil oma müügi- ja turundustegevusi iga kliendi profiiliga kohandada. 

**Müügi ja tulususe tulemuste sisu** võimaldab müügijuhtidel analüüsida müügitulemusi järgmisel viisil.

-   Aasta senine tulu (kliendigruppide ja eraldi klientide, müügikategooriate ja eraldi toodete ning geograafiliste asukohtade järgi)
-   Tulu muutus aastate lõikes (kliendipiirkondade ja müügikategooriate alusel)

Kasumlikkuse analüüsimiseks on järgmised võimalused.

-   Brutokasum ja kasumimarginaal (kliendigruppide ja toote müügikategooriate alusel)
-   Brutokasumi muutus aastate lõikes
-   Kliendi kasumlikkus (tulu järgi võrreldes kogutuluga)

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 2017. aasta juuli värskendust, siis kuvatakse **müügi ja tulususe jõudluse** Power BI sisu lehel **Müügi ja tulususe jõudlus** (**Müük ja turundus** > **Päringud ja aruanded** > **Müügitulemuste analüüs** > **Müügi ja tulususe jõudlus**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad mõõdikud
**Müügi ja tulususe jõudluse** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate sisu visualiseerimistest.

| Aruandeleht            | Diagrammid                                     | Paanid                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Tulu kliendi alusel    | 10 parimat klienti tulu alusel                | Kogutulem                                           |
|                        | Kogutulu kliendigrupi alusel            | YOY tulu kasv                                      |
|                        | Keskmine kliendi tulu kliendigrupi alusel | Kogutulu                                            |
|                        | Tulu ja brutokasum kliendigrupi alusel   |                                                         |
| Tulu toote alusel     | Tulu ja brutokasum müügikategooria alusel   | Toodete \# kokku                                    |
|                        | 10 parimat toodet tulu alusel                 | Aktiivsete toodete arv ja osakaal koguarvust |
|                        | Kogutulu müügikategooria alusel            | Toodete arv, mis annavad 80% tulust           |
| Tulu perioodi alusel\*    | Tulu kuu alusel                           | YOY tulu kasv                                      |
|                        | Varasema tulu hälve, YOY             | YOY tulu kasvu %                                    |
|                        | Müügihälve kokku kliendipiirkonna alusel    |                                                         |
| Tulu asukoha järgi    | Müügitulu linna alusel                      |                                                         |
|                        | YOY tulu kasvu %                       |                                                         |
|                        | Müügitulu piirkonna alusel                    |                                                         |
| Kliendi kasumlikkus | Kogutulu võrreldes kliendipõhise tuluga   | Brutokasum, kogutulu, YOY tulu kasv          |
| Tulususe analüüs | Tulu ja kogutulu kuu alusel          |                                                         |
|                        | 15 parimat klienti kogutulu alusel           |                                                         |
|                        | Kogutulu kuu alusel, YOY                 |                                                         |

\* Selle ja eelmise aasta tulu ja kasv müügikategooriate alusel.

## <a name="extending-the-power-bi-content"></a>Power BI sisu laiendamine
Kasutades teenuses Microsoft Dynamics Lifecycle Services (LCS) olevaid sisupakette, saate pakkuda suurepäraseid analüüsivõimalusi inimestele, kes rakendusse Microsoft Dynamics 365 sisse ei logi. Neid sisupakette saab muuta nii, et need sisaldaksid teisi aruandeid või visuaale, ja avaldada siis sisupaketid analüüsimiseks Power BI.com-i rentnikus.

Power BI sisu **Müügi ja tulususe jõudlus** leiate LCS-i ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Laadige kindlasti alla **Müügi ja tulususe jõudluse** Power BI sisu, mis kehtib teie kasutatava Dynamics 365 versiooni puhul.

> [!NOTE]
> Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operationsi versiooni 1611, siis on selle Power BI sisu eeltingimus KB 4011327. Pärast LCS-i sisselogimist pääsete teabebaasiartiklile juurde aadressil https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Aruandelehtede täitmiseks **müügi ja tulususe jõudluse** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md). 

Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 müügikuubis olnud koondmõõtmiste alamkogum. Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks. Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Power BI integratsioon üksuse kauplusega Dynamicsis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). 

Järgmisi arve ridade üksuse peamisi koondmõõtmisi kasutatakse sisu alusena.

| Üksus        | Peamised koondmõõtmised                   | Dynamics 365 andmeallikas                    | Väli                                        | Kirjeldus                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Arve read | Tulu                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Summa arvestusvaluutas.            |
|               | Müüdud kaupade omahind                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Kulusumma ja korrigeerimine    |
|               | Komisjoni rea summa – arvestusvaluuta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisjonitasu summa arvestusvaluutas. |

Järgmine tabel näitab arve ridade üksuse peamisi koondmõõtmisi, mida kasutatakse mitme arvutatud meetme loomiseks sisu andmekogumis.

| Mõõt           | Kalkulatsioon                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Kogukasum      | SUM(Tulu – COGS – Komisjon – Käibemaks (sisaldub kliendiarve rea summas))          |
| Kogutulu      | SUM(Kogutulu / (Tulu – Käibemaks (sisaldub kliendiarve rea summas)))             |
| Eelmise aasta tulu | Eelmise aasta tulu = CALCULATE(SUM('Arve read'\[Tulu\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\])) |

Järgmises müügikuubis olevaid põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.

| Üksus           | Atribuutide näited                               |
|------------------|------------------------------------------------------|
| Kliendid        | Kliendigrupid, Kliendipiirkonnad, Aadress, Valdkond |
| Tooted         | Tootenumber, Toote nimi, Kaubagruppide nimi       |
| Müügikategooriad | Müügi kategooria nimed                                 |
| Juriidilised isikud   | Juriidilise isiku nimed                                   |
| Kuupäevad            | Kuupäevad                                                |

Vaikimisi näitab sisu jooksva kalendriaasta andmeid. Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises. Saate muuta ka ettevõtte filtrit.

