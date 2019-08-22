---
title: Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation vahel.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838363"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation vahel.

> [!NOTE]
> - Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.
> - Tegelike näitajate integratsioon on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.1 või uuemas.
> - Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Andmevoog Project Service Automationi ja Finance and Operationsi puhul

Project Service Automationi ja Finance and Operationsi integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ning Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti kulukannete kategooriate kohta Finance and Operationsi ja Project Service Automationi vahel.

Kui projekti kulukategooriad on loodud Finance and Operationsis, on integratsioonivoog esmalt Finance and Operationsist Project Service Automationisse. Projekti kulukategooriate integratsiooni ID-d värskendatakse seejärel sünkroonimise kaudu Project Service Automationist Finance and Operationsisse.

Kui projekti kulukategooriad on loodud Project Service Automationis, on integratsioonivoog esmalt Project Service Automationist Finance and Operationsisse. Enne Project Service Automationist sünkroonimist peavad projekti kategooriad olema juba Finance and Operationsis konfigureeritud. Seejärel sünkroonige Finance and Operationsist tagasi Project Service Automationisse ja siis uuesti Project Service Automationist Finance and Operationsisse. Sel viisil saate tagada, et kategooriad on seotud ja duplikaate ei looda.

> [!NOTE]
> Tavaliselt luuakse projekti kulukategooriad Finance and Operationsis. Kui need aga ei ole loodud Finance and Operationsis või kui kulukategooriad on juba loodud Project Service Automationis, peate kõigepealt sünkroonima, kasutades projekti kulukannete kategooriate (Project Service Automationist Finance and Operationsisse) malli. Seejärel sünkroonige, kasutades projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) malli. Pärast seda peaksite veel üks kord sünkroonima Project Service Automationist Finance and Operationsisse.
>
> Kui sünkroonite esmalt Project Service Automationist, peavad enne sünkroonimist olema Finance and Operationsis täidetud järgmised tingimused.
>
> - Olemas peab olema ühiskasutuses kategooria, mis vastab Project Service Automationis üles seatud projekti kategooriale, ja see peab olem lubatud nii suvandi **Projekt** kui ka **Kulu** jaoks.
> - Iga integreeritava Finance and Operationsi juriidilise isiku puhul peavad olemas olema järgmised projekti kategooriad.
>
>     - **Projekti kategooria** on olemas. 
>     - **Kasuta kuludes** on lubatud.
>     - **Aktiivne töölehel** on lubatud.
>     - **Kande tüüp** on määratud olekule **Kulu**.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Projekti kulukategooriate sünkroonimine Finance and Operationsist Project Service Automationisse

### <a name="template-and-task"></a>Mall ja ülesanne

Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti kulukategooriate sünkroonimiseks Finance and Operationsist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Andmeintegratsioon malli nimi:** projekti kulukannete kategooriad (Finance and Operationsist Project Service Automationisse)
- **Ülesande nimi projektis:** kategooriate sünkroonimine Project Service Automationisse

### <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategooriate integratsiooniüksus | Kandekategooriad     |

### <a name="entity-flow"></a>Üksuse voog

Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena.

### <a name="power-query"></a>Power Query

Project Service Automationisse sünkroonimisel peate kasutama Microsoft Power Queryt Exceli jaoks, et määrata kandekategooriale arveldustüüp. Projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) mallil on olemas vaikeveerg ja vastendus. Kui loote oma malli, peate lisama selle tingimusveeru Power Querys. Tehke järgmist.

1. Klõpsake noolt, et avada projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse)mallis projekti kulukannete kategooriate vastendamise ülesanne.
2. Klõpsake linki **Täpsem päring ja filtreerimine**, et avada Power Query.
2. Valige suvand **Lisa tingimusveerg**.
3. Andke uuele veerule nimi, nt **ArvelduseTüüp**.
4. Sisestage järgmine tingimus: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Klõpsake veerus **OK**.
6. Vastendage see uus veerg kindlasti vastenduslehel.

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Finance and Operationsist Project Service Automationisse.

[![Malli vastendamine](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Projekti kulukategooriate sünkroonimine Project Service Automationist Finance and Operationsisse

### <a name="template-and-task"></a>Mall ja ülesanne

Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Malli nimi andmete integratsioonis:** projekti kulukannete kategooriad (Project Service Automationist Finance and Operationsisse)
- **Ülesande nimi projektis:** kategooriate sünkroonimine Finance and Operationsisse

### <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Kandekategooriad     | Kategooriate integratsiooniüksus |

### <a name="entity-flow"></a>Üksuse voog

Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena. Finance and Operationsisse tagasi sünkroonimine värskendab projektikategooriat Finance and Operationsis integratsiooni ID-ga Project Service Automationist.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.

> [!NOTE]
> Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
