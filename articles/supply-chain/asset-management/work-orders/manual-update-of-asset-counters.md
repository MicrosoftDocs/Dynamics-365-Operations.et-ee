---
title: Varaloendurite käsitsi värskendamine
description: Selles teemas kirjeldatakse varaloendurite käsitsi värskendust varahalduses.
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
ms.openlocfilehash: 4618ff2d6880f478683fbed0ed716af5ab8d4d9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842245"
---
# <a name="manual-update-of-asset-counters"></a>Varaloendurite käsitsi värskendamine

[!include [banner](../../includes/banner.md)]



Loendureid kasutatakse vara registreeringute loomiseks, nt registreeringud tundide arvu kohta, mille jooksul vara oli töös või toodetud koguse kohta.

Loenduri jaoks valitud loenduri tüüp võib olla seatud loenduri väärtusi pärima. Teiste sõnadega on valiku **Päri vara loenduri väärtused** seatud väärtusele **Jah** lehe **Loendurid** (**Varahaldus** > **Seadistus** > **Varatüübid** > **Loendurid**) kiirkaardil **Üldine**. Sel juhul, kui loote uue seda tüüpi loenduri, uuendatakse iga alamvara, mis kasutab sama loenduri tüüpi, automaatselt.

Lehel **Kõik varad** saate luua varale tundide või koguse loenduri registreeringud vara näitude põhjal.

1. Valige **Varahaldus** > **Ühised** > **Varad** > **Kõik varad**.

2. Valige vara ja seejärel tehke vahekaardi **Vara** jaotise **Ennetav** tegumiribal valik **Loendurid**. Lehel **Vara loendurid** kuvatakse loend kõigist valitud vara eelmistest loenduri registreeringust.

3. Valige uue registreeringu loomiseks **Uus**. Vara ID sisestatakse automaatselt väljale **Vara**.

4. Valige asjakohane loendur väljal **Loendur**. Valimiseks on saadaval ainult varale valitud vara tüübiga seotud loendurid. Seotud ühik sisestatakse automaatselt väljale **Ühik**.

5. Valige väljal **Registreeritud** loenduri registreeringu kuupäev ja kellaaeg.

6. Sisestage väljale **Väärtus** arv eelmisest loenduri registreeringust. Teise võimalusena sisestage väljale **Koondväärtus** loenduri koguarv.

Pidage meeles järgmiseid punkte.

- Kui paigaldate füüsiliselt varale uue loenduri, peate registreerima vara muudatuse lehel **Vara loendurid**. Järgmisena peate looma kaks identsete ajatemplitega registreeringurida. Esimene rida peab olema loenduri jaoks, mille asendate. Uue loenduriga seotud real märkige ruut **Loenduri lähtestamine**. Väljal **Kogusummad** on loenduri koguarvuks kõigi selle loenduritüübi registreeritud väärtuste loenduri kogusumma.

- Kui varale on valitud märkeruut **Loenduri lähtestamine** kasutades hoolduskava intervallitüübiga "Üks kord alates..." või "Üks kord ületades...", on loendur uuel loenduri real ikka aktiivne, sest loote eraldi loenduri rea ja alustate uue loenduriga algusest peale.

Alloleval joonisel on esitatud lehe **Varaloendurid** näide.

![Joonis 1](media/11-work-orders.png)

Lehel **Varaloendurid** (**Varahaldus** > **Päringud** > **Varad** > **Varaloendurid**), saate vajadusel korraga teha mitme vara loenduri registreeringuid.

>[!NOTE]
>Saate seadistada vahemiku, et määratleda hälbed käsitsi loenduri registreeringutes. Samuti saate määrata teate tüübi, mis kuvatakse, kui registreeringud jäävad väljapoole määratletud vahemikku. Teavet loendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]