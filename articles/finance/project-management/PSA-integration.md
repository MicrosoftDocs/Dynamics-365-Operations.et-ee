---
title: Project Service Automationi ülevaade
description: Sellest teemast leiate teavet Dynamics 365 Project Service Automationi Dynamics 365 Financesse integreerimise kohta.
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250549"
---
# <a name="project-service-automation-overview"></a>Project Service Automationi ülevaade

[!include[banner](../includes/banner.md)]

Project Service Automationist Finance’ga integratsiooni lahendus kasutab andmete sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation eksemplaride vahel teenuse Common Data Service kaudu andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsiooniga saadaolevad integratsioonimallid võimaldavad andmevoogu projektide, projektilepingute, projektide, projektilepingu ridade, projektilepingu rea vahekokkuvõtete, projektiülesannete, kulukannete kategooriate, tunnihinnangute ja kuluhinnangute kohta Project Service Automationist Finance’i.

> [!NOTE]
> - Kui kasutate versiooni 7.3.0, peate installima KB 4074835. Seejärel saate integreerida fikseeritud hinnaga projekte.
> - Kui kasutate versiooni 7.3.0 ja toote tasukanded rakendusest Project Service Automation üle, peate installima KB 4345320, et need tasud projekti arvesse kaasata.
> - Kui kasutate versiooni 8.0, saate kasutada projektiülesannete integreerimist, kulukannete kategooriaid, tunnihinnanguid, kuluhinnanguid ja funktsioonide lukustamist.
> - Kui kasutate versooni 8.0.1 või uuemat, saate sünkroonida tegelikke näitajaid.

Enne kui saate Project Service Automationi Finance’iga integreerida, peate konfigureerima Project Service Automationi integratsiooniparameetrid. Lisateabe saamiseks vt teemat [Project Service Automationi integratsiooniparameetrid](PSA-parameters.md).

See integratsioonilahendus võimaldab otsest sünkroonimist järgmistes stsenaariumides.

- Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.
- Projektide loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.
- Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.
- Projektilepingute vahekokkuvõtete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.
- Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.
- Kulukannete kategooriate haldamine Finance’is ja nende sünkroonimine Finance’ist otse Project Service Automationisse.
- Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.
- Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.
- Projekti aja, kulu ja tasu tegelike näitajate loomine Project Service Automationis ja projektikannete loomine Project Service Automationi integratsiooni töölehel, et neid saaks sisestada Finance’i.

## <a name="data-synchronization"></a>Andmete sünkroonimine

Järgmine joonis näitab, kuidas sünkroonitakse andmeid integratsiooni osana Project Service Automationi ja Finance’i vahel.

> [!NOTE]
> Kõik mallid pole praegu saadaval. Mallid väljastatakse, kui need on lõpule viidud.

[![Project Service Automationi integreerimisparameetrid Finance’iga](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Rakenduse Finance süsteeminõuded

Project Service Automationist Finance’iga integratsiooni lahenduse kasutamiseks peate installima rakenduse Enterprise edition 7.3 platvormivärskendusega 12 või uuemaga.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automationi süsteeminõuded

Project Service Automationist Finance’i integratsiooni lahenduse kasutamiseks peate installima järgmised komponendid.

- Dynamics 365 Project Service Automationi versioon 9.0.0.0 või uuem
- Lahendus Prospect to cash rakendusele Dynamics 365 Sales, versioon 1.14.0.0 (v14) või hilisem.
- Project Service Automationi Finance’iga integratsiooni lahendus rakenduse Dynamics 365 Project Service Automation versioonile 1.0.0.0 või uuemale

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automationist Finance’i integratsiooni lahenduse installimine oma Project Service Automationi eksemplari

Laadige Project Service Automationi Finance’iga integreerimislahendus alla [Microsofti allalaadimiskeskusest](https://www.microsoft.com/download/details.aspx?id=57016) ja järgige lahendusega kaasasolevaid juhiseid.
