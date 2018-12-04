---
title: "Pangakonto täpsema vastavusseviimise ülevaade"
description: "Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ff59250b836a73986848109ce48f843fed1d71a9
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="advanced-bank-reconciliation-overview"></a>Pangakonto täpsema vastavusseviimise ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.

Pangakonto täpsema vastavusseviimise funktsioon võimaldab teil pangaväljavõtted importida. Imporditud pangaväljavõtte saab seejärel automaatselt pangakannetest vastavusse viia. Järgmiselt on toodud pangakonto täpsema vastavusseviimise voo etapid.

1.  Pangaväljavõtte impordi seadistamine.
    -   Pangaväljavõtete importimine andmeüksuse raamistiku kaudu.
    -   Kolm tavapärast pangaväljavõtte vormingut on sisse ehitatud: ISO20022, BAI2 ja MT940.
    -   Funktsiooni saab laiendada mis tahes vormingusse.

2.  Pangakonto täpsema vastavusseviimise puhul kasutatava numbriseeria seadistamine ja pangakonto vastavusseviimise vastendusreeglite määratlemine.
    -   Vastavusseviimise vastendusreegel on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja Microsoft Dynamics 365 for Finance and Operationsi pangakande ridade filtrimiseks vastavusseviimise protsessi ajal. Olenevalt oma äritavast saate vastavusseviimise protsessi automatiseerimiseks ja optimeerimiseks seadistada rohkem kui ühe vastendusreegli.

3.  Pangaväljavõtete vastavusseviimine Finance and Operationsi pangakannetega.
    -   Vastavusseviimise töölehtede automaatne võrdlemine ja loomine.
    -   Pangaväljavõtete ja Finance and Operationsi pangakannete kuvamine kõrvuti.
    -   Finance and Operationsi pangakannete automaatne sisestamine, kui need kuvatakse pangaväljavõttel, kuid ei kuvata Finance and Operationsis.
    -   Vastavusseviimiseks väljavõtte loomine.






