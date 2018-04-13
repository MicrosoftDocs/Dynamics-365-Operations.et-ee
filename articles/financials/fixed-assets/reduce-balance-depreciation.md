---
title: "Väheneva jääkväärtuse kuluarvestusmeetod"
description: "Selles artiklis antakse ülevaade väheneva kulumiarvestusmeetodi kohta."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29bc8cd02d98479197d7e5f5664b9859c03893b3
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="reduce-balance-depreciation"></a>Väheneva jääkväärtuse kuluarvestusmeetod

[!INCLUDE [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade väheneva kulumiarvestusmeetodi kohta.

Kui valite põhivara kulumireeglite seadistamisel lehe Kulumireeglid väljal Meetod suvandi Vähenev saldo, on selle kulumireegliga põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune.

Väheneva saldoga kulumireegli seadistamiseks tuleb teil teha valikud ka lehe Kulumireeglid kiirkaardi Üldine väljadel. Kõigepealt valige aasta väljal Kulumiarvestusaasta. Valikust olenevalt kuvatakse väljal Perioodi sagedus erinevad väärtused, nagu selgitatakse järgmistes jaotistes. 

Samuti tuleb teil sisestada kulumireegli puhul väärtus väljale Protsent. Valiku Täielik kulum puhul võetakse viimasel kulumiperioodil aluseks allesjäänud kulum ja selleks võib olla väga suur summa. Osades riikides/regioonides ei kasutata ümberlülitust lineaarsele meetodile. Ümberlülitus ilmneb, kui alternatiivse kulumimeetodi summa on algsest kulumireegli summast suurem või sellega võrdne ja arvestatakse alternatiivse meetodi summat. 

Kuna protsendiarvutuste alusel ei saa põhivara kunagi täielikult amortiseerida, tuleb põhivara täielikuks amortiseerimiseks kasutada valikut Täielik kulum.

## <a name="select-a-depreciation-year"></a>Kulumiaasta valimine
Saate lehe Kulumireeglid väljalt Kulumiarvestusaasta valida kas suvandi Kalender või Rahandusaasta. Valik määratleb väljal Perioodi sagedus saadaolevad suvandid. Vaikesuvandiks on Kalender.

### <a name="calendar"></a>Kalender

Suvandiga Kalender värskendatakse iga aasta 1. jaanuaril kulumiarvestuse alust, milleks on tavaliselt raamatupidamislik jääkväärtus miinus mahakandmismaksumus. Selles teemas hiljem esinevas väheneva saldoga kulumi näites on kulumiarvestuse alus arvutusveeru avaldise esimeseks liikmeks. 

Valides suvandi Kalender on teil kalendriaasta kulumisumma jaotust ja selle sisestuskuupäevi määratleval väljal Perioodi sagedus saadaval järgmised suvandid.

-   Kord aastas sisestatakse 31. detsembril.
-   Kord kuus sisestab igakuise summa iga kalendrikuu lõpus.
-   Kord kvartalis sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).
-   Kord poolaastas sisestab kulumisumma iga poolaasta lõpus (30. juunil ja 31. detsembril).
-   Kord päevas sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.

Näiteks suvandi Kord aastas valimisel sisestatakse aasta kulum ainult üks kord iga aasta 31. detsembril. Suvandi Kord kuus valimisel sisestatakse kulum igal kuul kui 1/12 aasta kulumisummast.

### <a name="fiscal"></a>Fiskaalne

Kui valite väljal Kulumiarvestusaasta suvandi Rahandusaasta, kasutatakse lineaarset kulumimeetodit. See arvutatakse rahandusaasta põhjal, mis seadistatakse lehel Rahanduskalendrid lehel Pearaamat valitud rahanduskalendri puhul. Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil. Rahandusaasta võib olla pikem või lühem kui 12 kuud. Iga rahandusperioodi kulumit korrigeeritakse. Järgmise rahandusaasta pikkus põhineb rahandusperioodidel, mille seadistate lehel Rahanduskalendrid uue rahandusaasta loomisel.


Rahandusaasta valimisel on väljal Perioodi sagedus saadaval järgmised suvandid.

-   Kord aastas sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.
-   Rahandusperiood sisestab arvutatud kulumi kogusumma rahandusaasta puhul, mis on jagatud rahandusperioodideks, mis on määratletud lehel Pearaamat valitud rahanduskalendrile või põhivara raamatu jaoks valitud rahanduskalendrile.

## <a name="example-of-reducing-balance-depreciation"></a>Väheneva saldoga kulumi näide

Oletagem, et põhivara soetamisväärtus on 11 000, mahakandemaksumus on 1000 ja kulumi teguriks on protsendimäär 30. 

Kasutades väheneva saldo meetodit, arvutatakse 30 protsenti kulumialusest (raamatupidamislik jääkväärtus miinus mahakandmismaksumus) eelmise kulumiarvestusperioodi lõpus. Esimese kolme aasta kulumit näidatakse järgmises tabelis.

| Periood | Aasta kulumisumma arvutamine | Raamatupidamislik jääkväärtus aasta lõpus |
|--------|-------------------------------------------|---------------------------------------|
| aasta 1 | (11 000 – 1 000) \* 30% = 3000           | (11 000 – 1000) – 3000 = 7000      |
| aasta 2 | (7000 – 1000) \* 30% = 1800            | (7000 – 1800) = 5200                |
| aasta 3 | (5200 – 1000) \* 30% = 1260            | (5200 – 1260) = 3940               |


-






