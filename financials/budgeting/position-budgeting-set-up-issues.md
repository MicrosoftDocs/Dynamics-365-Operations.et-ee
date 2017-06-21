---
title: "Ametikoha eelarvestamise tõrkeotsing"
description: "Selles artiklis on vastused küsimustele, mis võivad teil ametikoha eelarvestuse konfigureerimisel tekkida. Käsitletud on korduma kippuvaid küsimusi selle kohta, kuidas luua eelarve kuluelemente, hüvitusgruppe ja hüvitusruudustikke."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3fe1e1842b1cd808d35105ec7ec494107127690
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="position-budgeting-troubleshooting"></a>Ametikoha eelarvestamise tõrkeotsing

[!include[banner](../includes/banner.md)]


Selles artiklis on vastused küsimustele, mis võivad teil ametikoha eelarvestuse konfigureerimisel tekkida. Käsitletud on korduma kippuvaid küsimusi selle kohta, kuidas luua eelarve kuluelemente, hüvitusgruppe ja hüvitusruudustikke. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Miks ma ei leia inimressursside moodulis prognoositavat ametikohta?
---------------------------------------------------------------

Prognoositavad ametikohad on teisaldatud eelarvestamise moodulisse.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Miks ma ei saa kustutada eelarve kuluelementi?
Prognoositavale ametikohale määratud eelarve kuluelementi ei saa kustutada. Enne eelarvekulu elemendi kustutamist tuleb see kõigist prognoositavatest ametikohtadest eemaldada. **Näpunäide:** kõigi ametikohtade leidmiseks, millele eelarve kuluelement on määratud, valige kuluelement lehelt **Eelarve kuluelemendid** ja klõpsake siis käsku **Uuenda ametikohti**. Kuluelementi kasutavad ametikohad on loetletud ülemisel ruudustikul.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Kuidas saan eemaldada kuluelemendi mitmelt prognoositavalt ametikohalt, ilma et peaks neid kõiki avama?
Kuluelementi ei saa eemaldada. Kuid kui muudate algus- ja lõppkuupäeva nii, et need jäävad väljapoole eelarve planeerimise tsükli kuupäevi, siis ei määrata kuluelementi enam eelarve planeerimise tsüklis prognoositavatele ametikohtadele. Selle muudatuse tegemiseks avage eelarve kuluelement ja klõpsake siis kiirkaardil **Kuluarvestus** käsku **Muuda kuupäevi** ning muutke jõustumiskuupäeva või aegumiskuupäeva. Seejärel klõpsake nuppu **OK**, et muuta automaatselt kõiki prognoositavaid ametikohti, millele kuluelement on määratud. **Näpunäide:** selle meetodi kasutamisel arvestage, et see eemaldab eelarve kuluelemendi **kõigilt** prognoositavatelt ametikohtadelt, kui alguse ja lõpu kuupäevad ei ole enam sobivas vahemikus. Kui te seda ei soovi, peate avama iga prognoositava ametikoha, millelt soovite eelarve kuluelementi eemaldada, ja tegema muudatuse käsitsi.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Miks ma ei saa sisestada aasta summat eelarve kuluelemendi kiirkaardile Kulu kalkulatsioon?
Te ei saa sisestada aasta summat, kui kiirkaardil **Kalkulatsiooni alus** on eelarve kuluelemendid, sest süsteem nõuab väärtuse arvutamiseks protsenti. Väärtuse muutmiseks eemaldage kiirkaardilt **Kalkulatsiooni alus** kõik eelarve kuluelemendid.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Miks ma ei saa muuta eelarve kulu tüüpi „teenimine” muuks eelarve kulu tüübiks?
Mõned eelarve kuluelemendid kasutavad kuluelementi „teenimine” arvutuse alusena. Välja **Eelarve kulu tüüp** muutmiseks eemaldage tulu kuluelement kõigi eelarve kuluelementide kiirkaardilt **Kalkulatsiooni alus**.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Miks ma ei saa muuta eelarve kuluelemendi ridadel eelarve kuluelemendi kuupäeva?
Eelarve kuluelemendi rea kuupäeva ei saa muuta siis, kui prognoositav ametikoht kasutab eelarve kuluelementi. See piirang aitab tagada, et prognoositavad ametikohad on alati eelarve kuluelemendi piires. Kuupäeva muutmiseks klõpsake kiirkaardil **Kulu kalkulatsioon** valikut **Muuda kuupäevi** ja sisestage uued kuupäevad. Seejärel klõpsake nuppu **OK**, et muuta prognoositavaid ametikohti, millele kuluelement on määratud.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Miks ma ei saa muuta eelarve kuluelemendi kulusid lehel Hüvitusgrupp?
Eelarve kuluelemente saab luua ja muuta ainult lehel **Eelarve kuluelemendid**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Miks ma saan tõrketeate, kui muudan prognoositava ametikoha kuluelemendi kuupäevi?
Prognoositava ametikoha kuluelemendi real olevad kuupäevad peavad jääma järgmistesse vahemikesse.

-   Ametikoha aktiveerimis- ja kõrvaldamiskuupäevad.
-   Eelarve kuluelemendi aktiveerimis- ja aegumiskuupäevad.
-   Prognoositava ametikoha eelarve planeerimise protsessiga seostatud eelarvetsükli algus- ja lõppkuupäevad.





