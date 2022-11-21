---
title: Inventory Visibility varude eraldamine
description: See artikkel selgitab, kuidas seadistada ja kasutada varude eraldamise funktsiooni, mis võimaldab teil kõrvale panna sihtotstarbeline inventuur, et tagada teie kõige tulusam kanalite või klientide täitmine.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762668"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility varude eraldamine

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Äritegevuse taust ja eesmärk

Organisatsioonid peavad sageli eelnevalt jaotama oma vaba laovaru oma kõige olulisematesse müügikanalitesse, kliendigruppidesse, regioonidesse ja kampaaniasündmustesse, et tagada eelnevalt eraldatud laovaru kaitse mis tahes muu kasutamise eest ja neid saab tarbida ainult eraldamist asjakohaste müügikannete kaudu. Varude eraldamine varude nähtavuses on müügitegevuse plaanimise protsessi osa ja seda tehakse enne mis tahes tegelike müügitegevuste toimumist või müügitellimuse loomist.

Näiteks firma, mille nimi on Contoso, toodab populaarset ettevõtet. Kahjuks on hiljutine tarneahela katkestus mõjutanud kõiki selle contoso transiitvarusid, Contoso on piiranud ainult vaba laovaru ja peab seda kõige paremini kasutama. Contoso tegutseb nii võrgus kui ka kaupluses. Ettevõttel on igas müügikanalis mõned olulised ettevõttepartnerid (turuplatsid ja suured jaemüüjad), kes nõuavad, et nende jaoks salvestatakse teatud osa laovarudest. Seetõttu peab jalgratasettevõte saama tasakaalustada lao jaotust kanalites ja ka hallata oma VIP-partnerite ootusi. Parim viis mõlema eesmärgi saavutamiseks on kasutada varude eraldamist, nii et iga kanal ja jaemüüja saavad kindlad eraldatud kogused, mida saab hiljem müüa tarbijale.

Laovarude eraldamisel on kaks põhilist äritegevuse eesmärki:

- **Varude kaitse (ring on kohustuslik)** – organisatsioonid soovivad eelernieerida piiratud või piiratud laovarud prioriteetsetele kanalitele, piirkondadele, VIP-klientidele ja allettevõtetele. Varude nähtavuse eraldamise funktsiooni sisu, millega kaitsta eraldatud varusid, nii et muud eraldamised, reserveeringud või muud müüginõudlused ei mõjuta eelnevalt eraldatud laovarusid.
- **Alistage** juhtelement – varude nähtavuse eraldamise funktsioon pakub välja eelnevalt eraldatud kogustele piirangu tegemiseks, et vastuvõttev osapool (nt kanal või kliendigrupp) ei tarbiks neid üle, kui jõustub kergel reserveerimisel põhinev tegelik müügikanne.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Eraldamise definitsioon varude nähtavuse teenuses

### <a name="allocation-virtual-pool"></a>Eraldamise virtuaalne kogum

Kuigi varude nähtavuse eraldamisfunktsioon ei pane kõrvale füüsilisi laokoguseid, ei viita see vabale füüsilise lao kogusele, *et* määrata selle virtuaalkausta koguse eraldamiseks saadav esialgne. Lao eraldamine varude nähtavuses on kerge eraldamine. Seda tehakse enne tegelike müügikannete ilmnemist ja see ei sõltu müügitellimustest. Näiteks saate eraldada lao oma kõige olulisematele müügikanalitele või suurtele ettevõtte jaemüüjatele enne, kui mis tahes lõppkliente külastavad müügikanalit või kaupluset selle ostmiseks.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Erinevus varude eraldamise ja kerge reserveerimise vahel

[Pehmed](inventory-visibility-reservations.md) reserveeringud on tavaliselt seotud tegelike müügikannetega (müügitellimuse read). Nii eraldamist kui ka softreserveeringut saab kasutada iseseisvalt, kuid kui soovite neid koos kasutada, tuleb pärast eraldamist teha ka soovitud reserveerimine. Soovitatav on esmalt teha lao eraldamine ja seejärel teha eraldatud koguste suhtes kerge reserveerimine, et saavutada reaalajale lähedalasuv tarbimine eraldamise suhtes. Lisateavet vt jaotisest Tarbi [kerge reserveerimisena](#consume-to-soft-reserved).

Lao eraldusfunktsioon võimaldab müügiplaanijatel või võtmekontohalduritel haldab ja eelallonida olulist laovaru eraldusgruppide lõikes (nt kanalid, regioonid ja kliendigrupid). Samuti toetab see reaalaja jälgimist, korrigeerimist ja tarbimisanalüüsi eraldatud koguste suhtes, et tagada varude jaotamine või ümberasumine õigeaegselt. See võime omada reaalaja nähtavust eraldamise, tarbimise ja eraldamise saldole on eriti oluline kiirmüügi või kampaania sündmuste puhul.

## <a name="terminology"></a>Terminoloogia

Järgmised terminid ja mõisted on kasulikud varude eraldamise aruteludel:

- **Eraldusgrupp** – grupp, mis omab eraldamist, nt müügikanal, kliendigrupp või tellimuse tüüp.
- **Eraldusgrupi** väärtus – iga eraldusgrupi väärtus. Näiteks võib veeb *või* *kauplus* olla müügikanali eraldusgrupi väärtus, *samal ajal kui VIP* *või* tavaline võib olla kliendi eraldamisgrupi väärtus.
- **Eraldamishierarhia** – A tähendab eraldamisgruppide kombineerimist hierarhilisel viisil. Näiteks saate määratleda kanali *hierarhiatasemena* 1, *2*. tasemena regioonina ja *kliendigrupi* tasemena 3. Varude eraldamise ajal peate järgima eraldamishierarhia seeriat, kui määrate eraldamisgrupi väärtuse. Näiteks võite eraldada 200 punane tolm veebikanalile, London’i *piirkonnale* ja VIP-kliendigrupile *·*.*·*
- **Eraldamiseks saadaval** – virtuaalne *ühisost*, mis näitab kogust, mis on edasiseks eraldamiseks saadaval. See on arvutatud mõõt, mille saate oma valemi abil vabalt määratleda. Kui kasutate ka soft reservation funktsiooni, soovitame kasutada sama valemit, et arvutada saadaolevad eraldamiseks ja reserveerimiseks saadaval.
- **Eraldatud** – füüsiline mõõt, mis näitab eraldatud tariife, mida eraldamisgrupid tarbida saavad. See arvatakse maha samal ajal, kui lisatakse tarbitud kogus.
- **Tarbitud** – füüsiline mõõt, mis näitab, et algse eraldatud koguse suhtes tarbitud kogused. Kui sellele füüsilisele mõõtu on lisatud numbreid, vähendatakse automaatselt eraldatud füüsilist mõõtu.

Järgmine näide näitab äritöövoogu laovarude eraldamiseks.

![Varude nähtavuse eraldamise äritöövoog](media/inventory-visibility-allocation-flow.png "Varude nähtavuse eraldamise äritöövoog")

Järgmine näide näitab eraldamishierarhiat ja eraldusgruppe. Siin *kuvatav* virtuaalne ühiskausta kasutatakse koguse eraldamiseks.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title=" Varude nähtavuse eraldamishierarhia" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

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

Eraldusfunktsiooni konfigureerimisel on kolm sammu:

- Lubage funktsioon varude nähtavuse rakenduses, kuite konfiguratsiooni funktsioonihaldus **\> > Sätete eraldamine \>**.
- Seadistage andmeallikas [ja](inventory-visibility-configuration.md#data-source-configuration) selle [määrad](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Seadistage eraldamisgrupi nimi ja hierarhia.

### <a name="predefined-data-source"></a>Eelmääratletud andmeallikas

Kui lubate eraldamisfunktsiooni ja kutsute konfiguratsiooni uuendamise API, loob varude nähtavus ühe eelmääratletud andmeallika ja mitu algset dimensioone.

Andmeallika nimi on `@iv`. See sisaldab füüsiliste vaikeväärtuste kogumeid. Neid saate vaadata varude nähtavuse rakendusest konfiguratsiooni **andmeallikasse \>.** Peaksite nägema andmeallikat **– @IV**. Algsete `@iv` füüsiliste rõhkde loendi vaatamiseks laiendage andmeallikat:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Algse arvutatud **mõõtu**, mille nimi on, vaatamiseks valige vahekaart Arvutatud mõõtmised `@iv.@available_to_allocate`.

- `@iv`

    - `@iv.@available_to_allocate` = `??`– –<a1/&a `??``@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Lisa muud füüsilised mõõtmised arvutatud mõõtu eraldamiseks saadaolevale

Eraldamise kasutamiseks peate arvutatud mõõtu () saadaolevale eraldamisele valemi õigesti seadistama `@iv.@available_to_allocate`. Näiteks on `fno` teil `onordered``pos` andmeallikas ja mõõt ning `inbound``fno.onordered` andmeallikas ja mõõt ning te soovite teha eraldamist vabale laovarule summa ja summa alusel `pos.inbound`. Sellisel juhul peaks see `@iv.@available_to_allocate` sisaldama `pos.inbound` valemit `fno.onordered` või seda valemis. Näide:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

> [!NOTE]
> Andmeallikas on `@iv` eelmääratletud andmeallikas ja eesliitega määratletud füüsilised `@iv``@` koormused on eelmääratletud andmed. Need arvud on eraldamisfunktsiooni jaoks eelmääratletud konfiguratsioon, nii et ärge muutke ega kustutage neid või ilmneb eraldamisfunktsiooni kasutades ootamatuid tõrkeid.
>
> Saate lisada eelmääratletud arvutatud mõõtu uusi `@iv.@available_to_allocate` füüsilisi mõõte, kuid te ei tohi selle nime muuta.

### <a name="manage-allocation-groups"></a>Eraldamisgruppide haldamine

Seadistada saab kuni kaheksa eraldusgrupi nime. Gruppidel on hierarhia. Eraldusgruppide vaatamiseks ja uuendamiseks järgige neid samme.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage leht **Konfiguratsioon** ja seejärel valige vahekaardil **Eraldamine** suvand Redigeeri **konfiguratsiooni**. Vaikimisi on olemas eraldamishierarhia, kus on neli kihti: `Channel` (ülemine kiht), `customerGroup` (teine kiht),`Region` (kolmas kiht) ja `OrderType` (neljas kiht).
1. Saate eemaldada olemasoleva eraldamisgrupi, valides **selle kõrval** x. Hierarhiasse saate lisada ka uusi eraldamisgruppe, sisestades igale uuele grupile nime otse väljale.

    > [!IMPORTANT]
    > Olge ettevaatlik, kui kustutate või muudate eraldamishierarhia vastendamist. Juhiseid vt eralduse [kasutamise näpunäidetest](#allocation-tips).

1. Kui olete eraldamisgrupi ja hierarhia sätete konfigureerimise lõpetanud, salvestage muudatused ja valige **seejärel ülemisel** paremal suvand Värskenda konfiguratsiooni. Konfigureeritud eraldamisgruppide väärtusi uuendatakse eraldamise loomisel kas kasutajaliidese või API POST-i (/api<wbr>/environmentId<wbr>/\{\}<wbr>/eraldamine<wbr>/eraldamine/eraldamine) abil. Üksikasjad mõlema lähenemise kohta leiate selles artiklis hiljem.

Kui kasutate nelja grupinime ja \[`channel``customerGroup` seadistate need väärtusele, `region``orderType`\] siis kehtivad need nimed konfiguratsiooni värskenduse API kutsumisel eraldamisega seotud taotlustele.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a> Eralduse kasutamise näpunäited

- Iga toote puhul peaks eraldamisfunktsioon kasutama sama *dimensiooni* tasemel vastavalt tooteindeksi hierarhiale, mille seate tooteindeksi [hierarhia konfiguratsioonis](inventory-visibility-configuration.md#index-configuration). Oletagem näiteks, et teie indekshierarhia on \[`Site`, `Location`, `Color`. `Size`\] Kui eraldate \[`Site``Location` teatud koguse ühele tootele dimensiooni tasemel, `Color`\] ja järgmisel korral, kui soovite seda toodet eraldada, peate eraldama ka samal \[`Site` tasemel,`Location``Color`\]. Kui kasutate taset\[`Site`, `Location` või `Color``Size`\]\[`Site`, on `Location`\] andmed vastuolus.
- **Eraldusgruppide ja hierarhia muutmine:** kui eraldamisandmed on süsteemis juba olemas, siis olemasolevate eraldamisgruppide kustutamine või eraldusgrupi hierarhia vahetus rikub olemasolevat eraldusgruppide omavahelist vastendust. Seega puhastage kõik vanad andmed enne uue konfiguratsiooni uuendamist käsitsi. Kuna aga uute eraldamisgruppide lisamine madalaimasse hierarhiasse ei mõjuta olemasolevaid vastendusi, ei pea te andmeid puhastama.
- Eraldamine õnnestus ainult juhul, kui tootel on positiivne `available_to_allocate` kogus.
- Toodete eraldamiseks kõrge eraldamise taseme *grupist* alamgruppi kasutage API-d`Reallocate`. Näiteks on teil eraldamisgrupi \[`channel` hierarhia, `customerGroup`, `region``orderType`\]\[ja soovite eraldada mõned tooted eraldusgrupist Online, VIP\] alameraldusgruppi \[Võrgus, VIP, EU\], `Reallocate` kasutage koguse teisaldamiseks API-d. API kasutamisel eraldab `Allocate` see koguse virtuaal ühiskaustast.
- Kogu toote saadavuse (üldkausta) vaatamiseks kasutage [päringu vaba laoseisu API-d](inventory-visibility-api.md#query-on-hand)*, et taotleda eraldamiseks saadaolevat laosummat*. Seejärel saate teha sellel teabel põhinevaid eraldamisotsuseid.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a> Kasuta eraldamise API-d

Praegu avatakse viis eraldamise API-d:

- **POST /API<wbr>/environment<wbr>/\{EnvironmentId\}<wbr>/eraldamine<wbr>/eraldamine** – seda API-d kasutatakse algse eraldamise loomiseks.
- **POST/API<wbr>/keskkonna<wbr>/\{environmentId\}<wbr>/eraldamine<wbr>/unallocate** – seda API-d kasutatakse eraldatud koguste tagasipööramiseks või eemaldamiseks.
- **POST /API<wbr>/environment<wbr>/\{EnvironmentId\}<wbr>/allocation<wbr>/reallocate** – Seda API-d kasutatakse eraldatud koguse teisaldamiseks olemasolevast eraldamisest muudesse eraldusgruppidesse.
- **POST/API<wbr>/keskkonna<wbr>/\{environmentId\}<wbr>/eraldamine<wbr>/tarbimine** – seda API-d kasutatakse eraldatud koguse mahaarvamiseks (kasutamiseks).
- **POST/API<wbr>/environment<wbr>/\{environmentId\}<wbr>/eraldamine<wbr>/päring** – seda API-d kasutatakse olemasolevate eraldamiskirjete otsimine eraldusgruppide ja hierarhia suhtes.

### <a name="allocate"></a>Eralda

Helistage `Allocate` API-le, et eraldada toode, mis sisaldab kindlaid dimensioone. Siin on nõude keha skeem.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
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

### <a name="unallocate"></a>Määra <a0/&/

Kasutage toimingu `Unallocate` tühistamiseks API-d`Allocate`. Negatiivne kogus pole toimingus `Allocate` lubatud. Keha on `Unallocate` identne kehaga `Allocate`.

### <a name="reallocate"></a>Jaota ümber

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
    "groups": {
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
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume"></a>Kasutamine

`Consume` Kasutage API-d tarbimiskoguse sisestamiseks eraldamise suhtes. Näiteks võite seda API-d kasutada eraldatud koguse teisaldamiseks mõneks reaalkoguseks. Siin on nõude keha skeem.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Tarbi kerge reserveerimisena

API `Consume` võib eraldatud koguse kasutada ka kerge reserveerimisena. Sel juhul vähendab `Consume` toiming eraldatud kogust ja teeb seejärel selle koguse jaoks softreserveeringu. Selle lähenemise kasutamiseks peate kasutama ka varude nähtavuse [kerge](inventory-visibility-reservations.md) reserveerimise funktsiooni.

Näiteks olete seadistanud pehme reserveerimise füüsiliseks mõõtu.`iv.softreserved` Arvutatud mõõtu reserveerimiseks saadaoleva valemina kasutatakse järgmist valemit:

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
    "groups": {
        "channel": "Web",
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

### <a name="query"></a>Päring

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
        "channel": "Web",
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
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Eraldamise kasutajaliidese kasutamine

Saate eraldamist käsitsi hallata kasutajaliidese kaudu, avades rakenduse Varude nähtavus ja avades töö nähtavuse **eraldamise \>**. Seejärel saate teha mis tahes toimingud, mida kirjeldatakse järgmistes alamjaotistes.

### <a name="create-an-allocation"></a>Eraldamise loomine

Järgige neid samme eraldamise loomiseks varude **nähtavuse** rakenduse leheküljelt.

1. Valige **eraldamiseks**.
1. Määrake baasväljade, dimensioonide ja sihteraldusgruppide väärtused. (Kui valite väljal andmeallika kogumise **,** Dimensioonide jaotis, kasutage esmalt ripploendit dimensioonide määramiseks (nt `siteId`). Seejärel sisestage kuvatavatele väljadele dimensiooniväärtused.)
1. Valige **edastamine**.

### <a name="consume-an-allocation"></a>Eraldamist tarbimine

Valige **eraldamist** tarbiv. Kindlustamaks, et tarbite õiges eraldusgrupis ja hierarhias, sisestage samad organisatsioonikogumid ja dimensiooni üksikasjad, mille sisestasite eraldamise loomisel.

### <a name="reallocate-an-allocation"></a>Eraldamiste ümberjaotamine

Valige **Jaota ümber,** et teisaldada olemasolev eraldatud kogus ühest eraldusgrupi komplektist teise.

### <a name="query-existing-allocations"></a>Olemasolevate eraldamiste päring

Valige **Päring** ning sisestage seejärel toote, organisatsiooni, dimensiooni ja eraldusgrupi väärtused, et saada olemasolevate eraldamiste päringutulemusi.
