---
title: Hinnangute ja arvustuste moodulid
description: See artikkel katab hinnangud ja ülevaated moodulitest, mida kasutatakse toote üksikasjade lehtedel Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ede42caac78dc48fa6315a2d3c22f1e0f12f0810
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283583"
---
# <a name="ratings-and-reviews-modules"></a>Hinnangute ja arvustuste moodulid

[!include [banner](includes/banner.md)]

See artikkel hõlmab hinnanguid ja ülevaateid moodulitest, mida kasutatakse toote üksikasjade lehtedel (PDP-d) moodulites Microsoft Dynamics 365 Commerce.

Hinnangud ja arvustused e-Commerce’i veebisaitidel aitavad klientidel saada toote kohta teavet enne ostuotsuse tegemist ja on lisaks mehhanism toodete kohta kliendi tagasiside kogumiseks. 

Hinnangud kuvatakse tooteloendi lehtedel, kategoorialoendi lehtedel, otsingutulemuste lehtedel ja teistel saidi lehtedel. 

Hinnangute histogrammid ja toodete ülevaated kuvatakse PDP-del. Nupu **Kirjuta arvustus** võimaldab klientidel edastada toote kohta hinnanguid ja arvustusi. Neid PDP-funktsioone kontrollivad hinnangute ja ülevaadete moodulid.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Hinnangute ja arvustuste moodulid PDP-des 

PDP-des näitavad hinnangute ja arvustuste kokkuvõtteid kolm moodulit.
- Arvustuse kirjutamise moodul
- Toote arvustuste loendi moodul
- Hinnangute histogrammi moodul
 
Järgmisel joonisel on näha, kuidas hinnangute ja arvustuste moodulid PDP-s välja näevad.

![Hinnangute ja arvustuste moodulid PDP-s.](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Teavet PDP-de mallide ja paigutuste optimeerimise kohta, et saaksite hinnangute ja arvustute moodulite konfiguratsioone jagada e-kaubanduse saidi mitme PDP vahel, vaadake teemat [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).

Järgmisel joonisel on näha, kuidas dialoogiaken **Lisa moodul** esitab rakenduses Dynamics 365 Commerce hinnangute ja arvustuste mooduleid.
![Mooduli dialoogiakna lisamine.](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Arvustuse kirjutamise moodul

Arvustuse kirjutamise moodul hõlmab nuppu **Kirjuta arvustus**, mis võimaldab kasutajatel sisse logida, määrata hinnang ja kirjutada toote kohta arvustus. See moodul võimaldab lisaks kasutajatel eelnevalt edastatud hinnangut või arvustust redigeerida. See moodul kuvatakse tavaliselt PDP-s hinnangute histogrammi ja toote arvustuste loendi moodulite kohal.
Järgmisel joonisel on kujutatud dialoogiaken **Kirjuta arvustus**, mis kuvatakse siis, kui klient valib suvandi **Kirjuta arvustus**. Klient saab seda dialoogiakent kasutada hinnangu ja arvustuse edastamiseks.

![Arvustuse kirjutamise dialoogiaken.](media/rnr-eCommerce-write-review-module.png)

Järgmises tabelis on näidatud arvustuse kirjutamise mooduli atribuut, mis tuleb autorluse tööriistas konfigureerida.

| Atribuudi nimi | Väärtus        | Atribuudi kirjeldus                 |
|---------------|--------------|--------------------------------------|
| Nimi          | Arvustuse kirjutamine | Arvustuse kirjutamise mooduli nimi. |

### <a name="ratings-histogram-module"></a>Hinnangute histogrammi moodul

Hinnangute histogrammi moodul näitab hinnangute histogrammi. See moodul kuvatakse tavaliselt PDP-s arvustuse kirjutamise mooduli ja toote arvustuste loendi mooduli vahel.
Hinnangute histogrammi moodul ei nõua konfiguratsiooni. Peate lihtsalt lisama mooduli PDP mallis. Järgmised joonised näitavad, kuidas PDP mall rakenduses Dynamics 365 Commerce välja näeb, kui hinnangute ja arvustuse moodulid on PDP-des kuvamiseks konfigureeritud.
![PDP mall, kui hinnangud ja arvustused on PDP-des kuvamiseks konfigureeritud.](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Toote arvustuste loendi moodul

Toote arvustuste loendi moodul kuvab toodete arvustuste loendi koos sortimise, filtreerimise ja lehejaotuse valikutega. See moodul kuvatakse PDP-s tavaliselt pärast hinnangute histogrammi moodulit
Järgmises tabelis on näidatud toote arvustuste loendi mooduli atribuudid, mis tuleb autorluse tööriistas konfigureerida.

| Atribuudi nimi              | Väärtus | Atribuudi kirjeldus |
|----------------------------|-------| ---------------------|
| Igal lehel kuvatavad arvustused | 10    | Arvustuste arv, mida tuleks korraga PDP-s kuvada. Nupud **Järgmine** ja **Eelmine** on kaasatud, nii et kasutajad saavad läbi arvustuste lehtede liikuda. |

#### <a name="ratings-histogram--summary-view"></a>Hinnangute histogramm – kokkuvõtte vaade

Toote arvustuste loendi moodul sisaldab pesa, kus saate lisada hinnangute histogrammi mooduli. Järgmisel joonisel on näidatud, kuidas saate lisada rakenduses Dynamics 365 Commerce hinnangute histogrammi mooduli toote arvustuste loendi moodulile.

![Hinnangute histogrammi mooduli lisamine toote arvustuste loendi moodulis.](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukorvimoodul](add-cart-module.md)

[Maksmismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
