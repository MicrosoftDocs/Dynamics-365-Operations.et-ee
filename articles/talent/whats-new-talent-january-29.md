---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (31. jaanuar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690048"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (31. jaanuar 2019)

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

**Järk 8.1.2128**

## <a name="core-hr-changes"></a>Core HR-i muudatused

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Puhkusel olevate inimeste kaardil olev vaba aeg ei võta arvesse puhkuseplaani kuupäevi
Puhkuseplaanide puhul, mida kalendriaastas ei rakendata, kuvatakse nüüd kaardil **Võetud** vaba aeg, mis on võetud määratletud puhkuseplaaniga aastal. Näiteks kui organisatsiooni puhkuseaasta on 1. juunist 30. maini ja töövõtja on võtnud detsembris kolm vaba päeva, kuvatakse 15. jaanuaril kaardil **Võetud** 3 päeva. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Kogunenud summad ei vasta järgu kuupäevale
Puhkustele ja puudumistele (suvandi **Inimressursid** parameetrid) on lisatud uued suvandid, mis võimaldavad klientidel määrata töövõtjate töötatud kuude kehtivusaja. Mõne organisatsiooni puhul on see kuu lõpus, teiste puhul võib olla järgmise kuu alguses. Näiteks võib üks organisatsioon võimaldada vaba aja 31. detsembril, teine aga 1. jaanuaril. See suvand võimaldab valida vaba aja toimumisaja. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Töötaja värbamistoimingud on kinni jäänud olekusse Töövoog on lõpetatud
Tehtud on muudatused, et parandada probleem, milles väike hulk töövoogusid lõpevad olekuga Töövoog on lõpetatud. Uued töövood peaksid nüüd minema töövoo lõppemisel olekusse Lõpule viidud. Kõik töövood, mille olek on Töövoog on lõpetatud, viiakse tõrkeolekusse, et võimaldada selle värskendamist või eemaldamist. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]