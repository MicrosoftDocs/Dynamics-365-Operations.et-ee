---
title: Konto struktuuride konfigureerimine
description: See artikkel annab teavet kontostruktuuride ja finantsdimensioonide kohta.
author: aprilolson
ms.date: 10/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3fbdd6e2cac61c358848a21e1126bea900e86b2
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713939"
---
# <a name="configure-account-structures"></a>Konto struktuuride konfigureerimine

[!include[banner](../includes/banner.md)]

Konto struktuurid kasutavad põhikontot ja finantsdimensioone, et luua reeglite kogumit, mis määravad konto numbri sisestamisel korra ja väärtused. Saate oma ettevõtte jaoks seadistada nii palju konto struktuure, kui vaja. Konto struktuurid määratakse ettevõtte pearaamatu seadistustele, nii et neid saab jagada.

Konto struktuuri loomisel on maksimaalne segmentide arv 11. Kui vajate rohkem kui 11 segmenti, hinnake põhjalikult oma seadistust ja nõudeid, kuna see mõjutab kasutajakogemust. Kaaluge, kas segmenti annaks hierarhiat kasutades tuletada aruandlusstsenaariumis, mitte andmesisestuse ajal, või tuletada kasutades kasutaja määratletud välja. Näiteks kui soovite aruannet asukoha kohta, kuid asukoha võite määrata osakonna või kulukeskuse kaupa, ei pea te asukohta finantsdimensiooniks. Kui te leiate pärast ülevaatust, et vaja on rohkem kui 11 segmenti, siis saate lisasegmente lisada täpsemate reeglite abil.

Konto struktuurid vajavad põhikontot. Põhikonto ei pea olema struktuuris esimene segment, kuid see määratleb, millist konto struktuuri kontonumbri kirje ajal kasutatakse. Seetõttu saab põhikonto väärtust pearaamatule määrata ainult ühes struktuuris, et nad ei kattuks. Pärast konto struktuuri määratlemist filtreeritakse lubatud väärtuste loend, et võimaldada kasutajal valida vaid sobivaid dimensiooniväärtusi, vähendades sellega vale töölehe sisestuse võimalust.

> [!NOTE] 
> Kui plaanite finantsdimensiooni suhtes eelarvet koostada, peab see olema konto struktuuri osa. Eelarvestamisel ei kasutata praegu täpsemaid reegleid.

## <a name="example"></a>Näide
Oletame konto struktuuri ülesseadmise hea tava illustreerimiseks, et ettevõte soovib jälgida bilansikontosid (100000–399999) konto ja äriüksuse finantsdimensiooni tasemel. Tulude ja kulude kontode (400000–999999) puhul jälgivad nad finantsdimensioone Äriüksus, Osakond ja Kulukeskus. Müügi tegemisel soovivad nad jälgida ka finantsdimensiooni Klient. Selle stsenaariumi kasutamisel soovitatakse määrata ettevõtte pearaamatule kaks kontostruktuuri – üks bilansikontode puhul ja teine kasumi- ja kahjumikontode jaoks. Kasutuskogemuse ja kinnitamise optimeerimiseks peaks dimensioon Klient olema täpsem reegel, mida kasutatakse vaid siis, kui kasutatakse müügikontot.

**Bilansikonto struktuur**

|Põhikonto          | Äriüksus    |
|----------------------|-----------|
|100000–399999 | *;"&nbsp;"|

**Tulu ja kulu konto struktuur**

|Põhikonto          | Äriüksus    |Osakond          | Kulukeskus    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000–999999 | \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"|

**Täpsem reegel kliendi lisamiseks**

Kriteerium: kui põhikonto on vahemikus 400000–499999, lisa klient. Seda ei saa tühjaks jätta.

|Klient         |
|-----------------|
|\* |

Selles lihtsustatud näites on lubatud kõik väärtused ja tühjad \* väärtused ning kasutatakse "&nbsp;".

## <a name="segments-and-allowed-values"></a>Segmendid ja lubatud väärtused
Jaotistes **Segmendid** ja **Lubatud väärtuse üksikasjad** saab tabelisse sisestada reegleid, mida järgitakse sisestamise ajal toimuval valideerimisel. Saate kirjutada otse tabeli lahtritesse, importida Excelist, või kasutada jaotist **Lubatud väärtuse üksikasjad**, mis teid juhendab.

Jaotis **Lubatud väärtuse üksikasjad** juhendab teid kriteeriumite loomisel, mis kasutavad **Tehtemärke** nagu algab väärtusega, vahel, hõlmab ja mitmeid teisi.

[![Luba väärtused.](./media/account.png)](./media/account.png) 

Lubatud väärtused sisestatakse vaikimisi töölehele või arvestuse jaotuse sisestamise lehele, kui konto struktuuri seadistuse järgi valimiseks pole muid võimalikke väärtusi.

Siin on näide **tulu ja kulu konto struktuurist**.

|Põhikonto          | Äriüksus    |Osakond          | Kulukeskus    |
|----------------------|-----------|----------------------|-----------|
|400000–999999 | 002 | 022 | 014 |

Töölehte sisestades ning kasumi ja kahjumi vahemikust kontot valides määrab äriüksus 002 väärtused 022 ja 014 kontrollkonto vaikeväärtusteks. See juhtub ka arvestuse jaotuse lehel. 

## <a name="more-than-seven-criteria-needed"></a>Rohkem kui 7 kriteeriumit on vajalikud

Kui teil on vaja üle seitsme kriteeriumi, saate jätkata nende lisamist järgmisele reale. Kui töötate jaotises Lubatud väärtuse **üksikasjad**, siis teate, **et pärast** sisestatud seitsmes kriteeriumi sisestamist pole +Lisa uued kriteeriumid enam aktiivsed. Seda mõjutavad järgmised tegurid. 
 - Veeru laius 
 - Kuidas andmeid talletatakse 
 - Juhtelemendi **Lubatud väärtuse üksikasjad** jõudlus
 - Kasutatavus  

> [!NOTE]
> Microsoft Dynamics AX Versiooni 2012 värskendus, kus määratud on üle 7 kriteeriumi, ei toetata. Enne finantside ja toimingute rakenduste uuendamise lõpule viimist tuleb see parandada. 

Täiendavate kriteeriumide lisamiseks klõpsake **Dubleeri segmendis** ja **Lubatud väärtuste jaotis**. Sellega kopeeritakse kriteeriumid uuele reale. Seejärel saate jaotisesse **Lubatud väärtuse üksikasjad** kirjutada või seda muuta.

## <a name="best-practices"></a>Head tavad
Konto struktuuri seadistamisel on mõned head tavad, mida saate järgida. See on siiski vaid juhis, nii et terviklik arutelu teie ettevõtte, kasvuplaani ja halduse kohta peaks olema selle arutelu osa.

- Tehke põhikonto esmalt või nii lähedale konto struktuuri ette kui võimalik, et kasutajad saaksid kõige paremini juhendatud kogemust konto sisestamise ajal.
  
  - Kontrollige, et mis tahes kolmanda osapoole lahendused, mida soovite kasutada, toetavad põhikontot esimesel positsioonil.

- Taaskasutage konto struktuure võimalikult palju, et vähendada juriidiliste isikute haldamise vaeva.

- Kaaluge juriidiliste isikute erinevuste jaoks täpsemate reeglite kasutamist, nii et konto struktuure saaks taaskasutada.

- Kasutage lubatud väärtuste määratlemisel nii palju vahemikke ja metamärke kui võimalik. Peale selle, et see võimaldab teil haldamise vaevadeta kasvada ja muutuda, toimib süsteem sellise konfiguratsiooniga kõige paremini.

- Ärge sisestage igasse konto struktuuri segmenti tärni, et toetuda vaid täpsematele reeglitele. Seda võib olla raske hallata ja tihtipeale põhjustab see haldamise ajal kasutaja vigasid, mistõttu ei suuda süsteem sisestada.

## <a name="account-structure-activation"></a>Konto struktuuri aktiveerimine
Kui olete uue seadistuse või konto struktuuri muudatusega rahul, peate selle aktiveerima. Kui konto struktuur on määratud pearaamatule, siis võib aktiveerimine võtta kaua aega, kuna kõik süsteemi sisestamata kanded tuleb sünkroonida uue struktuuriga. Konto struktuuri muudatused ei mõjuta sisestatud kandeid. Rakenduse versiooni 10.0.31 järgi on funktsioonihalduses saadaval uus funktsioon nimega **Konto** struktuuri aktiveerimise jõudluse täiustus. Lisateavet selle uue funktsiooni kohta konto struktuuri aktiveerimiseks vt Konto struktuuri [aktiveerimise jõudluse täiustus.](account-structure-improvement.md) 

Lisateavet vt oma kontoplaani [, finantsdimensioonide](plan-chart-of-accounts.md)[...](financial-dimensions.md)[ning konto- ja dimensioonikombinatsioonide sisestamise kohta (segmenditud kirje kontroll).](enter-account-dimension-combinations-segmented-entry-control.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
