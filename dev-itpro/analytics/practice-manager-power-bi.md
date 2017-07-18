---
title: Harjutushalduri Power BI sisu
description: "See teema kirjeldab, mida hõlmab harjutushalduri Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutatakse."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017

---

# <a name="practice-manager-power-bi-content"></a>Harjutushalduri Power BI sisu

[!include[banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **harjutushalduri** Microsofti Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Harjutushalduri** Power BI sisu on mõeldud harjutushalduritele ja projektijuhtidele. See pakub põhimõõdikuid, mis on seotud projektidega, millega organisatsioon töötab. Juhtpaneel annab ülevaate projektidest ja seotud klientidest. Aruande taseme filtri abil saab koostada aruandeid konkreetsetele juriidilistele isikutele. See Power BI sisu toob andmed projekti raamatupidamise koondnäitajatest.

**Harjutushalduri** Power BI sisu sisaldab viit aruandelehte: ühte ülevaatelehte ja nelja lehte, millel on projekti kulude, tulude, teenitud väärtude haldamise ja tunniarvestuse mõõdikud, mis on mitmesuguste dimensioonide lõikes osadeks jagatud.

Kõik sisus antud summad on näidatud süsteemivaluutas. Süsteemi valuuta saab seadistada lehel **Süsteemi parameetrid**.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 2017. aasta juuli värskendust, kuvatakse **harjutushalduri** Power BI sisu aruanded tööruumis **Projektihaldus**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded

Järgmises tabelis on üksikasjad **harjutushalduri** Power BI sisu igal aruandelehel leiduvate mõõdikute kohta.

| Aruandeleht       | Mõõdikud |
|-------------------|---------|
| Projektide ülevaade | <ul><li>Loodud projektid</li><li>Eeldatavad projektid</li><li>Pooleliolevad projektid</li><li>Projektide arv etappide kaupa</li><li>Projektide arv linnade kaupa</li><li>Tegelik tulu kliendi alusel</li><li>Eelarve kogutulu projektide kaupa</li><li>Teenitud väärtuse haldamise ülevaade</li></ul> |
| Kulu              | <ul><li>Tegelik vs eelarvekulu kuude kaupa</li><li>Tegelik vs eelarvekulu aastate kaupa</li><li>Tegelik vs eelarvekulu kategooriate kaupa</li><li>Tegelik kulu kande tüübi alusel</li></ul> |
| Tulu           | <ul><li>Tegelik tulu kuude kaupa</li><li>Tegelik tulu sihtnumbri alusel</li><li>Tegelik vs eelarvetulu kategooriate kaupa</li><li>Tegelik tulu kliendi valdkonna alusel</li></ul> |
| EVM               | Kulu ja graafiku jõudlusindeks projektide kaupa |
| Tunnid             | <ul><li>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega võrreldes eelarvetundidega</li><li>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega projektide kaupa</li><li>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega ressursside kaupa</li><li>Tegelike arveldatavate tundide suhtarv projektide kaupa</li><li>Tegelike arveldatavate tundide suhtarv ressursside kaupa</li></ul> |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Visualisatsioonis summeeritud alusandmete eksportimiseks saab kasutada funktsiooni Alusandmete eksportimine.

## <a name="extending-the-power-bi-content"></a>Power BI sisu laiendamine
Kasutades teenuses Microsoft Dynamics Lifecycle Services (LCS) olevaid sisupakette, saate pakkuda suurepäraseid analüüsivõimalusi inimestele, kes rakendusse Microsoft Dynamics 365 sisse ei logi. Neid sisupakette saab muuta nii, et need sisaldaksid teisi aruandeid või visuaale, ja avaldada need siis analüüsimiseks Power BI.com-i rentnikus. 

Power BI sisu **Harjutushaldur** leiate LCS-i ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Laadige kindlasti alla **harjutushalduri** Power BI sisu, mis kehtib teie kasutatava Dynamics 365 versiooni puhul.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

Aruandelehtede täitmiseks **harjutushalduri** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).

Järgmistes jaotistes kirjeldatakse igas üksuses kasutatavaid koondmõõtmisi.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Üksus: ProjectAccountingCube_ActualHourUtilization
**Andmeallikas:** ProjEmplTrans

| Peamine koondmõõtmine      | Väli                              | Kirjeldus | 
|--------------------------------|------------------------------------|-------------|
| Tegelikud arveldatavad kasutatud tunnid | Sum(ActualUtilizationBillableRate) | Tegelike arveldatavate kasutatud tundide arv kokku. |
| Tegelikud arveldatavad seisakutunnid   | Sum(ActualBurdenBillableRate)      | Tegelik seisakumäär kokku. |

### <a name="entity-projectaccountingcubeactuals"></a>Üksus: ProjectAccountingCube_Actuals
**Andmeallikas:** ProjTransPosting

| Peamine koondmõõtmine | Väli              | Kirjeldus | 
|---------------------------|--------------------|-------------|
| Tegelik müügitulu            | Sum(ActualRevenue) | Kõigi kannete sisestatud tulu kokku. |   
| Tegelik kulu               | Sum(ActualCost)    | Sisestatud kulu kõigi kandetüüpide kohta kokku. |

### <a name="entity-projectaccountingcubecustomer"></a>Üksus: ProjectAccountingCube_Customer
**Andmeallikas:** CustTable

| Peamine koondmõõtmine | Väli                                            | Kirjeldus | 
|---------------------------|--------------------------------------------------|-------------|
| Projektide arv        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Olemasolevate projektide arv. |


### <a name="entity-projectaccountingcubeforecasts"></a>Üksus: ProjectAccountingCube_Forecasts
**Andmeallikas:** ProjTransBudget

| Peamine koondmõõtmine | Väli                  | Kirjeldus | 
|---------------------------|------------------------|-------------|
| Eelarvekulu               | Sum(BudgetCost)        | Prognoositud kulu kõigi kandetüüpide kohta kokku. |
| Eelarvetulu            | Sum(BudgetRevenue)     | Prognoositud viittulu / arveldatud tulu kokku.  |
| Eelarve kogutulu       | Sum(BudgetGrossMargin) | Kogu prognoositud tulusumma ja kogu prognoositud kulusumma vahe. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Üksus: ProjectAccountingCube_ProjectPlanCostsView
**Andmeallikas:** projekt

| Peamine koondmõõtmine | Väli                    | Kirjeldus | 
|---------------------------|--------------------------|-------------|
| Plaanitud kulu              | Sum(SumOfTotalCostPrice) | Kogu omahinna prognoos kõigi plaanitud ülesannetega projektikannete tüüpide kohta. |

### <a name="entity-projectaccountingcubeprojects"></a>Üksus: ProjectAccountingCube_Projects
**Andmeallikas:** projekt

| Peamine koondmõõtmine    | Väli | Kirjeldus | 
|------------------------------|-------|-------------|
| Kulujõudluse indeks       | ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total actual cost of completed tasks] | Kogu teenitud väärtuse ja tegeliku kulu jagatise arvutus. |
| Jõudluse plaanimise indeks   | ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total planned cost of completed tasks] | Kogu teenitud väärtuse ja kogu plaanitud kulu jagatise arvutus. |
| Valmis töö protsendimäär | Valmis töö protsendimäär = ProjectAccountingCube_Projects[Total actual cost of completed tasks] / (ProjectAccountingCube_Projects[Total actual cost of completed tasks] + ProjectAccountingCube_Projects[Total planned cost of project] - ProjectAccountingCube_Projects[Total planned cost of completed tasks]) | Lõpuleviidud töö koguprotsent, mis põhineb kogu lõpetatud ülesande tegelikul kulul ja projekti plaanitud kulul. |
| Tegelike arveldatavate tundide suhtarv  | ProjectAccountingCube_Projects[Project total actual billable utilized hours] / (ProjectAccountingCube_Projects[Project total actual billable utilized hours] + ProjectAccountingCube_Projects[Project total actual billable burden hours]) | Tegelikud arveldatavad tunnid kasutatud tundide ja seisakutundide põhjal. |
| Plaanitud väärtus                 | ProjectAccountingCube_Projects[Total planned cost of project] * ProjectAccountingCube_Projects[Percentage of work completed] | Plaanitud kogukulu ja lõpuleviidud töö protsendi korrutis. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Üksus: ProjectAccountingCube_TotalEstimatedCosts 
**Andmeallikas:** ProjTable

| Peamine koondmõõtmine       | Väli               | Kirjeldus | 
|---------------------------------|---------------------|-------------|
| Lõpetatud tegevuse plaanitud kulu | Sum(TotalCostPrice) | Kogu omahinna prognoos kõigi lõpetatud ülesannetega projektikannete tüüpide kohta. |

