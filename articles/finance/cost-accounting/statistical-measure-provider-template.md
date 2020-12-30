---
title: Statistilise dimensiooni liikmed ja statistiliste mõõtude pakkuja mallid
description: Selles teemas antakse teavet statistilise dimensiooni liikmete ja statistilise meetme pakkuja mallide kohta. Statistilise dimensiooni liikmeid saab kasutada eraldamisalusena poliitikates nagu kulu jaotus ja kulu eraldamine. Neid saab kasutada ka mitterahalise kulu tarbimise registreerimiseks.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate, CAMAXStatisticalMeasureProviderConfiguration, CAMStatisticalDimensionMember, CAMDataConnectorStatisticalMeasure, CAMImportedStatisticalMeasure, CAMImportedStatisticalMeasureProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec8ec7bc7785b1ddec58b78bd14ce164ad1ce032
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442475"
---
# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Statistilise dimensiooni liikmed ja statistiliste mõõtude pakkuja mallid

[!include [banner](../includes/banner.md)]

Statistilist dimensiooni ja selle liikmeid kasutatakse mitterahaliste kirjete registreerimiseks ja juhtimiseks kuluarvestuses. Statistilise dimensiooni liikmeid saab kasutada kahel eesmärgil:

- eraldamisalusena poliitikates nagu kulu jaotus või kulu eraldamine
- mitterahalise tarbimise registreerimiseks

## <a name="statistical-dimension"></a>Statistiline dimensioon

Statistilisel dimensioonil on kordumatu nimi ja kordumatute dimensiooniliikmete kogum. Statistiline dimensioon on määratud kuluarvestuse pearaamatu ID-le. See seos ühendab kõik vastavad statistilise dimensiooni liikmed kuluarvestuse pearaamatuga. Seetõttu luuakse kõik statistilised kirjed kuluarvestuse pearaamatu kontekstis.

> [!NOTE]
> Statistilise dimensiooni saab määrata mitmele kuluarvestuse pearaamatule.

Siin on statistilise dimensiooni näide.

| Nimi                        | Andmekonnektor dimensiooniliikmete jaoks |
|-----------------------------|--------------------------------------|
| Ühised statistilised elemendid | Imporditud dimensiooniliikmed           |

Siin on näide statistilise dimensiooni kohta, mis on määratud kuluarvestuse pearaamatule.

| Nimi                  | Arvestusvaluuta | Vahetuskursi tüüp | Rahanduskalender | Kuluelemendi dimensioon | Statistiline dimensioon       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Juhi raamatupidamine | USA dollar                 | Konstantne valuuta  | Rahandusperiood   | Ühised kuluelemendid   | Ühised statistilised elemendid |

## <a name="statistical-dimension-members"></a>Statistilise dimensiooni liikmed

Statistilise dimensiooni liige esindab üksust, millele soovite mitterahalisi meetmeid registreerida. Neid meetmeid saab kasutada eraldamisalusena või lihtsalt mitterahaliste väärtuste registreerimiseks.

Statistilise dimensiooni liikmed saab käsitsi luua. Teine võimalus on importida need failist, kasutades andmehalduse impordi-/eksporditööriista.

Statistilise dimensiooni liikmest saab automaatselt eelmääratud eraldamisalus. Seda saab kasutada eraldamisalusena poliitikates või sisendina teist tüüpi eraldamisalustes.

Siin on mõned näited tüüpiliste statistilise dimensiooni liikmete kohta.

| Statistilise dimensiooni nimi  | Statistilised elemendid | Kirjeldus             | Üksus |
|-----------------------------|----------------------|-------------------------|------|
| Ühised statistilised elemendid | TTE                  | Täiskohaga töötajad     | Ea.  |
| Ühised statistilised elemendid | Elektrienergia          | Elektri tarbimine | kWh  |
| Ühised statistilised elemendid | Pakendi CC              | Pakendi kulukeskus   | Tunnid |

## <a name="statistical-measure-provider-template"></a>Statistiliste mõõtude pakkuja mall

Statistilised mõõdud võivad pärineda erinevatest allikatest. Dynamics 365 Finance on suurepärane allikas, millest statistilisi mõõte hankida. Võite kasutada statistilise mõõdu pakkuja malli, et konfigureerida hõlpsasti statistilisi mõõte, mida soovite hankida.

Statistilise mõõdu pakkuja malli definitsioon on üldine ja seda saab kasutada uuesti mitmes statistilise dimensiooni liikmes.

> [!NOTE]
> Kõiki tabeleid, mis sisaldavad finantsdimensioone, saab kasutada statistiliste mõõtude allikana.

**Näide: töötajate arv kulukeskuse kohta**

Töötajate arv kulukeskuse kohta on statistiline mõõt, mida saab kasutada mitmesugusteks juhtimisülevaateid pakkuvateks eesmärkideks.

- Statistiline aruandlusmõõt kulukeskuse järgi
- Eraldamisalus mitmesuguste kulutüüpide jaoks
- Sisemised kulumäärad kulukeskuste kaupa.

    - Kulu töötaja järgi
    - Tulu töötaja järgi

Tabelis HcmEmployment on loend kõigist töötajatest eksemplaris. See on üldine tabel. Seega pole kirjed seotud konkreetse andmevaldkonna ID-ga.

Siin on näide töötajate kohta tabelis HcmEmployment.

| Nimi       | Kulukeskus | Kirjeldus   | Töötaja tüüp |
|------------|-------------|----|-------------|
| Töötaja 1 | CC001       | Personaliosakond | Töötaja    |
| Töötaja 2 | CC002       | FI | Töötaja    |
| Töötaja 3 | CC002       | FI | Töötaja    |
| Töötaja 4 | CC003       | LÜ | Töötaja    |
| Töötaja 5 | CC003       | LÜ | Töötaja    |
| Töötaja 6 | CC002       | FI | Peatöövõtja  |

Kui loote kirje **Statistiliste mõõtude pakkuja mall**, siis peate otsustama, millist funktsiooni kasutada.

- **Loendamine** – edastatakse kirjete arv kuluobjekti kohta.
- **Summa** – edastatakse kirjete summa kuluobjekti kohta. (Väljad **Summa** ja **Kuupäev** on kohustuslikud.)

## <a name="using-the-count-function"></a>Loendamise funktsiooni kasutamine

Näiteks saab statistilise mõõdu pakkuja malli seadistada järgmiselt.

| Nimi  | Funktsioon | Lähtetabel  | Summa väli      | Kuupäevaväli     |
|-------|----------|---------------|----------------|----------------|
| TTE-d  | Loendus    | HcmEmployment | Pole kohaldatav | Pole kohaldatav |

Võite lisada ka vähemalt ühe vahemiku lähtetabelist pärinevate mõõtude kitsendamiseks.

Kui soovite selle näite puhul lihtsalt kõigi täisajaga töötajate (TTE) arvu, saate lisada vahemiku väljal **Töötaja tüüp**. Tehke väljal **Kriteeriumid** valik **Töötaja** väljundvahemiku piiramiseks järgmiselt.

**Vahemikud**

| Lähtetabel  | Väli       | Kriteeriumid |
|---------------|-------------|----------|
| HcmEmployment | Töötaja tüüp | Töötaja |

Enne kui saate statistilised mõõdud kuluarvestusse, tuleb luua seos statistilise mõõdu pakkuja malli ja statistilise dimensiooni liikme vahel. See seos luuakse kuluarvestuse pearaamatu ja versiooni kohta. Seos koosneb andmekonnektorist ja andmepakkujast. Teil võib olla statistilise dimensiooni kohta mitu andmekonnektorit ja andmepakkujat.

> [!NOTE]
> Selles näites loome seose ainult **tegeliku versiooni** jaoks.

Avage **Kuluarvestuse pearaamat** \> **Tegelik versioon** \> **Halda** \> **Statistilised mõõdud** seose loomiseks. Selle stsenaariumi puhul valige andmekonnektor **Dynamics 365 Finance – statistilised mõõdud**, kuna soovime ekstraktida andmed rakendusest Finance.

**Andmeallikas**

| Nimi        | Andmekonnektor                                                                     | Statistilise dimensiooni liige |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| TTE-d D365FO | Dynamics 365 Finance – statistilised mõõdud | TTE-d                         |

**Andmepakkuja konfiguratsioon**

| Statistilise malli nimi |
|---------------------------|
| TTE-d                      |

Pärast statistilise mõõdu lähteandmete töötlemist luuakse kuluarvestusse järgmised statistilised kirjed.

**Tööleht**

| Tööleht | Töölehe tüüp                       | Rahanduskalendri periood | Aasta   |  Periood  |  Versioon | Andmekonnektori allikakirjed|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Statistilise kirje ülekandmistööleht | Fiskaalne                 | 2017   | Periood 1 | CA pearaamatu USMF | TTE-d                   |

**Statistilise kirje ülekandmistöölehe sisestused**

| Aruandluskuupäev | Väärtus | Statistiline element |   Kirjeldus       | Kulukeskus |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31-01-2017      | 1,00      | TTE-d                | Täiskohaga töötajad | CC001       |
| 31-01-2017      | 2.00      | TTE-d                | Täiskohaga töötajad | CC002       |
| 31-01-2017      | 2.00      | TTE-d                | Täiskohaga töötajad | CC003       |

**Statistilised kirjed**

| Kuluobjekt |    | Aruandluskuupäev | Statistilise dimensiooni liige |  Kirjeldus        | Väärtus |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personaliosakond | 31-01-2017      | TTE-d                         | Täiskohaga töötajad | 1,00      |
| CC002       | FI | 31-01-2017      | TTE-d                         | Täiskohaga töötajad | 2.00      |
| CC003       | LÜ | 31-01-2017      | TTE-d                         | Täiskohaga töötajad | 2.00      |

Kui TTE-de eelmääratud dimensiooniliikme eraldamisalus on määratud eraldamisaluseks kulu jaotusreeglis, siis jaotatakse kulu, kasutades järgmist eraldamistegurit.

| Kuluobjekt | Kirjeldus    | Väärtus | Eraldamistegur |
|-------------|----|-----------|-------------------|
| CC001       | Personaliosakond | 1,00      | (1/5) × summa    |
| CC002       | FI | 2.00      | (2/5) × summa    |
| CC003       | LÜ | 2.00      | (2/5) × summa    |

## <a name="using-the-sum-function"></a>Summa funktsiooni kasutamine

Tootmise kulukeskus CC010 (Pakkimine) vastutab toodete pakkimise eest enne nende saatmist klientidele. Otsene töö maksumus lisatakse toodetele koosluse (BOM) ja protsessi kaudu. Kulukeskuse käitamise kaudsed kulud tuleb samuti toodetud toodetele eraldada. Sageli on sellise eraldamise parim statistiline mõõt registreeritud tootmistundide arv toote kohta antud perioodil.

Tabelis ProdRouteTrans on kõik tootmistööjõu kanded juriidilise isiku kohta DataAreadID.

Siin on tabeli ProdRouteTrans näide.

| Viide        | Kood | Toiming | Tüüp | Aeg  | Füüsiline kuupäev | Tootegrupp (finantsdimensioon) | Juriidiline isik |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Tootmistellimus | P0001  | Pakendamine | Aeg | 8.00  | 01-01-2017    | Apelsinimahl B2B                    | USMF         |
| Tootmistellimus | P0001  | Pakendamine | Aeg | 8.00  | 02-01-2017    | Apelsinimahl B2B                    | USMF         |
| Tootmistellimus | P0002  | Pakendamine | Aeg | 4,00  | 03-01-2017    | Apelsinimahl tarbija               | USMF         |
| Tootmistellimus | P0003  | Pakendamine | Aeg | 4,00  | 03-01-2017    | Apelsinimahl tarbija               | USMF         |
| Tootmistellimus | P0004  | Rekonst.  | Aeg | 10,00 | 03-01-2017    | Apelsinimahl tarbija               | USMF         |

Kui loote kirje **Statistiliste mõõtude pakkuja mall**, siis peate otsustama, millist funktsiooni kasutada.

- **Loendamine** – edastatakse kirjete arv kuluobjekti kohta.
- **Summa** – edastatakse kirjete summa kuluobjekti kohta. (Väljad **Summa** ja **Kuupäev** on kohustuslikud.)

Statistilise mõõdu pakkuja malli saab seadistada järgmiselt.

| Nimi    | Funktsioon | Lähtetabel   | Summa väli | Kuupäevaväli    |
|---------|----------|----------------|-----------|---------------|
| Pakendi CC | Summa      | ProdRouteTrans | Tunnid     | Füüsiline kuupäev |

Võite lisada ka vahemikke lähtetabelist pärinevate mõõtude kitsendamiseks.

Selles näites, kui soovite ainult kulukeskusega CC010 Pakkimine seotud tundide summat, võite lisada vahemiku väljal **Toiming**. Tehke väljal **Kriteeriumid** valik **Pakkimine** väljundvahemiku piiramiseks järgmiselt.

**Vahemikud**

| Lähtetabel   | Väli     | Kriteeriumid  |
|----------------|-----------|-----------|
| ProdRouteTrans | Toiming | Pakendamine |

Enne kui saate statistilised mõõdud kuluarvestusse, tuleb luua seos statistilise mõõdu pakkuja malli ja statistilise dimensiooni liikme vahel. See seos luuakse kuluarvestuse pearaamatu ja versiooni kohta. Seos koosneb andmekonnektorist ja andmepakkujast. Teil võib olla statistilise dimensiooni kohta mitu andmekonnektorit ja andmepakkujat.

> [!NOTE]
> Selles näites loome seose ainult **tegeliku versiooni** jaoks.

Avage **Kuluarvestuse pearaamat** \> **Tegelik versioon** \> **Halda** \> **Statistilised mõõdud** seose loomiseks. Selle stsenaariumi puhul valige andmekonnektor **Dynamics 365 Finance – statistilised mõõdud**, kuna soovime ekstraktida andmed rakendusest Finance.

**Andmeallikas**

| Nimi           | Andmekonnektor                                                                     | Statistilise dimensiooni liige |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pakendi CC D365FO | Dynamics 365 Finance – statistilised mõõdud | Pakendi CC                      |

Süsteem tuvastab, et ProdRouteTrans on tabel, kus iga kirje kuulub eraldi juriidilise isiku juurde. Seetõttu palutakse teil valida juriidiline isik, kust kanded tuleks importida.

**Andmepakkuja konfiguratsioon**

| Statistilise malli nimi | Juriidiline isik |
|---------------------------|--------------|
| Pakendi CC                   | USMF         |

Pärast statistilise mõõdu lähteandmete töötlemist luuakse kuluarvestusse järgmised statistilised kirjed.

**Tööleht**

| Tööleht | Töölehe tüüp                     | Rahanduskalendri periood | Aasta   | Periood | Versioon   |   Andmekonnektori allikakirjed  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Statistilise kirje ülekandmistööleht | Fiskaalne               | 2017    | Periood 1  | CA pearaamatu USMF | Pakendi CC |

**Statistilise kirje ülekandmistöölehe sisestused**

| Aruandluskuupäev | Väärtus | Statistiline element |  Kirjeldus          | Tootegrupp         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31-01-2017      | 16.00     | Pakendi CC             | Pakendi kulukeskus | Apelsinimahl B2B      |
| 31-01-2017      | 8.00      | Pakendi CC             | Pakendi kulukeskus | Apelsinimahl tarbija |

**Statistilised kirjed**

| Kuluobjekt           | Aruandluskuupäev | Statistilise dimensiooni liige |    Kirjeldus        | Väärtus |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Apelsinimahl B2B      | 31-01-2017      | Pakendi CC                      | Pakendi kulukeskus | 16.00     |
| Apelsinimahl tarbija | 31-01-2017      | Pakendi CC                      | Pakendi kulukeskus | 8.00      |

Kui Pakendi CC eelmääratud dimensiooniliikme eraldamisalus on määratud eraldamisaluseks kulu jaotusreeglis, siis jaotatakse kulu, kasutades järgmist eraldamistegurit.

| Kuluobjekt           | Väärtus | Eraldamistegur  |
|-----------------------|-----------|--------------------|
| Apelsinimahl B2B      | 16.00     | (16 ÷ 24) × summa |
| Apelsinimahl tarbija | 8.00      | (8 ÷ 24) × summa  |

## <a name="imported-statistical-measures"></a>Imporditud statistilised mõõdud

Saate importida statistilised mõõdud kuluarvestusse, kasutades andmehalduse impordi/ekspordi tööriista.

Importimiseks kasutatavat andmeüksust nimetatakse imporditud statistilisteks mõõtudeks.

> [!NOTE]
> See andmeüksus on mõeldud lubama kuni viit kordumatut dimensiooniväärtust kirje kohta.

Elektritarbimine registreeritakse Microsoft Excelis, kasutades eelmääratud andmeüksuse vormingut. Siin on näide.

| Aruandluskuupäev | Dimensiooniliikme nimi 1 | Dimensiooniliikme nimi 2 | Dimensiooniliikme nimi 5 | Väärtus  | Lähteidentifikaator |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31-01-2017      | CC001                  |                        |                        | 2,450.00   | Elektrienergia       |
| 31-01-2017      | CC002                  |                        |                        | 4,100.00   | Elektrienergia       |
| 31-01-2017      | CC003                  |                        |                        | 15,000.00  | Elektrienergia       |

Kui importisite andmed andmehalduse kaudu, salvestatakse andmed kuluarvestuse vahetabelisse. Seetõttu saab imporditud andmeid kasutada mitmes kuluarvestuse pearaamatus. Andmete uuesti laadimine pole vajalik.

Andmete importimiseks avage **Imporditud andmed** \> **Andmeüksus** \> **Imporditud statistilised mõõdud**.

| Lähteidentifikaator | Aruandluskuupäev | Väärtus  | Dimensiooniliikme nimi 1 | Dimensiooniliikme nimi 2 | Dimensiooniliikme nimi 5 |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektrienergia       | 31-01-2017      | 2,450.00   | CC001                  |                        |                        |
| Elektrienergia       | 31-01-2017      | 4,100.00   | CC002                  |                        |                        |
| Elektrienergia       | 31-01-2017      | 15,000.00  | CC003                  |                        |                        |

Enne kui saate statistilised mõõdud kuluarvestusse, tuleb luua seos lähteidentifikaatori ja statistilise dimensiooni liikme vahel. See seos luuakse kuluarvestuse pearaamatu ja versiooni kohta. Seos koosneb andmekonnektorist ja andmepakkujast. Teil võib olla statistilise dimensiooni kohta mitu andmekonnektorit ja andmepakkujat.

> [!NOTE]
> Selles näites loome seose ainult **tegeliku versiooni** jaoks.

Avage **Kuluarvestuse pearaamat** \> **Tegelik versioon** \> **Halda** \> **Statistilised mõõdud** seose loomiseks. Selle stsenaariumi puhul valige andmekonnektor **Imporditud statistilised mõõdud**, kuna andmed on imporditud muu osapoole süsteemist Exceli kaudu kuluarvestusse.

**Andmeallikas**

| Nimi        | Andmekonnektor                | Statistilise dimensiooni liige |
|-------------|-------------------------------|------------------------------|
| Elektrienergia | Imporditud statistilised mõõdud | Elektrienergia                  |

**Andmepakkuja konfiguratsioon**

| Lähteidentifikaatori importimine | Funktsioon | Dimensioon 1   | Dimensioon 2 | Dimensioon 5 |
|--------------------------|----------|--------------|------------|------------|
| Elektrienergia              | Summa      | Kulukeskused |            |            |

> [!NOTE]
> Kui määratlete andmepakkuja konfiguratsiooni, siis peate määrama, milliseid kuluobjekti dimensioone imporditud kannetega vastendada. Pärast statistilise mõõdu lähteandmete töötlemist luuakse kuluarvestusse järgmised statistilised kirjed.

**Tööleht**

| Tööleht | Töölehe tüüp                       | Rahanduskalendri periood | Aasta  | Periood  |Versioon      |Andmekonnektori allikakirjed |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Statistilise kirje ülekandmistööleht | Fiskaalne                 | 2017  | Periood 1 | CA pearaamatu USMF | Elektrienergia |

**Statistilise kirje ülekandmistöölehe sisestused**

| Aruandluskuupäev | Väärtus  | Kuluelement |   Kirjeldus           | Kulukeskus |
|-----------------|------------|--------------|-------------------------|-------------|
| 31-01-2017      | 2,450.00   | Elektrienergia  | Elektri tarbimine | CC001       |
| 31-01-2017      | 4,100.00   | Elektrienergia  | Elektri tarbimine | CC002       |
| 31-01-2017      | 15,000.00  | Elektrienergia  | Elektri tarbimine | CC003       |

**Statistilised kirjed**

| Kuluobjekt |    | Aruandluskuupäev | Statistilise dimensiooni liige |      Kirjeldus                   | Väärtus  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | Personaliosakond | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 2,450.00   |
| CC002       | FI | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 4,100.00   |
| CC003       | LÜ | 31-01-2017      | Elektrienergia                  | Elektri tarbimine | 15,000.00  |

Kui elektrienergia eelmääratud dimensiooniliikme eraldamisalus on määratud eraldamisaluseks kulu jaotusreeglis, siis jaotatakse kulu, kasutades järgmist eraldamistegurit.

| Kuluobjekt |    | Väärtus | Eraldamistegur          |
|-------------|----|-----------|----------------------------|
| CC001       | Personaliosakond | 2,450.00  | (2450 ÷ 21 550) × summa  |
| CC002       | FI | 4,100.00  | (4100 ÷ 21 550) × summa  |
| CC003       | LÜ | 15,000.00 | (15 000 ÷ 21 550) × summa |

## <a name="additional-resources"></a>Lisaressursid

[Eraldamise alused](allocation-bases.md)
