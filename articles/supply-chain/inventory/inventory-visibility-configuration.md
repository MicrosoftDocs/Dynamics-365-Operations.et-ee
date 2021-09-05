---
title: Varude nähtavuse konfigureerimine
description: Selles teemas kirjeldatakse, kuidas Varude nähtavust konfigureerida.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345029"
---
# <a name="inventory-visibility-configuration"></a>Varude nähtavuse konfiguratsioon

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse, kuidas Varude nähtavust konfigureerida.

## <a name="introduction"></a><a name="introduction"></a>Sissejuhatus

Enne kui alustate Varude nähtavusega tööd, peate lõpuni viima järgmise konfiguratsiooni, nii nagu selles teemas kirjeldatud.

- [Andmeallika konfiguratsioon](#data-source-configuration)
- [Sektsiooni konfiguratsioon](#partition-configuration)
- [Tooteindeksi hierarhia konfiguratsioon](#index-configuration)
- [Reserveeringu konfiguratsioon (valikuline)](#reservation-configuration)
- [Vaikekonfiguratsiooni näidis](#default-configuration-sample)

> [!NOTE]
> Varude nähtavuse konfiguratsioone saate vaadata ja redigeerida rakenduses [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration). Kui konfiguratsioon on lõpule viidud, valige rakenduses **Konfiguratsiooni värskendamine**.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Andmeallika konfiguratsioon

Andmeallikas tähistab süsteemi, millest teie andmed tulevad. näidete hulka kuuluvad `fno` (mis tähistab rakendusi Dynamics 365 Finance and Operations) and `pos` (mis tähistab kassat).

Andmeallika konfiguratsioon hõlmab järgmisi osi.

- Dimensioon (dimensiooni vastendamine)
- Füüsiline mõõde
- Arvutatud mõõde

> [!NOTE]
> Andmeallikas `fno` on reserveeritud rakendusele Dynamics 365 Supply Chain Management.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensioon (dimensiooni vastendamine)

Dimensioonide konfigureerimise eesmärk on ühtlustada mitme süsteemi integreerimist sündmuste ja päringute sisestamise jaoks vastavalt dimensioonide kombinatsioonidele.

Varude nähtavus toetab järgmisi üldiseid põhidimensioone.

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

> [!NOTE]
> Eelmises tabelis loetletud dimensiooni tüübid on ainult viiteks. Te ei pea neid Varude nähtavuses määratlema.
>
> Varude (kohandatud) dimensioone saab reserveerida rakenduse Supply Chain Management jaoks. Sel juhul saate kasutada laiendatud dimensioone.

Välistel süsteemidel on juurdepääs Varude nähtavusele läbi selle RESTful API-de. Integreerimiseks võimaldab Varude nähtavus konfigureerida _välise andmeallika_ ja vastenduse _väliselt dimensioonilt_ _põhidimensioonile_. Siin on dimensioonide vastenduse tabeli näide.

| Väline dimensioon | Põhidimensioon |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Dimensioonide vastendamise konfigureerimisel saate saata välised dimensioonid otse Varude nähtavusse. Varude nähtavus teisendab seejärel välised dimensioonid automaatselt põhidimensioonideks.

### <a name="physical-measures"></a>Füüsilised mõõtmed

Füüsilised mõõtmed muudavad kogust ja kajastavad varude olekut. Vastavalt vajadustele saate määratleda omaenda füüsilised mõõtmed.

Varude nähtavus annab vaikimise füüsiliste mõõtude loendi, mis on seotud rakendusega Supply Chain Management (`fno` andmeallikaga). Järgmine tabel esitab füüsiliste mõõtmete näite.

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

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Arvutatud mõõtmed

Arvutatud mõõtmed annavad kohandatud arvutusvalemi, mis koosneb füüsiliste mõõtmete kombinatsioonist. See funktsioon võimaldab teil määratleda füüsiliste mõõtmete komplekti, mis liidetakse, ja füüsiliste mõõtmete komplekti, mis lahutatakse kohandatud mõõtude moodustamiseks.

Näiteks on teil järgmised päringutulemused.

```json
[
    {
        "productId": "T-shirt",
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
            "externalchannel": {
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
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Selle arvutusvalemi kasutamisel sisaldab uus päringutulemus kohandatud mõõdet.

```json
[
    {
        "productId": "T-shirt",
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
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Üksuse `MyCustomAvailableforReservation` väljund, mis põhineb kohandatud mõõtmiste arvutamise sättel, on 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Sektsiooni konfiguratsioon

Sektsiooni konfiguratsioon koosneb põhidimensioonide kombinatsioonist. See määratleb andmejaotuse mustri. Andmetoimingud samas sektsioonis toetavad kõrget jõudlust ja ei maksa liiga palju. Seetõttu võivad head sektsioonimustrid anda märkimisväärseid eeliseid.

Varude nähtavus annab järgmise sektsiooni vaikekonfiguratsiooni.

| Põhidimensioon | Hierarhia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Sektsiooni vaikekonfiguratsioon on ainult viiteks. Te ei pea seda Varude nähtavuses määratlema. Sektsiooni konfiguratsiooni täiendust praegu ei toetata.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Tooteindeksi hierarhia konfiguratsioon

Enamasti ei ole vaba kaubavaru päring üksnes kõrgeimal "kogusumma" tasemel. Selle asemel võite soovida näha ka tulemusi, mis on koondatud varude dimensioonide alusel.

Varude nähtavus pakub paindlikkust, võimaldades teil seadistada _indekseid_. Need indeksid põhinevad dimensioonil või dimensioonide kombinatsioonil. Indeks koosneb *määratud numbrist*, *dimensioonist* ja *hierarhiast*, nii nagu määratletud järgmises tabelis.

| Nimi | Kirjeldus |
|---|---|
| Komplekti number | Samasse komplekti (indeksisse) kuuluvad dimensioonid grupeeritakse kokku ja neile eraldatakse sama komplekti number. |
| Dimensioon | Põhidimensioonid, mille põhjal päringu tulemus koondatakse. |
| Hierarhia | Hierarhiat kasutatakse toetatud dimensioonikombinatsioonide määratlemiseks, mille kohta saab päringu esitada. Näiteks seadistate dimensioonikomplekti, mille hierarhia järjestus on `(ColorId, SizeId, StyleId)` Sel juhul toetab süsteem nelja dimensioonikombinatsiooni päringuid. Esimene kombinatsioon on tühi, teine on `(ColorId)`, kolmas on `(ColorId, SizeId)` ja neljas on `(ColorId, SizeId, StyleId)`. Teisi kombinatsioone ei toetata. Lisateavet vt järgmistest näitest. |

### <a name="example"></a>Näide

See jaotis annab näite hierarhia toimimise kohta.

Laos on järgmised kaubad.

| Kaup | ColorId | SizeId | StyleId | Kogus |
|---|---|---|---|---|
| T-särk | Must | Väike | Lai | 1 |
| T-särk | Must | Väike | Tavaline | 2 |
| T-särk | Must | Suur | Lai | 3 |
| T-särk | Must | Suur | Tavaline | 4 |
| T-särk | Punane | Väike | Lai | 5 |
| T-särk | Punane | Väike | Tavaline | 6 |
| T-särk | Punane | Suur | Tavaline | 7 |

Siin on indeks.

| Komplekti number | Dimensioon | Hierarhia |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indeks võimaldab teil teha vaba kaubavaru kohta päringuid järgmistel viisidel:

- `()`– Grupeeritud kõige alusel

    - T-särk, 28

- `(ColorId)` – Grupeeritud `ColorId` alusel

    - T-särk, must, 10
    - T-särk, punane, 18

- `(ColorId, SizeId)` – Grupeeritud kombinatsiooni `ColorId` ja `SizeId` alusel

    - T-särk, must, väike, 3
    - T-särk, must, suur, 7
    - T-särk, punane, väike, 11
    - T-särk, punane, suur, 7

- `(ColorId, SizeId, StyleId)` – Grupeeritud kombinatsiooni `ColorId`, `SizeId`, ja `StyleId` alusel

    - T-särk, must, väike, lai, 1
    - T-särk, must, väike, tavaline, 2
    - T-särk, must, suur, lai, 3
    - T-särk, must, suur, tavaline, 4
    - T-särk, punane, väike, lai, 5
    - T-särk, punane, väike, tavaline, 6
    - T-särk, punane, suur, tavaline, 7

> [!NOTE]
> Sektsiooni konfiguratsioonis määratletud põhidimensioone ei tohi määratleda indeksi konfiguratsioonides.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Reserveeringu konfiguratsioon (valikuline)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Kui soovite kasutada esialgse reserveerimise funktsiooni, on vajalik reserveeringu konfiguratsioon. Konfiguratsioon koosneb kahest põhiosast.

- Esialgse reserveerimise vastendus
- Esialgse reserveeringu hierarhia

### <a name="soft-reservation-mapping"></a>Esialgse reserveerimise vastendus

Reserveerides võite soovida teada, kas vaba kaubavaru on praegu reserveerimiseks saadaval. Kinnitamine on seotud arvutatud mõõtmega, mis esindab füüsiliste mõõtmete kombinatsiooni arvutusvalemit.

Näiteks põhineb reserveeringu mõõde `SoftReservOrdered` füüsilisel mõõtmel andmeallikast `iv` (Varude nähtavus). Sel juhul saate seadistada andmeallika `iv` arvutatud mõõtme `AvailableToReserve`, nagu siin näidatud.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `AvailPhysical` |
| Lisa | `pos` | `Inbound` |
| Lahutamine | `pos` | `Outbound` |
| Lahutamine | `iv` | `SoftReservOrdered` |

Seejärel seadistage esialgse reserveeringu vastendamine, et anda vastendus `SoftReservOrdered` reserveeringu mõõtmelt arvutatud mõõtmele `AvailableToReserve`.

| Füüsilise mõõtme andmeallikas | Füüsiline mõõde | Reserveerimiseks saadaolev andmeallikas | Reserveerimiseks saadaolev arvutatud mõõde |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Kui nüüd teete `SoftReservOrdered` reserveeringu, leiab Varude nähtavus automaatselt `AvailableToReserve` ja sellega seotud arvutusvalemi reserveeringu valideerimiseks.

Näiteks on teil Varude nähtavuses järgmine vaba kaubavaru.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Seetõttu, kui püüate teha `iv.SoftReservOrdered` reserveeringuid ja kogus on väiksem või võrdne kui `AvailableToReserve` (10) saate reserveeringu teha.

### <a name="soft-reservation-hierarchy"></a>Esialgse reserveeringu hierarhia

Reserveerimishierarhia kirjeldab dimensioonide järjestust, mis tuleb reserveeringute tegemisel määratleda. See toimib samamoodi, nagu toote indeksi hierarhia töötab vaba kaubavaru päringute puhul.

Reserveerimishierarhia ei sõltu tooteindeksi hierarhiast. See sõltumatus võimaldab teil juurutada kategooriahaldust, kus kasutajad saavad dimensioonid täpsemate reserveeringute nõuete määramiseks osadeks lammutada.

Siin on esialgse reserveeringu hierarhia näide.

| Põhidimensioon | Hierarhia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Selles näites saate reserveerida järgmisi dimensioonide järjestusi.

- `()`– Dimensiooni ei ole määratletud.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Kehtiv dimensioonijärjestus peaks rangelt järgima reserveerimise hierarhiat dimesnioonide kaupa. Näiteks hierarhia järjestus `(SiteId, LocationId, SizeId)` ei kehti, kuna `ColorId` puudub.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Vaikekonfiguratsiooni näidis

Lähtestamise etapis seadistab Varude nähtavus vaikekonfiguratsiooni. Saate konfiguratsiooni vajaduse korral muuta.

### <a name="data-source-configuration"></a>Andmeallika konfiguratsioon

#### <a name="configuration-of-the-iv-data-source"></a>Iv andmeallika konfiguratsioon

See jaotis kirjeldab, kuidas konfigureerida `iv` andmeallikat.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Iv andmeallika jaoks konfigureeritud füüsilised meetmed

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
| Lisa | `fno` | `ReservPhysical` |
| Lisa | `fno` | `ReservOrdered` |
| Lisa | `iv` | `ReservPhysical` |
| Lisa | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Fno andmeallika konfiguratsioon

See jaotis kirjeldab, kuidas konfigureerida `fno` andmeallikat.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Fno andmeallika dimensioonivastendused

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fno andmeallika jaoks konfigureeritud füüsilised meetmed

Andmeallika `fno` jaoks konfigureeritakse järgmised füüsilised mõõtmed.

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Pos andmeallika konfiguratsioon

See jaotis kirjeldab, kuidas konfigureerida `pos` andmeallikat.

##### <a name="physical-measures-for-the-pos-data-source"></a>Pos andmeallika jaoks konfigureeritud füüsilised meetmed

Andmeallika `pos` jaoks konfigureeritakse järgmised füüsilised mõõtmed.

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity arvutatud mõõde

`AvailQuantity` arvutatud mõõde konfigureeritakse `pos` andmeallikale nii nagu näidatud järgmises tabelis.

| Kalkulatsiooni tüüp | Andmeallikas | Füüsiline mõõde |
|---|---|---|
| Lisa | `fno` | `AvailPhysical` |
| Lisa | `pos` | `PosInbound` |
| Lahutamine | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Iom andmeallika konfiguratsioon

Andmeallika `iom` (nutika tellimusehalduse) jaoks on konfigureeritud järgmised füüsilised meetmed.

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Erp andmeallika konfiguratsioon

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

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Järgmine tabel näitab reserveeringu vaikevastendust.

| Füüsilise mõõtme andmeallikas | Füüsiline mõõde | Reserveerimiseks saadaolev andmeallikas | Reserveerimiseks saadaolev arvutatud mõõde |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reserveerimishierarhia

Järgmine tabel näitab reserveeringu vaikehierarhiat.

| Põhidimensioon | Hierarhia |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
