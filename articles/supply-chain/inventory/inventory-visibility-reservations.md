---
title: Varude nähtavuse reserveeringud
description: See teema kirjeldab, kuidas Varude nähtavuse abil seadistada reserveerimisfunktsiooni, et luua reserveeringuid, tarbida reserveeringuid ja/või tühistada konkreetsete varude koguste reserveerinduid.
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
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345145"
---
# <a name="inventory-visibility-reservations"></a>Varude nähtavuse reserveeringud

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

See teema kirjeldab, kuidas Varude nähtavuse abil seadistada reserveerimisfunktsiooni, et luua reserveeringuid, tarbida reserveeringuid ja/või tühistada konkreetsete varude koguste reserveerinduid.

Reserveeringud märgivad tulevikus kasutatava varude koguse. Reserveerimise loomisel takistab süsteem teistel tellimustel reserveeritud kaupu seni reserveerida või tarbida, kuni reserveering kas tarbitakse või reserveering tühistatakse. Reserveeringud luuakse, tarbitakse ja tühistatakse Varude nähtavuse teenuse API kutsete abil.

Soovi korral saate seadistada rakenduse Microsoft Dynamics 365 Supply Chain Management (ja teised kolmanda osapoole süsteemid) automaatselt tasakaalustama kogust, mis on Varude nähtavuse abil reserveeritud. Nihke kogus kustutatakse Varude nähtavuse reserveerimiskirjetest.

Kui lülitate reserveerimisfunktsiooni sisse, on rakendus Supply Chain Management automaatselt valmis Varude nähtavust kasutades tehtud reserveeringute tasakaalustamiseks.

> [!NOTE]
> Nihke funktsionaalsus nõuab rakenduse Supply Chain Management versiooni 10.0.22 või uuemat. Kui soovite kasutada Varude nähtavuse reserveeringuid, on soovitatav oodata, kuni olete uuendanud rakenduse Supply Chain Management versioonile 10.0.22 või uuemale.

## <a name="turn-on-the-reservation-feature"></a>Lülitage reserveerimisfunktsioon sisse

Reserveerimisfunktsiooni sisselülitamiseks toimige järgmiselt.

1. Avage Power Appsis **Varude nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Lülitage vahekaardil **Funktsioonihaldus** sisse funktsioon *OnHandReservation*.
1. Logige sisse rakendusse Supply Chain Management.
1. Avage **Varude haldus \> Seadistus \> Varude nähtavuse integratsiooni parameetrid**.
1. Seadke jaotises **Reserveerimise vastaskonto** valiku **Luba reserveerimise vastaskonto** väärtuseks *Jah*.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Reserveerimise funktsiooni kasutamine Varude nähtavuses

Kui kutsute reserveerimise API, märgib süsteem määratud kaupade ja koguste reserveerimise. Peate määratlema reserveerimishierarhia ja sisestama nõuded, mis vastavad sellele reserveerimishierarhiale. Seejärel saab reserveeringuid teha, kutsudes reserveerimise API-d otse.

### <a name="configure-the-reservation-hierarchy"></a>Reserveerimishierarhia konfigureerimine

Reserveerimishierarhia kirjeldab dimensioonide järjestust, mis tuleb reserveeringute tegemisel määratleda. See toimib samamoodi, nagu indeksi hierarhia töötab vaba kaubavaru päringute puhul.

Reserveerimishierarhia võib indeksihierarhiast erineda. See sõltumatus võimaldab teil juurutada kategooriahaldust, kus kasutajad saavad dimensioonid täpsemate reserveeringute nõuete määramiseks osadeks lammutada.

Esialge reserveerimishierarhia konfigureerimiseks Power Appsis avage leht **Konfiguratsioon** ja seejärel seadistage vahekaardil **Esialgse reserveerimise vastendamine** reserveerimishierarhia, lisades ja/või muutes dimensioone ja nende hierarhiatasemeid.

### <a name="call-the-reservation-api"></a>Reserveerimise API kutsumine

Reserveerimised tehakse Varude nähtavuse teenuses, esitades teenuse URL-ile nagu nt `/api/environment/{environment-ID}/onhand/reserve` SISESTAMISE taotluse.

Reserveerimiseks peab taotluse sisu sisaldama organisatsiooni ID-d, toote ID-d, reserveeritud koguseid ja dimensioone. Taotlus loob kordumatu reserveerimise ID igale reserveerimiskirjele. Reserveerimiskirje sisaldab toote ID ja dimensioonide kordumatut kombinatsiooni.

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

> [!NOTE]
> Nihke funktsionaalsus on saadaval alates versioonist 10.0.22

### <a name="set-up-the-reserve-offset-modifier"></a>Reservi vastaskonto muutja häälestamine

Reservi vastaskonto muutja määrab tellimuse töötlemise etapi, mis käivitab nihked. Etappi jälgitakse tellimuse laokande oleku alusel. Reservi vastaskonto muutuja häälestamiseks toimige järgmiselt.

1. Avage **Varude haldus \> Seadistus \> Varude nähtavuse integratsiooni parameetrid \> Reserveerimise vastaskonto**.
1. Seadistage välja **Reservi vastaskonto muutuja** väärtuseks üks järgnevatest.

    - *Tellimusel* – oleku *Kandel* korral saadab tellimus loomisel vastaskonto taotluse.
    - *Reserv* – Oleku *Reservi tellimise kanne* korral saadab tellimus vastaskonto taotluse, kui see on reserveeritud, komplekteeritud, saatelehtedega sisestatud või arveldatud. Taotlus käivitatakse ainult üks kord esimese sammu korral, kui nimetatud protsess aset leiab.

### <a name="set-up-reservation-ids"></a>Reserveerimise ID seadistamine

Reserveerimise ID märgib kordumatult reserveeringukirje Varude nähtavuses. Rakenduse Supply Chain Management kasutajad panevad reserveeringud tellimuse ridadele, et märkida vastava reserveerimiskirje vastaskonto.

Reserveeringu ID seadistamiseks rakenduses Supply Chain Management toimige järgmiselt.

1. Avage müügitellimus (nt lehelt **Kõik müügitellimused**).
1. Valige kiirkaardil **Müügitellimuse read** tellimuse rida.
1. Tehke tööriistariba kiirkaardil **Müügitellimuse read** valik **Värskenda rida \> Varud \> Varude nähtavuse integratsioon**.
1. Sisestage asjakohased reserveeringu ID-d.

Varude oleku muutmine vastab vastaskonto muutuja häälestusele.
