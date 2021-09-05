---
title: Dynamics 365 Commerce'i hindamiskeskkonna KKK
description: Selles jaotises antakse vastuseid korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 Commerce hindamiskeskkonna kohta.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343554"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce'i hindamiskeskkonna KKK

[!include [banner](includes/banner.md)]

Selles jaotises antakse vastuseid korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 Commerce hindamiskeskkonna kohta.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Kas saame kasutada Commerce'i hindamiskeskkonda e-kaubanduse poena klientidele, kes rakendavad praegu jaemüüki?

Nr Commerce'i hindamiskeskkond on ainult hindamiseks. Kui vajate jaemüügis kasutatava kliendi jaoks keskkonda, siis kontakteeruge Microsoftiga.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Kas Commerce'i hindamiskeskkonda saab kasutada e-kaubanduse funktsioonide pakkumiseks olemasoleva rakenduse/keskkonna jaoks, mis rakendab jaemüüki?

Ei (enamasti). Commerce'i hindamise komponendid on saadaval ainult keskkondadele, mis vastavad eeltingimustes ja ettevalmistamise juhendis määratud konfiguratsioonidele. Lisaks ei ole nõutavad aluseks olevad demoandmed saadaval keskkondades, mis on rakendatud algses väljalaskes, mis on varasem kui 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Millised kulud on kaasatud Commerce'i hindamiskeskkonna Microsoft Azure keskkonna kasutamisele läbi Microsoft Dynamics Lifecycle Serviceses (LCS)?

Traditsiooniline Dynamics 365 Finance'i / Dynamics 365 Supply Chain Managementi / Dynamics 365 Commerce'i peakontori demokeskkond (virtuaalarvuti \[VM\]) majutatakse teie Azure'i tellimuses. Selle kulu hindamiseks saate kasutada [Azure hinnakujunduse kalkulaatorit ](https://azure.microsoft.com/pricing/calculator/).

Muud komponendid, nt Commerce Scale Unit, Commerce'i saidiehitaja ja teie e-kaubanduse sait, on saadaval tarkvarana teenusena (SaaS) ja majutatakse Microsoftis.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Millised Azure'i geograafilised piirkonnad on praegu Commerce'i hindamiskeskkonna jaoks toetatud?

Commerce'i hindamiskeskkonda saab kasutada ainult Põhja-Ameerika piirkonnas.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Kas on olemas ka allalaaditav virtuaalne kõvaketas (VHD), millel on täielik OneBox virtuaalarvuti (VM) suvand?

Dynamics 365 Commerce ja Commerce Scale Unit on täielikult tarkvara teenusena (SaaS) ja peavad olema pilve majutatud.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Kui kaua saab Commerce'i hindamiskeskkonda kasutada?

Commerce'i hindamiskeskkonnal on 30-päevane ajapiirang alates SaaS-konponentide, nagu Commerce Scale Uniti, Commerce'i saidiehitaja ja teie e-kaubanduse saidi, ettevalmistamise kuupäevast.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Kas ma saan oma Commerce'i hindamiskeskkonna ajapiirangut pikendada?

Piirangu pikendamine on erand ja seda käsitletakse juhtumipõhiselt. Abi saamiseks peaksite pöörduma oma Microsofti partneri kontakti poole.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce'i hindamiskeskkonna ülevaade](cpe-overview.md)

[Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine](provisioning-guide.md)

[Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine](cpe-post-provisioning.md)

[BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas](cpe-bopis.md)

[Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
