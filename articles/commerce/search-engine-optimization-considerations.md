---
title: Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused
description: See artikkel katab otsingumootori optimeerimise (SEO) kaalutlused saidilt arenduse ja tootmiseni.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 6747df3c56fb05248210f78ebf2176a56ce78329
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896897"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused


[!include [banner](includes/banner.md)]

See artikkel katab otsingumootori optimeerimise (SEO) kaalutlused saidilt arenduse ja tootmiseni.

## <a name="a-site-that-is-under-development"></a>Arendatav sait

Kindlustamaks, et otsingumootorid ei indekseeri arenduse all saiti, **peaksid kõigil saidilehtedel olema noindex** **ja nofollow** metasildid. Hea tava on luua killus, mis põhineb [MetaTagsi moodulil](metatags-module.md), mis sisaldab järgmist metasildi kirjet ja veenduge, et kill lisatakse kõigi teie saidil kasutatavate mallide HTML-jaotisesse \<head\>.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Saidi esialgne käivitamine

"Esialgse käivitamise" ajal tehakse veebisait kättesaadavaks piiratud publikule või turule enne täieliku käivitamise toimumist. Kui käivitate oma veebisaidi kergelt, peaksite kaaluma **sõlme metasiltide** mahajätmist. Sel viisil aitate tagada, et esialgne käivitamine piirduks piiratud publikuga, kelleni soovite jõuda.

## <a name="a-site-that-is-in-production"></a>Sait, mis on tootmises

Kui sait on tootmisse kaasatud, veenduge, et kõik saidi lehed on õigesti märgistatud. Microsoft Dynamics 365 Commerce kasutab lehe jaoks sisestatud teavet, et renderdada kõik SEO andmed sellel lehel. Järgmised moodulid pakuvad seda funktsiooni: kategooria lehekülje kokkuvõte, loendi lehekülje kokkuvõte ja toote lehekülje kokkuvõte.

Otsingumootori indekseerimise optimeerimiseks kasutab renderdamise raamistik mõlemat teavet SEO atribuutidest, mis on konfigureeritud rakenduses Dynamics 365 Commerce ja konkreetse mooduli teabes. Tootmiseks kasutatava saidi puhul peaksite veenduma, et fail robots.txt võimaldab kogu saidi indekseerimist ja see sisaldab linke teie avaldatud saidi vastenduse dokumendile. Peaksite lülitama saidi kaardi loomise funktsioonid **Saidi sätted \> Saidi kaart on lubatud**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Lehekülje SEO sätted sisemise eelvaate, piiratud sihtrühmade ja kogu publiku jaoks

Kuna rakendus Dynamics 365 Commerce toetab „mida sa näed on see, mida sa saad” (WYSIWYG) autenditud eelvaateid visuaalses leheehitajas, saavad autorid ette valmistada oma lehe sisu, ilma et peaks muretsema, et teave muutub saidi külastajatele nähtavaks. Kui leht tuleb avaldada, kuid selle mõju peab olema piiratud, **peab sellel olema metasilt noindex**, nii et otsingumootorid ei indekseeri seda. Seejärel, kui leht on kõigi sihtrühmade jaoks valmis, tuleb esitada kõik põhilised SEO metaandmed, et maksimeerida otsingumootori indekseerimise efektiivsust. Lisaks tuleb sõlme **meta silt** eemaldada.

## <a name="additional-resources"></a>Lisaressursid

[E-kaubanduse kasutajate ja rollide haldamine](manage-ecommerce-users-roles.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)

[Sisu turbepoliitika (CSP) haldamine](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
