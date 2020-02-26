---
title: Sortimendi haldus
description: Selles teemas selgitatakse sortimendi halduse põhikontseptsioone rakenduses Dynamics 365 Commerce ja esitatakse juurutamise kaalutlusi teie projekti jaoks.
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: e1b177989065740eef0bd917a7ce1e0a2c79088b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022210"
---
# <a name="assortment-management"></a>Sortimendi haldus

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce pakub *sortimente*, mis võimaldavad teil hallata toote saadavust kanalite lõikes. Sortimendid määratlevad, millised tooted on konkreetsetes kauplustes ja millise perioodi jooksul saadaval.

Commerce'is on sortiment ühe või mitme kanali (või kanaligruppide, kui kasutatakse organisatsiooni hierarhiaid) vastendamine ühe või mitme tootega (või tootegruppidega, kui kasutatakse kategooria hierarhiaid).

Kanali üldine tootevalik määratletakse kanalile määratud avaldatud sortimentidega. Seetõttu saate konfigureerida mitu aktiivset sortimenti kanali kohta.

### <a name="basic-assortment-setup"></a>Sortimendi põhiseadistus

Järgmises näites on iga kaupluse jaoks konfigureeritud kordumatu sortiment. Sel juhul on kaupluses 1 saadaval ainult toode 1 ja kaupluses 2 on saadaval ainult toode 2.

![Iga toode on ühes kaupluses saadaval](./media/Managing-assortments-figure1.png)

Et toode 2 oleks saadaval kaupluses 1, saate toote lisada sortimenti 1.

![Toode 2 lisati sortimenti 1](./media/Managing-assortments-figure2.png)

Teise võimalusena saate lisada kaupluse 1 sortimenti 2.

![Kauplus 1 lisati sortimenti 2](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organisatsiooni hierarhiad

Olukordades, kus mitu kanalit jagavad samu tootesortimente, saate sortimentide konfigureerimiseks kasutada Commerce'i sortimendi organisatsiooni hierarhiat. Kui hierarhia sõlmed on lisatud, kaasatakse kõik vastavas sõlmes ja selle alamsõlmedes olevad kanalid.

![Organisatsiooni hierarhia](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Tootekategooriad

Samuti saate toote poolel lisada tootegruppe, kasutades tootekategooria hierarhiaid. Saate konfigureerida sortimente, lisades ühe või mitu kategooria hierarhia sõlme. Sel juhul sisaldab sortiment kõiki tooteid, mis on selles kategooriasõlmes ja selle alamsõlmedes.

![Tootekategooriad](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Välja jäetud tooted või kategooriad

Lisaks toodete ja kategooriate kaasamisele sortimentidesse saate kasutada suvandit Välista, et määratleda konkreetseid kaupu või kategooriad, mis tuleks sortimentidest välistada. Järgmises näites soovite kaasata kõik konkreetses kategoorias olevad tooted, välja arvatud toote 2. Sel juhul ei pea te määratlema sortimendi tooteid toodete kaupa või looma täiendavaid kategooriasõlmi. Selle asemel saate lihtsalt lisada kategooria ja toote välja jätta.

> [!NOTE]
> Kui toode on määratluse järgi ühte või mitmesse sortimenti korraga nii kaasatud kui ka sortimendist välja jäetud, loetakse toode alati välja jäetuks.

![Välistatud tooted](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Üldised ja väljastatud tooted

Sortimente määratletakse üldisel tasemel ja need võivad sisaldada mitme juriidilise isiku kanaleid. Ka sortimentidesse kaasatud tooteid ja kategooriaid jagatakse juriidiliste isikute vahel. Siiski tuleb toode enne väljastada, kui seda saab kanalil reaalselt müüa, tellida, loendada või vastu võtta (näiteks kassas \[POS\]). Seetõttu, kuigi kaks kauplust erinevates juriidilistes isikutes saavad samu tooteid sisaldavat sortimenti jagada, on tooted saadaval alles siis, kui need on nendesse juriidilistesse isikutesse vabastatud.

### <a name="dynamic-and-static-assortments"></a>Dünaamilised ja staatilised sortimendid

Sortimente saab määratleda konkreetse kanalite ja toodetega või kaasates organisatsiooniüksuseid ja kategooriad. Sortimente, mis sisaldavad viiteid nendele gruppidele, loetakse dünaamilisteks sortimentideks. Kui nende gruppide määratlus või sisu muutub ajal, mil sortiment on aktiivne, muutub ka sortimendi määratlus.

Näiteks on sortiment algselt määratletud ja avaldatud nii, et see viitab toodete kategooriale. Kui kategooriasse lisatakse hiljem tooteid juurde, kaasatakse need tooted automaatselt olemasoleva sortimendi määratlusse. Te ei pea tooteid käsitsi sortimenti lisama. Sarnaselt, kui organisatsiooniüksus lisatakse teise sõlme, korrigeeritakse organisatsiooniüksuse sortimenti automaatselt selle määratluse põhjal.

### <a name="stopped-products"></a>Peatatud tooted

Saate müügiprotsessi jaoks väljastatud tooted peatada, lülitades sisse vastava sätte **tellimuse vaikesätetes**. Seda sätet kasutatakse kõige sagedamini toote elutsükli lõpus, kui seda toodet ei tohiks enam ühelgi kanalil müüa. Sortimendid järgivad seda sätet ja peatatud tooteid ei kaasata sortimenti, olenemata sortimendi konfiguratsioonist.

### <a name="blocked-products"></a>Blokeeritud tooted

Lisaks toote müümise peatamisele saate toote müümise ajutiselt blokeerida. Seda sätet saate konfigureerida väljastatud toote vahekaardil **Kaubandus**. Blokeeritud tooted kuuluvad endiselt sortimenti, kuid saate kassas teate, et seda toodet ei saa müüa.

### <a name="date-effectivity"></a>Kuupäeva jõustumine

Sortimendid sõltuvad kuupäevast. Seetõttu saavad jaemüüjad konfigureerida, millal peaksid tooted kanali kohta saadaval olema. Saate määratleda ja avaldada sortimente enne tähtaega ning määrata algus- ja lõppkuupäevad. Tooted on määratud kuupäevadel automaatselt saadaval või mittesaadaval.

### <a name="process-assortments-batch-job"></a>Sortimendi pakett-töö töötlemine

Commerce'is määratletud sortimente tuleb enne nende jõustumist töödelda. Töötlemine toimub järgmistel põhjustel.

- Sortimendi määratlused tuleb denormaliseerida, et kanalitel oleks neid lihtsam tarbida. Kanali tootevalikut saab määratleda erinevate sortimentide kaudu, millele kehtivad erinevad kuupäevavahemikud. Kui osa sellest teabest arvutatakse serveris enne tähtaega, parandab see kanali jõudlust.
- Sortimendis olevad tooted ja kanalid võivad muutuda väljaspool sortimenti. Dünaamilisi sortimente, mis sisaldavad viiteid kategooriatele või organisatsiooniüksustele, tuleb töödelda regulaarselt, et need kaasaks või välistaks praeguse määramise põhjal kirjeid.

## <a name="implementation-considerations"></a>Juurutamise kaalutlused

Kui plaanite ja haldate oma Commerce'i juurutuse jaoks sortimente, arvestage järgmiste juurutamisnõuetega.

- **Andmete edastamine ja andmebaasi suurus** – kuigi sortimentid aitavad ettevõttel hallata toodete saadavust, on need ka oluline vahend kanali ja võrguühenduseta andmebaaside suuruse haldamisel. Hästi hallatud sortimendid aitavad vähendada töötlemist vajavate ning kanalile ja võrguühenduseta andmebaasidesse edastatavate andmete mahtu. Need aitavad vähendada ka kinnistamist vajavate kirjete arvu. Kui nendes andmebaasides on vähem kirjeid, suureneb jõudlus, kui lisate kandele kaupu ning otsite ja sirvite tooteid.
- **Kuupäevast sõltuvad / aeguvad sortimendid** – üks kõige tõhusamaid tööriistu toodete arvu haldamiseks kanalil ja võrguühenduseta andmebaasides on sortimentide kuupäeva jõustumine. Kui jätate andmebaasi hooajaliste toodete või elutsükli lõpus olevate toodete avatud (mitteaeguvaid) sortimente, kasvavad need andmebaasid piiramatult. Selle olukorra haldamiseks saate kasutada erinevaid lähenemisviise. Näiteks saate hallata eraldi sortimente hooajaliste toodete jaoks ning alati saadaval olevate toodete jaoks.
- **Müük ja tagastused väljaspool sortimente** – see võimalus aitab jaemüüjatel oma sortimente tõhusalt hallata, võimaldades piirata saadaolevate toodete arvu toodetega, mis kuuluvad kaupluse peamisse tootevalikusse. See võimalus aitab jaemüüjatel käsitleda olukordi, kus toode jäeti ekslikult sortimendist välja või kus toode tagastati väljaspool sortimendi kehtivuskuupäevi.

Kui toote andmeid pole kanali andmebaasis, teeb kassa vajaliku teabe hankimiseks reaalajas kõnesid peakontorisse, et toodet saaks müüa, tagastada või panna klienditellimusse. Sel viisil hangitav tooteteave on saadaval ainult selle kande käitlemise ajal. Seda toodet ei lisata sortimendi määratlusse. Seetõttu tehakse järgnevad reaalajas kõned vastavalt vajadusele.
