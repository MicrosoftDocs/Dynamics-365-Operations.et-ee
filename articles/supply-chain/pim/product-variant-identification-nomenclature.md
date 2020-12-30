---
title: Tootevariandi numbrite ja nimede nomenklatuur
description: See teema kirjeldab, kuidas seadistada tootenumbri nomenklatuuri fikseeritud [Tooteetaloni number – Konfiguratsioon – Suurus – Värv – Laad] vormingu asendamiseks.
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 90c01e4281246d890ef888c56ca137f83e83741c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426028"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Tootevariandi numbrite ja nimede nomenklatuur

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada tootenumbri nomenklatuuri fikseeritud [Tooteetaloni number – Konfiguratsioon – Suurus – Värv – Laad] vormingu asendamiseks. Uuel nomenklatuuril on sihipärane vorming, mis sisaldab tooteetaloni numbrit, aktiivseid tootedimensioone ja teie valitud teksti eraldajaid. Nomenklatuuri saab luua ka tootenimede kohta. Lõpuks saab koostada nomenklatuuri piirangupõhise tootekonfiguraatoriga loodud konfiguratsioonide tuvastamiseks. Need nomenklatuurid võivad sisaldada teie valitud atribuute.

Tootevariandi numbrite ja nimede uued nomenklatuurid võimaldavad kaasata identifikaatoritesse tootevariantide segmente. Need segmendid võivad sisaldada tooteetaloni numbrit ja nime, tootedimensiooni ID-sid ja nimesid, numbriseeriaid, tekstikonstante ja atribuute. See funktsionaalsus võimaldab teil müügitellimuse või ostutellimuse loomisel kiiresti leida konkreetse tootevariandi. Nomenklatuure saab luua nii tootevariandi numbrite kui ka nimede kohta, kasutades lehte **Toote nomenklatuur**. Selle lehe avamiseks klõpsake nuppe **Tooteteabe haldus** &gt; **Seadistus**.

## <a name="nomenclature-of-predefined-product-variants"></a>Eelmääratletud tootevariantide nomenklatuur
Tootevariandid luuakse tooteetalonidele vastavalt ühele kolmest konfiguratsioonitehnoloogiast.

-   Eelmääratletud variandid
-   Piirangupõhised
-   Dimensioonipõhised

Igal tootevariandil on number ja nimi ning tootevariandi ID nomenklatuurid võimaldavad valida segmendid, mida kaasatakse igas tootevariandi numbris või nimes. Saate valida lehel **Toote nomenklatuur** järgmisi segmente.

-   Tooteetaloni number
-   Tooteetaloni nimi
-   Numbriseeria väärtus
-   Tekstikonstant
-   Tootedimensioonid
    -   Konfiguratsiooni ID või nimi
    -   Värvi ID või nimi
    -   Suuruse ID või nimi
    -   Laadi ID või nimi

Pärast tootevariandi ID-numbri nomenklatuuri määratlemist saab selle seostada tootedimensioonigrupiga. Kõigile sellele tootedimensioonigrupile viitavatele tooteetalonidele määratakse siis nomenklatuuri põhjal tootevariandi numbrid. Kuid tootevariandi nime nomenklatuure ei saa tootedimensiooni gruppidega seostada. Tootevariandi ID nomenklatuuri saab seostada ka otse tooteetaloniga. Sel juhul määratakse tooteetaloni juurde kuuluvatele tootevariantidele nomenklatuuride alusel tootevariandi numbrid ja nimed.

### <a name="example"></a>Näide

T-särki (TS1234) toodetakse kolmes suuruses (S, M, L), nelja värvi (punane, roheline, sinine, kollane) ja kahes stiilis (polo, V). Seetõttu on võimalikud 24 tootevarianti (= 3 × 4 × 2). Loote tootevariandi numbri nomenklatuuri, millel on järgmised segmendid.

1.  Tooteetaloni number
2.  Tekstikonstant: „-”
3.  Värv
4.  Tekstikonstant: „-”
5.  Suurus
6.  Tekstikonstant: „-”
7.  Laad

Sellisel juhul on tootevariandi number punase väikese polosärgi puhul TS1234-punane-väike-polo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Piirangupõhiste konfiguratsioonide nomenklatuur
Piirangupõhiste konfiguratsioonide puhul saab tootedimensiooni konfigureerimiseks luua spetsiaalse nomenklatuuri. Saate valida lehel **Toote nomenklatuur** järgmisi segmente.

-   Numbriseeria väärtus
-   Tekstikonstant
-   Atribuudi väärtus

Igal toote konfiguratsioonimudelis oleval komponendil võib olla oma konfiguratsiooninomenklatuur. Kasutada saab ainult komponendile kuuluvaid atribuute. Alamkomponente või kasutajanõuete atribuute ei saa kasutada.

### <a name="example"></a>Näide

Toote konfiguratsioonimudelil on kahe atribuudiga juurkomponent.

-   Materjal (plast, puit, teras)
-   Pikkus (10...100)

Loote konfiguratsiooni nomenklatuuri, millel on järgmised segmendid.

1.  Atribuudi väärtus: materjal
2.  Tekstikonstant: „AAA”
3.  Atribuudi väärtus: pikkus

Sellisel juhul on konfiguratsiooni ID puitmaterjali puhul pikkusega 78 PuitAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Dimensioonipõhiste konfiguratsioonide nomenklatuur
Dimensioonipõhiste konfiguratsioonide puhul saab tootedimensiooni konfigureerimiseks luua spetsiaalse nomenklatuuri. Saate valida lehel **Toote nomenklatuur** järgmisi segmente.

-   Numbriseeria väärtus
-   Tekstikonstant
-   Konfiguratsioonigrupi kaup

Konfiguratsiooninomenklatuuri saab määratleda kooslusele.

### <a name="example"></a>Näide

Kooslusel on neli koosluserida, mis on jagatud kaheks konfiguratsioonigrupiks.

-   Koosluserida: M0007, standardkorpus
    -   Konfiguratsioonigrupp: korpus
-   Koosluserida: M0008, tipptasemel korpus
    -   Konfiguratsioonigrupp: korpus
-   Koosluserida: M0021, kangast esivõre
    -   Konfiguratsioonigrupp: esivõre
-   Koosluserida: M0022, metallist esivõre
    -   Konfiguratsioonigrupp: esivõre

Loote konfiguratsiooni nomenklatuuri, millel on järgmised segmendid.

1.  Konfiguratsioonigrupp: korpus
2.  Tekstikonstant: „&”
3.  Konfiguratsioonigrupp: esivõre

Sellisel juhul on kangast esivõrega standardse korpuse konfiguratsiooni-ID M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Tootevariantide ja konfiguratsioonide kombinatsiooni nomenklatuur
Kui kasutate tooteetalonile tootevariantide konfigureerimiseks piirangupõhist või dimensioonipõhist konfiguratsioonitehnoloogiat, võivad tootevariantide tootevariandi numbrid hõlmata konfiguratsioonidimensioonist pärit nomenklatuuri. Variantide konfigureerimiseks tehke järgmist.

1.  Määratlege lehel **Toote nomenklatuur** tootevariandi numbrite nomenklatuur, mis sisaldab konfiguratsioonidimensiooni.
2.  Määrake see nomenklatuur konfiguratsioonidimensiooniga tootedimensioonigrupile.
3.  Määratlege konfiguratsiooninomenklatuur komponentidele või kooslustele, mida kasutatakse tootevariantide konfigureerimiseks.

Nomenklatuure saab luua ka tootevariantide nimedele. Tootevariantide nimed saab konfigureerida nii, et need sisaldaksid konfiguratsiooni ID-d või nime.

### <a name="example-for-constraint-based-configurations"></a>Piirangupõhiste konfiguratsioonide näide

Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.

1.  Tooteetaloni number
2.  Tekstikonstant: „\_”
3.  Konfiguratsioon

Konfiguratsiooninomenklatuur koosneb järgmistest segmentidest.

1.  Atribuudi väärtus: materjal
2.  Tekstikonstant: „AAA”
3.  Atribuudi väärtus: pikkus

Saate sisestada segmentidele järgmised väärtused.

-   Tooteetaloni number = **M0099**
-   Materjal = **plast**
-   Pikkus = **12**

Sellisel juhul saab tootevariandi numbriks M0099\_PlastAAA12.

### <a name="example-for-dimension-based-configurations"></a>Dimensioonipõhiste konfiguratsioonide näide

Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.

1.  Tooteetaloni number
2.  Tekstikonstant: „//”
3.  Konfiguratsioon

Konfiguratsiooninomenklatuur koosneb järgmistest segmentidest.

1.  Konfiguratsioonigrupp: korpus
2.  Tekstikonstant: „&”
3.  Konfiguratsioonigrupp: esivõre

Saate sisestada segmentidele järgmised väärtused.

-   Tooteetaloni number = **D0123**
-   Korpus = **M0008**
-   Esivõre = **M0022**

Sellisel juhul saab tootevariandi numbriks D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numbrikonfliktid
Mõnikord ei pruugi seadistatav tootevariandi numbrite nomenklatuur anda kordumatuid tootevariandi numbreid. Tootevariantide numbrid pole kordumatud näiteks juhul, kui üks aktiivne tootedimensioon ei sisaldu eelmääratud variandi konfiguratsioonitehnoloogiat kasutava tooteetaloni nomenklatuuris. Konfliktide lahendamise viis võib olla erinev, olenevalt konfiguratsiooni tehnoloogiast.

### <a name="predefined-variants"></a>Eelmääratletud variandid

Kui proovite luua tootevariante käsitsi või automaatselt, nii et mitmel tootevariandil on sama tootevariandi number, tekib tõrge. Selle stsenaariumi vältimiseks tuleks kasutada tootedimensiooni grupis kõiki aktiivseid tootedimensioone. Teine võimalus on lisada numbriseeria, mis aitab tagada kordumatud tootevariantide numbrid.

### <a name="constraint-based-configurations"></a>Piirangupõhised konfiguratsioonid

Olenevalt nomenklatuurist võib süsteem püüda määrata konfiguratsioonile mittekordumatu tootevariandi numbri. Sellisel juhul kasutab süsteem tootevariandi numbrina konfiguratsioonidimensiooni numbriseeriat ja kuvatakse hoiatus. Selle stsenaariumi vältimiseks tuleks lisada nomenklatuuri piisavalt atribuute, mis aitaksid tagada kordumatud tootevariantide numbrid. Samuti peaksite veenduma, et valik **Taaskasuta** oleks komponendi puhul sisse lülitatud.

### <a name="dimension-based-configurations"></a>Dimensioonipõhised konfiguratsioonid

Ühe konfiguratsiooniprotsessi etapi ajal soovitab süsteem nomenklatuurile vastavat konfiguratsiooniväärtust. Selles etapis saate konfiguratsiooniväärtust käsitsi muuta. Konfiguratsiooni salvestamisel kontrollib süsteem, kas konfiguratsiooniväärtus on kordumatu. Kui sisestatud väärtus ei ole kordumatu, saate tõrketeate. Konfiguratsiooni salvestamiseks peate sisestama kordumatu konfiguratsiooniväärtuse.

<a name="additional-resources"></a>Lisaressursid
--------

[Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Kaubakoodi nomenklatuuri loomine konfigureeritud tootevariantidele](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

