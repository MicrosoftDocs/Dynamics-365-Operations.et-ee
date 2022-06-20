---
title: Saidi valija moodul
description: See artikkel katab saidi valijamooduli ja kirjeldab, kuidas lisada see saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
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
ms.openlocfilehash: ef7753658f878fdf76c6a6beb82ce54e9c12e212
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884599"
---
# <a name="site-picker-module"></a>Saidi valija moodul

[!include [banner](includes/banner.md)]

See artikkel katab saidi valijamooduli ja kirjeldab, kuidas lisada see saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Kui ettevõttel on eri turgudel, piirkondadel ja lokaatidel erinevad saidid, on saidi kasutajatel vaja hõlpsasti liikuda saitide vahel ja valida enda eelistatud ostlemissait. Selle stsenaariumi järgimiseks võimaldab saidi valija moodul kasutajatel sirvida mitmel saidil. Saidi valija on [soovitatav ka siis, kui geotuvastus](geo-detection-redirection.md) ja ümbersuunamine on teie e-kaubanduse saidi puhul kasutusele võetud, nii et klientidel on võimalus alistada saidi eelistus, [mida nad riigi/regiooni komplektaatori mooduli](country-region-picker-module.md) abil näitavad. 

Saidi valija moodul peab olema konfigureeritud nende saitide loendiga (turud, regioonid või lokid), mida saidi kasutajad saavad sirvida. Järgmine näide näitab näidet saidi valijamooduli kohta, mis on saidilehe päises.

![Näide saidi valijamooduli kohta saidilehe päises.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Saidi valijamooduli atribuudid

| Atribuudi nimi | Väärtus                 | Kirjeldus |
|---------------|-----------------------|-------------|
| Pealkiri       | Tekst                  | Mooduli pealkiri. |
| Saidisuvandid  | Nimi, pilt, URL      | See atribuut määrab nime, lingi saidi avalehele ja valikulise pildi, mida kuvatakse iga moodulisse lisatud saidi jaoks. Pildiks võib olla lipp või midagi muud, mis tähistab turgu, piirkonda või lokaati. |

## <a name="add-a-site-picker-module-to-a-page"></a>Saidi valijamooduli lisamine lehele

Saidi valijamooduli saab lisada päisemooduli **saidi valija** pesasse [...](author-header-module.md). Pärast saidivalija mooduli lisamist saate määrata mooduli päise ja saidi valikud. Üldiselt sisaldub päisemoodul päise killus, mida saab jagada saidi e-kaubanduse lehtede vahel. 

Saidi valijamooduli lisamiseks päisemoodulile järgige neid samme.

1. Päise killu päisemooduli saidivalija pesas valige ellips (**...**) ja seejärel valige **lisamoodul**.**·**
1. **Dialoogiboksis Vali moodulid** lisage saidi valija **moodul** ja seejärel valige **OK**.
1. Saidi valija **atribuutide paanil** valige suvand Lisa **saidi suvandite loend**. Kuvatakse redigeeritava **saidi suvandite** loendi suvand.
1. Valige **saidi suvandite loend**. Kuvatakse **saidi suvandite** loendi dialoogiboks.
1. Sisestage **saidi** nime all saidi nime tekst, mis kuvatakse saidi valija ripploendis.
1. Valige **jaotises Saidi ümbersuunamise** URL **suvand Lisa link**. Kuvatakse **lingi väljalõpppaan** Lisa.
1. Valige paanil **Lingi** lisamine suvand Kohandatud **ja** seejärel suvand **Edasi**.
1. Valige saidi URL-i loendist URL, mille lõite kanali lisamisel saidile (`www.adventure-works.com/fr-ca` nt) ja seejärel valige **rakenda**.
1. Valige nupp **OK**.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **lehe** avaldamiseks avaldamine.

Järgmises näites on saidi valijamoodul lisatud päisemooduli saidi valija pesasse, **mis** sisaldub päise fragmendis nimega **HeaderContainer**.

![Näide saidi valijamoodulist päise tükis.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Päisemoodul](author-header-module.md)

[Lingireamoodul](add-breadcrumb.md)

[Navigeerimismenüü moodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
