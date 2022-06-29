---
title: Varaloendurite käsitsi värskendamine
description: Selles artiklis kirjeldatakse varahalduses varaloendurite käsitsi uuendamist.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 30c672286c16a4353556a507019960edb93f8b1b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016590"
---
# <a name="manual-update-of-asset-counters"></a>Varaloendurite käsitsi värskendamine

[!include [banner](../../includes/banner.md)]



Loendureid kasutatakse vara registreeringute loomiseks, nt registreeringud tundide arvu kohta, mille jooksul vara oli töös või toodetud koguse kohta.

Loenduri jaoks valitud loenduri tüüp võib olla seatud loenduri väärtusi pärima. Teiste sõnadega on valiku **Päri vara loenduri väärtused** seatud väärtusele **Jah** lehe **Loendurid** (**Varahaldus** > **Seadistus** > **Varatüübid** > **Loendurid**) kiirkaardil **Üldine**. Sel juhul, kui loote uue seda tüüpi loenduri, uuendatakse iga alamvara, mis kasutab sama loenduri tüüpi, automaatselt.

Lehel **Kõik varad** saate luua varale tundide või koguse loenduri registreeringud vara näitude põhjal.

1. Valige **Varahaldus** > **Varad Kõik** > **varad**.

2. Valige vara ja seejärel tehke vahekaardi **Vara** jaotise **Ennetav** tegumiribal valik **Loendurid**. Lehel **Vara loendurid** kuvatakse loend kõigist valitud vara eelmistest loenduri registreeringust.

3. Valige uue registreeringu loomiseks **Uus**. Vara ID sisestatakse automaatselt väljale **Vara**.

4. Valige asjakohane loendur väljal **Loendur**. Valimiseks on saadaval ainult varale valitud vara tüübiga seotud loendurid. Seotud ühik sisestatakse automaatselt väljale **Ühik**.

5. Valige väljal **Registreeritud** loenduri registreeringu kuupäev ja kellaaeg.

6. Sisestage väljale **Väärtus** arv eelmisest loenduri registreeringust. Teise võimalusena sisestage väljale **Koondväärtus** loenduri koguarv.

Pidage meeles järgmiseid punkte.

- Kui paigaldate füüsiliselt varale uue loenduri, peate registreerima vara muudatuse lehel **Vara loendurid**. Järgmisena peate looma kaks identsete ajatemplitega registreeringurida. Esimene rida peab olema loenduri jaoks, mille asendate. Uue loenduriga seotud real märkige ruut **Loenduri lähtestamine**. Väljal **Kogusummad** on loenduri koguarvuks kõigi selle loenduritüübi registreeritud väärtuste loenduri kogusumma.

- Kui varale on valitud märkeruut **Loenduri lähtestamine** kasutades hoolduskava intervallitüübiga "Üks kord alates..." või "Üks kord ületades...", on loendur uuel loenduri real ikka aktiivne, sest loote eraldi loenduri rea ja alustate uue loenduriga algusest peale.

Alloleval joonisel on esitatud lehe **Varaloendurid** näide.

![Joonis 1.](media/11-work-orders.png)

Lehel **Varaloendurid** (**Varahaldus** > **Päringud** > **Varad** > **Varaloendurid**), saate vajadusel korraga teha mitme vara loenduri registreeringuid.

>[!NOTE]
>Saate seadistada vahemiku, et määratleda hälbed käsitsi loenduri registreeringutes. Samuti saate määrata teate tüübi, mis kuvatakse, kui registreeringud jäävad väljapoole määratletud vahemikku. Teavet loendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]