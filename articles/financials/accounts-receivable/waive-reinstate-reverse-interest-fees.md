---
title: "Intressimäärade nõudest loobumine, selle ennistamine või tühistamine"
description: "Selles artiklis selgitatakse, kuidas loobuda, ennistada ja tagasi pöörata intressi ja tasude kulusid."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59fa39db725032cdd202704d53a39b85fd946f89
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="waive-reinstate-or-reverse-interest-fees"></a>Intressimäärade nõudest loobumine, selle ennistamine või tühistamine

[!include[banner](../includes/banner.md)]


Selles artiklis selgitatakse, kuidas loobuda, ennistada ja tagasi pöörata intressi ja tasude kulusid.

Võite kasutada nuppe loendilehe **Kõik kliendid** vahekaardil **Kogu**, et tasude nõudest loobuda, neid tühistada või ennistada.

-   Loobutud tasunõuded kustutatakse. Tasu nõudest võib loobuda, kui näiteks klient vaidlustab tasu ja te soovite temaga häid ärisuhteid hoida.
-   Ennistatud tasunõuded muutuvad uuesti sissenõutavaks. Saate ennistada tasu nõuded, millest varem loobuti. Peate võib-olla tasude nõuded ennistama, kui määrate, et neist ei tuleks loobuda.
-   Tühistatud tasud eemaldatakse kliendi kontolt ja need ei ole enam sissenõutavad. Tasusid võib tühistada, kui näiteks kliendi võlasumma arvutamiseks valiti vale intressimäär. Saate kasutada eraldi protsessi intressi uuesti arvutamiseks ja kliendile uusi tasusid sisaldava viivisearve loomiseks.

Kõik need tegevused muudavad viivisearvet. Viivisearve on äridokument, mis teavitab kliente, kui nende kontolt võetakse intressi või tasusid. Kui loobute või tühistate intressi või tasud, luuakse tasude tasakaalustamiseks automaatselt kreeditarve või korrigeerimisarve. Kui ennistate loobutud tasunõude, luuakse automaatselt arve koos deebetsummaga, et ennistada kliendi võlgnetavad tasud. Järgmises tabelis kirjeldatakse iga tegevuse tulemusi.

| Tegevus                                                                                                                                                                                                            | Tulemus kliendi jaoks                                                                                             | Protsess                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Loobuge kogu viivisearvest koos kõigi neis sisalduvate intresside ja tasudega. või Valige ja loobuge tasudest või intressikannetest, mis on osa viivisearvetest.                                        | Tasunõuded kustutatakse.                                                                                           | Kliendi jaoks luuakse kreeditarve või korrigeerimisarve. Kreeditarvet kasutatakse automaatselt viivisearve või teie valitud intressikannete või tasude tasakaalustamiseks. Tasakaalustatud summa võrdub tasude kogusummaga, millest on lahutatud kliendi varasemad maksed ja kõik summad, millest varem loobuti või mis kanti maha. Kui kreeditarve summa ületab kliendi võla summa, saate teisendada kreeditarve hankija arveks. Seejärel saate kliendile teha tagasimakse.                                                       |
| Ennistage kogu viivisearve koos kõigi neis sisalduvate intresside ja tasudega. või Valige ja ennistage tasud või intressikanded, mis on osa viivisearvetest.                                | Loobutud summa kuulub uuesti sissenõudmisele.                                                                                     | Luuakse deebetsummaga arve ja summa tasakaalustatakse automaatselt varem loobutud tasudega. Tegelikke viivisearveid ei ennistata. Selle asemel luuakse arve, mis näitab kliendilt nõutavat summat. Kreeditarved või korrigeerimisarved, mis loodi loobutud viivisearvete tasakaalustamiseks, võivad endiselt alles olla, kui neid ei kasutatud viivisearvete tasakaalustamiseks. Sellisel juhul tasumata kreeditarved tühistatakse. Laekumata kreeditarved tasakaalustatakse tavaliselt automaatselt, kui viivisearvetest loobutakse. Siiski võib laekumata kreeditarve alles olla, kui klient vaidlustas tasud, kuid ikkagi tasus viivisearve. |
| Tühistage täielikud viivisearved. või Tühistage valitud intressikanded, mis on osa viivisearvetest. **Märkus.** Te ei saa tühistada tasu. Siiski saate tühistada kogu viivisearve, mis sisaldab tasu. | Tasusid ei nõuta enam kliendilt sisse. Intressi ümberarvutamisel tekib tasude nõue siiski uuesti. | Protsess on sama, nagu viivisearvetest või valitud intressikannetest loobumise protsess. Kliendi jaoks luuakse kreeditarve või korrigeerimisarve. Kreeditarvet kasutatakse viivisearve automaatseks tasakaalustamiseks. Eraldi protsessi abil saate ümber arvutada intressi ja luua uue viivisearve.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Lootusetute võlgade mahakandmiseks saate kasutada ka eraldi protsessi. See protsess märgib tasakaalustamiseks kõik kliendi kanded, selle asemel, et loobuda üksnes nendest tasudest, mis on viivisearvete osad.

## <a name="adjust-interest-for-invoices"></a>Arvete intressi korrigeerimine
Lisaks viivisearvete korrigeerimisele saate arvetelt intressitasusid eemaldada, kasutades ühte järgmistest toimingutest. Mõlemad protsessid korrigeerivad ka seotud viivisearveid.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Seotud intressiga arve korrigeerimine

Saate korrigeerida sisestatud arvet, mis sisaldub viivisearves. See protsess kopeerib andmed olemasolevalt arvelt uuele arvele, et teha ainult teie soovitud parandused. Arve tühistatakse ja luuakse uus arve. Samuti tühistatakse viivisearve kande intress, kui viivisearve on sisestatud. 

Saate parandusi teha, kasutades vabas vormis arve tegevuspaani nuppu **Arve parandamine**. See nupp on saadaval ainult juhul, kui on valitud konfiguratsioonivõti **Vabas vormis arve parandamine**.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Seotud intressiga kliendikande tühistamine

Saate tühistada kliendikande arvel, kui arve loodi valesti. Kui tühistatud kliendikandel on viivisearves sisalduv intress ja viivisearve on sisestatud, tühistatakse ka kande intress viivisearvel. Kui viivisearve pole sisestatud, siis see tühistatakse. 

Saate kliendi kanded tühistada, kasutades nuppu **Tühista**lehel **Kliendi kanded**.

## <a name="waive-or-reinstate-interest-notes"></a>Viivisearvetest loobumine või nende ennistamine
Saate loobuda või ennistada kõik tasud valitavatel viivisearvetel. Kui loobute tasude nõuetest, ei saa loobumise kogusumma ületada määratud summapiiranguid. Viivisearve saab ennistada ainult juhul, kui sellest eelnevalt loobuti. 

Saate viivisearvetest loobuda või need ennistada, kasutades nuppu **Viivisearve** lehe **Klient** vahekaardil **Kogu**.

## <a name="waive-or-reinstate-interest-transactions"></a>Intressikannetest loobumine või nende ennistamine
Võite loobuda või ennistada viivisearve konkreetsed intressikanded, selle asemel et korrigeerida kõiki viivisearve tasusid. Kui loobute tasude nõuetest, ei saa loobumise kogusumma ületada määratud summapiiranguid. Intressikande saab ennistada ainult juhul, kui sellest eelnevalt loobuti. 

Saate viivisearvetest loobuda või need ennistada, kasutades nuppu **Kande intress** lehe **Klient** vahekaardil **Kogu**.

## <a name="waive-or-reinstate-fees"></a>Tasudest loobumine või nende ennistamine
Võite loobuda või ennistada viivisearve konkreetsed tasud, selle asemel et korrigeerida kõiki viivisearve tasusid. Kui loobute tasude nõuetest, ei saa loobumise kogusumma ületada määratud summapiiranguid. Tasu saab ennistada ainult juhul, kui sellest varem loobuti. 

Saate viivisearvetest loobuda või need ennistada, kasutades nuppu **Tasu** lehe **Klient** vahekaardil **Kogu**.

## <a name="reverse-interest-notes"></a>Viivisearvete tühistamine
Saate tühistada kõik tasud valitavatel viivisearvetel. Tühistatud tasud eemaldatakse kliendi kontolt ja need ei ole enam sissenõutavad. Pärast seda, kui viivisearve tühistatakse, saab intressi ümber arvutada ja luua uue viivisearve. 

Saate viivisearved tühistada, kasutades nuppu **Viivisearve**lehe **Klient** vahekaardil **Kogu**.

## <a name="reverse-interest-transactions"></a>Intressikannete tühistamine
Saate tühistada kõik intressikanded, mille valite. Tühistatud tasud eemaldatakse kliendi kontolt ja need ei ole enam sissenõutavad. Pärast seda, kui kanded tühistatakse, saab intressi ümber arvutada ja luua uue viivisearve.

Saate intressikanded tühistada, kasutades nuppu **Kande intress** lehe **Klient** vahekaardil **Kogu**.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Loobutud, ennistatud või tühistatud tasude korrigeerimiste ajaloo vaatamine
Saate vaadata viivisearvetes tehtud korrigeerimiste üksikasjalikku ajalugu, näiteks korrigeerimise sisestanud kasutajat, korrigeerimise tüüpi, summat ja sisestamise aega. Näiteks võite vaadata viivisearvele sisestatud eelmisi korrigeerimisi enne uue viivisearve loomist. 

Saate intressikanded tühistada, kasutades nuppu **Ajalugu**lehe **Klient** vahekaardil **Kogu**.




