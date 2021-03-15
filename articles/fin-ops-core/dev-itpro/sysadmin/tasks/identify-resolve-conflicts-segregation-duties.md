---
title: Kohustuste jagamise konfliktide tuvastamine ja lahendamine
description: Selles teemas kirjeldatakse, kuidas tuvastada ja lahendada konflikte kohustuste jagamisel.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826364"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Kohustuste jagamise konfliktide tuvastamine ja lahendamine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas tuvastada ja lahendada konflikte kohustuste jagamisel. Saate seadistada reeglid nende kohustuste eraldamiseks, mille peavad täitma erinevad kasutajad. Seda põhimõtet nimetatakse kohustuste jagamiseks. Kui turberolli määratlus või kasutaja rollimäärangud rikuvad reegleid, logitakse konflikt. Administraator peab kõik konfliktid lahendama. Konfliktide tuvastamiseks ja lahendamiseks kasutage järgmist protseduuri.

Pärast reegli lisamist kontrollige, kas kõik olemasolevad rollid ühilduvad. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollige, kas olemasolevad rollid ja kohustused vastavad uutele kohustuste jagamise reeglitele
1. Avage **Süsteemihaldus** > **Turve** > **Kohustuste jagamine** > **Kohustuste jagamise reeglid**.
3. Valige **Kohustuste ja rollide kinnitamine**. Kui mis tahes roll rikub reegleid, kuvatakse teade, mis sisaldab reegli nime, rolli ja konfliktsete kohustuste nimesid. Konfliktsed rollid peavad olema muudetud suvandi **Turvakonfiguratsioon** abil ja need ei tohi sisaldada vastuolulisi kohustusi. Kui ükski roll valitud reeglit ei riku, kuvatakse teade, et kõik rollid vastavad.   

> [!NOTE]
> Kinnitamine tehakse ainult valitud reeglile. Oluline on kontrollida vastavust iga reegli puhul.   

Rolli loomisel või muutmisel jõustatakse kohustuste jagamise reeglid automaatselt. Rollile ei saa määrata vastuolulisi kohustusi.

Järgmisena kontrollige, kas kõik olemasolevad rollimäärangud ühilduvad.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollige, kas kasutajarolli määramised vastavad uutele kohustuste jagamise reeglitele
1. Avage **Süsteemihaldus > Turve > Kohustuste jagamine > Kasutaja rollimäärangute vastavuse kontrollimine**.
2. Valige nupp **OK**. Kuvatakse teade kinnitamise tulemustega. Konfliktid logitakse lehel **Kohustuste jagamise lahendamata konfliktid**.   

Kasutajate rollide määramisel jõustatakse kohustuste jagamise reeglid automaatselt. Kui proovite määrata kasutajat rollidele, mis sisaldavad vastuolulisi kohustusi, kuvatakse tõrketeade. Seejärel peate konflikti lahendama, keelates või lubades täiendava rollimäärangu. Lisaroll määratakse pärast määramise lubamist. 

> [!NOTE]
> Vastuolusid ei kontrollita praegu kasutajatele, kellele on Active Directory domeenigruppide alusel määratud rollid.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Konfliktsete kasutaja rollimäärangute kuvamine ja lahendamine
1. Avage **Süsteemihaldus** > **Turve** > **Kohustuste jagamine** > **Kohustuste jagamise lahendamata konfliktid**. 
2. Valige vastuolu ja valige seejärel üks järgmistest tegevustest. 

  - **Määrangu keelamine**: sellega keelatakse kasutaja määramine täiendavale turberollile. Automaatse Rollimäärangu keelamisel märgitakse kasutaja rollist välistatuks. Välistatud kasutajale ei anta rolliga seotud juurdepääsu ja teda ei saa sellesse rolli määrata seni, kuni administraator välistuse eemaldab. 
-  **Luba määramine**: see alistab vastuolu ja kasutajale on võimalik määrata täiendav turberoll. Kui alistate konflikti, siis peate sisestama põhjuse väljale **Alistamise põhjus**. Kõiki alistatud rollimääranguid saab vaadata lehel **Kohustuste jagamise konfliktid**.  

> [!NOTE]
> Kui sama kasutaja kohta on loetletud mitu konflikti, valige kasutajakirje ja hinnake lehel **Kasutajad** määratud rolle. Konflikti vältimiseks kontrollige iga reeglit pärast selle lisamist või muutmist.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]