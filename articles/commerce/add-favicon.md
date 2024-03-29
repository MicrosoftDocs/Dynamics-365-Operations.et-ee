---
title: Leheikooni lisamine
description: See artikkel selgitab, kuidas lisada oma saidile ikooni.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 41d6d8f823c7364f9206fd0f7588e35b6f0a018a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270433"
---
# <a name="add-a-favicon"></a>Leheikooni lisamine

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas lisada oma saidile ikooni.

Favicon on väike graafika fail, mis kuvatakse muu hulgas veebibrauseri vahekaardil, aadressiribal, sirvimisajaloos ja järjehoidjates või lemmikutes. Soovitame lisada saidile faviconi, kuna see esindab ja tugevdab teie kaubamärki ja aitab eristada teie saiti teistest saitidest, mida teie kliendid külastavad.

Ehkki saate saidile lisada mitmeid mitme erineva suuruse ja failitüübiga failitüüpe, näitab see artikkel, kuidas lisada üks mõõdukonteiin. Samas kasutatakse sama protsessi ja asukohta rohkemate faviconide lisamiseks.

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

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Teie lemmikuikooni metasilti sisaldava fragmendi loomine

Teie lemmikuikooni metasilti sisaldava fragmendi loomiseks järgige neid juhiseid.

1. Avage **Fragmendid** ja valige **Uus**.
1. Määrake dialoogiboksis **Uus fragment** mooduliks (millel põhineb fragment) **Metasildid**.
1. Sisestage fragmendi nimi ja valige **OK**.
1. Valige fragmendihierarhiapuus tütarüksus **Vaikimisi metasildid**.
1. Valige parempoolsel paanil jaotises **Metasildid** suvand **Lisa** ja seejärel sisestage HTML-string, mille eelnevalt faviconi jaoks lõite. 
1. Valige **Lõpeta redigeerimine** ja seejärel valige fragmendi avaldamiseks **Avalda**.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Metasildi fragmendi lisamine lehtede HTML-i päise jaotisse

Metasildi fragmendi lisamiseks lehtede HTML-i **päise** jaotisse järgige neid juhiseid.

1. Avage **Mallid**, avage lehtede mall, mille soovite oma faviconile lisada ja valige seejärel **Redigeeri**.
1. Valige malli hierarhiapuus ümbrisest **HTML-i päis** paremal asuv kolmikpunkti (**...**) nupp ja seejärel valige **Lisa fragment**.
1. Valige dialoogiboksis **Vali fragment** varem loodud metasildi fragment ja seejärel valige **OK**.
1. Valige **Lõpeta redigeerimine** ja seejärel valige malli avaldamiseks **Avalda**.

> [!NOTE]
> Kui teie sait kasutab rohkem kui ühte malli, peate metasiltide fragmendi lisama kõigile mallidele.

Kui vaatate nende lehtede eelversiooni, mis põhinevad mallil, millele lisasite metasiltide fragmendi, peaksite nüüd nägema lemmikuikooni brauseri vahekaardil.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
