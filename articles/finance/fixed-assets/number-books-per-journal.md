---
title: Raamatute arv töölehe kohta
description: Selles teemas kirjeldatakse seost töölehtede ja vararaamatute vahel, kui loote põhivara soetamise või kulumisoovituse pakett-töö kaudu. Saate määratleda iga soetamise ja kulumi jaoks kaasatud raamatute maksimaalse arvu.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d4ba98cefdc0b555eedfaa56b6a3ca4870b5de93
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650656"
---
# <a name="number-of-books-per-journal"></a>Raamatute arv töölehe kohta

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse seost töölehtede ja vararaamatute vahel, kui loote põhivara soetamise või kulumisoovituse pakett-töö kaudu. Saate määratleda iga soetamise ja kulumi jaoks kaasatud raamatute maksimaalse arvu, kasutades välju vahekaardi **Üldine** jaotises **Raamatute arv töölehe kohta** lehel **Põhivara parameetrid** (**Põhivara \> Seadistamine \> Põhivara parameetrid**). Need väljad võimaldavad teil jaotada vararaamatute arvu soetuse töölehe ja kulumi töölehe kohta.

Soetussoovituse puhul on vaikeväärtuseks vähemalt 10 000 raamatut. Kulumisoovituse puhul on vaikeväärtuseks vähemalt 2000 raamatut.

Näiteks kui on 4000 põhivara ja kaks raamatut on seotud iga varaga, sisestatakse üks raamat praegusele kihile ja teine raamat sisestatakse maksukihile. Kui soetate 4 000 põhivara pakktöötluse kaudu, sisaldab pakett-töö, mis loob ühe põhivara soetamise töölehe, 4000 vara raamatut.

> [!NOTE]
> Loodud töölehte kasutatakse jätkuvalt, kuni pakett-töö on lõpetatud.
>
> Tuletatud raamatuid ei kaasata maksimaalsesse raamatute arvu töölehe kohta.

Saate kasutada pakktöötlust, et käitada kulum samale soetatud varade kogumile. Näiteks loob pakett-töö kaks kulumi töölehte, millest kumbki koosneb 2000st vararaamatust. Esimene tööleht sisaldab raamatuid, mis on seotud põhivaradega, mis on nummerdatud 1 kuni 2000. Teine tööleht sisaldab siis raamatuid, mis on seotud põhivaradega, mis on nummerdatud 2001 kuni 4000.

Pakett-töötluse töö välistab suletud raamatud. Näiteks pakett-töös kulumi puhul suletakse 2000st esimesest raamatust 10. Sellel juhul sisaldab esimene tööleht raamatuid, mis on seotud põhivaradega, mis on nummerdatud 1 kuni 2011. Teine tööleht sisaldab siis raamatuid, mis on seotud põhivaradega, mis on nummerdatud 2,012 kuni 4,000.

Kui dubleeritud vara ID-d ei ole samas töölehel, rakendatakse raamatute arvu limiiti. Kui aga vara ID on sama, mis raamatu ID, siis on võimalik ületada raamatute arv töölehe kohta, et hoida vara ID samas töölehel.

Näiteks on 5001 põhivara ID-d, kolm raamatut on seostatud iga põhivara ID-ga ja iga vararaamat sisestatakse samasse sisestamiskihti. Käivitate kulumi kolmel järestikusel kuul ilma summeerimata. Kulumi tööleht luuakse pakett-töö kaudu ja süsteem loob seitse töölehte, millel on 667 põhivara ID-d ja kolm raamatut iga põhivara ID kohta. Tulemuseks on 2001 raamatut. Seetõttu on kolme kuu järel samal töölehel sama vara ID-ga 6003 töölehe rida. Süsteem loob ka ühe töölehe, millel on 332 põhivara ID-d ja kolm raamatut iga põhivara ID kohta. Kolme kuu pärast on kokku 2988 rida.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]