---
title: Kohustuste jagamise konfliktide tuvastamine ja lahendamine
description: Selles teemas kirjeldatakse, kuidas tuvastada ja lahendada konflikte kohustuste jagamisel.
author: peakerbl
manager: AnnBe
ms.date: 07/08/2019
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
ms.openlocfilehash: b7e25a568b86ce3161e2c52045ff2361c0bc4a0e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681590"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Kohustuste jagamise konfliktide tuvastamine ja lahendamine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas tuvastada ja lahendada konflikte kohustuste jagamisel. Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad. Seda põhimõtet nimetatakse kohustuste jagamiseks. Kui turberolli määratlus või kasutaja rollimäärangud rikuvad reegleid, logitakse konflikt. Administraator peab kõik konfliktid lahendama. Konfliktide tuvastamiseks ja lahendamiseks kasutage järgmist protseduuri. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollige, kas kasutajarolli määramised vastavad uutele kohustuste jagamise reeglitele.
1. Avage **Navigeerimispaan > Moodulid > Süsteemiadministratsioon > Turvalisus > Kohustuste jagamine > Kinnita kasutajarollide rollimääramise vastavuse**.
2. Valige nupp **OK**. Kuvatakse teade kinnitamise tulemustega. Konflikti korral saate avada lehe **Kasutajad** ja muuta kasutaja rollimääranguid. Konfliktid logitakse ka lehele **Kohustuste jagamise konfliktid**. Kinnitusprotsessi käitamiseks pakett-tööna valige suvand **Pakktöötlus** ja seejärel seadistage muud partii parameetrid. Pärast pakett-töö käitamist saate konfliktid üle vaadata lehel **Kohustuste jagamise konfliktid**.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Konfliktsete kasutaja rollimäärangute kuvamine ja lahendamine
1. Avage **Navigeerimispaan > Moodulid > Süsteemiadministratsioon > Turvalisus > Kohustuste jagamine > Kohustuste konfliktide jagamine**. Valige konflikt ja seejärel klõpsake ühte järgmistest nuppudest: **määrangu keelamine – kasutajale täiendava turberolli määrangu keelamine**. Automaatse Rollimäärangu keelamisel märgitakse kasutaja rollist välistatuks. Välistatud kasutajale ei anda rolliga seotud juurdepääsu ja kasutajat ei saa sellesse rolli määrata seni, kuni administraator välistuse eemaldab. Luba määramine – **Alista** konflikt ja kasutajale on võimalik määrata mõlemad turberollid. Kui alistate konflikti, siis peate sisestama põhjuse väljale **Alistamise põhjus**.  
2. Sulgege leht.
3. Avage **Navigeerimispaan > Moodulid > Süsteemiadministratsioon > Turvalisus > Kohustuste jagamine > Kohustuste lahendamata konfliktide jagamine**. Valige konflikt ja seejärel klõpsake ühte järgmistest nuppudest: **määrangu keelamine – kasutajale täiendava turberolli määrangu keelamine**. Automaatse Rollimäärangu keelamisel märgitakse kasutaja rollist välistatuks. Välistatud kasutajale ei anda rolliga seotud juurdepääsu ja kasutajat ei saa sellesse rolli määrata seni, kuni administraator välistuse eemaldab. Luba määramine – **Alista** konflikt ja kasutajale on võimalik määrata mõlemad turberollid. Kui alistate konflikti, siis peate sisestama põhjuse väljale **Alistamise põhjus**.    
4. Sulgege leht.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollige, kas olemasolevad rollid vastavad uutele kohustuste jagamise reeglitele.
1. Avage **Navigeerimispaan > Moodulid > Süsteemiadministratsioon > Turvalisus > Kohustuste jagamine > Kohustuste reeglite jagamine**. Valige reegel.  
2. Valige **Kohustuste ja rollide kinnitamine**. Kui mis tahes olemasolev roll rikub valitud reeglit, kuvatakse teade, mis sisaldab rolli nime ja konfliktsete kohustuste nimesid. Administraator peab kas näitama turberiski vähendamist või muutma rolli, nii et see ei rikuks kohustuste jagamise reegleid. Kui ükski roll valitud reeglit ei riku, kuvatakse teade, et kõik rollid on vastavuses.  

