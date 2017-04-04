---
title: "Luua töö komponendid"
description: "Teema käsitleb tipptehnoloogilisi et töö võib sisaldada ja näited kasutamist nende organisatsioonis."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Luua töö komponendid

Teema käsitleb tipptehnoloogilisi et töö võib sisaldada ja näited kasutamist nende organisatsioonis. 

Töökohtade loomiseks peate seadistama mõned viiteteavet. Tööd, ainult nime loomiseks. Siiski täiendavat teavet, nt ametinimetus, lisades ette vaikeväärtused on määratud töö positsioonidel. Lisaks teie sisestatud teabest saab filtreerida hüvitiste plaanide kindlatele projektidele. Kui soovite seadistada abikõlblikkuse, mille abil saate filtreerida hüvitiste plaanide konkreetse töö, määrake ametikohustuste täitmiseks ja töö enne tööd. Need vaikeväärtused saadaval lastes säästate aega, kui lisate seisukohad töö. 

Töö, töö pealkiri, tüüp ja funktsiooni, nagu on mõnevõrra kuupäev-efektiivne. Looge töö täna, kuid ei lisa neid andmeid alles hiljem, kui vaatate seejärel töökohtade loomise kuupäeva seisuga, neid üksikasju ei kuvata. Seetõttu tuleb teil luua viide teave enne te seda nõuavad. Nii saate lisada teavet uute töökohtade loomise käigus.

## <a name="job-titles"></a>Ametinimetused
Enne tööde loomist peate seadistama tööde ametinimetused. Ametikohtade ametinimetused tuletatakse töödest, millega ametikohad seotud on. 

Säilitada ametinimetusi, kasutades selle **pealkirjad** lehele, mida saate avada kasutades otsingu funktsiooni. Kohta ning ** pealkirjad ** lehekülg, sisestage pealkirjad, mida soovite kasutada oma töökohti.

## <a name="job-types"></a>Töötüübid
Töötüübid abil saate grupeerida sarnaste töökohtade kategooriatesse. Töö ei ole kohustuslikud. Kuid kui te kavatsete kasutada töö tüüpe kompensatsioonihalduse sobivuse reeglite seadistamisel, peaksite seadistama töö tüübid enne tööde seadistamist. Töötüübid kasutavad täis- ja osalise tööajaga või palga ja tunnitasu maksta. Säilitada töötüübid abil on **töö tüübid** lehel. Kohta ning **töö tüübid** lehekülg, sisestage nimi ja administreerimiskirjeldus töö tüüp. Aastal ning **vabastada staatuse** number üks järgmistest tööd selle töö tüüp on ausa töö seaduse (FLSA) maksuvaba oleku näitamiseks,:

-   **Vabastada** – töökohti on ületunnitöö ning FLSA alusel vabastatud.
-   **Vabastamata** – töökohta ei vabastatud selle FLSA alusel ületunnitöö.
-   **Ei kohaldata** – FLSA katvus ei ole kohaldatav.

## <a name="job-functions"></a>Tööfunktsioonid
Tööd ristmikel kirjeldada kõrgetasemelise funktsioonikategooria ja kõrgetasemelisi kohustusi käsitleda. Ametikohustuste täitmiseks ei ole vajalik. Ametikohustuste täitmiseks koos töö liike, saate filtreerida hüvitiste plaanide kindlatele projektidele. On seostada ametikohustuste täitmiseks ja töö hüvitiste plaanide seadmisega abikõlblikkuse reeglid on **abikõlblikkuse eeskirjad** lehel. Seejärel saate manustada tasemete komplekti hüvitiste plaan, töö liik ja tööülesannetest, teie poolt määratletud läbi abikõlblikkuse eeskiri kombinatsiooni suhtes. (Need funktsioonid kehtivad kindlaksmääratud hüvitiste plaanide ja muutuva hüvitiste plaanide.) Aga kui kavatsete ametikohustuste täitmiseks abikõlblikkuse eeskirjad hüvitise juhtimise seadistamisel, peaksite seadistama ametikohustuste täitmiseks enne tööd. Järgmises tabelis on mõned näited ametikohustuste täitmiseks.

| Töö           | Tööfunktsioon      |
|---------------|-------------------|
| Müügijuht | Keskastme juht |
| Raamatupidaja    | Spetsialistid     |

Ametikohustuste täitmiseks säilitada abil on **tööfunktsioonide** lehel. Kohta ning **tööfunktsioonide** lehekülg, sisestage tunnuskood ja töö funktsiooni lühikirjeldus.

## <a name="job-tasks"></a>Tööülesanded
Tööülesannetest kirjeldada töötaja, kes suudab töökohta täitma põhiülesanded. Sama töö ülesanne saab lisada rohkem töökohti ja seisukohti prinditööd, mis kasutavad need töö ülesanded. Järgmises tabelis on mõned näited tööülesannetest.

<table>
<thead>
<tr class="header">
<th>Töö</th>
<th>Tööülesanne</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Müügijuht</td>
<td><ul>
<li><strong>Täiuslik-keskmiseks</strong> – läbi iga müügiisiku töötulemused.</li>
<li><strong>ABS-keskmiseks</strong> – kinnitamine või hülgamine iga müügiisiku taotluste puudumise registreerimised.</li>
</ul></td>
</tr>
<tr class="even">
<td>Raamatupidaja</td>
<td><strong>FIN-aruanne</strong> – iganädalane finantsaruannete esitada rahandusjuht.</td>
</tr>
</tbody>
</table>

Te säilitamiseks tööülesannetest ning **töö ülesanded** lehel. Kohta ning **töö ülesannete** lehekülg, sisestage nimi ja töö ülesande kirjeldus. Aastal ning **Märkus** välja, saate soovi korral sisestada lisateavet. Märkmeid saate uuendada konkreetse töö märgib, et sisestatud on siin muutmata.

## <a name="areas-of-responsibility"></a>Vastutusalad
Vastutusalasid saate tööülesanded, protsesse ja tooteid, mis on töötaja, kes suudab töö. Näiteks võib olla ühes valdkonnas tööd, mille nimi on "Raamatupidaja", "Finantsaruandluse toote a valimist" Te säilitamiseks vastutusalad ning **kohta** lehekülg, mille leiad otsingufunktsiooni abil. Kohta ning **kohta** lehekülg, sisestage nimi ja kirjeldus vastutusala. Aastal ning **Märkus** välja, saate soovi korral sisestada lisateavet. Märkmeid saate uuendada konkreetse töö märgib, et sisestatud on siin muutmata.


