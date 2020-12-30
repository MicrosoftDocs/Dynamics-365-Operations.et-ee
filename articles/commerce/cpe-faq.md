---
title: Dynamics 365 Commerce'i hindamiskeskkonna KKK
description: Selles jaotises antakse vastuseid korduma kippuvatele küsimustele Microsoft Dynamics 365 Commerce'i hindamiskeskkonna kohta.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411572"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce'i hindamiskeskkonna KKK

[!include [banner](includes/banner.md)]

Selles jaotises antakse vastuseid korduma kippuvatele küsimustele Microsoft Dynamics 365 Commerce'i hindamiskeskkonna kohta.

**Kas saame kasutada Commerce'i hindamiskeskkonda e-kaubanduse poena klientidele, kes rakendavad praegu jaemüüki?**

Nr Commerce'i hindamiskeskkond on ainult hindamiseks. Kui vajate jaemüügis kasutatava kliendi jaoks keskkonda, siis kontakteeruge Microsoftiga.

**Kas Commerce'i hindamiskeskkonda saab kasutada e-kaubanduse funktsioonide pakkumiseks olemasoleva rakenduse/keskkonna jaoks, mis rakendab jaemüüki?**

Ei (enamasti). Commerce'i hindamise komponendid on saadaval ainult keskkondadele, mis vastavad eeltingimustes ja ettevalmistamise juhendis määratud konfiguratsioonidele. Lisaks ei ole nõutavad aluseks olevad demoandmed saadaval keskkondades, mis on rakendatud algses väljalaskes, mis on varasem kui 10.0.8. 

**Millised kulud on kaasatud Commerce'i hindamiskeskkonna Microsoft Azure keskkonna kasutamisele läbi Microsoft Dynamics Lifecycle Servicesi (LCS)?**

Traditsiooniline Dynamics 365 Finance'i / Dynamics 365 Supply Chain Managementi / Dynamics 365 Commerce'i peakontori demokeskkond (virtuaalarvuti \[VM\]) majutatakse teie Azure'i tellimuses. Selle kulu hindamiseks saate kasutada [Azure hinnakujunduse kalkulaatorit ](https://azure.microsoft.com/pricing/calculator/).

Muud komponendid, nt Commerce Scale Unit, Commerce'i saidiehitaja ja teie e-kaubanduse sait, on saadaval tarkvarana teenusena (SaaS) ja majutatakse Microsoftis.

**Millised Azure'i geograafilised piirkonnad on praegu Commerce'i hindamiskeskkonna jaoks toetatud?**

Commerce'i hindamiskeskkonda saab kasutada ainult Põhja-Ameerika piirkonnas.

**Kas on olemas ka allalaaditav virtuaalne kõvaketas (VHD), millel on täielik OneBox virtuaalarvuti (VM) suvand?**

Dynamics 365 Commerce ja Commerce Scale Unit on täielikult tarkvara teenusena (SaaS) ja peavad olema pilve majutatud.

**Kui kaua saab Commerce'i hindamiskeskkonda kasutada?**

Commerce'i hindamiskeskkonnal on 30-päevane ajapiirang alates SaaS-konponentide, nagu Commerce Scale Uniti, Commerce'i saidiehitaja ja teie e-kaubanduse saidi, ettevalmistamise kuupäevast.

**Kas ma saan oma Commerce'i hindamiskeskkonna ajapiirangut pikendada?**

Piirangu pikendamine on erand ja seda käsitletakse juhtumipõhiselt. Abi saamiseks peaksite pöörduma oma Microsofti partneri kontakti poole.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce'i hindamiskeskkonna ülevaade](cpe-overview.md)

[Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine](provisioning-guide.md)

[Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine](cpe-post-provisioning.md)

[BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas](cpe-bopis.md)

[Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md)
