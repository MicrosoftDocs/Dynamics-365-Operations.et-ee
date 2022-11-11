---
title: Tootmise planeerimine
description: See artikkel kirjeldab tootmise planeerimist ja selgitab plaanitud tootmistellimuste muutmise plaanimise optimeerimise abil.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 43da249637c44b3f56e8b5e210a0e44d9ac6cb9d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740545"
---
# <a name="production-planning"></a>Tootmise planeerimine

[!include [banner](../../includes/banner.md)]

Järgmises videos antakse lühike sissejuhatus mõnedele selles artiklis nimetatud mõistetele: optimeerimise [Dynamics 365 Supply Chain Management optimeerimise täiustuste planeerimine](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-this-feature-on-or-off-for-your-system"></a>Lülitage see funktsioon süsteemi sisse või välja

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse tööruumist plaanimise optimeerimise funktsiooni plaanitud tootmistellimused.](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="planned-production-orders"></a>Plaanitud tootmistellimused

Kui koondplaneerimine loob plaanitud tellimuste täitmiseks nõuded, määratletakse tellimuse tüüp välja **Plaanitud tellimuse tüüp** väärtusega. Kui välja **Plaanitud tellimuse tüüp** tüäärtuseks on seatud *Tootmine*, luuakse plaanitud tootmistellimused. Need plaanitud tootmistellimused sisaldavad teavet aktiivse koosluse kohta (BOM) ja protsessi ID-d seostuvast tootmise seadistusest.

## <a name="requirements-from-boms"></a>Koosluste nõuded

Koondplaneerimise ajal arvestatakse koosluse teabega. Plaani väljund hõlmab materjalitarnet, mis kataks seotud materjali nõudluse tootmisele.

Koondplaneerimise ajal kasutatakse praegust aktiivset kooslust tootmiseks vajalike materjalide määramiseks. See samm tehakse läbi kõigi nõutava tootmistellimusega seotud koosluse struktuuri tasemetel. Materjalivajadus täidetakse, kasutades saadaolevaid vabasid kaubavarusid, olemasolevaid tellimuse tarneid ja kinnitatud plaanitud tellimusi. Kui lisamaterjale vajatakse kus tahes, luuakse nõudluse katmiseks plaanitud tellimus.

## <a name="scheduling-during-firming"></a>Plaanimine kinnitamis ajal

Plaanitud tootmistellimused sisaldavad protsessi ID-d, mis on vajalik tootmise planeerimiseks. Samas planeerimise tugi plaanitud tellimustele käitamise ajal on ootel. Protsessi ID-d kasutatakse plaanitud tootmistellimuste plaanimiseks tootmise ajal. Seetõttu võib plaanitud tootmistellimuste täitmisaeg erineda plaanitud ja neist loodud kindlast tootmistellimuste täitmisajast, nagu on järgnevalt kirjeldatud.

- **Plaanitud tootmistellimus** – täitmisaeg põhineb väljastatud toote staatilisel täitmisajal.
- **Kinnistatud tootmistellimus** – täitmisaeg põhineb planeerimisel, mis kasutab protsessiteavet ja seotud ressursipiiranguid.

## <a name="delays"></a>Hilinemised

Kui nõutava materjali täitmisaeg on pikem kui periood tänase kuupäeva ja materjalivajaduse kuupäeva vahel, siis nõutava materjali plaanitud tellimus ja seotud tootmistellimus hilinevad. Plaanitud tellimuste puhul arvutatakse viivitus (päevades) väljastatud toote täitmisaja alusel. Viivituse teavet levitatakse seejärel kõigi koosluse struktuuri tasemete kaudu. Seega saate hilinenud toormaterjali mõju jälgida kogu tee kliendi müügitellimuseni.

## <a name="modifying-planned-orders"></a>Plaanitud tellimuste muutmine

Kui muudate plaanitud tellimuse teavet, saate järgmise teate: „Pange tähele, et plaanitud tellimustes käsitsi tehtud muudatuste mõju ei kajastu ülejäänud plaanis enne järgmise koondplaani käivitamist.”

Kui soovite muuta plaanitud tellimuse teavet ja vaadata mõju seotud materjalinõuetele, järgige järgmisi samme.

1. Värskendage plaanitud tellimust.
2. Kinnitage plaanitud tellimus.
3. Käivitage koondplaneerimine.

Koondplaneerimise käivitamisel ei tohiks kasutada filtreid, kui kaasatud on plaanitud tootmistellimused. Lisateavet vt selle artikli jaotisest [Filtrid](#filters).

> [!NOTE]
> Kui plaanitud tellimuse tarnekuupäev muudetakse hilisemaks kuupäevaks, võib nõudlus olla seotud uue plaanitud tellimusega. Selline käitumine ilmneb siis, kui uus tarnekuupäev põhjustab seotud nõudluse viivitusi, kuid vastavalt täitmisaja sätetele võib viivitusi vältida.

## <a name="explosion-page"></a>Koosluse leht

Saate kasutada lehte **Kooslus**, et analüüsida nõudlust, mis on vajalik konkreetse tootmistellimuse või plaanitud tootmistellimuse, seotud laovarude ja sidumisteabe jaoks. Teavet lehel **Kooslus** uuendatakse koondplaneerimise ajal. Teavet ei saa uuendada otse lehel **Kooslus**.

## <a name="filters"></a><a name="filters"></a>Filtrid

Selleks, et tagada koondplaneerimisel õige tulemuse arvutamiseks vajalik teave, peate kaasama kõik tooted, mis on mis tahes seosega toodetega plaanitud tellimuse kooslusestruktuuris. Tootmisega seotud stsenaariumite plaanimiseks on soovitatav vältida filtreeritud koondplaneerimise käitamist.

Kuigi sõltuvaid tütarüksusi tuvastati ja kaasatakse koondplaneerimisel automaatselt, siis taunitud koondplaneerimise mootori kasutamisel ei soorita plaanimise optimeerimine praegu seda tegevust.

Näiteks kui toote A koosluse struktuurist kasutatakse ka üksikut polti ka toote B tootmiseks, peavad filtrisse olema kaasatud kõik tooted, mis on toodete A ja B koosluse struktuuris. Kuna kõigi toodete filtri osa kindlustamine võib olla väga keerukas, on soovitatav vältida filtreeritud koondplaneerimise käivitamist tootmistellimuste puhul. Vastasel juhul annab koondplaneerimine soovimatud tulemused.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Filtreeritud koondplaneerimise käitamise vältimiseks

Kui käivitate toote filtreeritud koondplaneerimise, ei tuvasta plaanimise optimeerimine (erinevalt taunitud koondplaneerimise mootorist) kõiki alamtootmisi ja toormaterjale selle toote kooslusestruktuurist ja seega ei kaasa neid koondplaanimise käitusse. Isegi kui planeerimise optimeerimine tuvastab toote koosluse struktuuri esimese taseme, ei laadita andmebaasist tootesätteid (nt tellimuse vaiketüüp või kauba laovarud).

Rakenduse Planning Optimization laaditakse eelnevalt käituse andmed ja rakendatakse filtrid. See tähendab, et kui konkreetsesse tootesse kaasatud alltootmine või toormaterjal ei ole filtri osa, ei hõivata selle teavet käituse kohta. Lisaks, kui alltootmine või toormaterjal on kaasatud ka teise tootesse, siis filtreeritud käitus, mis sisaldab ainult algtoodet ja selle komponente, eemaldaks olemasoleva planeeritud nõudluse, mis loodi selle teise toote jaoks.

Selle loogikaga võidakse ootamatuid tulemusi anda filtreeritud koondplaneerimise käitamised. Järgmised jaotised pakuvad näiteid, mis illustreerivad ootamatuid tulemusi, mis võivad ilmneda.

### <a name="example-1"></a>Näide 1

Valmis toode *FG* koosneb järgmistest komponentidest:

- Toormaterjal *R*
- Alltootmine *S1*, mis koosneb alltootmisest *S2*

Toormaterjal *R* käsutuses on kaubavaru, samas kui laos puudub alaproduk *S1*.

Kui käivitate filtreeritud koondplaneerimise lõpetatud toote *FG* jaoks, saate plaanitud tootmistellimuse valmistootele *FG*, plaanitud ostutellimuse toormaterjali *R* ja plaanitud ostutellimuse alamtootmise *S1* jaoks. See on tulemuse andmine, kuna planeerimise optimeerimine on ignoreerinud tooraine *R* ja alltootmise *S1* olemasolevat tarnet tuleb toota *S2* abil, selle asemel, et seda otse tellida. See toimus, kuna planeerimise optimeerimisel on ainult lõpetatud kauba *FG* komponentide loend ilma seotud teabeta, nagu selle komponentide olemasolev tarne või tellimuse vaikesätted.

### <a name="example-2"></a>Näide 2

Eelmise näite põhjal toetudes kasutab täiendav lõpetatud toode *FG2*, ka alamtootmist *S1*. Valmis toode *FG2* tellimuste jaoks on plaanitud tellimus olemas ja kõikide selle komponentide puhul on plaanitud nõudlus, sealhulgas *S1*.

Otsustate planeerida eelmisest näitest pärit filtreeritud koondplaneerimise soovimatud tulemused, lisades filtrile kõik alltootmised ja toormaterjalid valmis *FG* kooslusestruktuurist ja käivitades seejäre täieliku taastootmise.

Kui käivitate täieliku taasloomise, kustutab süsteem kõik olemasolevad tulemused kõigi kaasatud toodete kohta ja taasloob tulemused uute arvutuste põhjal. See tähendab, et olemasolev planeeritud nõudlus tootele *S1* kustutatakse ja seejärel taaslooduna, võttes arvesse ainult lõpetatud toote *FG* nõudeid, samas kui eiratakse valmis toote *FG2* nõudeid. See juhtub, sest Planning Optimizatio käivitamisel ei sisalda see muude plaanitud tootmistellimuste plaanitud nõudlust, mida käitatakse&mdash;kasutatakse ainult käituse ajal loodud plaanitud nõudlust.

> [!NOTE]
> Kui valmis kauba *FG2* olemasolev plaanitud tellimus on olekus *Kinnitatud*, siis kaasatakse kinnitatud plaanitud nõudlus ka siis, kui ematoodet ei lisata filtrile.

Seega, kui te ei lisa lõpetatud *FG* kõiki komponente, valmis *FG2* tooteid ja kõiki muid tooteid, mille juurde need komponendid kuuluvad (koos nende komponentidega), annab filtreeritud koondplaneerimise käitaminesoovimatuid tulemusi.

Kuna kõigi toodete filtri osa kindlustamine võib olla väga keerukas, on soovitatav vältida filtreeritud koondplaneerimise käivitamist tootmistellimuste puhul.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
