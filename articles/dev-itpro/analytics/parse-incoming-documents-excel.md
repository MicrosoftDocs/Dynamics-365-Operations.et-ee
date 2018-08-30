---
title: "Sissetulevate dokumentide sõelumine Excelis vormingus"
description: "Selles teemas selgitatakse elektroonilise aruandluse vormingute kujundamist sissetulevates Microsoft Exceli failides oleva sisu sõelumiseks."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 32fd82f0e46068c7ed7bfcfddc4ff84603bd20b4
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="parse-incoming-documents-in-excel-format"></a>Sissetulevate dokumentide sõelumine Excelis vormingus

[!include[banner](../includes/banner.md)]

Saate kujundada elektroonilise aruandluse vormingud sõeluma sissetulevaid Microsoft Exceli faile, mis esitavad andmeid Microsoft Exceli töövihikutes (XLSX-vormingus failid). Seejärel saate neist failidest pärit sisu kasutada rakenduse andmete värskendamiseks. See on kasulik järgmistel juhtudel.

- Uue mudeli ja vormingu kujundamine, testides neid käitusajal. Sellisel juhul simuleerib Excel tegelikke rakenduse andmeid.
- Lisaks rakenduse Exceli andmete haldamiseks ja soovite importida kindla aruande andmed.

Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusejuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (1. osa: vormingu kujundamine)** ja **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (2. osa: andmete importimine)** (osad äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)). Need tegevusejuhised selgitavad, kuidas saab sissetulevat Exceli faili elektroonilise aruandluse vormingu abil sõeluda, et importida teavet sissetulevatest dokumentidest ja värskendada rakenduse andmeid. Saate tegevusejuhise failid alla laadida [Microsofti allalaadimiskeskusse](https://go.microsoft.com/fwlink/?linkid=874684).

Eespool nimetatud tegevusejuhiste lõpuleviimiseks laadige alla järgmised failid.

| Sisu kirjeldus                         | Fail                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Sissetulev fail XLSX-vormingus – mall    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Sissetulev fail XLSX-vormingus – näidisandmed | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Kui te pole järgmist tegevusejuhist, [Elektrooniline aruandlus: nõutud konfiguratsioonide loomine andmete importimiseks välisest failist](./tasks/er-required-configurations-import-data.md), praeguses rakenduses Dynamics 365 for Finance and Operation veel vaadanud, laadige alla järgmine fail.

| Sisu kirjeldus    | Fail                                                            |
|------------------------|-----------------------------------------------------------------|
| Elektroonilise aruandluse mudeli konfiguratsioon | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |

