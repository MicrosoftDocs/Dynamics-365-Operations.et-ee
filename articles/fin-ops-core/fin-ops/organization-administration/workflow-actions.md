---
title: Toimingud töövoo kinnitusprotsessides
description: Selles artiklis selgitatakse toiminguid, mida iga osaleja saab töövoo kinnitusprotsessis teha.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2da54d147c7e9c8a42ef9de94abcbe7f36c98295
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355744"
---
# <a name="actions-in-workflow-approval-processes"></a>Toimingud töövoo kinnitusprotsessides

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse toiminguid, mida iga osaleja saab töövoo kinnitusprotsessis teha.

Töövoog võib hõlmata mitut inimeste gruppi: algataja, ülesandes osalejad, otsustajad ja kinnitajad. Näiteks järgmises kuluaruande töövoos on Sam algataja, järjekorra liikmed on ülesandes osalejad, John on otsustaja ning Frank, Sue ja Ann on kinnitajad.

[![Töövoog\_ManuaalseOtsusega.](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)

Järgmistes jaotistes selgitatakse töövoo toiminguid, mida iga grupp saab teha.

## <a name="actions-that-an-originator-can-perform"></a>Toimingud, mida algataja saab teha

Algataja alustab töövoo eksemplari, edastades dokumendi töötlemiseks. Näiteks Sam peab oma kuluaruande esitamiseks klõpsama nuppu **Edasta** lehel **Kuluaruanne**.

## <a name="actions-that-a-task-assignee-can-perform"></a>Toimingud, mida ülesandes osaleja saab teha

Ülesande saab määrata mitmele inimesele või tööüksuste järjekorrale, mida jälgib mitu inimest. Ülesande täita saab siiski ainult üks inimene. Näiteks Sam on esitanud kuluaruande ja on suunanud oma sissetulekud oma organisatsiooni kuluaruannete osakonnale ülevaatamiseks.

Ettevõtte Adventure Works kuluaruannete osakonna liikmed jälgivad järjekorda. Julie, selle osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid. Ta võib nüüd teha ühe järgmistest toimingutest: lõpule viia, tagasi lükata, delegeerida, paluda muutmist, ümber määrata või vabastada.

> [!NOTE]
> Kasutatavad toimingud on erinevad, olenevalt sellest, kuidas tarkvaraarendaja ülesande üles ehitas.

### <a name="complete"></a>Lõpule viimine

Kui kasutaja viib ülesande lõpule, määratakse töötlemiseks edastatud dokument vajaduse korral järgmisele töövoo kasutajale, kui järgmine kasutaja on olemas. Kui rohkem töötlemist ei ole vaja, siis töövoo protsess lõpeb.

Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid. Kui Julie on oma ülevaatuse lõpetanud, määratakse dokument Johnile.

### <a name="reject"></a>Lükka tagasi

Kui kasutaja lükkab dokumendi tagasi, lõpeb töövooprotsess.

Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid. Kui Julie selle kuluaruande tagasi lükkab, lõpeb töövoog.

Sam saab seejärel kuluaruande uuesti esitada. Ta saab teha esmalt muudatusi või edastada uuesti algse versiooni. Kui Sam kuluaruande uuesti esitab, käivitatakse töövoo protsess käsitsi ülevaatamise toimingust.

### <a name="delegate"></a>Delegeeri

Kui kasutaja delegeerib ülesande, määratakse ülesanne teisele kasutajale.

Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid. Julie delegeerib ülesande Timile, kes on tema assistent.

Tim tegutseb seejärel Julie nimel. Seetõttu, kui Tim ülevaatamise lõpetab, määratakse kuluaruanne Johnile, just nii, nagu Julie oleks selle ülesande täitnud.

### <a name="request-change"></a>Taotle muudatust

Kui kasutaja taotleb edastatud dokumendi muutmist, saadetakse dokument tagasi algatajale.

Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid. Julie märkab kuluaruandes mõnda viga ja soovib muudatusi. Kuluaruanne saadetakse tagasi Samile.

Sam saab kuluaruande uuesti esitada. Ta võib teha esmalt soovitud muudatused või edastada uuesti algse versiooni. Kui Sam kuluaruande uuesti esitab, peab tööüksuste järjekorra liige kuluaruande ja kviitungid uuesti üle vaatama.

### <a name="reassign"></a>Määra uuesti

Tööüksuste järjekorra liikmed võivad määrata selles järjekorras olevaid dokumente ka teise järjekorda ümber.

Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, jälgib järjekorda. Et aidata töökoormust tasakaalustada, võib ta kuluaruande ja sellega kaasas olevad kviitungid teise järjekorda ümber määrata.

### <a name="release"></a>Vabasta

Aeg-ajalt võib tööüksuste järjekorra liige ülesande vastu võtta, kuid seejärel otsustada, et ta ei saa seda lõpule viia. Sel juhul võib ülesande vastuvõtnud inimene vabastada dokumendi tagasi tööüksuste järjekorda.

Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid. Kui Julie otsustab, et ta ei saa ülesannet lõpule viia, võib ta dokumendi vabastada. Kuluaruanne tagastatakse järjekorda, et ettevõtte Adventure Works kuluaruannete osakonna teised liikmed saaksid ülesande täita.

## <a name="actions-that-a-decision-maker-can-perform"></a>Toimingud, mida otsustaja saab teha

Tavaliselt määratakse dokument otsustajale seetõttu, et selles on küsimus, millele otsustaja peab vastama. Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**. Kui otsustaja valikut ei tee, võib ta otsustamise delegeerida.

### <a name="choice-1-or-choice-2"></a>\[Valik 1\] või \[Valik 2\]

Otsustaja peab dokumendiga seotud küsimusele vastama. Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**. Otsustaja valitud vastus määrab dokumendi töötlemiseks kasutatava töövooharu.

Näiteks Sami kuluaruanne on määratud Johnile. John peab otsustama, kas dokumendi teave nõuab Sami juhile helistamist. Kui John leiab, et kõne on vajalik, määratakse kuluaruanne Arethale, kes peab siis Sami juhile helistama. Kui John otsustab, et kõne pole vajalik, määratakse kuluaruanne Frankile kinnitamiseks.

### <a name="delegate"></a>Delegeeri

Kui otsustaja otsuse delegeerib, määratakse dokument teisele kasutajale, kes peab otsuse langetama.

Näiteks Sami kuluaruanne on määratud Johnile. John delegeerib otsustamise Mariale, kes on tema assistent.

Maria tegutseb seejärel Johni nimel. Kui Maria leiab, et kõne Sami juhile on vajalik, määratakse kuluaruanne Arethale, kes peab siis Sami juhile helistama. Kui Maria otsustab, et kõne pole vajalik, määratakse kuluaruanne Frankile kinnitamiseks.

## <a name="actions-that-an-approver-can-perform"></a>Toimingud, mida kinnitaja saab teha

Kui dokument määratakse kinnitajale, saab kinnitaja teha ühe järgmistest toimingutest: kinnitada, tagasi lükata, delegeerida või paluda muutmist.

### <a name="approve"></a>Kinnitamine

Kui kinnitaja kinnitab dokumendi, määratakse see vajadusel järgmisele töövoo kasutajale, kui järgmine kasutaja on olemas. Kui rohkem töötlemist ei ole vaja, siis töövoo protsess lõpeb.

Näiteks Sam on esitanud kuluaruande väärtuses USD 6000 ja see dokument on määratud Frankile. Kui Frank kinnitab dokumendi, määratakse see Suele kinnitamiseks. Kui Sue on kuluaruande kinnitanud, siis töövoo protsess lõpeb.

### <a name="reject"></a>Lükka tagasi

Kui kinnitaja lükkab dokumendi tagasi, lõpeb töövoo protsess.

Näiteks Sam on esitanud kuluaruande väärtuses USD 12 000 ja see dokument on määratud Suele. Kui Sue selle kuluaruande tagasi lükkab, lõpeb töövoog.

Sam saab kuluaruande uuesti esitada. Ta võib teha esmalt muudatused või edastada uuesti kuluaruande algse versiooni. Kui Sam taasesitab kuluaruande, käivitatakse kinnitusprotsess uuesti.

### <a name="delegate"></a>Delegeeri

Kui kinnitaja delegeerib dokumendi, määratakse dokument kinnitamiseks teisele kasutajale.

Näiteks Sam on esitanud kuluaruande väärtuses USD 12,000 ja see dokument on määratud Frankile. Frank delegeerib kuluaruande Annile.

Ann tegutseb seejärel Franki nimel. Seetõttu, kui Ann kinnitab dokumendi, määratakse see Suele kinnitamiseks, täpselt nagu Frank oleks pidanud seda kinnitama. Kui Sue on dokumendi kinnitanud, saadetakse see Annile kinnitamiseks.

### <a name="request-change"></a>Taotle muudatust

Kui kinnitaja taotleb dokumendi muutmist, saadetakse dokument tagasi algatajale.

Näiteks Sam on esitanud kuluaruande väärtuses USD 12 000 ja see dokument on määratud Suele. Kui Sue soovib muutmist, saadetakse kuluaruanne tagasi Samile.

Sam saab kuluaruande uuesti esitada. Ta võib teha esmalt soovitud muudatused või edastada uuesti kuluaruande algse versiooni. Kui Sam taasesitab kuluaruande, saadetakse see Frankile kinnitamiseks, sest Frank on selle kinnitamisprotsessi esimene kinnitaja.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]