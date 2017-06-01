---
title: "Allesjäänud eluea lineaarne kulum"
description: "Selles artiklis antakse ülevaade kulumiarvestusmeetodist Allesjäänud lineaarne eluiga."
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
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 765825ba43cad44b076ea6628d2787011e97fc57
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="straight-line-life-remaining-depreciation"></a>Allesjäänud eluea lineaarne kulum

[!include[banner](../includes/banner.md)]


Selles artiklis antakse ülevaade kulumiarvestusmeetodist Allesjäänud lineaarne eluiga.

Kui seadistate põhivara kulumireegli ja valite lehe **Kulumireeglid** väljal **Meetod** suvandi **Allesjäänud lineaarne eluiga**, siis põhineb kulumireeglile määratud põhivarade tarbimiskulum põhivara järelejäänud tööeal. Tavaliselt on sel juhul kõigi kulumiperioodide kulumisumma ühesuurune. Allesjäänud eluea lineaarne kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**. Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.

## <a name="select-a-depreciation-year"></a>Kulumiaasta valimine
Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**. Vaikeväärtus on **Kalendriaasta**. Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid. See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.

### <a name="calendar"></a>Kalender

Kui valite suvandi **Kalender** väljal ***Kulumiaasta***, arvestatakse aastana perioodi 1. jaanuarist kuni 31. detsembrini, isegi kui olete rahanduskalendri teisiti määratlenud. Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril. Kulumiarvestuse alus on tavaliselt raamatupidamislik jääkväärtus miinus jääkväärtus. Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige. Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.

-   **Kord aastas** sisestab summa 31. detsembril.
-   **Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.
-   **Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).
-   **Kord poolaastas** iga poolaasta lõpus (30. juunil ja 31. detsembril) poole aasta summa sisestamine.
-   **Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.

Näiteks suvandi **Kord aastas** valimisel sisestatakse aasta kulum ainult üks kord iga aasta 31. detsembril. Suvandi **Kord kuus** valimisel sisestatakse kulum igal kuul kui 1/12 aasta kulumisummast.

### <a name="fiscal"></a>Fiskaalne

Kuiv alite väljal **Kulumiarvestusaasta** suvandi **Rahandusaasta**, kasutatakse allesjäänud eluea lineaarset kulumit. Kulum arvutatakse järelejäänud rahandusaastate alusel. Näiteks finantsaastal 1. juulist 2015 kuni 30. juunini 2016 käivitub kulumiarvestus 1. juulil. Rahandusaasta võib olla pikem või lühem kui 12 kuud. Iga rahandusperioodi kulumit korrigeeritakse. Järgmise rahandusaasta pikkuse määravad rahandusperioodid, mis on seadistatud lehel **Rahanduskalendrid**. Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.

-   **Kord aastas** sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.
-   **Rahandusperiood**arvutab rahandusaasta kulumi kogusumma. See summa kogutakse siis rahandusperioodidesse, mis on määratletud lehel **Rahaduskalendrid** raamatu jaoks määratud rahanduskalendri jaoks.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Muutmata põhivara lineaarse kulumi näide
Põhivaral on järgmised näitajad.

|                     |        |
|---------------------|--------|
| Soetusmaksumus    | 11 000 |
| Jääkväärtus       | 1000  |
| Kulumiarvestuse alus   | 10 000 |
| Kasutusea aastad  | 5      |
| Aastane kulumisumma | 2 000  |

Kulumisumma on igal aastal sama: (soetusmaksumus – jääkväärtus) ÷ kasuliku eluea aastad

| Periood | Aasta kulumisumma arvutamine | Raamatupidamislik jääkväärtus aasta lõpus |
|--------|-----------------------------------------------|---------------------------------------|
| aasta 1 | (11 000 – 1000) ÷ 5 = 2000                  | 9000                                 |
| aasta 2 | (9000 – 1000) ÷ 4 = 2000                   | 7 000                                 |
| aasta 3 | (7000 – 1000) ÷ 3 = 2000                   | 5 000                                 |
| aasta 4 | (5000 – 1000) ÷ 2 = 2000                   | 3 000                                 |
| aasta 5 | (3000 – 1000) ÷ 1 = 2000                   | 1000                                 |






