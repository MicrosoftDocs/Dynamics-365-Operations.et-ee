---
title: Konto struktuuride konfigureerimine
description: Teema sisaldab teavet konto struktuuride ja finantsdimensioonide kohta.
author: aprilolson
manager: AnnBe
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55c3d6c0f2cddb4da8fd82f26ca3184b194e174b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975887"
---
# <a name="configure-account-structures"></a>Konto struktuuride konfigureerimine

[!include[banner](../includes/banner.md)]

Konto struktuurid kasutavad põhikontot ja finantsdimensioone, et luua reeglite kogumit, mis määravad konto numbri sisestamisel korra ja väärtused. Saate oma ettevõtte jaoks seadistada nii palju konto struktuure, kui vaja. Konto struktuurid määratakse ettevõtte pearaamatu seadistusele, nii et neid saab jagada.

Konto struktuuri loomisel on maksimaalne segmentide arv 11. Kui vajate rohkem segmente, siis vaadake põhjalikult üle oma seadistus ja nõuded, sest see mõjutab kasutuskogemust. Kaaluge, kas segmenti annaks hierarhiat kasutades tuletada aruandlusstsenaariumis, mitte andmesisestuse ajal, või tuletada kasutades kasutaja määratletud välja. Näiteks kui soovite asukohta määratleda, kuid saate seda välja nuputada osakonna või kulukeskuse alusel, siis pole teil asukohta finantsdimensioonina vaja. Kui te leiate pärast ülevaatust, et vaja on rohkem kui 11 segmenti, siis saate lisasegmente lisada täpsemate reeglite abil.

Konto struktuurid vajavad põhikontot. Põhikonto ei pea olema struktuuris esimene segment, kui see näitab konto numbri sisestamisel, millist konto struktuuri kasutatakse. Seetõttu saab põhikonto väärtus olla vaid ühes pearaamatule määratud struktuuris, et vältida kattumist. Pärast konto struktuuri määratlemist filtreeritakse lubatud väärtuste loend, et võimaldada kasutajal valida vaid sobivaid dimensiooniväärtusi, vähendades sellega vale töölehe sisestuse võimalust.

> [!NOTE] 
> Kui plaanite finantsdimensiooni suhtes eelarvet koostada, peab see olema konto struktuuri osa. Eelarvestamisel ei kasutata praegu täpsemaid reegleid.

## <a name="example"></a>Näide
Oletame konto struktuuri ülesseadmise hea tava illustreerimiseks, et ettevõte soovib jälgida bilansikontosid (100000–399999) konto ja äriüksuse finantsdimensiooni tasemel. Tulude ja kulude kontode (400000–999999) puhul jälgivad nad finantsdimensioone Äriüksus, Osakond ja Kulukeskus. Müügi tegemisel soovivad nad jälgida ka finantsdimensiooni Klient. Selle stsenaariumi puhul oleks soovitatav kasutada kahte ettevõtte pearaamatule määratud konto struktuuri – üks Bilansikontode ning teine Tulu ja kulu kontode jaoks. Kasutuskogemuse ja kinnitamise optimeerimiseks peaks dimensioon Klient olema täpsem reegel, mida kasutatakse vaid siis, kui kasutatakse müügikontot.

**Bilansikonto struktuur**

|Põhikonto          | Äriüksus    |
|----------------------|-----------|
|100000–399999 | *; „ “|

**Tulu ja kulu konto struktuur**

|Põhikonto          | Äriüksus    |Osakond          | Kulukeskus    |
|----------------------|-----------|----------------------|-----------|
|400000–999999 | *; „ “|*; „ “|*; „ “|*; „ “|

**Täpsem reegel kliendi lisamiseks**

Kriteerium: kui põhikonto on vahemikus 400000–499999, lisa klient. Välja ei tohi tühjaks jätta.

|Klient         |
|-----------------|
|* |

Selles lihtsustatud näites on lubatud kõik väärtused ja tühjad väärtused, mida tähistatakse sümbolitega * ja „ “.

## <a name="segments-and-allowed-values"></a>Segmendid ja lubatud väärtused
Jaotistes **Segmendid** ja **Lubatud väärtuse üksikasjad** saab tabelisse sisestada reegleid, mida järgitakse sisestamise ajal toimuval valideerimisel. Saate kirjutada otse tabeli lahtritesse, importida Excelist, või kasutada jaotist **Lubatud väärtuse üksikasjad**, mis teid juhendab.

Jaotis **Lubatud väärtuse üksikasjad** juhendab teid kriteeriumite loomisel, mis kasutavad **Tehtemärke** nagu algab väärtusega, vahel, hõlmab ja mitmeid teisi.

[![Lubatud väärtused](./media/account.png)](./media/account.png) 

Lubatud väärtused sisestatakse vaikimisi töölehele või arvestuse jaotuse sisestamise lehele, kui konto struktuuri seadistuse järgi valimiseks pole muid võimalikke väärtusi.

Siin on näide **tulu ja kulu konto struktuurist**.

|Põhikonto          | Äriüksus    |Osakond          | Kulukeskus    |
|----------------------|-----------|----------------------|-----------|
|400000–999999 | 002 | 022 | 014 |

Töölehte sisestades ning kasumi ja kahjumi vahemikust kontot valides määrab äriüksus 002 väärtused 022 ja 014 kontrollkonto vaikeväärtusteks. See juhtub ka arvestuse jaotuse lehel. 

## <a name="more-than-7-criteria-needed"></a>Rohkem kui 7 kriteeriumit

Kui teil on vaja rohkem kui 7 kriteeriumit, saate nende lisamist jätkata järgmisel real. Jaotises **Lubatud väärtuse üksikasjad** töötades märkate, et kriteerium **+ Lisa uus** pole enam pärast seitsmenda kriteeriumi sisestamist aktiivne. Seda mõjutavad järgmised tegurid. 
 - Veeru laius 
 - Kuidas andmeid talletatakse 
 - Juhtelemendi **Lubatud väärtuse üksikasjad** jõudlus
 - Kasutatavus  
 
Täiendavate kriteeriumide lisamiseks klõpsake **Dubleeri segmendis** ja **Lubatud väärtuste jaotis**. Sellega kopeeritakse kriteeriumid uuele reale. Seejärel saate jaotisesse **Lubatud väärtuse üksikasjad** kirjutada või seda muuta.

## <a name="best-practices"></a>Head tavad
Konto struktuuride ülesseadmisel on välja kujunenud mõned head tavad, mida järgida saate. See on siiski vaid juhis, nii et terviklik arutelu teie ettevõtte, kasvuplaani ja halduse kohta peaks olema selle arutelu osa.

- Looge põhikonto struktuuri esimeseks osaks või sellele võimalikult lähedale, et kasutajad saaksid konto sisestamise ajal parima juhendatud kogemuse.

- Taaskasutage konto struktuure võimalikult palju, et vähendada juriidiliste isikute haldamise vaeva.

- Kaaluge juriidiliste isikute erinevuste jaoks täpsemate reeglite kasutamist, nii et konto struktuure saaks taaskasutada.

- Kasutage lubatud väärtuste määratlemisel nii palju vahemikke ja metamärke kui võimalik. Peale selle, et see võimaldab teil haldamise vaevadeta kasvada ja muutuda, toimib süsteem sellise konfiguratsiooniga kõige paremini.

- Ärge sisestage igasse konto struktuuri segmenti tärni, et toetuda vaid täpsematele reeglitele. Seda võib olla raske hallata ja tihtipeale põhjustab see haldamise ajal kasutaja vigasid, mistõttu ei suuda süsteem sisestada.

## <a name="account-structure-activation"></a>Konto struktuuri aktiveerimine
Kui olete konto struktuuri häälestuse või muudatusega rahul, tuleb see aktiveerida. Kui konto struktuur on määratud pearaamatule, siis võib aktiveerimine võtta kaua aega, kuna kõik süsteemi sisestamata kanded tuleb sünkroonida uue struktuuriga. Konto struktuuri muudatused ei mõjuta sisestatud kandeid.

Lisateabe saamiseks vaadake jaotisi [Kontoplaanide plaanimine](plan-chart-of-accounts.md), [Finantsdimensioonid](financial-dimensions.md) ja [Konto ja dimensioonide kombinatsioonide sisestamine (segmenditud sisestamise juhtimine)](enter-account-dimension-combinations-segmented-entry-control.md).
