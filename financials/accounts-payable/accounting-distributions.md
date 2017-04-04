---
title: Arvestuse jaotused
description: "Selles artiklis antakse teavet arvestuse jaotuste kohta ja kirjeldatakse nende töötlemiseks saadaolevaid võimalusi. Arvestuse jaotusi kasutatakse rahasummade eraldamiseks lähtedokumendi jaoks teatud pearaamatukontode puhul."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a98ce08dc115bc96cec07c2d6ced10d774785fe9
ms.openlocfilehash: b1057caae6f47e5a17e194834fbbcb9d7d731605
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-distributions"></a>Arvestuse jaotused

Selles artiklis antakse teavet arvestuse jaotuste kohta ja kirjeldatakse nende töötlemiseks saadaolevaid võimalusi. Arvestuse jaotusi kasutatakse rahasummade eraldamiseks lähtedokumendi jaoks teatud pearaamatukontode puhul. 

Arvestuse jaotused on programmiülene võimalus, mida kasutatakse ja laiendatakse iga lähtedokumendiga (nt ostutellimuse, hankija arve, kuluaruande ja vabas vormis arvega). Vaikimisi luuakse iga lähtedokumendi rea jaoks arvestuse jaotus ja rahasumma ning see on muutmiseks tingimuslikult lubatud. 

> [!Note] 
> Mõned dokumendid toetavad ka päise dokumendi rahalised suurused, näiteks tellimuste ja arvete eest. 

Üldised arvestuse jaotuse võimalused annavad arvestuse jaotuse töötlemiseks järgmised võimalused.

-   **Summade jaotamine** – saate kuvada ja muuta arvestuse jaotusi üksiku dokumendipäise või rea ja alamüksuste ridade kohta (nt maksud või tasud).
    -   Ülemise rahasumma jaotuse (põhijaotuse) puhul võib olla põhikontot ja finantsdimensioone võimalik redigeerida otse ruudustiku segmenditud sisestuse juhtelemendis. Laiendatud hind on sellise põhijaotuse tüüpiline näide.
    -   Jaotuste summad põhinevad dokumendi tingimuse valuutal. See valuuta on tavaliselt kandevaluuta. Arvestus- ja aruandlusvaluuta summad luuakse alammooduli raamatupidamise osana.
    -   Jaotustes kuvatakse aruandluskuupäev ja arvestussündmus. Tavaliselt on arvestussündmuse sätteks määratud **Pole**, kuni dokument on sisestatud / töölehele lisatud. Selles punktis saab arvestussündmuse olekuks **Algne**. Pärast jaotuste sisestamist ei saa jaotusi muuta.
    -   Põhijaotuste puhul võib olla lubatud nupp **Tükelda**. **Tükelda** loob uued arvestuse jaotused ja tükeldamine võib põhineda protsendil, summal või kogusel.
    -   Nuppu** Jaota võrdselt** saab kasutada koos nupuga **Tükelda** summa automaatseks eraldamiseks võrdselt kõigile jaotustele.
    -   Nupu **Lähtesta** saab lubada põhijaotuste puhul, kui on olemas rohkem kui üks jaotus. Nupp **Lähtesta** tühistab kõik jaotusele käsitsi tehtud muudatused, kustutades kõik olemasolevad jaotused ja luues uuesti vaikejaotused.
    -   Kõik alamjaotused, nagu allahindlus, tasu ja käibemaks, järgnevad alati põhijaotusele. Ema/tütre seost kell kuvatakse **viide**&gt;**vanem teavet**.
    -   Põhikontot ja finantsdimensioone võib olla võimalik redigeerida ka alamüksuste puhul.
    -   Arvestuste jaotuste finantsdimensioonid järgivad vaikemustrit, mida dokument võib laiendada. Täiendavad üksikasjad leiate seotud artiklitest.
    -   Hälbe jaotusi võidakse luua vastendamisstsenaariumides, nt hankija arve ja ostutellimuse vastendamisel. Saate vaadata raamatupidamise levik vastavaid suhteid **viide**&gt;**dokumenditeave**.
    -   Nupp **Paranda** kuvatakse ja on lubatud dokumentide puhul, mis toetavad parandusi. **Õige** loob uue jaotuse. Esiteks distributsioonid luuakse mis on algne jaotamist. Nende distributsioonid ei saa muuta. Next, uus õige raamatupidamise distributsioonid on loodud. Neid jaotusi saab muuta, kui algseid jaotusi sai muuta.
    -   Nupp** Projekti üksikasjad** lubatakse laiendusena, kui projektiga seostatakse rida. Projekti arvestuse jaotuste abil saate muuta üksikasju nagu näiteks rahastamise allikas ja rea atribuut.
    -   Saate vaadata praeguse dokumendi raamatupidamise olek **viide**. Olek on kogu dokumendis ja näitab, kas dokument on pooleli või lõpule viidud.
-   ** Vaata distributsioonid **-Vaata raamatupidamise jaotamist kõigi rea-ja rahasummad dokumendile. Selles vaates arvestuse jaotusi muuta ei saa.


Lisateabe saamiseks vaadake [raamatupidamise jagamisel ja subledger päevikukannete tasuta tekst arved](accounting-distributions-subledger-journal-entries-vendor-invoices.md).

