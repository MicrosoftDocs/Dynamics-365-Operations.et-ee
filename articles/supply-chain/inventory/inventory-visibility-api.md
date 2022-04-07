---
title: Varude nähtavuse avalikud API-d
description: Selles teemas kirjeldatakse Varude nähtavuse pakutavaid avalikke API-sid.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: cbd33b16a4b21e8e1931bc61cb55e376e7d73179
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524461"
---
# <a name="inventory-visibility-public-apis"></a>Varude nähtavuse avalikud API-d

[!include [banner](../includes/banner.md)]


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
| /API/keskkond/{environmentId} vaba/muudatused ule | Sisesta | [Ühe plaanitud vaba kaubavaru muudatuse loomine](inventory-visibility-available-to-promise.md) |
| /API/keskkond/{environmentId} vaba/muudatuste sõlm/hulgi | Sisesta | [Mitme plaanitud vaba kaubavaru muudatuste loomine](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Sisesta | [Päring sisestamismeetodi abil](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Hangi | [Päring hankimismeetodi abil](#query-with-get-method) |

> [!NOTE]
> Tee {environmentId} osa on keskkonna ID rakenduses Microsoft Dynamics Lifecycle Services (LCS).
> 
> Hulgi-API saab tagastada maksimaalselt 512 kirjet iga taotluse kohta.

Microsoftil on valmiskujul nõudekogum *Postman*. Saate importida selle kogumi oma tarkvarasse *Postman*, kasutades järgmist ühiskasutuses olevat linki: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Lõpp-punkti leidmine vastavalt Lifecycle Services keskkonnale

Varude nähtavuse mikroteenused juurutatakse rakenduses Microsoft Azure Service Fabric mitmes piirkonnas ja mitmes regioonis. Praegu puudub keskne lõpp-punkt, mida saab automaatselt ümber suunata teie taotluse vastavasse asukohta ja regiooni. Seepärast tuleb teil koostada teabetükid URL-i, kasutades järgmist mustrit.

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Regiooni lühinime leiate rakenduse Microsoft Dynamics Lifecycle Services (LCS) keskkonnast. Järgmises tabelis on toodud hetkel saadaolevad regioonid.

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
| Lõuna-Brasiilia        | sbr               |
| Kesk-USA lõunaosa    | scus              |

Saare number on see, kus teie LCS keskkond on rakendusele Service Fabric juurutatud. Praegu puudub viis selle teabe hankimiselt kasutaja poolelt.

Microsoft on loonud kasutajaliidese (UI) rakendustekomplekti Power Apps, et saaksite mikroteenuse täieliku lõpp-punkti. Lisateavet vt jaotisest [Teenuse lõpp-punkti leidmine](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentimine

Platvormi turbeluba kasutatakse Laovarude nähtavuse API kutsumiseks. Seepärast peate _Azure Active Directory (Azure AD) loa_ genereerima kasutades Azure AD rakendust. Seejärel peate kasutama Azure AD luba, et saada _pääsutõend_ turvateenusest.

Microsoft pakub kastist välja *Postimehe* hankimismärkide kogu. Saate importida selle kogumi oma tarkvarasse *Postman*, kasutades järgmist ühiskasutuses olevat linki: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Turbeteenusetõendi hankimiseks tehke järgmist.

1. Logige Azure’i portaali sisse ja kasutage seda oma rakenduse Dynamics 365 Supply Chain Management  `clientId` ja `clientSecret` väärtuste leidmiseks.
1. Tooge Azure AD luba (`aadToken`), edastades järgmiste atribuutidega HTTP-taotluse.

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Meetod:** `GET`
   - **Sisu (vormi andmed):**

     | Võti           | Väärtus                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | resource      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

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
   - `context` väärtud peab olema LCS keskkonna ID, kus soovite lisandmooduli juurutada.
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
> Kui kasutate *Postimehe* taotluse kogumist, et kutsuda varude nähtavuse avalikud API-d, peate iga taotluse jaoks lisama kandjatõendi. Oma kandjaloa leidmiseks valige taotluse URL-i all **Autoriseerimise** vahekaart, valige **Kandjatõendi** tüüp ja kopeerige viimases sammus toodnud juurdepääsuluba. Selle teema hilisemates jaotistes kasutatakse `$access_token`, et esindada luba, mis eelmises sammus saadi.

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

> [!NOTE]
> Sektsiooni `SiteId` ja `LocationId` parameetrid konstrueerivad [partitsiooni konfiguratsioon](inventory-visibility-configuration.md#partition-configuration). Seetõttu peate need dimensioonides määrama, kui loote vaba kaubavaru muutuse sündmusi, seadistate või alistate vaba kaubavaru kogused või loote reserveerimissündmused.

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
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
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
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Mitme muutmise sündmuse loomine

See API võib luua korraga mitu kirjet. Ainsad erinevused selle API ja [üksiksündmuse API](#create-one-onhand-change-event) vahel on väärtused `Path` ja `Body`. Selle API puhul annab `Body` palju kirjeid. Maksimaalne kirjete arv on 512, mis tähendab, et vaba kaubavaru muudatuse hulgi-API võib toetada korraga kuni 512 muutuse sündmust.

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
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
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
             "PosSiteId": "1",
            "PosLocationId": "11",
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

API *Reserveerimine* kasutamiseks peate avama reserveerimisfunktsiooni ja viima lõpuni reserveerimise konfiguratsiooni. Lisateavet vt teemast [Reserveerimise konfigureerimine (valikuline)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Ühe reserveerimissündmuse loomine

Reserveerida saab erinevate andmeallikate sätete suhtes. Seda tüüpi reserveeringute konfigureerimiseks määrake parameetris esmalt `dimensionDataSource` andmeallikas. Seejärel määrake `dimensions` parameetris dimensioonid vastavalt sihtandmeallika dimensioonisätetele.

Kui kutsute reserveerimise API, saate kontrollida reserveerimise kinnitamist, määrates `ifCheckAvailForReserv` kahendmuutuja parameetri taotluse kehas. Väärtus `True` tähendab, et kinnitamist nõutakse, samas kui väärtus `False` tähendab, et kinnitamist ei nõuta. Vaikeväärtus on `True`.

Kui soovite tühistada reserveeringu või määratud laokogused reserveerimata, määrake koguseks negatiivne väärtus ja seadke `ifCheckAvailForReserv` parameetrile kinnitus `False` vahele jätmiseks.

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

Kasutage päringu _vaba laoseisu_ API-d oma toodetele praeguste vaba kaubavaru andmete toomiseks. API toetab praegu päringuid kuni 100 üksiku üksuse kohta väärtuse `ProductID` alusel. Iga `SiteID` päringu `LocationID` puhul saab määrata ka mitu väärtust. Maksimaalne limiit on määratletud kui `NumOf(SiteID) * NumOf(LocationID) <= 100`.

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

- `organizationId` sisaldab ainult üht väärtust, kuid on siiski massiiv.
- `productId` võib sisalda üht või mitut väärtust. Kui see on tühi massiiv, tagastatakse kõik tooted.
- `siteId` ja `locationId` kasutatakse rakenduses Inventory Visibility sektsioonimiseks. Saate päringu *Vaba kaubavaru* nõudes määrata rohkem kui ühe `siteId` ja `locationId` väärtuse. Praeguses väljalaskes tuleb määrata nii `siteId` väärtused kui ka `locationId` väärtused.

Parameeter `groupByValues` peaks järgima indekseerimiseks teie konfiguratsiooni. Lisateavet leiate teemast [Tooteindeksi hierarhia konfiguratsioon](./inventory-visibility-configuration.md#index-configuration).

Parameeter `returnNegative` kontrollib, kas tulemused sisaldavad negatiivseid kandeid.

> [!NOTE]
> Kui olete lubanud vaba muutmise graafiku ja lubaduse andmiseks saadaolevad funktsioonid, `QueryATP` võib teie päring sisaldada ka Boole'i parameetrit, mis kontrollib, kas päringu tulemused sisaldavad ATP teavet. Lisateavet ja näiteid vt Varude nähtavuse [vaba kaubavaru muutmise graafikutest ja on saadaval lubaduse andmiseks](inventory-visibility-available-to-promise.md).

Järgmises näites on toodud näidissisu.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

Järgmised näited näitavad, kuidas teha päringuid kõigi toodete kohta konkreetsel saidil ja asukohas.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
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

Siin on hankimise URL-i näidis. See hankimise taotlus on täpselt sama, mis varem antud sisestamise näide.

```txt
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Lubaduse andmiseks saadaval

Saate seadistada varude nähtavuse, et teil planeerida tulevasi vaba kaubavaru muudatusi ja arvutada ATP koguseid. ATP on kauba kogus, mis on saadaval ja mida saab kliendile järgmisel perioodil lubada. ATP arvutuse kasutamine võib tellimuse täitmise võimalusi oluliselt suurendada. Teavet selle kohta, kuidas seda funktsiooni lubada ja kuidas suhelda varude nähtavusega oma API kaudu pärast funktsiooni lubamist, [vt varude nähtavuse vabade kaubavarude muudatuste graafikuid ja lubaduse andmiseks saadaval graafikuid](inventory-visibility-available-to-promise.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
