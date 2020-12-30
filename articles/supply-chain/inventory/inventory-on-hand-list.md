---
title: Vaba kaubavaru loend
description: Selles teemas kirjeldatakse, kuidas kasutada vaba kaubavaru loendi lehte, et vaadata vaba kaubavaru üksikasju. Selles näidatakse mõnda viisi, kuidas eri filtreerimis- ja sortimissuvandid koos töötavad ja kuidas need valikud võivad mõnikord põhjustada ühendamisel ootamatuid tulemusi.
author: sherry-zheng
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 33e5ccc454191e27e33835a05094b823ec54e891
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426674"
---
# <a name="inventory-on-hand-list"></a>Vaba kaubavaru loend

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada lehte **Vaba kaubavaru loend**, et vaadata vaba kaubavaru üksikasju. Selles näidatakse mõnda viisi, kuidas eri filtreerimis- ja sortimissuvandid koos töötavad ja kuidas need valikud võivad mõnikord põhjustada ühendamisel ootamatuid tulemusi.

## <a name="query-your-on-hand-inventory"></a>Oma vaba kaubavaru kontrollimine

Varude kättesaadavuse kontrollimiseks avage **Varude haldus \> Päringud ja aruanded \> Vaba kaubavaru loend**.

Lehte **Vaba kaubavaru loend** uuendatakse automaatselt varudes kannete tegemisel. Need kanded võivad olla prognoositud, füüsilised või finantskanded.

Kasutage otsitavate toodete leidmiseks järgmisi tööriistu.

- Valige toimingupaanil [**Dimensioonid**](#dimensions), et avada dialoogiboks, kus saate lisada või eemaldada veerge, mis kuvatakse ruudustikus **Vaba kaubavaru**.
- Sisestage [paanil **Filtrid**](#filters-pane) kindlatele väljadele väärtused, et näidata ainult nende väärtustega ühtivaid kirjeid. Võtke arvesse, et siin määratletud filtreid rakendatakse lähtetabelite puhul, mida võidakse hiljem koondada dimensioonide järgi, mille te kuvamiseks valisite. Teavet selle kohta, kuidas see käitumine võib teie tulemusi mõjutada, leiate hiljem selle teema [näidetest](#examples).
- Valige paanil **Filtrid** suvand **Rakenda**, et luua **Vaba kaubavaru** ruudustikus ühtiva vaba kaubavaru loend.
- Valige **Vaba kaubavaru** ruudustikus ükskõik milline veerupäis, et sortida või filtreerida selle veeru väärtuste alusel. Ruudustiku ülaosas olev kiirfilter pakub täiendavaid filtreerimissuvandeid. Need filtrid rakenduvad tulemustele, mitte lähtetabelitele. Teavet selle kohta, kuidas see käitumine võib teie tulemusi mõjutada, leiate hiljem selle teema [näidetest](#examples).

**Vaba kaubavaru** ruudustikus on iga ühtiva kauba kohta järgmised varude teavet sisaldavad veerud.

| Veerg | Kirjeldus |
|---|---|
| Füüsilised varud | Laos füüsiliselt saadaolev kogus. |
| Füüsiliselt reserveeritud | Kogu füüsiliselt reserveeritud kogus. |
| Füüsiliselt vaba | Vaba (mitte reserveeritud) kogus, mis on füüsiliselt laos saadaval.<p>**Füüsiliselt vaba** on arvutatud väli. Selle väärtuse leidmiseks lahutatakse väärtusest **Füüsilised varud** väärtus **Füüsiliselt reserveeritud**.</p> |
| Füüsiliselt vaba lisadimensioonide alusel | Saadaolev füüsiline kogus kõigi ruudustikus kuvatud dimensioonide alusel. |
| Tellitud kokku | Lõplik kogus, mida sisaldavad sissetulevad tellimused või mille kogus on eri varude töölehtedel positiivne. |
| Tellimusel | Lõplik kogus, mida sisaldavad väljaminevad tellimused või mille kogus on eri varude töölehtedel negatiivne. |
| Tellitud reserveeritud | Lõplik kogus, mis on tellitud sissetulekutel reserveeritud. Selle välja väärtus tähistab olekuga _Tellitud reserveeritud_ väljaminevate kannete kaupade lõplikku kogust. Kaubad, mis on tellituna reserveeritud, pole laos füüsiliselt saadaval. Seetõttu ei saa neid otse komplekteerida ega tarnida. |
| Reserveerimiseks saadaval | Vaba kaubavaru lõplik kogus, mida saab reserveerida.<p>**Märkus.** Kui märkeruut **Reserveeri tellitud kaubad** on lehel **Varude ja laohalduse parameetrid** valitud, sisaldab selle välja väärtus eeldatavaid sissetulekuid. Kui märkeruut on tühjendatud, ei hõlma väärtus eeldatavaid sissetulekuid.</p> |
| Kokku vaba | Saadaolev kogus kokku.<p>**Kokku vaba** on arvutatud väli. Väärtuse leidmiseks liidetakse väärtus **Füüsiliselt vaba** väärtusele **Tellitud kokku**, millest lahutatakse **Tellimusel**.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Filtrite rakendamine otsitavate kirjete leidmiseks

Kasutage paani **Filtrid**, filtreerida vaba kaubavaru loendit nii, et see sisaldaks ainult kirjeid, mille puhul väljaväärtused ühtivad filtreerimiskriteeriumidega. Filtri määratlemiseks toimige järgmiselt.

1. Otsige paanil **Filtrid** üles filter, mida soovite kasutada filtreerimiseks.
2. Valige sihtvälja nime all asuvalt väljalt loogiline tehtemärk (nt *algus*, *võrdne* või *suurem kui*).
3. Sisestage või valige otsitav väärtus.

> [!IMPORTANT]
> Leht **Vaba kaubavaru loend** koostatakse üksikasjalikust vaba kaubavaru tabelist, mis sisaldab kõiki saadaolevaid dimensioone. Sellel lehel olev loend on aga vaid kokkuvõte. Seetõttu võidakse selles kombineerida lähtetabeli ridu, koondades väärtuseid kuvatud dimensioonide järgi.
>
> Paanil **Filtrid** määratletud filtrid rakenduvad lähtetabelile, mitte koondatud loendile. Selline käitumine võib mõnikord põhjustada ootamatuid tulemusi. Teavet selle kohta, kuidas see käitumine võib teie tulemusi mõjutada, leiate hiljem selle teema [näidetest](#examples).
> 
> [Ruudustikus esitatud filtrid](#grid-filters) rakenduvad *siiski* koondatud loendile. Need filtrid hõlmavad nii kiirfiltrit ruudustiku ülaosas kui ka iga veerupäise filtrit.

Saate muuta filtreid, mis on saadaval paanil **Filtrid**, järgmiseid juhiseid järgides.

- Paanilt filtri eemaldamiseks valige selle **sulgemise** nupp (**X**).
- Filtri lisamiseks valige suvand **Lisa**, mis asub paani **Filtrid** ülaosas. Avanenud dialoogiboksis **Lisa filtrivälju** on kuvatud saadaolevate väljade loend. Samuti kuvatakse selles teave iga välja andmetüübi ja tabeli kohta. Kasutage veerupäiseid, et filtreerida ja sortida loendit oma vajaduse järgi, ning seejärel valige märkeruut iga välja puhul, mida soovite paanile **Filtrid** lisada. Kui olete lõpetanud, valige oma muudatuse rakendamiseks **Sisesta**.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Kuvatavate dimensioonide valimine

Dimensioonid annavad kõikide vaba kaubavaru loendis olevate kaupade kohta lisateavet ning rohkem võimalusi loendi sortimiseks ja filtreerimiseks. Dimensioonid, mida valite kuvamiseks, mõjutavad ka seda, kuidas read lehel **Vaba kaubavaru loend** koondatakse. Koondamine võib omakorda mõjutada seda, kuidas lähtetabelite read kombineeritakse tulemustes, mida näete. Teavet selle kohta, kuidas see käitumine võib teie tulemusi mõjutada, leiate hiljem selle teema [näidetest](#examples).

Kuvatavate varude dimensioonide valiku kohandamiseks toimige järgmiselt.

1. Valige toimingupaanil **Dimensioonid**.

    Avanenud dialoogiboksis **Dimensiooni kuvamine** kuvatakse kõik dimensioonid.

2. Valige märkeruut iga dimensiooni puhul, mida soovite ruudustikku lisada.
3. Kui soovite, et teie valikut kasutataks vaikimisi järgmisel korral, kui avate lehe **Vaba kaubavaru loend**, seadke suvandi **Salvesta seadistus** väärtuseks **Jah**. Kui seate selle suvandi väärtuseks **Ei**, kasutatakse teie valikut ainult praeguse seansi jooksul. Seetõttu kasutatakse järgmine kord, kui avate lehe, praegust vaikevalikut.
4. Valige **OK**, et dialoogiboks sulgeda ja oma muudatused rakendada.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Vaba kaubavaru loendi väljundi alusel filtreerimine

Saate valida **Vaba kaubavaru** ruudustikus ükskõik millise veerupäise, et sortida või filtreerida selle veeru väärtuste alusel. Ruudustiku ülaosas olev kiirfilter pakub täiendavaid filtreerimissuvandeid. Need filtrid rakenduvad tulemustele, mitte lähtetabelitele. Teavet selle kohta, kuidas see käitumine võib teie tulemusi mõjutada, leiate hiljem selle teema [näidetest](#examples).

> [!NOTE]
> Te ei saa filtreerida ega sortida kõigi veergude alusel. Enamikus koguseveergudes pole sortimise ja filtreerimise juhtelemente, kuna need on arvutatud väljad. Veerg **Tellimusel** on erand.

## <a name="examples"></a><a name="examples"></a>Näited

Teie süsteem sisaldab üksikasjalikku (koondamata) varude tabelit, milles näidatakse järgmist vaba kaubavaru.

| Kaubakood | Sait | Ladu | Füüsilised varud | Füüsiliselt vaba |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>1. stsenaarium

Leht **Vaba kaubavaru loend** on seadistatud kuvama järgmisi lõplikke dimensioone.

- Kaubakood
- Sait
- Ladu

Paanil **Filtrid** on seadistatud järgmised filtreerimiskriteeriumid.

- **Kaubakood** \| **on täpselt** \| _IA0001_
- **Füüsiliselt vaba** \| **väiksem kui või võrdne** \| _1_

Siin on selle tulemus.

| Kaubakood | Sait | Ladu | Füüsilised varud | Füüsiliselt vaba |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>2. stsenaarium

Leht **Vaba kaubavaru loend** on seadistatud kuvama järgmisi lõplikke dimensioone.

- Kaubakood
- Sait

Paanil **Filtrid** on seadistatud järgmised filtreerimiskriteeriumid.

- **Kaubakood** \| **on täpselt** \| _IA0001_
- **Füüsiliselt vaba** \| **väiksem kui või võrdne** \| _1_

Siin on selle tulemus.

| Kaubakood | Sait | Füüsilised varud | Füüsiliselt vaba |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Pange tähele, et paani **Filtrid** sätted rakenduvad üksikasjalikule (koondamata) varude tabelile, mis on toodud selle jaotise alguses. Seetõttu leiab kriteerium **Füüsiliselt vaba** \| **väiksem kui või võrdne** \| _1_ sellest tabelist kaks rida (esimese ja kolmanda rea, sest mõlema suvandi **Füüsiliselt vaba** väärtus on _1_). Kuid selles olukorras pole lehte **Vaba kaubavaru loend** seadistatud kuvama dimensiooni **Ladu**. Seetõttu koondab see kaks algset rida üheks reaks, kuna mõlemal real on identsed väärtused kõiki kuvatud dimensioone arvestades. See rida näib olevat vastuolus filtreerimiskriteeriumiga, kuna suvandi **Füüsiliselt vaba** väärtus on _2_. Kuid tulemus on õige, kuna paani **Filtrid** sätted rakenduvad lähtetabelile, mitte tabelile, mis on kuvatud lehel **Vaba kaubavaru loend**.
