---
title: Hinnangute ja arvustuste kasutamise valimine
description: Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.
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
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697976"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Hinnangute ja arvustuste kasutamise valimine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.

## <a name="overview"></a>Ülevaade

Hinnangute ja arvustuste lahendus on omnikanali lahendus, mille saate rakenduses Dynamics 365 Commerce teha kättesaadavaks, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS). LCS on haldusportaal, mida jaemüüjad kasutavad oma keskkondade juhtimiseks alates ettevalmistusest kuni kasutusest eemaldamiseni.

Kui soovite oma Commerce’i veebisaidil kasutada hinnanguid ja arvustusi, peate nendega esmalt nõustuma.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Hinnangute ja arvustuste kasutamise valimine

Oma saidil hinnangute ja arvustuste kasutamisega nõustumiseks järgige neid samme.

1. Järgige samme teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md).
1. Olles endiselt LCS-is, avage suvand **Jaemüügi juurutamise häälestus \> Muud sätted**.
1. Määrake suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** väärtusele **Jah**.
1. Sisestage väljale **AAD hinnangute ja arvustuse moderaatori turberühm (turberühma objekti ID)** Microsoft Azure Active Directory (Azure AD) turberühma ID, mis hõlmab hinnangute ja arvustuste moderaatoreid.

    ![Hinnangute ja arvustuste kasutamise valimine](media/LCS_RnR_Preference.png)

1. Viige e-kaubanduse lähtestamise protsess lõpule.

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail](sync-product-ratings.md)
