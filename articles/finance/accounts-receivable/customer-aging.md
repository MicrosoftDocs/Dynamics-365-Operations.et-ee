---
title: Kliendi ajalise jaotuse aruanne
description: Kliendi ajalise jaotuse aruandes kuvatakse deebetsaldod, mis on sorditud kuupäevavahemiku või aegumisperioodi alusel.
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33bee60a3807c92cc97f0f5e6d660a67cdd7f297
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595085"
---
# <a name="customer-aging-report"></a>Kliendi ajalise jaotuse aruanne 

**Kliendi ajalise jaotuse** aruandes kuvatakse deebetsaldod, mis on sorditud kuupäevavahemiku või aegumisperioodi alusel.

Selle aruande loomisel kuvatakse järgmised vaikeparameetrid. Neid parameetreid saate kasutada aruandes kuvatud andmete filtreerimiseks. Lisateavet leiate teemast [Sissenõuete seadistamine](set-up-collections.md).

<table>
<colgroup>
<col>
<col>
</colgroup>
<thead>
<tr class="header">
<th><p>Väli</p></th>
<th><p>Kirjeldus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Arveldusklassifikatsioon</strong></p></td>
<td><p>Valige aruandesse lisamiseks vähemalt üks arveldusklassifikatsioon.</p>
<div class="alert">

**Märkus.** See juhtelement on saadaval ainult juhul, kui on valitud konfiguratsioonivõti <STRONG>Avalik sektor</STRONG>.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Ilma arveldusklassifikatsioonita kannete kaasamine</strong></p></td>
<td><p>Kui see märkeruut on märgitud, siis kuvatakse aruandes kõik kanded, millele pole määratud arveldusklassifikatsiooni.</p>
<div class="alert">

**Märkus.** See juhtelement on saadaval ainult juhul, kui on valitud konfiguratsioonivõti <STRONG>Avalik sektor</STRONG>.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Ajaline jaotus seisuga</strong></p></td>
<td><p>Sisestage praeguses ajalise jaotuse vahemikus kasutatud kuupäev.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Saldo seisuga</strong></p></td>
<td><p>Sisestage kuupäev, et vaadata kliendi saldosid. Seda nimetatakse ka kannete piirkuupäevaks.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alguskuupäev</strong></p></td>
<td><p>Sisestage kuupäev, mis jääb esimese perioodiintervalli või aegumisperioodi piiridesse, et see aruandesse kaasata.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Kriteerium</strong></p></td>
<td><p>Valige kuupäeva tüüp, millel aruanne põhineb.</p>
<ul>
<li><p><strong>Kande kuupäev</strong> – kannete sisestuskuupäev. Näiteks võib see olla arve kuupäev, mis on tähtaja arvutamise aluseks.</p></li>
<li><p><strong>Tähtaeg</strong> – kannete tähtaeg maksetingimuste järgi.</p></li>
<li><p><strong>Dokumendi kuupäev</strong> – kasutaja määratud dokumendikuupäev, mille alusel arvutatakse tähtaeg.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Aegumisperioodi definitsioon</strong></p></td>
<td><p>Valige aegumisperioodi definitsioon. Välja <strong>Intervall</strong> ei kasutata, kui valite aegumisperioodi definitsiooni.</p>
<p>Prinditaval aruandel ei saa kasutada aegumisperioodi definitsioone, millel on rohkem kui kuus aegumisperioodi.</p>
<div class="alert">

**Märkus.** Aegumisperioode saate seadistada lehel <STRONG>Aegumisperioodi definitsioonid</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Aegumisperioodi kirjelduse printimine</strong></p></td>
<td><p>Valige <strong>Jah</strong> aegumisperioodide kirjelduste kaasamiseks aruandes iga aegumisperioodi veeru ülaosas. Valige <strong>Ei</strong>, et printida aruanne ilma veerupäisteta.</p></td>
</tr>
<tr class="even">
<td><p><strong>Intervall</strong></p></td>
<td><p>Määrake kasutatav periood, sisestades igas perioodis päeva- või kuuühikute arvu. Näiteks nädalapõhise aegumisteabe vaatamiseks sisestage sellele väljale 7 ja valige väljal <strong>Päev/kuu</strong> suvand <strong>Päev</strong>.</p>
<div class="alert">

**Märkus.** Sellele väljale sisestatavat teavet kasutatakse üksnes juhul, kui te pole aegumisperioodi definitsiooni valinud. Vastasel juhul määratletakse printimissuund aegumisperioodi definitsioonis.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Päev/kuu</strong></p></td>
<td><p>Valige ühik, kas <strong>Päev</strong> või <strong>Kuu</strong>, mida kasutatakse perioodi määratlemiseks väljal <strong>Intervall</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Printimissuund</strong></p></td>
<td><p>Valige, kas arvutada saldosid ja printida möödunud või tulevaste perioodide ajalise jaotuse aruanne. Kuupäevi hinnatakse väljal <strong>Saldo seisuga</strong> valitud kuupäeva arvestades. Valige <strong>Tagasiulatuv</strong>, et näidata eelmiste perioodide teavet. Valige <strong>Edasiulatuv</strong>, et näidata tulevaste perioodide teavet.</p>
<div class="alert">
  
<STRONG>Märkus.</STRONG> Sellele väljale sisestatavat teavet kasutatakse üksnes juhul, kui te pole aegumisperioodi definitsiooni valinud.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Üksikasjad</strong></p></td>
<td><p>Valige, et loetleda kanded, mis on aruandel näidatud saldodesse kaasatud.</p></td>
</tr>
<tr class="even">
<td><p><strong>Kandevaluutas summade kaasamine</strong></p></td>
<td><p>Valige, et kaasata summad nii kandevaluutas kui ka arvestusvaluutas. Kui see märkeruut ei ole märgitud, kuvatakse aruandes olevad summad ainult arvestusvaluutas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Negatiivne saldo</strong></p></td>
<td><p>Valige, et kaasata kliendikontod, millel on negatiivne saldo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nullsaldo kontode välistamine</strong></p></td>
<td><p>Valige, et välistada kliendikontod, mille saldo on null.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Maksete paigutamine</strong></p></td>
<td><p>Valige, et kuvada maksed, mida pole arveldatud. Need kuvatakse aruande esimeses veerus.</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]