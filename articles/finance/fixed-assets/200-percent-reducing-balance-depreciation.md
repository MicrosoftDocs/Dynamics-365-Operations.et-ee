---
title: 200 protsenti väheneva saldoga kulum
description: See artikkel annab ülevaate 200-protsendise vähenevsaldo kulumimeetodist.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7abcf26f3e658e8a6f451f26240890d183547982
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870158"
---
# <a name="200-percent-reducing-balance-depreciation"></a>200 protsenti väheneva saldoga kulum

[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate 200-protsendise vähenevsaldo kulumimeetodist.

Kui valite põhivara kulumireeglite seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **200% vähenev saldo**, on sellele kulumireeglile määratud põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune. Protsendimäära arvutamise aluseks on põhivara tööiga. Nt kui põhivara kasulik eluiga on viis aastat, arvutatakse perioodi kulumiks 40 protsenti (200% ÷ 5). 

Seda meetodit tuntakse ka kahekordselt väheneva kulumina.

200% väheneva saldoga kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**. Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.

## <a name="select-a-depreciation-year"></a>Kulumiaasta valimine
Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**. Vaikeväärtus on **Kalendriaasta**. 

Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid. See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.

### <a name="calendar"></a>Kalender

Võite säilitada vaikeväärtuse väljal **Kulumiarvestusaasta** jaotises **Kalendriaasta**. 

Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril. Kulumiarvestus on tavaliselt raamatupidamislik jääkväärtus miinus mahakandemaksumus. Selles artikli näites on kulumiarvestuse alus arvutusveeru avaldise esimeseks lugejaks. 

Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.

-   **Kord aastas** sisestab summa 31. detsembril.
-   **Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.
-   **Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).
-   **Kord poolaastas** poolaasta kulumisumma sisestatakse poolaasta lõpus (30. juunil ja 31. detsembril).
-   **Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.

### <a name="fiscal"></a>Fiskaalne

Kui valite väljal **Kulumiaasta** suvandi **Rahandusaasta**, arvutatakse 200% väheneva jääkväärtuse kulumist rahanduskalendri rahandusaasta alusel, mis on määratud raamatule, või rahanduskalendri alusel, mis on valitud lehel **Pearaamat**. Rahanduskalendrid seadistatakse lehel **Rahanduskalendrid**. 

Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil. Rahandusaasta võib olla pikem või lühem kui 12 kuud. Iga perioodi kulumit korrigeeritakse. Järgmise rahandusaasta pikkuse määravad perioodid, mis on seadistatud lehel **Rahanduskalendrid**. 

Kui valite kulumiarvestusaastaks **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.

-   **Kord aastas** sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.
-   **Rahandusperiood** sisestab rahandusaasta kohta arvutatud kulumi kogusumma. See summa on jagatud rahandusperioodideks, mis on määratletud lehel **Rahanduskalendrid**.

## <a name="example-of-200-reducing-balance-depreciation"></a>200% väheneva saldoga kulumi näide

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| Soetusmaksumus               | 11 000 |
| Jääkväärtus                  | 1000 |
| Kulumiarvestuse alus              | 10 000 |
| Kasutusea aastad             | 5      |
| Kulumiprotsent aastas | 40%    |

200% väheneva saldo meetod jagab 200 protsenti kasutusea aastatega. See protsendimäär korrutatakse aasta kulumisumma kindlaksmääramiseks põhivara raamatupidamisliku jääkväärtusega.

| Periood | Aasta kulumisumma arvutamine | Arvestuslik väärtus             | Raamatupidamislik jääkväärtus aasta lõpus |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| aasta 1 | (11 000 – 1000) × 40% = 4000                | 11 000 – 4000 = 7000 | 11 000 – 1000 – 4000 = 6000        |
| aasta 2 | 6000 × 40% = 2400                           | 7000 – 2400 = 4600  | 6000 – 2400 = 3600                 |
| aasta 3 | 3600 × 40% = 1440                           | 4600 – 1440 = 3160  | 3600 – 1440 = 2160                 |

> [!NOTE] 
> Tavaliselt kui 200% väheneva saldo kulumiarvestusmeetodiga arvutatud summa on väiksem kui lineaarse meetodiga arvutades tulemuseks olev summa, teisendatakse järelejäänud eluiga lineaarse meetodi järgi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
