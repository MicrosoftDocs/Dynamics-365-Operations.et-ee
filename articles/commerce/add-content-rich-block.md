---
title: Tekstiploki moodul
description: See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025593"
---
# <a name="text-block-module"></a>Tekstiploki moodul


[!include [banner](includes/banner.md)]

See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Tekstiploki moodul on moodul, mida kasutatakse tekstilise sisu lisamiseks. See sisu võib olla kas teavitav või kampaaniaga seotud.

Tekstiploki moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele. Need on eraldiseisvad moodulid, mis ei sõltu lehekülje kontekstist ega ühestki teisest moodulist.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>E-kaubanduse tekstiploki moodulite näited

Tekstiploki mooduleid saab kasutada järgmistel viisidel.

* Toote üksikasjade lehel toote funktsioonide tutvustamiseks.
* Teavitamise eesmärgil mis tahes lehel. Näiteks võivad need selgitada püsikliendiprogrammide eeliseid, kirjeldada tarne- ja tagastamispoliitikaid, vastata korduma kippuvatele küsimustele või lisada sisu osale „Tutvustus”.
* Lisada toote üksikasjade lehele kohandatud sõnumeid. (nt „Üle 50 euro maksvad tellimused tarnitakse tasuta”).
* Lahtiütluste ja kontaktandmete jaoks toote üksikasjade lehtedel, ostukorvi lehtedel, maksmise lehtedel ja teistel lehtedel (nt „Tarnimisele ja tagastustele kehtivad poe eeskirjad”).

## <a name="text-block-module-properties"></a>Tekstiploki mooduli omadused

| Atribuudi nimi     | Value                                            | Kirjeldus |
|-------------------|--------------------------------------------------|-------------|
| Rikastekst         | Rikastekst                                        | Lõigu tekst. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst. |
| Kohandatud klassinimi | Kaskaadlaadistiku (CSS) klassi nimi        | Kohandatud CSS'i klassi nimi, mille arendaja annab selle mooduli vormindamiseks. Klassi nimi tuleks määratleda kujundusepaketis. |
| Fondi suurus         | **Väike**, **Keskmine**, **Suur** või **Väga suur** | Sisu fondi suurus. |

## <a name="add-a-text-block-module-to-a-page"></a>Tekstiploki mooduli lehele lisamine

Uuele lehele tekstiploki mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge lehe mall nimega **Sisu mall**. 
1. Lisage pesasse **Kehatekst** moodul **Vaikeleht**.
1. Viige lõpuni malli redigeerimine ja avaldage see.
1. Kasutage äsja loodud sisu malli, et luua leht, mille nimi on **Sisu leht**.
1. Lisage uue lehe pessa **Peamine** konteinermoodul.
1. Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.
1. Lisage konteineri moodulile tekstiploki moodul. 
1. Lisage tekst tekstiploki mooduli atribuutide paani väljale **Rikastekst**.
1. Viige lõpuni lehe redigeerimine ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Reklaambänneri moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Sisuploki moodul](add-hero-module.md)

[Videopleierimoodul](add-video-player.md)

