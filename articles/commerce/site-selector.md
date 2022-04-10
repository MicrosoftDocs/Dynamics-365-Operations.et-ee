---
title: Saidi valija moodul
description: See teema käsitleb saidi valijamoodulit ja kirjeldab, kuidas lisada see saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2022
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 381163fdd6180a76def2e1bfb733f597b611c517
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109702"
---
# <a name="site-picker-module"></a>Saidi valija moodul

[!include [banner](includes/banner.md)]

See teema käsitleb saidi valijamoodulit ja kirjeldab, kuidas lisada see saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Kui ettevõttel on eri turgudel, piirkondadel ja lokaatidel erinevad saidid, on saidi kasutajatel vaja hõlpsasti liikuda saitide vahel ja valida enda eelistatud ostlemissait. Selle stsenaariumi järgimiseks võimaldab saidi valija moodul kasutajatel sirvida mitmel saidil.

Saidi valija moodul peab olema konfigureeritud nende saitide loendiga (turud, regioonid või lokid), mida saidi kasutajad saavad sirvida.

> [!NOTE]
> Saidi valijamoodul on saadaval väljalaskes Dynamics 365 Commerce 10.0.14.

Järgmine näide näitab näidet saidi valijamooduli kohta, mis on saidilehe päises.

![Näide saidi valijamooduli kohta saidilehe päises.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Saidi valijamooduli atribuudid

| Atribuudi nimi | Väärtus                 | Kirjeldus |
|---------------|-----------------------|-------------|
| Pealkiri       | Tekst                  | Mooduli pealkiri. |
| Saidisuvandid  | Nimi, pilt, URL      | See atribuut määrab nime, lingi saidi avalehele ja valikulise pildi, mida kuvatakse iga moodulisse lisatud saidi jaoks. Pildiks võib olla lipp või midagi muud, mis tähistab turgu, piirkonda või lokaati. |

## <a name="add-a-site-picker-module-to-a-page"></a>Saidi valijamooduli lisamine lehele

Saidi valijamooduli saab lisada päisemooduli **saidi valija** pesasse [...](author-header-module.md). Pärast saidivalija mooduli lisamist saate määrata mooduli päise ja saidi valikud. Üldiselt sisaldub päisemoodul päise killus, mida saab jagada saidi e-kaubanduse lehtede vahel. Järgmises näites on saidi valijamoodul lisatud päisemooduli saidi valija pesasse, **mis** sisaldub päise fragmendis nimega **HeaderContainer**.

![Näide saidi valijamoodulist päise tükis.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Päisemoodul](author-header-module.md)

[Lingireamoodul](add-breadcrumb.md)

[Navigeerimismenüü moodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
