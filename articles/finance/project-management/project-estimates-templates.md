---
title: Projektihinnangute sünkroonimine otse Project Service Automationist rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti eeldatavate tundide ja projekti eeldatava kulu sünkroonimiseks rakendusest Microsoft Dynamics 365 Project Service Automation otse rakendusse Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770285"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projektihinnangute sünkroonimine otse Project Service Automationist rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti eeldatavate tundide ja projekti eeldatava kulu sünkroonimiseks rakendusest Dynamics 365 Project Service Automation otse rakendusse Dynamics 365 Finance.

> [!NOTE]
> - Versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.
> - Tegelike näitajate integratsioon on saadaval versioonis 8.0.1 või uuemas.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automationi andmevoog rakendusse Finance

Rakendusest Project Service Automation rakendusse Finance integratsiooni lahendus kasutab andmeintegratsiooni funktsiooni, et sünkroonida andmeid Project Service Automationi ja Finance’i eksemplaride vahel. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti tunnihinnangute ja projekti kuluhinnangute kohta Project Service Automationist Finance’i.

Järgmine illustratsioon näitab, kuidas andmeid Project Service Automationi ja Finance’i vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks Finance’iga](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekti eeldatavad tunnid

### <a name="template-and-tasks"></a>Mall ja ülesanded

Saadaolevatele mallidele juurdepääsuks valige Microsoft Power Appsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti tunnihinnangute sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projekti tunnihinnangud (Project Service Automationist Finance and Operationsisse)
- **Ülesannete nimed projektis:**

    - Kandeseosed
    - Kuluhinnangud

### <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finantsid                                       |
|----------------------------|-----------------------------------------------|
| Projektiülesanded              | Projekti eeldatavate tundide integratsiooniüksus |

### <a name="entity-flow"></a>Üksuse voog

Projekti tunnihinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance’iga projekti tunnieelarvetena.

### <a name="prerequisites"></a>Eeltingimused

Enne projekti tunnihinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.

### <a name="power-query"></a>Power Query

Porjekti eeldatavate tundide mallis peate kasutama Microsoft Power Queryt Exceli jaoks, et täita järgmised ülesanded.

- Eelarve vaikemudeli ID seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.
- Ülesandest kõigi ressursikohaste kirjete väljafiltreerimine, mille integratsioon tunnieelarveteks nurjub.
- Kõigi tühjade kandekategooria ridade väljafiltreerimine. Selle ülesande täitmatajätmine võib põhjustada valesid tunnieelarved.

#### <a name="set-the-default-forecast-model-id"></a>Eelarve vaikemudeli ID määramine

Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake noolt **Vastendus**, et avada vastendus. Seejärel valige link **Täpsem päring ja filtreerimine**.

- Kui kasutate projekti tunnihinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige **Sisestatud tingimus** loendist **Rakendatud etapid**. Asendage kirjes **Funktsioon** sõne **O\_forecast** selle eelarvemudeli ID nimega, mida tuleb integratsioonis kasutada. Vaikemall kasutab eelarvemudeli ID-d demoandmetest.
- Uue malli loomisel peate lisama selle veeru. Power Querys valige **Lisa tingimusveerg** ja andke uuele veerule nimi, nt **ModelID**. Sisestage veerule tingimus, mis kui projektiülesanne ei ole null, siis \<sisestage eelarvemudeli ID\>; muidu null.

#### <a name="filter-out-resource-specific-records"></a>Ressursikohaste kirjete väljafiltreerimine

Projekti tunnihinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis eemaldab kõik ressursikohased kirjed. Kui loote oma malli, peate selle filtri lisama. Valige link **Täpsem päring ja filtreerimine**, et filtreerida veerg **msdyn\_islinetask**, nii et kaasatud oleks ainult kirjed väärtusega **Väär**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Tühjade kandekategooria ridade väljafiltreerimine

Peate lisama filtri, millega eemaldada kõik tühjade kandekategooriatega read. See ülesanne on nõutav, olenemata sellest, kas kasutate vaikemalli või loote oma malli. See filter eemaldab kõik Project Service Automationist pärinevad kokkuvõtteread, mille tõttu võivad tunnieelarved Finance’is valed olla. Valige link **Täpsem päring ja filtreerimine**, et filtreerida välja nullkirjed veerus **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projekti kuluhinnangud

### <a name="template-and-tasks"></a>Mall ja ülesanded

Projekti tunnihinnangute sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projekti kuluhinnangud (Project Service Automationist Finance and Operationsisse)
- **Ülesannete nimed projektis:**

    - Kandeseosed 
    - Kuluhinnangud

### <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finantsid                                                  |
|----------------------------|----------------------------------------------------------|
| Kandeühendused    | Projekti kande seoste integratsiooniüksus |
| Hinnanguread             | Projekti eeldatava kulu integratsiooniüksus         |

### <a name="entity-flow"></a>Üksuse voog

Projekti kuluhinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance’iga projekti kulueelarvetena.

### <a name="prerequisites"></a>Eeltingimused

Enne projekti kuluhinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.

### <a name="power-query"></a>Power Query

Projekti kuluhinnangute mallis peate kasutama Power Queryt järgmiste ülesannete täitmiseks.

- Filtreerimine kaasamaks ainult kuluhinnangu rea kirjed.
- Eelarve vaikemudeli ID seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.
- Arveldustüüpide teisendamine
- Kandetüüpide teisendamine.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtreerimine kaasamaks ainult kuluhinnangu read

Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis kaasab integratsiooni ainult kuluread. Kui loote oma malli, peate selle filtri lisama. Valige ülesanne **Kandeseosed** ja seejärel klõpsake noolt **Vastendus**, et avada vastendus. Valige link **Täpsem päring ja filtreerimine**. Filtreerige veergu **msdyn\_transactiontype1**, nii et kuvataks ainult **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Eelarve vaikemudeli ID määramine

Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake valige ülesanne **Kuluhinnangud** ja seejärel klõpsake noolt **Vastendus**, et avada vastendus. Valige link **Täpsem päring ja filtreerimine**.

- Kui kasutate projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige Power Querys esimene **Sisestatud tingimus** jaotises **Rakendatud etapid**. Asendage kirjes **Funktsioon** sõne **O\_forecast** selle eelarvemudeli ID nimega, mida tuleb integratsioonis kasutada. Vaikemall kasutab eelarvemudeli ID-d demoandmetest.
- Uue malli loomisel peate lisama selle veeru. Power Querys valige **Lisa tingimusveerg** ja andke uuele veerule nimi, nt **ModelID**. Sisestage veerule tingimus, mis kui hinnangurea ID ei ole null, siis \<sisestage eelarvemudeli ID\>; muidu null.

#### <a name="transform-the-billing-types"></a>Arveldustüüpide teisendamine

Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg, mida kasutatakse Project Service Automationist integratsiooni käigus saadud arveldustüüpide teisendamiseks. Kui loote oma malli, peate selle tingimusveeru lisama. Valige link **Täpsem päring ja filtreerimine** ja seejärel valige **Lisa tingimusveerg**. Andke uuele veerule nimi, nt **ArvelduseTüüp**. Sisestage järgmine tingimus:

Kui **msdyn\_billingtype** = 192350000 , siis **NonChargeable**  
muidu kui **msdyn\_billingtype** = 192350001, siis **Chargeable**  
muidu kui **msdyn\_billingtype** = 192350002, siis **Complimentary**  
muidu **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Kandetüüpide teisendamine

Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg, mida kasutatakse Project Service Automationist integratsiooni käigus saadud kandetüüpide teisendamiseks. Kui loote oma malli, peate selle tingimusveeru lisama. Valige link **Täpsem päring ja filtreerimine** ja seejärel valige **Lisa tingimusveerg**. Andke uuele veerule nimi, nt **TransactionType**. Sisestage järgmine tingimus:

Kui **msdyn\_transactiontypecode** = 192350000, siis **Cost**  
muidu kui **msdyn\_transactiontypecode** = 192350005, siis **Sales**  
muidu **null**

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Malli vastendamine](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
