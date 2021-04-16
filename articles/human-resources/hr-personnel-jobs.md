---
title: Töö komponentide seadistamine
description: See artikkel kirjeldab töö võimalikke põhielemente ja toob näiteid, kuidas saate neid elemente oma organisatsioonis kasutada.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c481a468b2d624f029082fe27e7f14ecf7c068d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803485"
---
# <a name="set-up-the-components-of-a-job"></a>Töö komponentide seadistamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab töö võimalikke põhielemente ja toob näiteid, kuidas saate neid elemente oma organisatsioonis kasutada. 

Enne tööde loomist tuleb seadistada teatud viiteteave. Saate luua töö, millel on ainult nimi. Täiendava teabe, näiteks ametinimetuse, lisamisega pakute aga tööle määratud ametikohtade vaikeväärtused. Peale selle saab osa sisestatud teavet kasutada teatud töödele tasuplaanide filtreerimiseks. Kui soovite seadistada sobivuse, mida saate kasutada kindlale tööle tasuplaanide filtreerimiseks, peate enne tööde seadistamist seadistama tööfunktsioonid ja töötüübid. Kui need vaikeväärtused on saadaval, hoiate tööle ametikohtade lisamisel aega kokku. 

Mõned töö üksikasjad, nagu ametinimetus, töö tüüp ja funktsioon, on kuupäevaliselt jõustuvad. Kui loote töö täna, kuid ei lisa nimetatud üksikasju kohe, ja otsite hiljem tööd loomiskuupäeva alusel, siis neid üksikasju ei kuvata. Seetõttu peate vajaliku viiteteabe enne selle otsimist looma. Nii saate lisada teabe uutele töödele juba nende loomisel.

## <a name="job-titles"></a>Ametinimetused
Enne tööde loomist peate seadistama tööde ametinimetused. Ametikohtade ametinimetused tuletatakse töödest, millega ametikohad seotud on. 

Ametinimetusi saate hallata lehel **Ametinimetused**, millele pääsete juurde otsingufunktsiooni abil. Lehel **Ametinimetused** saate sisestada ametinimetused, mida kavatsete oma tööde jaoks kasutada.

## <a name="job-types"></a>Töötüübid
Sarnaste tööde kategooriatesse grupeerimiseks saate kasutada töötüüpe. Töötüübid ei ole nõutavad. Kuid kui te kavatsete kasutada töö tüüpe kompensatsioonihalduse sobivuse reeglite seadistamisel, peaksite seadistama töö tüübid enne tööde seadistamist. Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ja tunnipalk. Töötüüpe saate hallata lehel **Töötüübid**. Sisestage lehel **Töötüübid** töötüübi nimi ja lühikirjeldus. Tehke väljal **Vabastatud olek** üks järgmistest valikutest, et näidata selle töötüübiga tööde õiglaste tööstandardite seaduse (FLSA) alusel vabastatud olekut.

-   **Vabastatud** – tööd on FLSA alusel ületunnitööst vabastatud.
-   **Mittevabastatud** – tööd ei ole FLSA alusel ületunnitööst vabastatud.
-   **Ei kohaldu** – FLSA kate ei kohaldu.

## <a name="job-functions"></a>Tööfunktsioonid
Tööfunktsioonid kirjeldavad kõrgetasemelisi funktsioonikategooriaid ja seotud kõrgetasemelisi kohustusi. Tööfunktsioonid ei ole nõutavad. Saate kasutada tööfunktsioone koos töötüüpidega, et filtreerida konkreetsete tööde tasuplaane. Seostage tööfunktsioonid ja töötüübid tasuplaanidega, seadistades sobivuse reeglid lehel **Sobivuse reeglid**. Seejärel saate lisada tasuplaanile ka tasemete komplekti, mida rakendada töötüübi/tööfunktsiooni kindla kombinatsiooni korral, mille määratlesite sobivuse reeglitega. (Need omadused kehtivad nii fikseeritud kui ka muutuvate tasuplaanide korral.) Kui te kavatsete siiski kasutada tööfunktsioone tasuhalduse jaoks sobivuse reeglite seadistamisel, peate seadistama tööfunktsioonid enne tööde seadistamist. Järgmises tabelis on toodud mõned tööfunktsioonide näited.

| Töö           | Tööfunktsioon         |
|---------------|----------------------|
| Müügijuht | Keskmise taseme haldur    |
| Raamatupidaja    | Professionaalid        |

Tööfunktsioone saate hallata lehel **Tööfunktsioonid**. Sisestage lehel **Tööfunktsioonid** tööfunktsiooni ID-kood ja lühikirjeldus.

## <a name="job-tasks"></a>Tööülesanded
Tööülesanded kirjeldavad teatud töö ametikohal tegutseva töötaja põhiülesandeid. Sama tööülesande saab lisada mitmele tööle ja neid tööülesandeid kasutavate tööde ametikohtadele. Järgmises tabelis on toodud mõned tööülesannete näited.

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
<li><strong>Jõudluse ülevaade</strong> – iga müüja tööjõudluse ülevaade.</li>
<li><strong>Puudumiste ülevaade</strong> – iga müüja puudumistaotluste või registreeringute kinnitamine või tagasilükkamine.</li>
</ul></td>
</tr>
<tr class="even">
<td>Raamatupidaja</td>
<td><strong>Finantsaruanne</strong> – iganädalaste finantsaruannete esitamine pealaekurile.</td>
</tr>
</tbody>
</table>

Tööülesandeid saate hallata lehel **Tööülesanded**. Sisestage lehel **Tööülesanded** tööülesande nimi ja lühikirjeldus. Väljale **Märkus** saate soovi korral sisestada ka lisateavet. Märkusi saab kindla töö puhul värskendada ilma siia sisestatud märkusi muutmata.

## <a name="areas-of-responsibility"></a>Vastutusalad
Vastutusalade abil saate näidata, milliste töörollide, protsesside ja toodete eest selle töö ametikohal tegutsev töötaja vastutab. Näiteks töö „Raamatupidaja” vastutusala võib olla „Toote A finantsaruandlus”. Vastutusalasid saate hallata lehel **Vastutusalad**, millele pääsete juurde otsingufunktsiooni abil. Sisestage lehel **Vastutusalad** vastutusala nimi ja lühikirjeldus. Väljale **Märkus** saate soovi korral sisestada ka lisateavet. Märkusi saab kindla töö puhul värskendada ilma siia sisestatud märkusi muutmata.

## <a name="steps-for-creating-a-job"></a>Töö loomise juhised
Uue töö loomise etapiviisilise protseduuri leiate artiklist [Uute tööde määratlemine](../fin-and-ops/hr/tasks/define-new-jobs.md). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]