---
title: Varude nähtavuse avalikud API-d
description: Selles teemas kirjeldatakse Varude nähtavuse pakutavaid avalikke API-sid.
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
ms.openlocfilehash: 0aca5838ff6d7c9c4d881698be1e2da2e0e1c02e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343628"
---
# <a name="inventory-visibility-public-apis"></a>Varude nähtavuse avalikud API-d

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Varude nähtavuse pakutavaid avalikke API-sid.

Varude nähtavuse lisandmooduli avalik REST API esitab integreerimiseks mitu kindlat lõpp-punkti. See toetab nelja peamist suhtlustüüpi.

- Lisandmoodulisse välise süsteemi kaudu vaba kaubavaru muudatuste sisestamine
- Välise süsteemi lisandmooduli vaba kaubavaru koguste seadistamine või ülekirjutamine
- Lisandmoodulisse reserveerimissündmuste sisestamine välise süsteemi kaudu
- Ajakohase vaba kaubavaru päring välisest süsteemist

Järgmises tabelis on toodud hetkel saadaolevad API-d.

| Tee | Meetod | Kirjeldus |
|---|---|---|
| /api/environment/{environmentId}/onhand | Postita | [Ühe vabade kaubavarude muutmise sündmuse loomine](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Postita | [Mitme muutmise sündmuse loomine](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Postita | [Vabade kaubavarude koguste seadistamine/ülekirjutamine](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Postita | [Ühe reserveerimissündmuse loomine](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Postita | [Mitme reserveerimissündmuse loomine](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | Hangi | [Päring sisestamismeetodi abil](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | Postita | [Päring hankimismeetodi abil](#query-with-get-method) |

Microsoftil on valmiskujul nõudekogum *Postman*. Saate importida selle kogumi oma tarkvarasse *Postman*, kasutades järgmist ühiskasutuses olevat linki: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Lõpp-punkti leidmine vastavalt Lifecycle Services keskkonnale

Varude nähtavuse mikroteenused juurutatakse rakenduses Microsoft Azure Service Fabric mitmes piirkonnas ja mitmes regioonis. Praegu puudub keskne lõpp-punkt, mida saab automaatselt ümber suunata teie taotluse vastavasse asukohta ja regiooni. Seepärast tuleb teil koostada teabetükid URL-i, kasutades järgmist mustrit.

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Regiooni lühinime leiate rakenduse Microsoft Dynamics Lifecycle Services (LCS) keskkonnast. Järgmises tabelis on toodud hetkel saadaolevad regioonid.

| Azure’i regioon | Regiooni lühinimi |
|---|---|
| Ida-Austraalia | Eau |
| Kagu-Austraalia | seau |
| Kesk-Kanada | cca |
| Ida-Kanada | eca |
| Põhja-Euroopa | neu |
| Lääne-Euroopa | weu |
| Ida-USA | eus |
| Lääne-USA | wus |
| Lõuna-ÜK | suk |
| Lääne-UK | wuk |

Saare number on see, kus teie LCS keskkond on rakendusele Service Fabric juurutatud. Praegu puudub viis selle teabe hankimiselt kasutaja poolelt.

Microsoft on loonud kasutajaliidese (UI) rakendustekomplekti Power Apps, et saaksite mikroteenuse täieliku lõpp-punkti. Lisateavet vt jaotisest [Teenuse lõpp-punkti leidmine](inventory-visibility-power-platform.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentimine

Platvormi turbeluba kasutatakse Laovarude nähtavuse API kutsumiseks. Seepärast peate _Azure Active Directory (Azure AD) loa_ genereerima kasutades Azure AD rakendust. Seejärel peate kasutama Azure AD luba, et saada _pääsutõend_ turvateenusest.

Turbeteenusetõendi hankimiseks tehke järgmist.

1. Logige Azure’i portaali sisse ja kasutage seda oma rakenduse Dynamics 365 Supply Chain Management  `clientId` ja `clientSecret` väärtuste leidmiseks.
1. Tooge Azure AD luba (`aadToken`), edastades järgmiste atribuutidega HTTP-taotluse.

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Meetod:** `GET`
    - **Sisu (vormi andmed):**

        | Võti | Väärtus |
        |---|---|
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resource | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

    Vastuseks peaksite saama Azure AD loa (`aadToken`). See peals sarnanema järgmise näitega.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Pidage meeles järgmiseid punkte.

    - Väärtus `client_assertion` peab olema see Azure AD luba (`aadToken`), mille eelmises etapis saite.
    - Väärtus `context` peab olema keskkonna ID, kus soovite lisandmooduli juurutada.
    - Häälestage kõik muud väärtused, nagu näites näidatud.

1. Edastage HTTP-taotlus, millel on järgmised atribuudid.

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

Hilisemates jaotistes kasutate luba `$access_token`, et esindada luba, mis eelmises sammus saadi.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Vaba kaubavaru muutmise sündmuste loomine

Vaba kaubavaru muutmise sündmuste loomiseks on kaks API-d.

- Ühe kirje loomine: `/api/environment/{environmentId}/onhand`
- Mitme kirje loomine: `/api/environment/{environmentId}/onhand/bulk`

Järgmine tabel võtab kokku JSON-i sisu iga välja tähenduse.

| Välja kood | Kirjeldus |
|---|---|
| `id` | Konkreetse muudatuse sündmuse kordumatu ID. Seda ID-d kasutatakse tagamaks, et kui suhtlus teenusega nurjub sisestamise ajal, ei loetaks sama sündmust süsteemis kahekordselt, kui see uuesti sisestatakse. |
| `organizationId` | Sündmusega lingitud organisatsiooni identifikaator. See väärtus vastendatakse organisatsiooniga või andmepiirkonna ID-ga rakenduses Supply Chain Management. |
| `productId` | Toote ID. |
| `quantities` | Kogus, mille võrra vaba kaubavaru kogust tuleb muuta. Näiteks kui riiulile lisatakse 10 uut raamatut, on selleks väärtuseks `quantities:{ shelf:{ received: 10 }}`. Kui kolm raamatut riiulilt eemaldatakse või müüakse, on selleks väärtuseks `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Muudatuse sündmuse ja päringu sisestamises kasutatud dimensioonide andmeallikas. Andmeallika määramisel saate kasutada määratud andmeallika kohandatud dimensioone. Varude nähtavus võib kasutada dimensiooni konfigureerimist kohandatud dimensioonide vastendamiseks üldiste vaikedimensioonidega. Kui väärtust `dimensionDataSource` pole määratletud, saate oma päringutes kasutada ainult üldisi [põhidimensioone](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dünaamiline võtme-väärtuse paar. Väärtused vastendatakse mõnede rakenduse Supply Chain Management dimensioonidega. Kuid te saate lisada ka kohandatud dimensioone (nt _Allikas_), et näidata, kas sündmus tuleb rakendusest Supply Chain Management või välisest süsteemist. |

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

Järgmises näites on toodud näidissisu. Selles näites sisestate toote *T-särki* muudatuse sündmuse. See sündmus on pärit kassa (POS) süsteemist ja klient on tagastanud punase T-särgi tagasi kauplusesse. See sündmus suurendab toote *T-särki* kogust 1 võrra.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Järgmises näites on toodud näidissisu ilma `dimensionDataSource`.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Mitme muutmise sündmuse loomine

See API võib luua korraga mitu kirjet. Ainsad erinevused selle API ja [üksiksündmuse API](#create-one-onhand-change-event) vahel on väärtused `Path` ja `Body`. Selle API puhul annab `Body` palju kirjeid.

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "@PRODUCT1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Vabade kaubavarude koguste seadistamine/ülekirjutamine

Api _Vabade kaubavarude määramine_ kirjutab konkreetse toote kehtivad andmed üle.

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

Järgmises näites on toodud näidissisu. Selle API käitumine erineb nende API-de käitumisest, mida kirjeldatakse käesolevas teemas eespool jaotises [Vabade kaubavarude muutmise sündmuste loomine](#create-onhand-change-event). Selles näites määratakse toote *T-särk* koguseks 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Reserveerimissündmuste loomine

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

API *Reserveerimine* kasutamiseks peate avama reserveerimisfunktsiooni ja viima lõpuni reserveerimise konfiguratsiooni. Lisateavet vt teemast [Reserveerimise konfigureerimine (valikuline)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Ühe reserveerimissündmuse loomine

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Mitme reserveerimissündmuse loomine

See API on [üksiksündmuse API](#create-one-reservation-event).

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

## <a name="query-on-hand"></a>Vaba kaubavaru päring

API-d _Vaba kaubavaru päring_ kasutatakse teie toodete praeguste vaba kaubavaru andmete toomiseks.

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
        organizationId: string,
        filters: {
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Järgmises näites on toodud näidissisu.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Päring hankimismeetodi abil

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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

Siin on hankimise URL-i näidis. See hankimise taotlus on täpselt sama, mis varem antud sisestamise näide.

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
