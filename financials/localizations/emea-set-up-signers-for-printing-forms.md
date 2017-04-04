---
title: Prindi vormid allkirjastajad seadistamine
description: "Juriidiliste isikutele, Tšehhi Vabariik, Eesti, Ungari, Leedu, Läti, Poola ja Venemaa, seadistage allkirjastajad ja ka hotelli ja müüjad, kes Prindi dokumendid nagu arved ja sularaha."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 263464
ms.assetid: 7213914a-ecb6-4711-99fe-4e11867aaf4d
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 45d2facde1e5502f4a5863863554a486916c26cd
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-signers-for-print-forms"></a>Prindi vormid allkirjastajad seadistamine

Juriidiliste isikutele, Tšehhi Vabariik, Eesti, Ungari, Leedu, Läti, Poola ja Venemaa, seadistage allkirjastajad ja ka hotelli ja müüjad, kes Prindi dokumendid nagu arved ja sularaha.

<a name="set-up-default-values"></a>Vaikeväärtuste seadistamine
---------------------

Allkirjastajad dokumentidele, mis firma prindib, kasutage selle **ametnike** lehel. Seadistage allkirjastajad ja pealkirjade nii ettevõtte kui ka klientide või hankijate, sõltuvalt dokumendi tüübist. Järgmises tabelis kirjeldatakse vahekaardid on **ametnike** lehel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vahekaart</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Üldine</td>
<td>Seisukohti ja seotud teavet allkirjastajad (direktor ja juhtiv audiitor) kes saab allkirjastada kõiki dokumente printida.</td>
</tr>
<tr class="even">
<td>Pearaamat</td>
<td>Lisada allkirjastaja, kellel on järgmised sisemine finantsdokumendid, mis on seotud rahavoogude asukoha ja seotud teave:
<ul>
<li>Kassaorderid</li>
<li>Ettemaksuaruanne</li>
<li>Kassaraamatu leht</li>
<li>Loendusväljavõte</li>
<li>Edasilükkamiste *</li>
</ul></td>
</tr>
<tr class="odd">
<td>Müügitellimused</td>
<td>Lisage positsioone ja seotud teave allkirjastajad, kellel on järgmised väljamineva algdokumente, mis on seotud hotelli:
<ul>
<li>Arve tasumine *</li>
<li>Arve</li>
<li>Faktuurarve *</li>
<li>Arve – kreeditarve</li>
<li>Faktuurarve - krediidi-Märkus *</li>
<li>Maksukande faktuurarve (kliendi) *</li>
</ul></td>
</tr>
<tr class="even">
<td>Ostutellimused</td>
<td>Lisage positsioone ja seotud teave allkirjastajad, kellel on järgmised sissetulevad algdokumente, hankijatega seotud:
<ul>
<li>Arve</li>
<li>Faktuurarve *</li>
<li>Arve – kreeditarve</li>
<li>Faktuurarve - krediidi-Märkus *</li>
<li>Arve tasumine *</li>
<li>Maksukande faktuurarve (hankija) *</li>
</ul></td>
</tr>
<tr class="odd">
<td>Laokaupade haldus</td>
<td>Lisage positsioone ja seotud teave allkirjastajad, kellel on järgmised laodokumentide kui materiaalne põhivara kliendile väljastatud või saadud hankija:
<ul>
<li>Väljastab saatelehe müügitellimuse (m-15) *</li>
<li>RMB. saatelehe/saamise järjekorras</li>
<li>Väljastab saatelehe üleviimistellimuse (m-15) *</li>
</ul></td>
</tr>
</tbody>
</table>

\*Selline dokument on saadaval ainult juriidiliste isikute, nende peamine aadress Venemaal. Järgmises tabelis kirjeldatakse väljad on **ametnike** lehel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ametikoht</td>
<td>Valige allkirjastaja postituse pealkiri.</td>
</tr>
<tr class="even">
<td>Nimi</td>
<td>Valige allkirjastaja nimi. Loendis nimed tulevad tabel või töötajate tabelist, sõltuvalt allkirjastaja (st sõltuvalt sellest, kas on <strong>meie</strong> ruut). Kui loendis puudub allkirjastaja nimi, sisestage käsitsi Allkirjastaja täielik nimi.</td>
</tr>
<tr class="odd">
<td>Ametinimetus</td>
<td>Valige allkirjastaja ametinimetus. Kui loendis puudub allkirjastaja nimi, sisestage käsitsi allkirjastaja nimi.</td>
</tr>
<tr class="even">
<td>Konto kood</td>
<td>Saate valida, kas allkirjastaja saate allkirjastada kõik dokumentidest valitud dokumendi tüübi või ainult mõne kindla kliendi või hankija.</td>
</tr>
<tr class="odd">
<td>Konto seos</td>
<td>Valige valitud konto kood seotud kliendi või hankija konto. See väli on saadaval ainult siis, kui valite <strong>kirje</strong> ja selle <strong>konto kood</strong> välja.</td>
</tr>
<tr class="even">
<td>Meie</td>
<td>Valitud ruudu märkimine näitab, et positsiooni on sisemine.</td>
</tr>
<tr class="odd">
<td>Seos laohoonega</td>
<td>Saate valida, kas allkirjastaja määratakse kõigi ladude või ainult kindla lao. Valikud on järgmised:
<ul>
<li><strong>Kõik</strong> – allkirjastaja on määratud kõik laod.</li>
<li><strong>Rekord</strong> – allkirjastaja on määratud kindla lao.</li>
</ul></td>
</tr>
<tr class="even">
<td>Ladu</td>
<td>Saate valida lao tähis, mis vastab allkirjastaja määratud lattu. See väli on saadaval ainult siis, kui valite <strong>kirje</strong> ja selle <strong>ladu koos</strong> välja.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Ametnike jaoks määratud numbriseeria kood
Saate määrata numbriseeria kood ametniku puhul on **Number sequences** osa ning **juriidiliste isikute** lehel. Valige numbriseeria kood jaoks ning **ametnike seansi ID** viide.

## <a name="modify-signers-in-primary-documents"></a>Muuta algdokumente allkirjastajad
Ametnike funktsioonid kuvatakse vaikimisi eelmääratletud allkirjastajad ametnike tabelist. Kohta ning **arve sisestamist** lehekülg, edasi on **ametnike** jaotises allkirjastaja nimi ja pealkiri dokumendi järgmisi põhidokumendi muutmiseks:

-   Kliendiarve
-   Hankija arve
-   Lähetuse üleviimistellimus
-   Kassaorder

**Märkus:** pärast seda, kui dokument konteeritakse, ametnikud ei saa redigeerida.


