---
title: Kategooria sihtlehe rikastamine
description: See artikkel katab kategoorialehtede rikastamise töös Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e3397ffee9b32f3d3efedea38255f88daee5233c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282157"
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
