---
title: Mobiilirakenduse Warehouse Management väljade konfigureerimine
description: See artikkel kirjeldab, kuidas määrata ja konfigureerida laohalduse mobiilirakenduses kuvatavate väljade nimesid ja prioriteete.
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1ce274c997119c7fdba193fa9559832e63febddc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893232"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a>Mobiilirakenduse Warehouse Management väljade konfigureerimine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas määrata ja konfigureerida laohalduse mobiilirakenduses kuvatavate väljade nimesid ja prioriteete.

> [!NOTE]
> See artikkel kehtib laohalduse funktsioonide kohta. See ei kehti funktsioonidele moodulis Varude haldus. Mobiilirakendus Warehouse Management on rakendus, mille abil saate täita laos vajalikke ülesandeid. Saate määratleda ja konfigureerida rakenduses kasutatavaid väljanimetusi, samuti konfigureerida prioriteeti, millele väljanimed tuleb määrata. See artikkel selgitab, kuidas määrata ja konfigureerida neid laohalduse mobiilirakenduse väljanimesid ja -prioriteete ning nende kasutamist.

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
<td>See valik määratleb, kas valitud väljanime puhul kuvatakse skannimisväli või käsitsi sisestamise väli. See aitab välju eristada olenevalt sellest, kas välja puhul kasutatakse vöötkoode. <strong>Märkus:</strong> Väljanimede puhul, mille eelistatud sisestusrežiim on <strong>Skannimine</strong>, saate sisestada teavet käsitsi, kui vöötkood on loetamatu või kahjustunud.</td>
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

Ülejäänud metaandmeid, näiteks asukohta, ülesandelehel ei kuvata, kuid need kuvatakse üksikasjade lehel. Lisateabe saamiseks ja kasutajaliidese näidete vaatamiseks lugege ajaveebipostitust [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

## <a name="additional-resources"></a>Lisaressursid

[Laohalduse mobiilirakenduse installimine ja ühendamine](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]