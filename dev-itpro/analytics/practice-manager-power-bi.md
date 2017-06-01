---
title: Harjutushalduri Power BI sisu
description: "See teema kirjeldab, mida hõlmab harjutushalduri Power BI sisu. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisupaketi loomiseks kasutatakse."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Harjutushalduri Power BI sisu

[!include[banner](../includes/banner.md)]


See teema kirjeldab, mida hõlmab **harjutushalduri** Microsofti Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Harjutushalduri** Power BI sisu on mõeldud harjutushalduritele ja projektijuhtidele. See pakub põhimõõdikuid, mis on seotud projektidega, millega organisatsioon töötab. Juhtpaneel annab ülevaate projektidest ja seotud klientidest. Aruande taseme filtri abil saab koostada aruandeid konkreetsetele juriidilistele isikutele. See Power BI sisu toob andmed Microsoft Dynamics 365 for Operationsi projekti raamatupidamise koondnäitajatest.

**Harjutushalduri** Power BI sisu sisaldab viit aruandelehte: ühte ülevaatelehte ja nelja lehte, millel on projekti kulude, tulude, teenitud väärtude haldamise ja tunniarvestuse mõõdikud, mis on mitmesuguste dimensioonide lõikes osadeks jagatud.

Kõik sisus antud summad on näidatud süsteemivaluutas. Süsteemi valuuta saab seadistada lehel **Süsteemi parameetrid**.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

**Harjutushalduri** Power BI sisu leiate Microsoft Dynamicsi elutsükliteenuste (LCS) ühiste vahendite teegist. Lisateavet sisupaketi allalaadimise ja selle ühendamise kohta Microsoft Dynamics 365 for Operationsi andmetega vt teemast [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).

Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office mix).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded

Järgmises tabelis on üksikasjad **harjutushalduri** Power BI sisu igal aruandelehel leiduvate mõõdikute kohta.

| Aruandeleht                                          | Mõõdikud               |
|------------------------------------------------------|-----------------------------------------------|
| Armatuurlaud  | Loodud projektid<br>Eeldatavad projektid<br>Pooleliolevad projektid<br>Projektide arv etappide kaupa<br>Projektide arv linnade kaupa<br>Tegelik tulu kliendi alusel<br>Eelarve kogutulu projektide kaupa<br>Teenitud väärtuse haldamise ülevaade |
| Kulu                                                 | Tegelik vs eelarvekulu kuude kaupa<br>Tegelik vs eelarvekulu aastate kaupa<br>Tegelik vs eelarvekulu kategooriate kaupa<br>Tegelik kulu kande tüübi alusel       |
| Tulu                                              | Tegelik tulu kuude kaupa<br>Tegelik tulu sihtnumbri alusel<br>Tegelik vs eelarvetulu kategooriate kaupa<br>Tegelik tulu kliendi valdkonna alusel        |
| EVM                                                  | Kulu ja graafiku jõudlusindeks projektide kaupa                 |
| Tunnid                                                | Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega võrreldes eelarvetundidega<br>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega projektide kaupa<br>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega ressursside kaupa<br>Tegelike arveldatavate tundide suhtarv projektide kaupa<br>Tegelike arveldatavate tundide suhtarv ressursside kaupa |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Visualisatsioonis summeeritud alusandmete eksportimiseks saab kasutada funktsiooni Alusandmete eksportimine.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

Aruandelehtede täitmiseks **harjutushalduri** Power BI sisus kasutatakse Dynamics 365 for Operationsi andmeid. Need andmed esitatakse koondmõõtmistena, mis on koondatud üksuse kauplusse, mis on analüüsimiseks optimeeritud Microsoft SQL-i andmebaas. Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).

Järgmistes jaotistes selgitatakse igas üksuses kasutatavaid koondmõõtmisi.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Üksus: ProjectAccountingCube_ActualHourUtilization
**Andmeallikas**: ProjEmplTrans

| Peamine koondmõõtmine                | Väli                                | Kirjeldus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Tegelike arveldatavate kasutatud tundide arv kokku |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Tegelik seisakumäär kokku             |

### <a name="entity-projectaccountingcubeactuals"></a>Üksus: ProjectAccountingCube_Actuals
**Andmeallikas**: ProjTransPosting

| Peamine koondmõõtmine                | Väli                                | Kirjeldus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Kogu kande sisestatud tulu kokku |   
| ActualCost   |                             Sum(ActualCost)           |    Sisestatud kulu kõigi kandetüüpide kohta kokku    |

### <a name="entity-projectaccountingcubecustomer"></a>Üksus: ProjectAccountingCube_Customer
**Andmeallikas**: CustTable

| Peamine koondmõõtmine                | Väli                                | Kirjeldus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Projektide arv        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Olemasolevate projektide arv    |


### <a name="entity-projectaccountingcubeforecasts"></a>Üksus: ProjectAccountingCube_Forecasts
**Andmeallikas**: ProjTransBudget

| Peamine koondmõõtmine                | Väli                                | Kirjeldus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Prognoositud kulu kõigi kandetüüpide kohta kokku     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Prognoositud viittulu / arveldatud tulu kokku         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Kogu prognoositud tulusumma ja kogu prognoositud kulusumma vahe

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Üksus: ProjectAccountingCube_ProjectPlanCostsView
**Andmeallikas**: projekt

| Peamine koondmõõtmine                | Väli                                | Kirjeldus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Kogu omahinna prognoos kõigi plaanitud ülesannetega projektikannete tüüpide kohta |

### <a name="entity-projectaccountingcubeprojects"></a>Üksus: ProjectAccountingCube_Projects
**Andmeallikas**: projekt

| Peamine koondmõõtmine                | Väli                                | Kirjeldus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Kulujõudluse indeks  |ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total actual cost of completed tasks] |     Kogu teenitud väärtuse ja tegeliku kulu jagatise arvutus|
|  Jõudluse plaanimise indeks |ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total planned cost of completed tasks]|Kogu teenitud väärtuse ja plaanitud kulu jagatise arvutus |
|Valmis töö protsendimäär |Percentage of work completed = ProjectAccountingCube_Projects[Total actual cost of completed tasks] / (ProjectAccountingCube_Projects[Total actual cost of completed tasks] + ProjectAccountingCube_Projects[Total planned cost of project] - ProjectAccountingCube_Projects[Total planned cost of completed tasks])|Lõpuleviidud töö koguprotsent, mis põhineb kogu lõpetatud ülesande tegelikul kulul ja projekti plaanitud kulul|
|Projekti tegelike arveldatavate tundide suhtarv|ProjectAccountingCube_Projects[Project total actual billable utilized hours] / (ProjectAccountingCube_Projects[Project total actual billable utilized hours] + ProjectAccountingCube_Projects[Project total actual billable burden hours])|Tegelikud arveldatavad tunnid kasutatud + seisaku põhjal|
|Plaanitud väärtus|ProjectAccountingCube_Projects[Total planned cost of project] * ProjectAccountingCube_Projects[Percentage of work completed]|Plaanitud kogukulu ja lõpuleviidud töö protsendi korrutis|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Üksus: ProjectAccountingCube_TotalEstimatedCosts 
**Andmeallikas**: ProjTable

| Peamine koondmõõtmine                | Väli                                | Kirjeldus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Kogu omahinna prognoos kõigi lõpuleviidud ülesannetega projektikannete tüüpide kohta|

## <a name="additional-resources"></a>Lisaressursid

Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

- [Andmeüksused](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI integreerimise konfigureerimine tööruumidele](configure-power-bi-integration.md)

