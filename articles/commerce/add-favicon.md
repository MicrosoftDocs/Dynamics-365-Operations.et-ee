---
title: Faviconi lisamine
description: See teema selgitab, kuidas lisada saidile faviconi.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d95e8b799c3b89418657342868e0ec7e94a86f9
ms.sourcegitcommit: ce79fb570e299a26a644e29da7ceb5a57a1374e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295076"
---
# <a name="add-a-favicon"></a>Faviconi lisamine

[!include [banner](includes/banner.md)]

See teema selgitab, kuidas lisada saidile faviconi.

## <a name="overview"></a>Ülevaade

Favicon on väike graafika fail, mis kuvatakse muu hulgas veebibrauseri vahekaardil, aadressiribal, sirvimisajaloos ja järjehoidjates või lemmikutes. Soovitame lisada saidile faviconi, kuna see esindab ja tugevdab teie kaubamärki ja aitab eristada teie saiti teistest saitidest, mida teie kliendid külastavad.

Kuigi saate lisada oma saidile erineva suuruse ja failitüübiga favicone, näitab see teema, kuidas lisata ühte faviconi. Samas kasutatakse sama protsessi ja asukohta rohkemate faviconide lisamiseks.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Faviconi üleslaadimine saidi varade kollektsiooni

Faviconi saidi varade kollektsiooni üleslaadimiseks toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.
1. Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.
1. Tuvastage File Exploreri aknas faviconi pildifail, mille soovite üles laadida, valige see ning seejärel valige **Ava**.
1. Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.
1. Pildi avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.

    > [!NOTE]
    > Kui te ei märgista ruutu **Avalda meediumiüksused pärast üleslaadimist**, peate naasma lehele **Meediumiüksused** ja avaldama faviconi hiljem käsitsi.

1. Valige nupp **OK**.
1. Parempoolsel atribuudipaanil kopeerige faviconi avalik URL-i. Seda URL-i kasutate hiljem.

## <a name="create-the-html-for-your-favicon"></a>Faviconi jaoks HTML-i loomine

Faviconi HTML-i loomiseks kasutage järgmist HTML-stringi. Atribuudi **href** jaoks asendage **Avalik\_URL\_teie\_faviconi\_jaoks** avaliku URL-iga, mille varem kopeerisite.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a>Looge lehefragment, mis sisaldab teie faviconi metasilti

Teie faviconi sisaldava lehefragmendi loomiseks toimige järgmiselt.

1. Avage suvand **Lehe fragmendid** ja valige seejärel **Uus**.
1. Valige dialoogiaknas **Uus lehefragment** lehefragmendi aluseks oleva moodulina **Metasildid**.
1. Sisestage lehefragmendi nimi ja seejärel valige nupp **OK**.
1. Valige fragmendihierarhiapuus tütarüksus**Vaikimisi metasildid**.
1. Valige parempoolsel paanil jaotises **Metasildid** suvand **Lisa** ja seejärel sisestage HTML-string, mille eelnevalt faviconi jaoks lõite. 
1. Valige **Lõpeta redigeerimine** ja seejärel valige lehefragmendi avaldamiseks **Avalda**.

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a>Lisage metasildi lehefragment oma lehtede HTML-i päise jaotisesse

Metasildi lehefragmendi lisamiseks oma lehtede HTML-i **päise** jaotisesse toimige järgmiselt.

1. Avage **Mallid**, avage lehtede mall, mille soovite oma faviconile lisada ja valige seejärel **Redigeeri**.
1. Vajutage mallihierarhiapuus kolmikpunkti (**...**) nupule, mis paikneb konteineri **HTML-i päis** paremal küljel, ja valige seejärel **Lisa lehefragment**.
1. Valige dialoogiaknas **Lehefragmendi valimine** varem loodud metasildi lehefragment ja seejärel **OK**.
1. Valige **Lõpeta redigeerimine** ja seejärel valige malli avaldamiseks **Avalda**.

> [!NOTE]
> Kui teie saidil kasutatakse enam kui üht malli, siis peate kõigile lisama metasiltide lehefragmendi.

Kui kuvate selliste lehtede eelvaate, mis põhinevad mallil, millele lisasite metasiltide lehefragmendi, siis peaksite nüüd nägema brauseriaknas faviconi.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Tervitussõnumi lisamine](add-welcome-message.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)

