---
title: "Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Järgmist malli ja aluseks olevaid ülesandeid kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

**Malli nimi andmete integratsioonis:**
- Projektid (rakendusest Finance and Operations rakendusse Field Service)

**Ülesannete nimed andmete integratsiooni projektis.**
- Projektid

Enne projektide loendi sünkroonimist on nõutavad järgmised sünkroonimisülesanded.
- Kontod (Müügi integratsioon Finance and Operationsiks) 

## <a name="entity-set"></a>Üksuste komplekt
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektid                |

## <a name="entity-flow"></a>Üksuse voog
Projektid luuakse rakenduses Finance and Operations. Projektid, mille **Projekti tüüp** on Aeg ja materjal ja **Projekti etapp** on Pooleli sünkroonitakse rakenduse Field Service **Väline projekt** alla, sealhulgas projekti number, projekti nimi, projekti etapp ja kliendikonto andmed. **Välise projekti** loendit kasutatakse Field Service'i töökäskude sidumiseks rakenduse Finance and Operations projektidega.
Rakenduse Field Service CRM-lahenduse Väline Projekt on uus üksus, mis saab kõik projektid Operationsist.
Välise projekti väli on lisatud üksusele Töökäsk. See väli otsimine, mis märgistades teie Töökäsu Müügitellimuse projektiga ühendatakse seejärel Projektiga Operationsis. Kui süsteemi olek muudab Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli Väline projekt ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine
### <a name="in-finance-and-operations"></a>Rakenduses Finance and Operations
Lubage muudatuste jälgimine Andmeüksuse projektide jaoks

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projektid (rakendusest Finance and Operations rakendusse Field Service): Projektid

[![Malli vastendamine andmete integratsioonis](./media/FSProject1.png)](./media/FSProject1.png)

