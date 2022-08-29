---
title: Aktiivne pildimoodul
description: See artikkel hõlmab aktiivseid pildimooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: fdcd54adc98c7bc52ab6ff1ef7d5d03616aadfc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267613"
---
# <a name="active-image-module"></a>Aktiivne pildimoodul

[!include [banner](includes/banner.md)]

See artikkel hõlmab aktiivseid pildimooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Aktiivset pildimoodulit saab kasutada tootesiltide pildile kaasamiseks. E-commerce saidi kasutajad saavad seejärel hõljutada kursorit siltide kohal, et vaadata pildil näidatud toodet. Eelvaated kuvatakse hüpikakendes. Valides hüpikakna eelvaate, saavad kasutajad minna otse vastava toote üksikasjade lehele.

Sildid määratletakse pildil X- ja Y-koordinaatide abil. Iga märgistatud punkt peab olema konfigureeritud pildil kuvatava toote ID-ga.

Järgmine näide kuvab näite hüpikakna eelvaatest pildil Adventure Worksi kodulehel.

![Aktiivse pildimooduli eelvaate hüpikakna näide](./media/Active_image.PNG)

> [!IMPORTANT]
> - Aktiivne pildimoodul on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.
> - Aktiivne pildimoodul kuvatakse Adventure Worksi teemas.

## <a name="active-image-module-properties"></a>Aktiivse pildimooduli atribuudid

| Atribuudi nimi      | Väärtused | Kirjeldus |
|--------------------|--------|-------------|
| Pilt              | Pildifail | Pilti saab kasutada ühe või mitme toote esitlemiseks. Pildi saab Commerce site koostajas üles laadida meediateeki või kasutada olemasolevat pilti. |
| Laius              | Pikslite arv | See atribuut määratleb pildi laiuse. Aktiivsed koordinaadid arvutatakse pildi laiuse alusel.|
| Aktiivsed koordinaadid | X- ja Y-koordinaadid ning toote ID-kood | Iga aktiivne pildi massiiv koosneb X- ja Y-koordinaatdest ning toote ID-numbrist.|
| Päis            | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Vaikimisi kasutatakse **H2** pealkirja silti päises, kuid pealkirja silti saab vajadusel muuta juurdepääsu nõuetele vastavaks. |
| Lõik          | Lõigu tekst | Moodul toetab RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu hüperlingid ja paks, allajoonitud, ning kursiivis tekst. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Seos               | Lingi tekst, lingi URL, Accessible Rich Internet Applications (ARIA) silt ja suvand **Ava link uuel vahekaardil** valija | Moodulid toetavad üht või mitut tegutsemiskutse linki. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil. |
| Alamtekst           | Pealkirja tekst ja lingid | Pildile saate lisada täiendavat sisu nagu nt autori või kujundaja nime või lingid isiklikele ajaveebidele.|
| Teksti kujundus         | **Hele** või **tume** | Atribuut võimaldab kasutajal taustapildi põhjal seada teksti heledaks või tumedaks seada. See on saadaval teema laiendina Adventure Worksi teemas. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Aktiivse pildimooduli lisamine uuele leheküljele

Uuele lehele aktiivse pildimooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Minge **mallidesse** ja avage oma saidi avalehe turundusmall (või looge uus turundusmall).
1. **Vaikelehe** põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige aktiivse **pildi moodul** ja seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge **lehekülgedele** ja avage saidi avaleht (või looge uus avaleht, kasutades turundusmalli).
1. Vaikelehe põhipesas valige kolmikpunkti nupp (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige aktiivse **pildi moodul** ja seejärel valige **OK**.
1. Aktiivse pildimooduli atribuudipaanil saate lisada pildi ja seada lõuendi laiuse pildi suuruseks.
1. Määrake X- ja Y-koordinaadid ning lisage sobiv toote ID-kood.
1. Lisage ja konfigureerige lisa aktiivseid pildimooduleid vastavalt vajadusele.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Adventure Works teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
