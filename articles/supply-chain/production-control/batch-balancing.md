---
title: Partii tasakaalustamine
description: Selles teemas kirjeldatakse partii tasakaalustamise protsessi.
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 46411052c7db25c3d1410c5280e8e856f0a40d3d
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250132"
---
# <a name="batch-balancing"></a>Partii tasakaalustamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas partii tasakaalustamise protsessi toetatakse. 

Lisateabe saamiseks vaadake [videot partii tasakaalustamise kohta](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

Partii tasakaalustamise protsessis arvutatakse tootmispartiis kasutatavate koostisosade arv valitud tootepartiides olevate toimeainete kontsentratsiooni põhjal.

<a name="products-that-have-an-active-ingredient"></a>Toimeainet sisaldavad tooted
---------------------------------------

Toote saab määratleda toimeaine kontsentratsiooni põhjal. Toote toimeaine modelleeritakse tootepõhise partii atribuudi põhjal, millel on miinimumväärtus, maksimumväärtus ja sihttase.

Partii atribuudi sihttase tähistab toote toimeaine hinnangulist protsenti. Minimaalne ja maksimaalne väärtus tähistavad aktsepteeritavat hälvet sihttasemest. Neid saab kasutada näiteks partiide kinnitatud hälbena toote sissetulekul.

Tootel võib olla ainult üks toimeaine. Toote toimeaine määramiseks peate esmalt määratlema tootepõhise partii atribuudi. Seejärel saate atribuudi seostada toote alusatribuudina.

Toote tasemel peate ka määratlema, kuidas toote partii toimeaine taset tuleks salvestada: ostu kättesaamise protsessi või kvaliteettellimuse protsessi osana.

Alusatribuudi seostamiseks tootega on vajalik järgmine seadistus.

-   Toode peab olema partii kaudu juhitud. Et muuta toode partii kaudu juhitavaks, peate aktiivse partii dimensiooniga tootele määrama jälgimisdimensiooni grupi.

-   Atribuut, mis näitab koostisosa tasemeid, peab olema määratletud toote tootepõhise partii atribuudina.

Saate vaadata ja redigeerida partii toimeaine tegelikku väärtust lehel **Varude partii atribuudid**. 

-  Valige **Varude haldus** \> **Päringud ja aruanded** \> **Jälgimisdimensioonid** \> **Partiid** \> **Varude partii atribuudid**.

<a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Koostisosa tüübid ja viis, kuidas need suhtlevad partii tasakaalustamise protsessis
---------------------------------------------------------------------

Loodud valemi real saab olla üks järgmistest koostisosa tüüpidest:

-   None

-   Aktiivne

-   Hüvitamine

-   Täitja

Ülejäänud jaotises on esitatud näited selle kohta, kuidas iga koostisosa tüüp toimib. Näited põhinevad järgmisel valemil, mille partii kogusuurus on 100 liitrit.

| **Koostisosa tüüp** | **Kaubakood** | **Valemirea kogus** | **Üksus** |
|---------------------|-----------------|---------------------------|----------|
| None                | A               | 20                        | liiter    |
| Aktiivne              | B               | 30                        | liiter    |
| Hüvitamine        | C               | 10                        | liiter    |
| Täitja              | D               | 40                        | liiter    |

### <a name="active"></a>Aktiivne

Kui valemireale lisatakse alusatribuudiga toode, viidatakse sellele kui valemi *toimeainele*. Partiitellimusi, millel on toimeaineid sisaldavad valemid, saab kasutada partii tasakaalustamise protsessi jaoks. Valemi iga koostisosa korral hindab partii tasakaalustamise protsess, millist kogust on vaja toote tootmiseks. Koguste hinnangu põhineb valitud partiides olevate toimeainete kontsentratsioonil.

**Näide**

Koostisosal B on alusatribuut X ja sihttase 30 ning seda kasutatakse valemis, mille korral on iga 100 liitri toote jaoks vaja 30 liitrit koostisosa B-d. Luuakse partiitellimus, mille partii suurus on 100 liitrit. Partiitellimust alustatakse ja partii tasakaalustamise protsessi ajal valib kasutaja koostisosa B (mille sisalduse tase on 35) partii. Kuna sisalduse tase 35 on kõrgem kui sihttase 30, vähendatakse koostisosa B tasakaalustatud kogust, kasutades sisalduse väärtuse ja partii sihttaseme suhet, mis korrutatakse hinnangulise kogusega. Tasakaalustatud koguse arvutuskäik on järgmine:

(30 ÷ 35) × 30 liitrit = 25,71 liitrit

| **Kaubakood** | **Koostisosa tüüp** | **Eeldatav kogus** | **Tasakaalustatud kogus** | **Aktiivne kogus** | **Üksus** | **Alusväärtus** |
|-----------------|---------------------|------------------------|-----------------------|---------------------|----------|----------------|
| A               | None                | 20                     | 20                    |                     | liiter    |                |
| B               | Aktiivne              | 30                     | 25,71                 | 9,00                | liiter    | 30,00          |
| C               | Hüvitamine        | 10                     | 14,72                 |                     | liiter    |                |
| D               | Täitja              | 40                     | 39,57                 |                     | liiter    |                |

### <a name="none"></a>None

Kui rakendate partii tasakaalustamise protsessi siis, kui koostisosa tüüp on **Puudub**, on partiitellimuse valemirea hinnanguline kogus ja tasakaalustatud kogus võrdsed.

**Näide**

Komponent A määratakse komponendile tüübiga **Puudub** ja lisatakse valmistoote valemile. Valem nõuab iga 100 liitri valmistoote jaoks 10 liitrit koostisosa A-d. Kui partiitellimus nõuab 200 liitrit, arvutatakse koostisosa A nii hinnanguline kogus kui ka tasakaalustatud kogus 20 liitrina.

### <a name="compensating"></a>Hüvitamine

Kompenseeriv aine saab toote toimeaine mõju kas tasakaalustada või täiendada. Seetõttu oleneb kompenseeriva aine tarbitud kogus toote sisaldusest.

-   **Vastandmõju** – kui toimeaine kogus on oodatust suurem, peate lisama vähem kompenseerivat ainet.

-   **Täiendav mõju** – kui toimeaine kogus on oodatust väiksem, peate lisama rohkem kompenseerivat ainet.

Toimeaine ja täiendava koostisosa vaheline seos on esitatud lehel **Kompenseerimise põhimõte**.

Järgige neid etappe koostisosade vaheliste seoste loomiseks.

1.  Valige **Tooteteabe haldus** \> **Kooslused, materjalid ja valemid** \> **Valemid**, avage valemirida ja valige **Koostisosad**, et avada leht **Kompenseerimise põhimõte**.

2.  Valige rida, mis tähistab kompenseerimise põhimõtet ja seejärel valige kompenseeritav toimeaine.

>   Kompenseerimise põhimõttes saate sisestada ka positiivse või negatiivse kompenseeriva teguri, et määratleda, kui palju kompenseerida ja kas põhimõte peaks olema vastandlik või täiendav. Positiivne tegur esindab täiendavat mõju ja negatiivne tegur vastandmõju.

**Näide**

Komponent B on toimeaine, mille alusatribuut on X ja sihttase 30. Seda kasutatakse valemis, mis nõuab iga 100 liitri toote jaoks 30 liitrit koostisosa B-d. Koostisosa C on kompenseeriv aine ja sama valem sisaldab kogust 10. Kompenseerimise põhimõttes on seadistatud kompenseeriv tegur 1.10. Seega vähendatakse kompenseeriva aine tasakaalustatud kogust erinevuse võrra toimeaine tasakaalustatud koguse ja hinnangulise vajaliku koguse vahel, mis on korrutatud teguriga 1.10.

Kui koostisosa tüüp on **Aktiivne**, saadi vajaliku toimeaine tasakaalustatud koguseks 25,71 ja hinnanguliseks vajalikuks koguseks 30. Sel juhul arvutatakse kompenseeriva aine tasakaalustatud kogus järgmiselt.

1.  Määratakse kindlaks erinevus hinnangulise ja tasakaalustatud koguse vahel:

>   25,71 – 30 = –4,29

2.  Tulemus korrutatakse kompenseeriva teguriga:

>   4,29 × 1,10 = –4,72

3.  Hinnangulist kompenseerivat kogust vähendatakse –4,72 võrra, et määrata kindlaks tasakaalustatud kompenseeriv kogus:

>   10 – (–4,72) = 14,72

Kuna 1.10 on positiivne kompenseeriv tegur, on sellel kompenseerimise põhimõttel täiendav mõju. Selles näites on toimeaine oodatust mõjusam. Seetõttu on vaja rohkem kompenseerivat ainet.

### <a name="filler"></a>Täitja

*Täiteaine* on neutraalne koostisosa, mida kasutatakse valmistoote soovitud väljundkoguse saamiseks. Täiteaine koguste korrigeerimisi arvutatakse toimeaine ja kompenseeriva aine variatsioonide põhjal võrreldes standardse kogusega.

**Näide**

Formuleerisite toote, mis sisaldab koostisaineid A, B, C ja D valemi jaoks, mille suurus on 100 liitrit. Arvutasite välja kõigi koostisosa tüüpide tasakaalustatud koguse, välja arvatud koostisosa tüübi **Täiteaine** jaoks, mida kasutatakse ühel real.
Täiteaine tasakaalustatud kogus arvutatakse erinevusena partii suuruse 100 liitrit ja koostisainete A, B ja C kogusumma vahel:

100 – (20 + 25,71 + 14,72) = 39,57

<a name="the-batch-balancing-process"></a>Partii tasakaalustamise protsess
---------------------------

Partii tasakaalustamise protsessi teostatakse lehel **Partii tasakaalustamine**.
Valige **Kuluhandlus** \> **Partiitellimused** ja seejärel valige vahekaardil **Protsess** suvand **Partii tasakaalustamine**. Partii tasakaalustamine on saadaval partiitellimustel, mille olek on **Alustatud**.

Üldjuhul saab partii tasakaalustamist partiitellimustele rakendada siis, kui valemis on vähemalt üks valemirida, kus koostisosa tüübiks on **Aktiivne**. (Selle reegli erandit vt käesolevas teemas allpool osa „Partiitellimused, mis ei ole partii tasakaalustamise jaoks sobilikud”.)

Partii tasakaalustamise protsessi saab jagada kaheks alamprotsessiks:

1.  Partii koostisosade tasakaalustamine

2.  Valemi kinnitamine ja väljastamine

### <a name="balance-batch-ingredients"></a>Partii koostisosade tasakaalustamine

Partii koostisosade tasakaalustamise alamprotsessis arvutatakse tootmispartii jaoks kasutatavate koostisosade arv valitud partiide põhjal, millel on toimeained. Tavaliselt saab arvutuse lõpule viia ainult siis, kui kõik koostisosad on täies ulatuses olemas. Te ei saa tasakaalustatada ainult osa partiist, mille tootmiseks partiitellimus on seadistatud.

[!NOTE]
Te ei saa arvutust salvestada ja seejärel partii tasakaalustamise protsessi hiljem lõpule viia. Kui sulgete lehe **Partii tasakaalustamine**, peate protsessi lõpule viimiseks arvutuse uuesti tegema.

### <a name="confirm-and-release-the-formula"></a>Valemi kinnitamine ja väljastamine

Kui koostisosa kogused on arvutatud, saate valemi kinnitada ja väljstada. Väljastamise protsess erineb olenevalt sellest, kas tooted on laohaldusprotsesside jaoks lubatud.

-   Kui toode on laohaldusprotsesside jaoks lubatud, väljastatakse valemirida lattu laohaldusprotsesside põhimõtete alusel. Valemirida väljastatakse kogustes, mis vastavad tasakaalustatud kogustele ja see väljastatakse kindlatele partiidele, mis on valitud toimeaine jaoks.

> [!NOTE]
>   Valemiread võib lattu väljastada ainult partii tasakaalustamise protsessi osana. Kuigi tootmise jaoks mõeldud materjalide väljastamiseks lattu on ka teisi valikuid, ei saa neid valikuid valemiridade korral kasutada.

-   Kui toode ei ole laohaldusprotsesside jaoks lubatud, luuakse valemi kinnitamisel ja väljastamisel toote jaoks tootmise komplekteerimisleht.

Saate ühes valemis kombineerida nii tooted, mis on laohaldusprotsesside jaoks lubatud, kui ka tooted, mis pole laohaldusprotsesside jaoks lubatud. Kui ühes valemis kasutatakse neid kahte tüüpi tooteid, väljastatakse lattu tooted, mis on laohaldusprotsesside jaoks lubatud. Toodete jaoks, mis ei ole laohaldusprotsesside jaoks lubatud, luuakse valemi kinnitamisel ja väljastamisel komplekteerimisleht.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Partii tasakaalustamise jaoks mittesobilikud partiitellimused

Olemas on üks erand reeglile, et partiitellimused on sobilikud partii tasakaalustamise jaoks, kui valemis on vähemalt üks valemirida, kus koostisosa tüübiks on **Aktiivne**.

Kui valem sisaldab laohaldusprotsesside jaoks lubatud toote toimeainet, kuid partii number on reserveerimishierarhias allpool asukohta, ei ole partiitellimus partii tasakaalustamiseks sobilik.

Partiitellimus, mis ei ole partii tasakaalustamiseks sobilik, läbib partiitellimuste tavapärase protsessitsükli.
