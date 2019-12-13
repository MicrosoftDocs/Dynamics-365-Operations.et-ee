---
title: Funktsioonimoodul
description: See teema hõlmab funktsioonimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785279"
---
# <a name="feature-module"></a>Funktsioonimoodul 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab funktsioonimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Funktsioonimoodulit kasutatakse toodete või kampaaniate turustamiseks läbi piltide ja teksti kombinatsiooni. Näiteks saab jaemüüja lisada funktsioonimooduli toote üksikasjade lehele, et tuua esile toote omadused.

Funktsioonimoodulit juhivad sisuhaldussüsteemi (CMS) andmed. See on eraldiseisev moodul, mis ei sõltu ühestki teisest lehe moodulist. Funktsioonimoodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, müük või funktsioonid).

## <a name="examples-of-feature-modules-in-e-commerce"></a>E-kaubanduse funktsioonimoodulite näited

Funktsioonimoodulit saab kasutada järgmistel lehtedel.

- Toote üksikasjade leht, et tutvustada toote funktsioone
- Avaleht, et tooteid reklaamida
- Kategooria leht, et tõsta esile toodete kategooria

## <a name="feature-module-properties"></a>Funktsioonimooduli atribuudid

| Atribuudi nimi     | Väärtused | Kirjeldus |
|-------------------|--------|-------------|
| Pilt             | Pildifail | Toote või kampaania turustamiseks saab kasutada pilti. Pildi saab laadida üles pildigaleriisse või kasutada olemasolevat pilti. |
| Pealkiri           | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Igal funktsioonimoodulil võib olla pealkiri. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |
| Lõik         | Lõigu tekst | Funktsioonimoodulid toetavad RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Seos              | Lingi tekst, lingi URL, silt ARIA (Accessible Rich Internet Applications) ja suvand **Ava link uuel vahekaardil** | Funktsioonimoodulid toetavad üht või mitut tegutsemiskutse linki. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil. |
| Pildi paigutus   | **Paremal**, **Vasakul**, **Üleval** või **All** | See atribuut määratleb pildi asukoha teksti suhtes. Näiteks kui on valitud suvand **Paremal**, ilmub pilt tekstist paremal. |
| Pildiveeru suurus | Väärtus vahemikus **1** kuni **12** | See atribuut määratleb pildi suuruse teksti suhtes. Suurus on väljendatud veergude arvuna lehel. Lehel on 12 veergu. Vaikimisi on pilt ja tekst võrdse suurusega (kuus veergu). Samas saab suurust vastavalt vajadusele reguleerida. |

## <a name="add-a-feature-module-to-a-new-page"></a>Uuele lehele funktsioonimooduli lisamine 

Uuele lehele funktsioonimooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja looge lehe mall nimega **funktsiooni mall**.
1. Lisage vaikelehe pessa **Peamine** funktsioonimoodul.
1. Registreerige mall ja avaldage see.
1. Kasutage äsja loodud funktsiooni malli, et luua leht, mille nimi on **funktsiooni leht**.
1. Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Dialoogiaknas **Lisa moodul** jaotises **Moodulite valimine** valige funktsioonimoodul ja klõpsake seejärel nuppu **OK**.
1. Valige vasakul liigendpuus funktsioonimoodul.
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

[Pannoomoodul](add-hero-module.md)

[Videopleieri moodul](add-video-player.md)
