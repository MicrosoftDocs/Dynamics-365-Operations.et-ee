---
title: "Pangakonto täpsema vastavusseviimise ülevaade"
description: "Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e069bf65e7dcab7f3b049aa786f3daff07383f4c
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-bank-reconciliation-overview"></a>Pangakonto täpsema vastavusseviimise ülevaade

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.

Pangakonto täpsema vastavusseviimise funktsioon võimaldab teil pangaväljavõtted importida. Imporditud pangaväljavõtte saab seejärel automaatselt pangakannetest vastavusse viia. Järgmiselt on toodud pangakonto täpsema vastavusseviimise voo etapid.

1.  Pangaväljavõtte impordi seadistamine.
    -   Pangaväljavõtete importimine andmeüksuse raamistiku kaudu.
    -   Kolm tavapärast pangaväljavõtte vormingut on sisse ehitatud: ISO20022, BAI2 ja MT940.
    -   Funktsiooni saab laiendada mis tahes vormingusse.

2.  Pangakonto täpsema vastavusseviimise puhul kasutatava numbriseeria seadistamine ja pangakonto vastavusseviimise vastendusreeglite määratlemine.
    -   Vastavusseviimise vastendusreegel on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja Microsoft Dynamics 365 for Finance and Operationsi, Enterprise edition, pangakande ridade filtrimiseks vastavusseviimise protsessi ajal. Olenevalt oma äritavast saate vastavusseviimise protsessi automatiseerimiseks ja optimeerimiseks seadistada rohkem kui ühe vastendusreegli.

3.  Pangaväljavõtete vastavusseviimine Finance and Operationsi pangakannetega.
    -   Vastavusseviimise töölehtede automaatne võrdlemine ja loomine.
    -   Pangaväljavõtete ja Finance and Operationsi pangakannete kuvamine kõrvuti.
    -   Finance and Operationsi pangakannete automaatne sisestamine, kui need kuvatakse pangaväljavõttel, kuid ei kuvata Finance and Operationsis.
    -   Vastavusseviimiseks väljavõtte loomine.






