---
title: Luba koondandmete otsing maksuarvestuse konfiguratsiooni jaoks
description: See teema kirjeldab, kuidas seadistada ja lubada maksu arvutamise koondandmete otsingufunktsioone.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 455e8becfdfa910a3733719653e1a91557b2f59a
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867348"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Luba koondandmete otsing maksuarvestuse konfiguratsiooni jaoks 

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada ja lubada maksu arvutamise koondandmete otsingufunktsioone. Ripploendit saab kasutada maksuarvutuse konfiguratsioonis selliste väljade väärtused nagu Juriidiline **isik**, **Hankija** konto, **Kaubakood** ja Tarne **tähtaeg**. Need väärtused tulevad andmeallikat kasutades Dynamics 365 Finance ühendatud Microsofti Microsoft Dataverse keskkonnast.

> [!NOTE] 
> Maksu arvutamise koondandmete otsingu funktsioon on valikuline funktsioon. Kui keelate maksuteenuse andmeallikate tugifunktsiooni regulatiivses konfiguratsiooniteenuses **Dataverse** (RCS), võite järgmised sammud vahele jätta. Sel juhul ei ole aga ripploend maksuarvestuse konfiguratsioonis saadaval.

1. Seadistage Microsoft Power Platform integreerimine rakenduses Microsoft Dynamics Lifecycle Services (LCS). Lisateavet vt teemast [Microsoft Power Platform ingegratsioon - lisandmooduli ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Pärast selle toimingu sooritamist kuvatakse jaotises **Power Platform Integration** Microsoft Power Platformi keskkonna nimi.
2. Minge [Microsoft Power Platformi halduskeskusesse](https://admin.powerplatform.microsoft.com/environments) ja valige keskkonna nimi. Keskkonna URL on esitatud.
3. Dynamics 365 Finance ja Dataverse häälestamine. Lisateavet vt teemadest [Virtuaalse olemi lahenduse leidmine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) ja [Autentimine ja autoriseerimine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Seadistage järgmised üksused. Lisateavet vt [Microsoft Dataverse virtuaalsete olemite lubamine](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

    - EttevõteInfoÜksus
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogistikaAadressLinnÜksus
    - LogistikaAadressRiikRegioonTõlgeÜksus
    - LogistikaAadressOsariikÜksus
    - OstaHankedTasuCDSÜksus
    - MüükTasuCDSÜksus
    - TaxGroupEntity
    - MaksKaupGruppPäisÜksus
    - VendVendorV2Entity

5. Seadistage Regulatory Configuration Service (RCS). Avage **Funktsioonide haldus** tööruumi ja lülitage sisse järgmised funktsioonid:

    - elektroonilise aruandluse Dataverse andmeallikate tugi
    - Maksuteenuse Dataverse'i andmeallikate tugi
    - Globaliseerimisfunktsioonid

6. Logige RCS-i sisse rentniku administraatorikontoga.
7. Avage **Elektrooniline aruandlus** > **Ühendatud rakendused**. 
8. Kirje lisamiseks klõpsake nuppu **Uus** ja sisestage järgmine väljateave. 

    - Väljale **Nimi** sisestage nimi.
    - Väljal **Tüüp** valige **Dataverse**.
    - Väljale **Rakendus** sisestage oma Dataverse URL.
    - Väljal **Rentnik** sisestage oma rentnik.
    - Sisestage väljale **Kohandatud URL** oma Dataverse URL ja lisage see tekstiga "/api/data/v9.1".

9. Valige **Kontrolli ühendust** ja viige ühendusprotsess lõpule. 

    [![Ühenduse kontrollimise nupp.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Avage **Elektrooniline aruandlus** > **Maksukonfiguratsioonid** ja importige maksukonfiguratsioonid teemast [Maksukonfiguratsioonid](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Maksukonfiguratsioonide leht, maksuandmete mudelipuu.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Microsofti konfiguratsiooni kasutamisel minge **Maksustatava dokumendi mudeli vastendamine** või **Dataverse mudelivastendus** ja valige väljal **Ühendatud rakendus** 7. etapis loodud kirje.
12. Seadistage **Vaikimisi mudeli vastendamise** väärtusele **Jah**.

    [![Mudelivastenduse leht.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
