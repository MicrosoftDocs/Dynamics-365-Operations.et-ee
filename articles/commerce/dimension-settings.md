---
title: Tootedimensioonidele kuvasätete rakendamine
description: See teema hõlmab tootedimensioonide kuvasätteid ja kirjeldab, kuidas neid rakendada rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117219"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Tootedimensioonidele kuvasätete rakendamine

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema hõlmab tootedimensioonide kuvasätteid ja kirjeldab, kuidas neid rakendada rakenduses Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce toetab suurust, stiili ja värvimõõtmeid tootevariantide eristamiseks. Mõõtmed kuvatakse tavaliselt tekstiväärtustena, näiteks "Väike", "Keskmine" ja "Suur" suuruste puhul ning "Must" ja "Pruun" värvide puhul. Kui aga toode toetab paljusid variatsioone, võib tootevariantide sirvimine olla keeruline, sest iga variandi pildi vaatamiseks on vaja mitut valikut. Tootevariantide sirvimise lihtsustamiseks saab Commerce'i versioonis 10.0.20 kasutada pilte ja kuueteistkümnendkoode dimensioonide kuvamiseks näidistena.

Commerce site ehitajas määratletakse varude sätted saidiehitaja jaotises **Saidi sätted \> Laiendused \> Varude haldus**. Järgmisel joonisel on toodud saidikoosturi dimensioonisätete näide.

![Ärisaidi koostaja saidisätete näide](./dev-itpro/media/swatch_site_settings.PNG)

Saadaval on kaks dimensioonisätet:

- **Pildina kuvatavad dimensioonid** – määrake, millised dimensioonid peaksid e-kaubanduse saidi lehtedel nagu näiteks toote üksikasjade lehtedel (PDPd) ja otsingutulemite loendi lehtedel olema kuvatud. Mis tahes värvi-, suuruse- ja stiilimõõtmete kombinatsiooni saab kuvada näitena. Kui dimensioon on valitud kuvamiseks kui näide, otsib Commerce module renderdamine hex-koodi saada olevat konfiguratsiooni. Kui hex-koodi pole konfigureeritud, otsib süsteemiloogika pildi URL-i näidise konfiguratsiooni. Kui pole konfigureeritud ei hex-koodi ega pildi URL-i, kuvatakse tekst.

    Järgmisel joonisel on kujutatud näide, kus e-kaubanduse saidi PDP sisaldab värvi- ja suuruse näiteid. Selles näites on värvidimensiooni jaoks konfigureeritud heksi kood. Seetõttu kuvatakse näited värvidena. Kuid ei hex-kood ega pildi URL pole suuruse dimensiooni jaoks konfigureeritud. Seetõttu kuvatakse teksti.

    ![Näide e-kaubanduse toote üksikasjade lehel näietena kuvatud värvidimensioonist](./dev-itpro/media/swatch_pdp.png)

- **Tootekaardil kuvatavad dimensioonid** – määrake, millised dimensioonid tuleks kuvada loendites ja loendilehtedel kuvatavatel tootekaartidel. Enne dimensiooni kuvamist tootekaardil peab see säte olema selle dimensiooni puhul lubatud. Lubatud peaksid olem ka **Pildisättena kuvatavad dimensioonid**. Tootekaartide näidise valiku käitumine on optimeeritud värvidimensiooni jaoks. Muude dimensioonide puhul võib näidise valiku käitumise kohandamiseks olla vaja vaatelaiendit.

    Järgmisel joonisel on kujutatud näide, kus e-kaubanduse saidi loendileht sisaldab värvinäidistega tootekaarte.

    ![Näide e-kaubanduse toote üksikasjade lehel näidetena kuvatud värvidimensioonist](./dev-itpro/media/swatch_searchresults.PNG)

Lisateavet selle kohta, kuidas konfigureerida tootedimensioone nii, et neid kuvataks saidilehtedel kelladena, leiate teemast [Tootedimensiooniväärtuste konfigureerimine näidistena kuvamiseks](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Otsingutulemuste moodul](search-result-module.md)

[Ostukastimoodul](add-buy-box.md)

[Tootedimensiooni väärtuste konfigureerimine näidistena kuvamiseks](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
