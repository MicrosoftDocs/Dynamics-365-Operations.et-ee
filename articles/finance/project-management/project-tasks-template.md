---
title: Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
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
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770262"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.

> [!NOTE]
> - Versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.
> - Kui kasutate rakendust Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.
> - Tegelike näitajate integratsioon on saadaval versioonis 8.0.1 või uuemas.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automationi andmevoog rakendusse Finance

Rakendusest Project Service Automation rakendusse Finance integratsiooni lahendus kasutab andmeintegratsiooni funktsiooni, et sünkroonida andmeid Project Service Automationi ja Finance’i eksemplaride vahel. Andmeintegratsiooni funktsioonis saadaolev integratsioonimall võimaldab andmevoogu projektiülesannete kohta Project Service Automationist Finance’i.

Järgmine illustratsioon näitab, kuidas andmeid Project Service Automationi ja Finance’i vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks Finance’iga](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mall ja ülesanne

Mallile juurdepääsuks valige Microsoft Power Appsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti tegelike näitajate sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projektiülesanded (Project Service Automationist Finance and Operationsisse)
- **Ülesande nimi projektis:** projektiülesanded

Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.

## <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finantsid                             |
|----------------------------|-------------------------------------|
| Projektiülesanded              | Projekti ülesande integratsiooniüksus |

## <a name="entity-flow"></a>Üksuse voog

Projektiülesandeid hallatakse Project Service Automationis ja need sünkroonitakse Finance’iga projektitegevustena.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.

## <a name="power-query"></a>Power Query

Peate kasutama andmete filtreerimiseks Microsoft Power Queryt Exceli jaoks, kui täidetud on järgmine tingimus.

- Teil on projektiülesandes ressursikohaseid kirjeid.

Kui peate kasutama Power Queryt, järgige järgmist juhtnööri.

- Projektiülesannete (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis välistab ressursikohased kirjed projektiülesandest, seades filtri veerus **IsLineTask** väärtusele **Väär**. Kui loote oma malli, peate selle filtri lisama.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
