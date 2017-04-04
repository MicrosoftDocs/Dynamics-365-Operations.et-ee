---
title: "Hüvitusplaanid"
description: "Hüvitise ja eeliste haldurid saavad kasutada hüvituste haldust, et hallata ning töödelda organisatsiooni töötajate fikseeritud ja ergutussüsteemi plaane."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 1809a6679685e483694a53b7742d80f02ade2cd5
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-plans"></a>Hüvitusplaanid

Hüvitise ja eeliste haldurid saavad kasutada hüvituste haldust, et hallata ning töödelda organisatsiooni töötajate fikseeritud ja ergutussüsteemi plaane.

### <a name="introduction"></a>Sissejuhatus

Hüvitise juhtimise kasutatakse kontrolli alus maksma ja auhinnad. Kui töövõtja fikseeritud alus maksma ja merit suureneb juhitakse läbi kindlaksmääratud hüvitiste plaanid. Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu. 

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
<li>Tegevusi saate tagada, et arvutuse kindlaksmääratud hüvitiste plaanide töötlemisel.  Näiteks meetmete tüüpi omakapitali võrrelda töötajate töötasu vähemalt viide punkti taseme kohta töötaja ja töötaja saada tasumine vähemalt minimaalne.</li>
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
<td>Tasu sagedustel kasutatakse mille hüvitis on määratud perioodi.  Näiteks saate aru, kui hüvitise summa on määratud aastapalk versus tunni tasu sagedus aitab maksma määr. Tunnitasu maksta sageduste palk Sagedus aastas maksma sagedused on ka kasutatud kehtestada ümberarvestuskoefitsiendid teisendada kompensatsiooni iga kuu, nädal, kaks korda nädalas.</td>
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
<td>Hüvitise võrkude sisaldada kompensatsiooni struktuuri.  Hüvitise võrkude kasutamist mõni hüvitiste plaanid.</td>
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

Hüvitist juhul luuakse iga kord protsessi sündmus käivitatakse.  Hüvitise sündmused sisaldavad hüvitise protseduuri tulemused iga töötaja sündmusega protsessi kaasatud.  Kui arvutused on õiged, saab laadida hüvitist sündmuse protsessi sündmuse mõjutatud töötajatele hüvitist kirjete värskendamiseks.

## <a name="recommendations"></a> Soovitused
Pärast protsessisündmuse käitamist võite soovitada korrigeerimisi töötaja lisatasu või preemiasumma suurendamiseks, tuginedes protsessisündmuse arvutatud juhistele. Töötajate kohta soovituste edastamiseks tuleb tasuplaanide või protsessisündmuse seadistamisel soovitused lubada.


