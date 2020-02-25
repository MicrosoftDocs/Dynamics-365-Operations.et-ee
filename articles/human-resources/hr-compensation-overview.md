---
title: Hüvitusplaanid
description: Hüvitise ja eeliste haldurid saavad kasutada hüvituste haldust, et hallata ning töödelda organisatsiooni töötajate fikseeritud ja ergutussüsteemi plaane.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1b2494ac717bc8c0171be49cc39e6aefff4425ab
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008803"
---
# <a name="compensation-plans"></a>Hüvitusplaanid

Hüvitise ja eeliste haldurid saavad kasutada hüvituste haldust, et hallata ning töödelda organisatsiooni töötajate fikseeritud ja ergutussüsteemi plaane.

### <a name="introduction"></a>Sissejuhatus

Tasuhaldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks. Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu. Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu. 

Töötajaid saab registreerida ühes või mitmes mõlemat tüüpi plaanis. Töötaja peab vastama järgmistele nõuetele, et tal oleks õigus tasuplaanis registreeruda.
-   Töötaja peab olema määratud aktiivsele ametikohale.
-   Töötaja peab vastama tasuplaani sobivusreeglitega määratletud kriteeriumidele.

## <a name="compensation-setup"></a> Tasu seadistamine
Järgmises tabelis on tasuprotsessi komponendid, mis võivad kuuluda teie ettevõtte tasuplaanide seadistusse.

<table>
<thead>
<tr class="header">
<th>Komponent</th>
<th>Lisateave ...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Põhipalga tegevused</td>
<td>Põhipalga toimingutel on kaks eesmärki.
<ul>
<li>Tegevused võivad määrata teabe liigi, mida tuleb salvestada, kui töötaja tasu muutub. Näiteks võite nõuda, et salvestatakse muudatuse põhjus (nt edutamine või madalamale ametikohale viimine).</li>
<li>Tegevused saavad tagada arvutuse rakendamise põhipalga plaanide töötlemisel.  Näiteks võrdlevad tegevused, mille tüüp on Omakapital, töötajate palka töötaja taseme minimaalse võrdluspunktiga ja tagavad, et töötajale makstakse vähemalt miinimum.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tasemed</td>
<td>Tasemed seostatakse töödega ning kõigi töö viitega seotud ametikohtadega. Saate luua diskreetseid tasemeid kolme tüüpi tasuplaanidele: klass, astmik ja etapp.</td>
</tr>
<tr class="odd">
<td>Palgavahemiku kasutusastme maatriks</td>
<td>Vahemiku kasutusmaatriks aitab viia töötajaid üle nende töö kontrollpunkti. Vahemiku kasutust saate kasutada ka ettevõttesiseste tasumäärade õigluse kontrollimiseks, pööramata tähelepanu töötaja individuaalsetele tulemustele või ettevõtte üldistele tulemustele. Näiteks oma vahemikus väiksemapalgalised töötajad saavad kõrgema protsendiga palgatõuse, kui selles vahemikus suuremapalgalised töötajad. Sel viisil saate tasakaalustada süstemaatiliselt omakapitali erinevusi. Vahemikukasutus arvutatakse järgmiselt: (fikseeritud palgamäär – vahemiku miinimum) ÷ (vahemiku maksimum – vahemiku miinimum).</td>
</tr>
<tr class="even">
<td>Viitepunktide seadistus</td>
<td>Viitepunkti seadistus hõlmab viitepunktide komplekti, mis kajastavad tasumäära maatriksi vahemikke. Iga vahemikku saab seostada tasumääraga. Näiteks on klassiplaanide viitepunktid sageli miinimum, keskpunkt ja maksimum.</td>
</tr>
<tr class="odd">
<td>Tasumaatriks</td>
<td>Tasumaatriks on viitepunktide ja tasemete kogum, mida kasutatakse tasustruktuuri loomiseks.</td>
</tr>
<tr class="even">
<td>Kompensatsiooni struktuur</td>
<td>Tasustruktuur on tasumaatriks, mille tasumäärad on seotud iga taseme viitepunktidega.</td>
</tr>
<tr class="odd">
<td>Sobivuse reeglid</td>
<td>Sobivusreegleid kasutatakse konkreetsete tasuplaanidega kaetud tööde, tööfunktsioonide, töö tüüpide, osakondade, ametiühingute või tasupiirkondadega seotud töötajate tuvastamiseks. Sobivusreeglid tuleb luua nii ergutussüsteemi kui ka põhipalga plaanide jaoks, et töötajaid plaani registreerida. Kui tasuplaani sobivusreeglid on määratud, saab määratleda tasemed, mida tuleb plaaniga hõlmatud tööde puhul rakendada.</td>
</tr>
<tr class="even">
<td>Tasusagedused</td>
<td>Maksmise sagedusi kasutatakse ajaperioodi määratlemiseks, millele tasu on määratud.  Näiteks aitab maksmise sagedus aru saada, kas tasusumma on määratud iga-aastase palgana või tunnitasu määrana. Maksmise sagedust kasutatakse ka teisendustegurite seadistamiseks, et teisendada kuu, nädala, kahe nädala ja tunni tasusummad iga-aastaseks maksesageduseks.</td>
</tr>
<tr class="odd">
<td>Hüvitise regioonid</td>
<td>Tasupiirkondi kasutatakse töötaja tasu määramiseks töökoha asukoha põhjal.</td>
</tr>
<tr class="even">
<td>kontrollpunkt</td>
<td>Kontrollpunkt näitab, seda, mida peetakse tasu tasemel ideaalseks tasumääraks kõigi töötajate puhul. Taseme plaanide struktuuride puhul on kontrollpunktid tavaliselt vahemike keskpunktid. Palgaastmikuga struktuurid kasutavad kontrollpunkte harva. Põhipalgaplaani kontrollpunkti saab määrata vormil Põhipalgaplaanid.</td>
</tr>
<tr class="odd">
<td>Tööfunktsioonid</td>
<td>Tööfunktsioonide abil klassifitseeritakse ja filtreeritakse konkreetsete tööde tasuplaane.</td>
</tr>
<tr class="even">
<td>Töötüübid</td>
<td>Töötüüpide abil klassifitseeritakse ja filtreeritakse konkreetsete tööde tasuplaane.</td>
</tr>
<tr class="odd">
<td>Tulemustasu tüübid</td>
<td>Tulemustasu tüüpe (nt aktsiapreemia või sularahapreemia) seadistatakse mitmesuguste tasuplaanide korral.</td>
</tr>
<tr class="even">
<td>Tasuruudustikud</td>
<td>Tasuruudustikud sisaldavad tasustruktuuri.  Tasuruudustikke saab kasutada ühes või mitmes tasuplaanis.</td>
</tr>
<tr class="odd">
<td>Jõudlusplaanid</td>
<td>Tulemusplaane kasutatakse tulemuse seostamiseks eraldamismaatriksiga, et saaksite kasutada plaani tulemustasu strateegia korral.</td>
</tr>
<tr class="even">
<td>Jõudluse hinnangud</td>
<td>Tulemuste hinnanguid kasutatakse tulemusplaanides lisatasu või tulemustasu summa määramiseks.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Protsessi sündmused
Protsessisündmus arvutab tasuteabe kindlal perioodi jaoks kõigi ühte või mitmesse fikseeritud või muutuvasse tasuplaani registreerunud töötajate puhul. Saate protsessisündmust käivitada korduvalt kalkuleeritud tasutulemuste testimiseks või uuendamiseks.

<a name="compensation-events"></a>Kompensatsiooni sündmused
-------------------

Iga kord, kui protsessisündmus käivitatakse, luuakse tasusündmus.  Tasusündmused sisaldavad tasuprotsessi tulemusi iga protsessisündmusesse kaasatud töötaja kohta  Kui arvutused on õiged, saate laadida tasusündmuse, et uuendada protsessisündmusest mõjutatud töötajate tasukirjeid.

## <a name="recommendations"></a> Soovitused
Pärast protsessisündmuse käitamist võite soovitada korrigeerimisi töötaja lisatasu või preemiasumma suurendamiseks, tuginedes protsessisündmuse arvutatud juhistele. Töötajate kohta soovituste edastamiseks tuleb tasuplaanide või protsessisündmuse seadistamisel soovitused lubada.



