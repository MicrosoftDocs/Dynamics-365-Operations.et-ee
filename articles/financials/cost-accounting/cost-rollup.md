---
title: Kulukomplekti poliitika ja üldkulude arvutus
description: See teema selgitab, kuidas määrata õige teiseste kuluelementide tase ja luua kulu ümberarvestusreeglid, mis sobivad organisatsiooni aruandluse ja kulu jälgitavusega.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e809cb2cadadc623134805e028de7f2e64dd662f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "356135"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Kulukomplekti poliitika ja üldkulude arvutus 

[!include [banner](../includes/banner.md)]

Kuluarvestuse abil saate ülevaate, kuidas kuluvoog on seotud organisatsioonis edastatavate toodete ja teenustega. Kulude läbipaistvuse tagamiseks on oluline saavutada sobival eraldamisalusel põhinev kulude jagamine kuluobjektide vahel. Vaikimisi saavutatakse kulude eraldamine esmase kuluelemendi jaoks, mis on mõnes olukorras vajalik, kuid sellel on mõningaid nüansse, mida peaks arvestama.

-   Täiendavad kuluobjektid jäävad pärast üldkulude arvutamist esmase kuluelemendi jaoks nullsaldoga.

-   Üldkulude arvutuse loodud kulukirjete maht võib olla väga suur.

-   Kuluobjektide vahelist kuluvoogu pole võimalik jälgida.

Nende mõjude vältimiseks võimaldab kuluarvestus konfigureerida kulude eraldamist nii, et see vastaks teie organisatsiooni juhtimisaruandluse vajadustele. See teema selgitab, kuidas saate määrata õige teiseste kuluelementide taseme ja luua kulu ümberarvestusreeglid, mis sobivad organisatsiooni aruandluse ja kulu jälgitavusega.

> [!NOTE]
> Nõuete muutuse registreerimisel saate konfiguratsioone muuta.

## <a name="example-of-cost-rollup-policy-setup"></a>Kulu ümberarvestuse poliitika seadistuse näide

Oletagem, et organisatsioonil on järgmine 4 kulukeskusega struktuur.

![Organisatsiooni struktuuri näide](./media/dimension-hierarchy-org.png)

**Kuluobjekti dimensioon**

| Kulukeskused | Kirjeldus          |
|--------------|-----------|
| CC001        | Personaliosakond        |
| CC002        | Finantsid   |
| CC003        | Assembler  |
| CC004        | Pakendamine |

**Kuluelemendi dimensioon**

| Kuluelemendid | Kirjeldus | Tüüp    |
|---------------|-------------|---------|
| 1001          | Elektrienergia | Esmane |
| 1002          | Palgad    | Esmane |
| 1003          | Reklaam | Esmane |

Dimensioonihierarhia, mis rahuldab organisatsiooni aruandlusvajadused, saab seadistada järgmiselt.

**Dimensioonihierarhia üksikasjad**

| Dimensioonihierarhia nimi | Dimensioon    | Dimensiooni hierarhia tüübi nimi      | Juurdepääsuloendi hierarhia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatsioon             | Kulukeskused | Dimensiooni klassifitseerimishierarhia | Ei                    |

**Dimensioonihierarhia**

|              | Dimensiooniliikmete vahemikud |                     |
|--------------|-------------------------|---------------------|
| **Sõlmed**        | **Lähtedimensiooni liige**   | **Sihtdimensiooni liige** |
| Organisatsioon |                         |                     |
| &nbsp;&nbsp;Administraator             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Finantsid              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;Personaliosakond               | CC002                   | CC002               |
| &nbsp;&nbsp;Tootmine               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakendamine              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembler             | CC004                   | CC004               |

Dimensioonihierarhia, mis täidab poliitika nõude, saab seadistada järgmiselt.

**Dimensioonihierarhia üksikasjad**

| Dimensioonihierarhia nimi | Dimensioon     | Dimensiooni hierarhia tüübi nimi      |
|--------------------------|---------------|------------------------------------|
| Kasumi- ja kahjumiväljavõte  | Kuluelemendid | Dimensiooni klassifitseerimishierarhia |

**Dimensioonihierarhia**

|                         | Dimensiooniliikmete vahemikud |                     |
|-------------------------|-------------------------|---------------------|
| Sõlmpunktid                   | Lähtedimensiooni liige   | Sihtdimensiooni liige |
| Kasumi- ja kahjumiväljavõte |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Peamine kulu                    | 10001                   | 10003               |

Pärast pearaamatukannete töötlemist näeb kulukirje saldo kuluobjektide kaupa välja selline.

|                      | **Kuluobjekt** |           |           |           | **Kokku**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Kuluelement**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 elekter** | 100,00          | 200,00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 palgad**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 reklaam** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Statistiline dimensioon**

| Statistilised elemendid |    Kirjeldus   |
|----------------------|------------------|
| SE-1                 | Inimressursside teenused      |
| SE-2                 | Rahandusteenused |

Kuluobjekt CC001 inimressursid jagab inimressursside teenused mitmele kuluobjektile.

Inimressursside teenuseid tarbitakse järgmises väärtuse jaotuses.

| Kuluobjekt | Kirjeldus |   Inimressursside teenused |
|-------------|-------------|----|
| CC002       | Finantsid     | 35 |
| CC003       | Assembler    | 55 |
| CC004       | Pakendamine   | 10 |

Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.

Finantsteenuseid tarbitakse järgmises väärtuse jaotuses.

| Kuluobjekt |   Kirjeldus    |  Rahandusteenused   |
|-------------|------------------|----|
| CC003       | Assembler         | 65 |
| CC004       | Pakendamine        | 35 |

Kulueralduspoliitikad saab seadistada järgmiselt.

| Poliitika nimi | Kirjeldus     | Kuluobjekti dimensioonihierarhia | Statistiline dimensioon | Kuluelemendi dimensioon |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Kulude eraldamine | Organisatsioon                    | Statistilised elemendid  | Kuluelemendid          |

Kulueraldusreeglid saab seadistada järgmiselt.

| Kuluobjekti dimensioonihierarhia sõlm | Kulukäitumine | Eraldamise alus        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Kokku         | **Inimressursside teenused**        |
| CC002                                | Kokku         | **Finantsteenused** |

<a name="brhow-cost-flows-between-cost-centers"></a><br>Kuidas kulu kulukeskuste vahel liigub 
---------------------------------------------------

Kui soovite teada, kuidas kulu organisatsioonis kulukeskuste vahel liigub, võite luua igale kulukeskusele kuluelemendid tüübiga **Teisene**. Neid kuluelemente kasutatakse seejärel saldode ülekandmiseks kulukeskuste vahel üldkulude arvutamise käigus.

Kuluelemendi dimensiooniliikmed saab seadistada järgmiselt.

| Kuluelemendid | Tüüp          |               |
|---------------|---------------|---------------|
| 1001          | Elektrienergia   | Esmane       |
| 1002          | Palgad      | Esmane       |
| 1003          | Reklaam   | Esmane       |
| **SC-CC001**  | **Inimressursid**        | **Teisene** |
| **SC-CC002**  | **Finantsid**   | **Teisene** |
| **SC-CC003**  | **Kokkupanek**  | **Teisene** |
| **SC-CC004**  | **Pakendamine** | **Teisene** |

Dimensioonihierarhiat **Kasumi- ja kahjumiaruanne** on vaja täiendada uute dimensiooniliikmetega, et dimensioonihierarhia sisaldaks õigeid andmeid, mida saab aruandluse ja poliitika määratlemiseks kasutada.

**Dimensioonihierarhia üksikasjad**

| Dimensioonihierarhia nimi | Dimensioon     | Dimensiooni hierarhia tüübi nimi      |
|--------------------------|---------------|------------------------------------|
| Kasumi- ja kahjumiväljavõte  | Kuluelemendid | Dimensiooni klassifitseerimishierarhia |

**Dimensioonihierarhia**

|                         | Dimensiooniliikmete vahemikud |                     |
|-------------------------|-------------------------|---------------------|
| Sõlmpunktid                   | Lähtedimensiooni liige   | Sihtdimensiooni liige |
| Kasumi- ja kahjumiväljavõte |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Peamine kulu                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Sekundaarne kulu                         | **SC-CC001**            | **SC-CC004**        |

Looge **Kulu ümberarvestuse poliitika**, kus iga kulukeskus vastendatakse vastava kuluelemendiga, mille tüüp on **Teisene**.

**Kulu ümberarvestuse poliitikad**

| Poliitika nimi | Kirjeldus | Kuluobjekti dimensioonihierarhia | Kuluelemendi dimensioonihierarhia |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Kuluvoog   | Organisatsioon                    | Kasumi- ja kahjumiväljavõte          |

**Kulu ümberarvestuse reeglid**

| Kuluobjekti dimensioonihierarhia sõlm | Kuluelemendi dimensioonihierarhia sõlm | Teisene kuluelement |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Kasumi- ja kahjumiväljavõte               | **SC-CC001**           |
| CC002                                | Kasumi- ja kahjumiväljavõte               | **SC-CC002**           |
| CC003                                | Kasumi- ja kahjumiväljavõte               | **SC-CC003**           |
| CC004                                | Kasumi- ja kahjumiväljavõte               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Üldkulude arvutamine

**Tööleht**

| Tööleht | Töölehe tüüp            | Rahanduskalendri periood | Aasta | Periood | Versioon       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Kulueralduse tööleht | Fiskaalne                 | 2017    | Periood 1 | Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood |

Süsteem rakendab nüüd **Kulude ümberarvestuse poliitika**, luues **kuluobjekti saldo töölehekirjed**.

**Kuluobjekti saldo töölehe sisestused**

| Aruandluskuupäev | Kuluobjekt | Kirjeldus  | Kuluelement | Kirjeldus |  Summa |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31-01-2017      | CC001       | Personaliosakond           | SC-CC001 | Personaliosakond        | 10.100,00 |
| 31-01-2017      | CC002       | Finantsid      | SC-CC002 | Finantsid   | 17.735,00 |
| 31-01-2017      | CC003       | Assembler     | SC-CC003 | Assembler  | 31.082,75 |
| 31-01-2017      | CC004       | Pakendamine    | SC-CC004 | Pakendamine | 15.717,25 |

> [!NOTE]
> Luuakse töölehekirjed jaotise **Kulude ümberarvestuse poliitika** reeglite põhjal, kui poliitika on olemas. Kuvatav saldo on üldkulude arvutuse saldo.

Leht **Kuluobjekti kulu saldo töölehekirje üksikasjad**, millele pääseb töölehekirjetest, kuvab saldo saamise viisi.

**Näide: töölehekirje kuluobjektile CC002 finantsid**

**Kuluobjekti kulu saldo töölehekirje üksikasjad**

| Kuluelemendi dimensiooniliige | Kirjeldus |  Summa   |
|-------------------------------|-------------|-----------|
| 1001                          | Elektrienergia | 200,00    |
| 1002                          | Palgad    | 10.000,00 |
| 1003                          | Reklaam | 4.000,00  |
| SC-CC001                      | Personaliosakond          | 3.535,00  |

**Üldkulude arvutusest saadud kulukirjed**

| Kuluobjekt | Kirjeldus  | Kuluelement   | Kirjeldus  |        Summa     |       Aruandluskuupäev     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | Personaliosakond           | SC-CC001 | Personaliosakond              | \-, 10.100,00 | 31-01-2017 |
| CC002       | Finantsid      | SC-CC001 | Personaliosakond              | 3.535,00    | 31-01-2017 |
| CC003       | Assembler     | SC-CC001 | Personaliosakond              | 5.555,00    | 31-01-2017 |
| CC004       | Pakendamine    | SC-CC001 | Personaliosakond              | 1.010,00    | 31-01-2017 |
| CC002       | Finantsid      | SC-CC002 | Finantsid         | \-, 17.735,00 | 31-01-2017 |
| CC003       | Assembler     | SC-CC002 | Finantsid         | 11.527,75   | 31-01-2017 |
| CC004       | Pakendamine    | SC-CC002 | Finantsid         | 6.207,25    | 31-01-2017 |

Kui **üldkulude arvutus** on tehtud, võite tulemuste kohta aruande koostada, kasutades tööriistu nagu Microsoft SharePointi tööruum, Excel või Power BI.

## <a name="view-reporting-in-excel"></a>Aruandluse vaatamine Excelis 

Dimensioonihierarhiad võimaldavad kuvada andmed erinevatel liitmistasemetel.

Siin on näide Power Pivoti aruandluse kohta Excelis.

| **Kasumi- ja kahjumiväljavõte** | **Kuluobjekt** |                |               |               |  **Kogusumma**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Peamine kulu**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| &nbsp;&nbsp;&nbsp;&nbsp;, 1001                            | 100,00          | 200,00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;, 1002                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;, 1003                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**Teisene kulu**                            | **-10100,00**  | **-14200,00** | **17,082,75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | \-, 10.100,00     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | \-, 17.735,00    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **Kokku**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Valikute **Kulu ümberarvestuse poliitika** ja **Teisest tüüpi kuluelemendid** võimaldab jätta peamise kulu kuluobjekti kohta sisemiseks aruandluseks peamise kuluna, mis jääb alles pärast **üldkulude arvutamist**.

Kui samas näites poleks **kulude ümberarvestuse poliitikat** loodud, oleks aruande tulemus olnud selline, nagu allpool näidatud. Kulu liigub õigesti, kuid jälgitavus ja ülevaade selle kohta, kuidas kulu kulukeskuste vahel liigub, lähevad kaotsi.

| **Kasumi- ja kahjumiväljavõte** | **Kuluobjekt** |           |               |               |          **Kokku**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Peamine kulu**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;, 1001                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;, 1002                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;, 1003                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Teisene kulu**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **Kokku**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Olenevalt aruandluse ja jälgitavuse vajadustest teie organisatsioonis, saate määrata õige teiseste kuluelementide taseme ja luua teie vajadustele vastavad kulu ümberarvestusreeglid.

Selge eraldatud valikute **Kulude eraldamine** ja **Kulude ümberarvestuspoliitikad** vahel tagab paindlikkuse pidevate muudatuste tegemisel, teineteist mõjutamata.



## <a name="additional-resources"></a>Lisaressursid
-  [Kuluobjekti dimensioonid](cost-objects.md)
-  [Kuluelemendi dimensioonid](cost-elements.md)
-  [Dimensioonihierarhiad](dimension-hierarchy.md)
-  [Üldkulude arvutus](overhead-calculation.md)
