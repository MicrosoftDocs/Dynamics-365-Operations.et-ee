---
title: Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation rakendusse Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355169"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation rakendusse Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.
> - Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.
> - Tegelike näitajate integratsioon on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.1 või uuemas.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Andmevoog Project Service Automationist Finance and Operationsisse

Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolev integratsioonimall võimaldab andmevoogu projektiülesannete kohta Project Service Automationist Finance and Operationsisse.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mall ja ülesanne

Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projektiülesannete sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Andmeintegratsioon malli nimi:** projektiülesanded (Project Service Automationist Finance and Operationsisse)
- **Ülesande nimi projektis:** projektiülesanded

Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.

## <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| Projektiülesanded              | Projekti ülesande integratsiooniüksus |

## <a name="entity-flow"></a>Üksuse voog

Projektiülesandeid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projektitegevustena.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.

## <a name="power-query"></a>Power Query

Peate kasutama andmete filtreerimiseks Microsoft Power Queryt Exceli jaoks, kui täidetud on järgmine tingimus.

- Teil on projektiülesandes ressursikohaseid kirjeid.

Kui peate kasutama Power Queryt, järgige järgmist juhtnööri.

- Projektiülesannete (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis välistab ressursikohased kirjed projektiülesandest, seades filtri veerus **IsLineTask** väärtusele **Väär**. Kui loote oma malli, peate selle filtri lisama.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
