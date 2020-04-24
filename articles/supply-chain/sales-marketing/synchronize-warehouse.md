---
title: Ladude sünkroonimine rakendusest Supply Chain Management rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6617b258a85a8f45b89a38f86919b44edc2100da
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215880"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Ladude sünkroonimine rakendusest Supply Chain Management rakendusse Field Service

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.

[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Järgmist malli ja aluseks olevaid ülesandeid kasutatakse rakendusest Supply Chain Management rakendusse Field Service ladude sünkroonimise kävitamiseks.

**Mall andmeintegratsioonis**
- Laod (rakendusest Supply Chain Management rakendusse Field Service)

**Ülesanne andmeintegratsiooni projektis**
- Ladu

## <a name="entity-set"></a>Üksuste komplekt
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Laod                             |

## <a name="entity-flow"></a>Üksuse voog
Rakenduses Supply Chain Management loodud ja säilitatud ladusid saab Common Data Service’i (CDS) andmeintegratsiooni projekti kaudu sünkroonida rakendusega Field Service. Ladusid, mille soovite sünkroonida rakendusega Field Service, saab juhtida suvandist Täpsem projekti päring ja filtreerimine. Laod, mis sünkroonivad rakendusest Supply Chain Management, luuakse rakenduses Field Service, nii et välja **On väliselt hallatud** väärtuseks on valitud **Jah** ja kirje on kirjutuskaitstud.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
Rakenduste Field Service ja Supply Chain Management vahelise integratsiooni toetamiseks on vajalikud rakenduse Field Service CRM lahenduse lisafunktsioonid. Lahenduses on väli **On väliselt hallatud** lisatud üksusele **Lao (msdyn_warehouses)**. See väli aitab tuvastada, kas ladu käsitletakse Supply Chain Managementist või on see olemas ainult rakenduses Field Service. Selle välja sätted on järgmised.
- **Jah**: ladu pärineb rakendusest Supply Chain Management ja seda ei saa rakenduses Sales muuta.
- **Ei** – ladu sisestati otse rakendusse Field Service ja seda hallatakse seal.

Väli **On väliselt hallatud** aitab juhtida varude tasemete, korrigeerimiste, üleviimiste ja töökäskude kasutuse sünkroonimist. Ainult ladusid, kus suvandi **On väliselt hallatud** sätteks on valitud **Jah**, saab kasutada otse teise süsteemi sama laoga sünkroonimiseks. 

> [!NOTE]
> Rakenduses Field Service on võimalik luua mitmeid ladusid (seadistusega **On väliselt hallatud** = Ei) ja seejärel vastendada need ühe laoga, kasutades täpsema päringu ja filtreerimise funktsiooni. Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondaks üksikasjaliku varude taseme ja saadaks rakendusse Supply Chain Management ainult värskendused. Sellisel juhul ei saa Field Service varude taseme värskendusi rakendusest Supply Chain Management. Lisateavet vt teemadest [Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Töökäskude sünkroonimine rakenduses Field Service rakenduses Finance and Operations projektiga seotud müügitellimustega](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine
### <a name="data-integration-project"></a>Andmeintegratsiooni projekt
Enne ladude sünkroonimist värskendage kindlasti suvandit Täpsem projekti päring ja filtreerimine, et see sisaldaks ainult ladusid, mille soovite tuua rakendusest Supply Chain Management rakendusse Field Service. Pange tähele, et vajate ladu rakenduses Field Service, et rakendada seda töökäskudele, korrigeerimistele ja üleviimistele.  

Veenduge, et üksuse **msdyn_workorders** jaoks oleks olemas **integreerimisvõti**.
1. Avage andmeintegratsioon.
2. Valige vahekaart **Ühendusekogum**.
3. Valige töökäsu sünkroonimiseks kasutatav ühendusekogum.
4. Valige vahekaart **Integreerimisvõti**.
5. Leidke msdyn_warehouses ja kontrollige, kas võti **msdyn_name (nimi)** on lisatud. Kui seda ei kuvata, klõpsake selle lisamiseks käsku **Lisa võti** ja seejärel lehe ülaosas käsku **Salvesta**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmeintegratsioonis.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Laod (rakendusest Supply Chain Management rakendusse Field Service): ladu

[![Malli vastendamine andmete integratsioonis](./media/Warehouse1.png)](./media/Warehouse1.png)
