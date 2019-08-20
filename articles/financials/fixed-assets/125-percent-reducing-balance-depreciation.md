---
title: 125 protsenti väheneva saldoga kulum
description: Selles artiklis antakse ülevaade 125% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.
author: saraschi2
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5af050fb6099b583be4e9c60ba56dacf38d31c08
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840861"
---
# <a name="125-percent-reducing-balance-depreciation"></a>125 protsenti väheneva saldoga kulum

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade 125% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.

Kui valite põhivara kulumireeglite seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **125% vähenev saldo**, on sellele kulumireeglile määratud põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune. Selle protsendimäära arvutamise aluseks on põhivara tööiga. Nt kui põhivara kasulik eluiga on viis aastat, arvutatakse perioodi kulumiks 25 protsenti (125% ÷ 5).

125% väheneva saldoga kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**. Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.

## <a name="select-a-depreciation-year"></a>Kulumiaasta valimine
Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**. Vaikeväärtus on **Kalendriaasta**. 

Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid. See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.

### <a name="calendar"></a>Kalender

Võite säilitada vaikeväärtuse väljal **Kulumiarvestusaasta** jaotises **Kalendriaasta**. 

Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril. Kulumiarvestuse alus on tavaliselt raamatupidamislik jääkväärtus miinus mahakandemaksumus. Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige. 

Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.

-   **Kord aastas** sisestab summa 31. detsembril.
-   **Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.
-   **Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).
-   **Kord poolaastas** poolaasta kulumisumma sisestatakse poolaasta lõpus (30. juunil ja 31. detsembril).
-   **Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.

### <a name="fiscal"></a>Fiskaalne

Kui valite väljal **Kulumiaasta** suvandi **Rahandusaasta**, arvutatakse 125% vähenevast kulumist rahanduskalendri rahandusaasta alusel, mis on määratud raamatule, või rahanduskalendri alusel, mis on valitud lehel **Pearaamat**. Rahanduskalendrid seadistatakse lehel **Rahanduskalendrid**. 

Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil. Rahandusaasta võib olla pikem või lühem kui 12 kuud. Kulumit korrigeeritakse iga perioodi puhul automaatselt ja järgmise rahandusaasta pikkuse määrab perioodide seadistus lehel **Rahanduskalendrid**. 

Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.

-   **Kord aastas** sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.
-   **Rahandusperiood** sisestab rahandusaasta kohta arvutatud kulumi kogusumma. See summa on jagatud rahandusperioodideks, mis on määratletud lehel **Rahanduskalendrid**.

## <a name="example-of-125-reducing-balance-depreciation"></a>125% väheneva saldoga kulumireegli näide

|                                |        |
|--------------------------------|--------|
| Soetusmaksumus               | 11 000 |
| Jääkväärtus                  | 1000  |
| Kulumiarvestuse alus              | 10 000 |
| Kasutusea aastad             | 5      |
| Kulumiprotsent aastas | 25%    |

125% väheneva saldo meetod jagab 125 protsenti kasutusea aastatega. See protsendimäär korrutatakse aasta kulumisumma kindlaksmääramiseks põhivara raamatupidamisliku jääkväärtusega.

| Periood | Aasta kulumisumma arvutamine | Arvestuslik väärtus                    | Raamatupidamislik jääkväärtus aasta lõpus |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| aasta 1 | (11 000 – 1000) × 25% = 2500                | (11 000 – 2500) = 8500      | (11 000 – 1000 – 2500) = 7500      |
| aasta 2 | 7500 × 25% = 1875                           | (8500 – 1875) = 6625       | (7500 – 1875) = 5625               |
| aasta 3 | 5625 × 25% = 1406,25                        | (6625 – 1406,25) = 5218,75 | (5625 – 1406,25) = 4218,75         |

> [!NOTE] 
> Tavaliselt kui 125% väheneva saldo kulumiarvestusmeetodiga arvutatud summa on väiksem kui lineaarse meetodiga arvutades tulemuseks olev summa, teisendatakse järelejäänud eluiga lineaarse meetodi järgi.



