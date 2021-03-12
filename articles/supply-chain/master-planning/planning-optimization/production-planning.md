---
title: Tootmise planeerimine
description: Selles teemas kirjeldatakse tootmise planeerimist ja selgitatakse, kuidas muuta plaanitud tootmistellimusi Planning Optimizationi abil.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992391"
---
# <a name="production-planning"></a>Tootmise planeerimine

Planning Optimization toetab mitut tootmisstsenaariumi. Kui migreerite olemasolevalt sisse-ehitatud koondplaneerimise mootorilt, on oluline, et teaksite mõnda muutunud käitumist.

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a>Plaanitud tootmistellimused

Kui koondplaneerimine loob plaanitud tellimuste täitmiseks nõuded, määratletakse tellimuse tüüp välja **Plaanitud tellimuse tüüp** väärtusega. Kui välja **Plaanitud tellimuse tüüp** tüäärtuseks on seatud *Tootmine*, luuakse plaanitud tootmistellimused. Need plaanitud tootmistellimused sisaldavad teavet aktiivse koosluse kohta (BOM) ja protsessi ID-d seostuvast tootmise seadistusest.

## <a name="requirements-from-boms"></a>Koosluste nõuded

Koondplaneerimise ajal arvestatakse koosluse teabega. Plaani väljund hõlmab materjalitarnet, mis kataks seotud materjali nõudluse tootmisele.

Koondplaneerimise ajal kasutatakse praegust aktiivset kooslust tootmiseks vajalike materjalide määramiseks. See samm tehakse läbi kõigi nõutava tootmistellimusega seotud koosluse struktuuri tasemetel. Materjalivajadus täidetakse, kasutades saadaolevaid vabasid kaubavarusid, olemasolevaid tellimuse tarneid ja kinnitatud plaanitud tellimusi. Kui lisamaterjale vajatakse kus tahes, luuakse nõudluse katmiseks plaanitud tellimus.

## <a name="scheduling-during-firming"></a>Plaanimine kinnitamis ajal

Plaanitud tootmistellimused sisaldavad protsessi ID-d, mis on vajalik tootmise planeerimiseks. Samas planeerimise tugi plaanitud tellimustele käitamise ajal on ootel. Protsessi ID-d kasutatakse plaanitud tootmistellimuste plaanimiseks tootmise ajal. Seetõttu võib plaanitud tootmistellimuste täitmisaeg erineda plaanitud ja neist loodud kindlast tootmistellimuste täitmisajast, nagu on järgnevalt kirjeldatud.

- **Plaanitud tootmistellimus** – täitmisaeg põhineb väljastatud toote staatilisel täitmisajal.
- **Kinnistatud tootmistellimus** – täitmisaeg põhineb planeerimisel, mis kasutab protsessiteavet ja seotud ressursipiiranguid.

Lisateavet funktsiooni eeldatava saadavuse kohta vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).

Kui te sõltute tootmise funktsioonidest, mis ei ole veel Planning Optimizationi jaoks saadaval, saate jätkata integreeritud koondplaneerimise mootori kasutamist. Erandit pole vaja.

## <a name="delays"></a>Hilinemised

Kui nõutava materjali täitmisaeg on pikem kui periood tänase kuupäeva ja materjalivajaduse kuupäeva vahel, siis nõutava materjali plaanitud tellimus ja seotud tootmistellimus hilinevad. Plaanitud tellimuste puhul arvutatakse viivitus (päevades) väljastatud toote täitmisaja alusel. Viivituse teavet levitatakse seejärel kõigi koosluse struktuuri tasemete kaudu. Seega saate hilinenud toormaterjali mõju jälgida kogu tee kliendi müügitellimuseni.

## <a name="modifying-planned-orders"></a>Plaanitud tellimuste muutmine

Kui muudate plaanitud tellimuse teavet, saate järgmise teate: „Pange tähele, et plaanitud tellimustes käsitsi tehtud muudatuste mõju ei kajastu ülejäänud plaanis enne järgmise koondplaani käivitamist.”

Kui soovite muuta plaanitud tellimuse teavet ja vaadata mõju seotud materjalinõuetele, järgige järgmisi samme.

1. Värskendage plaanitud tellimust.
2. Kinnitage plaanitud tellimus.
3. Käivitage koondplaneerimine.

Koondplaneerimise käivitamisel ei tohiks kasutada filtreid, kui kaasatud on plaanitud tootmistellimused. Lisateabe saamiseks vaadake selle teema järgnevaid jaotisi [Filtrid](#filters).

> [!NOTE]
> Kui plaanitud tellimuse tarnekuupäev muudetakse hilisemaks kuupäevaks, võib nõudlus olla seotud uue plaanitud tellimusega. Selline käitumine ilmneb siis, kui uus tarnekuupäev põhjustab seotud nõudluse viivitusi, kuid vastavalt täitmisaja sätetele võib viivitusi vältida.

## <a name="explosion-page"></a>Koosluse leht

Saate kasutada lehte **Kooslus**, et analüüsida nõudlust, mis on vajalik konkreetse tootmistellimuse või plaanitud tootmistellimuse, seotud laovarude ja sidumisteabe jaoks. Teavet lehel **Kooslus** uuendatakse koondplaneerimise ajal. Teavet ei saa uuendada otse lehel **Kooslus**.

## <a name="filters"></a><a name="filters"></a>Filtrid

Tootmisega seotud stsenaariumite plaanimiseks on soovitatav vältida filtreeritud koondplaneerimise käitamist. Kindlustamaks, et teenusel Planning Optimization oleks õige tulemuse arvutamiseks vajalik teave, peate kaasama kõik tooted, millel on mis tahes seos toodetega plaanitud tellimuse koosluse struktuuris.

Kuigi sõltuvad alamüksused tuvastatakse ja kaasatakse koondplaneerimisel automaatselt, siis integreeritud koondplaneerimise mootori kasutamisel plaanimise optimeerimine seda tegevust ei tee.

Näiteks kui toote A koosluse struktuurist kasutatakse ka üksikut polti ka toote B tootmiseks, peavad filtrisse olema kaasatud kõik tooted, mis on toodete A ja B koosluse struktuuris. Kuna kõigi toodete filtri osa kindlustamine võib olla väga keerukas, on soovitatav vältida filtreeritud koondplaneerimise käivitamist tootmistellimuste puhul.
