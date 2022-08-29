---
title: Kiirvaatemoodul
description: See artikkel hõlmab kiirvaate mooduleid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16f4b0aad803434f10a1c0ab8375552772ee534a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286860"
---
# <a name="quick-view-module"></a>Kiirvaatemoodul

[!include [banner](includes/banner.md)]

See artikkel hõlmab kiirvaate mooduleid ja kirjeldab, kuidas lisada neid saidile lehekülgedele moodulis Microsoft Dynamics 365 Commerce.

Kiirvaatemoodul võimaldab kasutajatel toodete sirvimisel loendilehel kiiresti vaadata tooteteavet ja lisada loendilehelt ostukorvi ühe või mitu toodet ilma toote üksikasjade lehele (PDP) minemiseta. Kiirvaatemoodul annab ülevaate tooteteabest, mida kasutajad vajavad "ostukorvi lisamise" otsuse tegemiseks. See sisaldab ka linki PDP-le, et kasutajad saaksid vaadata täiendavaid toote üksikasju ja ostuvalikuid.

Kiirvaatemoodulit toetavad moodulid [tootekogum](product-collection-module-overview.md) ja [otsingutulemused](search-result-module.md).

> [!IMPORTANT]
> Kiirvaatemoodul on saadaval alates Commerce'i versioonist 10.0.17.

Järgmisel illustratsioonil on näide toodete loendi lehe kiirvaate moodulist.

![Toodete loendi lehe kiirvaate mooduli näide.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

Kiirvaate moodul toetab mõningaid samu funktsioone nagu ostuboksi moodul. Seega on kiirvaate mooduli atribuudid sarnased ostukasti mooduli atribuutidega.

| Atribuut | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pealkirja silt | **H1**, **H2**, **H3**, **H4**, **H5**, or **H6** | See atribuut määratleb toote pealkirjale pealkirja sildi. Kui kiirvaate moodul on lehe ülaosas, tuleb see atribuut seada väärtusele **H1**, et vastata juurdepääsetavuse standarditele. |
| Luba kohandatud hind | **Tõene** või **Väär** | Kui atribuudi väärtuseks on seatud **Tõene**, saab kasutaja sisestada kohandatud hinna. |
| Vähim hind | Täisarv | See atribuut on rakendatav ainult siis, kui atribuut **Luba kohandatud hind** on seatud väärtusele **Tõene**. Sellega määratletakse minimaalne hind, mille kasutaja saab sisestada (nt $1). |
| Suurim hind | Täisarv | See atribuut on rakendatav ainult siis, kui atribuut **Luba kohandatud hind** on seatud väärtusele **Tõene**. Sellega määratletakse maksimaalne hind, mille kasutaja saab sisestada (nt $1,000). |

## <a name="commerce-site-builder-settings"></a>Commerce'i saidiehitaja sätted

Nagu ostukasti moodul, järgib ka kiirvaate moodul sätteid jaotises **Saidisätted \> Laiendused \> Toote ostukorvi lisamine**. Siiski, ignoreeritakse sätet **Liigu ostukorvi lehele**, sest see ei vasta kiirvaate mooduli eesmärgile, mis on võimaldada kasutajatel sirvida mitmeid tooteid loendilehel ja lisada neid ostukorvi ilma loendilehelt eemale minemiseta.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Tootekogumi moodulile kiirvaate mooduli lisamine

Kiirvaatemoodulit saab lisada tootekogumi ja otsingutulemuste moodulitele.

Tootekogumi moodulile kiirvaatemooduli lisamisekd Commerce'i saidiehitajas toimige jägmiselt.

1. Avage **Lehed** ja seejärel valige Fabrikami saidi avaleht.
1. Minge kodulehe **mis tahes** tootekogumi moodulisse, valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige kiirvaate **moodul** ja seejärel valige **OK**.
1. Valige mooduli **Kiirvaade** atribuutide paanil **Pealkiri**. Seadistage dialoogiboksis **Pealkiri** väli **Pealkirja aste** väärtusele **H2** ja seejärel valige **OK**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Tootekogumi moodul](product-collection-module-overview.md)

[Otsingutulemuste moodul](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
