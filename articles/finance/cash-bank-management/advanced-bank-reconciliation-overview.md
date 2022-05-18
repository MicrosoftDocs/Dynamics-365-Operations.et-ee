---
title: Pangakonto täpsema vastavusseviimise ülevaade
description: Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.
author: panolte
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6dadc5fd49a7103df8e1cacfd3be09c24a06e67
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711404"
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
    -   Vastavusseviimise vastavusse viimise reegel on kriteeriumite kogum, mida kasutatakse pangaväljavõtte ridade Microsoft Dynamics ja 365 Finantspanga kande ridade filtreerimiseks vastavusseviimise protsessi ajal. Olenevalt oma äritavast saate vastavusseviimise protsessi automatiseerimiseks ja optimeerimiseks seadistada rohkem kui ühe vastendusreegli.

3.  Pangaväljavõtete vastavusseviimine Finance'i pangakannetega.
    -   Vastavusseviimise töölehtede automaatne võrdlemine ja loomine.
    -   Pangaväljavõtete ja Finance'i pangakannete kuvamine kõrvuti.
    -   Finance'i pangakannete automaatne sisestamine, kui need kuvatakse pangaväljavõttel, kuid ei kuvata rakenduses Finance.
    -   Vastavusseviimiseks väljavõtte loomine.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
