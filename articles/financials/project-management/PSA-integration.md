---
title: Project Service Automation
description: "See lahendus kasutab andmeintegratsiooni funktsiooni andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service (CDS) kaudu."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: et-ee
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Project Service Automationist Finance and Operationsisse integratsiooni lahendus kasutab andmeintegratsiooni funktsiooni andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service (CDS) kaudu. Andmeintegratsiooni funktsiooniga saadaolevad integratsioonimallid võimaldavad andmevoogu projektide, projektilepingute, projektide, projektilepingu ridade, projektilepingu rea vahekokkuvõtete, projektiülesannete, kulukannete kategooriate, tunnihinnangute ja kuluhinnangute kohta Project Service Automationist Finance and Operationisse.

> [!NOTE] 
> Kui kasutate rakendust Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, peate installima KB 4074835. See võimaldab teil integreerida fikseeritud hinnaga projekte.
>
> Kui kasutate rakenduse Dynamics 365 for Finance and Operations versiooni 8.0, saate kasutada projektiülesannete integreerimist, kulukannete kategooriaid, tunnihinnanguid, kuluhinnanguid ja funktsioonide lukustamist.
>
> Kui kasutate rakenduse Dynamics 365 for Finance and Operations versiooni 8.0.1, saate sünkroonida tegelikke näitajaid.
>
> Kui kasutate rakendust Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada malle projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.

Enne kui saate Project Service Automationi Finance and Operationsiga integreerida, peate konfigureerima Service Automationi integratsiooniparameetrid. Lisateabe saamiseks vt teemat Project Service Automationi integratsiooniparameetrid.

See integratsioonilahendus võimaldab otsest sünkroonimist järgmistes stsenaariumides.

- Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektide loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektilepingu ridade haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektilepingu ridade vahekokkuvõtete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projektiülesannete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Kulukannete kategooriate haldamine Finance and Operationsis ja nende sünkroonimine Finance and Operationsist otse Project Service Automationisse.
- Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.
- Projekti kuluhinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.

## <a name="data-synchronization"></a>Andmete sünkroonimine
Järgmine joonis näitab, kuidas sünkroonitakse andmeid integratsiooni osana Project Service Automationi ja Finance and Operationsi vahel.

> [!NOTE]
> Kõik mallid pole praegu saadaval. Mallid väljastatakse, kui need on lõpule viidud.

[![Project Service Automationi integratsioon Finance and Operationsiga](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Rakenduse Finance and Operations süsteeminõuded

Project Service Automationist Finance and Operationsisse integratsiooni lahenduse kasutamiseks peate installima rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 koos platvormivärskendusega 12 või uuemaga.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automationi süsteeminõuded

Project Service Automationist Finance and Operationsisse integratsiooni lahenduse kasutamiseks peate installima järgmised komponendid.

- Rakenduse Microsoft Dynamics 365 for Project Service Automation versioon 9.0.0.0 või uuem.
- Lahendus Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.14.0.0 (v14) või hilisem.
- Project Service Automationist Operationsisse lahendus rakendusele Dynamics 365 for Project Service Automation versioon 1.0.0.0 või uuem.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automationist Finance and Operationsisse integratsiooni lahenduse installimine oma Project Service Automationi eksemplari



