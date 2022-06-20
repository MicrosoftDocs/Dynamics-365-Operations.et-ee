---
title: Inventory Visibility varude eraldamine
description: See artikkel selgitab, kuidas seadistada ja kasutada varude eraldamise funktsiooni, mis võimaldab teil kõrvale panna sihtotstarbeline inventuur, et tagada teie kõige tulusam kanalite või klientide täitmine.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: ccc3a8c4b3d0649397b1d1f9139f7feebf39b02f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852501"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility varude eraldamine

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Äritegevuse taust ja eesmärk

Paljudel juhtudel peavad tootjad, jaemüüjad ja teised tarneahela äriisikud eraldama kaubavarusid olulistele müügikanalitele, asukohtadele või klientidele või konkreetsetele müügisündmustele. Lao eraldamine on tavaline tava müügitegevuse plaanimise protsessis ja seda tehakse enne tegelike müügitegevuste toimumist ja müügitellimuse loomist.

Näiteks on rattaettevõttel piiratud vaba kaubavaru väga populaarse jaoks. See ettevõte teeb nii võrgu- kui ka kaupluses müüki. Ettevõttel on igas müügikanalis mõned olulised ettevõttepartnerid (turuplatsid ja suured jaemüüjad), kes nõuavad, et nende jaoks salvestatakse teatud osa laovarudest. Seetõttu peab jalgratasettevõte saama tasakaalustada lao jaotust kanalites ja ka hallata oma VIP-partnerite ootusi. Parim viis mõlema eesmärgi saavutamiseks on kasutada varude eraldamist, nii et iga kanal ja jaemüüja saavad kindlad eraldatud kogused, mida saab hiljem müüa tarbijale.

Laovarude eraldamisel on kaks põhilist äritegevuse eesmärki:

- **Varude kaitse (ringpiirangud)** – organisatsioonid soovivad eelernitud või piiratud laovaru eraldada prioriteetsetesse kanalitesse, regioonidesse, VIP-klientidesse ja allettevõtetesse. Varude nähtavuse eraldamise funktsiooni sisu, millega kaitsta eraldatud varusid, nii et muud eraldamised, reserveeringud või muud müüginõudlused ei mõjuta eelnevalt eraldatud laovarusid.
- **Alistage** juhtelement – varude nähtavuse eraldamise funktsioon pakub välja eelnevalt eraldatud kogustele piirangu tegemiseks, et vastuvõttev osapool (nt kanal või kliendigrupp) ei tarbiks neid üle, kui jõustub kergel reserveerimisel põhinev tegelik müügikanne.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Eraldamise definitsioon varude nähtavuse teenuses

Kuigi varude nähtavuse teenuse eraldamisfunktsioon ei pane kõrvale füüsilisi laokoguseid, ei viita see vabale füüsilise lao kogusele, *et* määratleda selle algne saadav, et eraldada virtuaalkausta kogus. Lao eraldamine varude nähtavuses on kerge eraldamine. Seda tehakse enne tegelike müügikannete ilmnemist ja see ei sõltu müügitellimustest. Näiteks saate eraldada lao oma kõige olulisematele müügikanalitele või suurtele ettevõtte jaemüüjatele enne, kui mis tahes lõppkliente külastavad müügikanalit või kaupluset selle ostmiseks.

Erinevus varude eraldamise ja varude kerge reserveerimise [vahel on see](inventory-visibility-reservations.md), et soft reservation on tavaliselt lingitud tegelike müügikannetega (müügitellimuse read). Seega, kui soovite koos kasutada eralduse ja soft reservation funktsioone, soovitame esmalt teha varude eraldamine ja seejärel teha eraldatud koguste suhtes soovitud reserveerimise. Lisateavet vt jaotisest Tarbi [kerge reserveerimisena](#consume-to-soft-reserved).

Lao eraldusfunktsioon võimaldab müügiplaanijatel või võtmekontohalduritel olulist laovaru eraldisgruppides (nt kanalid, regioonid ja kliendigrupid) hallata ja eeljaotust eraldada. Samuti toetab see eraldatud koguste reaalaja jälgimist, korrigeerimist ja tarbimisanalüüsi, nii et täiendamist või ümberasutamist saab teha õigeaegselt. See võime omada reaalaja nähtavust eraldamise, tarbimise ja eraldamise saldole on eriti oluline kiirmüügi või kampaania sündmuste puhul.

## <a name="terminology"></a>Terminoloogia

Järgmised terminid ja mõisted on kasulikud varude eraldamise aruteludel:

- **Eraldusgrupp** – grupp, mis omab eraldamist, nt müügikanal, kliendigrupp või tellimuse tüüp.
- **Eraldusgrupi** väärtus – iga eraldusgrupi väärtus. Näiteks võib veeb *või* *kauplus* olla müügikanali eraldusgrupi väärtus, *samal ajal kui VIP* *või* tavaline võib olla kliendi eraldamisgrupi väärtus.
- **Eraldamishierarhia** – A tähendab eraldamisgruppide kombineerimist hierarhilisel viisil. Näiteks saate määratleda kanali *hierarhiatasemena* 1, *2*. tasemena regioonina ja *kliendigrupi* tasemena 3. Varude eraldamise ajal peate järgima eraldamishierarhia seeriat, kui määrate eraldamisgrupi väärtuse. Näiteks võite eraldada 200 punane tolm veebikanalile, London'i *piirkonnale* ja VIP-kliendigrupile *·*.*·*
- **Eraldamiseks saadaval** – virtuaalne *ühisost*, mis näitab kogust, mis on edasiseks eraldamiseks saadaval. See on arvutatud mõõt, mille saate oma valemi abil vabalt määratleda. Kui kasutate ka soft reservation funktsiooni, soovitame kasutada sama valemit, et arvutada saadaolevad eraldamiseks ja reserveerimiseks saadaval.
- **Eraldatud** – füüsiline mõõt, mis näitab eraldatud tariife, mida eraldamisgrupid tarbida saavad.
- **Tarbitud** – füüsiline mõõt, mis näitab, et algse eraldatud koguse suhtes tarbitud kogused. Kui sellele füüsilisele mõõtu on lisatud numbreid, vähendatakse automaatselt eraldatud füüsilist mõõtu.

Järgmine näide näitab äritöövoogu laovarude eraldamiseks.

![Varude nähtavuse eraldamise äritöövoog](media/inventory-visibility-allocation-flow.png "Varude nähtavuse eraldamise äritöövoog")

## <a name="set-up-inventory-allocation"></a>Saate häälestada varude eraldamist.

Varude eraldamisfunktsioon koosneb järgmistest komponentidest:

- Eelmääratletud, eraldamisega seotud andmeallikas, füüsilised meetmed ja arvutatud andmed.
- Kohandatavad eraldamisgrupid, mille maksimum on kaheksa taset.
- Eraldamise rakenduse programmeerimisliideste (API-de) kogum:

    - eraldama
    - Jaota ümber
    - Ei saa jaotada
    - Tarbida
    - Päringu

Eraldusfunktsiooni konfigureerimisel on kaks sammu:

- Seadistage andmeallikas [ja](inventory-visibility-configuration.md#data-source-configuration) selle [määrad](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Seadistage eraldamisgrupi nimi ja hierarhia.

### <a name="predefined-data-source"></a>Eelmääratletud andmeallikas

Kui lubate eraldamisfunktsiooni ja kutsute konfiguratsiooni uuendamise API, loob varude nähtavus ühe eelmääratletud andmeallika ja mitu algset dimensioone.

Andmeallika nimi on `@iv`.

Siin on esialgsed füüsilised meetmed:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Siin on esialgsed arvutatud meetmed:

- `@iv`

    - `@iv.@available_to_allocate` = `??`– –<a1/&a `??``@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Lisa muud füüsilised mõõtmised arvutatud mõõtu eraldamiseks saadaolevale

Eraldamise kasutamiseks peate seadistama arvutatud mõõtu (eraldamiseks saadaoleva).`@iv.@available_to_allocate` Näiteks on teil andmeallikas `fno` ja mõõt, `onordered``pos` andmeallikas ja mõõt ning te soovite teha vabale kaubavarule eraldamise summa ja `inbound` summa alusel`fno.onordered`.`pos.inbound` Sellisel juhul peaks see `@iv.@available_to_allocate` sisaldama `pos.inbound` valemit `fno.onordered` või seda valemis. Näide:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

### <a name="change-the-allocation-group-name"></a>Eraldamisgrupi nime muutmine

Seadistada saab kuni kaheksa eraldusgrupi nime. Gruppidel on hierarhia.

Seadistage grupinimed varude nähtavuse **Power App konfiguratsioonilehel**. Selle lehe avamiseks avage oma keskkonnas Microsoft Dataverse rakenduse Varude nähtavus ja valige konfiguratsiooni **eraldamine \>**.

Näiteks kui kasutate \[`channel``customerGroup` nelja grupinime ja seadistate need väärtusele,, `region``orderType`\] kehtivad need nimed konfiguratsiooni värskenduse API kutsumisel eraldamisega seotud taotlustele.

### <a name="allocation-using-tips"></a>Eraldus näpunäidete abil

- Iga toote puhul peaks eraldamisfunktsioon kasutama sama *dimensiooni* tasemel vastavalt tooteindeksi hierarhiale, mille seate tooteindeksi [hierarhia konfiguratsioonis](inventory-visibility-configuration.md#index-configuration). Oletagem näiteks, et teie indekshierarhia on \[`Site`, `Location`, `Color`. `Size`\] Kui eraldate \[`Site``Location` teatud koguse ühele tootele dimensiooni tasemel, `Color`\] ja järgmisel korral, kui soovite seda toodet eraldada, peate eraldama ka samal \[`Site` tasemel, `Location`. `Color`\] Kui kasutate taset\[`Site`, `Location` või `Color``Size`\]\[`Site`, on `Location`\] andmed vastuolus.
- Eraldusgrupi nime muutmine ei mõjuta teenuses salvestatud andmeid.
- Eraldamine peaks toimuma pärast seda, kui tootel on positiivne laokogus.
- Toodete eraldamiseks kõrge eraldamise taseme *grupist* alamgruppi kasutage API-d `Reallocate`. Näiteks on teil eraldamisgrupi \[`channel` hierarhia, `customerGroup`, `region``orderType`\]\[ja soovite eraldada mõned tooted eraldusgrupist Online, VIP\] alameraldusgruppi \[Võrgus, VIP, EU\], `Reallocate` kasutage koguse teisaldamiseks API-d. API kasutamisel eraldab `Allocate` see koguse virtuaal ühiskaustast.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a> Eralduse API kasutamine

Praegu avatakse viis eraldamise API-d:

- POST /API/keskkond/eraldamine{environmentId}/eraldamine
- POST/API/keskkond/{environmentId} eraldamine/unallocate
- POST/API/keskkond/{environmentId} eraldamine/ümberjaotamine
- POST/API/keskkond/eraldamine{environmentId}/tarbimine
- POST /API/keskkond/eraldamine{environmentId}/päring

#### <a name="allocate"></a>Eralda

Helistage `Allocate` API-le, et eraldada toode, mis sisaldab kindlaid dimensioone. Siin on nõude keha skeem.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Näiteks soovite koguseks eraldada 10 *kogust tooteleKogus*, *saidi 1*, asukohale 11 *,* *punasele* värvile, kanalile *Online*, kliendigrupi *VIP-le* ja *PIIRKONNAle USA-s*. Selleks eraldamiseks võite teha kõne, mis sisaldab järgmist kehasisu.

```json
{
    "id": "???",
    "productId": "Bike",
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Kogus peab alati olema suurem kui 0 (null).

#### <a name="unallocate"></a>Määra <a0/&/

Kasutage toimingu `Unallocate` tühistamiseks API-d `Allocate`. Negatiivne kogus pole toimingus `Allocate` lubatud. Keha on `Unallocate` identne kehaga `Allocate`.

#### <a name="reallocate"></a>Jaota ümber

`Reallocate` Kasutage API-d mõne eraldatud koguse teisaldamiseks teisele grupikombinatsioonile. Siin on nõude keha skeem.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "targetGroups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Näiteks saate teisaldada kaks kogust, mille dimensioonide sait = 1, asukoht = 11, värv = \[\] punane eraldusgrupist Online, VIP, \[\] USA eraldusgruppi \[Online, VIP, EU,\]`Reallocate` kutsudes API ja pakkudes järgmise kehateksti.

```json
{
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

#### <a name="consume"></a>Kasutamine

`Consume` Kasutage API-d tarbimiskoguse sisestamiseks eraldamise suhtes. Näiteks võite seda API-d kasutada eraldatud koguse teisaldamiseks mõneks reaalkoguseks. Siin on nõude keha skeem.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Näiteks on kaheksa eraldatud kogumit, mille dimensioonide sait = 1, asukoht = 11, värv =\[\] punane eraldusgrupile \[Online, VIP, US \]. Kasutatakse järgmist saadaolevat valemit eraldamiseks:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

Kaheksa kogust eraldatakse mõõtu `pos.inbound`.

Nüüd müüakse kolm päeva ja need võetakse eraldamiskaustast. Selle teisaldamise registreerimiseks võite teha kõne, mis omab järgmist taotluse keha.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Pärast seda kõnet vähendatakse tootele eraldatud kogust 3 võrra. Lisaks loob varude nähtavus vaba kaubavaru muudatuse sündmuse, kus `pos.inbound` = *-3*. Võite väärtuse säilitada ka nii `pos.inbound`, nagu see on, ja lihtsalt kasutada eraldatud kogust. Sel juhul peate siiski looma kas teise füüsilise mõõtu tarbitud koguste alles hoida või kasutama eelmääratletud mõõtu `@iv.@consumed`.

Pange sellele taotlusele tähele, et füüsiline mõõt, mida tarbitavas nõude kehas kasutate, peaks kasutama vastupidist muutujatüüpi (Liitmine või Lahutamine), võrreldes arvutatud mõõtus kasutatava muutja tüübiga. Seega on selles tarbitud kehas `iv.inbound` väärtus`Subtraction`, mitte `Addition`

Andmeallikat `fno` ei saa tarbitavas kehas kasutada, nagu me alati nõudsime, et varude nähtavus ei saa muuta andmeallika `fno` andmeid. Andmevoog on ühene viis, mis tähendab `fno`, et kõik andmeallika koguse muudatused peavad tulema teie tarneahela halduse keskkonnast.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Tarbi kerge reserveerimisena

API `Consume` võib eraldatud koguse kasutada ka kerge reserveerimisena. Sel juhul vähendab `Consume` toiming eraldatud kogust ja teeb seejärel selle koguse jaoks softreserveeringu. Selle lähenemise kasutamiseks peate kasutama ka varude nähtavuse [kerge](inventory-visibility-reservations.md) reserveerimise funktsiooni.

Näiteks olete seadistanud soft reservation muutja (mõõt) kui `iv.softreserved`. Arvutatud mõõtu reserveerimiseks saadaoleva valemina kasutatakse järgmist valemit:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– `iv.softreserved`

Selle seadistuse kasutamiseks eraldusfunktsiooniga lisage see `@iv.@allocated``iv.available_to_reserve`, et luua järgmine valem:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– –<a1/&a `iv.softreserved``@iv.@allocated`

Seejärel uuenda `@iv.@available_to_allocate` samale väärtusele.

Kui soovite tarbida koguseks 3 ja selle koguse otse reserveerida, saate teha kõne, millele on järgmine taotluse keha.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

Selles taotluses pange tähele`iv.softreserved`, et väärtus on`Addition`, mitte `Subtraction`

#### <a name="query"></a>Päring

`Query` Kasutage API-d, et tuua mõnede toodete jaoks eraldamisega seotud teavet. Tulemuste kitsendamiseks saate kasutada dimensioonifiltreid ja eraldusgrupi filtreid. Dimensioonid peavad vastama täpselt samale, mida soovite tuua, \[näiteks saidil =1, asukohal =11\]\[on mitteseotud tulemusi võrreldes saidiga =1, asukohaga=11, värv=punane \].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Näiteks kõigi eralduskirjete \[toomiseks kasutage välja sait=1, asukoht=11, värv=\] punane ja tühi grupid.

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Kasutage \[site=1, asukoht =11, värv = punane\] ja \[gruppide kanal =Online, customerGroup=VIP, region=US\], et saada sellele grupile eralduskirjeid:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
