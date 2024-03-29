---
title: Mallkooslused
description: Mallkoosluses (BOM) on pidevalt kasutatavate teenuseobjekti komponentide standardnimekiri.
author: sorenva
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdda8ffaaf4e5696b286273fd5ad770de5349b48
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678146"
---
# <a name="template-boms"></a>Mallkooslused

[!include [banner](../includes/banner.md)]

Mallkoosluses (BOM) on pidevalt kasutatavate teenuseobjekti komponentide standardnimekiri. Mallkoosluses loetletud komponendid kujutavad endast teenuseobjekti eraldiseisvaid alamkomponente. Kui te rakendate mallkooslust teenuseobjektil, saate säilitada teenuseobjektil vahetatud alamkomponentide kirjet.

Teenuseleppes ja teenusetellimuses mallkoosluse rakendamiseks tuleb teil see lisada teenuseobjekti seosesse.

> [!NOTE]
> Teenuseobjektile saate rakendada ainult ühe mallkoosluse.

## <a name="create-a-template-bom"></a>Käsitsi koostatava mallkoosluse loomine

Järgmises tabelis on toodud teave mitmesuguste meetodite kohta, mida saate kasutada mallkoosluse loomiseks.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Meetod</p></th>
<th><p>Kirjeldus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Tootmine</p></td>
<td><p>Mallkooslus põhineb tootmistellimusel. See valik on rakendatav vaid siis, kui töötate tootmiskeskkonnas. Eeliseks on teil kehtiv, üksikasjalik loetelu komponentidest, millest kaup koosneb.</p></td>
</tr>
<tr class="even">
<td><p>Kaup BOM</p></td>
<td><p>Mallkooslus põhineb kauba kooslusel. Kauba kooslus on erinevalt tootmiskooslusest staatiline nimekiri komponentidest, mis moodustavad kauba.</p></td>
</tr>
<tr class="odd">
<td><p>Olemasolev mall</p></td>
<td><p>Mall põhineb olemasoleval mallkooslusel.</p></td>
</tr>
<tr class="even">
<td><p>Käsitsi</p></td>
<td><p>Kui te teate, milliseid varuosi tavaliselt teenuseobjektil vahetatakse, saate luua oma mallkoosluse käsitsi. See meetod aitab tagada, et mallis sisalduvad komponendid peegeldavad teie töökoha praegusi nõudeid.</p></td>
</tr>
</tbody>
</table>

## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Mallkoosluse rakendamine teenuseleppele või hooldustellimusele

Saate rakendada mallkooslust teenuseleppele, hooldustellimusele või mõlemale. Teenuselepe hõlmab tavaliselt pikaajalist suhet kliendiga. Teenusekoosluses salvestatud asenduste ajalugu on kasulik teave teenuseleppe jaoks.

Saate mallkooslust rakendada ka hooldustellimusele, et salvestada teenuseobjektil tehtud teenuste ajalugu.

## <a name="copy-the-history-of-a-service-bom"></a>Teenusekoosluse ajaloo kopeerimine

Teenusekoosluse rea ajaloo saate kopeerida ühest teenuseleppest teise. Kopeerides teenuse ajalugu ühest teenuseleppest teise, saate säilitada kaubal tehtud asenduste kirje.

### <a name="example"></a>Näide

Olete koostanud 3-aastase teenuseleppe kliendi auto kohta. Selle perioodi jooksul harjub klient ettevõtte pakutava hea teenindusega. Seega soovib klient pärast leppe aegumist sõlmida uue. Nüüd on teil võimalik läbi rääkida ettevõtte jaoks kasulikuma lepingu suhtes. Kuna asendatud komponentide kirje võib tulevikus olla kasulik, võite kopeerida teenusekoosluse ajaloo uude leppesse.

## <a name="modify-the-template-bom"></a>Mallkoosluse muutmine

Kui mallkooslus ei ole teenuseobjektiga seotud, saate selle ridu muuta või kustutada. Pärast mallkoosluse sidumist teenuseobjektiga saate muuta ainult koosluse kohalikku versiooni. Kui te soovite mallkoosluse kohaliku versiooni seadistust duplitseerida, saate luua uue kohalikul versioonil põhineva mallkoosluse. Lisateavet vt teemast [Teenusekoosluse muutmine](modify-service-bom.md).

Kui te asendate koosluses kauba, saate asenduse registreerida koosluse koostaja kooslusereal. Võite asenduskauba jaoks luua ka hooldustellimuse rea. Kui loote hooldustellimuse rea, saate asenduskauba arveldada. Kui te asendusele hooldustellimuse rida ei loo, säilitatakse asenduse registreering teenuseobjekti ajaloo jälgimiseks.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Kooslusereal kuvatava teabe muutmine

Saate muuta viisi, kuidas kuvatakse koosluserida kõigis malli- ja teenusekooslustes. Muudatused rakendatakse kõikidele malli- ja teenusekooslustele. See hõlmab ka teenuseobjektidega seotud kooslusi.

## <a name="set-up-number-sequences-for-template-boms"></a>Mallkoosluste numbriseeriate seadistamine

Mallkoosluste kasutamiseks peate seadistama kaks numbriseeriat. Seadistage üks numbriseeria mallkoosluse ja teine koosluse ajaloo rea numbri jaoks.

> [!NOTE]
> Numbriseeriaid kasutatakse identifikaatorite eraldamiseks kirjetele, mis neid nõuavad. Enne kui saate mallkooslusele või koosluse ajaloo rea numbrile numbriseeria määrata, peate seadistama numbriseeria koodid.

## <a name="set-up-number-sequences"></a>Seadista numbriseeriad

1. Looge loendilehel **Numbriseeriad** numbriseeriad mallkoosluste ja koosluse ajaloo raja numbri jaoks.
1. Valige **Teenuste haldus** \> **Häälestus** \> **Teenuste halduse parameetrid**.
1. Valige **Numbriseeriad** ja seejärel valige numbriseeria kood numbriseeria viidetele, mille lõite vormis **Numbriseeriad**.
1. Muudatuste salvestamiseks sulgege vorm.

> [!NOTE]
> Koosluse ajaloo rea numbrit kasutab süsteem koosluse ajaloo kannete seostamiseks hooldusleppe või -tellimusega. Numbrit ei kuvata kasutajaliideses.

## <a name="see-also"></a>Vt ka

[Käsitsi koostatava mallkoosluse loomine](create-template-bom.md)

[teenuslepingute objektiseoste mallkoosluste haldamine](manage-template-boms-on-object-relations.md)

[Teenusekoosluse muutmine](modify-service-bom.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
