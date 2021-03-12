---
title: Varude nähtavuse lisandmoodul
description: See teema kirjeldab varude nähtavuse lisandmooduli installimist ja konfigureerimist Dynamics 365 Supply Chain Managementi jaoks.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625061"
---
# <a name="inventory-visibility-add-in"></a>Varude nähtavuse lisandmoodul

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Varude nähtavuse lisandmoodul on sõltumatu ja väga muutuv mikroteenus, mis võimaldab reaalajas vaba kaubavaru jälgimist, andes seega ülevaate varude nähtavuse kohta.

Kogu vaba kaubavaruga seotud teave eksporditakse teenusesse peaaegu reaalajas madalama taseme SQL-i integratsiooni kaudu. Välised süsteemid pääsevad teenusele juurde avatud API-de kaudu, et teha päringuid antud dimensioonide kogumi kohta, seega hankides saadaolevate vabade ametikohtade loendi.

Varude nähtavus on teenusel Common Data Service rajanev mikroteenus, mis tähendab, et saate seda laiendada, luues rakendusi Power Apps ja rakendades Power BI, et võimaldada ärivajaduste täitmiseks kohandatud funktsioone. Samuti on võimalik uuendada indeksit laopäringute tegemiseks.

Varude nähtavus pakub konfigureerimisvõimalusi, mis võimaldavad seda integreerida mitme kolmanda osapoole süsteemidega. See toetab standardset varude dimensiooni, kohandatud laiendatavust ning standardiseeritud konfigureeritavaid ja arvutatavaid koguseid.

Selles teemas kirjeldatakse, kuidas installida ja konfigureerida varude nähtavuse lisandmoodul Dynamics 365 Supply Chain Managementi jaoks ja kuidas kasutada rakenduse programmeerimise liidest (API).

## <a name="install-the-inventory-visibility-add-in"></a>Varude nähtavuse lisandmooduli installimine

Varude nähtavuse lisandmooduli saate installida, kasutades teenust Microsoft Dynamics Lifecycle Services (LCS). LCS on koostööportaal, mis pakub keskkonda ja regulaarselt värskendatud teenuseid, mis aitavad hallata Dynamics 365 Finance and Operationsi rakenduste töötsüklit.

Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Eeltingimused

Enne varude nähtavuse lisandmooduli installimist peate tegema järgmist.

- Hankige LCS-i juurutamise projekt, millel on vähemalt üks juurutatud keskkond.
- Looge oma LCS-i pakkumise beeta-võtmed.
- Lubage oma pakkumise beeta-võtmeid oma kasutajale LCS-is.
- Kontakteeruge Microsofti varude nähtavuse tootemeeskonnaga ja sisestage keskkonna ID, kus soovite varude nähtavuse lisandmoodulit kasutada.

Kui teil on küsimusi nende eeltingimuste kohta, võtke ühendust varude nähtavuse tootemeeskonnaga.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Lisandmooduli installimine

Varude nähtavuse lisandmooduli installimiseks tehke järgmist.

1. Logige sisse [teenuse Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portaali.
1. Avalehel valige projekt, kus teie keskkond juurutati.
1. Projekti lehel valige keskkond, kuhu soovite lisandmooduli installida.
1. Liikuge keskkonna lehel kerides allapoole, kuni kuvatakse jaotis **Keskkonna lisandmoodulid**. Kui jaotist ei ole näha, veenduge, et eeltingimuseks olevad beeta-võtmed oleksid täielikult töödeldud.
1. Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
    ![LCS-i keskkonna leht](media/inventory-visibility-environment.png "LCS-i keskkonna leht")
1. Valige link **Installi uus lisandmoodul**. Avaneb saadaolevate lisandmoodulite loend.
1. Valige loendist **Varude teenus**. (Pidage meeles, et selle nimi loendis võib nüüd olla **Dynamics 365 Supply Chain Managementi varude nähtavuse lisandmoodul**.)
1. Sisestage oma keskkonna järgmiste väljade väärtused.

    - **AAD Rakenduse ID**
    - **AAD Rentniku ID**

    ![Lisandmooduli häälestamise leht](media/inventory-visibility-setup.png "Lisandmooduli häälestamise leht")

1. Nõustuge tingimuste, märkides ruudu **Tingimused**.
1. Valige **Installi**. Kuvatakse lisandmooduli olek **Installimine**. Kui see on tehtud, värskendage lehte, et näha muutunud olekut **Installitud**.

### <a name="get-a-security-service-token"></a>Turbeteenusetõendi hankimine

Turbeteenusetõendi hankimiseks tehke järgmist.

1. Hankige `aadToken` ja kutsuge lõpp-punkt: https://securityservice.operations365.dynamics.com/token.
1. Asendage sisus `client_assertion` tõendiga `aadToken`.
1. Asendage sisu kontekst keskkonnas, kus soovite lisandmoodulit kasutada.
1. Asendage ulatus sisus järgmisega.

    - MCK ulatus – „https://inventoryservice.operations365.dynamics.cn/.default“  
    (Azure Active Directory MCK rakenduse ID ja rentniku ID leiate failist `appsettings.mck.json` .)
    - PROD-i ulatus – „https://inventoryservice.operations365.dynamics.com/.default“  
    (Azure Active Directory PROD-i rakenduse ID ja rentniku ID leiate failist `appsettings.prod.json`.)

    Tulemus peals sarnanema järgmise näitega.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. Saate vastuseks tõendi `access_token`. Seda on teil vaja juurepääsuloaks, et kutsuda nähtavuse API. Siin on näide.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Lisandmooduli desinstallimine

Lisandmooduli desinstallimiseks valige nupp **Desinstalli**. Värskendage LCS-i ja varude nähtavuse lisandmoodul eemaldatakse. Desinstallimise käigus eemaldatakse lisandmoodul ja käivitatakse ka töö, et kustutada kõik teenuses talletatud äriandmed.

## <a name="inventory-visibility-add-in-public-api"></a>Varude nähtavuse lisandmooduli avalik API

Varude nähtavuse lisandmooduli avalik REST API esitab integreerimiseks mitu kindlat lõpp-punkti. See toetab kolme peamist suhtlustüüpi.

- Lisandmoodulisse vaba kaubavaru muudatuste sisestamine välise süsteemi kaudu.
- Praegu vaba kaubavaru päring välisest süsteemist.
- Saadaval on automaatne sünkroonimine Supply Chain Managementiga.

Automaatne sünkroonimine ei ole osa avalikust API-st, aga see toimub taustal keskkonnas, kus on lubatud laovarude nähtavuse lisandmoodul.

### <a name="authentication"></a>Autentimine

Platvormi turbetõendit kasutatakse varude nähtavuse lisandmooduli kutsumiseks, seega tuleb teil Azure Active Directory rakenduse abil luua luba Azure Active Directory tõend.

Lisateavet selle kohta, kuidas saada turbetõend, leiate teemast [Varude nähtavuse lisandmooduli installimine](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Varude nähtavuse API konfigureerimine

Enne teenuse kasutamist peate tegema järgmistes jaotistes kirjeldatud konfiguratsioonid. Konfiguratsioon võib teie keskkonna üksikasjade põhjal erineda. See hõlmab peamiselt nelja osa.

- [Eraldamine](#partitioning)
- [Dimensioonide konfiguratsioonid](#dimension-configurations)
- [Indekseerimine](#indexing)
- [Kohandatud mõõtmine](#custom-measurement)

#### <a name="partitioning"></a>Sektsioonimine

Sektsioonimine võib oluliselt mõjutada varude nähtavuse API jõudlust. Mõistlik on määratleda skeem, mis võimaldab väikseid andmegruppe, aga samas ka sisukaid andmepäringuid.

`organizationId` (Supply Chain Managementis `dataAreaId`) on alati osa sektsioonimisest ja varude nähtavuse vaikeväärtuseks on määratud sektsioonid, mille dimensioonid on *Sait +asukoht*. See tähendab, et teenusepäringu esitamiseks peab need dimensioonid alati filtreerima.

> [!NOTE]
> *Sait* ja *asukoht* on varude nähtavuses kaks üldist vaikedimensiooni. Supply Chain Managementis nimetatakse neid dimensioone *saidiks* (`InventSiteId`) ja *laoks* (`InventLocationId`)

### <a name="dimension-configurations"></a>Dimensioonide konfiguratsioonid

Varude nähtavus annab loendi üldistest dimensioonidest, et lubada mitme allika süsteemi integreerimist.

Järgmises tabelis loetletakse varude dimensioonid, mis on varude nähtavuse dimensioonide nimed.

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

> [!NOTE]
> Eelmises tabelis loetletud dimensiooni tüüp on ainult teave. Varude nähtavuses ei ole vaja määratleda dimensiooni tüüpi.

Kui on olemas kohandatud dimensioon ja see peab muutuma vaikeväärtuseks, kui varude nähtavus seda kasutab, saate **kohandatud dimensiooni** nime varude nähtavuses konfigureerida.

Väliste süsteemide juurdepääs varude nähtavusele läbi RESTfuli API-de, mis võimaldavad esitada teavet antud dimensioonide kohta. Integratsiooni jaoks võimaldab varude nähtavus teil konfigureerida *väliskanali andmeallika* ja lähtedimensiooni vastavalt *sihtdimensioonile* varude nähtavuse korral.

Sihtdimensioonid peavad hõlmama ühte järgmistest.

- Varude nähtavuse vaikedimensioonid
- Kohandatud dimensioonid

Dimensioonide konfigureerimise eesmärk on ühtlustada mitme süsteemi integreerimist vastavalt päringule dimensioonide ja sisestamise sündmuse dimensioonidega.

#### <a name="indexing"></a>Indekseerimine

Enamiku ajast ei ole vaba kaubavaru päring mitte ainult kõrgeimal „kogutasemel“, kuid soovi korral saate vaadata varude dimensioonide alusel summeeritud tulemusi.

Varude nähtavus annab paindlikkuse, lubades teil häälestada indekseid, mis põhinevad dimensioonil või dimensioonide kombinatsioonil.

> [!NOTE]
> Praegu saate indekseid konfigureerida ainult kuni viieni. Peate hoolikalt kaaluma, millist dimensiooni või dimensioonide kombinatsiooni kasutate enne rakendamist, et tagada selle vastavus teie ettevõtte vajadustele. Näiteks kui soovite teha päringuid toodete kohta järgmiselt.

- Päring saadaval oleva summeeritud toote kohta *värvi* ja *suuruse* dimensioonide kaupa.
- Mõnel juhul soovite ainult toote kohta päringut esitada.

Teil oleks kaks indeksit, mis on määratletud järgmiselt.

- `["ColorId", "SizeId"]`
- `[]`

Tühi sulg summeeritakse sektsioonis toote ID põhjal.

Indekseerimine määratleb, kuidas saate oma tulemusi grupeerida päringusätte `groupBy` alusel. Sel juhul, kui te ei määratle ühtegi sätte `groupBy` väärtust, saate kogusummad `productid` kaupa. Vastasel juhul, kui määrate `groupBy` väärtuseks `groupBy=ColorId&groupBy=SizeId`, saadetaks teile mitu rida, mis põhinevad süsteemi erinevate värvide ja suuruse kombinatsioonidel.

Saate esitada päringu kriteeriumid päringu sisus.

Siin on näide päringust toote värvi ja suuruse kombinatsiooniga.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Kohandatud mõõtmine

Vaikimisi mõõtmiskogused on seotud Supply Chain Managementiga, kuid soovi korral võib olla kogus, mis koosneb vaikimisi mõõtmiste kombinatsioonist. Selleks võib olla kohandatud koguste konfiguratsioon, mis lisatakse vabade päringute väljundile.

Funktsioon võimaldab teil kohandatud mõõtmiseks määratleda lisatavate mõõtude kogumi ja/või meetmete kogumi, mis on kohandatud mõõtmisest lahutatud.

Näiteks järgmise päringu tingimusega konfigureerite kohandatud mõõtmise koguse üksusena `MyCustomAvailableforReservation`, mida tarbib tarbimise süsteem.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Tarbimise süsteem | Arvutatud mõõdikud | Andmeallikas | Muutuja | Muutuja arvutustüüp |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Lisa |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Lisa |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Lahutamine |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Lisa |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Lahutamine |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Lisa |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Lisa |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Lahutamine |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Lahutamine |

Sellega tagastatakse kohandatud mõõtmise koguse päring järgmise väljundina.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Üksuse `MyCustomAvailableforReservation` väljundi aluseks on kohandatud mõõtmiste arvutamise säte.  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Vaba kaubavaru muudatuste sisestamine

Sündmuse sisestamise täpne URL sõltub geograafilisest piirkonnast. See on järgmises vormis.

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Kui see on autenditud, saab seda URL-i kasutada koos HTTP `POST`-meetodiga, et saata teenusele vaba kaubavaru muudatuste sündmusi.

Dynamics 365 teenustega suhtlemiseks HTTP-taotluste kaudu kasutatakse spetsiaalset päist, mis tähistab Supply Chain Managementi eksemplari keskkonna ID-d, millega andmed on lingitud. Näide:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Vaba kaubavaru muudatuste päringu sisestamise näide 1

See näide näitab olukorda, kus häälestate dimensiooni konfiguratsiooni Power Appsis.

Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone. Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Vaba kaubavaru muudatuste päringu sisestamise näide 2

Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada. Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` on väärtusega null, tühi või seal on tühik.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON-dokumendi väljade atribuudid

Eespool antud JSON-päringu näidete väljadel on järgmises tabelis loetletud atribuudid.

| Välja kood | Kirjeldus |
|---|---|
| `id` | Konkreetse muudatuse sündmuse kordumatu ID. Seda ID-d kasutatakse tagamaks, et kui suhtlus teenusega nurjub sisestamise ajal, ei põhjustaks sündmuse taasesitamine süsteemis sama sündmuse topeltloendamist. |
| `organizationId` | Sündmusega lingitud organisatsiooni identifikaator. See vastendab Supply Chain Managementi organisatsioonide või andmepiirkonna ID-sid. |
| `productId` | Kõnealuse toote identifikaator. |
| `quantity` | Kogus, mille võrra laoseisu tuleb muuta. Kui riiulile lisati näiteks kümme uut saiakest, oleks see väärtus 10. Kui riiulilt eemaldati või müüdi kolm saiakest, oleks see väärtus -3. |
| `dimensionDataSource` | See on sisestatud muudatuse sündmuses ja päringus kasutatud andmeallikas. Andmeallika määramisel saate kasutada määratud andmeallika kohandatud dimensioone. Dimensiooni konfigureerimisega saab varude nähtavus vastendada kohandatud dimensioonid üldiste vaikedimensioonidega. Kui väärtust `dimensionDataSource` pole määratud, saate päringutes kasutada ainult üldisi vaikedimensioone.   |
| `dimensions` | Dünaamiline võtme-/väärtusepaari mapp. Need vastendavad mõned dimensioonid Supply Chain Managementis, kuid võite lisada ka kohandatud dimensioone (nt *Allikas*), mis võib tähistada sündmuse pärinemist Supply Chain Managementist või välisest süsteemist. |

### <a name="querying-current-on-hand"></a>Praeguse vaba kaubavaru päring

Praeguse laoseisu päringute puhul on lõpp-punktil sarnane URL.

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

See on päringus meetodiga HTTP `POST`.

#### <a name="current-on-hand-query-example-1"></a>Praeguse vaba kaubavaru päringu näide 1

See näide näitab olukorda, kus olete Power Appsis dimensioonide konfigureerimise juba lõpule viinud.

Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone. Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks. Saate määrata väärtuse `DimensionDataSource` üksusel `filters` ja määrata kohandatud dimensioonid nii üksuse `filters` kui ka `groupByValues` jaoks. Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Praeguse vaba kaubavaru päringu näide 2

Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada. Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` jaotises `filters` on väärtusega null, tühi või seal on tühik.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Näide tagastatud tulemusest

Eelmistes näidetes kuvatud päringud võivad tagastada sellise tulemuse.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Võtke arvesse, et koguseväljad on struktuurilt justkui meetmete ja nendega seotud väärtuste sõnastikud.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]