---
title: ADLS lubamine Dynamics 365 Commerce keskkonnas
description: Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage (ADLS) ja katsetada Dynamics 365 Commerce keskkonda, mis on toote soovituste lubamise eeltingimus.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c037f5603af5af84917084eefa1edd508891c0d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154432"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="ff9ad-103">ADLS lubamine Dynamics 365 Commerce keskkonnas</span><span class="sxs-lookup"><span data-stu-id="ff9ad-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff9ad-104">Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage (ADLS) ja katsetada Dynamics 365 Commerce keskkonda, mis on toote soovituste lubamise eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="ff9ad-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ff9ad-105">Overview</span></span>

<span data-ttu-id="ff9ad-106">Dynamics 365 Commerce lahenduses jälgitakse kogu toote ja kande teavet keskkonna üksuse kaupluses.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="ff9ad-107">Et muuta need andmed kättesaadavaks teistele Dynamics 365 teenustele, nagu andmeanalüütika, äriteave ja isikupärastatud soovitused, on vaja ühendada keskkond kliendi omanduses oleva Azure Data Lake Storage Gen 2 (ADLS) lahendusega.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="ff9ad-108">Kuna ADLS on keskkonnas konfigureeritud, peegeldatakse kõik vajalikud andmed üksuse kauplusest, mis on endiselt kaitstud ja kliendi kontrolli all.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="ff9ad-109">Kui toote soovitused või isikupärastatud soovitused on keskkonnas samuti lubatud, antakse toote soovituste pinule juurdepääs spetsiaalsele kaustale ADLS-is, et tuua kliendi andmed ja arvutada selle põhjal soovitusi.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ff9ad-110">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="ff9ad-110">Prerequisites</span></span>

<span data-ttu-id="ff9ad-111">Klientidel peab olema ADLS konfigureeritud Azure'i kordustellimuses, mida nad omavad.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="ff9ad-112">See teema ei hõlma Azure'i kordustellimuse ostmist või ADLS-toega salvestusruumi konto häälestust.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="ff9ad-113">Lisateavet ADLS kohta vt [ADLS ametlikust dokumentatsioonist](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="ff9ad-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="ff9ad-114">Konfiguratsiooni etapid</span><span class="sxs-lookup"><span data-stu-id="ff9ad-114">Configuration steps</span></span>

<span data-ttu-id="ff9ad-115">Selles jaotises käsitletakse ADLS lubamiseks vajalikke konfiguratsiooni etappe.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="ff9ad-116">ADLS lubamine keskkonnas</span><span class="sxs-lookup"><span data-stu-id="ff9ad-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="ff9ad-117">Logige sisse keskkonna kontoriportaali.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="ff9ad-118">Otsige **Süsteemi parameetreid** ja navigeerige vahekaardile **Andmeühendused**.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="ff9ad-119">Määrake **Luba Data Lake integratsioon** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="ff9ad-120">Määrake **Data Lake värskenduse niristamine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="ff9ad-121">Seejärel sisestage järgmine kohustuslik teave:</span><span class="sxs-lookup"><span data-stu-id="ff9ad-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="ff9ad-122">**Rakenduse ID** // **Rakenduse saladus** // **DNS-i nimi** – vajalik ühenduse loomiseks KeyVaultiga, kus ADLS saladus on talletatud.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="ff9ad-123">**Salajane nimi** – KeyVaulti salvestatud salajane nimi, mida kasutatakse ADLS autentimiseks.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="ff9ad-124">Salvestage muudatused lehe ülemises vasakus nurgas.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="ff9ad-125">Järgmine pilt näitab näidet ADLS konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-125">The following image shows an example ADLS configuration.</span></span>

![Ekspordi ADLS konfiguratsioon](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="ff9ad-127">ADLS ühenduse kontrollimine</span><span class="sxs-lookup"><span data-stu-id="ff9ad-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="ff9ad-128">Testige ühendust KeyVault, kasutades **Testi Azure Key Vault** linki.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="ff9ad-129">Testige ühendust ADLS-iga, kasutades **Testi Azure Storage** linki.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="ff9ad-130">Kui testid ebaõnnestuvad, kontrollige, kas kõik ülaltoodud KeyVaulti andmed on õiged ja proovige uuesti.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="ff9ad-131">Kui ühenduse testid on edukad, peate lubama automaatse värskendamise üksuse kaupluses.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="ff9ad-132">Üksuse poe automaatse värskendamise lubamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="ff9ad-133">Otsige **Üksuse kauplust**.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="ff9ad-134">Liikuge vasakpoolses loendis kirjeni **RetailSales** ja valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="ff9ad-135">Veenduge, et **Automaatne värskendamine lubatud** väärtuseks oleks seatud **Jah**, valige **Värskenda** ja seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="ff9ad-136">Järgmisel pildil on üksuse kaupluse näide, millel automaatne värskendamine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Üksuse kaupluse näide, millel automaatne värskendamine on lubatud](./media/exampleADLSConfig2.png)

<span data-ttu-id="ff9ad-138">ADLS on nüüd keskkonna jaoks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="ff9ad-139">Kui see ei ole juba lõpule viidud, järgige juhiseid keskkonna [tootesoovituste ja isikupärastamise lubamiseks](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ad-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff9ad-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ff9ad-140">Additional resources</span></span>

[<span data-ttu-id="ff9ad-141">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="ff9ad-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ff9ad-142">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="ff9ad-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ff9ad-143">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="ff9ad-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ff9ad-144">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="ff9ad-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ff9ad-145">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="ff9ad-145">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ff9ad-146">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="ff9ad-146">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ff9ad-147">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="ff9ad-147">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ff9ad-148">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="ff9ad-148">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ff9ad-149">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="ff9ad-149">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ff9ad-150">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="ff9ad-150">Product recommendations FAQ</span></span>](faq-recommendations.md)


