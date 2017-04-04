---
title: "Konfigureerida rakendus väljanimed Warehousing appi"
description: "Selles teemas kirjeldatakse, kuidas määratleda ja seadistada lao app välja- ja prioriteetide Dynamics 365 toiminguteks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigureerida rakendus väljanimed Warehousing appi

Selles teemas kirjeldatakse, kuidas määratleda ja seadistada lao app välja- ja prioriteetide Dynamics 365 toiminguteks. 

**Märkus:** see teema kehtib Laohaldus funktsioonid. See ei kehti varude juhtimise funktsioonid. Dynamics 365 toiminguteks - ladustamine on rakendus, mis kasutage lao toimingute sooritamiseks. Te saate määratleda ja konfigureerida väljade nimed, mida kasutatakse rakenduse ning konfigureerida kuhu väljanimed määratakse prioriteet. Selles teemas selgitatakse, kuidas määratleda ja seadistada need laost app välja- ja prioriteedid ja kuidas neid kasutatakse Dynamics 365 - ladustamine. Vaadake üksikasjalikku teavet kuidas seadistada ühendust Dynamics 365 toiminguteks - ladustamis-, juhendaja [installida ja konfigureerida Dynamics 365 toiminguteks - lao](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Seadistada lao app väljanimed
===================================

Dynamics 365 kasutamisel toiminguteks - lao mobiilsideseadmes, saate konfigureerida kuidas metaandmed kuvatakse seadme kohta on **ladu app väljanimed** lehel. Uue ettevõtte Dynamics 365 toiminguteks, valige **Loo vaikimisi seadistus** luua kõigi väljade nimesid, mida kasutatakse lao mobiilseadme töövood, ja seejärel määrake eelistatud sisestusrežiim ja sisendi tüüp neile. Pärast kõikide väljade nimed on loodud, saate valida järgmisi andmeid võimalusi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Suvand</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Eelistatud sisestusrežiim</td>
<td>See valik määrab, kas skaneerimise välja või käsitsi kande sisestamise väljale näidatakse valitud välja nimi. See on kasulik eristada väljad sõltuvalt vöötkoode kasutamisel välja. <strong>Märkus:</strong> puhul välja nimed koos eelistatud sisendrežiimi määratud <strong>skannimise</strong>, saate sisestada teabe käsitsi kui vöötkoodi on loetamatu või rikutud.</td>
</tr>
<tr class="even">
<td>Sisestuse tüüp</td>
<td>See valik määrab, milline sisendi tüüp võib kasutada valitud välja nimi. On saadaval nelja suvandid.
<ul>
<li><strong>Valiku</strong> - sisaldab loetelu võimalusi valida. Välja nimi see suvand ei saa redigeerida.</li>
<li><strong>Kuupäev</strong> - välja nimed nagu kuupäev kuupäevavormingu sildiga. See aitab näha sisestada kuupäeva vormingu laotöölistele. Välja nimi see suvand ei saa redigeerida.</li>
<li><strong>Alpha</strong> - märkimisel seadme klaviatuuri kasutatakse teabe sisestamine käsitsi rakendus. Klaviatuuri kogemusi saab muuta sõltuvalt sellest, millist seadet kasutatakse.</li>
<li><strong>Numbrilise</strong> - puhul välja nimed selle kasutamise numbriline ainult sisend, valige see suvand, et kuvada ka kohandatud numbriklahvistiku välja seadme klaviatuuri asemel.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Seadistada lao app välja prioriteet
======================================

Kohta ning **ladu app välja prioriteet** leht, paned väljanimed erinevad prioriteedi gruppidesse. Seetõttu on võimalik otsustada, millist teavet tuleks kuvada lehel põhiülesanne laotöötajad ülesannete rakenduse abil. Kui klõpsate **Loo vaikimisi seadistus**, luuakse vaikimisi määratud prioriteetsed rühmad. On võimalik luua nii palju prioriteetsed rühmad vastavalt vajadusele, kuid ainult kolm prioriteetsed rühmad kuvatakse lehel ülesanne. Kui Dynamics 365 operatsioonide saadab rakenduse metaandmed, see määrata igale väljale sõltuvalt oma prioriteetne rühm suhteline prioriteet ja rakenduses kuvatakse esimese kolme Eelisrühmad sisalduvate metaandmete ülesanne lehel. Ülejäänud täis metaandmed kuvatakse teisese üksikasjade lehel. Järgmises tabelis on näiteks viis prioriteetsed rühmad.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioriteetne rühm</th>
<th>Määratud väljad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Prioriteet 10</td>
<td><ul>
<li>Kaup</li>
<li>Kogus</li>
<li>Mõõtühik</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioriteet 20</td>
<td><ul>
<li>Kogumi positsioon</li>
<li>Kogum</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioriteet 30</td>
<td><ul>
<li>Kauba kirjeldus</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioriteet 40</td>
<td><ul>
<li>Konfiguratsioon</li>
<li>Värv</li>
<li>Suurus</li>
<li>Laad</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioriteet 50</td>
<td><ul>
<li>Koht</li>
<li>Litsentsiplaat</li>
</ul></td>
</tr>
</tbody>
</table>

Näiteks kui töötaja lao ülesannet, mobiilsideseadmesse, kui metaandmeid, mis kuvatakse rakenduse koosneb järgmistest väljadest:

-   Kaup
-   Kogus
-   Mõõtühik
-   Kauba kirjeldus
-   Suurus ja asukoht

Vastavalt eespool esitatud tabelis seadistada lao app välja prioriteet, järgmised 3 rida teavet kuvatakse lehe ülesanne:

-   1. rida: Kauba, koguse, toodanguühiku
-   2. rida: Kauba kirjeldus
-   Rida 3: suurus

Ülejäänud metaandmed, näiteks asukoht, ei kuvata lehel ülesanne, kuid kuvatakse üksikasjade lehel. Rohkem ja Vaata näiteid kasutajaliidese, vt ajaveeb postitage [teada Dynamics 365 toiminguteks - lao](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Vt ka
--------

[Installida ja konfigureerida Microsoft Dynamics 365 operatsioonideks – ladustamine](install-configure-warehousing-app.md)


