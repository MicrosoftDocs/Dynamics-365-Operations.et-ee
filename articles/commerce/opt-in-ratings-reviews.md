---
title: Hinnangute ja arvustuste kasutamise valimine
description: Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057506"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Hinnangute ja arvustuste kasutamise valimine

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas nõustuda rakenduses Microsoft Dynamics 365 Commerce saidi hinnangute ja arvustuste kasutamisega.

## <a name="overview"></a>Ülevaade

Hinnangute ja arvustuste lahendus on omnikanali lahendus, mille saate rakenduses Dynamics 365 Commerce teha kättesaadavaks, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS). LCS on haldusportaal, mida jaemüüjad kasutavad oma keskkondade juhtimiseks alates ettevalmistusest kuni kasutusest eemaldamiseni.

Kui soovite oma Commerce’i veebisaidil kasutada hinnangute ja arvustuste lahendust, peate rakenduses Dynamics 365 Commerce e-kaubanduse saidi juurutamisel nõustuma hinnangute ja arvustustega.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Hinnangute ja arvustuste kasutamise valimine

Oma saidil hinnangute ja arvustuste kasutamisega nõustumiseks järgige neid samme.

1. Järgige samme teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md).
1. Olles endiselt LCS-is, avage suvand **Jaemüügi juurutamise häälestus \> Muud sätted**.
1. Määrake suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** väärtusele **Jah**.
1. Sisestage väljale **AAD hinnangute ja arvustuse moderaatori turberühm (turberühma objekti ID)** Microsoft Azure Active Directory (Azure AD) turberühma ID, mis hõlmab hinnangute ja arvustuste moderaatoreid.

    ![Hinnangute ja arvustuste kasutamise valimine](media/LCS_RnR_Preference.png)

1. Viige e-kaubanduse lähtestamise protsess lõpule.

> [!NOTE] 
> Kui olete olemasolev rakenduse Dynamics 365 Commerce klient, kes on juba võtnud e-kaubanduse saidi kasutusele, ilma et oleks valinud hinnanguid ja arvustusi, ning nüüd soovite kasutada Dynamics 365 Commerce’i paketist hinnanguid ja arvustusi, esitage teenusetaotlus. Teavet teenusetaotluse kasutamise kohta vt teemast [Teenusetaotluse esitamise protsess](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine rakenduses Dynamics 365 Commerce](sync-product-ratings.md)


