---
title: Hinnangute ja arvustuste konfigureerimine
description: Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3f9ff4b0654ec5fa7548ac62e16ae64f44383e7
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968098"
---
# <a name="configure-ratings-and-reviews"></a>Hinnangute ja arvustuste konfigureerimine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.

Hinnangud ja arvustused e-Commerce’i veebisaitidel aitavad klientidel saada toote kohta teavet enne ostuotsuse tegemist, näidates neile, mida teised kliendid nendest toodetest arvavad. E-kaubanduse veebisaitide jaoks on hinnangud ja arvustused lisaks viis klientidelt toodete kohta tagasiside kogumiseks. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks

Hinnangute ja arvustuste konfiguratsiooni väärtused (nt rentniku ID, arvustuse teksti pikkus ja arvustuse pealkirja pikkus) konfigureeritakse saidi tasemel. 

Saidi konfigureerimiseks hinnangute ja arvustuste kuvamiseks toimige järgmiselt. 

1. Avage suvand **Koduleht \> Saidid**.
1. Valige oma saidi nimi. 
1. Avage **Saidi sätted \> Laiendused**. 
1. Sisestage väljale **Arvustuse teksti max pikkus** arvustuse tekstis sisalduvate tärkide maksimaalne arv (nt **1000**). 
1. Sisestage väljale **Arvustuse pealkirja max pikkus** arvustuse pealkirjas sisalduvate tärkide maksimaalne arv (nt **55**). 
1. Valige suvand **Salvesta ja avalda**. 

Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.

![Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Toote hinnangu linkimine PDP arvustuste jaotisega

Toote hinnang kuvatakse PDP ülaosas toote pealkirja all. Toote hinnangut saab konfigureerida nii, et see on lingitud sama PDP jaotisega **Arvustused**. 

Toote hinnangu linkimiseks PDP jaotisega **Arvustused** tehke järgmist.

1. Avage PDP mall. 
1. Avage suvand **Ostukasti konteinermooduli sätted**.
1. Suvandis **Ostukast** valige **Toote hinnangud** ja seejärel valige märkeruut **Link täisarvustuste mooduli klõpsamisele**.

Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.

![Toote hinnangu linkimine PDP arvustuste jaotisega.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Privaatsuse ja poliitika lehe lingi konfigureerimine

Privaatsuse ja poliitika lehe lingi kommenteerimiseks järgige neid samme.

1. Avage suvand **Koduleht \> Saidid**.
1. Valige oma saidi nimi. 
1. Avage **Saidi sätted \> Laiendused**.
1. Vahekaardil **Marsruudid** suvandis **RNR-i privaatsus ja poliitika** valige suvand **Lisa link** Kui link on juba sisestatud ja soovite selle asendada, valige link. 
1. Dialoogiaknas **Lisa link** valige privaatsuse ja poliitika lehe link ning valige seejärel **OK.** 
1. Valige suvand **Salvesta ja avalda**. 

Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.

![Privaatsuse ja poliitika lehe lingi konfigureerimine.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Hinnangute ja arvustuste moodulite konfigureerimine toote üksikasjade lehtedel

Lisateavet toote üksikasjade lehtedel hinnangute ja arvustuste moodulite konfigureerimise kohta vt [Hinnangute ja arvustuste moodulid](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail](sync-product-ratings.md)

[Lubage hinnangute ja ülevaadete käsitsi avaldamine moderaatori poolt](manual-publish-rating-reviews.md)

[Hinnangute ja kommentaaride importimine ja eksportimine](import-export-reviews.md)

[Teenusepõhise autentimise konfigureerimine](service-to-service-auth.md)

[Hinnangud ja arvustused KKK](ratings-reviews-faq.md)

[Hinnangute ja arvustuste moodulid](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
