---
title: "Arvestus- või aruandlusvaluutade teisendamine"
description: 
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 728af2fff6317c17e47d48ea07dbeb57068fbf3f
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>Arvestus- või aruandlusvaluutade teisendamine

[!include[banner](../includes/banner.md)]




Ettevõttel, mis peab muutma oma arvestusvaluutat või aruandlusvaluutat, on kaks võimalust. Esimene võimalus on luua uus ettevõte ja alustada otsast peale. Teine võimalus on käivitada arvestus-- ja aruandlusvaluuta teisenduse protsess. See on väga pikaajalisne protsess, mis muudab süsteemis iga kannet. Enne protsessi käitamist on nõutav ka mõningane seadistus.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Juriidilise isiku ettevalmistamine valuutateisenduseks
Enne juriidilise isiku valuuta teisendamist peate ennistama kõik kliendi ja hankija kontode välisvaluuta ümberarvutamise summad ning sulgema eelmised rahandusaastad. Peate ka andmebaasi teisenduseks ette valmistama ning seejärel tegema juriidilise isiku kontole, millel toimub valuutateisendus, nõutud muudatused. Kui olete valuutateisenduse lõpule viinud, peate tegema veel mõne täiendava toimingu. Peate teisendatud summade ümarduserinevused vastavusse viima, äristatistika ümber arvutama, pearaamatukanded töölehele paigutama, piirama juurdepääsu teisendustööriistale ning välisvaluutade summad kliendi- ja hankijakontode jaoks ümber hindama.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Automaatsete kannete kontode seadistamine
Valuutateisendusprotsessi ajal sisestatakse kasumid või kahjumid või sendierinevused lehel **Automaatsete kannete kontod** määratletud kontodele. Enne teisendusprotsessi käivitamist tuleb põhikontod määrata järgmist tüüpi kannetele.

-   Arvestusvaluuta konversiooni tulu
-   Arvestusvaluuta konversiooni kulu
-   Arvestusvaluuta sendierinevus
-   Sendierinevus aruandlusvaluutas
-   Aastalõpu tulemus

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Ümarduserinevuste ja ümberarvutuste sisestamine
Järgmine teave selgitab, kust võivad tekkida ümardamisel erinevused.

-   Tootehindade nulliks (0) teisendamisel luuakse aruanne, millel kuvatakse tootenumber, mooduli tüüp, teisenduseelne hind ja ühik.
-   Käibemaksu ja pearaamatu vahel tekkinud ümardusvahed sisestatakse pearaamatusse.
-   Välisvaluuta ümberarvutamise summad ning kliendi- ja hankijakannete summad arvutatakse ümber.
-   Iga kliendi- ja hankijakande ümardusvahede jaoks luuake kliendi ja hankija tasakaalustuskirjed.
-   Klientide ja hankijate ümardusvahed sisestatakse pearaamatusse.
-   Tasakaalustatud omahind ja omahinna korrigeerimissummad suletud laokannetes arvutatakse ümber.
-   Laohalduse ümardusvahed sisestatakse pearaamatusse.
-   Vaba kaubavaru arvutatakse ümber.
-   Pearaamatu töölehtede kogusummad arvutatakse ümber.
-   Pearaamatu sulgemislehed arvutatakse ümber.
-   Pearaamatusaldod arvutatakse ümber.
-   Pearaamatu ümardusvahed sisestatakse pearaamatusse.
-   Pearaamatu avamiskanded arvutatakse ümber.
-   Arvutatakse pearaamatusaldode lõplik summa.

Kui teisendate uueks pearaamatu arvestusvaluutaks ja kogusummade ümberarvutamisel või ümarduserinevuste sisestamisel ilmneb viga, peate lehe **Pearaamatu arvestusvaluuta teisendus** sulgema. Kogusummad arvutatakse ümber ja ümarduserinevused sisestatakse.

## <a name="processing-the-currency-conversion"></a>Valuutateisenduse töötlemine
Valuutateisenduse protsessi käivitamisel tuleb kõik kasutajad süsteemist välja logida. Peate määratlema uue pearaamatu või aruandlusvaluuta ja vahetuskursid. Kui klõpsate **OK**, käivitub protsess ja värskendab süsteemis kõik kanded. Valuutateisendus on väga pikk protsess. Kui see on lõpule viidud, näete värskendatud arvestus- või aruandlusvaluutat lehel **Pearaamat**.

## <a name="completing-the-currency-conversion"></a>Valuutateisenduse lõpule viimine
Pärast valuutateisendust peate kõik vastavusse viimise aruanded uuesti looma, et tagada kõigi teisendatud summade õigsus.

-   Kui pearaamatu arvestusvaluuta teisendus põhjustab ümarduserinevusi, ei sisestata neid erinevusi kande abil kohas, kus ümarduserinevus ilmnes. Selle asemel sisestatakse erinevused kande abil, mis sisestati teisendussisestuste jaoks. Need ümarduserinevused kuvatakse kõigis teisendusjärgsetes kande- ja kuupäevakontrolliga aruannetes. See käitumine on õige ja seda võib eirata.
-   Kui kliendi ja hankija vastavusseviimise aruannetel kuvatakse kogu rea erinevussumma ja erinevussummat enne teisendust ei olnud, tuleb see erinevussumma sisestada. Konto on koondkonto klientide ja hankijate jaoks. Vastaskonto on pearaamatukonto teisenduse kulu või teisenduse tulu jaoks.

Kui kõik pearaamatu kandetöölehed on kustutatud, saate pearaamatukanded töölehele paigutada. Klõpsake valikuid **Pearaamat** &gt; **Perioodiline** &gt; **Töölehed** &gt; **Töölehele paigutamine**. Pärast valuutateisenduse, saab välisvaluuta summad ümber hinnata, kui ümberhindamine on nõutav. Saate välisvaluuta summad ümber hinnata, valides ümberhindamise jaotises välja **Meetod** suvandiks **Standardne**.




