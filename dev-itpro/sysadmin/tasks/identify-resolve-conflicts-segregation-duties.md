--- 
title: Konfliktide tuvastamine ja lahendamine kohustuste jagamisel
description: "Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: fdc0bbd0a239c8d7719271445a4d6a5323e87aad
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Konfliktide tuvastamine ja lahendamine kohustuste jagamisel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad. Seda põhimõtet nimetatakse kohustuste jagamiseks. Kui turberolli määratlus või kasutaja rollimäärangud rikuvad reegleid, logitakse konflikt. Administraator peab kõik konfliktid lahendama. Konfliktide tuvastamiseks ja lahendamiseks kasutage järgmist protseduuri. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollige, kas kasutajarolli määramised vastavad uutele kohustuste jagamise reeglitele.
1. Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kasutaja rollimäärangute vastavuse kontrollimine.
2. Klõpsake nuppu OK.
    * Kuvatakse teade kinnitamise tulemustega.     Konflikti korral saate avada lehe Kasutajad ja muuta kasutaja rollimääranguid. Konfliktid logitakse ka lehele Kohustuste jagamise konfliktid.     Kinnitusprotsessi käitamiseks pakett-tööna valige suvand Pakktöötlus ja seejärel seadistage muud partii parameetrid. Pärast pakett-töö käitamist saate konfliktid üle vaadata lehel Kohustuste jagamise konfliktid.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Konfliktsete kasutaja rollimäärangute kuvamine ja lahendamine
1. Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kohustuste jagamise konfliktid.
    * Valige konflikt ja seejärel klõpsake ühte järgmistest nuppudest: määrangu keelamine – kasutajale täiendava turberolli määrangu keelamine. Automaatse Rollimäärangu keelamisel märgitakse kasutaja rollist välistatuks. Välistatud kasutajale ei anda rolliga seotud juurdepääsu ja kasutajat ei saa sellesse rolli määrata seni, kuni administraator välistuse eemaldab.     Luba määramine – konflikt alistatakse ja kasutajale on võimalik määrata mõlemad turberollid. Kui alistate konflikti, siis peate sisestama põhjuse väljale Alistamise põhjus.  
2. Sulgege leht.
3. Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kohustuste jagamise lahendamata konfliktid.
    * Valige konflikt ja seejärel klõpsake ühte järgmistest nuppudest: määrangu keelamine – kasutajale täiendava turberolli määrangu keelamine. Automaatse Rollimäärangu keelamisel märgitakse kasutaja rollist välistatuks. Välistatud kasutajale ei anda rolliga seotud juurdepääsu ja kasutajat ei saa sellesse rolli määrata seni, kuni administraator välistuse eemaldab.     Luba määramine – konflikt alistatakse ja kasutajale on võimalik määrata mõlemad turberollid. Kui alistate konflikti, siis peate sisestama põhjuse väljale Alistamise põhjus.    
4. Sulgege leht.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollige, kas olemasolevad rollid vastavad uutele kohustuste jagamise reeglitele.
1. Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kohustuste jagamise reeglid.
    * Valige reegel.  
2. Klõpsake suvandit Kohustuste ja rollide kinnitamine.
    * Kui mis tahes olemasolev roll rikub valitud reeglit, kuvatakse teade, mis sisaldab rolli nime ja konfliktsete kohustuste nimesid. Administraator peab kas näitama turberiski vähendamist või muutma rolli, nii et see ei rikuks kohustuste jagamise reegleid.     Kui ükski roll valitud reeglit ei riku, kuvatakse teade, et kõik rollid on vastavuses.  


