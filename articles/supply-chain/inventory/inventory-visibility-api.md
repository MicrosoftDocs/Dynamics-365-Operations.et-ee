---
title: Inventory Visibility avalikud API-d
description: See artikkel kirjeldab varude nähtavuse pakutavaid avalikuid API-sid.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762830"
---
# <a name="inventory-visibility-public-apis"></a>Inventory Visibility avalikud API-d

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab varude nähtavuse pakutavaid avalikuid API-sid.

Varude nähtavuse lisandmooduli avalik REST API esitab integreerimiseks mitu kindlat lõpp-punkti. See toetab nelja peamist suhtlustüüpi.

- Lisandmoodulisse välise süsteemi kaudu vaba kaubavaru muudatuste sisestamine
- Välise süsteemi lisandmooduli vaba kaubavaru koguste seadistamine või ülekirjutamine
- Lisandmoodulisse reserveerimissündmuste sisestamine välise süsteemi kaudu
- Ajakohase vaba kaubavaru päring välisest süsteemist

Järgmises tabelis on toodud hetkel saadaolevad API-d.

| Tee | Meetod | Kirjeldus |
|---|---|---|
| /api/environment/{environmentId}/onhand | Postita | [Ühe vabade kaubavarude muutmise sündmuse loomine](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | Postita | [Mitme muutmise sündmuse loomine](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Postita | [Vabade kaubavarude koguste seadistamine/ülekirjutamine](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Sisesta | [Loo üks soft reservation sündmus](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Sisesta | [Loo mitu kerget reserveerimise sündmust](#create-multiple-reservation-events) |
| /API/keskkond/{environmentId}/töötlemata/mittereservee | Sisesta | [Tühista üks soft reservation sündmus](#reverse-one-reservation-event) |
| /API/keskkond/{environmentId}/töötlemata/reservee/hulgi | Sisesta | [Mitme tarkvara reserveerimise sündmuse tagasipööramine](#reverse-multiple-reservation-events) |
| /API/keskkond/{environmentId}/eelnevalt/muudatused ule | Sisesta | [Ühe plaanitud vaba kaubavaru muudatuse loomine](inventory-visibility-available-to-promise.md) |
| /API/keskkond/{environmentId}/eelnevalt/muudatused ule/hulgi | Sisesta | [Mitme vaba kaubavaru muudatuste loomine kuupäevadega](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Sisesta | [Päring sisestamismeetodi abil](#query-with-post-method) (soovitatav) |
| /api/environment/{environmentId}/onhand | Hangi | [Päring hankimismeetodi abil](#query-with-get-method) |
| /API/keskkond/{environmentId}/ettemärge/täpnepäring | Sisesta | [Täpne päring sisestamismeetodi abil](#exact-query-with-post-method) |
| /API/keskkond/eraldamine{environmentId}<wbr>/eraldamine | Sisesta | [Loo üks eraldav sündmus](inventory-visibility-allocation.md#using-allocation-api) |
| /API/keskkond/{environmentId} eraldamine<wbr>/unallocate | Sisesta | [Ühe unallocate sündmuse loomine](inventory-visibility-allocation.md#using-allocation-api) |
| /API/keskkond/{environmentId} eraldamine<wbr>/ümberjaotamine | Sisesta | [Loo üks ümberjaotatud sündmus](inventory-visibility-allocation.md#using-allocation-api) |
| /API/keskkond/eraldamine{environmentId}/<wbr> tarbimine | Sisesta | [Loo üks tarbitud sündmus](inventory-visibility-allocation.md#using-allocation-api) |
| /API/keskkond/eraldamine{environmentId}<wbr>/päring | Sisesta | [Päringu eraldamise tulemus](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Tee {environmentId} osa on keskkonna ID elutsükli Microsoft Dynamics teenustes.
> 
> Hulgi-API saab tagastada maksimaalselt 512 kirjet iga taotluse kohta.

Microsoftil on valmiskujul nõudekogum *Postman*. Saate importida selle kogumi oma tarkvarasse *Postman*, kasutades järgmist ühiskasutuses olevat linki: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Lõpp-punkti leidmine vastavalt Lifecycle Services keskkonnale

Varude nähtavuse mikroteenused juurutatakse rakenduses Microsoft Azure Service Fabric mitmes piirkonnas ja mitmes regioonis. Praegu puudub keskne lõpp-punkt, mida saab automaatselt ümber suunata teie taotluse vastavasse asukohta ja regiooni. Seepärast tuleb teil koostada teabetükid URL-i, kasutades järgmist mustrit.

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Regiooni lühinime leiate elutsükli teenuste keskkonnast. Järgmises tabelis on toodud hetkel saadaolevad regioonid.

| Azure’i regioon        | Regiooni lühinimi |
| ------------------- | ----------------- |
| Ida-Austraalia      | Eau               |
| Kagu-Austraalia | seau              |
| Kesk-Kanada      | cca               |
| Ida-Kanada         | eca               |
| Põhja-Euroopa        | neu               |
| Lääne-Euroopa         | weu               |
| Ida-USA             | eus               |
| Lääne-USA             | wus               |
| Lõuna-ÜK            | suk               |
| Lääne-UK             | wuk               |
| Ida-Jaapan          | ejp               |
| Lääne-Jaapan          | wjp               |
| Kesk-India       | cin               |
| Lõuna-India         | Patt               |
| Põhja-Šveits   | Nch <a0/&amp               |
| Šveitsi läänerannikud    | wch               |
| Lõuna-Prantsusmaa        | sfr               |
| Ida-Aasia           | Süsteemi <a0/               |
| Lõuna-Ida-Aasia     | Merede              |
| Põhja-Aüe           | nae               |
| Norra, Ida         | Eno (eno)               |
| Norra Lääs         | wno               |
| Lõuna-Aafrika Läänerannikud   | Wza (üks)               |
| Lõuna-Aafrika (Põhja-Aafrika)  | Nza (nza)               |

Selle saare number on koht, kus teie elutsükli teenuste keskkond juurutatakse teenus kangas. Praegu pole võimalik seda teavet kasutajapoolsest teabest saada.

Microsoft on loonud kasutajaliidese (UI) rakendustekomplekti Power Apps, et saaksite mikroteenuse täieliku lõpp-punkti. Lisateavet vt jaotisest [Teenuse lõpp-punkti leidmine](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentimine

Platvormi turbeluba kasutatakse Laovarude nähtavuse API kutsumiseks. Seepärast peate *Azure Active Directory (Azure AD) loa* genereerima kasutades Azure AD rakendust. Seejärel peate kasutama Azure AD luba, et saada *pääsutõend* turvateenusest.

Microsoft pakub kastist välja *Postimehe* hankimismärkide kogu. Saate importida selle kogumi oma tarkvarasse *Postman*, kasutades järgmist ühiskasutuses olevat linki: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Turbeteenusetõendi hankimiseks tehke järgmist.

1. Logige Azure’i portaali sisse ja kasutage seda oma rakenduse Dynamics 365 Supply Chain Management  `clientId` ja `clientSecret` väärtuste leidmiseks.
1. Tooge Azure AD luba (`aadToken`), edastades järgmiste atribuutidega HTTP-taotluse.

    - **URL:**`https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Meetod:** `GET`
    - **Sisu (vormi andmed):**

        | Võti           | Väärtus                                            |
        | ------------- | -------------------------------------------------|
        | client_id     | ${aadAppId}                                      |
        | client_secret | ${aadAppSecret}                                  |
        | grant_type    | client_credentials                               |
        | Ulatus         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.Vaikimisi    |

    Vastuseks peaksite saama Azure AD loa (`aadToken`). See peals sarnanema järgmise näitega.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Vormindage JavaScripti objektiteatise (JSON) taotlus, mis sarnaneb järgmise näitega.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Pidage meeles järgmiseid punkte.

    - Väärtus `client_assertion` peab olema see Azure AD luba (`aadToken`), mille eelmises etapis saite.
    - Väärtus `context` peab olema elutsükli teenuste keskkonna ID, kus soovite lisandmooduli juurutada.
    - Häälestage kõik muud väärtused, nagu näites näidatud.

1. Tooge juurdepääsuluba (`access_token`), esitades HTTP-päringu, millel on järgmised omadused:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Meetod:** `POST`
    - **HTTP päis:** kaasake API versioon. (Võti on `Api-Version` ja väärtus on `1.0`.)
    - **Sisu:** lisage eelmises sammus loodud JSON-i taotlus.

    Vastuseks peaksite saama juurdepääsuloa (`access_token`). Luba on teil vaja juurepääsuloaks, et kutsuda Varude nähtavuse API. Siin on näide.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Kui kasutate *Postimehe* taotluse kogumist, et kutsuda varude nähtavuse avalikud API-d, peate iga taotluse jaoks lisama kandjatõendi. Oma kandjaloa leidmiseks valige taotluse URL-i all **Autoriseerimise** vahekaart, valige **Kandjatõendi** tüüp ja kopeerige viimases sammus toodnud juurdepääsuluba. Selle artikli hilisemates jaotistes kasutatakse luba, `$access_token` mis tooti viimases sammus.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Vaba kaubavaru muutmise sündmuste loomine

Vaba kaubavaru muutmise sündmuste loomiseks on kaks API-d.

- Ühe kirje loomine: `/api/environment/{environmentId}/onhand`
- Mitme kirje loomine: `/api/environment/{environmentId}/onhand/bulk`

Järgmine tabel võtab kokku JSON-i sisu iga välja tähenduse.

| Välja kood | Kirjeldus |
|---|---|
| `id` | Konkreetse muudatuse sündmuse kordumatu ID. Kui taasedastamise põhjus on teenuse tõrge, kasutatakse seda ID-d selleks, et tagada sama sündmuse kaks korda arvestamist süsteemis. |
| `organizationId` | Sündmusega lingitud organisatsiooni identifikaator. See väärtus vastendatakse organisatsiooniga või andmepiirkonna ID-ga rakenduses Supply Chain Management. |
| `productId` | Toote ID. |
| `quantities` | Kogus, mille võrra vaba kaubavaru kogust tuleb muuta. Näiteks kui riiulile lisatakse 10 uut raamatut, on selleks väärtuseks `quantities:{ shelf:{ received: 10 }}`. Kui kolm raamatut riiulilt eemaldatakse või müüakse, on selleks väärtuseks `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Muudatuse sündmuse ja päringu sisestamises kasutatud dimensioonide andmeallikas. Andmeallika määramisel saate kasutada määratud andmeallika kohandatud dimensioone. Varude nähtavus võib kasutada dimensiooni konfigureerimist kohandatud dimensioonide vastendamiseks üldiste vaikedimensioonidega. Kui väärtust `dimensionDataSource` pole määratletud, saate oma päringutes kasutada ainult üldisi [põhidimensioone](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dünaamiline võtme-väärtuse paar. Väärtused vastendatakse mõnede rakenduse Supply Chain Management dimensioonidega. Kuid te saate lisada ka kohandatud dimensioone (nt *Allikas*), et näidata, kas sündmus tuleb rakendusest Supply Chain Management või välisest süsteemist. |

> [!NOTE]
> Sektsiooni `siteId` ja `locationId` parameetrid konstrueerivad [partitsiooni konfiguratsioon](inventory-visibility-configuration.md#partition-configuration). Seetõttu peate need dimensioonides määrama, kui loote vaba kaubavaru muutuse sündmusi, seadistate või alistate vaba kaubavaru kogused või loote reserveerimissündmused.

Järgmised alamjaotised pakuvad näiteid, mis näitavad, kuidas neid API-sid kasutada.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Ühe vabade kaubavarude muutmise sündmuse loomine

See API loob ühe vaba kaubavaru muudatuse sündmuse.

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Järgmises näites on toodud näidissisu. Selles näites on ettevõttel müügikoha (POS) süsteem, mis töötleb kaupluse kandeid ja seega laomuudatusi. Klient on tagastanud teie kauplusele punase T-särki. Muudatuse kajastamiseks sisestate T-särki tootele *ühekordse muutuse sündmuse*. See sündmus suurendab toote *T-särki* kogust 1 võrra.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Järgmises näites on toodud näidissisu ilma `dimensionDataSource`. Sel juhul, `dimensions` on [alus dimensioon](inventory-visibility-configuration.md#data-source-configuration-dimension). Kui `dimensionDataSource` on seadistatud, võivad `dimensions` olla andmeallika mõõtmed või baasmõõtmed.

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Mitme muutmise sündmuse loomine

See API võib luua muudatusi nii, nagu üksiksündmuse [API](#create-one-onhand-change-event) saab. Ainus erinevus on see, et see API saab korraga luua mitu kirjet. Seetõttu erinevad väärtused `Path``Body`. Selle API puhul annab `Body` palju kirjeid. Maksimaalne kirjete arv on 512. Seetõttu võib vaba kaubavaru hulgi-API toetada korraga kuni 512 muutuse sündmust. 

Näiteks töötles kaupluse kassamasin järgmisi kandeid:

- Üks punase T-särki tagastustellimus
- Üks kolme musta T-särki müügikanne

Sel juhul saate mõlemad laouuendused kaasata ühte API kutsesse.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

Järgmises näites on toodud näidissisu.

```json
[
    {
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Vabade kaubavarude koguste seadistamine/ülekirjutamine

Api *Vabade kaubavarude määramine* kirjutab konkreetse toote kehtivad andmed üle. Seda funktsiooni kasutatakse tavaliselt laoseisu loendusuuenduste puhul. Näiteks igapäevase laoseisu inventuuri ajal võib kauplus leida, et punane T-särk on 100 vaba kaubavaru. Seetõttu tuleb kassa sissetulev kogus uuendada 100-ks, olenemata sellest, milline oli eelmine kogus. Seda API-d saate kasutada olemasoleva väärtuse alistamiseks.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Järgmises näites on toodud näidissisu. Selle API käitumine erineb [API-de käitumisest, mida on kirjeldatud käesolevas artiklis eespoolses](#create-onhand-change-event) jaotises Vaba kaubavaru muutmise sündmuste loomine. Selles näites määratakse toote *T-särk* koguseks 1.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Reserveerimissündmuste loomine

Reservi API kasutamiseks *peate* sisse lülitama reserveerimise funktsiooni ja lõpule täitma reserveerimise konfiguratsiooni. Lisateavet (k.a andmevoog ja näidisstsenaarium) vt reserveerimise [konfiguratsiooni (valikuline)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Ühe reserveerimissündmuse loomine

Reserveerida saab erinevate andmeallikate sätete suhtes. Seda tüüpi reserveeringute konfigureerimiseks määrake parameetris esmalt `dimensionDataSource` andmeallikas. Seejärel määrake `dimensions` parameetris dimensioonid vastavalt sihtandmeallika dimensioonisätetele.

Kui kutsute reserveerimise API, saate kontrollida reserveerimise kinnitamist, määrates `ifCheckAvailForReserv` kahendmuutuja parameetri taotluse kehas. Väärtus `True` tähendab, et kinnitamist nõutakse, samas kui väärtus `False` tähendab, et kinnitamist ei nõuta. Vaikeväärtus on `True`.

Kui soovite tühistada reserveeringu või määratud laokogused reserveerimata, määrake koguseks negatiivne väärtus ja seadke parameetrile kinnitus `ifCheckAvailForReserv``False` vahele jäetud. Sama otstarbel on olemas ka sihtotstarbeline mittereserveentide API. Erinevus seisneb ainult selles, kuidas kahte API-d kutsutakse. Konkreetse reserveeringusündmuse tagasipööramine on lihtsam, kui kasutate `reservationId` seda *reserveerimata API-ga*. Lisateavet vt jaotisest Ühe [reserveeringusündmuse reserveerimine](#reverse-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Järgmises näites on toodud näidissisu.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Järgmine näide näitab edukat vastust.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Mitme reserveerimissündmuse loomine

See API on [üksiksündmuse API](#create-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>Tühista reserveerimissündmused

Reserveerimata *API on* reserveerimise sündmuste tühistamistoiming [*·*](#create-reservation-events). See võimaldab tühistada reserveerimissündmuse, mille on määranud `reservationId` või vähendada reserveerimiskogust.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a> Tühista üks reserveerimissündmus

Reserveeringu loomisel kaasatakse `reservationId` see vastuse kehaosasse. Peate sisestama sama reserveerimise `reservationId` tühistamiseks ja kaasama sama ja seda `organizationId` kasutatakse `dimensions` reserveerimise API kutses. Lõpuks määrake väärtus `OffsetQty`, mis näitab eelmisest reserveeringust vabastatavate kaupade arvu. Reserveerimise saab määratud aja järgi kas täielikult või osaliselt tühistada `OffsetQty`. Näiteks kui reserveeriti *100* kaubaühikut, `OffsetQty: 10`*saate algsest reserveeritud summast 10* reserveerimata määrata.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Järgmine kood näitab kehasisu näidet.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Järgmine kood näitab eduka vastuse keha näidet.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Vastuse kehas, kui `OffsetQty` see on reserveeringu kogusest väiksem või sellega võrdne, `processingStatus` on "*edukas*" `totalInvalidOffsetQtyByReservId` ja on *0*.
>
> Kui `OffsetQty` see on suurem kui reserveeritud summa, `processingStatus` on see "*partialSuccess*" `totalInvalidOffsetQtyByReservId` ja on reserveeritud `OffsetQty` summa vahe.
>
>Näiteks kui reserveeringu kogus on *10* ja `OffsetQty`*selle väärtus on 12*, `totalInvalidOffsetQtyByReservId` oleks *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a> Mitme reserveerimissündmuse stornatsioon

See API on [üksiksündmuse API](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [      
        {
            id: string,
            organizationId: string,
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Vaba kaubavaru päring

Kasutage päringu *vaba laoseisu* API-d oma toodetele praeguste vaba kaubavaru andmete toomiseks. Seda API-d saate kasutada alati laovarude olemasolu kohta, nt kui soovite oma e-äri veebisaidil läbi vaadata tootevarude tasemeid või kui soovite kontrollida toote saadavust regioonides või lähedalasumis kauplustes ja ladudes. API toetab praegu päringuid kuni 5000 üksiku kauba kohta väärtuse `productID` alusel. Iga `siteID` päringu `locationID` puhul saab määrata ka mitu väärtust. Maksimumlimiidi määratleb järgmine võrrand:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Päring sisestusmeetodi abil

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Taotluse kehaosa, `dimensionDataSource` on siiski valikuline parameeter. Kui see pole määratud, käsitletakse `filters` seda *põhidimensioonidena*. Väljadel on neli `filters` kohustuslikku välja: `organizationId`, `productId`, `siteId` ja `locationId`.

- `organizationId` peaks sisaldama ainult üht väärtust, kuid on siiski massiiv.
- `productId` võib sisaldada üht või enamat väärtust. Kui see on tühi massiiv, tagastatakse kõik tooted.
- `siteId` ja `locationId` kasutatakse rakenduses Inventory Visibility sektsioonimiseks. Saate päringu *Vaba kaubavaru* nõudes määrata rohkem kui ühe `siteId` ja `locationId` väärtuse. Praeguses väljalaskes tuleb määrata nii `siteId` väärtused kui ka `locationId` väärtused.

Soovitame kasutada parameetrit indekseerimisel `groupByValues` konfiguratsiooni järgimiseks. Lisateavet leiate teemast [Tooteindeksi hierarhia konfiguratsioon](./inventory-visibility-configuration.md#index-configuration).

Parameeter `returnNegative` kontrollib, kas tulemused sisaldavad negatiivseid kandeid.

> [!NOTE]
> Kui olete lubanud vaba muutmise graafiku ja lubaduse andmiseks saadaolevad funktsioonid, `QueryATP` võib teie päring sisaldada ka Boole’i parameetrit, mis kontrollib, kas päringu tulemused sisaldavad ATP teavet. Lisateavet ja näiteid vt Varude nähtavuse [vaba kaubavaru muutmise graafikutest ja on saadaval lubaduse andmiseks](inventory-visibility-available-to-promise.md).

Järgmises näites on toodud näidissisu. See näitab, et saate teha päringuid vaba kaubavaru kohta mitmest asukohast (laost).

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Järgmine näide näitab, kuidas teha päringuid kõigi toodete kohta konkreetsel saidil ja asukohas.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Päring hankimismeetodi abil

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Siin on url-i näidis. See hankimise taotlus on täpselt sama, mis varem antud sisestamise näide.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a> Vaba kaubavaru täpne päring

Vaba kaubavaru täpsed päringud sarnanevad regulaarsete vaba kaubavaru päringutega, kuid nad lasevad teil määratleda vastendamise hierarhia saidi ja asukoha vahel. Näiteks on teil kaks järgmist sasaiti:

- Sait 1, mis on vastendatud asukohaga A
- Sait 2, mis on vastendatud asukohaga B

Kui määrate ja sisestate regulaarse `"siteId": ["1","2"]``"locationId": ["A","B"]` vaba kaubavaru päringu, teeb varude nähtavus järgmiste saitide ja asukohtade kohta tulemuse kohta automaatselt päringuid:

- Koht 1, asukoht A
- Koht 1, asukoht B
- 2. koht, asukoht A
- 2. koht, asukoht B

Nagu näete, ei tunnista regulaarne vaba kaubavaru päring seda asukohta A, mis on olemas ainult saidil 1 ja asukoht B on olemas ainult 2. saidil. Seetõttu teeb see liigseid päringuid. Selle hierarhilise vastenduse mahutamiseks saate kasutada vaba kaubavaru täpset päringut ja määratleda asukoha vastendused päringu kehas. Sel juhul saate päringu ja saate tulemused ainult 1. saidi, asukoha A ja saidi 2, asukoha B kohta.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a> Täpne päring sisestamismeetodi abil

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Taotluse kehaosa on `dimensionDataSource` valikuline parameeter. Kui see pole määratud, käsitletakse `dimensions` in-dimensioone `filters` põhidimensioonidena *·*. Väljadel on neli `filters` kohustuslikku välja: `organizationId`, `productId`, `dimensions` ja `values`.

- `organizationId` peaks sisaldama ainult üht väärtust, kuid on siiski massiiv.
- `productId` võib sisaldada üht või enamat väärtust. Kui see on tühi massiiv, tagastatakse kõik tooted.
- Massiivis `dimensions` on nõutud`siteId`, `locationId` kuid võib ilmuda koos teiste elementidega mis tahes järjestuses.
- `values` võib sisaldada ühte või enamale eristatavale väärtuse tupletile, mis vastavad väärtusele `dimensions`.

`dimensions` sees `filters` lisatakse automaatselt:`groupByValues`

Parameeter `returnNegative` kontrollib, kas tulemused sisaldavad negatiivseid kandeid.

Järgmises näites on toodud näidissisu.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Järgmine näide näitab, kuidas teha päringuid kõigi toodete kohta mitmel saitidel ja asukohtades.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Lubaduse andmiseks saadaval

Saate seadistada varude nähtavuse, et teil planeerida tulevasi vaba kaubavaru muudatusi ja arvutada ATP koguseid. ATP on kauba kogus, mis on saadaval ja mida saab kliendile järgmisel perioodil lubada. ATP arvutuse kasutamine võib tellimuse täitmise võimalusi oluliselt suurendada. Teavet selle kohta, kuidas seda funktsiooni lubada ja kuidas suhelda varude nähtavusega oma API kaudu pärast funktsiooni lubamist, [vt varude nähtavuse vabade kaubavarude muudatuste graafikuid ja lubaduse andmiseks saadaval graafikuid](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Eraldamine

Eraldamisega seotud API-d asuvad varude nähtavuse [eraldamises](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
