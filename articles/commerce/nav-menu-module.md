---
title: Navigeerimismenüü moodul
description: See artikkel hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d58d3957749fa961b7be164a0a474ac90a23321f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281504"
---
# <a name="navigation-menu-module"></a>Navigeerimismenüü moodul

[!include [banner](includes/banner.md)]

See artikkel hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce

Navigeerimismenüü moodulite peamine eesmärk on võimaldada saidi kasutajatel sirvida tooteid ja saite vastavalt Dynamics 365 Commerce'i peakontoris määratletud kanali navigeerimishierarhiale. Navigeerimismenüü moodulis konfigureeritud üksused ilmuvad saidi päise navigeerimises. Navigeerimismenüü moodulid toetavad ka staatilisi menüü-üksusi, mis lingivad e-kaubanduse saidi muudele lehtedele.

Navigeerimismenüü mooduli saab lisada lehe päisemoodulisse. Fabrikami kujunduse navigeerimismenüüs kuvatakse vaikimisi kaks taset. Starteri kujunduse navigeerimismenüüs kuvatakse vaikimisi kolm taset. Tasemete arvu muutmiseks on kujunduses nõutav vaate laiend.

Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüü näide, millel on kaks kategooriahierarhia taset ja mõned staatilised menüü-üksused.
![Navigeerimismenüü mooduli näide.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Navigeerimismenüü mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Allikas                  | **Jaemüük**, **Käsitsi koostamine**, **Jaemüük ja käsitsi koostamine** | Väärtus **Jaemüük** võimaldab navigeerimismenüüs kuvada kanali navigeerimishierarhia Commerce'i peakontorist. Väärtus **Käsitsi koostamine** võimaldab staatiliste menüüde üksusi kureerida. Väärtus **Jaemüük ja käsitsi koostamine** võimaldab mõlemat. |
| Kategooria piltide kuvamine | **Tõene** või **Väär**    | Kui see on lubatud, kuvatakse navigeerimismenüüs kategooria pildid, nagu on määratletud iga kategooria kohta Commerce’i peakontoris. Lisatud Commerce'i väljalaskesse 10.0.14. |
| Kuva reklaamipildid | **Tõene** või **Väär** | Kui see atribuut on lubatud, saab kampaaniaid konfigureerida piltide, linkide ja teksti abil. See atribuut lisati Commerce'i versiooni 10.0.17 väljalaskesse. |
|Lisa kategooria reklaamsisu | Tekst, pilt või link | Kui atribuut **Kuva kreklaampildid** on lubatud, saate lisada navigeerimismenüüst kampaaniasisuna teksti, pildi või lingi. |
| Mitme tasemega navigeerimismenüü lubamine | **Tõene** või **Väär** | Kui see atribuut on lubatud, võib navigeerimismenüü kuvada navigeerimise hierarhia mitut taset. See funktsioon on saadaval Commerce'i versiooni 10.0.15 väljalaskes. |
| Tasemete arv | täisarv | See atribuut määratleb tasemete numbrid, mis tuleb kuvada, kui atribuudi **Luba mitmetasandiline navigeerimismenüü** väärtuseks on seatud **Tõene**. |
| Staatiline menüü-üksus| Väärtuste massiiv| Staatilised menüü-üksused, mis seostavad menüü-üksuse nime staatilise saidi lingiga. Menüü-üksusi saate luua muude menüü-üksuste all. Vaikimisi kuvatakse staatilised menüüd juuretasandil ja need lisatakse kanali navigeerimishierarhiasse, kui see on olemas. |
| Juurmenüü kuvamine | **Tõene** või **Väär** | Kui see atribuut on lubatud, saab navigeerimismenüü määratleda kohandatud juure alusel (nt **Osta kohe**). See funktsioon on saadaval Dynamics 365 Commerce'i versioonis 10.0.15. |
| Juurmenüü | string | Seda atribuuti saab kasutada kohandatud juure teksti määratlemiseks, kui atribuudi **Kuva juurmenüü** väärtuseks on seatud **Tõene**. |

Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüüs kuvatav kategooria pilt.
![Kategooria piltidega navigeerimismenüü mooduli näide.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Navigeerimismenüü mooduli lisamine päisemoodulisse

Üksikasjalikumat teavet selle kohta, kuidas lisada navigeerimismenüü moodulit päisemoodulisse, vt teemast [Päisemoodul](author-header-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Lingireamoodul](add-breadcrumb.md)

[Saidi valija moodul](site-selector.md)

[Ostukastimoodul](add-buy-box.md)

[Küpsise vastavus](cookie-compliance.md)

[Päisemoodul](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
