---
title: Koondandmete otsingu keskkonna häälestamine
description: Selles teemas selgitatakse, kuidas seadistada oma keskkond kasutama maksuarvestuse põhiandmete otsingufunktsiooni.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924150"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Koondandmete otsingu keskkonna häälestamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada oma keskkond kasutama maksuarvestuse põhiandmete otsingufunktsiooni.

1. Seadistage energiaplatvormi integreerimine rakenduses Lifecycle Services (LCS). Lisateavet vt teemast [Microsoft Power Platform ingegratsioon - lisandmooduli ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Dynamics 365 Finance ja Microsoft Dataverse häälestamine. Lisateavet vt teemadest [Lahenduse leidmine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ja [Autentimine ja autoriseerimine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Seadistage järgmised üksused. Lisateavet leiate [Virtuaalsete jaotiste lubamine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
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
4. Seadistage Dynamics 365 Regulatory Configuration Service (RCS). 
5. Järgmiste funktsioonide lendamise lubamiseks looge Microsofti jaoks teenusetaotlus.

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Minge **Funktsioonide haldus** tööruumi ja lülitage sisse järgmised funktsioonid:

      - (Eelvaade) Elektroonilise aruandluse Dataverse andmeallikate tugi
      - (Eelversioon) Maksuteenuse Dataverse'i andmeallikate tugi
      - (Eelvaade) Globaliseerimisfunktsioonid

5. Logige RCS-i sisse rentniku administraatorikontoga.
6. Avage **Elektrooniline aruandlus** > **Ühendatud rakendused**. 
7. Kirje lisamiseks klõpsake nuppu **Uus** ja sisestage järgmine väljateave. 

   - Väljale **Nimi** sisestage nimi.
   - Väljal **Tüüp** valige **Dataverse**.
   - Väljale **Rakendus** sisestage oma Dataverse URL.
   - Väljal **Rentnik** sisestage oma rentnik.
   - Sisestage väljale **Kohandatud URL** oma Dataverse URL ja lisage see tekstiga "/api/data/v9.1".

8. Valige **Kontrolli ühendust** ja viige ühendusprotsess lõpule. 

   [![Nupp Kontrolli ühendust](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Avage **Elektrooniline aruandlus** > **Maksukonfiguratsioonid** ja importige maksukonfiguratsioonid teemast [Maksukonfiguratsioonid](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Maksukonfiguratsioonide leht, maksuandmete mudelipuu](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Microsofti konfiguratsiooni kasutamisel minge **Maksustatava dokumendi mudeli vastendamine** või **Dataverse mudelivastendus** ja valige väljal **Ühendatud rakendus** 7. etapis loodud kirje.
11. Seadistage **Vaikimisi mudeli vastendamise** väärtusele **Jah**.

   [![Mudelivastenduse leht](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
