---
title: Tootenomenklatuuri number
description: "Selles teemas kirjeldatakse, kuidas saate seadistada number tootenomenklatuuri asendada kindlas vormingus [toote kapten - konfiguratsioon - suurus - värv - numbrilaad], suunatud vormi, kus kapten tootenumber, aktiivse toote mõõtmed ja valitud tekst eraldajaid. Samuti saate koostada nomenklatuuri piirangupõhise tootekonfiguraatoriga loodud konfiguratsioonide tuvastamiseks. Need nomenklatuurid võivad sisaldada teie valitud atribuute."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Tootenomenklatuuri number

Selles teemas kirjeldatakse, kuidas saate seadistada number tootenomenklatuuri asendada kindlas vormingus [toote kapten - konfiguratsioon - suurus - värv - numbrilaad], suunatud vormi, kus kapten tootenumber, aktiivse toote mõõtmed ja valitud tekst eraldajaid. Samuti saate koostada nomenklatuuri piirangupõhise tootekonfiguraatoriga loodud konfiguratsioonide tuvastamiseks. Need nomenklatuurid võivad sisaldada teie valitud atribuute.

Uus tootevariandi numbrite nomenklatuur võimaldab kaasata tootevariandi identifikaatorites segmente. Need segmendid võivad sisaldada tooteetaloni numbrit, tootedimensioone, numbriseeriaid, tekstikonstante ja atribuute. See funktsionaalsus võimaldab teil müügitellimuse või ostutellimuse loomisel kiiresti leida konkreetse tootevariandi.

## <a name="nomenclature-of-predefined-product-variants"></a>Eelmääratletud tootevariantide nomenklatuur
Tootevariandid luuakse tooteetalonidele vastavalt ühele kolmest konfiguratsioonitehnoloogiast.

-   Eelmääratletud variandid
-   Piirangupõhised
-   Dimensioonipõhised

Igal tootevariandil on number ja tootevariandi ID nomenklatuur võimaldab valida segmendid, mida kaasatakse igas tootevariandi numbris. Saate valida lehel **Toote nomenklatuur** järgmisi segmente.

-   Tooteetaloni number
-   Numbriseeria väärtus
-   Tekstikonstant
-   Tootedimensioonid
    -   Konfiguratsioon
    -   Värv
    -   Suurus
    -   Laad

Kui tootevariandi ID-nomenklatuur on määratletud, saab selle seostada tootedimensioonigrupiga. Seega määratakse kõigile sellele tootedimensioonigrupile viitavatele tooteetalonidele nomenklatuuri põhjal tootevariandi numbrid. Samuti on võimalik määrata tootevariandi ID-nomenklatuur otse tooteetalonile, millisel juhul määratakse sellele etalonile kuuluvatele tootevariantidele nomenklatuuri põhjal tootevariandi numbrid.

### <a name="example"></a>Näide

T-särki (TS1234) toodetakse 3 erinevas suuruses (S, M, L), 4 erinevas värvis (punane, roheline, sinine, kollane) ja kahes stiilis (polo, V-kaelus), mis annab kokku 24 võimalikku tootevarianti. Tootevariandi ID-nomenklatuur luuakse järgmiste segmentidega.

1.  Tooteetaloni number
2.  Tekstikonstant: –
3.  Värv
4.  Tekstikonstant: –
5.  Suurus
6.  Tekstikonstant: –
7.  Laad

Tootevariandi number punase väikese polo puhul on järgmine: TS1234-punane-väike-polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nomenklatuuri constraintbased koosseisud
Konfiguratsioonide piiranguteta põhineva saab ehitada spetsiaalne eriotstarbeline toote konfiguratsiooni dimensiooni. Saate valida lehel **Toote nomenklatuur** järgmisi segmente.

-   Numbriseeria väärtus
-   Tekstikonstant
-   Atribuudi väärtus 

Igal toote konfiguratsioonimudelis oleval komponendil võib olla oma konfiguratsiooninomenklatuur. Kasutada võib ainult komponendile kuuluvaid atribuute. Alamkomponendid või kasutajanõuete atribuudid pole saadaval.

### <a name="example"></a>Näide

Toote konfiguratsioonimudelil on juurkomponent kahe atribuudiga.

-   Materjal (plast, puit, teras)
-   Pikkus (10...100)

Konfiguratsiooninomenklatuur määratletakse järgmiste segmentide põhjal.

1.  Atribuudi väärtus: materjal
2.  Tekstikonstant: AAA
3.  Atribuudi väärtus: pikkus

Puitmaterjali, mille pikkus on 78, konfiguratsiooni ID on järgmine: PuitAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Nomenklatuuri dimensionbased koosseisud
Dimensiooni põhinev konfiguratsioonide puhul saab ehitada spetsiaalne eriotstarbeline toote konfiguratsiooni dimensiooni. Saate valida lehel **Toote nomenklatuur** järgmisi segmente.

-   Numbriseeria väärtus
-   Tekstikonstant
-   Konfiguratsioonigrupi kaup

Konfiguratsiooninomenklatuuri saab määratleda kooslusele.

### <a name="example"></a>Näide

Kooslusel on neli koosluse rida, mis on jaotatud kahte konfiguratsioonigruppi.

-   Koosluserida: M0007, standardkorpus
    -   Konfiguratsioonigrupp: korpus
-   Koosluserida: M0008, tipptasemel korpus
    -   Konfiguratsioonigrupp: korpus
-   Koosluserida: M0021, kangast esivõre
    -   Konfiguratsioonigrupp: esivõre
-   Koosluserida: M0022, metallist esivõre
    -   Konfiguratsioonigrupp: esivõre

Konfiguratsiooninomenklatuur määratletakse järgmiste segmentide põhjal.

1.  Konfiguratsioonigrupp: korpus
2.  Tekstikonstant: &
3.  Konfiguratsioonigrupp: esivõre

Kangast esivõrega standardse korpuse konfiguratsiooni-ID on järgmine: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Tootevariantide ja konfiguratsioonide kombinatsiooni nomenklatuur
Kui kasutate tooteetalonile tootevariantide konfigureerimiseks piirangupõhist või dimensioonipõhist konfiguratsioonitehnoloogiat, saavad tootevariandid tootevariandi numbrid, mis hõlmavad konfiguratsioonidimensioonist pärit nomenklatuuri. Variantide konfigureerimiseks toimige järgmiselt.

1.  Määratlege lehel **Toote nomenklatuur** tootevariandi numbrite nomenklatuur, mis sisaldab konfiguratsioonidimensiooni.
2.  Määrake see nomenklatuur konfiguratsioonidimensiooniga tootedimensioonigrupile.
3.  Määratlege konfiguratsiooninomenklatuur komponentidele või kooslustele, mida kasutatakse tootevariantide konfigureerimiseks.

### <a name="example-for-constraint-based-configurations"></a>Piirangupõhiste konfiguratsioonide näide

Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.

1.  Tooteetaloni number
2.  Tekstikonstanti "\_"
3.  Konfiguratsioon

Konfiguratsiooninomenklatuur võib sisaldada järgmisi segmente.

1.  Atribuudi väärtus: materjal
2.  Tekstikonstant: AAA
3.  Atribuudi väärtus: pikkus

Saate sisestada segmentidele järgmised väärtused.

-   Tooteetaloni number = M0099
-   Materjal = plast
-   Pikkus = 12

Toote variandinumbrit muutub: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Dimensioonipõhiste konfiguratsioonide näide

Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.

1.  Tooteetaloni number
2.  Tekstikonstant: //
3.  Konfiguratsioon

Konfiguratsiooninomenklatuur võib sisaldada järgmisi segmente.

1.  Konfiguratsioonigrupp: korpus
2.  Tekstikonstant: &
3.  Konfiguratsioonigrupp: esivõre

Saate sisestada segmentidele järgmised väärtused.

-   Tooteetaloni number = D0123
-   Korpus = M0008
-   Esivõre = M0022

Tootevariandi numbriks muutub: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numbrikonfliktid
Võimalik on seadistada tootevariandi numbrite nomenklatuur, mille tulemuseks ei ole kordumatud tootevariandi numbrid. See võib juhtuda näiteks siis, kui üks aktiivne tootedimensioon ei sisaldu eelmääratud variandi konfiguratsioonitehnoloogiat kasutava tooteetaloni nomenklatuuris. Konflikte käsitletakse erinevate konfiguratsioonitehnoloogiate puhul erinevalt.

### <a name="predefined-variants"></a>Eelmääratletud variandid

Kui proovite luua tootevariante käsitsi või automaatselt, nii et ühel või mitmel on tulemuseks sama tootevariandi number, tekib tõrge. Selle vältimiseks peaksite kasutama kõiki selles tootedimensioonigrupis olevaid aktiivseid tootedimensioone või kaasama numbriseeria, et tagada tootevariandi numbrite kordumatus.

### <a name="constraint-based-configurations"></a>Piirangupõhised konfiguratsioonid

Olenevalt nomenklatuurist võib süsteem püüda määrata konfiguratsioonile mittekordumatu tootevariandi numbri. Sel juhul süsteem kasutab numbriseeriat konfiguratsioonidimensioon kui toote variandinumbrit asemel. Sel juhul kuvatakse hoiatus. Selle vältimiseks peaksite kaasama nomenklatuuri piisavalt atribuute, et tagada kordumatus, ning veenduma, et komponendi puhul oleks suvand **Korduvkasutus** sisse lülitatud.

### <a name="dimension-based-configurations"></a>Dimensioonipõhised konfiguratsioonid

Konfigureerimisprotsess sisaldab etappi, milles süsteem soovitab nomenklatuuri põhjal konfiguratsiooniväärtust. Selles etapis saate konfiguratsiooniväärtust käsitsi muuta. Konfiguratsiooni salvestamisel kontrollib süsteem, kas konfiguratsiooniväärtus on kordumatu. Kui see ii pole, kuvatakse tõrge. Konfiguratsiooni salvestamiseks peate sisestama kordumatu konfiguratsiooniväärtuse.



<a name="see-also"></a>Vt ka
--------

[Loo number tootenomenklatuuri eelmääratletud toote variantide (ülesande juhend)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Loo number tootenomenklatuuri konfigureeritud toote variantide (ülesande juhend)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)


