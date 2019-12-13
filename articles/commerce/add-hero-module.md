---
title: Pannoomoodul
description: See teema hõlmab pannoomooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785383"
---
# <a name="hero-module"></a>Pannoomoodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab pannoomooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Pannoomoodulit kasutatakse toodete või kampaaniate turustamiseks läbi piltide ja teksti kombinatsiooni. Näiteks saab jaemüüja lisada pannoomooduli e-kaubanduse saidi avalehele, et reklaamida uut toodet ja tõmmata klientide tähelepanu.

Pannoomoodulit juhivad sisuhaldussüsteemi (CMS) andmed. See on eraldiseisev moodul, mis ei sõltu ühestki teisest lehe moodulist. Pannoomoodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, müük või funktsioonid).

## <a name="examples-of-hero-module-in-e-commerce"></a>E-kaubanduse pannoomooduli näited

- Pannoomoodulit saab kasutada e-kaubanduse saidi avalehel kampaaniate ja uute toodete esiletõstmiseks.
- Pannoomoodulit saab kasutada toote üksikasjade lehel, et esitleda toote teavet.
- Karusellmoodulisse saab lisada mitu pannoomoodulit, et tõsta esile mitu toodet või kampaaniat.

## <a name="hero-module-properties"></a>Pannoomooduli atribuudid

| Atribuudi nimi  | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pilt          | Pildifail | Toote või kampaania esitlemiseks saab kasutada pilti. Pildi saab laadida üles pildigaleriisse või kasutada olemasolevat pilti. |
| Pealkiri        | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Igal pannoomoodulil võib olla pealkiri. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |
| Lõik      | Lõigu tekst | Pannoomoodulid toetavad RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Seos           | Lingi tekst, lingi URL, silt ARIA (Accessible Rich Internet Applications) ja suvand **Ava link uuel vahekaardil** | Pannoomoodulid toetavad üht või mitut tegutsemiskutse linki. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil. |
| Teksti paigutus | **Üleval vasakul**, **üleval paremal**, **üleval keskel**, **all vasakul**, **all paremal**, **all keskel**, **keskel vasakul**, **keskel paremal** või **keskel keskel** | See atribuut määratleb pildi asukoha teksti suhtes. Näiteks kui on valitud suvand **Paremal**, ilmub pilt tekstist paremal. |
| Teksti teema     | **Hele** või **tume** | Tekstile saab määratleda taustapildi põhjal värviskeemi. Näiteks kui pildil on tume taust, saab rakendada heledat kujundust, et muuta tekst nähtavamaks ja olla juurdepääsetavuse eesmärgil vastavuses värvide kontrastsuse suhtega. |
| Astmik       | **Tõene** või **Väär** | Pildile saab rakendada astmikku, et olla juurdepääsetavuse eesmärgil vastavuses värvide kontrastsuse suhtega. |

## <a name="add-a-hero-module-to-a-new-page"></a>Pannoomooduli lisamine uuele lehele

Uuele lehele pannoomooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja looge lehe mall nimega **pannoo mall**.
1. Lisage vaikelehe pessa **Peamine** pannoomoodul.
1. Registreerige mall ja avaldage see.
1. Kasutage äsja loodud pannoo malli, et luua leht, mille nimi on **pannoo leht**.
1. Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Dialoogiaknas **Lisa moodul** jaotises **Moodulite valimine** valige pannoomoodul ja klõpsake seejärel nuppu **OK**.
1. Valige vasakul liigendpuus pannoomoodul.
1. Parempoolsel atribuutide paanil valige suvand **Lisa pilt**. Seejärel valige kas olemasolev pilt või laadige üles uus pilt.
1. Valige suvand **Pealkiri**.
1. Dialoogiaknas **Pealkiri** lisage pealkirja tekst, valige pealkirja tase ja seejärel klõpsake nuppu **OK**.
1. Suvandis **Rikastekst** lisage tekst, mida vajate.
1. Valige suvand **Lisa tegevuse link**.
1. Dialoogiaknas **Tegevuse link** lisage lingi tekst, lingi URL ja lingi ARIA-silt ning klõpsake seejärel nuppu **OK**.
1. Salvestage muudatused ja kuvage oma muudatuste eelvaade.
1. Registreerige leht ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Teatise moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Sisurikas plokimoodul](add-content-rich-block.md)

[Sisupaigutuse moodul](add-content-placement-modules.md)

[Funktsioonimoodul](add-feature-module.md)

[Videopleieri moodul](add-video-player.md)
