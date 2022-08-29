---
title: Hinnangute ja arvustuste kasutamise valimine
description: See artikkel selgitab, kuidas soovite oma saidi hinnanguid ja ülevaateid Microsoft Dynamics 365 Commerce kasutada.
author: gvrmohanreddy
ms.date: 02/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 00fd30ded916cc6b587ceff67728e7d964714716
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269158"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Hinnangute ja arvustuste kasutamise valimine

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas soovite oma saidi hinnanguid ja ülevaateid Microsoft Dynamics 365 Commerce kasutada.

Hinnangute ja arvustuste lahendus on omnikanali lahendus, mille saate rakenduses Dynamics 365 Commerce teha kättesaadavaks, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS). LCS on haldusportaal, mida jaemüüjad kasutavad oma keskkondade juhtimiseks alates ettevalmistusest kuni kasutusest eemaldamiseni.

Kui soovite oma Commerce’i veebisaidil kasutada hinnangute ja arvustuste lahendust, peate rakenduses Dynamics 365 Commerce e-kaubanduse saidi juurutamisel nõustuma hinnangute ja arvustustega.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Hinnangute ja arvustuste kasutamise valimine

Oma saidil hinnangute ja arvustuste kasutamisega nõustumiseks järgige neid samme.

1. Järgige samme teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md).
1. Olles endiselt LCS-is, avage suvand **Jaemüügi juurutamise häälestus \> Muud sätted**.
1. Määrake suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** väärtusele **Jah**.
1. Sisestage **AAD reitingute ja läbivaatuse moderaatori** väljale Microsofti (Azure Active Directory) turvagrupi ID Azure AD, mis sisaldab hinnanguid ja vaatab modera doublei üle.

    ![Hinnangute ja arvustuste kasutamise valimine.](media/LCS_RnR_Preference_2.png)

1. Viige e-kaubanduse lähtestamise protsess lõpule.

> [!NOTE] 
> Kui olete olemasolev rakenduse Dynamics 365 Commerce klient, kes on juba võtnud e-kaubanduse saidi kasutusele, ilma et oleks valinud hinnanguid ja arvustusi, ning nüüd soovite kasutada Dynamics 365 Commerce’i paketist hinnanguid ja arvustusi, esitage teenusetaotlus. Teavet teenusetaotluse kasutamise kohta vt teemast [Teenusetaotluse esitamise protsess](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine rakenduses Dynamics 365 Commerce](sync-product-ratings.md)

[Lubage hinnangute ja ülevaadete käsitsi avaldamine moderaatori poolt](manual-publish-rating-reviews.md)

[Hinnangute ja arvustuste importimine ja eksportimine](import-export-reviews.md)

[Teenusest teenusesse autentimise konfigureerimine](service-to-service-auth.md)

[Hinnangud ja arvustused KKK](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
