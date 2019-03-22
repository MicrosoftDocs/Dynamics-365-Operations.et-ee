---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (31. jaanuar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ab43bab53afd979d64099425f0582f6c1bb5a8b0
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/08/2019
ms.locfileid: "377846"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (31. jaanuar 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Dynamics 365 for Talenti uusi või muutunud funktsioone

**Järk 8.1.2128**

## <a name="core-hr-changes"></a>Core HR-i muudatused

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Puhkusel olevate inimeste kaardil olev vaba aeg ei võta arvesse puhkuseplaani kuupäevi
Nende puhul, kellel on puhkuseplaanid, mida kalendriaastas ei rakendata, kuvatakse nüüd kaardil **Võetud** vaba aeg, mis on võetud määratletud puhkuseplaaniga aastal. Näiteks kui organisatsiooni puhkuseaasta on 1. juunist 30. maini ja töövõtja on võtnud detsembris kolm vaba päeva, kuvatakse 15. jaanuaril kaardil **Võetud** kolm päeva. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Kogunenud summad ei vasta järgu kuupäevale
Puhkustele ja puudumistele (suvandi **Inimressursid** parameetrid) on lisatud uued suvandid, mis võimaldavad klientidel määrata töövõtjate töötatud kuude kehtivusaja. Mõne organisatsiooni puhul on see kuu lõpus, teiste puhul võib olla järgmise kuu alguses. Näiteks võib üks organisatsioon võimaldada vaba aja 31. detsembril, teine aga 1. jaanuaril. See suvand võimaldab valida vaba aja toimumisaja. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Töötaja värbamistoimingud on kinni jäänud olekusse Töövoog on lõpetatud
Tehtud on muudatused, et parandada probleem, milles väike hulk töövoogusid lõpevad olekuga Töövoog on lõpetatud. Uued töövood peaksid nüüd minema töövoo lõppemisel olekusse Lõpule viidud. Kõik töövood, mille olek on Töövoog on lõpetatud, viiakse tõrkeolekusse, et võimaldada selle värskendamist või eemaldamist. 
