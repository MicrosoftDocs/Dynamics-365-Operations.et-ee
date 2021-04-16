---
title: Harjutushalduri Power BI sisu
description: See teema kirjeldab, mida hõlmab harjutushalduri Power BI sisu.
author: KimANelson
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 77079a8013cb98acc5f36787ca10706c361736d3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753086"
---
# <a name="practice-manager-power-bi-content"></a>Harjutushalduri Power BI sisu

[!include [banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **Harjutushalduri** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Harjutushalduri** Power BI sisu on mõeldud harjutushalduritele ja projektijuhtidele. See pakub põhimõõdikuid, mis on seotud projektidega, millega organisatsioon töötab. Juhtpaneel annab ülevaate projektidest ja seotud klientidest. Aruande taseme filtri abil saab koostada aruandeid konkreetsetele juriidilistele isikutele. See Power BI sisu toob andmed projekti raamatupidamise koondnäitajatest.

**Harjutushalduri** Power BI sisu sisaldab viit aruandelehte: ühte ülevaatelehte ja nelja lehte, millel on projekti kulude, tulude, teenitud väärtude haldamise ja tunniarvestuse mõõdikud, mis on mitmesuguste dimensioonide lõikes osadeks jagatud.

Kõik sisus antud summad on näidatud süsteemivaluutas. Süsteemi valuuta saab seadistada lehel **Süsteemi parameetrid**.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

**Harjutushalduri** Power BI sisu kuvatakse tööruumis **Projektijuhtimine**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad aruanded

Järgmises tabelis on üksikasjad **harjutushalduri** Power BI sisu igal aruandelehel leiduvate mõõdikute kohta.

| Aruandeleht       | Mõõdikud |
|-------------------|---------|
| Projektide ülevaade | <ul><li>Loodud projektid</li><li>Eeldatavad projektid</li><li>Pooleliolevad projektid</li><li>Tegelik tulu kliendi alusel</li><li>Eelarve kogutulu projektide kaupa</li><li>Teenitud väärtuse haldamise ülevaade</li></ul> |
| Kulu              | <ul><li>Tegelik vs eelarvekulu kuude kaupa</li><li>Tegelik vs eelarvekulu aastate kaupa</li><li>Tegelik vs eelarvekulu kategooriate kaupa</li><li>Tegelik kulu kande tüübi alusel</li></ul> |
| Tulu           | <ul><li>Tegelik tulu kuude kaupa</li><li>Tegelik tulu sihtnumbri alusel</li><li>Tegelik vs eelarvetulu kategooriate kaupa</li><li>Tegelik tulu kliendi valdkonna alusel</li></ul> |
| EVM               | Kulu ja graafiku jõudlusindeks projektide kaupa |
| Tunnid             | <ul><li>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega võrreldes eelarvetundidega</li><li>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega projektide kaupa</li><li>Tegelikud arveldatavad kasutatud tunnid võrreldes tegelike arveldatavate seisakutundidega ressursside kaupa</li><li>Tegelike arveldatavate tundide suhtarv projektide kaupa</li><li>Tegelike arveldatavate tundide suhtarv ressursside kaupa</li></ul> |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Visualisatsioonis summeeritud alusandmete eksportimiseks saab kasutada funktsiooni Alusandmete eksportimine.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

Aruandelehtede täitmiseks **harjutushalduri** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Power BI integratsioon üksuse kauplusega](power-bi-integration-entity-store.md).

Järgmistes jaotistes kirjeldatakse igas üksuses kasutatavaid koondmõõtmisi.

### <a name="entity-projectaccountingcube_actualhourutilization"></a>Üksus: ProjectAccountingCube\_ActualHourUtilization
**Andmeallikas:** ProjEmplTrans

| Peamine koondmõõtmine      | Väli                              | Kirjeldus |
|--------------------------------|------------------------------------|-------------|
| Tegelikud arveldatavad kasutatud tunnid | Sum(ActualUtilizationBillableRate) | Tegelike arveldatavate kasutatud tundide arv kokku. |
| Tegelikud arveldatavad seisakutunnid   | Sum(ActualBurdenBillableRate)      | Tegelik seisakumäär kokku. |

### <a name="entity-projectaccountingcube_actuals"></a>Üksus: ProjectAccountingCube\_Actuals
**Andmeallikas:** ProjTransPosting

| Peamine koondmõõtmine | Väli              | Kirjeldus |
|---------------------------|--------------------|-------------|
| Tegelik müügitulu            | Sum(ActualRevenue) | Kõigi kannete sisestatud tulu kokku. |
| Tegelik kulu               | Sum(ActualCost)    | Sisestatud kulu kõigi kandetüüpide kohta kokku. |

### <a name="entity-projectaccountingcube_customer"></a>Üksus: ProjectAccountingCube\_Customer
**Andmeallikas:** CustTable

| Peamine koondmõõtmine | Väli                                             | Kirjeldus |
|---------------------------|---------------------------------------------------|-------------|
| Projektide arv        | COUNTA(ProjectAccountingCube\_Projects\[PROJECTS\]) | Olemasolevate projektide arv. |

### <a name="entity-projectaccountingcube_forecasts"></a>Üksus: ProjectAccountingCube\_Forecasts
**Andmeallikas:** ProjTransBudget

| Peamine koondmõõtmine | Väli                  | Kirjeldus |
|---------------------------|------------------------|-------------|
| Eelarvekulu               | Sum(BudgetCost)        | Prognoositud kulu kõigi kandetüüpide kohta kokku. |
| Eelarvetulu            | Sum(BudgetRevenue)     | Prognoositud viittulu / arveldatud tulu kokku. |
| Eelarve kogutulu       | Sum(BudgetGrossMargin) | Kogu prognoositud tulusumma ja kogu prognoositud kulusumma vahe. |

### <a name="entity-projectaccountingcube_projectplancostsview"></a>Üksus: ProjectAccountingCube\_ProjectPlanCostsView
**Andmeallikas:** projekt

| Peamine koondmõõtmine | Väli                    | Kirjeldus |
|---------------------------|--------------------------|-------------|
| Plaanitud kulu              | Sum(SumOfTotalCostPrice) | Kogu omahinna prognoos kõigi plaanitud ülesannetega projektikannete tüüpide kohta. |

### <a name="entity-projectaccountingcube_projects"></a>Üksus: ProjectAccountingCube\_Projects
**Andmeallikas:** projekt

| Peamine koondmõõtmine    | Väli | Kirjeldus |
|------------------------------|-------|-------------|
| Kulujõudluse indeks       | ProjectAccountingCube\_Projects\[Teenitud väärtus\] ÷ ProjectAccountingCube\_Projects\[Lõpuleviidud ülesannete tegelik kogukulu\] | Kogu teenitud väärtuse ja tegeliku kulu jagatise arvutus. |
| Jõudluse plaanimise indeks   | ProjectAccountingCube\_Projects\[Teenitud väärtus\] ÷ ProjectAccountingCube\_Projects\[Lõpuleviidud ülesannete plaanitud kogukulu\] | Kogu teenitud väärtuse ja kogu plaanitud kulu jagatise arvutus. |
| Valmis töö protsendimäär | Valmis töö protsendimäär = ProjectAccountingCube\_Projects\[Lõpuleviidud ülesannete tegelik kogukulu\] ÷ (ProjectAccountingCube\_Projects\[Lõpuleviidud ülesannete tegelik kogukulu\] + ProjectAccountingCube\_Projects\[Projekti plaanitud kogukulu\] – ProjectAccountingCube\_Projects\[Lõpuleviidud ülesannete plaanitud kogukulu\]) | Lõpuleviidud töö koguprotsent, mis põhineb kogu lõpetatud ülesande tegelikul kulul ja projekti plaanitud kulul. |
| Tegelike arveldatavate tundide suhtarv  | ProjectAccountingCube\_Projects\[Projekti tegelike arveldatavate kasutatud tundide koguarv\] ÷ (ProjectAccountingCube\_Projects\[Projekti tegelike arveldatavate kasutatud tundide koguarv\] + ProjectAccountingCube\_Projects\[Projekti tegelike arveldatavate kasutatud tundide koguarv\]) | Tegelikud arveldatavad tunnid kasutatud tundide ja seisakutundide põhjal. |
| Plaanitud väärtus                 | ProjectAccountingCube\_Projects\[Projekti plaanitud kogukulu\] × ProjectAccountingCube\_Projects\[Lõpuleviidud töö protsent\] | Plaanitud kogukulu ja lõpuleviidud töö protsendi korrutis. |

### <a name="entity-projectaccountingcube_totalestimatedcosts"></a>Üksus: ProjectAccountingCube\_TotalEstimatedCosts 
**Andmeallikas:** ProjTable

| Peamine koondmõõtmine       | Väli               | Kirjeldus |
|---------------------------------|---------------------|-------------|
| Lõpetatud tegevuse plaanitud kulu | Sum(TotalCostPrice) | Kogu omahinna prognoos kõigi lõpetatud ülesannetega projektikannete tüüpide kohta. |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]