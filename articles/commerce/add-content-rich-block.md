---
title: Tekstiploki moodul
description: See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411609"
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

Järgmisel pildil on näide tekstiploki moodulist, mida kasutatakse avalehel.

![Tekstiploki mooduli näide](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Tekstiploki mooduli omadused

| Atribuudi nimi     | Väärtus                                            | Kirjeldus |
|-------------------|--------------------------------------------------|-------------|
| Rikastekst         | Rikastekst                                        | Lõigu tekst. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst. |
| Kohandatud klassinimi | Kaskaadlaadistiku (CSS) klassi nimi        | Kohandatud CSS-i klassi nimi, mille arendaja annab selle mooduli vormindamiseks. Klassi nimi tuleks määratleda kujundusepaketis. |
| Fondi suurus         | **Väike**, **Keskmine**, **Suur** või **Väga suur** | Sisu fondi suurus. |

## <a name="add-a-text-block-module-to-a-page"></a>Tekstiploki mooduli lehele lisamine

Uuele lehele tekstiploki mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksi **Uus mall** jaotises **Malli nimi** **Sisumall**.
1. Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiaknas **Vali mall** **Sisumall**. Sisestage jaotises **Lehe nimi** väärtus **Sisuleht** ja seejärel valige **OK**.
1. Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**. 
1. Lisage tekst tekstiploki mooduli atribuutide paani väljale **Rikastekst**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kampaania ribareklaami moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Sisuploki moodul](add-hero-module.md)

[Videopleierimoodul](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]