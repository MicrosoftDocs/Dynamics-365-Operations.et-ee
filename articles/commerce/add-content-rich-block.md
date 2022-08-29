---
title: Tekstiploki moodul
description: See artikkel katab tekstiblokaadi moodulid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270478"
---
# <a name="text-block-module"></a>Tekstiploki moodul

[!include [banner](includes/banner.md)]

See artikkel katab tekstiblokaadi moodulid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce.

Tekstiploki moodul on moodul, mida kasutatakse tekstilise sisu lisamiseks. See sisu võib olla kas teavitav või kampaaniaga seotud.

Tekstiploki moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele. Need on eraldiseisvad moodulid, mis ei sõltu lehekülje kontekstist ega ühestki teisest moodulist.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>E-kaubanduse tekstiploki moodulite näited

Tekstiploki mooduleid saab kasutada järgmistel viisidel.

* Toote üksikasjade lehel toote funktsioonide tutvustamiseks.
* Teavitamise eesmärgil mis tahes lehel. Näiteks võivad need selgitada püsikliendiprogrammide eeliseid, kirjeldada tarne- ja tagastamispoliitikaid, vastata korduma kippuvatele küsimustele või lisada sisu osale „Tutvustus”.
* Lisada toote üksikasjade lehele kohandatud sõnumeid. (nt „Üle 50 euro maksvad tellimused tarnitakse tasuta”).
* Lahtiütluste ja kontaktandmete jaoks toote üksikasjade lehtedel, ostukorvi lehtedel, maksmise lehtedel ja teistel lehtedel (nt „Tarnimisele ja tagastustele kehtivad poe eeskirjad”).

Järgmisel pildil on näide tekstiploki moodulist, mida kasutatakse avalehel.

![Tekstiploki mooduli näide.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Tekstiploki mooduli omadused

| Atribuudi nimi     | Väärtus                                            | Kirjeldus |
|-------------------|--------------------------------------------------|-------------|
| Rikastekst         | Rikastekst                                        | Lõigu tekst. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst. |
| Kohandatud klassinimi | Kaskaadlaadistiku (CSS) klassi nimi        | Kohandatud CSS-i klassi nimi, mille arendaja annab selle mooduli vormindamiseks. Klassi nimi tuleks määratleda kujundusepaketis. |
| Fondi suurus         | **Väike**, **Keskmine**, **Suur** või **Väga suur** | Sisu fondi suurus. |

## <a name="add-a-text-block-module-to-a-page"></a>Tekstiploki mooduli lehele lisamine

Uuele lehele tekstiploki mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Dialoogiboksis Uus **mall** sisestage malli nime **all** sisumall **·**.
1. Kehapesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige vaikelehemoodul **ja** seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Dialoogiaknas **Uue lehe loomine** sisestage jaotises **Lehe nimi** sisuleht **ja** seejärel valige suvand **Edasi**.
1. Valige **jaotises Vali mall** sisumall **ja** seejärel **edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui teil on vaja lehekülje teavet redigeerida, valige **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**. 
1. Uue lehekülje põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige tekstibloki **moodul** ja seejärel valige **OK**. 
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
