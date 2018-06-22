---
title: "Projektiülesannete sünkroonimine Project Service Automationist"
description: "See teema kirjeldab malli ja aluseks olevat ülesannet, mida kasutatakse projektiülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Dynamics 365 for Finance and Operations."
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
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: et-ee
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Projektiülesannete sünkroonimine Project Service Automationist otse Finance and Operationsi projektitegevustesse

See teema kirjeldab malli ja aluseks olevat ülesannet, mida kasutatakse projektiülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Andmevoog Project Service Automationist Finance and Operationsisse

Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolev integratsioonimall võimaldab andmevoogu projektiülesannete kohta Project Service Automationist Finance and Operationsisse.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mall ja ülesanne

Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projektiülesannete sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

-**Andmeintegratsiooni malli nimi:** projektiülesanded (Project Service Automationist Finance and Operationsisse) -**Ülesande nimi projektis:** projektiülesanded

Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.

## <a name="entity-set"></a>Üksuste komplekt

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Projektiülesanded                           | Projektiülesande integratsiooniüksus.   |

## <a name="entity-flow"></a>Üksuse voog

Projektiülesandeid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projektitegevustena.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.

## <a name="power-query"></a>Power Query

Peate kasutama andmete filtreerimiseks Microsoft Power Queryt, kui täidetud on järgmised tingimused.

- Teil on projektiülesandes ressursikohaseid kirjeid.

Kui peate kasutama Power Queryt, järgige järgmisi juhtnööre.

- Projektiülesannete (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter ressursikohaste kirjete välistamiseks projektiülesandes, seades filtri veerus **IsLineTask** väärtusele **Väär**. Kui loote oma malli, peate selle filtri lisama.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


