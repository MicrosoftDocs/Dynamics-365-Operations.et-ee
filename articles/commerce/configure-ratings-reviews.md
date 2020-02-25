---
title: Hinnangute ja arvustuste konfigureerimine
description: Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002193"
---
# <a name="configure-ratings-and-reviews"></a>Hinnangute ja arvustuste konfigureerimine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.

## <a name="overview"></a>Ülevaade

Hinnangud ja ülevaated e-kaubanduse veebisaidil aitavad klientidel saada toote kohta teavet enne ostuotsuse tegemist, näidates neile, mida teised kliendid nendest toodetest arvavad. E-kaubanduse veebisaitide jaoks on hinnangud ja arvustused lisaks viis klientidelt toodete kohta tagasiside kogumiseks. 

Hinnangud kuvatakse tooteloendi lehtedel, kategoorialoendi lehtedel, otsingutulemuste lehtedel ja teistel saidi lehtedel. Hinnangute histogrammid ja toodete ülevaated kuvatakse toote üksikasjade lehtedel (PDP-d). Nupu **Kirjuta arvustus** võimaldab klientidel edastada toote kohta hinnanguid ja arvustusi.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Hinnangute ja arvustuste moodulid PDP-des 

PDP-des näitavad hinnangute ja arvustuste kokkuvõtteid kolm moodulit.

- Arvustuse kirjutamise moodul
- Toote arvustuste loendi moodul
- Hinnangute histogrammi moodul
 
Järgmisel joonisel on näha, kuidas hinnangute ja arvustuste moodulid PDP-s välja näevad.

![Hinnangute ja arvustuste moodulid PDP-s](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Teavet PDP-de mallide ja paigutuste optimeerimise kohta, et saaksite hinnangute ja arvustute moodulite konfiguratsioone jagada e-kaubanduse saidi mitme PDP vahel, vaadake teemat [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).

Järgmisel joonisel on näha, kuidas dialoogiaken **Lisa moodul** esitab rakenduses Dynamics 365 Commerce hinnangute ja arvustuste mooduleid.

![Mooduli dialoogiakna lisamine](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Arvustuse kirjutamise moodul

Arvustuse kirjutamise moodul hõlmab nuppu **Kirjuta arvustus**, mis võimaldab kasutajatel sisse logida, määrata hinnang ja kirjutada toote kohta arvustus. See moodul võimaldab lisaks kasutajatel eelnevalt edastatud hinnangut või arvustust redigeerida. See moodul kuvatakse tavaliselt PDP-s hinnangute histogrammi ja toote arvustuste loendi moodulite kohal.

Järgmisel joonisel on kujutatud dialoogiaken **Kirjuta arvustus**, mis kuvatakse siis, kui klient valib suvandi **Kirjuta arvustus**. Klient saab seda dialoogiakent kasutada hinnangu ja arvustuse edastamiseks.

![Arvustuse kirjutamise dialoogiaken](media/rnr-eCommerce-write-review-module.png)

Järgmises tabelis on näidatud arvustuse kirjutamise mooduli atribuut, mis tuleb autorluse tööriistas konfigureerida.

| Atribuudi nimi | Väärtus        | Atribuudi kirjeldus                 |
|---------------|--------------|--------------------------------------|
| Nimi          | Arvustuse kirjutamine | Arvustuse kirjutamise mooduli nimi. |

### <a name="ratings-histogram-module"></a>Hinnangute histogrammi moodul

Hinnangute histogrammi moodul näitab hinnangute histogrammi. See moodul kuvatakse tavaliselt PDP-s arvustuse kirjutamise mooduli ja toote arvustuste loendi mooduli vahel.

Hinnangute histogrammi moodul ei nõua konfiguratsiooni. Peate lihtsalt lisama mooduli PDP mallis. 

Järgmised joonised näitavad, kuidas PDP mall rakenduses Dynamics 365 Commerce välja näeb, kui hinnangute ja arvustuse moodulid on PDP-des kuvamiseks konfigureeritud.

![PDP mall, kui hinnangud ja arvustused on PDP-des kuvamiseks konfigureeritud](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Toote arvustuste loendi moodul

Toote arvustuste loendi moodul kuvab toodete arvustuste loendi koos sortimise, filtreerimise ja lehejaotuse valikutega. See moodul kuvatakse PDP-s tavaliselt pärast hinnangute histogrammi moodulit

Järgmises tabelis on näidatud toote arvustuste loendi mooduli atribuudid, mis tuleb autorluse tööriistas konfigureerida.

| Atribuudi nimi              | Väärtus | Atribuudi kirjeldus |
|----------------------------|-------| ---------------------|
| Igal lehel kuvatavad arvustused | 10    | Arvustuste arv, mida tuleks korraga PDP-s kuvada. Nupud **Järgmine** ja **Eelmine** on kaasatud, nii et kasutajad saavad läbi arvustuste lehtede liikuda. |

#### <a name="ratings-histogram--summary-view"></a>Hinnangute histogramm – kokkuvõtte vaade

Toote arvustuste loendi moodul sisaldab pesa, kus saate lisada hinnangute histogrammi mooduli. Järgmisel joonisel on näidatud, kuidas saate lisada rakenduses Dynamics 365 Commerce hinnangute histogrammi mooduli toote arvustuste loendi moodulile.

![Hinnangute histogrammi mooduli lisamine toote arvustuste loendi moodulis](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks

Hinnangute ja arvustuste konfiguratsiooni väärtused (nt rentniku ID, arvustuse teksti pikkus ja arvustuse pealkirja pikkus) konfigureeritakse saidi tasemel. 

Saidi konfigureerimiseks hinnangute ja arvustuste kuvamiseks toimige järgmiselt. 

1. Avage suvand **Koduleht \> Saidid**.
1. Valige oma saidi nimi. 
1. Avage suvand **Saidi haldus \> Laiendatavus**. 
1. Sisestage väljale **Arvustuse teksti max pikkus** arvustuse tekstis sisalduvate tärkide maksimaalne arv (nt **1000**). 
1. Sisestage väljale **Arvustuse pealkirja max pikkus** arvustuse pealkirjas sisalduvate tärkide maksimaalne arv (nt **55**). 
1. Valige suvand **Salvesta ja avalda**. 

Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.

![Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Toote hinnangu linkimine PDP arvustuste jaotisega

Toote hinnang kuvatakse PDP ülaosas toote pealkirja all. Toote hinnangut saab konfigureerida nii, et see on lingitud sama PDP jaotisega **Arvustused**. 

Toote hinnangu linkimiseks PDP jaotisega **Arvustused** tehke järgmist.

1. Avage PDP mall. 
1. Avage suvand **Ostukasti konteinermooduli sätted**.
1. Suvandis **Ostukast** valige **Toote hinnangud** ja seejärel valige märkeruut **Link täisarvustuste mooduli klõpsamisele**.

Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.

![Toote hinnangu linkimine PDP arvustuste jaotisega](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Privaatsuse ja poliitika lehe lingi konfigureerimine

Privaatsuse ja poliitika lehe lingi kommenteerimiseks järgige neid samme.

1. Avage suvand **Koduleht \> Saidid**.
1. Valige oma saidi nimi. 
1. Avage suvand **Saidi haldus \> Laiendatavus**
1. Vahekaardil **Marsruudid** suvandis **RNR-i privaatsus ja poliitika** valige suvand **Lisa link** Kui link on juba sisestatud ja soovite selle asendada, valige link. 
1. Dialoogiaknas **Lisa link** valige privaatsuse ja poliitika lehe link ning valige seejärel **OK.** 
1. Valige suvand **Salvesta ja avalda**. 

Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.

![Privaatsuse ja poliitika lehe lingi konfigureerimine](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail](sync-product-ratings.md)
