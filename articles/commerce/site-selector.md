---
title: Saidi valija moodul
description: See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e24590d4a8f172809704aab0d761f6db0fb0e11b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234337"
---
# <a name="site-selector-module"></a>Saidi valimise moodul

[!include [banner](includes/banner.md)]

See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Kui ettevõttel on eri turgudel, piirkondadel ja lokaatidel erinevad saidid, on saidi kasutajatel vaja hõlpsasti liikuda saitide vahel ja valida enda eelistatud ostlemissait. Selle stsenaariumi võimaldamiseks saavad kasutajad saidi valija moodulis sirvida mitmel saidil.

Saidi valija moodulis tuleb konfigureerida saitide loend (turud, piirkonnad või lokaadid), millel saidi kasutajad saavad sirvida.

> [!NOTE]
> Saidi valija moodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.14.

Järgmisel joonisel on kujutatud saidi lehe päises esiletõstetud saidi valija mooduli näide.

![Saidi valija mooduli näide saidi lehe päises](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Saidi valija mooduli atribuudid

| Atribuudi nimi | Väärtus                 | Kirjeldus |
|---------------|-----------------------|-------------|
| Pealkiri       | Tekst                  | Mooduli pealkiri. |
| Saidisuvandid  | Nimi, pilt, URL      | See atribuut määrab nime, lingi saidi avalehele ja valikulise pildi, mida kuvatakse iga moodulisse lisatud saidi jaoks. Pildiks võib olla lipp või midagi muud, mis tähistab turgu, piirkonda või lokaati. |

## <a name="add-a-site-selector-module-to-a-page"></a>Saidi valija mooduli lehele lisamine

Saidi valija moodulit saab lisada saidi valija pesa [päise moodulisse](author-header-module.md). Pärast selle lisamist saate määratleda mooduli pealkirja ja saidi suvandid.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Päisemoodul](author-header-module.md)

[Lingireamoodul](add-breadcrumb.md)

[Navigeerimismenüü moodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]