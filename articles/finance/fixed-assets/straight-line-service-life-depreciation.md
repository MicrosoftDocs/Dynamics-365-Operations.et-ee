---
title: Kasuliku eluea lineaarne kulum
description: Selles artiklis antakse ülevaade kulumiarvestusmeetodist Lineaarne kasulik eluiga.
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5853265492edc88acbbd297bc5cb639b46fa0b41
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210067"
---
# <a name="straight-line-service-life-depreciation"></a>Kasuliku eluea lineaarne kulum

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade kulumiarvestusmeetodist Lineaarne kasulik eluiga.

Kui seadistate põhivara kulumireegli ja valite lehe Kulumireeglid väljal Meetod suvandi Tööeapõhine lineaarne, arvutatakse varad, millele on määratud see kulumiprofiil, vara kogu tööea põhjal. Tavaliselt on sel juhul kõigi kulumiperioodide kulumisumma ühesuurune. 

Erinevus allesjäänud tööea lineaarse kulumi ja tööea lineaarse kulumi puhul arvutatud kulumisummade vahel tekib, kui põhivarale on sisestatud korrektsioon. 

Tööea lineaarse kulumi seadistamiseks peate valima ka suvandid lehe Kulumireeglid väljadel Kulumiaasta ja Perioodi sagedus.

## <a name="select-a-depreciation-year"></a>Kulumiaasta valimine
Saate lehe Kulumireeglid väljalt Kulumiarvestusaasta valida kas suvandi Kalender või Rahandusaasta. Valik määratleb väljal Perioodi sagedus saadaolevad suvandid. Vaikesuvandiks on Kalender.

### <a name="calendar"></a>Kalender

Kui valite suvandi Kalender, arvestatakse aastana perioodi 1. jaanuarist kuni 31. detsembrini, isegi kui olete määratlenud rahanduskalendri teisiti. 

Suvandiga Kalender värskendatakse iga aasta 1. jaanuaril kulumiarvestuse alust, mis on tavaliselt raamatupidamislik jääkväärtus miinus likvideerimisväärtus. Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige. 

Valides suvandi Kalender on teil kalendriaasta kulumisumma jaotust ja selle sisestuskuupäevi määratleval väljal Perioodi sagedus saadaval järgmised suvandid.
-   Sisestamine kord aastas (31. detsembril).
-   Kord kuus sisestab igakuise summa iga kalendrikuu lõpus.
-   Kord kvartalis sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).
-   Kord poolaastas (iga poolaasta lõpus, 30. juunil ja 31. detsembril) poole aasta summa sisestamine.
-   Kord päevas sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.

Näiteks suvandi Kord aastas valimisel sisestatakse aasta kulum ainult üks kord iga aasta 31. detsembril. Suvandi Kord kuus valimisel sisestatakse kulum igal kuul kui 1/12 aasta kulumisummast.

### <a name="fiscal"></a>Fiskaalne

Kui valite väljal Kulumiarvestusaasta suvandi Rahandusaasta, kasutatakse lineaarset tööea kulumit. See arvutatakse raamatu jaoks määratud rahanduskalendriga või lehel Pearaamat valitud rahanduskalendriga määratletud rahandusaasta põhjal. Rahanduskalendrid seadistatakse lehel Rahanduskalendrid.

Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil. Rahandusaasta võib olla pikem või lühem kui 12 kuud. Iga rahandusperioodi kulumit korrigeeritakse automaatselt. Järgmise rahandusaasta pikkus põhineb rahandusperioodidel, mille seadistate vormil Rahanduskalendrid uue rahandusaasta loomisel. 

Rahandusaasta valimisel on väljal Perioodi sagedus saadaval järgmised suvandid.
-   Kord aastas sisestatakse rahandusaasta kohta arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.
-   Rahandusperiood arvutab rahandusaasta kulumi kogusumma, mis on jagatud vormil Rahanduskalendrid rahanduskalendri jaoks määratletud perioodideks.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Näide. Muutmata põhivara lineaarne kulum
Oletame, et põhivaral on järgmised näitajad.

|                     |        |
|---------------------|--------|
| Soetusmaksumus    | 11 000 |
| Jääkväärtus       | 1000  |
| Kulumiarvestuse alus   | 10 000 |
| Kasutusea aastad  | 5      |
| Aastane kulumisumma | 2 000  |

Saate sama kulumisumma igal aastal: (soetusmaksumus - mahakandmismaksumus) / kasuliku eluea aastad

| Periood | Aasta kulumisumma arvutamine | Raamatupidamislik jääkväärtus aasta lõpus |
|--------|-------------------------------------------|---------------------------------------|
| aasta 1 | (11 000 – 1000) / 5 = 2000              | 9000                                 |
| aasta 2 | (11 000 – 1000) / 5 = 2000              | 7000                                 |
| aasta 3 | (11 000 – 1000) / 5 = 2000              | 5000                                 |
| aasta 4 | (11 000 – 1000) / 5 = 2000              | 3 000                                 |
| aasta 5 | (11 000 – 1000) / 5 = 2000              | 1000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a> Näide. Muudetud põhivara lineaarne kulum

Oletame, et lisate 2. aastal samale põhivarale soetuse korrigeerimise summas 4000. 

Soetuse korrigeerimise tööiga on sama mis põhivaral ning algab põhivara soetamisest. Raamatupidamislik jääkväärtus aasta 5 lõpus säilib, vastavalt soetuse korrigeerimise raamatupidamislikule jääkväärtusele. Perioodide kulumi arvutamist vt järgmisest tabelist.

| Periood | Aasta kulumisumma arvutamine | Raamatupidamislik jääkväärtus aasta lõpus |
|--------|-------------------------------------------|---------------------------------------|
| aasta 1 | 10 000 / 5 = 2000                        | 11 000 – 2000 = 9000                |
| aasta 2 | 4000 (soetuse korrigeerimine)            | 9000 + 4000 =13 000                 |
| aasta 2 | 14 000 / 5 = 2800                        | 13 000 – 2800 = 10 200               |
| aasta 3 | 14 000 / 5 = 2800                        | 10 200 – 2800 = 7400                |
| aasta 4 | 14 000 / 5 = 2800                        | 7400 – 2800 = 4600                 |
| aasta 5 | 14 000 / 5 = 2800                        | 4600 – 2800 = 1800                 |
| aasta 6 | Jääksumma 800\*                           | 1800 – 800 = 1000                   |

\*Kuna jääksumma on kulumisummast väiksem, võetakse arvesse ainult jääksumma ilma jääkväärtuseta.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]