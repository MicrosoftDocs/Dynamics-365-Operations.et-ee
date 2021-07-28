---
title: Toote hinnangute sünkroonimine Dynamics 365 Commerceis
description: Selles teemas kirjeldatakse, kuidas sünkroonida tootehinnanguid rakenduses Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6f23b4c15937a0e61eb64b25eadef58c1fda231e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354609"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Toote hinnangute sünkroonimine Dynamics 365 Commerceis

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas sünkroonida tootehinnanguid rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Tootehinnangute kasutamiseks omnikanalis, nt kassas (POS) ja kõnekeskustes, tuleb tootehinnangud hinnangute ja arvustuste teenusest importida Commerce’i kanali andmebaasi. Kui tootehinnangud omnikanalites saadavaks tehakse, aitavad need kliente kaudselt suhtluses müüjatega.

Selles teemas kirjeldatakse järgmisi toiminguid.

1. Konfigureerige suvand **Tootehinnangute sünkroonimise töö** pakett-tööna, et sünkroonida tootehinnangud suvandist **Hinnangute ja arvustuste teenus**.
1. Kontrollimine, kas tootehinnangute sünkroonimise pakett-töö õnnestus.
1. Tootehinnangute muutmine kassas kättesaadavaks.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Pakett-töö konfigureerimine tootehinnangute sünkroonimiseks

> [!IMPORTANT]
> Enne alustamist veenduge, et installitud oleks rakenduse Dynamics 365 Commerce versioon 10.0.6 või uuem.

### <a name="initialize-the-commerce-scheduler"></a>Kaubanduse ajasti lähtestamine

Kaubanduse ajasti lähtestamiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Kaubanduse ajasti \> Kaubanduse ajasti lähtestamine**. Võite ka sisestada otsingu „Kaubanduse ajasti lähtestamine”.
1. Dialoogiboksis **Kaubanduse ajasti lähtestamine** veenduge, et suvand **Kustuta olemasolev konfiguratsioon** oleks määratud valikule **Ei** ja seejärel valige nupp **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>Alamtöö RetailProductRating kontrollimine

Selleks et kontrollida, kas alamtöö **RetailProductRating** on olemas, tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Kaubanduse ajasti \> Ajasti alamtööd**. Võite ka sisestada otsingu „Andmeedastaja alamtööd”.
1. Alamtööde loendist otsige alamtööd **RetailProductRating**.

Järgmisel joonisel on näha alamtöö üksikasjade näide rakenduses Commerce.

![Alamtöö RetailProductRating üksikasjad.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Kui te ei leia alamtööd **RetailProductRating**, on võimalik, et olete enne kaubanduse ajasi lähtestamist juba käitanud töö **Tootehinnangute sünkroonimine** ja töö **1040 CDX**. Sellisel juhul tehke töö **Andmete täielik sünkroonimine** käitamiseks järgmist.

> 1. Avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Kaubanduse ajasti \> Kanali andmebaas**. Võite ka sisestada otsingu „Kanali andmebaas”.
> 1. Valige sünkroonimiseks kanali andmebaas.
> 1. Valige tegumiribal suvand **Andmete täielik sünkroonimine**.
> 1. Valige rippmenüü dialoogiboksis **Jaotusgraafiku valimine** suvand **1040 – tooted** ja seejärel valige nupp **OK**.
> 1. Korrake eelmise protseduuri etappe, et kontrollida, kas alamtöö **RetailProductRating** on loodud.

### <a name="import-product-ratings"></a>Tootehinnangute importimine

Tootehinnangute importimiseks Commerce’i hinnangute ja arvustuste teenusest tehke järgmist.

1. Valige suvandid **Jaemüük ja kaubandus \> Kaupluse haldus \> Kaubanduse ajasti \> Tootehinnangute töö sünkroonimine**. Võite ka sisestada otsingu „Tootehinnangute töö sünkroonimine”.
1. Dialoogiboksist **Tootehinnangute tõmbamine** kiirkaardil **Käivita taustal** valige suvand **Kordumine**.
1. Seadistage dialoogiboksis **Kordumise määratlemine** kordumismuster. (Soovitatud väärtus on kaks tundi.) Ärge määrake kordumist, mis on vähem kui kaks tundi.
1. Valige nupp **OK**.
1. Määrake suvandi **Pakktöötlus** väärtuseks **Jah**. See seadistus aitab tagada, et saate logisid auditeerida ja kontrollida pakett-töö käituste olekut.
1. Pakett-töö plaanimiseks valige nupp **OK**.

Järgmisel joonisel on näha pakett-töö konfiguratsiooni näide Commerce’is.

![Tootehinnangute pakett-töö sünkroonimise konfiguratsioon.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Kontrollimine, kas tootehinnangute sünkroonimise pakett-töö õnnestus

Selleks et kontrollida, kas pakett-töö **Tootehinnangute sünkroonimine** õnnestus, tehke järgmist.

1. Valige suvandid **Jaemüük ja kaubandus \> Süsteemiadministraator \> Päringud \> Pakett-tööd**, või kui kasutate ainult Commerce’i jaoks mõeldud varude arvestusühikut (SKU) valige suvandid **Jaemüük ja kaubandus \> Päringud ja aruanded \> Pakett-tööd**. Võite sisestada otsingu „Pakett-tööd”.
1. Pakett-töö üksikasjade vaatamiseks otsige pakett-töö loendist veerust **Töö kirjeldus** kirjeldust, mis sisaldab fraasi „Tootehinnangute tõmbamine”.
1. Valige töö ID, et vaadata pakett-töö üksikasju, nagu plaanitud alguskuupäev/-kellaaeg ja kordumise tekst.

Järgmisel joonisel on näha näide pakett-töö üksikasjadest Commerce’is, kui pakett-töö on plaanitud käivituma kahetunnise intervalliga.

![Tootehinnangute pakett-töö sünkroonimise üksikasjad.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Tootehinnangute muutmine kassas kättesaadavaks

Hinnangute ja arvustuste lahendus rakenduses Dynamics 365 Commerce on omnikanali lahendus. Kuid vaikimisi tootehinnanguid kassas ei kuvata. Selleks et kliendid poodides näeksid hinnanguid ja arvustusi, kui müüjad neid aitavad, peate tootehinnangud kassas sisse lülitama.

Tootehinnangute kassas sisselülitamiseks tehke järgmist.

1. Minge jaotisse **Jaemüük ja kaubandus \> Kaubanduse seadistamine \> Parameetrid \> Kaubanduse parameetrid**. Võite ka sisestada otsingu „Kaubanduse parameetrid”.
1. Valige vahekaardilt **Konfiguratsiooni parameetrid** suvand **Uus**.
1. Sisestage nimi, nt **RatingsAndReviews.EnableProductRatingsForRetailStores**, ja määrake väärtuseks **tõene**.
1. Valige käsk **Salvesta**.
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**. Võite ka sisestada otsingu „Jaotusgraafik”.
1. Valige tööde loendist suvand **1110** (**Globaalne konfiguratsioon**) ja seejärel valige käsk **Käivita kohe**.
1. Kui töö on edukalt käivitatud, kontrollige, kas tootehinnangud kuvatakse nüüd kassas.

Järgmisel on joonisel on näha näide Kaubanduse parameetrite konfiguratsioonist tootehinnangute sisselülitamiseks kassas.

![Commerce parameetrite konfiguratsioon tootehinnangute jaoks kassas.](media/rnr-hq-enable-ratings-in-pos.png)

Järgmisel joonisel on näha näide tootehinnangutest kassas.

![Tootehinnangud kassas.](media/rnr-pos-catalog-ratings.png)

Järgmisel joonisel on näha näide tootehinnangutest kõnekeskuse kanalites.

![Tootehinnangud kõnekeskuse kanalis.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]