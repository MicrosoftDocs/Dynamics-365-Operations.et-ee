---
title: Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: aa54945cea5821da163e1f6ea1747ac29b31a3ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308364"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

**Mallid andmeintegratsioonis**
- Varude korrigeerimine (rakendusest Field Service rakendusse Finance and Operations)
- Varude üleviimine (rakendusest Field Service rakendusse Finance and Operations)

**Ülesanded andmeintegratsiooni projektides**
- Varude korrigeerimine
- Varude üleviimine

## <a name="entity-set"></a>Üksuste komplekt
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-i varude korrigeerimise töölehe päised ja read |
| msdyn_inventoryadjustmentproducts | CDS-i varude üleviimise töölehe päised ja read   |

## <a name="entity-flow"></a>Üksuse voog
Rakenduses Field Service tehtud varude korrigeerimised ja üleviimised sünkroonitakse rakendusse Finance and Operations siis, kui **Sisestuse olek** muudetakse olekust **Loodud** olekusse **Sisestatud**. Sellisel juhul lukustatakse korrigeerimis- või üleviimistellimus ja see muutub kirjutuskaitstuks. See tähendab, et korrigeerimised ja üleviimised saab rakendusse Finance and Operations sisestada, kuid neid ei saa muuta. Rakenduses Finance and Operations saate seadistada pakett-töö automaatselt korrigeerimisi sisestama ja integratsiooni ajal loodud varude töölehti üle viima. Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus 
Üksusse **Toode** on lisatud väli **Laoühik**. See väli on vajalik, sest müügi- ja laoühik ei ole Finance and Operationsis alati sama ning Finance and Operationisis on laoühik laovarude jaoks vajalik.
Kui määrate toote lehel Varude korrigeerimise toode nii suvandi Varude korrigeerimised kui ka Varude üleviimised puhul, tuuakse ühik varude toote väärtusest. Kui väärtus leitakse, lukustatakse väli **Ühik** varude korrigeerimise tootele.

Väli **Sisestuse olek** on lisatud nii üksusele **Varude korrigeerimine** kui ka üksusele **Varude üleviimine**. Seda välja kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Finance and Operationsi. Selle välja vaikeväärtus on Loodud (1), kuid seda ei saadeta Finance and Operationsisse. Kui värskendate väärtuse valikule Sisestatud (2), saadetakse see Finance and Operationsisse, kuid seejärel ei saa te korrigeerimist ega üleviimist enam muuta ega uusi ridu lisada.

Üksusele **Varude korrigeerimise toode** on lisatud väli **Numbriseeria**. See väli tagab, et integratsioonil on kordumatu number, nii et integratsioon saab korrigeerimisi luua ja värskendada. Esimese varude korrigeerimise toote loomisel tekitab see üksusse **P2C Automaatnummerdus** uue kirje kasutatava numbriseeria ja prefiksi haldamiseks.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="finance-and-operations"></a>Finance and Operations
Integratsiooniga loodud integratsiooni varude töölehed saab pakett-tööga automaatselt sisestada. Selle lubamiseks valige suvandid **Varude haldus > Perioodilised ülesanded > CDS-integratsioon > Integratsiooni varude töölehtede sisestamine**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Varude korrigeerimine (Field Service’ist Finance and Operationsisse): varude korrigeerimine

[![Malli vastendamine andmete integratsioonis](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Varude üleviimine (Field Service’ist Finance and Operationsisse): varude üleviimine

[![Malli vastendamine andmete integratsioonis](./media/FSTrans1.png)](./media/FSTrans1.png)
