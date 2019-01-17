---
title: "Komisjonitasude jälgimine kassas müügigruppide abil"
description: "Jaekaubanduses on tavapärane müügi jälgimine kliendiga töötanud müüja järgi, kes osutab abi, teeb lisa- ja ristmüüki ning töötleb kannet."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ed4f9b3055e164600827b62d57b7a5068edb3b1a
ms.contentlocale: et-ee
ms.lasthandoff: 01/04/2019

---

# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>Komisjonitasude jälgimine kassas müügigruppide abil

[!include [banner](includes/banner.md)]

Jaekaubanduses on tavapärane müügi jälgimine kliendiga töötanud müüja järgi, kes osutab abi, teeb lisa- ja ristmüüki ning töötleb kannet.

Müügi jälgimine müügiesindaja järgi mõõdab müüja müügivõimeid, samas kui müügi mõõtmine kassapidaja järgi mõõdab tema kiirust ja tõhusust. Müügiesindaja järgi jälgitavat müüki kasutatakse samuti sageli komisjonitasude või muude lisatasude arvestamiseks.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Töötaja müügiesindajaks konfigureerimine kassas

Kui töötaja lisatakse müügigruppi, tekib tal õigus komisjonitasule ja ta saab süsteemis müügiesindajaks märkida. Töötajal, kes müügigruppi ei kuulu, puudub komisjonitasu saamise õigus ja teda ei registreerita kassarakenduses müügiesindajaks. Kassas tuletatakse müügiesindajate nimekiri kõigist müügigruppidest, mis sisaldavad vähemalt ühte kauplusele määratud töötajat. Loend kuvatakse kassas müügigrupi ID ja nime kombinatsioonina (ID : Nimi). Vaike-müügigrupi saab määrata töötajatele selliste stsenaariumide toetuseks, kus jaemüüja otsustab määrata müügiesindaja kassaridadele automaatselt. Kasutajad saavad valida mis tahes müügigruppidest, mille liige töötaja on.

## <a name="functionality-profile-settings"></a>Funktsiooniprofiilide seaded

Kauplusel on mitmesuguseid funktsiooniprofiili sätteid, mis määravad kassas müügiesindajaid hõlmava voo ja protsessi.

<table>
<thead>
<tr>
<th>Reeglid</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vaikimisi kassapidaja, kui võimalik</td>
<td>Kui see valik on lubatud, täidab kassa automaatselt kande read praeguse kassapidaja vaike-müügigrupiga. Kui kassapidajale pole vaike-müügigruppi määratud, siis väärtust ei määrata. Kasutaja saab müügigrupi siiski käsitsi määrata, kasutades kassa nupupaneeli nuppu.</td>
</tr>
<tr>
<td>Müügiesindaja määramine</td>
<td>Sellel valikul on kolm võimalikku väärtust:
<ul>
<li><strong>Ei</strong> - selle valiku korral ei paluta kasutajal müügigruppi valida. Väärtuse saab siiski määrata, kasutades kassapidaja vaike-müügigruppi, või käsitsi, kasutades kassa nupupaneeli nuppu.</li>
<li><strong>Kande algus</strong> – selle valiku korral, kui valikut <strong>Vaikimisi kassapidaja</strong> pole lubatud või praegusel kassapidajal pole vaike-müügigruppi, palutakse kasutajal valida müügigrupp iga kande alguses. Müügigrupi valimisel sellest viibast lähtestatakse kõik järgnevad read valitud müügigrupiks. Kasutaja saab müügigrupi siiski käsitsi määrata, kasutades kassa nupupaneeli nuppu.</li>
<li><strong>Iga rea puhul</strong> – selle valiku korral, kui valikut <strong>Vaikimisi kassapidaja</strong> pole lubatud või praegusel kassapidajal pole vaike-müügigruppi, palutakse kasutajal valida müügigrupp pärast iga rea lisamist. Kasutaja saab müügigrupi siiski käsitsi määrata, kasutades kassa nupupaneeli nuppu.</li>
</ul>
</td>
</tr>
<tr>
<td>Nõua</td>
<td>See valik kehtib ainult siis, kui kassa on konfigureeritud müügiesindajat küsima. Kui see on lubatud, siis nõutakse, et kasutaja valiks enne jätkamist müügigrupi. Muidu kuvatakse kasutajale viip, kuid ta võib tühistada ja jätkata valikut tegemata. Pärast rea lisamist saab piisavate õigustega kasutaja siiski müügigrupi realt eemaldada. Selles olukorras ei rakendata valikut „Nõua müügiesindajat”.</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Müügiesindaja andmete kuvamine kassa kannete ekraanil

Kassa kannete ekraani paigutust ja sisu saab konfigureerida, kasutades ekraanipaigutuse kujundajat ja kauplustele, registritele või töötajatele määratud ekraanipaigutusi. Välja **Müügiesindaja** saab lisada vahekaardile Read paanil Sissetulek.  Siis kuvatakse iga kande ekraani rea puhul määratud müügigrupi ID.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Müügiesindaja toimingute lisamine kassa nupupaneelidele

Kassa võimaldab kasutajatel konfigureerida ekraanipaigutustes sisalduvaid nupupaneele juurdepääsu andmiseks kassatoimingutele. Nupupaneeli nuppudele saab lisada järgmisi müügiesindajaid puudutavaid kassatoiminguid.

| Toiming                                 | Kirjeldus |
|-------------------------------------------|-------------|
| Määra reale müügiesindaja          | See kassatoiming kuvab loendi vastavatest kaupluse müügigruppidest (ID : Nimi). Müügigrupi valimisel sellest loendist määratakse praegusel kande real väärtus. |
| Tühjenda realt müügiesindaja        | See kassatoiming eemaldab praeguse müügigrupi väärtuse praeguselt kande realt. |
| Kande müügiesindaja määramine   | See kassatoiming kuvab loendi vastavatest kaupluse müügigruppidest (ID : Nimi). Müügigrupi valimisel sellest loendist määratakse praeguse kande vaikeväärtus. Määratakse mis tahes olemasolevad read ilma määratud müügigrupita ning kõik hiljem lisatud read. |
| Kandest müügiesindaja kustutamine | See kassatoiming eemaldab praeguse vaike-müügigrupi väärtuse praeguselt kandelt. See ei mõjuta kandes juba olemasolevaid ridu. |

## <a name="calculating-commissions"></a>Komisjonitasu arvutamine

Komisjonitasu arvutatakse määratud müügigruppide töötajatele väljavõtte või müügitellimuse sisestamise ajal. Komisjonitasu summa määratakse kliendi ja/või kande toodete puhul müügigrupis määratletud töötaja komisjonitasu osakaalu ja seotud komisjonitasu arvutamise sätete alusel.

