---
title: "Pangakonto täpsema vastavusseviimise ülevaade"
description: "Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Pangakonto täpsema vastavusseviimise ülevaade

Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.

Pangakonto täpsema vastavusseviimise funktsioon võimaldab teil pangaväljavõtted importida. Imporditud pangaväljavõtte saab seejärel automaatselt pangakannetest vastavusse viia. Järgmiselt on toodud pangakonto täpsema vastavusseviimise voo etapid.

1.  Pangaväljavõtte impordi seadistamine.
    -   Pangaväljavõtete importimine andmeüksuse raamistiku kaudu.
    -   Kolm tavapärast pangaväljavõtte vormingut on sisse ehitatud: ISO20022, BAI2 ja MT940.
    -   Funktsiooni saab laiendada mis tahes vormingusse.

2.  Pangakonto täpsema vastavusseviimise puhul kasutatava numbriseeria seadistamine ja pangakonto vastavusseviimise vastendusreeglite määratlemine.
    -   Reeglina leppimise sobitamine on kogum alusel filtreerida panga väljavõtte read ja Microsoft Dynamics 365 operatsioonid panga ridu kooskõlastusprotsessi ajal. Sõltuvalt ettevõtte äritegevuse saate seadistada mitu vastavat reeglit automatiseerida ja optimeerida oma kooskõlastusprotsessi.

3.  Panga väljavõtteid Dynamics 365 toimingute pangatehingute vastavusse viia.
    -   Vastavusseviimise töölehtede automaatne võrdlemine ja loomine.
    -   Pangaväljavõtete vaatamine ja Dynamics 365 toimingute pangatehingute kõrvuti.
    -   Automaatselt postitada Dynamics 365 toimingute pangatehingute kui nad ilmuvad pangaväljavõte, kuid ei kuvata Dynamics 365 toiminguteks.
    -   Vastavusseviimiseks väljavõtte loomine.




