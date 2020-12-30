---
title: Sisuploki moodul
description: See teema hõlmab sisuploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a8b1c214ba31b7c47cecbe67bef493f5fa450fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411612"
---
# <a name="content-block-module"></a>Sisuploki moodul


[!include [banner](includes/banner.md)]

See teema hõlmab sisuploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Sisuploki moodulit kasutatakse toodete või kampaaniate turustamiseks läbi piltide ja teksti kombinatsiooni. Näiteks saab jaemüüja lisada sisuploki mooduli e-kaubanduse saidi avalehele, et reklaamida uut toodet ja tõmmata klientide tähelepanu.

Sisuploki moodulit juhivad sisuhaldussüsteemi (CMS) andmed. See on eraldiseisev moodul, mis ei sõltu ühestki teisest lehe moodulist. Sisuploki moodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, müük või funktsioonid).

## <a name="examples-of-content-block-module-in-e-commerce"></a>E-kaubanduse sisuploki moodulite näited

- Sisuploki moodulit saab kasutada e-kaubanduse saidi avalehel kampaaniate ja uute toodete esiletõstmiseks.
- Sisuploki moodulit saab kasutada toote üksikasjade lehel, et esitleda toote teavet.
- Karusellmoodulisse saab lisada mitu sisuploki moodulit, et tõsta esile mitu toodet või kampaaniat.

## <a name="content-block-modules-and-themes"></a>Sisuploki moodulid ja kujundused

Sisuploki moodulid võivad toetada mitmesuguseid kujundusi ja laade kujunduse alusel. Näiteks on Fabrikami kujunduses toetatud sisuploki mooduli kolme paigutuse variatsiooni: pannoo, funktsioon ja paan. Pannoo paigutus näitab pilti taustal koos ülekattetekstiga. Funktsiooni paigutus näitab pilti ja teksti kõrvuti. Paani paigutus võimaldab mitmeid sisuplokke paanivormingus.

Lisaks võib teema paljastada iga paigutuse jaoks erinevaid atribuute. Kujunduse arendaja saab luua rohkem kujundusi rohkemate stiilidega, kasutades selleks sisuploki moodulit.

Järgmine pilt näitab sisuploki mooduli näidet pannoo paigutusega.

![Pannoo mooduli näide](./media/Hero.PNG)

Järgmine pilt näitab sisuploki mooduli näidet funktsiooni paigutusega.

![Funktsiooni moodulite näited](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Sisuploki mooduli atribuudid

| Atribuudi nimi  | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pilt          | Pildifail | Toote või kampaania esitlemiseks saab kasutada pilti. Pildi saab laadida üles pildigaleriisse või kasutada olemasolevat pilti. |
| Pealkiri        | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Igal pannoomoodulil võib olla pealkiri. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |
| Lõik      | Lõigu tekst | Pannoomoodulid toetavad RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Seos           | Lingi tekst, lingi URL, silt ARIA (Accessible Rich Internet Applications) ja suvand **Ava link uuel vahekaardil** | Pannoomoodulid toetavad üht või mitut tegutsemiskutse linki. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Sisuploki mooduli atribuudid, mis on paljastatud Fabrikami kujundusega 

| Atribuudi nimi  | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Teksti paigutus | **Vasakul**, **Paremal**, **Keskel** | See atribuut määratleb teksti asukoha pildi peal. See kehtib ainult pannoo paigutuse kohta. |
| Teksti teema     | **Hele** või **tume** | Tekstile saab määratleda taustapildi põhjal värviskeemi. Näiteks kui pildil on tume taust, saab rakendada heledat kujundust, et muuta tekst nähtavamaks ja olla juurdepääsetavuse eesmärgil vastavuses värvide kontrastsuse suhtega. See kehtib ainult pannoo paigutuse kohta.|
| Pildi paigutus       | **Vasakul**,  **Paremal** | See atribuut määrab, kas pilt peaks olema tekstist vasakul või paremal. See kehtib ainult funktsiooni paigutuse kohta.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Sisuploki mooduli lisamine uuele lehele

Uuele lehele pannoomooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja looge lehe mall nimega **Sisuploki mall**.
1. Lisage vaikelehe pessa **Peamine** pannoomoodul.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Kasutage äsja loodud pannoo malli, et luua leht, mille nimi on **Sisuploki leht**.
1. Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Dialoogiaknas **Lisa moodul** jaotises **Moodulite valimine** valige pannoomoodul ja klõpsake seejärel nuppu **OK**.
1. Valige vasakul liigendpuus sisuploki moodul.
1. Parempoolsel atribuutide paanil valige suvand **Lisa pilt**. Seejärel valige kas olemasolev pilt või laadige üles uus pilt.
1. Valige suvand **Pealkiri**.
1. Dialoogiaknas **Pealkiri** lisage pealkirja tekst, valige pealkirja tase ja seejärel klõpsake nuppu **OK**.
1. Suvandis **Rikastekst** lisage tekst, mida vajate.
1. Valige **Lisa link**.
1. Lisage dialoogiaknas **Link** lingi tekst, lingi URL ja lingi ARIA-silt ning klõpsake seejärel nuppu **OK**.
1. Valige **Pannoo** paigutus.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kampaania ribareklaami moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Tekstiploki moodul](add-content-rich-block.md)

[Videopleierimoodul](add-video-player.md)
