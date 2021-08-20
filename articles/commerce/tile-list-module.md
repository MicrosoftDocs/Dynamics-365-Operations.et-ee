---
title: Paanide loendi moodul
description: See teema hõlmab paani mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 513775afe325008ebd6cd18d2d9485a972984090da3803d255a1584b16b1e014
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767847"
---
# <a name="tile-list-module"></a>Paanide loendi moodul

[!include [banner](includes/banner.md)]

See teema hõlmab paani mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Paaniloendimoodul on paanide kogum. Seda kasutatakse tootekategooriate või tootemarkide turusmiseks piltide ja teksti kaudu. Näiteks saab jaemüüja lisada paaniloendi mooduli e-kaubanduse saidi kodulehele, et propageerida kõiki tippmüügikategooriaid.

Paani loendi moodulit juhivad sisuhaldussüsteemi (CMS) andmed. See ei sõltu muudest moodulitest ega Commerce peakontori andmetest. Paani loendi moodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, kategooriad või brändid).

Järgmine näide näitab paaniloendi mooduli ja paanimoodulite näidet Adventure Worksi kodulehel.

![Paaniloendi mooduli ja paanimoodul näide Adventure Works kodulehel.](./media/Tile_list.PNG)

> [!IMPORTANT]
> Paaniloendi moodul on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.
> Paaniloendi moodul kuvatakse Adventure Works teemas.

## <a name="tile-list-modules-and-themes"></a>Paaniloendi moodulid ja kujundused

Paaniloendi moodulid võivad toetada mitmesuguseid kujundusi ja stiile kujunduse alusel. Näiteks Adventure Works teemas näitavad paanid animaefekti, kui saidi kasutajad nendest üle liiguvad. Iga kujundus võib sisaldada paaniloendi ja paanimoodulite täiendavaid atribuute. Teema rendajad võivad lisaks ehitada paaniloendi ja paanimoodulite lisakujundusi.

## <a name="tile-list-module-properties"></a>Paaniloendi mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Päis       | Pealkirja tekst ja pealkirja silt | Paaniloendi mooduli tekstipäis. |

## <a name="tile-module-properties"></a>Paanimooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pilt         | Pildifail | Toote või kategooria esitlemiseks saab kasutada pilti. Pildi saab Commerce site koostajas üles laadida meediateeki või kasutada olemasolevat pilti. |
| Päis       | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Vaikimisi kasutatakse **H2** pealkirja silti päises, kuid pealkirja silti saab vajadusel muuta juurdepääsu nõuetele vastavaks. |
| Lõik     | Lõigu tekst | Moodul toetab RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu hüperlingid ja paks, allajoonitud, ning kursiivis tekst. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Seos          | Lingi tekst, lingi URL, silt ARIA (Accessible Rich Internet Applications) ja suvand **Ava link uuel vahekaardil** | Paanmoodulid toetavad üht või mitut tegutsemiskutse linki. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil. |
| Paani link     | Lingi tekst, lingi URL, ARIA silt ja suvand **Ava link uuel vahekaardil** valik | Seda atribuuti kasutatakse lingi "tegevusele kutsumine" määratlemiseks. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil.|
| Ikoon          | Pilt | Lisaks toote- või kategooriapildile saab lisada ka ikoonisümboli. Ikooni sümboli pilt kuvatakse toote või kategooria pildi kohal. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Paaniloendi mooduli lisamine uuele lehele

Paaniloendi mooduli uuele lehele lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Minge **mallidesse** ja avage oma saidi avalehe turundusmall (või looge uus turundusmall).
1. Valige vaikelehe pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** **Paaniloendi** moodul ja klõpsake seejärel **Ok**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge **lehekülgedele** ja avage saidi avaleht (või looge uus avaleht, kasutades turundusmalli).
1. Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** **Paaniloendi** moodul ja klõpsake seejärel **Ok**.
1. Paaniloendi mooduli atribuudipaanil lisage pealkiri.
1. **Paaniloendi** pesas, valige kolmikpunkt (**...**) ja seejärel valige **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** **Paanimooduli** moodul ja klõpsake seejärel **Ok**.
1. Paanimooduli atribuudipaanil saate lisada pildi, pealkirja ja ikoonisümboli pildi.
1. Lisage ja konfigureerige lisa aktiivseid paanimooduleid vastavalt vajadusele.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Adventure Works teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
