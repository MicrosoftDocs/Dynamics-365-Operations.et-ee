---
title: Moderaatori hinnangute ja ülevaadete käsitsi avaldamise lubamine
description: See teema kirjeldab, kuidas lubada moderaatori hinnangute ja ülevaadete käsitsi avaldamist rakenduses Microsoft Dynamics 365 Commerce ning kuidas käsitsi hinnanguid ja ülevaateid avaldada.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 443ebaa13d7ac29df66ffe77a2ed938e44a0c488
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968199"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Moderaatori hinnangute ja ülevaadete käsitsi avaldamise lubamine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lubada moderaatori hinnangute ja ülevaadete käsitsi avaldamist rakenduses Microsoft Dynamics 365 Commerce ning kuidas käsitsi hinnanguid ja ülevaateid avaldada.

Dynamics 365 Commerce hinnangute ja läbivaatuse lahendus kasutab teenust Azure Cognitive Services, et automaatselt deaktiveerida profiili ülevaatuse pealkirjad ja sisu ning avaldada hinnangud ja ülevaated. Seetõttu ei ole käsitsi sekkumine vajalik hinnangute ja läbivaatuste ülevaatamiseks ja avaldamiseks teie e-äri saidil.

Mõned ettevõtted võivad siiski eelistada, et moderaatorid sisestaksid ülevaatused enne nende avaldamist käsitsi ja kinnitaksid. Hinnangute ja ülevaadete käsitsi avaldamiseks moderaatori poolt peate lubama **Nõutav moderaator hinnanguteks ja ülevaadeteks** funktsiooni Commerce'i saidikonstruktoris.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Commerce'i saidilooja hinnangute ja ülevaatete funktsiooni nõua moderaatorit lubamine

Et lubada **Nõua moderaatorit hinnangutele ja ülevaadetele** funktsiooni Commerce'i saidiloojas, järgi järgmisi samme.

1. Avage **Avaleht \> Arvustused \> Seaded**.
1. Seadke **hinnangute ja ülevaadete jaoks moderaatori nõudmise** suvandi väärtuseks **Sees**.

> [!NOTE]
> Lubades **hinnangute ja ülevaadete jaoks moderaator** funktsiooni, peatate hinnangute ja kommentaaride automaatse avaldamise, nii et on nõutav käsitsi avaldamine. Azure Cognitive Services teenused jätkavad siiski uuesti profileerimist läbivaatuse pealkirjades ja sisus.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Hinnangute ja arvustuste avaldamine

Hinnangute ja ülevaadete käsitsi avaldamiseks moderaatori poolt peate lubama **Nõutav moderaator hinnanguteks ja ülevaadeteks** funktsiooni Commerce'i saidikonstruktoris, et see ilmuks teie e-äris.

Et vaadata ja avaldada hinnanguid ja kommentaare Commerce saidiehitajas, toimige järgmiselt.

1. Avage **Arvustused \> Modereerimine**.
1. Kui ruudustikus **Olek** väli rea jaoks on seatud väärtusele **Avaldamata**, ei ole selle rea hinnangut ja ülevaadet veel avaldatud. Ainult avaldamata hinnangute ja läbivaatuste kuvamiseks valige **Olek: vajab ülevaatamist** ruudustiku kohal olekufiltris.
1. Valige üks või mitu hinnangut ja ülevaadet, mille olek on **Avaldamata** ja seejärel valige käsuribal **Avaldamine**. Valitud hinnangud ja ülevaated lisatakse avaldamisjärjekorda ja kuvatakse pärast nende avaldamist e-kaubanduse saidil.

> [!NOTE]
> - Pärast hindamise ja ülevaatuse avaldamist muutub oleku väärtus **Avaldamata** nullväärtuseks (tühi väli).
> - Kui valite mitu hinnangut ja ülevaadet, mille olekud on erinevad, ja seejärel valite **Avalda**, avaldatakse veel avaldamata hinnangud ja ülevaated. Kuid juba avaldatud hinnanguid ja kommentaare ei avaldata uuesti.

Järgmine illustratsioon kujutab näidet, kus Commerce'i saidilooja **Modereerimise** lehel on valitud kolm avaldamata hinnangut ja ülevaadet.

![Commerce'i saidilooja Modereerimise lehel valitud kolm avaldamata hinnangut ja ülevaadet.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine](sync-product-ratings.md)

[Hinnangute ja kommentaaride importimine ja eksportimine](import-export-reviews.md)

[Teenusepõhise autentimise konfigureerimine](service-to-service-auth.md)

[Hinnangud ja arvustused KKK](ratings-reviews-faq.md)
