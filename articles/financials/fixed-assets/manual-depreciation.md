---
title: Käsitsi kulumiarvestus
description: Selles artiklis antakse ülevaade käsitsi rakendatavast kulumiarvestusmeetodist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840309"
---
# <a name="manual-depreciation"></a>Käsitsi kulumiarvestus

[!include [banner](../includes/banner.md)]

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

Kui valite <strong>Kord poolaastas</strong> *<strong>väljalt<em>Perioodi sagedus</em>*</strong>, seadistate kaks käsitsi graafikuintervalli. Järgmine tabel näitab nende kahe intervalli kulumisummasid.

| Intervall    | Kulumisumma            |
|-------------|--------------------------------|
| 30. juuni     | (11 000 – 1000) × 10% = 1000 |
| 31. detsember | (11 000 – 1000) × 50% = 5000 |

Kõigi intervallide protsentide kogusumma ei pea olema 100. Kuid saate teate, kui väärtus väljal **Kumulatiivne protsent** lehel **Põhivara kulumireeglite graafikud** ei ole **100**.



