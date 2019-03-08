---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (11. jaanuar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talent Core HR-i uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6e7edf52db663c7ad28f316c324d68e57bf6699a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304077"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (11. jaanuar 2019)

[!include [banner](includes/banner.md)]

**Järk 8.1.2100**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.

## <a name="changes"></a>Muudatused

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Puhkusetaotluste valideerimine, prognoosides saadaolevat saldot
Selles versioonis tehtud muudatused võimaldavad töövõtjatel taotleda tulevast puhkust seda praegusest saldost lahutamata. Kõigis tulevastes taotlustes kasutatakse standardseid töövooge. Lisateavet vt teemast [Töötundidel põhinev kumulatiivne puhkuseaeg](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Prognoositud puhkusesaldo kuvamine rakendustes Töövõtja iseteenindus ja Inimesed
See funktsioon võimaldab personaliosakonnal, juhtidel ja töövõtjatel vaadata saldosid tulevasteks puhkuseperioodideks. Töövõtjad saavad tulevasi saldosid vaadata tööruumis **Töövõtja iseteenindus** ja personaliosakond pääseb samale teabele juurde tööruumis **Inimesed**.

### <a name="notifications-for-changing-leave-balances"></a>Teatised puhkusesaldode muutmise kohta
Puhkusesaldod kuvavad töövõtjate jooksva saldo. Tulevased saldod on saadaval tööruumides **Töövõtja iseteenindus** ja **Inimesed**, sisestades prognoositud saldo arvutamiseks kuupäeva.

Prognoositud saldode kuvamiseks on lisatud navigeerimisfunktsioon järgmistele aladele.
  - Kaart **Vaba aeg** tööruumis **Töövõtja iseteenindus**.
  - Kaart **Puhkused ja puudumised** tööruumis **Juhi iseteenindus**.
  - Leht **Puhkused ja puudumised** tööruumis **Inimesed**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Kümnendkohtade lubamine ergutussüsteemi plaanides (sularahaplaanid)
Ergutussüsteemi sularahapreemiatel ja plaanidel on nüüd täiendav paindlikkus kümnendkohtadega summade ja väärtuste tühistamise suhtes.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Ergutussüsteemi registreerimistel ei saa kuupäevi pärast plaani salvestamist muuta
See muudatus võimaldab plaani lõppkuupäeva värskendada (pikendatud või aegunud) pärast plaani salvestamist. Plaane saab algus- ja kuupäevadest sõltumatult siiski aktiveerida või inaktiveerida.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Palgateave on saadaval, kui on määratud palgaarvestuse administraatori turberoll
Palgaarvestuse administraatori rolli on värskendatud juurdepääsuga palgateabele taotlusprotsessi ajal.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Töövõtja iseteenindus | Ametikohahierarhia süvitsiminek paanilt emasõlme toomiseks nurjub
Tehtud on muudatused kõrvaldamaks tõrge, mis ilmneb ametikohtade hierarhia lisamisel uutesse tööruumidesse ja organisatsiooni struktuuris navigeerimisel.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Uus valideerimisteade, kui personalinumbrite seeria on kasutusel
Tehtud on muudatus selgitamaks probleemi, mis ilmneb, kui palkate töövõtja ja järgmine personalinumber on kasutusel.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Esmase käivituslehena on valitud töövõtja iseteeninduse tööruum
Kui kasutaja esmase käivituslehena on valitud tööruum **Töötaja iseteenindus** ja kasutajale ei ole töövõtja rolli määratud, suunab süsteem ta edasi vaikearmatuurlauale.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Lõpetamise põhjusekood värskendab ametikoha määramise kirjet
Lõpetamise põhjusekood värskendab nüüd ametikoha määramist töövõtjaga töösuhte lõpetamisel ja ametikoha sulgemisel. 
