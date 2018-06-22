---
title: "Projektihinnangute sünkroonimine Project Service Automationist otse Finance and Operationsi projektieelarvetesse"
description: "See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tunnihinnangute ja projekti kuluhinnangute sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: et-ee
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Projektihinnangute sünkroonimine Project Service Automationist otse Finance and Operationsi projektieelarvetesse

See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tunnihinnangute ja projekti kuluhinnangute sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Andmevoog Project Service Automationist Finance and Operationsisse

Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti tunnihinnangute ja projekti kuluhinnangute kohta Project Service Automationist Finance and Operationsisse.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti tunnihinnangute sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

-  **Andmeintegratsioon malli nimi:** projekti tunnihinnangud (Project Service Automationist Finance and Operationsisse)

-  **Ülesannete nimed projektis:** 
    - Kandeseosed 
    - Kuluhinnangud

## <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Projektiülesanded                   | Projekti eeldatavate tundide integratsiooniüksus   |

## <a name="entity-flow"></a>Üksuse voog

Projekti tunnihinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projekti tunnieelarvetena.

## <a name="preconditions"></a>Eeltingimused

Enne projekti tunnihinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.

## <a name="power-query"></a>Power Query

Peate kasutama Microsoft Power Queryt projekti tunnihinnangute mallis järgmisel otstarbel.
- **Eelarvemudeli ID** seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.
- Ülesandest kõigi ressursikohaste kirjete väljafiltreerimine, mille integratsioon tunnieelarveteks nurjub.
- Kõigi tühjade kandekategooria ridade väljafiltreerimine. Selle tegematajätmine võib põhjustada valesid tunnieelarved.

### <a name="forecast-model-id"></a>Eelarvemudeli ID
Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake noolt **Vastendus**, et avada vastendus. Valige suvandi Täpsem päring ja filtreerimine avamiseks.
- Kui kasutate Microsoft Projecti tunnihinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige viimane **Sisestatud tingimus** jaotises **Rakendatud etapid**. Asendage kirjes **Funktsioon** sõne **O_forecast** selle **eelarvemudeli** nimega, mida tuleb integratsioonis kasutada. Vaikemall kasutab eelarvemudeli ID-d demoandmetest.
- Uue malli loomisel peate lisama selle veeru. Valige suvand **Lisa tingimusveerg** ja andke veerule nimi, nt ModelID. Sisestage veerule tingimus, kus kui projektiülesanne ei ole null, siis <enter the forecast model ID>, muidu null.

### <a name="filter-out-resource-specific-records"></a>Ressursikohaste kirjete väljafiltreerimine
Projekti tunnihinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis eemaldab kõik ressursikohased kirjed. Kui loote oma malli, peate selle filtri lisama. Filtreerige vormil Täpsem päring ja filtreerimine veerg **msdyn_islinetask** nii, et see kuvaks ainult kirjed väärtusega **Väär**.

### <a name="filter-out-empty-transaction-category-rows"></a>Tühjade kandekategooria ridade väljafiltreerimine
Peate lisama filtri, millega eemaldada kõik tühjade kandekategooriatega read. See on vajalik sõltumata sellest, kas kasutate vaikemall või loote oma malli. See filter eemaldab kõik Project Service Automationist pärinevad kokkuvõtteread, mille tõttu võivad tunnieelarved Finance and Operationsis valed olla. Filtreerige vormil Täpsem päring ja filtreerimine veerus **msdyn_transactioncategory_value** välja nullkirjed.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Projekti kuluhinnangute sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

-  **Andmeintegratsioon malli nimi:** projekti kuluhinnangud (Project Service Automationist Finance and Operationsisse)
-  **Ülesannete nimed projektis:** 
     - Kandeseosed 
     - Kuluhinnangud

## <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Kandeühendused         | Projekti kandeseoste integratsiooniüksus.   |
| Hinnanguread                  | Projekti kuluhinnangute integratsiooniüksus.           |

## <a name="entity-flow"></a>Üksuse voog

Projekti kuluhinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projekti kulueelarvetena.

## <a name="prerequisites"></a>Eeltingimused

Enne projekti kuluhinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.

## <a name="power-query"></a>Power Query

Peate kasutama Microsoft Power Queryt projekti kuluhinnangute mallis järgmisel otstarbel.
- Filtreerimine kaasamaks ainult kuluhinnangu rea kirjed
- **Eelarvemudeli ID** seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.
- Arveldustüüpide teisendamine
- Kandetüüpide teisendamine.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtreerimine kaasamaks ainult kuluhinnangu read
Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis kaasab integratsiooni ainult kuluread. Kui loote oma malli, peate selle filtri lisama. Valige kandeseoste ülesanne ja klõpsake noolt **Vastendus**. Valige **Täpsem päring ja filtreerimine**. Filtreerige veergu **msdyn_transactiontype1**, nii et kuvataks ainult **msdyn_estimateline**.

### <a name="forecast-model-id"></a>Eelarvemudeli ID
Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake kuluhinnangute ülesande puhul noolt **Vastendus**, et avada vastendus. Valige suvandi Täpsem päring ja filtreerimine avamiseks.
- Kui kasutate Microsoft Projecti kuluhinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige esimene **Sisestatud tingimus** jaotises **Rakendatud etapid**. Asendage kirjes **Funktsioon** sõne **O_forecast** selle **eelarvemudeli** nimega, mida tuleb integratsioonis kasutada. Vaikemall kasutab eelarvemudeli ID-d demoandmetest.
- Uue malli loomisel peate lisama selle veeru. Valige suvand **Lisa tingimusveerg** ja andke veerule nimi, nt ModelID. Sisestage veerule tingimus, mis kui hinnangurea ID ei ole null, siis < sisestage eelarvemudeli ID >; muidu null.

### <a name="transform-the-billing-types"></a>Arveldustüüpide teisendamine
Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg Project Service Automationist integratsiooni käigus saadud arveldustüüpide teisendamiseks.
- Kui loote oma malli, peate selle tingimusveeru lisama. Valige vormil Täpsem päring ja filtreerimine suvand **Lisa tingimusveerg**. Andke veerule nimi, nt BillingType. Sisestatav tingimus on järgmine.

    Kui **msdyn_billingtype** = 192350000, siis **NonChargeable**, muidu kui **msdyn_billingtype** = 192350001, siis **Chargeable**, muidu kui **msdyn_billingtype** = 192350002, siis **Complimentary**, muidu **NotAvailable**

### <a name="transform-the-transaction-types"></a>Kandetüüpide teisendamine
Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg Project Service Automationist integratsiooni käigus saadud kandetüüpide teisendamiseks.
- Kui loote oma malli, peate selle tingimusveeru lisama. Valige vormil Täpsem päring ja filtreerimine suvand **Lisa tingimusveerg**. Andke veerule nimi, nt TransactionType. Sisestatav tingimus on järgmine. Kui **msdyn_transactiontypecode** = 192350000, siis **Cost**, muidu kui **msdyn_transactiontypecode** = 192350005, siis **Sales**, muidu **null**

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Malli vastendamine](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




