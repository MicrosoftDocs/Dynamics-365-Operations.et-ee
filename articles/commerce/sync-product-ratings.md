---
title: Toote hinnangute sünkroonimine Dynamics 365 Retailis
description: Selles teemas kirjeldatakse, kuidas sünkroonida tootehinnanguid rakenduses Microsoft Dynamics 365 Retail.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698161"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a>Toote hinnangute sünkroonimine Dynamics 365 Retailis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas sünkroonida tootehinnanguid rakenduses Microsoft Dynamics 365 Retail.

## <a name="overview"></a>Ülevaade

Tootehinnangute kasutamiseks omnikanalis, nt kassas (POS) ja kõnekeskustes, tuleb tootehinnangud hinnangute ja arvustuste teenusest importida jaemüügikanali andmebaasi. Kui tootehinnangud omnikanalites saadavaks tehakse, aitavad need kliente kaudselt suhtluses müüjatega.

Selles teemas kirjeldatakse järgmisi toiminguid.

1. Jaemüügi pakett-töö konfigureerimine tootehinnangute importimiseks.
1. Kontrollimine, kas tootehinnangute sünkroonimise pakett-töö õnnestus.
1. Tootehinnangute muutmine kassas kättesaadavaks.

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a>Retaili pakett-töö konfigureerimine tootehinnangute importimiseks

> [!IMPORTANT]
> Enne alustamist veenduge, et installitud oleks Retaili versioon 10.0.6 või uuem.

### <a name="initialize-the-retail-scheduler"></a>Kaupluse andmeedastaja lähtestamine

Kaupluse andmeedastaja lähtestamiseks toimige järgmiselt.

1. Valige suvandid **Retail \> Kaupluse haldus \> Kaupluse andmeedastaja \> Kaupluse andmeedastaja lähtestamine**. Võite ka sisestada otsingu „Kaupluse andmeedastaja”.
1. Dialoogiboksis **Kaupluse andmeedastaja** veenduge, et suvand **Kustuta olemasolev konfiguratsioon** oleks määratud valikule **Ei** ja seejärel valige nupp **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>Alamtöö RetailProductRating kontrollimine

Selleks et kontrollida, kas alamtöö **RetailProductRating** on olemas, tehke järgmist.

1. Valige suvandid **Retail \> Kaupluse haldus \> Kaupluse andmeedastaja \> Andmeedastaja alamtööd**. Võite ka sisestada otsingu „Andmeedastaja alamtööd”.
1. Alamtööde loendist otsige alamtööd **RetailProductRating**.

Järgmisel joonisel on näha alamtöö üksikasjade näide Retailis.

![Alamtöö RetailProductRating üksikasjad](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Kui te ei leia alamtööd **RetailProductRating**, on võimalik, et olete enne kaupluse andmeedastaja lähtestamist juba käitanud töö **Tootehinnangute sünkroonimine** ja töö **1040 CDX**. Sellisel juhul tehke töö **Andmete täielik sünkroonimine** käitamiseks järgmist.
>
> 1. Valige suvandid **Retail \> Kaupluse haldus \> Kaupluse andmeedastaja \> Kanali andmebaas**. Võite ka sisestada otsingu „Kanali andmebaas”.
> 1. Valige sünkroonimiseks kanali andmebaas.
> 1. Valige tegumiribal suvand **Andmete täielik sünkroonimine**.
> 1. Valige rippmenüü dialoogiboksis **Jaotusgraafiku valimine** suvand **1040 – tooted** ja seejärel valige nupp **OK**.
> 1. Korrake eelmise protseduuri etappe, et kontrollida, kas alamtöö **RetailProductRating** on loodud.

### <a name="import-product-ratings"></a>Tootehinnangute importimine

Tootehinnangute importimiseks Retaili hinnangute ja arvustuste teenusest tehke järgmist.

1. Valige suvandid **Retail \> Kaupluse haldus \> Kaupluse andmeedastaja \> Tootehinnangute töö sünkroonimine**. Võite ka sisestada otsingu „Tootehinnangute töö sünkroonimine”.
1. Dialoogiboksist **Tootehinnangute tõmbamine** kiirkaardil **Käivita taustal** valige suvand **Kordumine**.
1. Seadistage dialoogiboksis **Kordumise määratlemine** kordumismuster. (Soovitatud väärtus on kaks tundi.) Ärge määrake kordumist, mis on vähem kui kaks tundi.
1. Valige nupp **OK**.
1. Määrake suvandi **Pakktöötlus** väärtuseks **Jah**. See seadistus aitab tagada, et saate logisid auditeerida ja kontrollida pakett-töö käituste olekut.
1. Pakett-töö plaanimiseks valige nupp **OK**.

Järgmisel joonisel on näha pakett-töö konfiguratsiooni näide Retailis.

![Tootehinnangute pakett-töö sünkroonimise konfiguratsioon](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Kontrollimine, kas tootehinnangute sünkroonimise pakett-töö õnnestus

Selleks et kontrollida, kas pakett-töö **Tootehinnangute sünkroonimine** õnnestus, tehke järgmist.

1. Valige suvandid **Retail \> Süsteemiadministraator \> Päringud \> Pakett-tööd**, või kui kasutate ainult Retaili jaoks mõeldud varude arvestusühikut (SKU) valige suvandid **Retail \> Päringud ja aruanded \> Pakett-tööd**. Võite sisestada otsingu „Pakett-tööd”.
1. Pakett-töö üksikasjade vaatamiseks otsige pakett-töö loendist veerust **Töö kirjeldus** kirjeldust, mis sisaldab fraasi „Tootehinnangute tõmbamine”.
1. Valige töö ID, et vaadata pakett-töö üksikasju, nagu plaanitud alguskuupäev/-kellaaeg ja kordumise tekst.

Järgmisel joonisel on näha näide pakett-töö üksikasjadest Retailis, kui pakett-töö on plaanitud käivituma kahetunnise intervalliga.

![Tootehinnangute pakett-töö sünkroonimise üksikasjad](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Tootehinnangute muutmine kassas kättesaadavaks

Hinnangute ja arvustuste lahendus rakenduses Dynamics 365 Commerce on omnikanali lahendus. Kuid vaikimisi tootehinnanguid kassas ei kuvata. Selleks et kliendid poodides näeksid hinnanguid ja arvustusi, kui müüjad neid aitavad, peate tootehinnangud kassas sisse lülitama.

Tootehinnangute kassas sisselülitamiseks tehke järgmist.

1. Valige suvandid **Retail \> Retaili seadistamine \> Parameetrid \> Retaili parameetrid**. Võite ka sisestada otsingu „Retaili parameetrid”.
1. Valige vahekaardilt **Konfiguratsiooni parameetrid** suvand **Uus**.
1. Sisestage nimi, nt **RatingsAndReviews.EnableProductRatingsForRetailStores**, ja määrake väärtuseks **tõene**.
1. Valige käsk **Salvesta**.
1. Avage **Jaemüük \> Jaemüügi IT \> Jaotusgraafik**. Võite ka sisestada otsingu „Jaotusgraafik”.
1. Valige tööde loendist suvand **1110** (**Globaalne konfiguratsioon**) ja seejärel valige käsk **Käivita kohe**.
1. Kui töö on edukalt käivitatud, kontrollige, kas tootehinnangud kuvatakse nüüd kassas.

Järgmisel on joonisel on näha näide Retaili parameetrite konfiguratsioonist tootehinnangute sisselülitamiseks kassas.

![Retaili parameetrite konfiguratsioon tootehinnangute jaoks kassas](media/rnr-hq-enable-ratings-in-pos.png)

Järgmisel joonisel on näha näide tootehinnangutest kassas.

![Tootehinnangud kassas](media/rnr-pos-catalog-ratings.png)

Järgmisel joonisel on näha näide tootehinnangutest kõnekeskuse kanalites.

![Tootehinnangud kõnekeskuse kanalis](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)
