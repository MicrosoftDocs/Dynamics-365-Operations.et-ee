---
title: "Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimise ja üleviimise sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimise ja üleviimise sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Järgmist malli ja aluseks olevaid ülesandeid kasutatakse varude korrigeerimise ja üleviimise sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.

**Mallide nimi andmete integratsioonis:**
- Varude korrigeerimine (rakendusest Field Service rakendusse Finance and Operations)
- Varude üleviimine (rakendusest Field Service rakendusse Finance and Operations)

**Ülesannete nimed andmete integratsiooni projektides.**
- Varude korrigeerimine
- Varude üleviimine

## <a name="entity-set"></a>Üksuste komplekt
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-i varude korrigeerimise töölehe päised ja read |
| msdyn_inventoryadjustmentproducts | CDS-i varude üleviimise töölehe päised ja read   |

## <a name="entity-flow"></a>Üksuse voog
Rakenduses Field Service tehtud varude korrigeerimine ja üleviimine sünkroonitakse rakendusse Finance and Operations siis, kui **Sisestuse olek** muudetakse olekust Loodud olekusse Sisestatud. Kui see juhtub, lukustatakse korrigeerimise või üleviimise käsk ja see muutub kirjutuskaitstuks, sest korrigeerimisi ja üleviimisi võib sisestada rakenduses Finance and Operations ning seega neid ei saa muuta.
Rakenduses Finance and Operations saate seadistada pakett-töö automaatselt korrektuure sisestama ja integratsiooniga loodud laotöölehti üle kandma. Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus 
Toote üksuse alla on lisatud väli Laoüksus. See väli on vajalik, sest Müügi- ja laoühik ei ole Operationsis alati sama ning meil on Operationsis Laoüksust Laovarude jaoks vaja.
Kui seadistate Toote Varude korrigeerimise Toote nii Varude korrigeerimise kui ka Varude üleviimise jaoks, võetakse Üksus Toote Laotoote väärtusest. Kui väärtus leitakse, lukustatakse väli Varude korrigeerimise tootele

Väli Sisestuse olek on lisatud nii Varude korrigeerimise üksusele kui ka Varude üleviimise üksusele. Seda välja kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Operationsi. Välja vaikeväärtuseks on Loodud (1) ja seejärel ei saadeta seda edasi Operationsi. Kui muudate selle väärtuseks Sisestatud (2), saadetakse see edasi Operationsi, kuid siis ei saa te enam midagi Korrigeerimise või Üleviimise all muuta ega sellele ridu lisada.
Varude korrigeerimise tooteüksusele on lisatud väli Numbrijada. See väli aitab integratsioonil omada kordumatut koodi, et integratsioon teaks, millal teha loomisi ja millal värskendusi. Esimese Varude korrigeerimise toote loomisel tekitab see uue kirje P2C Automaatnummerduse üksusesse kasutatava numbrijada ja prefiksi säilitamiseks.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="in-finance-and-operations"></a>Rakenduses Finance and Operations
Integratsiooni loodud integratsiooni laotöölehed saab pakett-tööga automaatselt postitada. Selle lubamiseks avage: Varude haldus > Perioodilised ülesanded > CDS-integratsioon > Integratsiooni laotöölehe sisestamine

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Varude korrigeerimine (Field Service'ist Finance and Operationsisse): Varude korrigeerimine

[![Malli vastendamine andmete integratsioonis](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Varude üleviimine (Field Service'ist Finance and Operationsisse): Varude üleviimine

[![Malli vastendamine andmete integratsioonis](./media/FSTrans1.png)](./media/FSTrans1.png)

