---
title: Rakenduse väljanimede konfigureerimine laorakenduses
description: See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamisrakenduse väljade nimesid ning prioriteete Dynamics 365 Supply Chain Managementis.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ac31b3d2b3b1d9ca51919fe75e06f0de1cda0c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963431"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a>Rakenduse väljanimede konfigureerimine laorakenduses

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamisrakenduse väljade nimesid ning prioriteete Dynamics 365 Supply Chain Managementis. 

> [!NOTE]
> See teema kehtib laohalduse funktsioonidele. See ei kehti funktsioonidele moodulis Varude haldus. Ladustamine on rakendus, mille abil saate täita laos vajalikke ülesandeid. Saate määratleda ja konfigureerida rakenduses kasutatavaid väljanimetusi, samuti konfigureerida prioriteeti, millele väljanimed tuleb määrata. See teema selgitab, kuidas neid ladustamisrakenduse väljade nimesid ja prioriteete määratleda ning konfigureerida ja kuidas neid moodulis Ladustamine kasutada. Üksikasjalikku teavet selle kohta, kuidas konfigureerida lao ühendamist, leiate juhendist [Laorakenduse installimise ja konfigureerimise ülevaade](install-configure-warehousing-app.md).

## <a name="configure-warehouse-app-field-names"></a>Laorakenduse väljade nimede konfigureerimine

Kui kasutate moodulit Ladustamine mobiilses seadmes, saate seadmes metaandmete kuvamise viisi konfigureerida lehel **Laorakenduse väljade nimed**. Valige uues ettevõttes käsk **Loo vaikeseadistus**, et luua kõik väljanimed, mida kasutatakse lao mobiilse seadme töövoogudes, ning seejärel määrake neile eelistatud sisestusrežiim ja sisestustüüp. Kui kõik väljanimed on loodud, saate valida järgmisi sisestusvalikuid.

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
<td>See valik määratleb, kas valitud väljanime puhul kuvatakse skannimisväli või käsitsi sisestamise väli. See aitab välju eristada olenevalt sellest, kas välja puhul kasutatakse vöötkoode. <strong>Märkus.</strong> Väljanimede puhul, mille eelistatud sisestusrežiim on <strong>Skannimine</strong>, saate sisestada teavet käsitsi, kui vöötkood on loetamatu või kahjustunud.</td>
</tr>
<tr class="even">
<td>Sisestuse tüüp</td>
<td>See valik määratleb, millist sisestustüüpi tuleb valitud väljanime puhul kasutada. Saadaval on neli valikut.
<ul>
<li><strong>Valik</strong> - sisaldab valikute loendit. Selle valikuga väljanimesid ei saa redigeerida.</li>
<li><strong>Kuupäev</strong> - kuupäevana määratud väljanimed kuvavad kuupäevavormingut koos sildiga. Tänu sellele näevad laotöötajad, millises vormingus tuleb kuupäev sisestada. Selle valikuga väljanimesid ei saa redigeerida.</li>
<li><strong>Tähed</strong> - selle valiku korral kasutatakse rakenduses teabe käsitsi sisestamisel seadme klaviatuuri. Klaviatuurikasutust saab muuta olenevalt kasutatavast seadmest.</li>
<li><strong>Numbrid</strong> - selle valiku korral saate ainult numbreid kasutavate väljanimede puhul kuvada seadme klaviatuuri kasutamise asemel kohandatud numbriklahvistiku koos sisestusväljaga.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Laorakenduse väljade prioriteedi konfigureerimine

Lehel **Laorakenduse väljade prioriteet** saate panna väljanimed erinevatesse prioriteedigruppidesse. See võimaldab otsustada, milline teave tuleb kuvada ülesande põhilehel, kui laotöötajad täidavad ülesandeid rakendust kasutades. Kui klõpsate valikut **Loo vaikeseadistus**, luuakse prioriteedigruppide vaikekomplekt. Prioriteedigruppe saab luua nii palju kui vaja, kuid ülesandelehel kuvatakse ainult kolm. Kui süsteem saadab metaandmed rakendusse, määrab see igale väljale suhtelise prioriteedi olenevalt selle prioriteedigrupist ja rakendus kuvab ülesandelehel kolm esimest metaandmetes sisalduvat prioriteedigruppi. Ülejäänud metaandmed kuvatakse teisel, üksikasjade lehel. Järgmises tabelis on toodud näide viiest prioriteedigrupist.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioriteedigrupp</th>
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

Näiteks kui laotöötaja täidab ülesannet mobiilses seadmes, sisaldavad rakenduses kuvatavad metaandmed järgmisi välju.

-   Kaup
-   Kogus
-   Mõõtühik
-   Kauba kirjeldus
-   Suurus ja asukoht

Ülaltoodud tabelis seadistatud laorakenduse väljade prioriteedi põhjal kuvatakse ülesandelehel järgmised kolm teaberida.

-   1. rida: kaup, kogus, mõõtühik
-   2. rida: kauba kirjeldus
-   3. rida: suurus

Ülejäänud metaandmeid, näiteks asukohta, ülesandelehel ei kuvata, kuid need kuvatakse üksikasjade lehel. Lisateabe saamiseks ja kasutajaliidese näidete vaatamiseks lugege ajaveebipostitust [Announcing Finance and Operations – Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="additional-resources"></a>Lisaressursid
--------

[Laorakenduse installimise ja konfigureerimise ülevaade](install-configure-warehousing-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]