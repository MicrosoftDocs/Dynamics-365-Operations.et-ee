---
title: Koondandmete otsingu keskkonna häälestamine
description: Selles teemas selgitatakse, kuidas seadistada oma keskkond kasutama maksuarvestuse põhiandmete otsingufunktsiooni.
author: kai-cloud
ms.date: 04/21/2021
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
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021340"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="3320d-103">Koondandmete otsingu keskkonna häälestamine</span><span class="sxs-lookup"><span data-stu-id="3320d-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3320d-104">Selles teemas selgitatakse, kuidas seadistada oma keskkond kasutama maksuarvestuse põhiandmete otsingufunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="3320d-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="3320d-105">Seadistage energiaplatvormi integreerimine rakenduses Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3320d-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="3320d-106">Lisateavet vt teemast [Microsoft Power Platform ingegratsioon - lisandmooduli ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3320d-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="3320d-107">Dynamics 365 Finance ja Microsoft Dataverse häälestamine.</span><span class="sxs-lookup"><span data-stu-id="3320d-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="3320d-108">Lisateavet vt teemadest [Lahenduse leidmine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ja [Autentimine ja autoriseerimine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="3320d-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="3320d-109">Seadistage järgmised üksused.</span><span class="sxs-lookup"><span data-stu-id="3320d-109">Set up the following entities.</span></span> <span data-ttu-id="3320d-110">Lisateavet leiate [Virtuaalsete jaotiste lubamine](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="3320d-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="3320d-111">EttevõteInfoÜksus</span><span class="sxs-lookup"><span data-stu-id="3320d-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="3320d-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="3320d-112">CurrencyEntity</span></span>
      - <span data-ttu-id="3320d-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="3320d-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="3320d-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="3320d-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="3320d-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="3320d-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="3320d-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="3320d-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="3320d-117">LogistikaAadressLinnÜksus</span><span class="sxs-lookup"><span data-stu-id="3320d-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="3320d-118">LogistikaAadressRiikRegioonTõlgeÜksus</span><span class="sxs-lookup"><span data-stu-id="3320d-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="3320d-119">LogistikaAadressOsariikÜksus</span><span class="sxs-lookup"><span data-stu-id="3320d-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="3320d-120">OstaHankedTasuCDSÜksus</span><span class="sxs-lookup"><span data-stu-id="3320d-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="3320d-121">MüükTasuCDSÜksus</span><span class="sxs-lookup"><span data-stu-id="3320d-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="3320d-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="3320d-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="3320d-123">MaksKaupGruppPäisÜksus</span><span class="sxs-lookup"><span data-stu-id="3320d-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="3320d-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="3320d-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="3320d-125">Seadistage Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="3320d-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="3320d-126">Järgmiste funktsioonide lendamise lubamiseks looge Microsofti jaoks teenusetaotlus.</span><span class="sxs-lookup"><span data-stu-id="3320d-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="3320d-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="3320d-127">ERCdsFeature</span></span>
      - <span data-ttu-id="3320d-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="3320d-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="3320d-129">Minge **Funktsioonide haldus** tööruumi ja lülitage sisse järgmised funktsioonid:</span><span class="sxs-lookup"><span data-stu-id="3320d-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="3320d-130">(Eelvaade) Elektroonilise aruandluse Dataverse andmeallikate tugi</span><span class="sxs-lookup"><span data-stu-id="3320d-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="3320d-131">(Eelversioon) Maksuteenuse Dataverse'i andmeallikate tugi</span><span class="sxs-lookup"><span data-stu-id="3320d-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="3320d-132">(Eelvaade) Globaliseerimisfunktsioonid</span><span class="sxs-lookup"><span data-stu-id="3320d-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="3320d-133">Logige RCS-i sisse rentniku administraatorikontoga.</span><span class="sxs-lookup"><span data-stu-id="3320d-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="3320d-134">Avage **Elektrooniline aruandlus** > **Ühendatud rakendused**.</span><span class="sxs-lookup"><span data-stu-id="3320d-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="3320d-135">Kirje lisamiseks klõpsake nuppu **Uus** ja sisestage järgmine väljateave.</span><span class="sxs-lookup"><span data-stu-id="3320d-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="3320d-136">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="3320d-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="3320d-137">Väljal **Tüüp** valige **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="3320d-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="3320d-138">Väljale **Rakendus** sisestage oma Dataverse URL.</span><span class="sxs-lookup"><span data-stu-id="3320d-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="3320d-139">Väljal **Rentnik** sisestage oma rentnik.</span><span class="sxs-lookup"><span data-stu-id="3320d-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="3320d-140">Sisestage väljale **Kohandatud URL** oma Dataverse URL ja lisage see tekstiga "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="3320d-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="3320d-141">Valige **Kontrolli ühendust** ja viige ühendusprotsess lõpule.</span><span class="sxs-lookup"><span data-stu-id="3320d-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="3320d-142">[![Nupp Kontrolli ühendust](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="3320d-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="3320d-143">Avage **Elektrooniline aruandlus** > **Maksukonfiguratsioonid** ja importige maksukonfiguratsioonid teemast [Maksukonfiguratsioonid](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="3320d-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="3320d-144">[![Maksukonfiguratsioonide leht, maksuandmete mudelipuu](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="3320d-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="3320d-145">Microsofti konfiguratsiooni kasutamisel minge **Maksustatava dokumendi mudeli vastendamine** või **Dataverse mudelivastendus** ja valige väljal **Ühendatud rakendus** 7. etapis loodud kirje.</span><span class="sxs-lookup"><span data-stu-id="3320d-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="3320d-146">Seadistage **Vaikimisi mudeli vastendamise** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3320d-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="3320d-147">[![Mudelivastenduse leht](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="3320d-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
