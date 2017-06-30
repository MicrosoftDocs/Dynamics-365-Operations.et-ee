---
title: "175 protsenti väheneva saldoga kulum"
description: "Selles artiklis antakse ülevaade 175% väheneva jääkväärtuse kulumiarvestusmeetodi kohta."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 40bbb07deb455d922244fc3856871cda7107543e
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="175-percent-reducing-balance-depreciation"></a>175 protsenti väheneva saldoga kulum

[!include[banner](../includes/banner.md)]


Selles artiklis antakse ülevaade 175% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.

Kui valite põhivara kulumireeglite seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **175% vähenev saldo**, on sellele kulumireeglile määratud põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune. 

175% väheneva saldoga kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**. Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.

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

Kui valite väljal **Kulumiaasta** suvandi **Rahandusaasta**, arvutatakse 175% väheneva jääkväärtuse kulumist rahanduskalendri rahandusaasta alusel, mis on määratud raamatule, või rahanduskalendri alusel, mis on valitud lehel **Pearaamat**. Rahanduskalendrid seadistatakse lehel **Rahanduskalendrid**. Lisateavet leiate teemast [Rahanduskalendrid, rahandusaastad ja -perioodid.](..\budgeting\fiscal-calendars-fiscal-years-periods.md).

Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil. Rahandusaasta võib olla pikem või lühem kui 12 kuud. Kulumit korrigeeritakse iga perioodi puhul automaatselt ja järgmise rahandusaasta pikkuse määrab perioodide seadistus lehel **Rahanduskalendrid**. 

Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.

-   **Kord aastas** rahandusaasta alusel arvestatud kulumisumma sisestatakse ühe summana rahandusaasta viimasel kuupäeval.
-   **Rahandusperiood** arvutab rahandusaasta kulumi kogusumma. See summa on jagatud rahandusperioodideks, mis on määratletud lehel **Rahanduskalendrid**.

## <a name="example-of-175-reducing-balance-depreciation"></a>175% väheneva saldoga kulumireegli näide
|                                |        |
|--------------------------------|--------|
| Soetusmaksumus               | 11 000 |
| Jääkväärtus                  | 1000  |
| Kulumiarvestuse alus              | 10 000 |
| Kasutusea aastad             | 5      |
| Kulumiprotsent aastas | 35%    |

175% väheneva jääkväärtuse kulumiarvestusmeetod jagab 175 protsenti kasutusea aastatega. See protsendimäär korrutatakse aasta kulumisumma kindlaksmääramiseks põhivara raamatupidamisliku jääkväärtusega.

| Periood | Aasta kulumisumma arvutamine | Arvestuslik väärtus                  | Raamatupidamislik jääkväärtus aasta lõpus |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| aasta 1 | (11 000 – 1000) × 35% = 3500                | 11 000 – 3500 = 7500      | 11 000 – 1000 – 3500 = 6500        |
| aasta 2 | 6500 × 35% = 2275                           | 7,500 – 2,275 = 5,225       | 6500 – 2275 = 4225                 |
| aasta 3 | 4225 × 35% = 1478.75                        | 5225 – 1478.75 = 3746.25 | 4225 – 1478.75 = 2746.25           |

> [!NOTE] 
> Tavaliselt kui 175% väheneva saldo kulumiarvestusmeetodiga arvutatud summa on väiksem kui lineaarse meetodiga arvutades tulemuseks olev summa, teisendatakse järelejäänud eluiga lineaarse meetodi järgi.




