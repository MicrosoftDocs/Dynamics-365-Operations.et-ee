---
title: Hajutatud tellimuste haldamise (DOM) kulukonfiguratsioon
description: Selles teemas kirjeldatakse Dynamics 365 Commercei hajutatud tellimuste haldamise (DOM) funktsiooni kulukonfiguratsiooni.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004224"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Hajutatud tellimuste haldamise (DOM) kulukonfiguratsioon

[!include [banner](../includes/banner.md)]

Organisatsioonid kasutavad tellimuse täitmise alusena kasutatava optimaalse asukoha määratlemiseks mitut kulukomponenti. Mõned neist kulukomponentidest on lähetuskulu, käsitluskulu ja pakenduskulu. Täitmisasukoha määratlemiseks arvutatakse nende kulude kombinatsioon.

Kui Dynamics 365 Commercei hajutatud tellimuste haldamise (DOM) esimene iteratsioon optimeeris tellimuste määramist täitmisasukohtadele, võttis see arvesse ainult vahemaad. Kuigi vahemaa saab olla kuluga vastastikuses seoses, pole see siiski sama mis kulu. Näiteks maksab öine saatmisviis rohkem kui sama vahemaaga kolmepäevane või seitsmepäevane tarne.

Kulukonfiguratsiooni funktsioon võimaldab jaemüüjatel määratleda ja konfigureerida täiendavad kulukomponendid, mis arvutatakse ja mida võetakse arvesse selleks, et määratled tellimuseridade täitmiseks alusena kasutatav optimaalne asukoht.

Kui kulukomponendi on konfigureeritud, kasutab DOM-i solver tellimuse täitmise jaoks optimaalse asukoha määratlemiseks ainult neid kulumääratlusi. See ei võta kuluna arvesse vahemaakomponenti. Kui kulukomponente pole aga konfigureeritud, kasutab DOM-i solver tellimuse täitmise jaoks optimaalse asukoha määratlemiseks kuluna vahemaakomponenti.

## <a name="set-up-cost-components"></a>Kulukomponentide seadistamine

Süsteemis saab määratleda kaks olulist kulukomponenti: **Lähetamine** ja **Muud**.

Mõlemad kulukomponenditüübid toetavad mitut arvutusbaasi, nagu on näha järgmises tabelis.

<table>
<thead>
<tr>
<th>Kulukomponendi tüüp</th>
<th>Arvutuse alus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lähetamine</td>
<td>
<ul>
<li>Lihtne</li>
<li>Astmeline</li>
</ul>
</td>
</tr>
<tr>
<td>Muud</td>
<td>
<ul>
<li>Müügitellimus</li>
<li>Müügirida</li>
<li>Koht</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Kulukomponendi tüüp Lähetamine

Selles jaotises selgitatakse, seadistada kulukomponendi tüübi **Lähetamine** ja lähetuskulude arvutuse aluse kombinatsioone. Lisaks selgitatakse, kuidas kasutab DOM-i solver iga kombinatsiooni.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Kulukomponendi tüüp = lähetamine; arvutuse alus = lihtne

Kulukomponendi tüübi **Lähetamine** ja arvutuse aluse **Lihtne** kombinatsiooni kasutades põhineb tarneviisi lähetuskulu kas fikseeritud kulul või vahemaal.

Selle kombinatsiooni jaoks peate seadistama järgmised väljad.

- **Kulutegur** – sisestage kuluteguri kordumatu identifikaator.
- **Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.
- **Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga. Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.
- **Aktiivne** – näidake, kas kulutegur on aktiivne. DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.
- **Ettevõte** – määrake juriidiline isik, mille jaoks kulutegur konfigureeritakse. Kõik arvutuskriteeriumite read peavad olema ette nähtud sama juriidilise isiku jaoks.
- **Tarneviisid** – määrake tarneviisid, mille jaoks kulu konfigureeritakse.
- **Arvutustüüp** – määrake, kuidas tuleb kulu konkreetse tarneviisi jaoks arvutada. Toetatakse kaht arvutustüüpi.

    - **Fikseeritud** – tarneviisi jaoks kasutataks fikseeritud kulu. Kui valite selle arvutustüübi, määratleb väli **Kulu** fikseeritud kulu.
    - **Vahemaaühiku kohta** – tarneviisi kulu arvutamiseks korrutatakse väljal **Kulu** määratud kuluväärtus tarneaadressi ja asukohtade vahelise vahemaaga.

- **Kulu** – määrake kuluväärtus, mida kasutatakse koos väljaga **Arvutuse tüüp** tarneviisi kulu arvutamiseks.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Kulukomponendi tüüp = lähetamine; arvutuse alus = astmeline

Kulukomponendi tüübi **Lähetamine** ja arvutuse aluse **Astmeline** kombinatsiooni kasutades põhineb tarneviisi lähetuskulu kas fikseeritud kulul või vahemaal. Selles kombinatsioonis põhineb vahemaa vahemaade astmelisel vahemikul.

Selle kombinatsiooni jaoks peate seadistama järgmised väljad.

- **Kulutegur** – sisestage kuluteguri kordumatu identifikaator.
- **Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.
- **Vaikekulu** – määrake kulu, mida tuleks kasutada tarneviisi puhul, kui vahemaa tarneaadressi ja asukoha vahel ei lange kokku tarneviisi ühegi astmelise vahemaaga.
- **Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga. Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.
- **Aktiivne** – näidake, kas kulutegur on aktiivne. DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.
- **Ettevõte** – määrake juriidiline isik, mille jaoks kulutegur konfigureeritakse. Kõik arvutuskriteeriumite read peavad olema ette nähtud sama juriidilise isiku jaoks.
- **Tarneviisid** – määrake tarneviisid, mille jaoks kulu konfigureeritakse.
- **Vahemaa tüüp** – määrake, kas astmelise vahemaa määratlus on vahemaa linnulennul või mööda maad mõõdetav vahemaa.
- **Vahemaaühikud** – määrake ühik, milles astmelist vahemaad mõõdetakse.
- **Vahemaa lähtekoht** – määrake astmelise vahemaa algvahemik.
- **Vahemaa sihtkoht** – määrake astmelise vahemaa lõppvahemik.
- **Arvutustüüp** – määrake, kuidas tuleb kulu konkreetse tarneviisi ja astmelise vahemaa jaoks arvutada. Toetatakse kaht arvutustüüpi.

    - **Fikseeritud** – tarneviisi jaoks kasutataks fikseeritud kulu. Kui valite selle arvutustüübi, määratleb väli **Kulu** fikseeritud kulu.
    - **Vahemaaühiku kohta** – tarneviisi ja astmelise vahemaa kulu arvutamiseks korrutatakse väljal **Kulu** määratud kuluväärtus tarneaadressi ja asukohtade vahelise vahemaaga.

- **Kulu** – määrake kuluväärtus, mida kasutatakse koos väljaga **Arvutuse tüüp** tarneviisi kulu arvutamiseks.

> [!NOTE]
> - Astmeliste vahemaade määratlemise korral kontrollib süsteem, ega kuskil pole puuduvaid ega kattuvaid vahemaid.
> - Tarneviisi jaoks kasutatav vahemaatüüp peab olema kõigil astmelistel vahemaadel sama.

### <a name="other-cost-component-type"></a>Muu kulukomponendi tüüp

Selles jaotises selgitatakse, seadistada lähetuskulude jaoks kulukomponendi tüübi **Muud** ja lähetamisega mitteseotud kulude muu kulutüübi kombinatsioone. Lisaks selgitatakse, kuidas kasutab DOM-i solver iga kombinatsiooni.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Kulukomponendi tüüp = muud; muu kulutüüp = müügitellimus

Kulukomponendi tüübi **Muud** ja muu kulutüübi **Müügitellimus** kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks müügitellimuse tasemel.

Selle kombinatsiooni jaoks peate seadistama järgmised väljad.

- **Kulutegur** – sisestage kuluteguri kordumatu identifikaator.
- **Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.
- **Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga. Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.
- **Aktiivne** – näidake, kas kulutegur on aktiivne. DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.
- **Kulu** – määrake lähetamisega mitteseotud kulu kuluväärtus müügitellimuse tasemel.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Kulukomponendi tüüp = muud; muu kulutüüp = müügirida

Kulukomponendi tüübi **Muud** ja muu kulutüübi **Müügirida** kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks müügitellimuse rea tasemel.

Selle kombinatsiooni jaoks peate seadistama järgmised väljad.

- **Kulutegur** – sisestage kuluteguri kordumatu identifikaator.
- **Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.
- **Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga. Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.
- **Aktiivne** – näidake, kas kulutegur on aktiivne. DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.
- **Kulu** – määrake lähetamisega mitteseotud kulu kuluväärtus müügitellimuse rea tasemel.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Kulukomponendi tüüp = muud; muu kulutüüp = asukoht

Kulukomponendi tüübi **Muud** ja muu kulutüübi **Asukoht** kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks asukohtade rühma või üksikasukoha jaoks.

Selle kombinatsiooni jaoks peate seadistama järgmised väljad.

- **Kulutegur** – sisestage kuluteguri kordumatu identifikaator.
- **Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.
- **Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga. Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.
- **Aktiivne** – näidake, kas kulutegur on aktiivne. DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.
- **Täitmisgrupp** – määrake nende asukohtade grupp, mille jaoks lähetamisega mitteseotud kulu määratletakse.
- **Täitmisasukoht** – määrake asukoht, mille jaoks lähetamisega mitteseotud kulu määratletakse.

    > [!NOTE]
    > Asukohapõhiste arvutuskriteeriumite jaoks ei saa ühel ja samal real määrata täitmisgruppi ja täitmisasukohta.

- **Kulu** – määrake lähetamisega mitteseotud kulu kuluväärtus täitmisgrupi tasemel või täitmisasukoha tasemel.

> [!IMPORTANT]
> Et DOM võtaks neid kulusid käitamisel arvesse, peate lisama kuluteguri asjakohasele täitmisprofiilile.
