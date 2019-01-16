---
title: "Ladude sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Ladude sünkroonimine rakendusest Finance and Operations rakendusse Field Service

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Järgmist malli ja aluseks olevaid ülesandeid kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

**Malli nimi andmete integratsioonis:**
- Laod (rakendusest Finance and Operations rakendusse Field Service)

**Ülesannete nimed andmete integratsiooni projektis.**
- Ladu

## <a name="entity-set"></a>Üksuste komplekt
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Laod                             |

## <a name="entity-flow"></a>Üksuse voog
Rakenduses Finance and Operations loodud ja säilitatud ladusid saab Common Data Service’i (CDS) andmeintegratsiooni projekti kaudu sünkroonida rakendusega Field Service. Soovitud ladusid, mis sünkroonivad rakendusse Field Service, saab juhtida suvandist Täpsem projekti päring ja filtreerimine. Laod, mis sünkroonivad rakendusest Finance and Operations, luuakse rakenduses Field Service, nii et väli On väliselt hallatud on seadistatud jah peale ja kirje on kirjutuskaitstud.
Rakenduse Field Service CRM-lahendus Rakenduste Field Service ja Finance and Operations vahelise integratsiooni toetamiseks on vajalikud rakenduse Field Service CRM lahenduse lisafunktsioonid. Lahendus sisaldab järgmisi muudatusi.
Väli **On väliselt hallatud** on lisatud **Lao (msdyn_warehouses)** üksusele. See väli aitab tuvastada, kas Ladu käsitletakse Operationsi alt või on see olemas ainult rakenduses Field Service.
- Jah – ladu pärineb rakendusest Finance and Operations ja seda ei saa rakenduses Sales muuta.
- Ei – ladu sisestati otse rakendusse Field Service ja seda hallatakse seal.

Väli **On väliselt hallatud** aitab juhtida kaubavarude taseme, korrigeerimiste, üleviimiste ja töökäskude kasutuse sünkroonimist. Ainult ladusid kus **On väliselt hallatud** = Jah, saab kasutada otse teise süsteemi samasse lattu sünkroonimiseks. 

Märkus: Rakenduses Field Services on võimalik luua mitmeid ladusid (seadistusega **Is Externally Maintained** = ei) ja seejärel vastendada need ühe laoga rakenduses Finance and Operations, koos täpsema pärinug- ja filtreerimise funktsionaalsusega. Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku kaubavaru taseme ja lihtsalt saadab värskendused rakendusse Finance and Operations. Sllisel juhul ei saa rakendus Field Service kaubavarude taseme värskendusi rakendusest Finance and Operations. Vaadake lisainfot varude korrigeerimise rakendusest Field Service rakendusse Finance and Operations sünkroonimise alt ja sünkroonige töökäsud rakendusest Field Service projektiga seotud töökäskudesse rakenduses Finance and Operations.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine
### <a name="in-the-data-integration-project"></a>Andmeintegratsiooni projektis
Enne ladude sünkroonimist veenduge, et uuendate suvandit Täpsem projekti päring ja filtreerimine, et see sisaldaks ainult ladusid, mida tahate tuua rakendusest Finance and Operations rakendusse Field Service. ÜPange tähele, et vajate ladu rakenduses Field Service, et rakendada seda töökäskudele, korrigeerimistele ja üleviimistele.  

Veenduge, et üksuse **msdyn_workorders** jaoks oleks olemas **msdyn_warehouses**.
1. Avage andmete integratsioon
2. Valige vahekaart **Ühenduskomplekt**
3. Valige töökäsu sünkroonimiseks kasutatud ühenduskomplekt
4. Valige vahekaart **Integreerimisvõti**
5. Leidke msdyn_warehouses ja kontrollige, kas võti **msdyn_name (nimi)** on lisatud. Kui seda ei kuvata, klõpsake selle lisamiseks lehe ülaosas valikut **Lisa võti** ja **Salvesta**

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Laod (rakendusest Finance and Operations rakendusse Field Service): Ladu

[![Malli vastendamine andmete integratsioonis](./media/Warehouse1.png)](./media/Warehouse1.png)

