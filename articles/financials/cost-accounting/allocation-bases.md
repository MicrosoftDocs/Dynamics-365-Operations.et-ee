---
title: Eraldamise alused
description: Teema sisaldab teavet eraldamisaluste kohta. Eraldamisalused on kuluarvestuse põhikomponendid ja neid kasutatakse enamasti üldkulude eraldamiseks.
author: AndersGirke
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 92824cf0fb5ad361090d8dccfd64353d2c16317c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "311676"
---
# <a name="allocation-bases"></a>Eraldamise alused 

[!include [banner](../includes/banner.md)]

Eraldamisalus on alus, mille põhjal kuluarvestus üldkulusid eraldab. Eraldamisalus võib olla kogus, nt masina kasutatavad töötunnid, tarbitavad kilovatt-tunnid (kWh) või kasutatav pindala. Eraldamisaluseid kasutatakse enamasti üldkulude määramiseks toodetavatele varudele. Näiteks IT-osakond eraldab tunnid arvutite arvu järgi, mida iga osakond kasutab.

Kuluarvestuses on kolme tüüpi eraldamisaluseid.

- Eelmääratletud dimensiooniliikme eraldamisalused
- Hierarhia eraldamisalused
- Valemi eraldamisalused

## <a name="predefined-dimension-member-allocation-bases"></a>Eelmääratletud dimensiooniliikme eraldamisalused

Eelmääratletud dimensiooniliikme eraldamisalused luuakse automaatselt ühte järgmist tüüpi dimensiooniliikme loomisel.

- Statistilise dimensiooni liikmed
- Kuluelemendi dimensiooniliikmed

> [!NOTE]
> Eelmääratletud dimensiooniliikme eraldamisalused, mis põhinevad kuluelemendi dimensiooniliikmel, arvestavad ainult andmeallika pakkujalt (nt pearaamatust või eelarvest) pärinevaid väärtusi.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Näide 1: kuluelemendi dimensiooniliikme kasutamine eraldamisalusena
See on näide kulueraldamisreegli loomise kohta kuluelemendi 10002 (töötaja kindlustus) eraldamiseks saldole, mis on registreeritud kuluelemendil 10001 (palgad). Eraldamisreegel määratletakse iga osakonna palkade ja kõigi palkade suhtarvu põhjal. (Vajalik on ülevaatamine!)

Pearaamatus määratletakse kontoplaan järgmiselt.

| Kontoplaan | Põhikonto | Kirjeldus        | Põhikonto tüüp |
|------------------|--------------|--------------------|-------------------|
| Ühine           | 10001        | Palgad           | Kulu           |
| Ühine           | 10002        | Töötaja kindlustus | Kulu           |

Määratlege kuluelemendi dimensioon ja konfigureerige andmekonnektor. Pärast andmete importimist luuakse kuluarvestusse järgmised kirjed.

**Kuluelemendi dimensiooniliikmed**

| Kuluelemendi dimensiooni nimi | Kuluelement |  Kirjeldus       | Tüüp    |
|-----------------------------|--------------|--------------------|---------|
| Kuluelemendid               | 10001        | Palgad           | Esmane |
| Kuluelemendid               | 10002        | Töötaja kindlustus | Esmane |

**Eelmääratletud dimensiooniliikme eraldamisalused** 

| Nimi  | Kirjeldus        | Kuluelemendi dimensioon |
|-------|--------------------|------------------------|
| 10001 | Palgad           | Kuluelemendid          |
| 10002 | Töötaja kindlustus | Kuluelemendid          |

Pearaamatusse on sisestatud järgmised kirjed.

- Kirjed, mis näitavad palkade põhikontot, pärinevad palgasüsteemist ja need sisestatakse kulukeskustesse.
- Töötaja kindlustuse kulu sisestatakse käsitsi vaike-kulukeskusse.

| Aruandluskuupäev | Kulukeskus |  Kirjeldus        | Põhikonto |  Kirjeldus       | Summa arvestusvaluutas |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 03-01-2017      | CC001       | Personaliosakond                  | 10001        | Palgad           | 2000,00                      |
| 03-01-2017      | CC002       | FI                  | 10001        | Palgad           | 5000,00                      |
| 03-01-2017      | CC003       | LÜ                  | 10001        | Palgad           | 3000,00                      |
| 03-01-2017      | CC099       | Vaike-kulukeskus | 10002        | Töötaja kindlustus | 1 000,00                      |

Pärast pearaamatu lähteandmete töötlemist luuakse kuluarvestusse järgmised kirjed.

**Kulukirjed**

| Kuluobjekt |  Kirjeldus        | Kuluelement  |  Kirjeldus       | Kulukäitumine   |Summa|Aruandluskuupäev|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | Personaliosakond                  | 10001         | Palgad           | Liigitamata    |2000,00|  03-01-2017    |
| CC002       | FI                  | 10001         | Palgad           | Liigitamata    |5000,00|     03-01-2017         |
| CC003       | LÜ                  | 10001         | Palgad           | Liigitamata    |3000,00|      03-01-2017        |
| CC099       | Vaike-kulukeskus | 10002         | Töötaja kindlustus | Liigitamata    |1 000,00|      03-01-2017       |

Selles lihtsustatud näites luuakse kulueraldamisreegel kuluelemendi 10002 (töötaja kindlustus) eraldamiseks seoses saldoga, mis on registreeritud kuluelemendil 10001 (palgad).

**Kulu jaotuse reegel**

| Kuluobjekti dimensioonihierarhia sõlm | Kuluelemendi dimensioonihierarhia sõlm | Kulukäitumine | Eraldamise alus |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Liigitamata  | 10001           |

**Üldkulude arvutamine**

Pärast kuluelemendi 10001 (palgad) rakendamist eraldamisalusena on üldkulude arvutuse tulemus järgmine.

| Kuluobjekt | Kirjeldus | Väärtus |   Eraldamistegur         | Summa |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | Personaliosakond          | 2 000     | (2000 ÷ 10 000) × 1 000.00 | 200,00 |
| CC002       | FI          | 5 000     | (5000 ÷ 10 000) × 1000.00 | 500,00 |
| CC003       | LÜ          | 3 000     | (3000 ÷ 10 000) × 1000.00 | 300.00 |

**Tööleht**

| Tööleht | Töölehe tüüp                          | Rahanduskalendri periood | Aasta | Periood   | Versioon                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Kulujaotuse arvutamise tööleht | Fiskaalne                 | 2017 | Periood 1 | Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood |

**Kuluobjekti saldo töölehe sisestused**

| Aruandluskuupäev | Kuluobjekt | Kirjeldus         | Kuluelement | Kirjeldus        | Kulukäitumine |  Summa  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31-01-2017      | CC099       | Vaike-kulukeskus | 10002        | Töötaja kindlustus | Liigitamata  | 1 000,00 |

**Kulukirjed**

| Kuluobjekt |  Kirjeldus        | Kuluelement |    Kirjeldus     | Kulukäitumine | Summa    | Aruandluskuupäev |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Vaike-kulukeskus | 10002        | Töötaja kindlustus | Liigitamata  | –1000,00 | 31-01-2017      |
| CC001       | Personaliosakond                  | 10002        | Töötaja kindlustus | Liigitamata  | 200,00    | 31-01-2017      |
| CC002       | FI                  | 10002        | Töötaja kindlustus | Liigitamata  | 500,00    | 31-01-2017      |
| CC099       | LÜ                  | 10002        | Töötaja kindlustus | Liigitamata  | 300.00    | 31-01-2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Näide 2: statistilise dimensiooni liikme kasutamine eraldamisalusena

Statistilise dimensiooni liikmeid saab kasutada eraldamisalusena poliitikate määratlemiseks või mitterahalise tarbimise registreerimiseks kuluobjektide järgi. Statistilise dimensiooni liikmeid saab luua käsitsi või importida neid failist, kasutades andmehalduse importi-/eksporditööriista.

**Statistilise dimensiooni liikmed**

| Statistilise dimensiooni nimi | Statistiline element | Kirjeldus               | Üksus |
|----------------------------|---------------------|---------------------------|------|
| Statistilised elemendid       | TTE                 | Täiskohaga töötajad       | Ea   |
| Statistilised elemendid       | Elektrienergia         | Elektri tarbimine   | kWh  |

Kui statistilise dimensiooni liige salvestatakse, luuakse eelmääratud dimensiooniliikmete eraldamisalustes vastav kirje.

**Eelmääratletud dimensiooniliikme eraldamisalused**

| Nimi        | Kirjeldus             | Statistilise elemendi dimensioon |
|-------------|-------------------------|-------------------------------|
| TTE         | Täiskohaga töötajad     | Statistilised elemendid          |
| Elektrienergia | Elektri tarbimine | Statistilised elemendid          |

Statistilised mõõdud võivad pärineda erinevatest allikatest.

- Elektritarbimist saab mõõta mõõteseadmetega, mis on paigaldatud ettevõtte erinevatesse piirkondadesse.
- Tabelites on statistilised mõõdud. Näiteks tabelis HcmEmployment on nimekiri kõikidest töötajatest ja kulukeskustest, milles nad töötavad.

| Nimi       | Kulukeskus |  Kirjeldus  | Töötaja tüüp |
|------------|-------------|----|-------------|
| Töötaja A | CC001       | Personaliosakond | Töötaja    |
| Töötaja B | CC002       | FI | Töötaja    |
| Töötaja C | CC002       | FI | Töötaja    |
| Töötaja D | CC003       | LÜ | Töötaja    |
| Töötaja F | CC003       | LÜ | Töötaja    |

> [!NOTE]
> Kõiki tabeleid, mis sisaldavad finantsdimensioone, saab kasutada statistiliste mõõtude allikana.

Kuluarvestus toetab statistiliste mõõtude kogumit, kasutades järgmisi andmeühendusi.

- Andmehalduse importimis-/eksportimistööriist
- Statistilised mõõdud

Statistiliste mõõtude toomiseks süsteemist on vajalik statistiliste mõõtude pakkuja mall. Lisateavet leiate teemast Statistiliste mõõtude pakkuja mall. (Kui see teema on kirjutatud, lisatakse link.)

**Statistiliste mõõtude pakkuja mallid**

| Nimi  | Funktsioon | Lähtetabel  | Summa väli      | Kuupäevaväli     |
|-------|----------|---------------|----------------|----------------|
| TTE-d | Loendus    | HcmEmployment | Pole kohaldatav | Pole kohaldatav |

Pärast statistilise mõõdu lähteandmete töötlemist luuakse kuluarvestusse järgmised kirjed.

**Statistilised kirjed**

| Kuluobjekt | Kirjeldus      | Aruandluskuupäev | Statistilise dimensiooni liige | Kirjeldus         | Väärtus |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personaliosakond               | 31-01-2017      | TTE-d                        | Täiskohaga töötajad | 1,00      |
| CC002       | FI               | 31-01-2017      | TTE-d                        | Täiskohaga töötajad | 2.00      |
| CC003       | LÜ               | 31-01-2017      | TTE-d                        | Täiskohaga töötajad | 2.00      |

Siin on näide kulu jaotusreeglist, kui TTE eelmääratud dimensiooniliikme eraldamisalus on määratud selles eraldamisaluseks.

| Kuluobjekt | Kirjeldus  | Väärtus | Eraldamistegur |
|-------------|------|-----------|-------------------|
| CC001       | Personaliosakond   | 1,00      | (1/5) × summa    |
| CC002       | FI   | 2.00      | (2/5) × summa    |
| CC003       | LÜ   | 2.00      | (2/5) × summa    |

Imporditud statistiliste mõõtude andmeüksust saab kasutada statistiliste mõõtude importimiseks kuluarvestusse. Kasutada saab ka andmehalduse impordi-/eksporditööriista. Excelis registreeritakse elektritarbimine järgmiselt.

| Aruandluskuupäev | Dimensiooniliige | Väärtus | Lähteidentifikaator |
|-----------------|------------------|-----------|-------------------|
| 31-01-2017      | CC001            | 2,450.00  | Elektrienergia       |
| 31-01-2017      | CC002            | 4,100.00  | Elektrienergia       |
| 31-01-2017      | CC003            | 15,000.00 | Elektrienergia       |

Pärast statistilise mõõdu lähteandmete töötlemist luuakse kuluarvestusse järgmised kirjed.

**Statistilised kirjed**

| Kuluobjekt |    | Aruandluskuupäev | Statistilise dimensiooni liige |    Kirjeldus          | Väärtus |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personaliosakond | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 2,450.00  |
| CC002       | FI | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 4,100.00  |
| CC003       | LÜ | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 15,000.00 |

Siin on näide kulu jaotusreeglist, kui elektri eelmääratud dimensiooniliikme eraldamisalus on määratud selles eraldamisaluseks.

| Kuluobjekt | Kirjeldus  | Väärtus | Eraldamistegur          |
|-------------|------|-----------|----------------------------|
| CC001       | Personaliosakond   | 2,450.00  | (2450 ÷ 21 550) × summa  |
| CC002       | FI   | 4,100.00  | (4100 ÷ 21 550) × summa  |
| CC003       | LÜ   | 15,000.00 | (15 000 ÷ 21 550) × summa |

## <a name="hierarchy-allocation-bases"></a>Hierarhia eraldamisalused

Kuluarvestajad saavad luua käsitsi hierarhia eraldamisaluseid, rakendades olemasolevale eraldamisalusele kuluobjekti dimensiooni hierarhiasõlme. Nii saab piirata algse eelmääratud dimensiooniliikme eraldamisaluse vahemikku. Ühe eelnevalt määratud dimensiooni eraldamise põhjal saab luua mitu hierarhia jaotamise alust. Vahemikke saab hallata kuluobjekti dimensioonihierarhias, mis on seotud hierarhia eraldamisalustega.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Näide: hierarhia eraldamisalused, mis põhinevad organisatsiooni täistööajaga töötajatel
Siin on näide kuluobjekti dimensioonihierarhiast, mille saab luua lihtsustatud organisatsiooni kirjeldamiseks.

| Hierarhia nimi | Sõlme tase 0 | Sõlme tase 1 | Sõlme tase 2 | Dimensiooniliikmed |
|----------------|--------------|--------------|--------------|-------------------|
| Organisatsioon   | Tegevjuht          | CFO          | FICO         | CC001             |
| Organisatsioon   | Tegevjuht          | CFO          | Personaliosakond           | CC002             |
| Organisatsioon   | Tegevjuht          | CIO          | LÜ           | CC003             |

Eelmises jaotises loodud TTE eelmääratletud liikme eraldamisaluses on järgmised kirjed.

**Statistilised kirjed**

| Kuluobjekt | Kirjeldus  | Aruandluskuupäev | Statistilise dimensiooni liige | Kirjeldus | Väärtus |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personaliosakond   | 31-01-2017      | TTE-d                        | Täiskohaga töötajad | 1,00      |
| CC002       | FI   | 31-01-2017      | TTE-d                        | Täiskohaga töötajad | 2.00      |
| CC003       | LÜ   | 31-01-2017      | TTE-d                        | Täiskohaga töötajad | 2.00      |

Kulu tuleb jagada organisatsiooni finantsjuhile (CFO) alluvate kulukeskuste vahel. On teada, et õige eraldamise suhtarv on täistööajaga töötajate (TTE-de) arv kulukeskuste kaupa.

**Hierarhia eraldamisalused**

| Nimi                  | Eraldamise alus | Kuluobjekti dimensioonihierarhia | Kuluobjekti dimensioonihierarhia sõlm |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| CFO TTE-de arv | TTE-d           | Organisatsioon                    | CFO                                  |

Eelvaate funktsioon võimaldab kontrollida hierarhia eraldamisalust, mis luuakse statistiliste kirjete põhjal süsteemis.

**Eraldamisaluse üksikasjad**

| Kuluobjekt | Kirjeldus  |  Väärtus |
|-------------|------|------------|
| CC001       | Personaliosakond   | 1,00       |
| CC002       | FI   | 2.00       |

Siin on näide kulu jaotusreeglist, kui eraldamisalus TTE-de arv CFO hierarhias on määratud selles eraldamisaluseks.

| Kuluobjekt | Kirjeldus  | Väärtus | Eraldamistegur |
|-------------|------|-----------|-------------------|
| CC001       | Personaliosakond   | 1,00      | (1/3) × summa    |
| CC002       | FI   | 2.00      | (2/3) × summa    |

## <a name="formula-allocation-bases"></a>Valemi eraldamisalused

Valemi jaotamise aluste abil saate määratleda täpsemad valemid õige eraldamisaluse saavutamiseks. Valemi eraldamise aluseid saab käsitsi luua.

Valemi eraldamise aluse loomisel saate valida, milline statistiline dimensioon ja kuluelemendi dimensioon peaks olema valemi alus. Kõiki eelnevalt valitud dimensioonidest pärinevaid eraldamisaluseid saab valemi eraldamisaluses kasutada.

> [!NOTE]
> Eelnevalt määratletud valemi eraldamisaluseid saab kasutada uue valemi eraldamisaluse määratlemiseks.

Valemi eraldamisaluse tegurites tuleb luua pseudonüüm ja seostada see eraldamisaluse või konstandiga. Seejärel kasutatakse pseudonüüme valemi määratlemiseks.

Valemi määratlemiseks saab kasutada järgmisi tehtemärke.

| Sümbolid | Tekst           |
|---------|----------------|
| ( )     | Sulud    |
| \<      | Väiksem kui   |
| \>      | Suurem kui    |
| +       | Lisa       |
| –       | Lahutamine    |
| \*      | Korrutamine |

Tavalisi **IF**-lauseid ei toetata. Kuid saate luua lauseid ja kinnitada, kas need on tõesed.

| Lause | Kinnitamine | Tulemus |
|-----------|------------|--------|
| a \> b    | Tõene       | 1      |
| a \> b    | Väär      | 0      |

### <a name="example-1-a-simple-formula"></a>Näide 1: lihtne valem

Elektriarved koosnevad sageli kahest osast.

- Fikseeritud tasu võrguühenduse eest
- Tarbimisega seotud kulu kWh kohta

Elektri eelmääratud dimensiooniliikme eraldamisalus on juba määratletud ja sisaldab neid väärtusi.

**Statistilised kirjed**

| Kuluobjekt | Nimi | Aruandluskuupäev | Statistilise dimensiooni liige | Kirjeldus             | Väärtus |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personaliosakond   | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 2,450.00  |
| CC002       | FI   | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 4,100.00  |
| CC003       | LÜ   | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 15,000.00 |

Kui fikseeritud tasu on nüüd vaja elektrit tarbivate kuluobjektide vahel võrdselt jagada, on kulude eraldamiseks kaks võimalust.

- Looge uus eelmääratud eraldamisalus nimega Fikseeritud elekter ja rakendage siis igale elektrit tarbinud kuluobjektile statistiline mõõt 1,00.
- Looge valemi eraldamisalus Fikseeritud elekter, milles kasutatakse süsteemis juba määratletud elektri eelmääratud eraldamisalust. Selle valiku eelis on see, et andmed tuleb laadida kuluarvestusse ainult ühe elektri statistiise dimensiooni liikme kohta.

**Valemi eraldamisalus** 

| Nimi              | Kuluelemendi dimensioon | Statistiline dimensioon | Valem |
|-------------------|------------------------|-----------------------|---------|
| Fikseeritud elekter |                        | Statistilised elemendid  |         |

Enne välja **Valem** täitmist peate määrama pseudonüümi, mida tuleks valemis kasutada.

**Valemi eraldamisaluse tegurid**

| Pseudonüüm | Konstant | Eraldamise alus |
|-------|----------|-----------------|
| a     |          | Elektrienergia     |
| b     | 0,01     |                 |

Pange tähele, et numbrit 0 (null) ei toetata konstandina.

**Valemi eraldamisalus**

| Nimi              | Kuluelemendi dimensioon | Statistiline dimensioon | Valem |
|-------------------|------------------------|-----------------------|---------|
| Fikseeritud elekter |                        | Statistilised elemendid  | a \> b  |

Eelvaate funktsioon võimaldab kontrollida valemi eraldamisalust, mis luuakse statistiliste kirjete põhjal süsteemis.

**Eraldamisaluse üksikasjad**

| Kuluobjekt | Kirjeldus  | Valem           | Väärtus |
|-------------|------|-------------------|-----------|
| CC001       | Personaliosakond   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1,00      |
| CC003       | LÜ   | 15.000,00 \> 0,01 | 1,00      |

Siin on kulu jaotusreegli näide, kui elektri valemi eraldamisalus on määratud selles eraldamisaluseks.

**Kuluobjekti väärtuse eraldamistegur**

| Kuluobjekt | Nimi | Väärtus |  Eraldamistegur |
|-------------|------|-----------|--------------------|
| CC001       | Personaliosakond   | 1,00      | (1/3) × summa     |
| CC002       | FI   | 1,00      | (1/3) × summa     |
| CC003       | LÜ   | 1,00      | (1/3) × summa     |

### <a name="example-2-an-advanced-formula"></a>Näide 2: täpsem valem
Selles näites ei pea elektrikulu lähtuma tegelikust tarbitud elektrist ühikutes kWh. Juhtkond soovib arvestada soodustust elektrikasutuse vähendamise eest. 

| Reegel              | Kurss | 
|-------------------|------|
| a <= 10000.00 kWh | 0.75 |
| a > 10000.00 kWh  | 1.15 |

Luuakse uus valemi eraldamisalus Elektrikasutus.

**Valemi eraldamisalus**

| Nimi              | Kuluelemendi dimensioon | Statistiline dimensioon | Valem |
|-------------------|------------------------|-----------------------|---------|
| Elektrikasutus |                        | Statistilised elemendid  |         |

Enne välja **Valem** täitmist peate määrama pseudonüümi, mida tuleks valemis kasutada.

**Valemi eraldamisaluse tegurid**

| Pseudonüüm | Konstant  | Eraldamise alus |
|-------|-----------|-----------------|
| a     |           | Elektrienergia     |
| b     | 10,000.00 |                 |
| c     | 0.75      |                 |
| d     | 1.15      |                 |

**Valemi eraldamisalus**

| Nimi              | Kuluelemendi dimensioon | Statistiline dimensioon | Valem                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Fikseeritud elekter |                        | Statistilised elemendid  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Eelvaate funktsioon võimaldab kontrollida valemi eraldamisalust, mis luuakse statistiliste kirjete põhjal süsteemis.

**Eraldamisaluse üksikasjad**

| Kuluobjekt |    | Valem                                                                                                                             | Väärtus |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | Personaliosakond | ((2450.00 \> 10 000.00) × ((10 000.00 × 0,75) + (2450.00 – 10 000.00) × 1,15)) + ((2450.00 \<= 10 000.00) × 2450.00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4100.00 \> 10 000.00) × ((10 000.00 × 0,75) + (4100.00 – 10 000.00) × 1,15)) + ((4100.00 \<= 10 000.00) × 4100.00 × 0,75)     | 3,075.00  |
| CC003       | LÜ | ((15000.00 \> 10 000.00) × ((10 000.00 × 0,75) + (15000.00 – 10 000.00) × 1,15)) + ((15000.00 \<= 10 000.00) × 15000.00 × 0,75) | 1,3250.00 |

Siin on valemi CC003 (IT) täpsem selgitus:

((15 000.00 \> 10 000.00) × ((10 000.00 × 0,75) + (15 000.00 – 10 000.00) × 1,15)) + ((15 000.00 \<= 10 000.00) × 15 000.00 × 0,75) = 13 250.00

(1 × (7500.00 + 5000.00 × 1,15)) + (0 × 15 000.00 × 0,75)            

1 × 7500.00 + 5750.00 + 0 

Siin on kulu jaotusreegli näide, kui elektri fikseeritud valemi eraldamisalus on määratud selles eraldamisaluseks.


| Kuluobjekt | Kirjeldus | Väärtus |        Eraldamistegur         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     Personaliosakond      | 1,837.50  | (1837.50 ÷ 18 162.50) × summa  |
|    CC002    |     FI      | 3,075.00  | (3075.00 ÷ 18 162.50) × summa  |
|    CC003    |     LÜ      | 13,250.00 | (13 250.00 ÷ 18 162.50) × summa |

