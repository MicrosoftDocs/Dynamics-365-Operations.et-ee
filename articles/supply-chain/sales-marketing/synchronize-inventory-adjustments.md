---
title: Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management
description: See artikkel käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste sünkroonimiseks ja üleviimisteks asukohast Dynamics 365 Supply Chain Management Dynamics 365 Field Service.
author: Henrikan
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: e59e50a4f54bac749b3d860404a3ecd444d99a89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854090"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management

[!include[banner](../includes/banner.md)]



See artikkel käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste sünkroonimiseks ja üleviimisteks asukohast Dynamics 365 Supply Chain Management Dynamics 365 Field Service.

[![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel.](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Field Service rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

**Mallid andmeintegratsioonis**
- Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management)
- Varude üleviimised (rakendusest Field Service rakendusse Supply Chain Management)

**Ülesanded andmeintegratsiooni projektides**
- Varude korrigeerimine
- Varude üleviimine

## <a name="table-set"></a>Tabelikomplekt
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Dataverse’i varude korrigeerimise töölehe päised ja read |
| msdyn_inventoryadjustmentproducts | Dataverse’i varude üleviimise töölehe päised ja read   |

## <a name="table-flow"></a>Tabelivoog
Rakenduses Field Service tehtud varude korrigeerimised ja üleviimised sünkroonitakse rakendusse Supply Chain Management siis, kui **Sisestuse olek** muudetakse olekust **Loodud** olekusse **Sisestatud**. Sellisel juhul lukustatakse korrigeerimis- või üleviimistellimus ja see muutub kirjutuskaitstuks. See tähendab, et korrigeerimised ja üleviimised saab rakendusse Supply Chain Management sisestada, kuid neid ei saa muuta. Rakenduses Supply Chain Management saate seadistada pakett-töö automaatselt korrigeerimisi sisestama ja integratsiooni ajal loodud varude töölehti üle viima. Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus 
Tabelisse **Toode** on lisatud veerg **Laoühik**. See veerg on vajalik, sest müügi- ja laoühik ei ole Supply Chain Managementis alati sama ning Supply Chain Managementis on laoühik laovarude jaoks vajalik.
Kui määrate toote lehel Varude korrigeerimise toode nii suvandi Varude korrigeerimised kui ka Varude üleviimised puhul, tuuakse ühik varude toote väärtusest. Kui väärtus leitakse, lukustatakse veerg **Ühik** varude korrigeerimise tootele.

Veerg **Sisestuse olek** on lisatud nii tabelile **Varude korrigeerimine** kui ka tabelile **Varude üleviimine**. Seda veergu kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Supply Chain Managementi. Selle veeru vaikeväärtus on Loodud (1), kuid seda ei saadeta Supply Chain Managementi. Kui värskendate väärtuse valikule Sisestatud (2), saadetakse see Supply Chain Managementi, kuid seejärel ei saa te korrigeerimist ega üleviimist enam muuta ega uusi ridu lisada.

Tabelile **Varude korrigeerimise toode** on lisatud veerg **Numbriseeria**. See veerg tagab, et integratsioonil on kordumatu number, nii et integratsioon saab korrigeerimisi luua ja värskendada. Esimese varude korrigeerimise toote loomisel tekitab see tabelisse **P2C Automaatnummerdus** uue kirje kasutatava numbriseeria ja eesliite haldamiseks.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="supply-chain-management"></a>Supply Chain Management
Integratsiooniga loodud integratsiooni varude töölehed saab pakett-tööga automaatselt sisestada. Selle lubamiseks valige suvandid **Varude haldus > Perioodilised ülesanded > Dataverse’i integratsioon > Integratsiooni varude töölehtede sisestamine**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management): varude korrigeerimine

[![Mallide kaardistamine andmete integreerimisel, varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management): Varude korrigeerimine.](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Varude üleviimine (rakendusest Field Service rakendusse Supply Chain Management): Varude üleviimine

[![Mallide kaardistamine andmete integreerimisel, varude ülekanne (rakendusest Field Service rakendusse Supply Chain Management): Varude ülekanne.](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]