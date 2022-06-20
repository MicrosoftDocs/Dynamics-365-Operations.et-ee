---
title: Inventory Visibility reserveeringud
description: See artikkel kirjeldab, kuidas seadistada reserveerimisfunktsiooni, et luua reserveeringuid, tarbida reserveeringuid ja/või reserveerimata määratud laokoguseid varude nähtavuse abil.
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
ms.openlocfilehash: 3b74907709ab97ddf4cc829dba324df213ca229f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895724"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility reserveeringud

[!include [banner](../includes/banner.md)]


See artikkel kirjeldab, kuidas seadistada reserveerimisfunktsiooni, et luua reserveeringuid, tarbida reserveeringuid ja/või reserveerimata määratud laokoguseid varude nähtavuse abil.

Reserveeringud märgivad tulevikus kasutatava varude koguse. Reserveerimise loomisel takistab süsteem teistel tellimustel reserveeritud kaupu seni reserveerida või tarbida, kuni reserveering kas tarbitakse või reserveering tühistatakse. Reserveeringud luuakse, tarbitakse ja tühistatakse Varude nähtavuse teenuse API kutsete abil.

Soovi korral saate seadistada rakenduse Microsoft Dynamics 365 Supply Chain Management (ja teised kolmanda osapoole süsteemid) automaatselt tasakaalustama kogust, mis on Varude nähtavuse abil reserveeritud. Nihke kogus kustutatakse Varude nähtavuse reserveerimiskirjetest.

Kui lülitate reserveerimisfunktsiooni sisse, on rakendus Supply Chain Management automaatselt valmis Varude nähtavust kasutades tehtud reserveeringute tasakaalustamiseks.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Lülitage reserveerimisfunktsioon sisse

Reserveerimisfunktsiooni sisselülitamiseks toimige järgmiselt.

1. Logige sisse rakendusse Power Apps ja avage **Inventory Visibility**.
1. Avage lehekülg **Konfiguratsioon**.
1. Lülitage vahekaardil **Funktsioonihaldus** sisse funktsioon *OnHandReservation*.
1. Logige sisse rakendusse Supply Chain Management.
1. Minge **[funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** tööruumi ja lubage *varude nähtavuse integreerimine reserveerimise vastas* funktsiooniga (nõuab versiooni 10.0.22 või uuemat).
1. Minge **Varude halduse \> Seadistus \> Inventory Visibility integreerimisparameetritele** avage **reserveerimise vastaskonto** vahekaart ja tehke järgmised sätted:
    - **Luba reserveerimise vastaskonto** – selle funktsiooni lubamiseks määrake väärtuseks *Jah*.
    - **Reserveerimise vastaskonto** - Valige laokande olek, mis tasakaalustab varude nähtavuse tehtud reserveerimised. See säte määrab tellimuse töötlemise etapi, mis käivitab vastaskontod. Etappi jälgitakse tellimuse laokande oleku alusel. Valige üks järgmistest:
        - *Tellimusel* – oleku *Kandel* korral saadab tellimus loomisel vastaskonto taotluse. Vastaskogus on loodud tellimuse kogus.
        - *Reserv* – Oleku *Reservi tellimise kanne* korral saadab tellimus vastaskonto taotluse, kui see on reserveeritud, komplekteeritud, saatelehtedega sisestatud või arveldatud. Taotlus käivitatakse ainult üks kord esimese sammu korral, kui nimetatud protsess aset leiab. Vastaskogus on kogus, mille puhul laokande olek on vastaval tellimusereal muudetud olekuks *Tellitud* või *Tellimusel reserveeritud* (või hilisem olek).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Reserveerimise funktsiooni kasutamine Varude nähtavuses

Kui kutsute reserveerimise API, märgib süsteem määratud kaupade ja koguste reserveerimise. Peate määratlema reserveerimishierarhia ja sisestama nõuded, mis vastavad sellele reserveerimishierarhiale. Seejärel saab reserveeringuid teha, kutsudes reserveerimise API-d otse.

### <a name="configure-the-reservation-hierarchy"></a>Reserveerimishierarhia konfigureerimine

Reserveerimishierarhia kirjeldab dimensioonide järjestust, mis tuleb reserveeringute tegemisel määratleda. See toimib samamoodi, nagu indeksi hierarhia töötab vaba kaubavaru päringute puhul.

Reserveerimishierarhia võib indeksihierarhiast erineda. See sõltumatus võimaldab teil juurutada kategooriahaldust, kus kasutajad saavad dimensioonid täpsemate reserveeringute nõuete määramiseks osadeks lammutada.

Esialge reserveerimishierarhia konfigureerimiseks avage Power Apps`is leht **Konfiguratsioon** ja seejärel seadistage vahekaardil **Esialgse reserveerimise vastendamine** reserveerimishierarhia, lisades ja/või muutes dimensioone ja nende hierarhiatasemeid.

Teie tarkvara reserveerimise hierarhia peaks sisaldama komponentidena `SiteId` ja `LocationId`, sest need konstrueerivad sektsiooni konfiguratsiooni.

Lisateavet reserveeringute konfigureerimise kohta vt teemast [Reserveermise konfiguratsioon](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Reserveerimise API kutsumine

Reserveerimised tehakse Varude nähtavuse teenuses, esitades teenuse URL-ile nagu nt `/api/environment/{environment-ID}/onhand/reserve` SISESTAMISE taotluse.

Reserveerimiseks peab taotluse sisu sisaldama organisatsiooni ID-d, toote ID-d, reserveeritud koguseid ja dimensioone. Taotlus loob kordumatu reserveerimise ID igale reserveerimiskirjele. Reserveerimiskirje sisaldab toote ID ja dimensioonide kordumatut kombinatsiooni.

Kui kutsute reserveerimise API, saate kontrollida reserveerimise kinnitamist, määrates `ifCheckAvailForReserv` kahendmuutuja parameetri taotluse kehas. Väärtus `True` tähendab, et kinnitamist nõutakse, samas kui väärtus `False` tähendab, et kinnitamist ei nõuta. Vaikeväärtus on `True`.

Kui soovite tühistada reserveeringu või määratud laokogused reserveerimata, määrake koguseks negatiivne väärtus ja seadke `ifCheckAvailForReserv` parameetrile kinnitus `False` vahele jätmiseks.

Siin on viiteks näide taotluse sisust.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Reserveeringute tasakaalustamine rakenduses Supply Chain Management

Laokande olekute puhul, mis hõlmavad määratud reservi vastaskonto muutujat, tasakaalustab kande uuendus vastava reserveerimiskirje, kui kõik järgmised tingimused on täidetud.

- Laokande reserveeringu ID vastab Varude nähtavuse teenuse reserveerimiskirje reserveeringu ID-le.
- Laokande dimensioonid on samad Varude nähtavuse teenuse reserveeringukirje dimensioonidega.
- Muudatused laokande olekus käivitavad reserveeringute nihked, kui laokande olek kajastab fakti, et tellimuse protsess on lõpetatud või vahele jäetud.

Nihke kogus järgib laokogust, mis on laokandel määratletud. Nihe ei jõustu, kui Varude nähtavuse teenusesse ei jää reserveeritud kogust alles.

### <a name="set-up-the-reservation-offset-modifier"></a>Seadistage broneeringu nihke teisendaja

Kui te pole seda juba teinud, seadistage reserveerimise muutja vastavalt kirjeldusele jaotises [Lülita sisse ja seadistage reserveerimisfunktsioon](#turn-on).

### <a name="set-up-reservation-ids"></a>Reserveerimise ID seadistamine

Reserveerimise ID märgib kordumatult reserveeringukirje Varude nähtavuses. Rakenduse Supply Chain Management kasutajad panevad reserveeringud tellimuse ridadele, et märkida vastava reserveerimiskirje vastaskonto.

Reserveeringu ID seadistamiseks rakenduses Supply Chain Management toimige järgmiselt.

1. Avage müügitellimus (nt lehelt **Kõik müügitellimused**).
1. Valige kiirkaardil **Müügitellimuse read** tellimuse rida.
1. Tehke tööriistariba kiirkaardil **Müügitellimuse read** valik **Värskenda rida \> Varud \> Varude nähtavuse integratsioon**.
1. Sisestage asjakohased reserveeringu ID-d.

Varude oleku muutmine vastab vastaskonto muutuja häälestusele.
