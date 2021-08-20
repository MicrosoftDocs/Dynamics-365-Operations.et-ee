---
title: Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused
description: See teema hõlmab otsingumootori optimeerimise (SEO) kaalutlusi teie saidi jaoks arengust tootmiseni.
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: df92aeae967bbf248b90dffc6bc2239a8d2959183acb9e9181bc344b9e3eff8d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716853"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused


[!include [banner](includes/banner.md)]

See teema hõlmab otsingumootori optimeerimise (SEO) kaalutlusi teie saidi jaoks arengust tootmiseni.

## <a name="a-site-that-is-under-development"></a>Arendatav sait

Kui saiti arendatakse, peaks kõigil saidi lehekülgedel olema metasildid **NOINDEX** ja **NOFOLLOW**, nii et otsingumootorid ei indekseeriks lehti ja kaupluse arenduse versioone oma saidi vahemälu. Selle konfiguratsiooni tegemiseks peate lisama vaikimisi metasildid mooduli lehe mallile. Vaikimisi metasiltide atribuudid on siis saadaval SEO atribuutide jaotises lehe redaktoris. Neid atribuute saate kasutada metasiltide haldamiseks.

## <a name="soft-launch-of-a-site"></a>Saidi esialgne käivitamine

"Esialgse käivitamise" ajal tehakse veebisait kättesaadavaks piiratud publikule või turule enne täieliku käivitamise toimumist. Kui teete oma veebisaidile esialgse käivitamise, peaksite metasildid **NOINDEX** jätma oma kohale. Sel viisil aitate tagada, et esialgne käivitamine piirduks piiratud publikuga, kelleni soovite jõuda.

## <a name="a-site-that-is-in-production"></a>Sait, mis on tootmises

Kui sait on tootmisse kaasatud, veenduge, et kõik saidi lehed on õigesti märgistatud. Microsoft Dynamics 365 Commerce kasutab lehe jaoks sisestatud teavet, et renderdada kõik SEO andmed sellel lehel. Järgmised moodulid pakuvad seda funktsiooni: kategooria lehekülje kokkuvõte, loendi lehekülje kokkuvõte ja toote lehekülje kokkuvõte.

Otsingumootori indekseerimise optimeerimiseks kasutab renderdamise raamistik mõlemat teavet SEO atribuutidest, mis on konfigureeritud rakenduses Dynamics 365 Commerce ja konkreetse mooduli teabes. Tootmiseks kasutatava saidi puhul peaksite veenduma, et fail robots.txt võimaldab kogu saidi indekseerimist ja see sisaldab linke teie avaldatud saidi vastenduse dokumendile. Peaksite lülitama saidi kaardi loomise funktsioonid **Saidi sätted \> Saidi kaart on lubatud**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Lehekülje SEO sätted sisemise eelvaate, piiratud sihtrühmade ja kogu publiku jaoks

Kuna rakendus Dynamics 365 Commerce toetab „mida sa näed on see, mida sa saad” (WYSIWYG) autenditud eelvaateid visuaalses leheehitajas, saavad autorid ette valmistada oma lehe sisu, ilma et peaks muretsema, et teave muutub saidi külastajatele nähtavaks. Kui leht tuleb avaldada, kuid selle säritus peab olema piiratud, peaks sellel olema metasilt **NOINDEX**, nii et otsingumootorid seda ei indekseeriks. Seejärel, kui leht on kõigi sihtrühmade jaoks valmis, tuleb esitada kõik põhilised SEO metaandmed, et maksimeerida otsingumootori indekseerimise efektiivsust. Lisaks tuleks eemaldada metasilt **NOLIMIT**.

## <a name="additional-resources"></a>Lisaressursid

[E-kaubanduse kasutajate ja rollide haldamine](manage-ecommerce-users-roles.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)

[Sisu turbepoliitika (CSP) haldamine](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]