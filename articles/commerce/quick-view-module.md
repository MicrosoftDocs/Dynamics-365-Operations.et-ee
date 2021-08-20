---
title: Kiirvaatemoodul
description: See teema hõlmab kiirvaatemooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 24b3a5552a83bfea52f6a274b836955e41acdb4281f7b7807acf040e9cd4af30
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777472"
---
# <a name="quick-view-module"></a>Kiirvaatemoodul

[!include [banner](includes/banner.md)]

See teema hõlmab kiirvaatemooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

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
1. Avage avalehel mistahes **Tootekogum**, valige kolmikpunkt (**...**) ja seejärel valige **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Kiirvaade** ja klõpsake seejärel **OK**.
1. Valige mooduli **Kiirvaade** atribuutide paanil **Pealkiri**. Seadistage dialoogiboksis **Pealkiri** väli **Pealkirja aste** väärtusele **H2** ja seejärel valige **OK**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Tootekogumi moodul](product-collection-module-overview.md)

[Otsingutulemuste moodul](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
