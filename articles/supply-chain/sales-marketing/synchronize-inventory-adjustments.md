---
title: Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: d76adf10b9df48f5a7a5196e0469bb7cb1dbb34f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552229"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.

[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Field Service rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

**Mallid andmeintegratsioonis**
- Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management)
- Varude üleviimised (rakendusest Field Service rakendusse Supply Chain Management)

**Ülesanded andmeintegratsiooni projektides**
- Varude korrigeerimine
- Varude üleviimine

## <a name="entity-set"></a>Üksuste komplekt
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-i varude korrigeerimise töölehe päised ja read |
| msdyn_inventoryadjustmentproducts | CDS-i varude üleviimise töölehe päised ja read   |

## <a name="entity-flow"></a>Üksuse voog
Rakenduses Field Service tehtud varude korrigeerimised ja üleviimised sünkroonitakse rakendusse Supply Chain Management siis, kui **Sisestuse olek** muudetakse olekust **Loodud** olekusse **Sisestatud**. Sellisel juhul lukustatakse korrigeerimis- või üleviimistellimus ja see muutub kirjutuskaitstuks. See tähendab, et korrigeerimised ja üleviimised saab rakendusse Supply Chain Management sisestada, kuid neid ei saa muuta. Rakenduses Supply Chain Management saate seadistada pakett-töö automaatselt korrigeerimisi sisestama ja integratsiooni ajal loodud varude töölehti üle viima. Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus 
Üksusse **Toode** on lisatud väli **Laoühik**. See väli on vajalik, sest müügi- ja laoühik ei ole Supply Chain Managementis alati sama ning Supply Chain Managementis on laoühik laovarude jaoks vajalik.
Kui määrate toote lehel Varude korrigeerimise toode nii suvandi Varude korrigeerimised kui ka Varude üleviimised puhul, tuuakse ühik varude toote väärtusest. Kui väärtus leitakse, lukustatakse väli **Ühik** varude korrigeerimise tootele.

Väli **Sisestuse olek** on lisatud nii üksusele **Varude korrigeerimine** kui ka üksusele **Varude üleviimine**. Seda välja kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Supply Chain Managementi. Selle välja vaikeväärtus on Loodud (1), kuid seda ei saadeta Supply Chain Managementi. Kui värskendate väärtuse valikule Sisestatud (2), saadetakse see Supply Chain Managementi, kuid seejärel ei saa te korrigeerimist ega üleviimist enam muuta ega uusi ridu lisada.

Üksusele **Varude korrigeerimise toode** on lisatud väli **Numbriseeria**. See väli tagab, et integratsioonil on kordumatu number, nii et integratsioon saab korrigeerimisi luua ja värskendada. Esimese varude korrigeerimise toote loomisel tekitab see üksusse **P2C Automaatnummerdus** uue kirje kasutatava numbriseeria ja prefiksi haldamiseks.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="supply-chain-management"></a>Supply Chain Management
Integratsiooniga loodud integratsiooni varude töölehed saab pakett-tööga automaatselt sisestada. Selle lubamiseks valige suvandid **Varude haldus > Perioodilised ülesanded > CDS-integratsioon > Integratsiooni varude töölehtede sisestamine**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management): varude korrigeerimine

[![Malli vastendamine andmete integratsioonis](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Varude üleviimine (rakendusest Field Service rakendusse Supply Chain Management): Varude üleviimine

[![Malli vastendamine andmete integratsioonis](./media/FSTrans1.png)](./media/FSTrans1.png)
