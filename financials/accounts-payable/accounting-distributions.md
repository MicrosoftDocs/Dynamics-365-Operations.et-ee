---
title: Arvestuse jaotused
description: "Selles artiklis antakse teavet arvestuse jaotuste kohta ja kirjeldatakse nende töötlemiseks saadaolevaid võimalusi. Arvestuse jaotusi kasutatakse rahasummade eraldamiseks lähtedokumendi jaoks teatud pearaamatukontode puhul."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 96ff984310ce5877c37a22f182064a5038d71752
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="accounting-distributions"></a>Arvestuse jaotused

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet arvestuse jaotuste kohta ja kirjeldatakse nende töötlemiseks saadaolevaid võimalusi. Arvestuse jaotusi kasutatakse rahasummade eraldamiseks lähtedokumendi jaoks teatud pearaamatukontode puhul. 

Arvestuse jaotused on programmiülene võimalus, mida kasutatakse ja laiendatakse iga lähtedokumendiga (nt ostutellimuse, hankija arve, kuluaruande ja vabas vormis arvega). Vaikimisi luuakse iga lähtedokumendi rea jaoks arvestuse jaotus ja rahasumma ning see on muutmiseks tingimuslikult lubatud. 

> [!Note] 
> Mõned dokumendid toetavad ka päisedokumendi rahasummasid, nagu tellimuste ja arvete tasud. 

Üldised arvestuse jaotuse võimalused annavad arvestuse jaotuse töötlemiseks järgmised võimalused.

-   **Summade jaotamine** – saate kuvada ja muuta arvestuse jaotusi üksiku dokumendipäise või rea ja alamüksuste ridade kohta (nt maksud või tasud).
    -   Ülemise rahasumma jaotuse (põhijaotuse) puhul võib olla põhikontot ja finantsdimensioone võimalik redigeerida otse ruudustiku segmenditud sisestuse juhtelemendis. Laiendatud hind on sellise põhijaotuse tüüpiline näide.
    -   Jaotuste summad põhinevad dokumendi tingimuse valuutal. See valuuta on tavaliselt kandevaluuta. Arvestus- ja aruandlusvaluuta summad luuakse alammooduli raamatupidamise osana.
    -   Jaotustes kuvatakse aruandluskuupäev ja arvestussündmus. Tavaliselt on arvestussündmuse sätteks määratud **Pole**, kuni dokument on sisestatud / töölehele lisatud. Selles punktis saab arvestussündmuse olekuks **Algne**. Pärast jaotuste sisestamist ei saa jaotusi muuta.
    -   Põhijaotuste puhul võib olla lubatud nupp **Tükelda**. **Tükelda** loob uued arvestuse jaotused ja tükeldamine võib põhineda protsendil, summal või kogusel.
    -   Nuppu**Jaota võrdselt** saab kasutada koos nupuga **Tükelda** summa automaatseks eraldamiseks võrdselt kõigile jaotustele.
    -   Nupu **Lähtesta** saab lubada põhijaotuste puhul, kui on olemas rohkem kui üks jaotus. Nupp **Lähtesta** tühistab kõik jaotusele käsitsi tehtud muudatused, kustutades kõik olemasolevad jaotused ja luues uuesti vaikejaotused.
    -   Kõik alamjaotused, nagu allahindlus, tasu ja käibemaks, järgnevad alati põhijaotusele. Põhi-/alamüksuse seost saab vaadata jaotises **Viide** &gt; **Põhidokumendi teave**.
    -   Põhikontot ja finantsdimensioone võib olla võimalik redigeerida ka alamüksuste puhul.
    -   Arvestuste jaotuste finantsdimensioonid järgivad vaikemustrit, mida dokument võib laiendada. Täiendavad üksikasjad leiate seotud artiklitest.
    -   Hälbe jaotusi võidakse luua vastendamisstsenaariumides, nt hankija arve ja ostutellimuse vastendamisel. Arvestuse jaotuse vastendamise seoseid saab vaadata jaotises **Viide** &gt; **Dokumendi teave**.
    -   Nupp **Paranda** kuvatakse ja on lubatud dokumentide puhul, mis toetavad parandusi. Nupp **Paranda** loob uued jaotused. Esmalt luuakse need jaotused, mis tühistavad algsed jaotused. Neid jaotusi ei saa muuta. Seejärel luuakse uued õiged arvestuse jaotused. Neid jaotusi saab muuta, kui algseid jaotusi sai muuta.
    -   Nupp**Projekti üksikasjad** lubatakse laiendusena, kui projektiga seostatakse rida. Projekti arvestuse jaotuste abil saate muuta üksikasju nagu näiteks rahastamise allikas ja rea atribuut.
    -   Praeguse dokumendi raamatupidamisolekut saab vaadata jaotises **Viide**. Olek kehtib kogu dokumendi puhul ja näitab, kas dokument on lõpetamata või lõpetatud.
-   **Jaotuste kuvamine** – saate kuvada arvestuse jaotused kõigi dokumendi ridade ja rahasummade kohta. Selles vaates arvestuse jaotusi muuta ei saa.


Lisateavet leiate teemast [Arvestuse jaotused ja alammooduli töölehe kirjed vabas vormis arvete puhul](accounting-distributions-subledger-journal-entries-vendor-invoices.md).



