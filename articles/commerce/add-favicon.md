---
title: Faviconi lisamine
description: See teema selgitab, kuidas lisada saidile faviconi.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001529"
---
# <a name="add-a-favicon"></a>Faviconi lisamine


[!include [banner](includes/banner.md)]

See teema selgitab, kuidas lisada saidile faviconi.

## <a name="overview"></a>Ülevaade

Favicon on väike graafika fail, mis kuvatakse muu hulgas veebibrauseri vahekaardil, aadressiribal, sirvimisajaloos ja järjehoidjates või lemmikutes. Soovitame lisada saidile faviconi, kuna see esindab ja tugevdab teie kaubamärki ja aitab eristada teie saiti teistest saitidest, mida teie kliendid külastavad.

Kuigi saate lisada oma saidile erineva suuruse ja failitüübiga favicone, näitab see teema, kuidas lisata ühte faviconi. Samas kasutatakse sama protsessi ja asukohta rohkemate faviconide lisamiseks.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Faviconi üleslaadimine saidi varade kollektsiooni

Faviconi saidi varade kollektsiooni üleslaadimiseks toimige järgmiselt.

1. Avage **Varad \> Laadi üles \> Varade üleslaadimine**.
1. Leidke ja valige kohalikus failisüsteemis favicon.
1. Sisestage pealkiri ja valige seejärel **OK**. 
1. Parempoolsel atribuudipaanil kopeerige faviconi avalik URL-i.

> [!NOTE]
> Kui te suvandit **Avalda varad pärast üleslaadimist** ei vali, peate naasma lehele **Varad** ja avaldama faviconi hiljem käsitsi.

## <a name="create-the-html-for-the-favicon"></a>Faviconi HTML-i loomine

Faviconi HTML-i loomiseks kasutage järgmist HTML-i lõiku. Atribuudi **href** jaoks asendage **"Avalik\_URL\_teie\_faviconi\_jaoks"** avaliku URL-iga, mille varem kopeerisite.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Lisage faviconi HTML oma lehtede elemendile \<head\>.

Oma saidile faviconi lisamiseks kasutage sama toimingut, mida kasutatakse mis tahes HTML-i või skripti lisamiseks saidi lehtede elemendile **\<head\>**.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Tervitussõnumi lisamine](add-welcome-message.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)

