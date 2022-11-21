---
title: Inventory Visibility konfigureerimine
description: See artikkel kirjeldab varude nähtavuse konfigureerimist.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 915382c14cc9ba89b9d543cfd668a94cecbc0a55
ms.sourcegitcommit: 4f987aad3ff65fe021057ac9d7d6922fb74f980e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9764865"
---
# <a name="configure-inventory-visibility"></a>Inventory Visibility konfigureerimine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida varude nähtavust varude nähtavuse rakenduse abil moodulis Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Sissejuhatus

Enne kui alustate tööd varude nähtavusega, peate lõpule täitma järgmise konfiguratsiooni, nagu kirjeldatud selles artiklis:

- [Andmeallika konfiguratsioon](#data-source-configuration)
- [Sektsiooni konfiguratsioon](#partition-configuration)
- [Tooteindeksi hierarhia konfiguratsioon](#index-configuration)
- [Reserveeringu konfiguratsioon (valikuline)](#reservation-configuration)
- [Vaikekonfiguratsiooni näidis](#default-configuration-sample)

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist installige ja seadistage Inventory Visibility lisandmoodul, nagu on kirjeldatud jaotises [Inventory Visibility installimine ja seadistamine](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Inventory Visibility rakenduse konfiguratsioonileht

Power Apps rakenduses **Konfiguratsioon** lehel [Inventory Visibility rakendus](inventory-visibility-power-platform.md) aitab teil seadistada konfiguratsiooni ja tarkvara reserveerimise konfiguratsiooni. Pärast lisandmooduli installimist sisaldab vaikekonfiguratsioon Microsoft Dynamics 365 Supply Chain Management-i väärtust (`fno` andmeallikas). Vaikesätted on võimalik üle vaadata. Lisaks sellele saate vastavalt teie äritegevuse nõuetele ja välise süsteemi lao sisestusnõuetele muuta konfiguratsiooni lahenduses , et ühtlustada viisi, kuidas saab erinevates süsteemides varude muudatusi sisestada, korraldada ja nende kohta päringuid esitada. Selle artikli ülejäänud jaotised selgitavad, kuidas kasutada konfiguratsioonilehe **iga osa**.

Kui konfiguratsioon on lõpule viidud, valige kindlasti rakenduses **Konfiguratsiooni värskendamine**.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Inventory Visibility funktsioonide lubamine Power Apps funktsioonihalduses

Inventory Visibility lisandmoodul lisab teie installile mitu uut Power Apps funktsiooni. Vaikimisi on need funktsioonid välja lülitatud. Nende kasutamiseks avage **konfiguratsioonileht** ja lülitage **seejärel vahekaardil Funktsioonihaldus** sisse järgmised funktsioonid vastavalt vajadusele.

| Funktsioonihalduse nimi | Kirjeldus |
|---|---|
| *OnHandReservation* | See funktsioon võimaldab varude nähtavust kasutades luua reserveeringuid, tarbida reserveeringuid ja/või reserveerimata laokoguseid. Lisateavet vt teemast [Varude nähtavuse reserveeringud](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | See funktsioon annab tootevarude kokkuvõtte koos kõigi dimensioonidega. Lao koondandmed sünkroonitakse perioodiliselt laovarude nähtavuse väljalt. Sünkroonimise vaikesagedus on kord iga 15 minuti järel ja seda saab seadistada nii kõrgeks kui üks kord iga 5 minuti järel. Lisateavet vt laovarude [kokkuvõttest](inventory-visibility-power-platform.md#inventory-summary). |
| *onHandIndexQueryPreloadBackgroundService* | Selle funktsiooniga saab eellaadida varude nähtavuse vaba kaubavaru päringuid eelnevalt valitud dimensioonidega vaba kaubavaru loendite kogumi jaoks. Sünkroonimise vaikesagedus on kord iga 15 minuti järel. Lisateavet vt teemast Sujuva [kaubavaru päringu eellaadimine](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *Sõlm OnhandChangeSchedule* | See valikuline funktsioon võimaldab vaba kaubavaru muutmise graafikut ja on saadaval lubamiseks (ATP) funktsioone. Lisateavet vt varude nähtavuse vaba [kaubavaru muutmise graafikust ja lubaduse andmiseks saadaval](inventory-visibility-available-to-promise.md). |
| *Eraldamine* | See valikuline funktsioon võimaldab varude nähtavust, omab võimalust laovarude kaitsmiseks (ringlimise kasutamine) ja alistab kontrolli. Lisateavet vt varude nähtavuse [varude eraldamisest](inventory-visibility-allocation.md). |
| *Laokauba lubamine varude nähtavuses* | See valikuline funktsioon võimaldab varude nähtavust, et toetada kaupu, mis on lubatud laohaldusprotsessidele (WMS). Lisateavet vt WMS-kaupade [varude nähtavuse tugi](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Teenuse lõpp-punkti leidmine

Kui te ei tea õiget varude nähtavuse teenuse lõpp-punkti, **·** Power Apps **avage konfiguratsiooni lehekülg ja valige siis ülemises parempoolses nurgas suvand Näita** teenuse üksikasju. Lehel kuvatakse õige teenuse lõpp-punkt. Lõpp-punkti võite leida ka elutsükli Microsoft Dynamics teenustes, nagu on kirjeldatud lõpp-punkti [otsimisel vastavalt elutsükli teenuste keskkonnale](inventory-visibility-api.md#endpoint-lcs).

> [!NOTE]
> Vale lõpp-punkti kasutamine võib põhjustada nurjunud varude nähtavuse installimise ja tõrked, kui tarneahela haldus on sünkroonitud varude nähtavusega. Kui te ei ole kindel, mis on teie lõpp-punkt, võtke ühendust oma süsteemiadministraatoriga. Lõpp-punkti URL-id kasutavad järgmist vormingut:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Andmeallika konfiguratsioon

Iga andmeallikas tähistab süsteemi, millest teie andmed tulevad. Andmeallikate nimede näited `fno` on (mis vastavad tarneahela haldamisele) `pos` ja (st. müügikohad). Vaikimisi on rakenduse Varude nähtavus andmeallikaks (`fno`) seadistatud Supply Chain Management.

> [!NOTE]
> Andmeallikas `fno` on reserveeritud tarneahela haldamiseks. Kui varude nähtavuse lisandmoodul on integreeritud tarneahela halduskeskkonnaga, on soovitatav mitte kustutada andmeallikaga `fno` seotud konfiguratsioone.

Andmeallika lisamiseks toimige järgmiselt.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Valige andmeallika **lisamiseks andmeallikas** **vahekaardil Andmeallikas** (nt mõni muu otstarbekas `ecommerce` andmeallika ID).

> [!NOTE]
> Andmeallika lisamisel kontrollige kindlasti enne varude nähtavuse teenuse konfiguratsiooni värskendamist oma andmeallika nime, füüsilisi mõõtmeid ja dimensioonivastendusi. Pärast suvandi **Konfiguratsiooni värskendamine** valimist ei saa te neid sätteid muuta.

Andmeallika konfiguratsioon hõlmab järgmisi osi.

- Dimensioon (dimensiooni vastendamine)
- Füüsilised mõõtmed
- Arvutatud mõõtmed

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensioon (dimensiooni vastendamine)

Dimensioonide konfigureerimise eesmärk on ühtlustada mitme süsteemi integreerimist sündmuste ja päringute sisestamise jaoks vastavalt dimensioonide kombinatsioonidele. Varude nähtavus annab põhidimensioonide loendi, mida saab vastendada teie andmeallika dimensioonidest. Vastendamiseks on saadaval kolmkümmend kolm dimensiooni.

- Kui kasutate tarneahela haldust ühe andmeallikana, on 13 dimensiooni juba tarneahela halduse standarddimensioonidega vastendatud. Muud 12 dimensiooni (`inventDimension1` kuni `inventDimension12`) on vastendatud ka tarneahela halduses kohandatud dimensioonidega. Ülejäänud kaheksa dimensiooni (`ExtendedDimension1` kuni `ExtendedDimension8`) on laiendatud dimensioonid, mida saate vastendada välistele andmeallikatele.
- Kui te ei kasuta ühe andmeallikana Supply Chain Managementi, võite dimensioonid vabalt vastendada. Järgmine tabel näitab saadaolevate dimensioonide täielikku loendit.

> [!NOTE]
> Kui kasutate tarneahela haldust ja muudate vaikedimensioonide vastendamist hankeahela halduse ja varude nähtavuse vahel, ei sünkrooni muudetud dimensioon andmeid. Seega, kui teie dimensioon ei ole dimensiooni vaikeloendis ja te kasutate välist andmeallikat, `ExtendedDimension1``ExtendedDimension8` on soovitatav kasutada seda vastendamiseks.

| Dimensiooni tüüp | Põhidimensioon |
|---|---|
| Toode | `ColorId` |
| Toode | `SizeId` |
| Toode | `StyleId` |
| Toode | `ConfigId` |
| Jälitamine | `BatchId` |
| Jälitamine | `SerialId` |
| Koht | `LocationId` |
| Koht | `SiteId` |
| Lao olek | `StatusId` |
| Laopõhine | `WMSLocationId` |
| Laopõhine | `WMSPalletId` |
| Laopõhine | `LicensePlateId` |
| Muud | `VersionId` |
| Varud (kohandatud) | `InventDimension1` kuni `InventDimension12` |
| Laiendus | `ExtendedDimension1` kuni `ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> Eelmises tabelis loetletud dimensioonitüübid on ainult teie viiteks. Te ei pea neid Varude nähtavuses määratlema.
>
> Varude (kohandatud) dimensioone saab reserveerida tarneahela halduse jaoks. Sel juhul kasutage laiendatud dimensioone.

Välistel süsteemidel on juurdepääs Varude nähtavusele läbi selle RESTful API-de. Integreerimiseks võimaldab Varude nähtavus konfigureerida *välise andmeallika* ja vastenduse *väliselt dimensioonilt* *põhidimensioonile*. Siin on näide dimensioonide vastendamise tabelist.

| Väline dimensioon | Põhidimensioon |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Dimensioonide vastendamise konfigureerimisel saate saata välised dimensioonid otse Varude nähtavusse. Varude nähtavus teisendab seejärel välised dimensioonid automaatselt põhidimensioonideks.

Dimensioonide vastenduste lisamiseks järgige neid juhiseid.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. **Valige vahekaardil Andmeallikas** andmeallikas, kus soovite dimensioonide vastendamist teha. Seejärel valige jaotises Dimensiooni **vastendamised** suvand **Lisa**, et lisada dimensioonivastendusi.

    ![Dimensioonivastenduste lisamine](media/inventory-visibility-dimension-mapping.png "Dimensioonivastenduste lisamine")

1. Määrake väljal **Dimensiooni nimi** lähtedimensioon.
1. Valige väljal **Põhidimensioonile** see rakenduse Varude nähtavus dimensioon, mida soovite vastendada.
1. Valige käsk **Salvesta**.

Näiteks olete juba loonud andmeallika nimega ja see `ecommerce` sisaldab toote värvi dimensiooni. Sel juhul saate vastendamise jaoks kõigepealt `ProductColor`**·**`ecommerce` lisada andmeallika väljale Dimensiooni nimi ja `ColorId`**seejärel valida väljal Baasdimensiooni.**

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Füüsilised mõõtmed

Kui andmeallikas sisestab rakendusse Varude nähtavus varude muudatuse, sisestab see muudatuse, kasutades *füüsilisi mõõtmeid*. Füüsilised mõõtmed muudavad kogust ja kajastavad varude olekut. Vastavalt vajadustele saate määratleda enda füüsilisi nõudeid. Päringud võivad põhineda füüsilistel mõõtudel.

Varude nähtavus annab vaikimisi füüsiliste ühikute loendi, mis on vastendatud tarneahela haldusega (`fno` andmeallikas). Need füüsilised mõõtmed võetakse laokannete olekutest rakenduse Supply Chain Management lehelt **Vaba kaubavaru loend** (**Varude haldus \> Päringud ja aruanded \> Vaba kaubavaru loend**). Järgmine tabel esitab füüsiliste mõõtmete näite.

| Füüsilise mõõtme nimi | Kirjeldus |
|---|---|
| `NotSpecified` | Pole määratud |
| `Arrived` | Saabunud |
| `AvailOrdered` | Saadaval tellitud |
| `AvailPhysical` | Füüsiliselt vaba |
| `Deducted` | Maha arvatud |
| `OnOrder` | OnOrder |
| `Ordered` | Tellitud |
| `PhysicalInvent` | Füüsiline ladu |
| `Picked` | Valitud |
| `PostedQty` | Sisestatud kogus |
| `QuotationIssue` | Pakkumiste väljaminek |
| `QuotationReceipt` | Saadud pakkumine |
| `Received` | Vastuvõetud |
| `Registered` | Registreeritud |
| `ReservOrdered` | Tellitud reserveeritud |
| `ReservPhysical` | Füüsiliselt reserveeritud |

Kui teie andmeallikaks on tarneahela haldus, ei pea te füüsilisi vaikeandmeid uuesti looma. Siiski saate neid etappe järgides luua väliste andmeallikate jaoks uusi füüsilisi mõõtmeid.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. **Valige vahekaardil Andmeallikas** andmeallikas, et lisada füüsilised meetmed (nt `ecommerce` andmeallikale). Seejärel valige jaotises **Füüsilised** mõõtmised **suvand Lisa** ja määrake mõõtu nimi (nt kui `Returned` soovite tagastatud kogused selles andmeallikas varude nähtavusse salvestada). Salvestage muudatused.

### <a name="calculated-measures"></a>Arvutatud mõõtmed

Varude nähtavust saate kasutada nii varude füüsiliste mõõtmete kui *kohandatud arvutatud mõõtmete* päringu esitamiseks. Arvutatud mõõtmed annavad kohandatud arvutusvalemi, mis koosneb füüsiliste mõõtmete kombinatsioonist. See funktsioon võimaldab teil määratleda füüsiliste mõõtmete komplekti, mis liidetakse, ja füüsiliste mõõtmete komplekti, mis lahutatakse kohandatud mõõtude moodustamiseks.

> [!IMPORTANT]
> Arvutatud mõõt on füüsiliste mõõtide koostis. Selle valem võib sisaldada ainult füüsilisi arvutusi ilma duplikaatideta, arvutamata arvutab arvutab.

Konfiguratsioon võimaldab teil määratleda arvutatud mõõtu valemite komplekti, mis sisaldab liitmise või lahutamise modifikaatoriid, et saada kogu liidetud väljundkogus.

Kohandatud arvutatud mõõtme seadistamiseks toimige järgmiselt.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Tehke arvutatud mõõtme lisamiseks vahekaardil **Arvutatud mõõde** valik **Uus arvutatud mõõde**.
1. Seadke uuele arvutatud mõõtudele järgmised väljad:

    - **Uus arvutatud mõõtunimi** – sisestage arvutatud mõõtu nimi.
    - **Andmeallikas** : valige andmeallikas, et kaasata uus arvutatud mõõt. Päringusüsteem on andmeallikas.

1. Valige **lisa**, et lisada uuele arvutatud mõõtu muutja.
1. Seadke uuele muutujale järgmised väljad:

    - **Modifikaatoriga**: valige muutuja tüüp (liitmine *või* *lahutamine*).
    - **Andmeallikas** : valige andmeallikas, kust tuleks leida muutuja väärtusega mõõt.
    - **Mõõt**: valige mõõtu nimi (valitud andmeallikast), mis annab muutujale väärtuse.

1. Korrake juhiseid 5–6, kuni olete kõik vajalikud modifikaatorid lisanud ja arvutatud mõõtu valemi lõpule viinud.
1. Valige käsk **Salvesta**.

Näiteks kasutab moeettevõtet kolme andmeallikat:

- `pos`: vastab kaupluse kanalile.
- `fno`– vastab tarneahela haldamisele.
- `ecommerce`: vastab teie veebikanalile.

Arvutatud mõõtudeta, kui te küsite toote D0002 (Kabinet) kohta saidil 1, `ColorID``Red` laos 11 ja dimensiooni väärtuses, võite saada järgmise päringu tulemuse, mis näitab varude koguseid iga eelkonfigureeritud füüsilise mõõdu all. Kuid te ei näe oma andmeallikates kõigi reserveerimiskoguste jaoks saadaolevat nähtavust.

```json
[
    {
        "productId": "D0002",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Seejärel konfigureerite arvutatud mõõtme nimega `MyCustomAvailableforReservation`, nii nagu järgmises tabelis näidatud. Tarbimise süsteem tarbib selle arvutatud mõõtme.

| Tarbimise süsteem | Arvutatud mõõde | Andmeallikas | Füüsiline mõõde | Kalkulatsiooni tüüp |
|---|---|---|---|---|
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Selle arvutusvalemi kasutamisel sisaldab uus päringutulemus kohandatud mõõdet.

```json
[
    {
        "productId": "D0002",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Üksuse `MyCustomAvailableforReservation` väljund, mis põhineb kohandatud mõõtmiste arvutamise sättel, on 100 + 50 - 10 + 80 - 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Sektsiooni konfiguratsioon

Sektsiooni konfiguratsioon koosneb praegu kahest põhidimensioonist (`SiteId``LocationId` ja ) sellest, kuidas andmeid jaotatakse. Sama sektsiooni toimingutega saab madalama hinnaga jõudlust parandada. Järgmine tabel näitab vaikimisi sektsiooni konfiguratsiooni, mille pakub varude nähtavuse lisandmoodul.

| Põhidimensioon | Hierarhia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Lahendus sisaldab vaikimisi seda sektsiooni konfiguratsiooni. Seetõttu ei *pea te seda ise määratlema*.

> [!IMPORTANT]
> Ärge kohandage sektsiooni vaikekonfiguratsiooni. Selle kustutamisel või muutmisel võib põhjustada ootamatu tõrge.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Tooteindeksi hierarhia konfiguratsioon

Enamasti ei ole vaba kaubavaru päring üksnes kõrgeimal "kogusumma" tasemel. Selle asemel võite soovida näha tulemusi, mis on laodimensioonide alusel koondatud.

Varude nähtavus pakub paindlikkust, lubades teil seadistada *indekseid* päringute jõudluse parandamiseks. Need indeksid põhinevad dimensioonil või dimensioonide kombinatsioonil. Indeks koosneb *määratud numbrist*, *dimensioonist* ja *hierarhiast*, nii nagu määratletud järgmises tabelis.

| Nimi | Kirjeldus |
|---|---|
| Komplekti number | Samasse komplekti (indeksisse) kuuluvad dimensioonid grupeeritakse kokku ja neile eraldatakse sama komplekti number. |
| Dimensioon | Põhidimensioonid, mille põhjal päringu tulemus koondatakse. |
| Hierarhia | Hierarhia võimaldab teil suurendada kindlate dimensioonikombinatsioonide jõudlust, kui seda kasutatakse päringu ja grupeerimise parameetrites. Näiteks kui seadistate dimensioonikogumi `(ColorId, SizeId, StyleId)` hierarhiaseeriaga, saab süsteem nelja dimensioonikombinatsiooniga seotud päringuid kiiremini töödelda. Esimene kombinatsioon on tühi, teine on `(ColorId)`, kolmas on `(ColorId, SizeId)` ja neljas on `(ColorId, SizeId, StyleId)`. Muid kombinatsioone ei saa kokku võtta. Filtrid ei ole tellimusega piiratud, vaid need peavad nende dimensioonide sees olema, kui soovite nende jõudlust parandada. Lisateavet vt järgmistest näitest. |

Tootehierarhia indeksi seadistamiseks toimige järgmiselt.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Dimensioonide vastenduste lisamiseks valige vahekaardilt **Tootehierarhia indeks** jaotisest **Dimensioonide vastendused** suvand **Lisa**.
1. Vaikimisi antakse indeksite loend. Olemasoleva indeksi muutmiseks valige vastava indeksi jaotisest **Redigeeri** või **Lisa**. Uue indeksikomplekti loomiseks valige suvand **Uus indeksikomplekt**. Iga indeksikomplekti iga rea jaoks valige väljal **Dimensioon** põhidimensioonide loendi hulgast. Järgmiste väljade väärtused luuakse automaatselt.

    - **Komplekti number** - samasse gruppi (indeksisse) kuuluvad dimensioonid grupeeritakse kokku ja neile eraldatakse sama komplekti number.
    - **Hierarhia** – hierarhia parandab kindlate dimensioonikombinatsioonide jõudlust, kui seda kasutatakse päringu parameetrites filtreerimiseks ja grupeerimiseks.

> [!TIP]
> Siin on mõned vihjed, mida indeksihierarhia seadistamisel silmas pidada.
>
> - Sektsiooni konfiguratsioonis määratletud põhidimensioone ei pea indeksikonfiguratsioonides määratlema. Kui indeksikonfiguratsioonis on baasdimensioon uuesti määratletud, ei saa te selle indeksi alusel päringuid esitada.
> - Kui teil on vaja teha päringuid ainult kõigi dimensioonide kombinatsioonidega liidetud varude kohta, siis seadistage üksik indeks, mis sisaldab baasdimensiooni `Empty`.

### <a name="example"></a>Näide

See jaotis annab näite hierarhia toimimise kohta.

Järgmises tabelis on toodud selle näite kohta saadaolevate varude loend.

| Kaup | ColorId | SizeId | StyleId | Kogus |
|---|---|---|---|---|
| D0002 (uuendatud) | Must | Väike | Lai | 1 |
| D0002 (uuendatud) | Must | Väike | Tavaline | 2 |
| D0002 (uuendatud) | Must | Suur | Lai | 3 |
| D0002 (uuendatud) | Must | Suur | Tavaline | 4 |
| D0002 (uuendatud) | Punane | Väike | Lai | 5 |
| D0002 (uuendatud) | Punane | Väike | Tavaline | 6 |
| D0002 (uuendatud) | Punane | Suur | Tavaline | 7 |

Järgmine tabel näitab, kuidas indeksi hierarhiat seadistatakse.

| Komplekti number | Dimensioon | Hierarhia |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indeks võimaldab teil teha vaba kaubavaru kohta päringuid järgmistel viisidel:

- `()`– Grupeeritud kõige alusel

    - D0002, 28

- `(ColorId)` – Grupeeritud `ColorId` alusel

    - D0002, Must, 10
    - D0002, Punane, 18

- `(ColorId, SizeId)` – Grupeeritud kombinatsiooni `ColorId` ja `SizeId` alusel

    - D0002, must, väike, 3
    - D0002, Must, Suur, 7
    - D0002, Punane, Väike, 11
    - D0002, Punane, Suur, 7

- `(ColorId, SizeId, StyleId)` – Grupeeritud kombinatsiooni `ColorId`, `SizeId`, ja `StyleId` alusel

    - D0002, must, väike, wide, 1
    - D0002, must, väike, Regulaarne, 2
    - D0002, Must, Suur, Wide, 3
    - D0002, Must, Suur, Regulaarne, 4
    - D0002, Punane, Väike, Lai, 5
    - D0002, Punane, Väike, Regulaarne, 6
    - D0002, punane, suur, regulaarne, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Reserveeringu konfiguratsioon (valikuline)

Kui soovite kasutada esialgse reserveerimise funktsiooni, on vajalik reserveeringu konfiguratsioon. Konfiguratsioon koosneb kahest põhiosast.

- Esialgse reserveerimise vastendus
- Esialgse reserveeringu hierarhia

### <a name="soft-reservation-mapping"></a>Esialgse reserveerimise vastendus

Reserveerides võite soovida teada, kas vaba kaubavaru on praegu reserveerimiseks saadaval. Kinnitamine on seotud arvutatud mõõtmega, mis esindab füüsiliste mõõtmete kombinatsiooni arvutusvalemit.

Seadistades vastendamise füüsiliselt mõõtmelt arvutatud mõõtmele, lubate Varude nähtavuse teenusel automaatselt kontrollida reserveeringu saadavust vastavalt füüsilisele mõõtmele.

Enne vastendamise seadistamist peavad konfiguratsioonilehe andmeallika ja arvutatud mõõtu vahekaardil olema määratletud füüsilised mõõtmised, **·** **arvutatud** mõõtmised ja nende andmeallikad (nagu kirjeldatud käesolevas artiklis).**·** Power Apps

Esialgse reserveerimise vastendamise määratlemiseks toimige järgmiselt.

1. Määratlege füüsiline mõõt, mis toimib esialgse reserveeringu mõõduna (nt `SoftReservPhysical`).
1. Määrake lehe **Konfiguratsioon** vahekaardil **Arvutatud mõõde** *reserveerimiseks saadaolev* (AFR) arvutatud mõõde, mis sisaldab selle ARF-i arvutamise valemit, mida soovite füüsilise mõõtmega vastendada. Näiteks võite seadistada väärtuse `AvailableToReserve` (reserveerimiseks saadaval) nii, et see vastendatakse varem määratletud füüsilise mõõtmega `SoftReservPhysical`. Sel viisil saate leida, millised kogused, mille varude olek on `SoftReservPhysical`, on reserveerimiseks saadaval. Järgmine tabel näitab AFR-i arvutamise valemit.

    | Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
    |---|---|---|
    | Lisa | `fno` | `AvailPhysical` |
    | Lisa | `pos` | `Inbound` |
    | Lahutamine | `pos` | `Outbound` |
    | Lahutamine | `iv` | `SoftReservPhysical` |

    Soovitame teil seadistada arvutatud mõõt nii, et see sisaldaks füüsilist mõõtu, mis reserveerimismõõt põhineb. Nii mõjutab broneeritud mõõdu kogus arvutatud mõõdu kogust. Seetõttu peaks andmeallika arvutatud `AvailableToReserve` mõõt sisaldama `iv` komponendina `SoftReservPhysical` sisaldama füüsilist `iv` mõõtu.

1. Avage lehekülg **Konfiguratsioon**.
1. Seadistage vahekaardil **Esialgse reserveeringu vastendamine** vastendamine füüsiliselt mõõtmelt arvutatud mõõtmele. Eelmise näite korral võite kasutada järgmisi sätteid, et vastendada `AvailableToReserve` varem määratletud füüsilise mõõduga `SoftReservPhysical`.

    | Füüsilise mõõtme andmeallikas | Füüsiline mõõde | Reserveerimiseks saadaolev andmeallikas | Reserveerimiseks saadaolev arvutatud mõõde |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Enne kui saate vahekaarti **Esialgse reserveeringu vastendamine** redigeerida, peate lülitama sisse funktsiooni *OnHandReservation* vahekaardil **Funktsioonihaldus**.

Kui nüüd teete `SoftReservPhysical` reserveeringu, leiab Varude nähtavus automaatselt `AvailableToReserve` ja sellega seotud arvutusvalemi reserveeringu valideerimiseks.

Näiteks on teil Varude nähtavuses järgmine vaba kaubavaru.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

Sellisel juhul kehtib järgmine arvutus.

`AvailableToReserve` = `fno.availphysical` + `pos.inbound`– –<a1/&a `pos.outbound``iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Seega, kui püüate teha reserveeringuid ja `iv.SoftReservPhysical` kogus on `AvailableToReserve` väiksem kui (10) või sellega võrdne, siis on soft reserveerimistaotlus edukas.

> [!NOTE]
> Kui kutsute reserveerimise API, saate kontrollida reserveerimise kinnitamist, määrates `ifCheckAvailForReserv` kahendmuutuja parameetri taotluse kehas. Väärtus tähendab `True`, et kontrollimine on nõutud, samas kui väärtus tähendab, `False` et kinnitamist ei nõuta (`AvailableToReserve` ehkki võite moodustada negatiivse koguse, võimaldab süsteem teil siiski teha reserveerimise kergeks). Vaikeväärtus on `True`.

### <a name="soft-reservation-hierarchy"></a>Esialgse reserveeringu hierarhia

Reserveerimishierarhia kirjeldab dimensioonide järjestust, mis tuleb reserveeringute tegemisel määratleda. See toimib samamoodi, nagu toote indeksi hierarhia töötab vaba kaubavaru päringute puhul.

Reserveerimishierarhia ei sõltu tooteindeksi hierarhiast. See sõltumatus võimaldab teil juurutada kategooriahaldust, kus kasutajad saavad dimensioonid täpsemate reserveeringute nõuete määramiseks osadeks lammutada. Teie tarkvara reserveerimise hierarhia peaks sisaldama komponentidena `SiteId` ja `LocationId`, sest need konstrueerivad sektsiooni konfiguratsiooni. Reserveeringu tegemisel peate määrama tootele sektsiooni.

Siin on soft reservation hierarhia näide.

| Põhidimensioon | Hierarhia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Selles näites saate reserveerida järgmisi dimensioonide järjestusi. Reserveeringu tegemisel peate toote jaoks eraldama sektsiooni. Seetõttu on peamine hierarhia, mida saate kasutada `(SiteId, LocationId)`.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Kehtiv dimensioonijärjestus peaks rangelt järgima reserveerimise hierarhiat dimesnioonide kaupa. Näiteks hierarhia järjestus `(SiteId, LocationId, SizeId)` ei kehti, kuna `ColorId` puudub.

## <a name="available-to-promise-configuration-optional"></a>Saadaval konfiguratsiooni lubaduse jaoks (valikuline)

Saate seadistada varude nähtavuse, et lubada teil planeerida tulevasi vaba kaubavaru muudatusi ja arvutada saadaolevaid (ATP) koguseid. ATP on kauba kogus, mis on saadaval ja mida saab kliendile järgmisel perioodil lubada. Selle arvutuse kasutamine võib tellimuse täitmise võimalusi oluliselt suurendada. Selle funktsiooni kasutamiseks peate selle lubama vahekaardil **Funktsioonihaldus** ja seejärel seadistama selle **ATP sätte vahekaardil** . Lisateavet vt varude nähtavuse [vaba kaubavaru muutmise graafikutest ja lubaduse andmiseks saadaval](inventory-visibility-available-to-promise.md).

## <a name="complete-and-update-the-configuration"></a>Lõpetage ja värskendage konfiguratsioon

Kui olete konfiguratsiooni lõpule viinud, peate kõik Varude nähtavuse muudatused kinnitama. Muudatustele muudatuste sooritamiseks järgige neid samme.

1. Valige Power Apps konfiguratsioonilehel **ülemises** parempoolses **nurgas** suvand Värskenda konfiguratsiooni. 
1. Süsteem taotleb sisselogimismandaatideks. Sisestage järgmised väärtused:

    - **Kliendi ID** – Azure'i rakenduse ID, mille lõite Varude nähtavuse jaoks.
    - **Rentniku ID** – Teie Azure'i rentniku ID.
    - **Kliendi saladus** – Azure'i rakenduse saladus, mille lõite Varude nähtavuse jaoks.

    Lisateavet nende mandaatide ja nende otsimise kohta vt Installi [ja seadista varude nähtavus](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Enne konfiguratsiooni värskendamist kontrollige kindlasti oma andmeallika nime, füüsilisi mõõte ja dimensioonivastendusi. Pärast värskendamist ei saa te neid sätteid muuta.

1. Pärast sisselogimist valige uuesti suvand **Värskenda konfiguratsiooni**. Süsteem rakendab teie sätted ja näitab, mida on muudetud.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Vaikekonfiguratsiooni näidis

Lähtestamise etapis seadistab , Inventory Visibility vaikekonfiguratsiooni, mida siin üksikasjalikult kirjeldatakse. Saate konfiguratsiooni vajaduse korral muuta.

### <a name="data-source-configuration"></a>Andmeallika konfiguratsioon

#### <a name="configuration-of-the-iv-data-source"></a>Iv andmeallika konfiguratsioon

See jaotis kirjeldab, kuidas konfigureerida `iv` andmeallikat.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Andmeallika "iv" jaoks konfigureeritud füüsilised meetmed

Andmeallika `iv` jaoks konfigureeritakse järgmised füüsilised mõõtmed.

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal arvutatud mõõde

`OrderedTotal` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `Ordered` |
| Lisa | `fno` | `Arrived` |
| Lisa | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Vaba kaubavaru arvutatud mõõde

`OnHand` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `PhysicalInvent` |
| Lisa | `iom` | `OnHand` |
| Lisa | `erp` | `Unrestricted` |
| Lisa | `erp` | `QualityInspection` |
| Lisa | `pos` | `PosInbound` |
| Lahutamine | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>ReservedTotal arvutatud mõõde

`ReservedTotal` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `ReservPhysical` |
| Lisa | `fno` | `ReservOrdered` |
| Lisa | `iv` | `SoftReservPhysical` |
| Lisa | `iv` | `SoftReservOrdered` |
| Lisa | `iv` | `ReservPhysical` |
| Lisa | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>SoftReserved arvutatud mõõde

`SoftReserved` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `iv` | `SoftReservPhysical` |
| Lisa | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>HardReserved arvutatud mõõde

`HardReserved` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `ReservPhysical` |
| Lisa | `fno` | `ReservOrdered` |
| Lisa | `iv` | `ReservPhysical` |
| Lisa | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>OpenOrder arvutatud mõõt

`OpenOrder` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `OnOrder` |
| Lisa | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>OnHandAvailable arvutatud mõõde

`OnHandAvailable` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `PhysicalInvent` |
| Lisa | `iom` | `OnHand` |
| Lisa | `erp` | `Unrestricted` |
| Lisa | `erp` | `QualityInspection` |
| Lisa | `pos` | `PosInbound` |
| Lahutamine | `fno` | `ReservPhysical` |
| Lahutamine | `iv` | `SoftReservPhysical` |
| Lahutamine | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>AvailableToReserve arvutatud mõõde

`AvailableToReserve` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `PhysicalInvent` |
| Lisa | `iom` | `OnHand` |
| Lisa | `erp` | `Unrestricted` |
| Lisa | `erp` | `QualityInspection` |
| Lisa | `pos` | `PosInbound` |
| Lisa | `fno` | `Ordered` |
| Lisa | `fno` | `Arrived` |
| Lisa | `iv` | `Ordered` |
| Lahutamine | `fno` | `ReservPhysical` |
| Lahutamine | `fno` | `ReservOrdered` |
| Lahutamine | `iv` | `SoftReservPhysical` |
| Lahutamine | `iv` | `SoftReservOrdered` |
| Lahutamine | `iv` | `ReservPhysical` |
| Lahutamine | `iv` | `ReservOrdered` |
| Lahutamine | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>InventorySupply arvutatud mõõt

`InventorySupply` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `Ordered` |
| Lisa | `fno` | `Arrived` |
| Lisa | `iv` | `Ordered` |
| Lisa | `fno` | `PhysicalInvent` |
| Lisa | `iom` | `OnHand` |
| Lisa | `erp` | `Unrestricted` |
| Lisa | `erp` | `QualityInspection` |
| Lisa | `pos` | `PosInbound` |
| Lahutamine | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>InventoryDemand arvutatud mõõt

`InventoryDemand` arvutatud mõõde konfigureeritakse `iv` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `OnOrder` |
| Lisa | `iom` | `OnOrder` |
| Lisa | `iv` | `SoftReservPhysical` |
| Lisa | `iv` | `SoftReservOrdered` |
| Liitmine | `fno` | `ReservPhysical` |
| Liitmine | `fno` | `ReservOrdered` |
| Liitmine | `iv` | `ReservPhysical` |
| Liitmine | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Andmeallika FNO konfigureerimine

See jaotis kirjeldab, kuidas konfigureerida `fno` andmeallikat.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Andmeallika "fno" dimensioonivastendused

Järgmises tabelis loetletud dimensioonivastendused on konfigureeritud `fno` andmeallika jaoks.

| Väline dimensioon | Põhidimensioon |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Andmeallika "fno" jaoks konfigureeritud füüsilised meetmed

Andmeallika `fno` jaoks konfigureeritakse järgmised füüsilised mõõtmed.

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>Andmeallika "pos" konfiguratsioon

See jaotis kirjeldab, kuidas konfigureerida `pos` andmeallikat.

##### <a name="physical-measures-for-the-pos-data-source"></a>Andmeallika "pos" füüsilised meetmed

Andmeallika `pos` jaoks konfigureeritakse järgmised füüsilised mõõtmed.

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity arvutatud mõõde

`AvailQuantity` arvutatud mõõde konfigureeritakse `pos` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõt |
|---|---|---|
| Liitmine | `fno` | `AvailPhysical` |
| Liitmine | `pos` | `PosInbound` |
| Lahutamine | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>IOM-i andmeallika konfiguratsioon

Andmeallika `iom` (nutika tellimusehalduse) jaoks on konfigureeritud järgmised füüsilised meetmed.

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Andmeallika erp konfigureerimine

Andmeallika `erp` (ettevõtte ressursiplaneerimise) jaoks on konfigureeritud järgmised füüsilised meetmed.

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Sektsiooni konfiguratsioon

Järgmine tabel näitab sektsiooni vaikekonfiguratsiooni.

| Põhidimensioon | Hierarhia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Indeksi konfiguratsioon

Järgmine tabel näitab indeksi vaikekonfiguratsiooni.

| Komplekti number | Dimensioon | Hierarhia |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Reserveeringu konfiguratsioon

Selles jaotises kirjeldatakse reserveeringu vaikekonfiguratsiooni.

#### <a name="reservation-mapping"></a>Reserveeringu vastendus

Järgmine tabel näitab reserveeringu vaikevastendust.

| Füüsilise mõõtme andmeallikas | Füüsiline mõõde | Reserveerimiseks saadaolev andmeallikas | Reserveerimiseks saadaolev arvutatud mõõde |
|---|---|---|---|
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reserveerimishierarhia

Järgmine tabel näitab reserveeringu vaikehierarhiat.

| Põhidimensioon | Hierarhia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
