---
title: Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.
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
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250503"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.

> [!NOTE]
> - Versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.
> - Tegelike näitajate integratsioon on saadaval versioonis 8.0.1 või uuemas.
> - Kui kasutate rakendust Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Andmevoog Project Service Automationis Finance’is

Project Service Automationist Finance’i integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance’i eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti kulukannete kategooriate kohta Finance’i ja Project Service Automationi vahel.

Kui projekti kulukategooriad on loodud Finance’is, on integratsioonivoog esmalt Finance’ist Project Service Automationisse. Projekti kulukategooriate integratsiooni ID-d värskendatakse seejärel sünkroonimise kaudu Project Service Automationist Finance’i.

Kui projekti kulukategooriad on loodud Project Service Automationis, on integratsioonivoog esmalt Project Service Automationist Finance’i. Enne Project Service Automationist sünkroonimist peavad projekti kategooriad olema juba Finance’is konfigureeritud. Seejärel sünkroonige Finance’ist tagasi Project Service Automationisse ja siis uuesti Project Service Automationist Finance’i. Sel viisil saate tagada, et kategooriad on seotud ja duplikaate ei looda.

> [!NOTE]
> Tavaliselt luuakse projekti kulukategooriad Finance’is. Kui need aga ei ole loodud või kui kulukategooriad on juba loodud Project Service Automationis, peate kõigepealt sünkroonima, kasutades projekti kulukannete kategooriate (Project Service Automationist Finance and Operationsisse) malli. Seejärel sünkroonige, kasutades projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) malli. Pärast seda peaksite veel üks kord sünkroonima Project Service Automationist Finance’i.
>
> Kui sünkroonite esmalt Project Service Automationist, peavad enne sünkroonimist olema Finance’is täidetud järgmised tingimused.
>
> - Olemas peab olema ühiskasutuses kategooria, mis vastab Project Service Automationis üles seatud projekti kategooriale, ja see peab olem lubatud nii suvandi **Projekt** kui ka **Kulu** jaoks.
> - Iga integreeritava Finance’i juriidilise isiku puhul peavad olemas olema järgmised projekti kategooriad.
>
>     - **Projekti kategooria** on olemas. 
>     - **Kasuta kuludes** on lubatud.
>     - **Aktiivne töölehel** on lubatud.
>     - **Kande tüüp** on määratud olekule **Kulu**.

Järgmine illustratsioon näitab, kuidas andmeid Project Service Automationi ja Finance’i vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks Finance’iga](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projekti kulukategooriate sünkroonimine Finance’ist Project Service Automationisse

### <a name="template-and-task"></a>Mall ja ülesanne

Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti kulukategooriate sünkroonimiseks Finance’ist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Andmeintegratsioon malli nimi:** projekti kulukannete kategooriad (Finance and Operationsist Project Service Automationisse)
- **Ülesande nimi projektis:** kategooriate sünkroonimine Project Service Automationisse

### <a name="entity-set"></a>Üksuste komplekt

| Finantsid                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategooriate integratsiooniüksus | Kandekategooriad     |

### <a name="entity-flow"></a>Üksuse voog

Projekti kulukategooriaid hallatakse Finance’is ja need sünkroonitakse Project Service Automationiga kandekategooriatena.

### <a name="power-query"></a>Power Query

Project Service Automationisse sünkroonimisel peate kasutama Microsoft Power Queryt Exceli jaoks, et määrata kandekategooriale arveldustüüp. Projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) mallil on olemas vaikeveerg ja vastendus. Kui loote oma malli, peate lisama selle tingimusveeru Power Querys. Tehke järgmist.

1. Klõpsake noolt, et avada projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse)mallis projekti kulukannete kategooriate vastendamise ülesanne.
2. Klõpsake linki **Täpsem päring ja filtreerimine**, et avada Power Query.
2. Valige suvand **Lisa tingimusveerg**.
3. Andke uuele veerule nimi, nt **ArvelduseTüüp**.
4. Sisestage järgmine tingimus: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Klõpsake veerus **OK**.
6. Vastendage see uus veerg kindlasti vastenduslehel.

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet, mis sünkroonitakse Finance’ist rakendusse Project Service Automation.

[![Malli vastendamine](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projekti kulukategooriate sünkroonimine Finance’ist Project Service Automationisse

### <a name="template-and-task"></a>Mall ja ülesanne

Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Malli nimi andmete integratsioonis:** projekti kulukannete kategooriad (Project Service Automationist Finance and Operationsisse)
- **Ülesande nimi projektis:** kategooriate sünkroonimine Finance and Operationsisse

### <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finantsid                           |
|----------------------------|-----------------------------------|
| Kandekategooriad     | Kategooriate integratsiooniüksus |

### <a name="entity-flow"></a>Üksuse voog

Projekti kulukategooriaid hallatakse Finance’is ja need sünkroonitakse Project Service Automationiga kandekategooriatena. Finance’i tagasi sünkroonimine värskendab projektikategooriat Finance’is integratsiooni ID-ga Project Service Automationist.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.

> [!NOTE]
> Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
