---
title: Interaktiivne funktsioonimoodul
description: See teema hõlmab interaktiivseid funktsioonimooduleid ja kirjeldab, kuidas neid Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5b18a29ce43e69ec0578602535f21e52388fe3d04ac14673bbdefed9ec8ea161
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749846"
---
# <a name="interactive-feature-module"></a>Interaktiivne funktsioonimoodul

[!include [banner](includes/banner.md)]

See teema hõlmab interaktiivseid funktsioonimooduleid ja kirjeldab, kuidas neid Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Interaktiivsed funktsioonimoodulid on funktsioonideta moodulid, mida saab kasutada mitme tootekategooria või toote kaubamärgi turus kasutamiseks piltide ja teksti kombinatsiooni abil. Näiteks saab jaemüüja lisada paaniloendi mooduli e-commerce saidi kodulehele, et propageerida kõiki e-commerce tippmüügikategooriaid. Interaktiivne funktsioonimoodul sarnaneb paaniloendi mooduliga, kuid sellel on erinev paigutus ja erinevad suhtlusfunktsioonid.

Iga interaktiivse funktsioonimoodul on interaktiivsete funktsiooniüksuse moodulite kogum. Iga funktsiooni üksuse moodulit juhivad sisuhaldussüsteemi (CMS) andmed. See ei sõltu muudest moodulitest ega Commerce peakontori andmetest. Interaktiivse funktsioonimoodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, kategooriad või brändid).

> [!IMPORTANT]
> - Interaktiivne funktsioonimoodul on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.
> - Interaktiivne funktsioonimoodul kuvatakse Adventure Worksi teemas.

Järgmine näide näitab interaktiivse funktsioonimooduli näidet Adventure Worksi kodulehel.

![Järgmine näide näitab interaktiivse funktsioonimooduli näidet Adventure Worksi kodulehel](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Interaktiivne funktsioonimoodul ja teemad

Interaktiivse funktsioonimoodulid võivad toetada mitmesuguseid kujundusi ja stiile kujunduse alusel. Näiteks teemas Adventure Works on interaktiivsel funktsioonimoodulil kaheveeruline paigutus, mis näitab animaefekti, kui saidi kasutaja selle üksustest üle liigub. Interaktiivne funktsioonimoodul on optimeeritud ühtlase arvu piltide jaoks, mis on korraldatud kaheveeru paigutusega.

## <a name="interactive-feature-module-properties"></a>Interaktiivse funktsioonimooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Päis       | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Teksti päis interaktiivsele funktsioonimoodulile. |

## <a name="interactive-feature-item-module-properties"></a>Interaktiivse funktsiooni üksuse mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pilt         | Pildifail | Pilt, mis esindab toodet või kategooriat. Pildi saab Commerce site koostajas üles laadida meediateeki või kasutada olemasolevat pilti. |
| Päis       | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Vaikimisi kasutatakse **H2** pealkirja silti päises, kuid pealkirja silti saab vajadusel muuta juurdepääsu nõuetele vastavaks. |
| Lõik     | Lõigu tekst | Moodul toetab RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu hüperlingid ja paks, allajoonitud, ning kursiivis tekst. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Seos          | Lingi tekst, lingi URL, Accessible Rich Internet Applications (ARIA) silt ja suvand **Ava link uuel vahekaardil** valija | Moodulid toetavad üht või mitut tegutsemiskutse linki. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Lisage interaktiivne funktsioonimoodul uuele lehele

Interaktiivse funktsioonimooduli uuele Commerce lehele lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Minge **mallidesse** ja avage oma saidi avalehe turundusmall (või looge uus turundusmall).
1. Valige vaikelehe pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul**, **Interaktiivne funktsioon** moodul ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge **lehekülgedele** ja avage saidi avaleht (või looge uus avaleht, kasutades turundusmalli).
1. Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Dialoogiaknas **Lisa moodul** jaotises **Moodulite valimine** valige **interaktiivne funktsiooni** moodul ja klõpsake seejärel nuppu **OK**.
1. Interaktiivse funktsiooni mooduli atribuudipaanil lisage pealkiri.
1. **Interaktiivse funktsiooni** pesas, valige kolmikpunkt (**...**) ja seejärel valige **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul**, **Interaktiivse funktsiooni üksuse** moodul ja klõpsake seejärel **OK**.
1. Interaktiivse funktsiooniüksuse mooduli atribuudipaanil saate lisada pildi, pealkirja teksti, lõigu teksti ja URL-i.
1. Lisage ja konfigureerige interaktiivse funktsiooni üksus vastavalt vajadusele.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Adventure Works teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
