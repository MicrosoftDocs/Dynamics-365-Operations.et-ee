---
title: Varude nähtavuse laoseisu muudatuste graafikud ja lubaduse andmiseks saadaval
description: See artikkel kirjeldab, kuidas planeerida tulevasi vaba kaubavaru muudatusi ja arvutada saadaolevaid ATP-koguseid.
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: f831c5d5719bbbd72c7cff37b8b35826f48ce6e4
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719287"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Varude nähtavuse laoseisu muudatuste graafikud ja lubaduse andmiseks saadaval

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas *seadistada vabade* kaubavaru muudatuste graafiku funktsioon, et planeerida tulevasi vaba kaubavaru muudatusi ja arvutada lubamiseks saadaolevaid (ATP) koguseid. ATP on kauba kogus, mis on saadaval ja mida saab kliendile järgmisel perioodil lubada. Selle arvutuse kasutamine võib tellimuse täitmise võimalusi oluliselt suurendada.

Paljude tootjate, jaemüüjate võikauplejate jaoks ei piisa ainult selleks, et teada, mis praegu on saadaval. Neil peab olema täielik nähtavus tulevase saadavuse suhtes. Selline tulevane saadavus peaks arvestama tulevase pakkumise, tulevase nõudluse ja ATP-ga.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a> Funktsioonide lubamine ja seadistamine

Enne ATP kasutamist peate ATP koguste arvutamiseks seadistama ühe või mitu kalkuleeritud maksmism nii. Samuti peate selle funktsiooni sisse lülitama ja ATP sätted seadistama Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>ATP kogustele arvutatud kogused

*ATP arvutatud mõõt* on eelmääratletud arvutatud mõõt, mida kasutatakse tavaliselt praegu saadaoleva vaba kaubavaru leidmiseks. Tarnekogus *on nende füüsiliste väärtuste koguste* *summa, mille lisamistüüp on Muutja, ning nõudluse kogus on nende füüsiliste väärtuste koguste* summa, *mille* lahutamise tüüp on muutja *.*

Mitme ATP koguse arvutamiseks saate lisada mitmeid arvutatud koguseid. Erinevate füüsiliste measures kogu arv kõigis ATP arvutatud failis peab olema väiksem kui üheksa.

> [!IMPORTANT]
> Arvutatud mõõt on füüsiliste mõõtide koostis. Selle valem võib sisaldada ainult füüsilisi arvutusi ilma duplikaatideta, arvutamata arvutab arvutab.

Näiteks seadistate järgmise arvutatud mõõtu:

**Vaba =** (PhysicalInvent *OnHand* + *·* + *piiranguteta QualityInspection* + *Inbound* + *) – (* ReservPhysical *SoftReservePhysical* + *Outbound* + *·*)

Summa (*PhysicalInvent* + *OnHand* + *piiranguteta* + *QualityInspection* + *Inbound*) esindab pakkumist ja summa (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) esindab nõudlust. Seetõttu saab arvutatud mõõtu mõista järgmisel viisil:

**Vaba pakkumine –** = *·* *nõudlus*

Saate lisada teise arvutatud mõõtu, et arvutada **vaba füüsiline** ATP kogus.

**Vaba füüsiline =** (PhysicalInvent *OnHand* + *·* + *piiranguteta QualityInspection* + *Inbound* + *) – (* väljaminev *·*)

Nende kahe ATP arvutatud mõõdu vahel on kaheksa erinevat füüsilist mõõdu: PhysicalInvent, OnHand *, Piiranguteta,* *QualityInspection* *,* Inbound *,* ReservPhysical *,* SoftReservePhysical *ja* Outbound *.* *·*

Lisateavet arvutatud measures kohta vt arvutatud [võetud dest](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Lülitage sisse vaba kaubavaru muutmise graafiku funktsioon ja konfigureerige ATP sätted.

Järgige neid samme, et lülitada sisse *vaba kaubavaru muutmise graafiku* funktsioon Power Apps ja konfigureerida ATP sätted.

1. Logige sisse ja Power Apps avage varude nähtavus.
1. Avage lehekülg **Konfiguratsioon**.
1. Funktsioonihalduse **vahekaardil** lülitage funktsioon *OnhandChangeSchedule* sisse.
1. Valige vahekaart **ATP** seadistus.
1. Varude nähtavuse kohta päringute esitamine annab selle tulemuse, mis sisaldab iga siin lisatav ATP arvutatud mõõtu. Valige **lisa**, et lisada ATP jaoks uus arvutatud mõõt.
1. Seadistage järgmised väljad.

    - **Andmeallikas** : valige andmeallikas, mis on seotud arvutatud mõõtu.
    - **Arvutatud** mõõt – valige valitud andmeallikaga seotud arvutatud mõõt, mida soovite kasutada praegu saadaoleva laokoguse leidmiseks.
    - **Ajakava** periood– sisestage päevade arv, mille jooksul kasutajad saavad valitud arvutatud mõõtu kasutamisel vaadata ja esitada plaanitud vaba kaubavaru muudatusi. Laoteavet küsivad kasutajad saavad selle perioodi iga päeva kohta vaba kaubavaru, planeeritud vaba kaubavaru muudatusi ja ATP-d alustades praegusest kuupäevast. Valige täisarv vahemikus 1–7.

    > [!IMPORTANT]
    > Ajakava periood sisaldab praegust kuupäeva. Seetõttu saavad kasutajad planeerida vaba kaubavaru muutusi mis tahes ajal alates käesolevast kuupäevast (päev, mil muudatus esitati) kuni (ajakava periood – 1) päeva edasi.

1. Valige käsk **Salvesta**.
1. Korrake samme 5 kuni 7, kuni olete lisanud kõik arvutatud meetmed, mida ATP jaoks vajate.
1. Kui olete kõigi nõutud sätete konfigureerimise lõpetanud, valige suvand Uuenda **konfiguratsiooni**.

Lisateavet vt teemast Konfiguratsiooni [lõpule viimine ja värskendamine](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Kuidas vaba kaubavaru muutmise graafik ja ATP arvutused töötavad?

Vaba *kaubavaru muutmise graafik* määrab planeeritud vaba kaubavaru muudatuste eeldatavad kuupäevad ja kogused. Saate edastada vaba laoseisu muutmise ajakava varude nähtavusse, eeldusel, et kuupäevad on perioodi sees, **mis** on määratletud sättega Plaaniperiood ([vt funktsioonide lubamist ja seadistamist](#setup)). Kasutajad, kes küsivad laoteavet, saavad vaba kaubavaru koguse, planeeritud vaba kaubavaru muudatused ja ATP selle perioodi iga päeva kohta.

Plaanitud muudatused on algselt olematud ja seega ei mõjuta te tegelikke vaba kaubavaru koguseid süsteemis. Muudatustele vastamaks peate esitama vaba *kaubavaru muudatuse sündmuse*, mis uuendab tegelikku vaba kaubavaru kogust. Seejärel peate plaanitud muudatuse tagasi võtma, esitades sobiva negatiivse koguse jaoks vaba laovaru muutmise graafiku.

Näiteks te paigutate tellimuse 10 võimlemiseks ja ootate selle saabuvat homset päeva. Seega esitate te vaba muudatuse ajakava, mille sissetulev kogus on 10 ja mis on kuupäevaga homseks. Kui tellimus saabub järgmisel päeval, lisate selle oma füüsilisele vabale kaubavarule. Seejärel peate oma süsteemile muudatuse tegema, et uuendada tegelikku vaba kaubavaru kogust. Muudatuse kooskõlastamiseks esitate vaba kaubavaru muudatuse sündmuse, mille saabumiskogus on 10. Seejärel taastate planeeritud muudatuse, esitades vaba kaubavaru muudatuse ajakava, mille sissetulev kogus on -10.

Varude nähtavuse päringute puhul laoseisu ja ATP koguste kohta tagastab see järgmise teabe graafikuperioodi iga päeva kohta:

- **Kuupäev** – kuupäev, milleni tulemus kehtib. Ajavöönd on koordineeritud maailmaaeg (UTC).
- **Vaba kaubavaru kogus** – määratud kuupäeva tegelik vaba kaubavaru. See arvutus tehakse vastavalt varude nähtavuse jaoks konfigureeritud ATP arvutatud mõõtu.
- **Plaanitud** tarne – kõigi planeeritud sissetulevate koguste summa, mis ei ole määratud kuupäeva jooksul otsetarbimiseks või lähetamiseks füüsiliselt saadaval.
- **Plaanitud** nõudlus – kõigi planeeritud väljaminevate koguste summa, mida pole määratud kuupäevaks tarbitud või lähetatud.
- **ATP kogus** – minimaalne prognoositud vaba kogus, mis on saadaval määratud kuupäevast kuni graafikuperioodi lõpuni. See kogus sisaldab kõiki planeeritud koguse korrigeerimisi. See on maksimaalne kogus, mida on võimalik jooksval tarne- või tarbimiskuupäeval sel päeval lubatud.

Näiteks kui praegune kuupäev on 1. veebruar 2022 ja ajakava periood on 7, saavad kasutajad esitada planeeritud vaba kaubavaru muudatusi, mis peaksid toimuma 01. veebruarist 7. veebruarini 2022. Sellisel juhul arvutatakse 3. veebruari ATP kogus selle päeva vaba koguse alusel ja planeeritud koguste põhjal 3. veebruarist 7. veebruarini.

## <a name="example"></a>Näide

Järgnev näide näitab, kuidas planeeritud koguse seeria muudatused mõjutavad vaba kaubavaru ja ATP koguseid, mida varude nähtavus aruanded mõjutavad. See näitab ka, kuidas teha planeeritud muudatusi, kuidas kooskõlastatud graafiku muudatus mõjutab tulemusi ja mis võib ilmneda, kui te ei kinnita planeeritud muudatust.

Selle näite tulemused näitavad prognoositud *vaba kaubavaru* väärtust. See väärtus sisaldab kõiki planeeritud uuendusi illustratsiooniks, kuid varude nähtavuse kohta päringute puhul seda tegelikult ei väljastata.

1. Süsteemi jaoks konfigureeritakse ATP seadistuse lehel **järgmised sätted**:Power Apps

    - **ATP arvutatud** mõõt – teil on arvutatud mõõt, mille nimi *on Vaba*. See arvutatakse kui Vabad *= Pakkumine - Nõudlus*. Te valite siin selle mõõtmise.
    - **Ajakava** periood – valige *7*.

1. Kehtivad ka järgmised tingimused:

    - Praegune kuupäev on 1. veebruar 2022.
    - Praegune vaba kogus on 20.

1. Praeguseks kuupäevaks (1. veebruar 2022) edastate planeeritud nõudluse koguse 3 varude nähtavusse. Seetõttu on prognoositud vaba kogus 17. Tulemust näitab järgmine tabel.

    | Kuupäev | Laoseis | Plaanitud tarne | Plaanitud nõudlus | Prognoositud vaba kaubavaru | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | | | 17 | 17 |
    | 2022-02-04 | 20 | | | 17 | 17 |
    | 2022-02-05 | 20 | | | 17 | 17 |
    | 2022-02-06 | 20 | | | 17 | 17 |
    | 2022-02-07 | 20 | | | 17 | 17 |

1. Käesolevaks kuupäevaks (1. veebruar 2022) esitate planeeritud tarnekoguseks 10 3. veebruaril 2022. Tulemust näitab järgmine tabel.

    | Kuupäev | Laoseis | Plaanitud tarne | Plaanitud nõudlus | Prognoositud vaba kaubavaru | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | 10 | | 27 | 27 |
    | 2022-02-04 | 20 | | | 27 | 27 |
    | 2022-02-05 | 20 | | | 27 | 27 |
    | 2022-02-06 | 20 | | | 27 | 27 |
    | 2022-02-07 | 20 | | | 27 | 27 |

1. Jooksval kuupäeval (1. veebruar 2022) esitate järgmised planeeritud kogusemuutused:

    - Nõudluse kogus 15, 4. veebruar 2022
    - Tarnekogus 1. veebruaril 2022
    - Tarnekogus 3. veebruaril 2022

    Tulemust näitab järgmine tabel.

    | Kuupäev | Laoseis | Plaanitud tarne | Plaanitud nõudlus | Prognoositud vaba kaubavaru | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 12 |
    | 2022-02-02 | 20 | | | 17 | 12 |
    | 2022-02-03 | 20 | 10 | | 27 | 12 |
    | 2022-02-04 | 20 | | 15 | 12 | 12 |
    | 2022-02-05 | 20 | 1 | | 13 | 13 |
    | 2022-02-06 | 20 | 3 | | 16 | 16 |
    | 2022-02-07 | 20 | | | 16 | 16 |

1. Praegusel kuupäeval (1. veebruar 2022) lähetate planeeritud nõudluse koguseks 3. Seetõttu peate selle muudatuse tegema, et see kajastuks teie tegelikus vabas koguses. Muudatuse sisseostmiseks esitate vaba kaubavaru muudatuse sündmuse, mille väljaminev kogus on 3. Seejärel taastate planeeritud muudatuse, esitades vaba kaubavaru muudatuse graafiku, mille väljaminev kogus on -3. Tulemust näitab järgmine tabel.

    | Kuupäev | Laoseis | Plaanitud tarne | Plaanitud nõudlus | Prognoositud vaba kaubavaru | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 17 | | 0 | 17 | 12 |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |

1. Järgmisel päeval (2. veebruar 2022) nihutab graafiku periood edasi ühe päeva võrra. Tulemust näitab järgmine tabel.

    | Kuupäev | Laoseis | Plaanitud tarne | Plaanitud nõudlus | Prognoositud vaba kaubavaru | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |
    | 2022-02-08 | 17 | | | 16 | 16 |

1. Kuid kahe päeva pärast (4. veebruar 2022) pole 3. veebruariks planeeritud tarnekogust ikka veel saabunud. Tulemust näitab järgmine tabel.

    | Kuupäev | Laoseis | Plaanitud tarne | Plaanitud nõudlus | Prognoositud vaba kaubavaru | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-04 | 17 | | 15 | 2 | 2 |
    | 2022-02-05 | 17 | 1 | | 3 | 3 |
    | 2022-02-06 | 17 | 3 | | 6 | 6 |
    | 2022-02-07 | 17 | | | 6 | 6 |
    | 2022-02-08 | 17 | | | 6 | 6 |
    | 2022-02-09 | 17 | | | 6 | 6 |
    | 2022-02-10 | 17 | | | 6 | 6 |

    Nagu näete, ei mõjuta planeeritud (kuid mitte kooskõlastatud) vaba kaubavaru muutmine tegelikku vaba kaubavaru kogust.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a> Edastage muudatuste graafikud, muutke sündmusi ja ATP-päringuid API kaudu.

Saate kasutada järgmisi rakenduse programmeerimisliidese (API) URL-e, et edastada vabade muudatuste graafikuid, muuta sündmusi ja päringuid.

| Tee | Meetod | Kirjeldus |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Loob ühe plaanitud vaba kaubavaru muudatuse. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Saate luua mitu plaanitud vaba kaubavaru muudatust. |
| `/api/environment/{environmentId}/onhand` | `POST` | Loo üks vaba kaubavaru muudatuse sündmus. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Saate luua mitu muutuse sündmust. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Saate seda meetodit kasutades päringut`POST`. |
| `/api/environment/{environmentId}/onhand` | `GET` | Saate seda meetodit kasutades päringut`GET`. |
| `/api/environment/{environmentId}/onhand/exactquery` | `POST` | Täpne päring meetodi `POST` abil. |

Lisateavet vt varude nähtavuse avalikud [API-d](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Ühe vaba kaubavaru muutmise graafiku loomine

Luuakse vaba laoseisu muudatuste `POST` graafik, esitades taotluse vastavale varude nähtavuse teenuse URL-ile (vt [API jaotise kaudu muudatuste graafikute esitamine, sündmuste muutmine ja ATP päringud](#api-urls)). Saate esitada ka hulgitaotlusi.

Vaba kaubavaru muutmise graafikut saab luua ainult siis, kui planeeritud kuupäev on praeguse kuupäeva ja praeguse ajakava perioodi lõpu vahel. Kuupäeva ja kellaaja vorming peab *olema aasta-kuu-päev* (nt **2022-02-01**). Ajavorming peab olema täpne ainult päeva kohta.

See API loob ühe vaba kaubavaru muutmise graafiku.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
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
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Järgmises näites on toodud näidissisu ilma `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Mitme vaba kaubavaru muutmise graafiku loomine

See API võib luua korraga mitu kirjet. Ainsad erinevused selle API ja üksiksündmuse API vahel on ja `Path` väärtused`Body`. Selle API puhul annab `Body` palju kirjeid. Maksimaalne kirjete arv on 512. Seetõttu võib vaba kaubavaru muutmise graafiku hulgi-API toetada korraga kuni 512 planeeritud muudatust.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
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
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
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
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Vaba kaubavaru muutmise sündmuste loomine

Vaba kaubavaru muutmise sündmused tehakse `POST` taotluse esitamisega vastavale varude nähtavuse teenuse URL-ile (vt [API jaotise kaudu muudatusgraafikute esitamine, sündmuste muutmine ja ATP-päringud](#api-urls)). Saate esitada ka hulgitaotlusi.

> [!NOTE]
> Vaba kaubavaru muutmise sündmused pole ATP funktsioonide jaoks kordumatud, vaid on osa standardsest varude nähtavuse API-st. See näide kaasati, kuna ATP-ga töötades on olulised sündmused. Vaba kaubavaru muutuse sündmused on sarnane vaba kaubavaru muudatuse reserveeringutele, kuid sündmuse sõnumid tuleb saata erinevale API URL-ile ja `quantities``quantityByDate` sündmuste kasutamine sõnumi kehas mitte. Lisateavet vabade muudatuste sündmuste ja laovarude nähtavuse API muude funktsioonide kohta vt varude [nähtavuse avalikud API-d](inventory-visibility-api.md#create-one-onhand-change-event).

Järgmine näide näitab taotluse keha, mis sisaldab ühte vaba kaubavaru muudatuse sündmust.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Plaanitud vaba kaubavaru muudatuste ja ATP tulemuste kohta päringute koostamine

Plaanitud vaba kaubavaru muudatuste ja ATP `POST``GET` tulemuste kohta saate teha päringuid, esitades taotluse või taotluse sobivale API URL-ile (vt [API jaotisest Muudatuste graafikute esitamine, sündmuste muutmine ja ATP päringud](#api-urls)).

Kui soovite teha päringuid plaanitud `QueryATP`*vaba* kaubavaru muudatuste ja ATP tulemuste kohta, määrake selle soovil tõene.

- Kui esitate taotluse meetodiga, seadke `GET` see parameeter URL-ist.
- Kui esitate taotluse meetodiga, seadke `POST` see parameeter taotluse kehas.

> [!NOTE]
> Olenemata sellest, kas parameeter `returnNegative`*·* *on* taotluse kehas seatud tõeseks või vääraks, sisaldab tulemus negatiivseid väärtusi, kui esitate päringuid planeeritud vaba kaubavaru muudatuste ja ATP tulemuste kohta. Need negatiivsed väärtused kaasatakse, sest kui plaanitakse ainult nõudlustellimusi või kui tarnekogused on väiksemad kui nõudluse kogused, on planeeritud vaba kaubavaru muudatuse kogused negatiivsed. Kui negatiivseid väärtusi ei kaasata, oleks tulemused segased. Lisateavet selle suvandi ja selle kohta, kuidas see toimib teist tüüpi päringute korral, vt varude nähtavuse [avalikud API-d](inventory-visibility-api.md#query-with-post-method).

### <a name="query-by-using-the-post-method"></a>Päring POST-meetodi abil

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

Järgmine näide näitab, kuidas luua indeksi päringu taotluse keha, mille saab meetodi abil varude nähtavusse `POST` esitada.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "SiteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-by-using-the-get-method"></a>Päring MEETODIGA GET

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

Järgmine näide näitab, kuidas luua indeksi päringu taotluse URL-i taotlusena`GET`.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Selle taotluse tulemus `GET` on täpselt sama, mis eelmise `POST` näite taotluse tulemus.

### <a name="exact-query-by-using-the-post-method"></a>Täpne päring POST-meetodit kasutades

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

Järgmine näide näitab, kuidas luua täpne päringu taotluse keha, mille saab meetodi abil varude nähtavusse `POST` esitada.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "dimensions": ["SiteId", "LocationId"],
        "values": [
            ["1", "11"]
        ]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-result-example"></a>Päringutulemuse näide

Mõni eelnevatest päringu näidetest võib anda järgmise vastuse. Selles näites on süsteem konfigureeritud järgmiste sätetega:

- **ATP arvutatud mõõt:** *iv.onhand = pos.inbound – pos.out*
- **Ajakava periood:** *7*

Siin on vastuse keha näide.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
