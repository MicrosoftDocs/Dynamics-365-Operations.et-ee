---
title: Arvestuse jaotused
description: Selles teemas leidub teave arvestuse jaotuste kohta ja kirjeldatakse nende töötlemiseks saadaolevaid võimalusi.
author: ShylaThompson
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3901fb61c1c8f9a9fd13b8ea558877daf884f3ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972227"
---
# <a name="accounting-distributions"></a>Arvestuse jaotused

[!include [banner](../includes/banner.md)]

Selles teemas leidub teave arvestuse jaotuste kohta ja kirjeldatakse nende töötlemiseks saadaolevaid võimalusi. Arvestuse jaotusi kasutatakse rahasummade eraldamiseks lähtedokumendi jaoks teatud pearaamatukontode puhul. 

Arvestuse jaotused on programmiülene võimalus, mida kasutatakse ja laiendatakse iga lähtedokumendiga (nt ostutellimuse, hankija arve, kuluaruande ja vabas vormis arvega). Vaikimisi luuakse iga lähtedokumendi rea jaoks arvestuse jaotus ja rahasumma ning see on muutmiseks tingimuslikult lubatud. 

> [!NOTE] 
> Mõned dokumendid toetavad ka päisedokumendi rahasummasid, nagu tellimuste ja arvete tasud. 

Üldised arvestuse jaotuse võimalused annavad arvestuse jaotuse töötlemiseks järgmised võimalused.

-   **Summade jaotamine** – saate kuvada ja muuta arvestuse jaotusi üksiku dokumendipäise või rea ja alamüksuste ridade kohta (nt maksud või tasud).
    -   Ülemise rahasumma jaotuse (põhijaotuse) puhul võib olla põhikontot ja finantsdimensioone võimalik redigeerida otse ruudustiku segmenditud sisestuse juhtelemendis. Laiendatud hind on sellise põhijaotuse tüüpiline näide.
    -   Jaotuste summad põhinevad dokumendi tingimuse valuutal. See valuuta on tavaliselt kandevaluuta. Arvestus- ja aruandlusvaluuta summad luuakse alammooduli raamatupidamise osana.
    -   Jaotustes kuvatakse aruandluskuupäev ja arvestussündmus. Tavaliselt on arvestussündmuse sätteks määratud **Pole**, kuni dokument on sisestatud / töölehele lisatud. Selles punktis saab arvestussündmuse olekuks **Algne**. Pärast jaotuste sisestamist ei saa jaotusi muuta.
    -   Põhijaotuste puhul võib olla lubatud nupp **Tükelda**. **Tükelda** loob uued arvestuse jaotused ja tükeldamine võib põhineda protsendil, summal või kogusel.
    -   Nuppu **Jaota võrdselt** saab kasutada koos nupuga **Tükelda** summa automaatseks eraldamiseks võrdselt kõigile jaotustele.
    -   Nupu **Lähtesta** saab lubada põhijaotuste puhul, kui on olemas rohkem kui üks jaotus. Nupp **Lähtesta** tühistab kõik jaotusele käsitsi tehtud muudatused, kustutades kõik olemasolevad jaotused ja luues uuesti vaikejaotused.
    -   Kõik alamjaotused, nagu allahindlus, tasu ja käibemaks, järgnevad alati põhijaotusele. Põhi-/alamüksuse seost saab vaadata jaotises **Viide** &gt; **Põhidokumendi teave**.
    -   Põhikontot ja finantsdimensioone võib olla võimalik redigeerida ka alamüksuste puhul.
    -   Arvestuste jaotuste finantsdimensioonid järgivad vaikemustrit, mida dokument võib laiendada.
    -   Hälbe jaotusi võidakse luua vastendamisstsenaariumides, nt hankija arve ja ostutellimuse vastendamisel. Arvestuse jaotuse vastendamise seoseid saab vaadata jaotises **Viide** &gt; **Dokumendi teave**.
    -   Nupp **Paranda** kuvatakse ja on lubatud dokumentide puhul, mis toetavad parandusi. Nupp **Paranda** loob uued jaotused. Esmalt luuakse need jaotused, mis tühistavad algsed jaotused. Neid jaotusi ei saa muuta. Seejärel luuakse uued õiged arvestuse jaotused. Neid jaotusi saab muuta, kui algseid jaotusi sai muuta.
    -   Nupp **Projekti üksikasjad** lubatakse laiendusena, kui projektiga seostatakse rida. Projekti arvestuse jaotuste abil saate muuta üksikasju nagu näiteks rahastamise allikas ja rea atribuut.
    -   Praeguse dokumendi raamatupidamisolekut saab vaadata jaotises **Viide**. Olek kehtib kogu dokumendi puhul ja näitab, kas dokument on lõpetamata või lõpetatud.
-   **Jaotuste kuvamine** – saate kuvada arvestuse jaotused kõigi dokumendi ridade ja rahasummade kohta. Selles vaates arvestuse jaotusi muuta ei saa.

Versioonis 10.0.13 lisati funktsioon, mis kontrollib arvestuse jaotuse tabelit, et tagada uute väljade õigesti seadistamine. Selle funktsiooni nimi on **Luba andmete täiendav kontrollimine dokumentide puhul, mis kasutavad lähtedokumendi raamatupidamisraamistikku**. Funktsiooni kasutamiseks peate selle lubama tööruumis **Funktsioonihaldus**. Funktsiooni lubamiseks otsige funktsiooni nime väljal **Otsing**, mis asub lehel **Funktsioonihaldus**, ja seejärel valige **Luba kohe**.

Lisateabe saamiseks vaadake jaotist [Arvestuse jaotus ja alammooduli töölehe kirjed hankija arvete jaoks](accounting-distributions-subledger-journal-entries-vendor-invoices.md).
