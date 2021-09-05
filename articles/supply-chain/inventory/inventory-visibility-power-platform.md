---
title: Varude nähtavuse rakendus
description: Selles teemas kirjeldatakse, kuidas kasutada varude nähtavuse rakendust.
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
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344998"
---
# <a name="inventory-visibility-app"></a>Varude nähtavuse rakendus

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada varude nähtavuse rakendust.

Varude nähtavus annab visualiseerimiseks mudelipõhise rakenduse. Rakendus sisaldab kolme lehekülge: **Konfiguratsioon**, **Operatiivne nähtavus** ja **Varude kokkuvõte**. Sellel on järgmised funktsioonid.

- See annab kasutajaliidese (UI) vaba kaubavaru konfigureerimiseks ja esialgse reserveerimise konfigureerimiseks.
- See toetab reaalajas vaba kaubavaru päringuid eri dimensioonide kombinatsioonide kohta.
- See annab kasutajaliidese reserveerimistaotluste sisestamiseks.
- See annab toodetele kohandatud vaba kaubavaru vaate koos kõigi dimensioonidega

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist installige ja seadistage varude nähtavuse lisandmoodul, nagu on kirjeldatud jaotises [Varude nähtavuse seadistamine](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Konfiguratsioon

Leht **Konfiguratsioon** aitab teil seadistada vaba kaubavaru konfiguratsiooni ja esialge reserveerimise konfiguratsiooni. Pärast lisandmooduli installimist sisaldab vaikekonfiguratsioon Microsoft Dynamics 365 Supply Chain Management-i väärtust (`fno` andmeallikas). Vaikesätet on võimalik üle vaadata. Lisaks sellele saate vastavalt teie äritegevuse nõuetele ja välise süsteemi lao sisestusnõuetele muuta konfiguratsiooni lahenduses [Dataverse](/powerapps/maker/common-data-service/data-platform-intro), et ühtlustada viisi, kuidas saab erinevates süsteemides varude muudatusi sisestada, korraldada ja nende kohta päringuid esitada.

### <a name="define-data-sources"></a>Andmeallikate määratlemine

Määratlete kõik *andmeallikad*, mida soovite varude nähtavuse rakendusse integreerida. Varude nähtavus toetab integreerimist erinevate andmeallikatega, nagu näiteks kassasüsteem, Supply Chain Management ja muud välised süsteemid. Vaikimisi on rakenduse Varude nähtavus andmeallikaks (`fno`) seadistatud Supply Chain Management.

Andmeallika lisamiseks toimige järgmiselt.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Andmeallika lisamiseks tehke vahekaardil **Andmeallikas** valik **Uus andmeallikas**.

> [!NOTE]
> Andmeallika lisamisel kontrollige kindlasti enne varude nähtavuse teenuse konfiguratsiooni värskendamist oma andmeallika nime, füüsilisi mõõtmeid ja dimensioonivastendusi. Pärast suvandi **Konfiguratsiooni värskendamine** valimist ei saa te neid sätteid muuta.

### <a name="set-up-dimension-mappings"></a>Dimensioonivastenduste seadistamine

Varude nähtavus annab põhidimensioonide loendi, mida saab vastendada teie andmeallika dimensioonidest. Vastendamiseks on saadaval kolmkümmend kolm dimensiooni.

- Kui kasutate ühe andmeallikana rakendust Supply Chain Management, vastendatakse 13 dimensiooni Supply Chain Managementi standarddimensioonidega. Kaksteist muud dimensiooni (`inventDimension1` kuni `inventDimension12`) vastendatakse rakenduse Supply Chain Management kohandatud dimensioonidega. Ülejäänud kaheksa dimensiooni on laiendatud dimensioonid, mida saate vastendada väliste andmeallikatega.
- Kui te ei kasuta ühe andmeallikana Supply Chain Managementi, võite dimensioonid vabalt vastendada. Järgmine tabel näitab saadaolevate dimensioonide täielikku loendit.

> [!NOTE]
> Kui dimensioon ei ole vaikedimensioonide loendis ja te kasutate välist andmeallikat, soovitame vastendamiseks kasutada dimensioone `ExtendedDimension1` kuni `ExtendedDimension8`.

| Dimensiooni tüüp | Dimensiooni nimi |
|---|---|
| Toode | `ColorId` |
| Toode | `SizeId` |
| Toode | `StyleId` |
| Toode | `ConfigId` |
| Jälitamine | `BatchId` |
| Jälitamine | `SerialId` |
| Koht | `LocationId` |
| Koht | `SiteId` |
| Varude olek | `StatusId` |
| Laopõhine | `WMSLocationId` |
| Laopõhine | `WMSPalletId` |
| Laopõhine | `LicensePlateId` |
| Muud | `VersionId` |
| Varud (kohandatud) | `InventDimension1` kuni `InventDimension12` |
| Muud | `ExtendedDimension1` kuni `ExtendedDimension8` |

Dimensioonide vastenduste lisamiseks järgige neid juhiseid.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Dimensioonide vastenduste lisamiseks valige vahekaardilt **Andmeallikas** jaotisest **Dimensioonide vastendused** suvand **Lisa**.
1. Määrake väljal **Dimensiooni nimi** lähtedimensioon.
1. Valige väljal **Põhidimensioonile** see rakenduse Varude nähtavus dimensioon, mida soovite vastendada.
1. Valige käsk **Salvesta**.

![Dimensioonivastenduste lisamine](media/inventory-visibility-dimension-mapping.png "Dimensioonivastenduste lisamine")

Näiteks kui andmeallikas sisaldab toote värvidimensiooni, saate selle vastendada põhidimensiooniga `ColorId`, et lisada kohandatud dimensioon `ProductColor` andmeallikasse `exterchannel`. Seejärel vastendatakse see põhidimensiooniga `ColorId`.

## <a name="create-a-physical-measure"></a>Füüsilise mõõtme loomine

Kui andmeallikas sisestab rakendusse Varude nähtavus varude muudatuse, sisestab see muudatuse, kasutades *füüsilisi mõõtmeid*. Füüsilised mõõtmed on muutujad, mis kajastavad summeeritud laokannete olekuid. Päringud võivad põhineda füüsilistel mõõtudel.

Varude nähtavuse rakenduses on füüsiliste vaikemõõtmete loend. Need füüsilised mõõtmed võetakse laokannete olekutest rakenduse Supply Chain Management lehelt **Vaba kaubavaru loend** (**Varude haldus \> Päringud ja aruanded \> Vaba kaubavaru loend**).

| Muutuja | Nimi |
|---|---|
| `PhysicalInvent` | Füüsilised varud |
| `ReservPhysical` | Füüsiliselt reserveeritud |
| `AvailPhysical` | Füüsiliselt vaba |
| `ReservOrdered` | Tellitud reserveeritud |
| `PostedQty` | Sisestatud kogus |
| `Deducted` | Maha arvatud |
| `Picked` | Valitud |
| `Received` | Vastuvõetud |
| `Registered` | Registreeritud |
| `Arrived` | Saabunud |
| `Ordered` | Tellitud |
| `OnOrder` | Tellimusel |
| `QuotationReceipt` | Saadud pakkumine |
| `QuotationIssue` | Pakkumise väljaminek |

Kui andmeallikaks on rakendus Supply Chain Management, ei pea te füüsilisi vaikemõõtmeid uuesti looma. Siiski saate neid etappe järgides luua väliste andmeallikate jaoks uusi füüsilisi mõõtmeid.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Valige vahekaardil **Andmeallikas** jaotises **Füüsilised mõõtmed** suvand **Lisa**, määratlege lähtemõõtme nimi ja salvestage muudatused.

## <a name="define-the-product-hierarchy-index"></a>Määratlege tootehierarhia indeks

Koondatud dimensioonigruppide seadistamisel saate kasutada rakendust Varude nähtavus vaba kaubavaru oleku kohta päringute tegemiseks. Rakenduses Varude nähtavus nimetatakse kõiki dimensioonigruppe *indeksiteks*. Iga indeks vastab määratud numbrile. Saate otsustada, milliseid dimensioone kasutatakse indekseerimise häälestamiseks, vastavalt sellele, kuidas rakenduses Varude nähtavus päringuid esitate.

Tootehierarhia indeksi seadistamiseks toimige järgmiselt.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Dimensioonide vastenduste lisamiseks valige vahekaardilt **Tootehierarhia indeks** jaotisest **Dimensioonide vastendused** suvand **Lisa**.
1. Vaikimisi antakse indeksite loend. Olemasoleva indeksi muutmiseks valige vastava indeksi jaotisest **Redigeeri** või **Lisa**. Uue indeksikomplekti loomiseks valige suvand **Uus indeksikomplekt**. Iga indeksikomplekti iga rea jaoks valige väljal **Dimensioon** põhidimensioonide loendi hulgast. Järgmiste väljade väärtused luuakse automaatselt.

    - **Komplekti number** - samasse gruppi (indeksisse) kuuluvad dimensioonid grupeeritakse kokku ja neile eraldatakse sama komplekti number.
    - **Hierarhia** – hierarhiat kasutatakse toetatud dimensioonikombinatsioonide määratlemiseks, mille kohta saab dimensioonigrupis (indeksis) päringu esitada. Näiteks kui seadistate dimensioonigrupi, mille hierarhiajärjesus on *Stiil*, *Värv* ja *Suurus*, toimetab süsteem kolme päringugrupi tulemust. Esimene grupp on ainult stiil. Teine grupp on stiili ja värvi kombinatsioon. Ja kolmas grupp on stiili, värvi ja suuruse kombinatsioon. Teisi kombinatsioone ei toetata.

Lisateavet leiate teemast [Tooteindeksi hierarhia konfiguratsioon](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Näide

See jaotis annab näite hierarhia toimimise kohta. Järgmises tabelis on toodud selle näite kohta saadaolevate varude loend.

| Kaup | Laad | Värv | Maht | Kogus |
|---|---|---|---|---|
| I0001 | Lai | Must | Väike | 1 |
| I0001 | Lai | Must | Suur | 2 |
| I0001 | Lai | Punane | Väike | 3 |
| I0001 | Tavaline | Must | Väike | 4 |
| I0001 | Tavaline | Must | Suur | 5 |
| I0001 | Tavaline | Punane | Väike | 6 |
| I0001 | Tavaline | Punane | Suur | 7 |

Järgmine tabel näitab, kuidas indeksi hierarhiat seadistatakse.

| Võti | Komplekti number | Hierarhia |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Eelnevate sätete alusel on Varude nähtavuse päringu dimensioonikombinatsioon *Stiil*, *Värv* ja *Suurus*. Hierarhia seadistus võimaldab välistel süsteemidel teha vaba kaubavaru kohta päringuid järgmistel viisidel.

- `()`– Grupeeritud kõige alusel. Siin on väljund:

    - I0001, 28

- `(StyleId)` – Grupeerimine stiili alusel. Siin on väljund:

    - I0001, Lai, 6
    - I0001, Tavaline, 22

- `(StyleId, ColorId)` – Grupeeritud stiili ja värvi kombinatsiooni alusel. Siin on väljund:

    - I0001, Lai, Must, 3
    - I0001, Lai, Punane, 3
    - I0001, Tavaline, Must, 9
    - I0001, Tavaline, Punane, 13

- `(StyleId, ColorId, SizeId)` – Grupeeritud stiili, värvi ja suuruse kombinatsiooni alusel. Siin on väljund:

    - I0001, Lai, Must, Väike, 1
    - I0001, Lai, Must, Suur, 2
    - I0001, Lai, Punane, Väike, 3
    - I0001, Tavaline, Must, Väike, 4
    - I0001, Tavaline, Must, Suur, 5
    - I0001, Tavaline, Punane, Väike, 6
    - I0001, Tavaline, Punane, Suur, 7

## <a name="set-up-a-custom-calculated-measure"></a>Kohandatud arvutatud mõõtme seadistamine

Varude nähtavust saate kasutada nii varude füüsiliste mõõtmete kui *kohandatud arvutatud mõõtmete* päringu esitamiseks.

Konfiguratsioon võimaldab teil määratleda muutujate komplekti, mis lisatakse või lahutatakse koondväljundi koguse saamiseks.

1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Tehke arvutatud mõõtme lisamiseks vahekaardil **Arvutatud mõõde** valik **Uus arvutatud mõõde**. Seejärel häälestage järgmises tabelis kirjeldatud väljad.

    | Field | Väärtus |
    |---|---|
    | Uue arvutatud mõõtme nimi | Sisestage arvutatud mõõtme nimi. |
    | Andmeallikas | Päringusüsteem on andmeallikas. |
    | Muutuja andmeallikas | Sisestage muutuja andmeallikas. |
    | Muutuja | Sisestage muutuja nimi. |
    | Muutuja tüüp | Valige muutuja tüüp (*Liitmine* või *Lahutamine*). |

Järgmises tabelis on `MyCustomAvailableforReservation` kohandatud arvutatud mõõtme näide. Lisateavet selle näite kohta leiate jaotisest [Andmeallika konfiguratsioon](inventory-visibility-configuration.md#data-source-configuration).

| Arvutatud mõõtme andmeallikas | Arvutatud mõõde | Muutuja andmeallikas | Muutuja | Muutuja tüüp |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Esialgse reserveerimise vastenduse seadistamine

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Enne kui saate vahekaarti **Esialgse reserveeringu vastendamine** redigeerida, peate lülitama sisse funktsiooni *OnHandReservation* vahekaardil **Funktsioonihaldus**.

Seadistades vastendamise füüsiliselt mõõtmelt arvutatud mõõtmele, lubate Varude nähtavuse teenusel automaatselt kontrollida reserveeringu saadavust vastavalt füüsilisele mõõtmele.

Enne selle vastenduse seadistamist tuleb määratleda füüsilised mõõtmed, arvutatud mõõtmed ja nende andmeallikad Power Appsi lehe **Konfiguratsioon** vahekaartidel **Andmeallikas** ja **Arvutatud mõõde** (nagu varem siin teemas kirjeldatud).

Esialgse reserveerimise vastendamise määratlemiseks toimige järgmiselt.

1. Määratlege füüsiline mõõt, mis toimib esialgse reserveeringu mõõduna (nt `softreservordered`).
1. Määrake lehe **Konfiguratsioon** vahekaardil **Arvutatud mõõde** *reserveerimiseks saadaolev* (AFR) arvutatud mõõde, mis sisaldab selle ARF-i arvutamise valemit, mida soovite füüsilise mõõtmega vastendada. Näiteks võite seadistada väärtuse `availforreserv` (reserveerimiseks saadaval) nii, et see vastendatakse varem määratletud füüsilise mõõtmega `softreservordered`. Sel viisil saate leida, millised kogused, mille varude olek on `softreservordered`, on reserveerimiseks saadaval. Järgmine tabel näitab AFR-i arvutamise valemit.

    | Muutuja | Andmeallikas | Mõõt |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Avage lehekülg **Konfiguratsioon**.
1. Seadistage vahekaardil **Esialgse reserveeringu vastendamine** vastendamine füüsiliselt mõõtmelt arvutatud mõõtmele. Eelmise näite korral võite kasutada järgmisi sätteid, et vastendada `availforreserv` varem määratletud füüsilise mõõduga `softreservordered`.

    | Füüsilise mõõtme andmeallikas | Füüsiline mõõde | Reserveerimiseks saadaolev andmeallikas | Reserveerimiseks saadaolev arvutatud mõõde |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Esialgse reserveerimise hierarhia seadistamine

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Enne kui saate vahekaarti **Esialgse reserveeringu hierarhia** redigeerida, peate lülitama sisse funktsiooni *OnHandReservation* vahekaardil **Funktsioonihaldus**.

Reserveerimishierarhia kirjeldab dimensioonide järjestust, mis tuleb reserveeringute tegemisel määratleda. See toimib samamoodi, nagu toote indeksi hierarhia töötab vaba kaubavaru päringute puhul.

Reserveerimishierarhia võib vaba kaubavaru indeksihierarhiast erineda. See sõltumatus võimaldab teil juurutada kategooriahaldust, kus kasutajad saavad dimensioonid täpsemate reserveeringute nõuete määramiseks osadeks lammutada.

#### <a name="example"></a>Näide

Järgmine reserveerimishierarhia on teie süsteemis seadistatud.

| Dimensioon | Hierarhia |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Arvestades seda reserveeringuhierarhiat, saate reserveerida järgmiste dimensioonide tellimustes.

- `()`– Dimensiooni ei ole antud.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Dimensioonijärjestus peaks rangelt järgima reserveerimise hierarhia järjestust dimesnioonide kaupa. Näiteks reserveeringud, millel on `(ColorId, StyleId)`, pole selles näites lubatud, sest seeria pole reserveerimishierarhias määratletud.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Funktsioonihalduse kontrollimine

Varude nähtavuse lisandmoodulil on sellised funktsioonid nagu *OnHandReservation* ja *OnHandMostSpecificBackgroundService*. Vaikimisi on need funktsioonid välja lülitatud. Nende kasutamiseks avage Power Appsi leht **Konfiguratsioon** ja seejärel lülitage need vahekaardil **Funktsioonihaldus** sisse.

### <a name="complete-and-update-the-configuration"></a>Lõpetage ja värskendage konfiguratsioon

Kui olete konfiguratsiooni lõpule viinud, peate kõik Varude nähtavuse muudatused kinnitama. Muudatuste kinnitamiseks valige **Konfiguratsiooni värskendamine** Power Appsi lehe **Konfiguratsioon** paremast ülanurgast.

Esimene kord, kui valite **Konfiguratsiooni värskendamine**, küsib süsteem teie mandaati.

- **Kliendi ID** – Azure'i rakenduse ID, mille lõite Varude nähtavuse jaoks.
- **Rentniku ID** – Teie Azure'i rentniku ID.
- **Kliendi saladus** – Azure'i rakenduse saladus, mille lõite Varude nähtavuse jaoks.

Pärast sisselogimist uuendatakse Varude nähtavuse teenuse konfiguratsioon.

> [!NOTE]
> Kontrollige kindlasti enne varude nähtavuse teenuse konfiguratsiooni värskendamist oma andmeallika nime, füüsilisi mõõtmeid ja dimensioonivastendusi. Pärast suvandi **Konfiguratsiooni värskendamine** valimist ei saa te neid sätteid muuta.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Teenuse lõpp-punkti leidmine

Kui te ei tea õiget Varude nähtavuse teenuse lõpp-punkti, avage Power Appsi leht **Konfiguratsioon** ja seejärel valige paremast ülanurgast **Kuva teenuse lõpp-punkti**. Lehel kuvatakse õige teenuse lõpp-punkt.

## <a name="operational-visibility"></a>Töö nähtavus

Leht **Töö nähtavus** annab reaalajas vaba kaubavaru päringu tulemused, põhinedes mitmete dimensioonide kombinatsioonidele. Kui funktsioon *OnHandReservation* on sisse lülitatud, saate sisestada reserveerimistaotlusi ka lehelt **Töö nähtavus**.

### <a name="on-hand-query"></a>Vaba kaubavaru päring

Vahekaardil **Vaba kaubavaru päring** kuvatakse reaalajas vaba kaubavaru päringu tulemused.

Kui valite vahekaardi **Vaba kaubavaru päring**, küsib süsteem teie mandaate, nii et see saaks juurdepääsuloa, mis on Varude nähtavuse teenuse päringuteks nõutav. Võite juurdepääsuloa lihtsalt väljale **Juurdepääsuluba** kleepida ja dialoogiboksi sulgeda. Seejärel saate sisestada vaba kaubavaru päringu taotluse.

Kui juurdepääsuluba ei kehti või kui see on aegunud, peate kleepima väljale **Juurdepääsuluba** uue loa. Sisestage õiged **Kliendi ID**, **Rentniku ID**, **Kliendi saladuse** väärtused ja valige **Värskenda**. Süsteem saab automaatselt uue kehtiva juurdepääsuloa.

Vaba kaubavaru päringu sisestamiseks sisestage päring päringu sisusse. Kasutage mustrit, mida on kirjeldatud jaotises [Päring sisestusmeetodi abil](inventory-visibility-api.md#query-with-post-method).

![Vaba kaubavaru päringu seaded](media/inventory-visibility-query-settings.png "Vaba kaubavaru päringu seaded")

### <a name="reservation-posting"></a>Reserveeringu sisestamine

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Kasutage vahekaarti **Reserveeringu sisestamine** reserveerimistaotluse sisestamiseks. Enne kui saate reserveerimistaotluse sisestada, peate lülitama sisse funktsiooni *OnHandReservation*. Selle funktsiooni kohta lisateabe saamiseks vt jaotist [Varude nähtavuse reserveeringuid](inventory-visibility-reservations.md).

Reserveerimistaotluse sisestamiseks peate väärtuse taotluse sisusse. Kasutage mustrit, mida kirjeldatakse jaotises [Ühe reserveerimissündmuse loomine](inventory-visibility-api.md#create-one-reservation-event). Seejärel valige **Sisesta**. Taotluse vastuse üksikasjade vaatamiseks valige suvand **Kuva üksikasjad**. Samuti saate vastuse üksikasjadest **reservationId** väärtuse.

## <a name="inventory-summary"></a>Varude kokkuvõte

**Varude kokkuvõte** on *Vabade varude summa olemi* kohandatud vaade. See annab toodetele varude kokkuvõtte koos kõigi dimensioonidega. Kasutades **Täpsemat filtrit**, mida Dataverse pakub, saate luua isikliku vaate, mis näitab teie jaoks olulisi ridu. Täpsema filtri võimalused lasevad teile luua mitmesuguseid vaateid, lihtsatest keerulisteni. Samuti võimaldavad nad filtritele lisada grupeeritud ja pesastatud tingimusi.

Lisateabe saamiseks **Täpsema filtri** kohta, vt jaotist [Isiklike vaadete redigeerimine või loomine täpsemate ruudustiku filtrite abil](/powerapps/user/grid-filters-advanced)

Kohandatud vaate ülaosas on kolm välja: **Vaikedimensioon**, **Kohandatud dimensioon** ja **Mõõde**. Nende väljade abil saate määrata, millised veerud on nähtavad.

Saate valida veeru päise, et praeguseid tulemusi filtreerida või sortida.

Kohandatud vaate allosas kuvatakse selline teave nagu "50 kirjet (29 valitud)" või "50 kirjet". See teave viitab praegu laaditud kirjetele **Täpsema filtri** tulemusest. Tekst "29 valitud" viitab kirjete arvule, mis on laaditud kirjete veeru päise filtri abil valitud.

Vaate allosas on nupp **Laadi veel**, mille abil saate laadida rohkem Dataverse'i kirjeid. Vaikimisi on laaditud kirjete arv 50. Kui valite **Laadi rohkem**, laaditakse vaatesse järgmised 1000 saadaolevat kirjet. Number nupul **Laadi veel** näitab praegu laaditud kirjeid ja **Täpsema filtri** tulemuste kõigi kirjete arvu.

![Varude kokkuvõte](media/inventory-visibility-onhand-list.png "Varude kokkuvõte")
