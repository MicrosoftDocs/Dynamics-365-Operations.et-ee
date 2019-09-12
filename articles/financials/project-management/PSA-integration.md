---
title: Project Service Automationi ülevaade
description: See teema annab teavet Project Service Automationi Finance and Operationsiga integreerimislahenduse kohta. See integratsioonilahendus kasutab andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service kaudu andmeintegratsiooni funktsiooni.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865624"
---
# <a name="project-service-automation-overview"></a>Project Service Automationi ülevaade

[!include[banner](../includes/banner.md)]

Project Service Automationist Finance and Operationsiga integratsiooni lahendus kasutab andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service kaudu andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsiooniga saadaolevad integratsioonimallid võimaldavad andmevoogu projektide, projektilepingute, projektide, projektilepingu ridade, projektilepingu rea vahekokkuvõtete, projektiülesannete, kulukannete kategooriate, tunnihinnangute ja kuluhinnangute kohta Project Service Automationist Finance and Operationisse.

> [!NOTE]
> - Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.
> - Kui kasutate Finance and Operationsi versiooni 7.3.0, peate installima KB 4074835. Seejärel saate integreerida fikseeritud hinnaga projekte.
> - Kui kasutate rakendust Finance and Operations 7.3.0 ja toote tasukanded rakendusest Project Service Automation üle, peate installima KB 4345320, et need tasud projekti arvesse kaasata.
> - Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations versiooni 8.0, saate kasutada projektiülesannete integreerimist, kulukannete kategooriaid, tunnihinnanguid, kuluhinnanguid ja funktsioonide lukustamist.
> - Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations versooni 8.0.1 või uuemat, saate sünkroonida tegelikke näitajaid.

Enne kui saate Project Service Automationi Finance and Operationsiga integreerida, peate konfigureerima Service Automationi integratsiooniparameetrid. Lisateabe saamiseks vt teemat [Project Service Automationi integratsiooniparameetrid](PSA-parameters.md).

See integratsioonilahendus võimaldab otsest sünkroonimist järgmistes stsenaariumides.

- Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektide loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektilepingu ridade haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektilepingu ridade vahekokkuvõtete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektiülesannete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Kulukannete kategooriate haldamine Finance and Operationsis ja nende sünkroonimine Finance and Operationsist otse Project Service Automationisse.
- Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projekti kuluhinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projekti aja, kulu ja tasu tegelike näitajate loomine Project Service Automationis ja projektikannete loomine Project Service Automationi integratsiooni töölehel, et neid saaks sisestada Finance and Operationsis.

## <a name="data-synchronization"></a>Andmete sünkroonimine

Järgmine joonis näitab, kuidas sünkroonitakse andmeid integratsiooni osana Project Service Automationi ja Finance and Operationsi vahel.

> [!NOTE]
> Kõik mallid pole praegu saadaval. Mallid väljastatakse, kui need on lõpule viidud.

[![Project Service Automationi integratsioon Finance and Operationsiga](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Rakenduse Finance and Operations süsteeminõuded

Project Service Automationist Finance and Operationsiga integratsiooni lahenduse kasutamiseks peate installima rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 platvormivärskendusega 12 või uuemaga.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automationi süsteeminõuded

Project Service Automationist Finance and Operationsisse integratsiooni lahenduse kasutamiseks peate installima järgmised komponendid.

- Microsoft Dynamics 365 for Project Service Automationi versioon 9.0.0.0 või uuem
- Lahendus Potentsiaalne klient sularahaks rakenduse Microsoft Dynamics 365 for Sales versioonile 1.14.0.0 (v14) või uuemale
- Project Service Automationi Finance and Operationsiga integratsiooni lahendus rakenduse Microsoft Dynamics 365 for Project Service Automation versioonile 1.0.0.0 või uuemale

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automationist Finance and Operationsisse integratsiooni lahenduse installimine oma Project Service Automationi eksemplari

Laadige Project Service Automationi Finance and Operationsiga integreerimislahendus alla [Microsofti allalaadimiskeskusest](https://www.microsoft.com/download/details.aspx?id=57016) ja järgige lahendusega kaasasolevaid juhiseid.
