---
title: Kategooria sihtlehe rikastamine
description: See artikkel katab kategoorialehtede rikastamise töös Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bfee3b09768fa19ab95c880d7f7cbf330a8c58d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856960"
---
# <a name="enrich-a-category-landing-page"></a>Kategooria sihtlehe rikastamine

[!include [banner](includes/banner.md)]

See artikkel katab kategoorialehtede rikastamise töös Dynamics 365 Commerce.

Commerce pakub kategooria vaikesihtlehe, mida kasutatakse kategooria andmete kuvamise ajal. Kategooria vaikeleht sisaldab nõutud elemente, nagu piiritlusatribuudid, kategoriseeritud tootepaigutus, sortimissuvandid, valikute kokkuvõte ja lehejaotuse juhtelemendid. 

Samas võite kategooria vaikelehe asemel tahta kasutada nn rikastatud kategooria sihtlehte, kus on rohkem sisu ja palju täpsemad elemendid. Tüüpiline rikastamine võib hõlmata kategooria lehele kategooriapõhise turundussisu lisamist. See sisu võib sisaldada kategooriaüleseid tootepaigutusi kaasamüügi eesmärgil, toimetusloendeid, pilte, videoid ja muud teksti. Võite muuta kas kategooria vaikelehte või määratleda konkreetse kategooria jaoks erineva kategoorialehe.

![Rikastatud kategooria sihtleht.](./media/CategoryLandingPages.png)

Commerce'i saidiehitajas sisaldab leht **Tooted** loendit kategooriatest, mis on pärit saidile määratud kanalist. Kui kategooria lehe jaoks on valitud olek **Rikastatud**, on see kategooria leht rikastatud. Muul juhul kasutatakse kategooria jaoks kategooria vaikelehte ja sisu. Võite kuvada kategooria jaoks nii rikastatud kui ka mitte rikastatud kategooria lehtede eelvaate, valides kategooria nime.

Kategooria lehe rikastamiseks tehke järgmist.

1. Lehel **Tooted** valige kategooria nimi, mille jaoks soovite kategooria lehte rikastada. Lehe redaktoris avatakse valitud kategooria jaoks kategooria vaikeleht.
2. Valige suvand **Kategooria lehe rikastamine**.
3. Valige rikastatud kategooria lehele mall. Kui teete ainult väikeseid muudatusi, saate valida kategooria vaikelehe. Teise võimalusena saate valida konkreetse kategooria lehe malli. Malli valimisel avatakse lehe redaktor ja valitud malli kasutatakse valitud kategooria jaoks uue kategooria lehe loomiseks. Leht registreeritakse teie jaoks välja ja saate nüüd oma muudatused teha.

> [!NOTE]
> Kategooria täpsustuse andmeid kasutavad moodulid kasutavad teie valitud kategooria andmeid. Valitud malli sätted määravad muudatused, mida saate teha.

## <a name="additional-resources"></a>Lisaressursid

[Olemasoleva saidilehe muutmine](modify-existing-page.md)

[Uue saidilehe lisamine](add-new-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)

[Lehe salvestamine, eelvaade ja avaldamine](save-preview-publish-page.md)

[Tootelehe rikastamine](enrich-product-page.md)

[Lehe sisu hõlbustusfunktsioonide kinnitamine](verify-accessibility.md)

[Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
