---
title: "Projekti kulukategooriate sünkroonimine Project Service Automationist"
description: "See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ning Dynamics 365 for Project Service Automation vahel."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: et-ee
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel

See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ning Dynamics 365 for Project Service Automation vahel.

> [!NOTE]
> Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Andmevoog Project Service Automationi ja Finance and Operationsi puhul

Project Service Automationi ja Finance and Operationsi integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ning Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti kulukannete kategooriate kohta Finance and Operationsi ja Project Service Automationi vahel.

Kui projekti kulukategooriad on loodud Finance and Operationsis, on integratsioonivoog esmalt Finance and Operationsist Project Service Automationisse ja seejärel värskendatakse projekti kulukategooriate integratsiooni ID-sid, sünkroonides need Project Service Automationist Finance and Operationsisse.

Kui projekti kulukategooriad on loodud Project Service Automationis, on integratsioonivoog esmalt Project Service Automationist Finance and Operationsisse. Enne Project Service Automationist sünkroonimist peavad projekti kategooriad olema juba Finance and Operationsis konfigureeritud. Seejärel sünkroonige Finance and Operationsist tagasi Project Service Automationisse ja siis uuesti Project Service Automationist Finance and Operationsisse. See tagab, et kategooriad on seotud ja duplikaate ei looda.

> [!NOTE]
> Tavaliselt luuakse projekti kulukategooriad Finance and Operationsis. Muul juhul või kui teil on Project Service Automationis kulukategooriad juba loodud, peate esmalt sünkroonima, kasutades projekti kulukannete kategooriaid (Project Service Automationist Finance and Operationsisse), ja seejärel sünkroonima, kasutades projekti kulukannete kategooriaid (Project Service Automationist Finance and Operationsisse). Seejärel peate sünkroonimise Project Service Automationist Finance and Operationsisse veel üks kord käivitama.

> Kui sünkroonite esmalt Project Service Automationist, peavad projekti kulukategooriad olema Finance and Operationsis juba seadistatud ja kõik kulukategooriad, mis tuleb Project Service Automationi kandekategooriatega sünkroonida, peavad olema seadistatud olekusse **Aktiivne töölehtedel**.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti kulukategooriate sünkroonimiseks Finance and Operationsist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

-  **Andmeintegratsioon malli nimi:** projekti kulukannete kategooriad (Finance and Operationsist Project Service Automationisse)
-  **Ülesande nimi projektis:** kategooriate sünkroonimine Project Service Automationisse

## <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Kategooriate integratsiooniüksus    | Kandekategooriad        |

## <a name="entity-flow"></a>Üksuse voog

Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena.

## <a name="power-query"></a>Power Query

Peate kasutama Microsoft Power Queryt kandekategooriale arveldustüübi määramiseks Project Service Automationisse sünkroonimisel. Projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) mallile on vaikeveerg ja vastendus juba antud. Kui loote oma malli, peate lisama selle tingimusveeru Power Querys.
- Avage projekti kulukategooriate ülesande vastenduses vorm Täpsem päring ja filtreerimine.
- Valige suvand **Lisa tingimusveerg**.
- Andke uuele veerule nimi, nt BillingType.
- Sisestage järgmine tingimus: kui **CATEGORYID ei ole null, siis 19235001, muidu null**.
- Klõpsake veerus **OK**.
- Vastendage see uus veerg kindlasti vastenduslehel.

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Finance and Operationsist Project Service Automationisse.

[![Malli vastendamine](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

-**Andmeintegratsiooni malli nimi:** projekti kulukannete kategooriad (Project Service Automationist Finance and Operationsisse) -**Ülesande nimi projektis:** kategooriate sünkroonimine Finance and Operationsisse

## <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Kandekategooriad          | Kategooriate integratsiooniüksus  | 

## <a name="entity-flow"></a>Üksuse voog

Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena. Tagasi Finance and Operationsisse sünkroonimine värskendab integratsiooni ID Project Service Automationist Finance and Operationsi projektikategoorias.

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.

> [!NOTE]
> Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

