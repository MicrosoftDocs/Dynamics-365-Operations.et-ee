---
title: Ladude sünkroonimine rakendusest Finance and Operations rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835666"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Ladude sünkroonimine rakendusest Finance and Operations rakendusse Field Service

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Ladude sünkroonimise käitamiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

**Mall andmeintegratsioonis**
- Laod (rakendusest Fin and Ops rakendusse Field Service)

**Ülesanne andmeintegratsiooni projektis**
- Ladu

## <a name="entity-set"></a>Üksuste komplekt
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Laod                             |

## <a name="entity-flow"></a>Üksuse voog
Rakenduses Finance and Operations loodud ja säilitatud ladusid saab Common Data Service’i (CDS) andmeintegratsiooni projekti kaudu sünkroonida rakendusega Field Service. Ladusid, mille soovite sünkroonida rakendusega Field Service, saab juhtida suvandist Täpsem projekti päring ja filtreerimine. Laod, mis sünkroonivad rakendusest Finance and Operations, luuakse rakenduses Field Service, nii et välja **On väliselt hallatud** väärtuseks on valitud **Jah** ja kirje on kirjutuskaitstud.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
Rakenduste Field Service ja Finance and Operations vahelise integratsiooni toetamiseks on vajalikud rakenduse Field Service CRM lahenduse lisafunktsioonid. Lahenduses on väli **On väliselt hallatud** lisatud üksusele **Lao (msdyn_warehouses)**. See väli aitab tuvastada, kas ladu käsitletakse Finance and Operationsist või on see olemas ainult rakenduses Field Service. Selle välja sätted on järgmised.
- **Jah** – ladu pärineb rakendusest Finance and Operations ja seda ei saa rakenduses Sales muuta.
- **Ei** – ladu sisestati otse rakendusse Field Service ja seda hallatakse seal.

Väli **On väliselt hallatud** aitab juhtida varude tasemete, korrigeerimiste, üleviimiste ja töökäskude kasutuse sünkroonimist. Ainult ladusid, kus suvandi **On väliselt hallatud** sätteks on valitud **Jah**, saab kasutada otse teise süsteemi sama laoga sünkroonimiseks. 

> [!NOTE]
> Rakenduses Field Service on võimalik luua mitmeid ladusid (seadistusega **Is Externally Maintained** = Ei) ja seejärel vastendada need ühe laoga rakenduses Finance and Operations täpsema päringu ja filtreerimise funktsiooniga. Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku varude taseme ja lihtsalt saadab värskendused rakendusse Finance and Operations. Sellisel juhul ei saa Field Service varude taseme värskendusi rakendusest Finance and Operations. Lisateavet vt teemadest [Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Töökäskude sünkroonimine rakenduses Field Service rakenduses Finance and Operations projektiga seotud müügitellimustega](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine
### <a name="data-integration-project"></a>Andmeintegratsiooni projekt
Enne ladude sünkroonimist värskendage kindlasti suvandit Täpsem projekti päring ja filtreerimine, et see sisaldaks ainult ladusid, mille soovite tuua rakendusest Finance and Operations rakendusse Field Service. Pange tähele, et vajate ladu rakenduses Field Service, et rakendada seda töökäskudele, korrigeerimistele ja üleviimistele.  

Veenduge, et üksuse **msdyn_workorders** jaoks oleks olemas **integreerimisvõti**.
1. Avage andmeintegratsioon.
2. Valige vahekaart **Ühendusekogum**.
3. Valige töökäsu sünkroonimiseks kasutatav ühendusekogum.
4. Valige vahekaart **Integreerimisvõti**.
5. Leidke msdyn_warehouses ja kontrollige, kas võti **msdyn_name (nimi)** on lisatud. Kui seda ei kuvata, klõpsake selle lisamiseks käsku **Lisa võti** ja seejärel lehe ülaosas käsku **Salvesta**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmeintegratsioonis.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>Laod (rakendusest Fin and Ops rakendusse Field Service): ladu

[![Malli vastendamine andmete integratsioonis](./media/Warehouse1.png)](./media/Warehouse1.png)
