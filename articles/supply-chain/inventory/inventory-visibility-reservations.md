---
title: Inventory Visibility reserveeringud
description: See artikkel kirjeldab, kuidas seadistada reserveerimisfunktsiooni, et luua reserveeringuid, tarbida reserveeringuid ja/või reserveerimata määratud laokoguseid varude nähtavuse abil.
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
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762718"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility reserveeringud

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab tüüpilist pehmete reserveeringute puhul kasutamise juhtumit ja selgitab nende seadistamist varude nähtavuses. See sisaldab teavet selle kohta, kuidas luua kergeid reserveeringuid, tasakaalustada neid füüsilisel tarbimisel ning korrigeerida või reserveerimata määratud laokoguseid.

## <a name="sample-use-case-for-soft-reservation"></a>Soft reservationi kasutamise näidisjuhtum

Pehmed reserveerimised aitavad organisatsioonidel saavutada vabade varude jaoks ühe tõese allika, eriti tellimuse täitmise protsessi ajal. See funktsioon on kasulik organisatsioonidele, kus on järgmised tingimused:

- Organisatsioonil on vähemalt kaks eri süsteemi, mis võtab otse välja väljaminevaid tellimusi.
- Organisatsioon on väga range ning soovib vältida tootevarude topeltbronüümist, mis võib juhtuda, kui mitu süsteemi saavad viimase laovaru üle reserveerida. Selline olukord on takistab, kui kõik tellimussüsteemid saavad teha kiireid ja kergeid reserveerimise API kutseid varude nähtavusse, mis annab varude saadavaloleku kohta ühe vaba kaubavaru allika.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title=" Varude nähtavuse kerge reserveerimine" width="720" />](media/inventory-visibility-soft-reservation.png)

Eelmine näide näitab, kuidas soft reservation toimib ja tõsteb esile järgmised toimingud:

- Teie algne varude tase sünkroonitakse Microsoftilt varude nähtavusega Dynamics 365 Supply Chain Management.
- Kerged reserveeringud sisestatakse igas tellimuskanalis või -süsteemis varude nähtavusse. Varude nähtavus kinnitab varude saadavuse ja püüab teha kerget reserveerimist. Kui kerge reserveerimine õnnestus, lisab varude nähtavus kerge reserveeritavale kogusele, arvatakse reserveerimiseks saadaolevast kogusest maha ja vastab kerge reserveerimise ID-ga.
- Sel ajal jääb teie füüsiline laokogus samaks.
- Seejärel saate sünkroonida kas üksikud või koondatud mittereserveeritud tellimused (tellimuse read) tarneahela haldusse, et teha raskeid reserveeringuid ja vabastada lattu või värskendada lõplik laoseisu kogust.
- Saate seada süsteemi tasakaalustama kergeid [reserveeringuid](#offset-scm), kui füüsiline ladu on tarneahela halduses värskendatud.

Kerged reserveeringud luuakse, tarbitakse ja tühistatakse tavaliselt API kutsete abil varude nähtavuse teenusele.

> [!NOTE]
> Võite valikuliselt seadistada tarneahela halduse (ja muud kolmanda osapoole süsteemid), et automaatselt tasakaalustada reserveeritud kogus varude nähtavuse abil. Nihke kogus kustutatakse Varude nähtavuse reserveerimiskirjetest.
>
> Vaikimisi lülitatakse vastasfunktsioon automaatselt sisse, kui lubate kerge reserveerimise funktsiooni.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Lülitage reserveerimisfunktsioon sisse

Reserveerimisfunktsiooni sisselülitamiseks toimige järgmiselt.

1. Logige sisse ja Power Apps avage varude **nähtavus**.
1. Avage lehekülg **Konfiguratsioon**.
1. Lülitage vahekaardil **Funktsioonihaldus** sisse funktsioon *OnHandReservation*.
1. Logige sisse oma tarneahela haldamise keskkonda.
1. Minge **[funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** tööruumi ja lubage *varude nähtavuse integreerimine reserveerimise vastas* funktsiooniga (nõuab versiooni 10.0.22 või uuemat).
1. Minge **Varude halduse \> Seadistus \> Inventory Visibility integreerimisparameetritele** avage **reserveerimise vastaskonto** vahekaart ja tehke järgmised sätted:

    - **Luba reserveerimise vastaskonto** – selle funktsiooni lubamiseks määrake väärtuseks *Jah*.
    - **Reserveerimise vastaskonto muutja** : valige laokande olek, mis tasakaalustab varude nähtavuse tehtud reserveerimised. See säte määrab tellimuse töötlemise etapi, mis käivitab vastaskontod. Etappi jälgitakse tellimuse laokande oleku alusel. Valige üks järgmistest väärtustest.

        - *Tellimusel* – tellimused, mille *olek* on Tellimusel, saadavad loomisel vastaskonto taotluse. Vastaskogus on loodud tellimuse (rea) kogus.
        - *Reserveerimine* : tellimused, mille *olek* on Reserveeri, saadavad vastaskonto taotluse, kui need on kas reserveeritud või füüsiliselt reserveeritud. Kui tasakaalustate *olekus* Reserveeri, saadab tellimus tasakaalustustaotluse mis tahes uue lao oleku korral, mis on komplekteeritud reserveeritud olekule lähim (nt komplekteeritud, saatelehega sisestatud või arveldatud). Selline käitumine toimub isegi siis, kui jätte tarneahela halduses reserveeringu vahele ja jätkate teise varude olekuga (nt kui jätte väljalaskest lattu vahele, et neid komplekteerida ja pakkida). Taotlus käivitatakse ainult üks kord. Kui see käivitatakse noppimisel, ei kopeeri see tasakaalustust saatelehe sisestamisel. Tasakaalustuskogus on sama, mis laokande oleku kogus tasakaalustuse käivitamisel (teisisõnu: *·*/*füüsiliselt* reserveeritud tellitud reserv või hilisem olek vastaval tellimusereal).

1. Logige tagasi varude nähtavuse rakendusse, **minge** konfiguratsioonilehele ja vaadake **seejärel** vahekaardilE Kerge reserveerimine üle vaikimisi nähtav reserveerimishierarhia. Lisage hierarhiasse uued dimensioonid vastavalt vajadusele.
1. Jaotises Seatud **kerge reserveerimise vastendamine** vaadake vaikesätteid. Vaikimisi salvestatakse reserveeritud varude kogused andmeallika `softreservephysical` füüsilise mõõtu suhtes `iv`. Reserveerimiseks *saadav* arvutatud mõõt on vastendatud väärtusega `availabletoreserve`. Kui soovite arvutatud mõõtu `availabletoreserve` värskendada, minge **konfiguratsioonilehele** ja seejärel **laiendage** ja muutke arvutatud mõõtu vahekaardil Arvutatud mõõt.

Lisateavet vt teemast [Inventory Visibility konfigureerimine](inventory-visibility-configuration.md).

> [!NOTE]
> Reserveerimishierarhia kirjeldab dimensioonide järjestust, mis tuleb reserveeringute tegemisel määratleda. See toimib samuti, nagu indeksi hierarhia töötaks vaba kaubavaru päringute puhul, kuid seda kasutatakse iseseisvalt, et kasutajad saaksid täpsemate reserveeringute määramiseks määrata dimensiooni üksikasju.
>
> Teie soft reservation hierarchy peaks sisaldama ja `SiteId` komponentidena `LocationId`, sest need konstruktoriks on varude nähtavuse sektsioonikonfiguratsioon.

Lisateavet reserveeringute konfigureerimise kohta vt teemast [Reserveermise konfiguratsioon](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Reserveerimise funktsiooni kasutamine Varude nähtavuses

Kui kutsute reserveerimise API, märgib süsteem määratud kaupade ja koguste reserveerimise.

Siin on näidestsenaarium ja API päringu näidiskogum. Ettevõte Contoso müüb toodet D0002 (valitsuskabinet) oma e-äri veebisaidilt. Klient asetab müügitellimuse väikesele punasele sahtlile veebisaidi kaudu. Contoso otsustab selle tellimuse täita järgmisi dimensioone kasutades:

- Organisatsiooni ID = usmf
- Sait = 1
- Ladu = 11
- Toode = D0002
- Värv = punane
- Suurus = väike

Contoso on juba oma e-ärisüsteemist seadistanud API ühenduse varude nähtavusega. Tellimuse saabumisel käivitab süsteem kohe API kutse lao nähtavuse liidesele kerge reserveerimise tegemiseks.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Loo reserveerimise API abil kerged reserveerimised

Reserveerimised tehakse Varude nähtavuse teenuses, esitades teenuse URL-ile nagu nt `/api/environment/{environmentId}/onhand/reserve` SISESTAMISE taotluse.

Reserveerimiseks peab taotluse sisu sisaldama organisatsiooni ID-d, toote ID-d, reserveeritud koguseid ja dimensioone.

Kui kutsute reserveerimise API, saate kontrollida reserveerimise kinnitamist, määrates `ifCheckAvailForReserv` kahendmuutuja parameetri taotluse kehas. Väärtus `True` tähendab, et kinnitamist nõutakse, samas kui väärtus `False` tähendab, et kinnitamist ei nõuta. Vaikeväärtus on `True`.

Kui soovite tühistada reserveeringu või määratud laokogused reserveerimata, määrake koguseks negatiivne väärtus ja seadke `ifCheckAvailForReserv` parameetrile kinnitus `False` vahele jätmiseks.

Siin on näide taotluse keha kohta, mis viitab müügitellimusele eelmises kontekstis.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Edukas pehme reserveerimistaotlus tagastab igale *reserveerimise kirjele kerge reserveerimise ID*. Kerge reserveerimise ID pole üksikule kerge reserveerimise kirjele kordumatu ID, vaid kerge reserveerimise taotlusega seostatud toote ID ja dimensiooniväärtuste kombinatsioon. Kui sünkroonite edukalt reserveeritud tellimused tarneahela haldusega või teise ERP-süsteemiga tasakaalustamiseks, saate tellimuse reale salvestada ka kerge reserveerimise ID.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a> Tasakaalusta kerged reserveerimised tarneahela haldamises

Saate tasakaalustada ajutiselt reserveeritud koguse pärast tellimusel oleva koguse füüsilist mahaarvamist tarneahela halduses või teises ERP süsteemis. Varude nähtavuse pakkumise boksist väljas reserveerimise tasakaalustav integratsioon tarneahela haldusega.

Järgige neid samme kerge reserveerimise tasakaalustamiseks.

1. Logige sisse rakendusse Supply Chain Management.
1. Avage müügi **- ja turunduse \> müügitellimused \> kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Looge väline müügitellimus uuesti ja lisage müügirida, mis kasutab täpselt sama toote ID- ja organisatsiooni-, lao-, lao- ja dimensiooniväärtusi.
1. **Valige müügitellimuse ridade kiirkaardil** äsja sisestatud müügirida ja seejärel valige tööriistaribal Varude reserveerimise **\> ID**.
1. Järgige üht neist sammudest.

    - Kopeerige soft reservation ID oma tarkvara reserveerimise taotluse vastusesse ja kleepige see reserveerimise **ID väljale**.
    - Jätke väli **Reserveeringu ID** tühjaks, kuid märkige ruut **Laoteenuse automaatne vastaskonto**. Süsteem määrab kauba ID ja valitud reale sisestatud dimensiooniväärtuste põhjal automaatselt tasakaalustavad toote- ja tootedimensioonid.

1. Valige nupp **OK**.
1. Kui sama müügirida on endiselt valitud, reserveerige **\>** **tellitud kogus füüsiliselt, valides tööriistaribal Müügitellimuse read kiirkaardi laoreserveeringu.**
1. Kui olete eelnevalt määranud välja **Reserveerimise tasakaalustuse modifikaatori** *väärtuseks* Reserveeritud *, käivitub vastaskonto, kui tellimuse rea olek on Füüsiliselt* reserveeri või Reserveeri *tellitud*. Pakett-töö käitatakse korra minuti jooksul tasakaalustustaotluste sünkroonimiseks tarneahela haldusest varude nähtavusse.

> [!NOTE]
> Kande olekute puhul, mis hõlmavad määratud reservi vastaskonto muutrit, tasakaalustab kande uuendus vastava reserveerimiskirje, kui kõik järgmised tingimused on täidetud:
>
> - Laokande reserveeringu ID vastab varude nähtavuse reserveerimiskirje reserveerimis-ID-le.
> - Laokande dimensioonid vastavad varude nähtavuse reserveerimiskirje dimensioonidele.
> - Muudatused laokande olekus käivitavad reserveeringute nihked, kui laokande olek kajastab fakti, et tellimuse protsess on lõpetatud või vahele jäetud.

Tasakaalustuskogused järgivad laokoguseid, mis on määratud vastavatel laokannetel. Tasakaalustus jõustub ainult juhul, kui reserveeritud kogus jääb varude nähtavusse.

### <a name="cancel-or-revert-a-soft-reservation"></a>Soft-reserveerimise tühistamine või ennistus

Kui algse tellimuse rida tühistatakse või kustutatakse ja peate vastava esialgse reserveerimise tühistama, sisestage negatiivne kogus, mis sisaldab täpselt sama teavet teie API päringu kehas.
