---
title: Tööde kogumisse kuuluvatele töödele aja eraldamine
description: Töid saate kogumisse siduda valikus Tootmise käivitamine. Seejärel saate alustada lehelt Tööde loend üheaegselt mitut tööd.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33d6bab9beb28d18e2094d7fb5e670e9425aac39
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552972"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Tööde kogumisse kuuluvatele töödele aja eraldamine

[!include [banner](../includes/banner.md)]

Töid saate kogumisse siduda valikus Tootmise käivitamine. Seejärel saate alustada lehelt Tööde loend üheaegselt mitut tööd.

Tööde kogumisse sidumisel tuleb määratleda, kuidas iga töö puhul kõikidele töödele registreeritud koguaega eraldada. Eraldamise määratlemiseks valige üks järgmistest suvanditest lehekülje **Eraldusvõtmed** väljal **Kogumi tüüp**.

-   **Hinnang** – aeg jagatakse tööde vahel töödele kuluva hinnangulise aja alusel.
-   **Tööd** – aeg jagatakse vastavalt kogumisse seotud tööde koguarvule ja kõigi tööde lõpetamiseks kulunud ajale.
-   **Netoaeg** – aeg jagatakse igal ajal kogumisse seotud tööde vahel võrdselt.
-   **Reaalajas** – eraldatakse tegelik tööaeg. Kulu saab arvutada tegelike palgakulude alusel. **Märkus.** Eraldusvõti **Reaalajas** on saadaval ainult siis, kui teie ettevõte kasutab tööajaarvestuse palgaarvestuse funktsiooni.

Järgmised näited näitavad erinevate eraldusvõtmete tulemusi.

## <a name="example-scenario"></a>Näidisstsenaarium
Tööjärjekorras ootavad lõpetamist kolm tööd. Alustate esimest tööd ja samal ajal, kui esimene on alles pooleli, alustate ka teist ja kolmandat tööd. Seega tekib kolme tööga kogum. Järgmises tabelis on näidatud igale tööle kuluv hinnanguline tootmisaeg.

| Töö   | Tootmisaeg |
|-------|-----------------|
| Töö 1 | 1 tund          |
| Töö 2 | 3 tundi         |
| Töö 3 | 4 tundi         |
| Kokku | 8 tundi         |

Järgmine tabel näitab tegelikku igale tööle kulunud töötundide arvu.

| Töö    | Algusaeg | Lõppaeg | Kogumiaeg |
|--------|------------|----------|-------------|
| Töö 1  | 09.00      | 11.00    | 2 tundi     |
| Töö 2  | 10.00      | 13.00    | 3 tundi     |
| Töö 3  | 10.00      | 15.00    | 5 tundi     |
| Kogum | 09.00      | 15.00    | 6 tundi     |

Järgmised jaotised kirjeldavad igale eraldusvõtmele arvutatud aega.

## <a name="estimation-allocation-key"></a>Hinnanguline eraldusvõti
Järgnev tabel illustreerib eraldatud aja arvutamise valemit. Siin on valem: tööks kuluv aeg = kogu kogumiaeg x (hinnanguline tööaeg / hinnanguline koguaeg)

| Töö   | Valem           | Eraldatud aeg |
|-------|-------------------|----------------|
| Töö 1 | 6 x (1 / 8) tundi | 0,75 tundi      |
| Töö 2 | 6 x (3 / 8) tundi | 2,25 tundi     |
| Töö 3 | 6 x (4 / 8) tundi | 3,00 tundi     |

## <a name="jobs-allocation-key"></a>Tööde eraldusvõti
Järgnev tabel illustreerib eraldatud aja arvutamise valemit. Siin on valem: tööks kuluv aeg = kogu kogumiaeg / tööde arv

| Töö   | Valem | Eraldatud aeg |
|-------|---------|----------------|
| Töö 1 | 6 / 3   | 2 tundi        |
| Töö 2 | 6 / 3   | 2 tundi        |
| Töö 3 | 6 / 3   | 2 tundi        |

## <a name="net-time-allocation-key"></a>Netoaja eraldusvõti
Järgnev tabel illustreerib eraldatud aja arvutamise valemit. Siin on valem: arvutatud aeg aruande kohta = kogumiaeg / tööde arv

|                              | 9.00–10.00 (1 tund) | 10.00–11.00 (1 tund) | 11.00–13.00 (2 tundi) | 13.00–15.00 (2 tundi) | Eraldatud aeg |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Kogumi tööde arv | 1                    | 3                    | 2                     | 1                     | Pole kohaldatav |
| Töö 1                        | 1 / 1 = 1 tund       | 1 / 3 = 0,33 tundi    | Pole kohaldatav        | Pole kohaldatav        | 1,33 tundi     |
| Töö 2                        | Pole kohaldatav       | 1 / 3 = 0,33 tundi    | 2 / 2 = 1 tund        | Pole kohaldatav        | 1,33 tundi     |
| Töö 3                        | Pole kohaldatav       | 1 / 3 = 0,33 tundi    | 2 / 2 = 1 tund        | 2 / 1 = 2 tundi       | 3,33 tundi     |

## <a name="real-time-allocation-key"></a>Reaalaja eraldusvõti
Kui soovite tootmiskulusid tegelike kulude põhjal arvutada, peate tühjendama leheküljel **Tootmistellimuse vaikesätted** suvandi **Kulukategooria**. Järgnev tabel illustreerib eraldatud aja arvutamise valemit. Siin on valem: töö tegelik aeg = tegelik aeg kogumis

| Töö   | Tegelik aeg |
|-------|-------------|
| Töö 1 | 2 tundi     |
| Töö 2 | 3 tundi     |
| Töö 3 | 5 tundi     |

Arvestage, et neid kolme tööd sooritab töötaja, kelle tunnitasu on 12,00 USA dollarit. Töödele kulutatud ajal ületunnitöö eest lisatasu ega preemiat ei teenitud. Töötaja on kulutanud kolme kogumisse seotud töö tegemiseks kokku kuus tundi. Seega on palgakulu 6 x 12,00 = 72,00 USA dollarit. Kui kasutate reaalaja eraldust, kasutatakse tunni kulude ümber arvutamisel valemist Netoaeg pärit tegurit. Seejärel kantakse iga töö peale kulutatud tegelik aeg üle koos juba korrigeeritud tunnihinnaga. Selles näites kulutati kuus tundi, ehkki eraldatud oli kümme tundi. Järgnev tabel illustreerib kulu arvutamise valemit. Siin on valem: tunni kulu = (töö kogu kogumiaeg (netoaeg) / töö tegelik aeg) x tunni standardne omahind

| Töö   | Korrigeeritud tunnikulu arvutamine | Korrigeeritud tunnikulu | Eraldatud aeg | Töö kogukulu |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| 1. töö | (1,33 / 2) x 12,00 USA dollarit                 | 8,00 USA dollarit                | 2 tundi        | 16,00 USA dollarit         |
| 2. töö | (1,33 / 3) x 12,00 USA dollarit                 | 5,33 USA dollarit                | 3 tundi        | 16,00 USA dollarit         |
| 3. töö | (3,33 / 5) x 12,00 USA dollarit                 | 8,00 USA dollarit                | 5 tundi        | 40,00 USA dollarit         |

Korrigeeritud kulu tunni kohta ja töö aeg sisestatakse tootmise töölehele. **Märkus.** Kui valite lehekülje **Tootmistellimuse vaikesätted** vahekaardil **Üldine** suvandi **Kulukategooria** kantakse töö tegemiseks kulunud tegelik aeg tootmise töölehele, kus kulu määratakse kindla töö kulukategooriale.



