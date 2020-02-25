---
title: Common Data Service’i üksused
description: Microsoft Dynamics 365 Human Resources kasutab teenust Common Data Service, et lubada laiendatavus ja integreerimise stsenaariumid.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008799"
---
# <a name="common-data-service-entities"></a>Common Data Service’i üksused

Microsoft Dynamics 365 Human Resources kasutab teenust Common Data Service, et lubada laiendatavus ja integreerimise stsenaariumid.

Teenuse Common Data Service kohta lisateabe saamiseks vt teemat [Mis on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Teenuses Common Data Service on saadaval järgmised rakenduse Human Resources üksused.

## <a name="benefit-entities"></a>Soodustuse üksused

**Soodustuse arvutamise sagedus**

| **Väljad**        | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------------|---------------|--------------|----------------|
| Kirjeldus       | Tekst          |              | X              |
| Sageduse juhtelement | Suvandikomplekt    | X            | X              |
| On muutmatu      | Kaks valikut   |              | X              |
| Nimi              | Tekst          | X            | X              |


**Soodustuse arvutamise määr**

| **Väljad**  | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------|---------------|--------------|----------------|
| Kirjeldus | Tekst          |              | X              |
| Nimi        | Tekst          | X            | X              |
| TierType    | Suvandikomplekt    | X            | X              |


**Soodustuse arvutamise määra üksikasjad**

| **Väljad**                             | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|----------------------------------------|----------------|--------------|----------------|
| Soodustuse arvutamise määra üksikasjade arv | Tekst           | X            | X              |
| Arvutamise määra ID                    | Otsing         | X            | X              |
| Lisamismeetod                    | Suvandikomplekt     | X            | X              |
| Jõustunud                              | Ainult kuupäev      | X            | X              |
| Tööandja panus                  | Kümnendarv |              | X              |
| Aegumine                             | Ainult kuupäev      | X            | X              |
| WorkerDeduction                        | Kümnendarv |              | X              |


**Soodustuse tüüp**

| **Väljad**           | **Andmetüüp** | **Nõutav** | **Otsitav** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Suvandikomplekt    |              | X              |
| Kirjeldus          | Tekst          |              | X              |
| Nimi                 | Tekst          | X            | X              |
| PayrollCategory      | Suvandikomplekt    |              | X              |


**Soodustusplaan**

| **Väljad**                               | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|------------------------------------------|----------------|--------------|----------------|
| Võlgnevuse limiidi meetod                      | Suvandikomplekt     |              | X              |
| Hüvitise liik                             | Otsing         | X            | X              |
| Panuse limiidi meetod                | Suvandikomplekt     |              | X              |
| Lisamismeetod                      | Suvandikomplekt     |              | X              |
| Valuuta                                 | Otsing         |              | X              |
| Mahaarvamise prioriteet                       | Täisarv   |              | X              |
| Lisamise piirmäära vaikesumma        | Valuuta       |              | X              |
| Lisamise vaikelimiidi summa (baas) | Valuuta       |              | X              |
| Lisamise piirmäära vaikeperiood        | Suvandikomplekt     |              | X              |
| Mahaarvamiste piirmäära vaikesumma           | Valuuta       |              | X              |
| Mahaarvamise vaikelimiidi summa (baas)    | Valuuta       |              | X              |
| Mahaarvamiste piirmäära vaikeperiood           | Suvandikomplekt     |              | X              |
| Kirjeldus                              | Tekst           |              | X              |
| Vahetuskurss                            | Kümnendarv |              | X              |
| On täiendav palgaarvestuskäitus                | Kaks valikut    |              | X              |
| Taskukohase ravikindlustuse eelnõule on esitatav        | Kaks valikut    |              | X              |
| On loodud võlgnevusega                      | Kaks valikut    |              | X              |
| On brutosumma                              | Kaks valikut    |              | X              |
| On esmane                               | Kaks valikut    |              | X              |
| Nimi                                     | Tekst           | X            | X              |
| Palga mõju                           | Suvandikomplekt     |              | X              |
| Pensioni tüüp                          | Suvand määratud     |              | X              |


**Tööhõive üksus**

| **Väljad**                     | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|--------------------------------|----------------|--------------|----------------|
| Korrigeeritud töötaja tööhõive alguskuupäev     | Kuupäev ja kellaaeg  |              | X              |
| Ettevõte                        | Otsing         | X            | X              |
| Tööandja teatise summa ühik | Kümnendarv |              | X              |
| Töövõtja teatise ühik        | Suvandikomplekt     |              | X              |
| Tööhõive lõpukuupäev            | Kuupäev ja kellaaeg  |              | X              |
| Tööhõive arv              | Tekst           | X            | X              |
| Töösuhte alguskuupäev          | Kuupäev ja kellaaeg  |              | X              |
| Viimane töötamise kuupäev              | Kuupäev ja kellaaeg  |              | X              |
| Siirde kuupäev                | Kuupäev ja kellaaeg  |              | X              |
| Kehtivuse algus                     | Kuupäev ja kellaaeg  | X            | X              |
| Kehtiv kuni                       | Kuupäev ja kellaaeg  |              | X              |
| Töötaja                         | Otsing         | X            | X              |
| Töötaja teatise summa           | Kümnendarv |              | X              |
| Töötaja tööhõive alguskuupäev             | Kuupäev ja kellaaeg  |              | X              |
| Töötaja tüüp                    | Suvandikomplekt     | X            | X              |
| Töötaja teatise ühik          | Suvandikomplekt     |              | X              |

## <a name="worker-entities"></a>Töötaja üksused

**Etniline päritolu**

| **Väljad**         | **Andmetüüp** | **Nõutav** | **Otsitav** |
|--------------------|---------------|--------------|----------------|
| Kirjeldus        | Tekst          |              | X              |
| Etnilise päritolu nimi | Tekst          | X            | X              |


**Keel**

| **Väljad**    | **Andmetüüp** | **Nõutav** | **Otsitav** |
|---------------|---------------|--------------|----------------|
| Kirjeldus   | Tekst          |              | X              |
| Keele nimi | Tekst          | X            | X              |


**Veterani staatus**

| **Väljad**           | **Andmetüüp** | **Nõutav** | **Otsitav** |
|----------------------|---------------|--------------|----------------|
| Kirjeldus          | Tekst          |              | X              |
| On kaitstud veteran | Kaks valikut    |              | X              |
| Keele nimi        | Tekst          | X            | X              |


**Töötaja**

| **Väljad**                | **Andmetüüp** | **Nõutav** | **Otsitav** |
|---------------------------|---------------|--------------|----------------|
| Sünnikuupäev                 | Ainult kuupäev     |              | X              |
| Kirjeldus               | Tekst          |              | X              |
| 1. meiliaadress           | Meilisõnum         |              | X              |
| 2. meiliaadress           | Meilisõnum         |              | X              |
| Facebooki kasutaja         | Tekst          |              | X              |
| Eesnimi                | Tekst          |              | X              |
| Täisnimi                 | Tekst          |              | X              |
| Sugu                    | Suvandikomplekt    |              | X              |
| Loomine                | Tekst          |              | X              |
| Meilikontakt on lubatud  | Kaks valikut   |              | X              |
| Telefonikontakt on lubatud  | Kaks valikut   |              | X              |
| Perekonnanimi                 | Tekst          |              | X              |
| LinkedIni kasutaja         | Tekst          |              | X              |
| Haldur                   | Otsing        |              | X              |
| Teine eesnimi               | Tekst          |              | X              |
| Mobiiltelefon              | Telefon         |              | X              |
| Office Graphi identifikaator   | Tekst          |              | X              |
| Esmane meiliaadress     | Meilisõnum         |              | X              |
| Esmane telefon         | Telefon         |              | X              |
| Elukutse                | Tekst          |              | X              |
| 1. suhtlusvõrk          | Suvandikomplekt    |              | X              |
| 2. suhtlusvõrk          | Suvandikomplekt    |              | X              |
| Suhtlusvõrgu kasutaja 1 | Tekst          |              | X              |
| Suhtlusvõrgu kasutaja 2 | Tekst          |              | X              |
| Lähtekoht                    | Suvandikomplekt    | X            | X              |
| Olek                    | Suvandikomplekt    | X            | X              |
| Telefon 1               | Telefon         |              | X              |
| Telefon 2               | Telefon         |              | X              |
| Telefon 3               | Telefon         |              | X              |
| Twitteri identiteet          | Tekst          |              | X              |
| Kasutaja                      | Otsing        |              | X              |
| Veebisaidi URL               | URL           |              | X              |
| Töötaja number             | Tekst          | X            | X              |
| Töötaja tüüp               | Suvandikomplekt    | X            | X              |
| Yomi eesnimi           | Tekst          |              | X              |
| Yomi täisnimi            | Tekst          |              | X              |
| Yomi perekonnanimi            | Tekst          |              | X              |
| Yomi teine eesnimi          | Tekst          |              | X              |


**Töötaja aadress**

| **Väljad**           | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|----------------------|----------------|--------------|----------------|
| Majanumber       | Tekst           | X            | X              |
| Aadressi tüüp         | Suvandikomplekt     | X            | X              |
| Linn                 | Tekst           |              | X              |
| Riik või regioon    | Tekst           |              | X              |
| Riik               | Tekst           |              | X              |
| Faks                  | Telefon          |              | X              |
| On eelistatud         | Kaks valikut    |              | X              |
| Laiuskraad             | Kümnendarv |              | X              |
| 1. rida               | Tekst           |              | X              |
| 2. rida               | Tekst           |              | X              |
| 3. rida               | Tekst           |              | X              |
| Pikkuskraad            | Kümnendarv |              | X              |
| Sihtnumber          | Tekst           |              | X              |
| Postkast      | Tekst           |              | X              |
| Tarneviisi kood | Täisarv   |              | X              |
| Osariik või provints    | Tekst           |              | X              |
| Telefon 1          | Telefon          |              | X              |
| Telefon 2          | Telefon          |              | X              |
| Telefon 3          | Telefon          |              | X              |
| UPS-i tsoon             | Tekst           |              | X              |
| UTC tasakaalustus           | Täisarv   |              | X              |
| Töötaja               | Otsing         | X            | X              |


**Töötaja isikuteave**

| Väljad                             | Andmetüüp    | Nõutav | Otsitav |
|------------------------------------|--------------|----------|------------|
| Sünnilinn                         | Tekst         |          | X          |
| Sünniriik või -regioon            | Suvandikomplekt   |          | X          |
| Sünnikuupäev                          | Ainult kuupäev    |          | X          |
| Kodakondsuse riik või regioon      | Suvandikomplekt   |          | X          |
| Surmakuupäev                      | Ainult kuupäev    |          | X          |
| Invaliidistunud veterani kinnitamise kuupäev | Ainult kuupäev    |          | X          |
| Haridus                          | Tekst         |          | X          |
| Etniline päritolu                     | Otsing       |          | X          |
| ExpatriateEndDate                  | Ainult kuupäev    |          | X          |
| ExpatriateStartDate                | Ainult kuupäev    |          | X          |
| Isa sünniriik või regioon     | Suvandikomplekt   |          | X          |
| Sugu                             | Suvandikomplekt   |          | X          |
| On keelatud                        | Kaks valikut  |          | X          |
| On invaliidistunud veteran                | Kaks valikut  |          | X          |
| Välislähetuse reegel on rakendatav    | Kaks valikut  |          | X          |
| On täiskohaga õpilane               | Kaks valikut  |          | X          |
| Perekonnaseis                     | Suvandikomplekt   |          | X          |
| Sõjaväeteenistuse lõpukuupäev          | Ainult kuupäev    |          | X          |
| Sõjaväeteenistuse alguskuupäev        | Ainult kuupäev    |          | X          |
| Ema sünniriik või regioon     | Suvandikomplekt   |          | X          |
| Kodakondsuse riik või regioon      | Suvandikomplekt   |          | X          |
| Emakeel                    | Otsing       |          | X          |
| Ülalpeetavate arv               | Täisarv |          |            |
| Veterani staatus                     | Otsing       |          | X          |
| Töötaja                             | Otsing       | X        | X          |
| Töötaja isiklike andmete arv      | Tekst         | X        | X          |


**Töötaja pangakonto**

| **Väljad**                 | **Andmetüüp** | **Nõutav** | **Otsitav** |
|----------------------------|---------------|--------------|----------------|
| Kontoomanik             | Tekst          |              | X              |
| Konto ID     | Tekst          |              | X              |
| Aadressi kirjeldus        | Tekst          |              | X              |
| Pangakonto tüüp          | Suvandikomplekt    |              | X              |
| Panga asukoha kood         | Tekst          |              | X              |
| Haru nimi                | Tekst          |              | X              |
| Haru kood              | Tekst          |              | X              |
| Linn                       | Tekst          |              | X              |
| Riik või regioon          | Tekst          |              | X              |
| Riik                     | Tekst          |              | X              |
| Kirjeldus                | Tekst          |              | X              |
| Piirkonna nimi              | Tekst          |              | X              |
| Meilisõnum                      | Tekst          |              | X              |
| Laiendus                  | Tekst          |              | X              |
| Faks                        | Tekst          |              | X              |
| IBAN                       | Tekst          |              | X              |
| 1. rida                     | Tekst          |              | X              |
| 2. rida                     | Tekst          |              | X              |
| 3. rida                     | Tekst          |              | X              |
| Mobiiltelefon               | Tekst          |              | X              |
| Inimese nimi             | Tekst          |              | X              |
| Sihtnumber                | Tekst          |              | X              |
| Postkast            | Tekst          |              |                |
| Protsessikood             | Tekst          |              | X              |
| Protsessikoodi tüüp        | Suvandikomplekt    |              | X              |
| Osariik või provints          | Tekst          |              | X              |
| SWIFT-kood                 | Tekst          |              | X              |
| Telefon                  | Tekst          |              | X              |
| Teleksinumber               | Tekst          |              | X              |
| Veebisaidi URL                | Tekst          |              | X              |
| Töötaja                     | Otsing        | X            | X              |
| Töötaja pangakonto number | Tekst          |              | X              |
| Töötaja pangakonto number | Tekst          | X            | X              |

**Töötaja põhipalk**

| Väljad                                | Andmetüüp      | Nõutav | Otsitav |
|---------------------------------------|----------------|----------|------------|
| Ettevõte                               | Otsing         | X        | X          |
| Hüvitise tüüp                     | Suvandikomplekt     |          | X          |
| Valuuta                              | Otsing         |          | X          |
| Kehtivuse alguskuupäev                        | Ainult kuupäev      |          | X          |
| Sündmus                                 | Otsing         | X        | X          |
| Vahetuskurss                         | Kümnendarv |          | X          |
| Aegumiskuupäev                       | Ainult kuupäev      |          | X          |
| Rea number                           | Kümnendarv |          | X          |
| Tasusagedus                         | Otsing         | X        | X          |
| Tasumäär                              | Valuuta       |          | X          |
| Tasumäär (baas)                       | Valuuta       |          | X          |
| Plaan                                  | Otsing         | X        | X          |
| Ametikoht                              | Otsing         | X        | X          |
| Protsessi tüüp                          | Suvandikomplekt     | X        | X          |
| Viitepunkti seadistusrida            | Otsing         |          | X          |
| Töötaja                                | Otsing         | X        | X          |
| Töötaja põhipalga number      | Tekst           | X        | X          |

**Töötaja isiku ID-number**

| Väljad                 | Andmetüüp   | Nõutav | Otsitav |
|------------------------|-------------|----------|------------|
| Kirjeldus            | Tekst        |          | X          |
| Kirje tüüp             | Tekst        |          | X          |
| Aegumiskuupäev        | Ainult kuupäev   |          | X          |
| ID-number  | Tekst        | X        | X          |
| ID tüüp    | Otsing      | X        | X          |
| On esmane             | Kaks valikut |          | X          |
| Väljastamise kuupäev             | Ainult kuupäev   |          | X          |
| Väljastav asutus         | Otsing      | X        | X          |
| Töötaja                 | Otsing      | X        | X          |


## <a name="position-entities"></a>Ametikoha üksused

**Ametikoht**

| **Väljad**               | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|--------------------------|----------------|--------------|----------------|
| Aktiveerimine               | Kuupäev ja kellaaeg  |              | X              |
| Määramiseks saadaval | Kuupäev ja kellaaeg  |              | X              |
| Osakond               | Otsing         |              | X              |
| Kirjeldus              | Tekst           |              | X              |
| Täistööaja vaste     | Kümnendarv |              | X              |
| Amet                      | Otsing         | X            | X              |
| Ametikoha number      | Tekst           | X            | X              |
| Peamine ametikoht      | Otsing         |              | X              |
| Ametikoha tüüp            | Otsing         |              | X              |
| Pensionile jäämine               | Kuupäev ja kellaaeg  |              | X              |
| Amet                    | Suvandikomplekt     |              | X              |
| Kehtivuse algus               | Kuupäev ja kellaaeg  | X            | X              |
| Kehtiv kuni                 | Kuupäev ja kellaaeg  |              | X              |


**Positsiooni tüüp**

| **Väljad**         | **Andmetüüp** | **Nõutav** | **Otsitav** |
|--------------------|---------------|--------------|----------------|
| Klassifikatsioon     | Suvandikomplekt    |              | X              |
| Kirjeldus        | Tekst          |              | X              |
| Ametikoha tüübi nimi | Tekst          | X            | X              |


**Ametikoha töötaja määramine**

| **Väljad**                        | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------------------------|---------------|--------------|----------------|
| Ametikoht                      | Otsing        | X            | X              |
| Ametikoha töötaja määramise number | Tekst          | X            | X              |
| Kehtivuse algus                        | Tekst          | X            | X              |
| Kehtiv kuni                          |               |              | X              |
| Töötaja                            |               | X            | X              |

## <a name="job-entities"></a>Töö üksused

**Töö**

| **Väljad**                   | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|------------------------------|----------------|--------------|----------------|
| Luba piiramatud ametikohad    | Kaks valikut    |              | X              |
| Vaikimisi täistööaja vaste | Kümnendarv |              | X              |
| Kirjeldus                  | Tekst           |              | X              |
| Töö kirjeldus              | Tekst           |              | X              |
| Tööfunktsioon                 | Otsing         |              | X              |
| Töö tüüp                     | Otsing         |              | X              |
| Ametikohtade maksimaalne arv  | Täisarv   |              | X              |
| Nimi                         | Tekst           | X            | X              |
| Amet                        | Suvandikomplekt     |              | X              |
| Kehtivuse algus                   | Kuupäev ja kellaaeg  | X            | X              |
| Kehtiv kuni                     | Kuupäev ja kellaaeg  |              | X              |


**Tööfunktsioon**

| **Väljad**        | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------------|---------------|--------------|----------------|
| Kirjeldus       | Tekst          | X            | X              |
| Tööfunktsiooni nimi | Tekst          | X            | X              |


**Töö tüüp**

| **Väljad**    | **Andmetüüp** | **Nõutav** | **Otsitav** |
|---------------|---------------|--------------|----------------|
| Kirjeldus   | Tekst          | X            | X              |
| Vabastuse olek | Suvandikomplekt    | X            | X              |
| Töö tüübi nimi | Tekst          | X            | X              |

## <a name="leave-and-absence-entities"></a>Puhkuste ja puudumiste üksused

**Puhkuse registreerimine**

| **Väljad**            | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------------|---------------|--------------|----------------|
| Lisandumise kuupäeva alus    | Ainult kuupäev     | X            | X              |
| Lisandumise alguskuupäev    | Ainult kuupäev     | X            | X              |
| Kohandatud kuupäev           | Ainult kuupäev     | X            | X              |
| Lisandumine on peatatud  | Kaks valikut   |              | X              |
| LeaveEnrollmentNumber | Tekst          | X            | X              |
| Puhkuseplaan            | Otsing        | X            | X              |
| Alguskuupäev            | Ainult kuupäev     | X            | X              |
| Taseme alus            | Suvandikomplekt    | X            | X              |
| Töötaja                | Otsing        | X            | X              |


**Puhkuse pangakanne**

| **Väljad**                    | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|-------------------------------|----------------|--------------|----------------|
| Summa                        | Kümnendarv | X            | X              |
| Ettevõte                       | Otsing         | X            | X              |
| Puhkuse pangakande number | Tekst           | X            | X              |
| Puhkuseplaan                    | Otsing         |              | X              |
| Puhkuse tüüp                    | Otsing         | X            | X              |
| Kande kuupäev              | Ainult kuupäev      | X            | X              |
| Kande number            | Kümnendarv | X            | X              |
| Kande tüüp              | Suvandikomplekt     | X            | X              |
| Töötaja                        | Otsing         | X            | X              |


**Puhkuseplaan**

| **Väljad**        | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------------|---------------|--------------|----------------|
| Lisandumissagedus | Suvandikomplekt    | X            | X              |
| Ettevõte           | Otsing        | X            | X              |
| Kirjeldus       | Tekst          |              | X              |
| Puhkuse tüüp        | Otsing        | X            | X              |
| Nimi              | Tekst          | X            | X              |
| Alguskuupäev        | Ainult kuupäev     | X            | X              |


**Puhkusetaotlus**

| **Väljad**           | **Andmetüüp** | **Nõutav** | **Otsitav** |
|----------------------|---------------|--------------|----------------|
| Kommentaar              | Tekst          | X            | X              |
| Ettevõte              | Otsing        | X            | X              |
| Puhkusetaotluse number | Tekst          |              | X              |
| Nõude kuupäev         | Kuupäev ja kellaaeg | X            | X              |
| Olek               | Suvandikomplekt    | X            | X              |
| Töötaja               | Otsing        | X            | X              |


**Puhkusetaotluse üksikasjad**

| **Väljad**                  | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|-----------------------------|----------------|--------------|----------------|
| Summa                      | Kümnendarv | X            | X              |
| Puhkuse kuupäev                  | Kuupäev ja kellaaeg  | X            | X              |
| Puhkusetaotlus               | Otsing         | X            | X              |
| Puhkusetaotluse üksikasjade number | Tekst           | X            | X              |
| Puhkuse tüüp                  | Otsing         | X            | X              |


**Puhkuse tüüp**

| **Väljad**      | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------|---------------|--------------|----------------|
| Ettevõte         | Otsing        | X            | X              |
| Kirjeldus     | Tekst          |              | X              |
| Tulukood    | Otsing        |              | X              |
| Puhkuse tüübi nimi | Tekst          | X            | X              |


**Tööaja kalender**

| **Väljad**  | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------|---------------|--------------|----------------|
| Ettevõte     | Otsing        | X            | X              |
| Kirjeldus | Tekst          |              | X              |
| Nimi        | Tekst          | X            | X              |


**Töökalendri päev**

| **Väljad**               | **Andmetüüp** | **Nõutav** | **Otsitav** |
|--------------------------|---------------|--------------|----------------|
| Kalendri kuupäev            | Ainult kuupäev     | X            | X              |
| Ettevõte                  | Otsing        |              | X              |
| Olek                   | Tekst          |              | X              |
| Töökalender            | Otsing        | X            | X              |
| Töökalendri päeva number | Tekst          | X            | X              |


**Töökalendri püha**

| **Väljad**  | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------|---------------|--------------|----------------|
| Nimi        | Tekst          |              | X              |
| Kirjeldus | Tekst          | X            | X              |


**Töökalendri puhkuse rida**

| **Väljad**                        | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------------------------|---------------|--------------|----------------|
| Püha kuupäev                      | Ainult kuupäev     | X            | X              |
| Nimi                              | Tekst          |              | X              |
| Töökalendri püha             | Otsing        | X            | X              |
| Töökalendri puhkuse rea number | Tekst          | X            | X              |


**Töökalendri ajaintervall**

| **Väljad**                         | **Andmetüüp** | **Nõutav** | **Otsitav** |
|------------------------------------|---------------|--------------|----------------|
| Ettevõte                            | Otsing        |              | X              |
| Lõppaeg                           | Täisarv  |              | X              |
| Algusaeg                         | Täisarv  |              | X              |
| Töökalender                      | Otsing        | X            | X              |
| Töökalendri päev                  | Otsing        | X            | X              |
| Töökalendri ajaintervalli number | Tekst          | X            | X              |

## <a name="organization-entities"></a>Organisatsiooni üksused

**Ettevõte**

| **Väljad**   | **Andmetüüp** | **Nõutav** | **Otsitav** |
|--------------|---------------|--------------|----------------|
| Ettevõtte kood | Tekst          | X            | X              |
| Nimi         | Tekst          | X            | X              |


**Osakond**

| **Väljad**        | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------------|---------------|--------------|----------------|
| Osakonna number | Tekst          | X            | X              |
| Kirjeldus       | Tekst          |              | X              |
| Nimi              | Tekst          | X            | X              |
| Emaosakond | Otsing        |              | X              |


**Valuuta**

| **Väljad**         | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|--------------------|----------------|--------------|----------------|
| Valuutakood      | Tekst           | X            | X              |
| Valuuta nimi      | Tekst           | X            | X              |
| Valuuta täpsus | Täisarv   | X            | X              |
| Valuuta sümbol    | Tekst           | X            | X              |
| Üksuse pilt       | Pilt          |              |                |
| Vahetuskurss      | Kümnendarv | X            | X              |
| Organisatsioon       | Otsing         | X            | X              |
| Olek             | Suvandikomplekt     |              | X              |

## <a name="payroll-entities"></a>Palgaolemid

**Palgatsükkel**

| **Väljad**  | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------|---------------|--------------|----------------|
| Kirjeldus | Tekst          | X            | X              |
| Sagedus   | Suvandikomplekt    | X            | X              |
| Nimi        | Tekst          | X            | X              |


**Makseperiood**

| **Väljad**           | **Andmetüüp** | **Nõutav** | **Otsitav** |
|----------------------|---------------|--------------|----------------|
| Makse vaikekuupäev | Ainult kuupäev     |              | X              |
| Kirjeldus          | Tekst          |              | X              |
| Palgatsükkel            | Otsing          | X            | X              |
| Maksuperioodi number    | Tekst          | X            | X              |
| Perioodi lõpukuupäev      | Ainult kuupäev     | X            | X              |
| Perioodi alguskuupäev    | Ainult kuupäev     | X            | X              |
| Olek               | Suvandikomplekt    |              | X              |


**Palga tulukood**

| **Väljad**              | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------------------|---------------|--------------|----------------|
| Kirjeldus             | Tekst          | X            | X              |
| Kaasa maksetüübis | Suvandikomplekt    | X            | X              |
| On produktiivne           | Kaks valikut   | X            | X              |
| Nimi                    | Tekst          |              | X              |
| Koguse ühik           | Suvandikomplekt    |              | X              |
| FMLA tundide jälgimine        | Kaks valikut   |              | X              |


**Maksuregioon**

| **Väljad**        | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------------|---------------|--------------|----------------|
| Linn              | Tekst          |              | X              |
| Riik või regioon | Tekst          |              | X              |
| Riik            | Tekst          |              | X              |
| Nimi              | Tekst          | X            | X              |
| Osariik või provints | Tekst          |              | X              |


**Soodustuse arvutamise sageduse makseperiood**

| **Väljad**                                      | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-------------------------------------------------|---------------|--------------|----------------|
| Soodustuse arvutamise sagedus                   | Otsing        | X            | X              |
| Soodustuse arvutamise sageduse makseperioodi number | Tekst          | X            | X              |
| Makseperiood                                      | Otsing        | X            | X              |


**Pangakonto väljamakse**

| **Väljad**                       | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|----------------------------------|----------------|--------------|----------------|
| Summa                           | Valuuta       |              | X              |
| Summa (baas)                    | Valuuta       |              | X              |
| Pangakonto                     | Otsing         | X            | X              |
| Pangakonto väljamakse number | Tekst           | X            | X              |
| Ettevõte                          | Otsing         | X            | X              |
| Valuuta                         | Otsing         |              | X              |
| Vahetuskurss                    | Kümnendarv |              | X              |
| On jääk                     | Kaks valikut    |              | X              |
| Prioriteet                         | Täisarv   |              | X              |

**Isiku ID väljastanud asutus**

| **Väljad**           | **Andmetüüp** | **Nõutav** | **Otsitav** |
|----------------------|---------------|--------------|----------------|
| Aadressi kirjeldus  | Tekst          |              | X              |
| Aadressirida 1       | Tekst          |              | X              |
| Aadressirida 2       | Tekst          |              | X              |
| Aadressirida 3       | Tekst          |              | X              |
| Linn                 | Tekst          |              | X              |
| Riik või regioon    | Suvandikomplekt    |              | X              |
| Riik               | Tekst          |              | X              |
| Kirjeldus          | Tekst          |              | X              |
| Meilisõnum                | Tekst          |              | X              |
| Laiendus            | Tekst          |              | X              |
| Faks                  | Tekst          |              | X              |
| Väljaandva asutuse nimi  | Tekst          | X            | X              |
| Mobiiltelefon         | Tekst          |              | X              |
| Leht                 | Tekst          |              | X              |
| Sihtnumber          | Tekst          |              | X              |
| Postkast      | Tekst          |              | X              |
| SMS                  | Tekst          |              | X              |
| Osariik või provints    | Tekst          |              | X              |
| Telefon            | Tekst          |              | X              |
| Teleks                | Tekst          |              | X              |
| Veebisaidi URL          | Tekst          |              | X              |

**Töötaja isiku identifitseerimistüüp**

| **Väljad**                        | **Andmetüüp**  | **Nõutav** | **Otsitav** |
|-----------------------------------|----------------|--------------|----------------|
| Lubatud väärtused                    | Suvandikomplekt     |              | X              |
| Riik või regioon                 | Tekst           |              | X              |
| Kirjeldus                       | Tekst           |              | X              |
| Fikseeritud pikkus                      | Täisarv   |              | X              |
| ID-numbri vorming      | Tekst           |              | X              |
| Tüüp                              | Suvandikomplekt     |              | X              |
| Töötaja isiku identifitseerimistüüp | Tekst           | X            | X              |

## <a name="fixed-compensation-entities"></a>Põhipalga üksused

**Tasu fikseeritud plaan**

| **Väljad**                  | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------------------|---------------|--------------|----------------|
| Ettevõte                     | Otsing        | X            | X              |
| Kogupalga tabel           | Otsing        |              | X              |
| Valuuta                    | Otsing        | X            | X              |
| Kirjeldus                 | Tekst          | X            | X              |
| Kehtivuse alguskuupäev              | Ainult kuupäev     | X            | X              |
| Aegumiskuupäev             | Ainult kuupäev     | X            | X              |
| Palkamise reegel                   | Suvandikomplekt    | X            | X              |
| Nimi                        | Tekst          | X            | X              |
| Vahemikust väljajäämise tolerants      | Suvandikomplekt    | X            | X              |
| Tasusagedus               | Otsing        | X            | X              |
| Soovitamine lubatud      | Kaks valikut   | X            | X              |
| Viitepunkti rea seadistamine  | Otsing        |              | X              |
| Tüüp                        | Suvandikomplekt    | X            | X              |

**Hüvitise ruudustik**

| **Väljad**                  | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------------------|---------------|--------------|----------------|
| Ettevõte                     | Otsing        | X            | X              |
| Valuuta                    | Otsing        |              | X              |
| Kirjeldus                 | Tekst          | X            | X              |
| Kehtivuse alguskuupäev              | Ainult kuupäev     |              | X              |
| Aegumiskuupäev             | Ainult kuupäev     |              | X              |
| Nimi                        | Tekst          | X            | X              |
| Võrdluspunkti seadistus       | Otsing        | X            | X              |
| Tüüp                        | Suvandikomplekt    | X            | X              |

**Hüvituse tase**

| **Väljad**      | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------|---------------|--------------|----------------|
| Kirjeldus     | Tekst          |              | X              |
| Nimi            | Tekst          | X            | X              |
| Tüüp            | Suvandikomplekt     | X            | X              |

**Tasu tasusagedus**

| **Väljad**                  | **Andmetüüp**   | **Nõutav** | **Otsitav** |
|-----------------------------|-----------------|--------------|----------------|
| Aastane teisendustegur    | Kümnendarv  |              | X              |
| Ettevõte                     | Otsing          | X            | X              |
| Kirjeldus                 | Tekst            |              | X              |
| Tunnine teisendustegur    | Kümnendarv  |              | X              |
| Igakuine teisendustegur   | Kümnendarv  |              | X              |
| Nimi                        | Tekst            | X            | X              |
| Periood                      | Suvandikomplekt      |              | X              |
| Nädalane teisendustegur    | Suvandikomplekt      |              | X              |


**Palga koos lisatasudega võrdluspunkti seadistus**

| **Väljad**          | **Andmetüüp**   | **Nõutav** | **Otsitav** |
|---------------------|-----------------|--------------|----------------|
| Ettevõte             | Otsing          | X            | X              |
| Hüvitise tüüp   | Suvandikomplekt      | X            | X              |
| Kirjeldus         | Tekst            | X            | X              |
| Nimi                | Tekst            | X            | X              |

**Hüvituse võrdluspunkti seadistuse rida**

| **Väljad**            | **Andmetüüp**   | **Nõutav** | **Otsitav** |
|-----------------------|-----------------|--------------|----------------|
| Ettevõte               | Otsing          | X            | X              |
| Kirjeldus           | Tekst            | X            | X              |
| Rea number           | Kümnendarv  | X            | X              |
| Nimi                  | Tekst            | X            | X              |
| Võrdluspunkti seadistus | Otsing          | X            | X              |

**Hüvituspiirkond**

| **Väljad**      | **Andmetüüp** | **Nõutav** | **Otsitav** |
|-----------------|---------------|--------------|----------------|
| Kirjeldus     | Tekst          | X            | X              |
| Nimi            | Tekst          | X            | X              |

**Kompensatsiooni struktuur**

| **Väljad**                    | **Andmetüüp**   | **Nõutav** | **Otsitav** |
|-------------------------------|---------------  |--------------|----------------|
| Summa                        | Valuuta        |              | X              |
| Summa baas                   | Valuuta        |              | X              |
| Ettevõte                       | Otsing          | X            | X              |
| Hüvituse struktuuri number | Tekst            | X            | X              |
| Valuuta                      | Otsing          |              | X              |
| Vahetuskurss                 | Kümnendarv  |              | X              |
| Ruudustik                          | Otsing          | X            | X              |
| Tase                         | Otsing          | X            | X              |
| Viitepunkt               | Otsing          | X            | X              |
| Viitepunkti rea seadistamine    | Otsing          | X            | X              |

**Põhipalga sündmus**

| **Väljad**            | **Andmetüüp**   | **Nõutav** | **Otsitav** |
|-----------------------|-----------------|--------------|----------------|
| Ettevõte               | Otsing          | X            | X              |
| Kirjeldus           | Tekst            | X            | X              |
| Sündmuse tüüp            | Suvandikomplekt      | X            | X              |
| On aktiivne             | Kaks valikut     | X            |                |
| Nimi                  | Tekst            | X            | X              |

## <a name="entity-relationship-models"></a>Üksuse seose mudelid

### <a name="worker"></a>Töötaja
![Töötaja](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Töö ja ametikoht
![Töö ja ametikoht](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Soodustused
![Soodustused](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensatsioon
![Kompensatsioon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Lahkumine
![Lahkumine](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Töökalender
![Töökalender](./media/HCMCommon-work-calendar-entity-diagram.png)
