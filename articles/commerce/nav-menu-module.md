---
title: Navigeerimismenüü moodul
description: See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817870"
---
# <a name="navigation-menu-module"></a>Navigeerimismenüü moodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Navigeerimismenüü moodulite peamine eesmärk on võimaldada saidi kasutajatel sirvida tooteid ja saite vastavalt Dynamics 365 Commerce'i peakontoris määratletud kanali navigeerimishierarhiale. Navigeerimismenüü moodulis konfigureeritud üksused ilmuvad saidi päise navigeerimises. Navigeerimismenüü moodulid toetavad ka staatilisi menüü-üksusi, mis lingivad e-kaubanduse saidi muudele lehtedele.

Navigeerimismenüü mooduli saab lisada lehe päisemoodulisse. Fabrikami kujunduse navigeerimismenüüs kuvatakse vaikimisi kaks taset. Starteri kujunduse navigeerimismenüüs kuvatakse vaikimisi kolm taset. Tasemete arvu muutmiseks on kujunduses nõutav vaate laiend.

Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüü näide, millel on kaks kategooriahierarhia taset ja mõned staatilised menüü-üksused.
![Navigeerimismenüü mooduli näide](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Navigeerimismenüü mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Allikas                  | **Jaemüük**, **Käsitsi koostamine**, **Jaemüük ja käsitsi koostamine** | Väärtus **Jaemüük** võimaldab navigeerimismenüüs kuvada kanali navigeerimishierarhia Commerce'i peakontorist. Väärtus **Käsitsi koostamine** võimaldab staatiliste menüüde üksusi kureerida. Väärtus **Jaemüük ja käsitsi koostamine** võimaldab mõlemat. |
| Kategooria piltide kuvamine | **Tõene** või **Väär**    | Kui see on lubatud, kuvatakse navigeerimismenüüs kategooria pildid, nagu on määratletud iga kategooria kohta Commerce’i peakontoris. Lisatud Commerce'i väljalaskesse 10.0.14. |
| Staatiline menüü-üksus| Väärtuste massiiv| Staatilised menüü-üksused, mis seostavad menüü-üksuse nime staatilise saidi lingiga. Menüü-üksusi saate luua muude menüü-üksuste all. Vaikimisi kuvatakse staatilised menüüd juuretasandil ja need lisatakse kanali navigeerimishierarhiasse, kui see on olemas. |

Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüüs kuvatav kategooria pilt.
![Kategooria piltidega navigeerimismenüü mooduli näide](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Navigeerimismenüü mooduli lisamine päisemoodulisse

Üksikasjalikumat teavet selle kohta, kuidas lisada navigeerimismenüü moodulit päisemoodulisse, vt teemast [Päisemoodul](author-header-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Küpsise vastavus](cookie-compliance.md)

[Päisemoodul](author-header-module.md)
