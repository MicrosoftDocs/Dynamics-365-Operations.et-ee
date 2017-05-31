---
title: "Käsitsi kulumiarvestus"
description: "Selles artiklis antakse ülevaade käsitsi rakendatavast kulumiarvestusmeetodist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 75d176623b4fdf2198440becd0345628f873f6da
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="manual-depreciation"></a>Käsitsi kulumiarvestus

[!include[banner](../includes/banner.md)]


Selles artiklis antakse ülevaade käsitsi rakendatavast kulumiarvestusmeetodist.

Kui teete põhivara kulumireeglite seadistamisel valiku **Käsitsi** väljal **Meetod** lehel **Kulumireeglid**, määratletakse selle kulumireegliga põhivarade kulum kalendriaasta intervallidele sisestatud protsendimääraga. Intervallid, millele protsendimäärad seadistate, sisestatakse väärtuse järgi, mille valite väljal **Perioodi sagedus** kiirkaardil **Üldine** lehel **Kulumireeglid**. Siin on väärtused, mida valida saate.

-   Kord aastas
-   Kord kuus
-   Kord kvartalis
-   Kord poolaastas
-   Kord päevas

Pärast perioodi sageduse valimist klõpsake valikut **Käsitsi koostatud graafikud** ja seadistage kõigi sisestusintervallide protsendimäärad. Käsitsi koostatud graafikud koos sisestusintervallidega määratlevad kulumisumma, nagu selles artiklis antud näidetest näha võib. Käsitsi sisestatud kulumid arvutatakse alati protsendina soetusmaksumusest. Käsitsi sisestatud kulumi puhul ei pea teie poolt kulumiintervallidele sisestatavate protsendimäärade summa olema 100 protsenti. Käsitsi kulumiarvestus on paindlik kulumiarvestusmeetod, mida kasutatakse sageli erakorralise kulumireegli määratlemiseks lehel **Raamatud**, nt mitteperioodiline kulum erieesmärkidel.

## <a name="examples"></a>Näited
Soetusmaksumus: 11 000.00 Eeldatav mahakandmismaksumus: 1000.00 Järgmises tabelis on näidatud intervallid ja protsendid, mille saab seadistada lehel **Põhivara kulumireeglite graafikud**.

| Intervalli number | Protsent |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8.00       |

Järgmises tabelis on näidatud, kuidas iga intervalli kulum arvutatakse.

|  Intervalli number | Aasta kulumisumma arvutamine | Raamatupidamislik jääkväärtus intervalli lõpus |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11 000 – 1000) × 10% = 1000                | 10 000 (11 000 – 1000)                   |
| 2                | (11 000 – 1000) × 50% = 5000                | 5000 (10000 – 5000)                    |
| 3                | (11 000 – 1000) × 8% = 800                   | 4200 (5000 – 800)                       |

Kui teete valiku **Igakuine** väljal**Perioodi sagedus**, seadistate 12 käsitsi graafikuintervalli. Järgmine tabel näitab kahe esimese intervalli kulumisummasid.

| Intervall | Kulumisumma            |
|----------|--------------------------------|
| Jaanuar  | (11 000 – 1000) × 10% = 1000 |
| Veebruar | (11 000 – 1000) × 50% = 5000 |

Kui valite **Kord poolaastas** väljalt ****Perioodi sagedus** **, seadistate kaks käsitsi graafikuintervalli. Järgmine tabel näitab nende kahe intervalli kulumisummasid.

| Intervall    | Kulumisumma            |
|-------------|--------------------------------|
| 30. juuni     | (11 000 – 1000) × 10% = 1000 |
| 31. detsember | (11 000 – 1000) × 50% = 5000 |

Kõigi intervallide protsentide kogusumma ei pea olema 100. Kuid saate teate, kui väärtus väljal **Kumulatiivne protsent** lehel **Põhivara kulumireeglite graafikud** ei ole **100**.




