---
title: Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas
description: Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage Dynamics 365 Commerce'i keskkonnas, mis on tootesoovituste lubamise eeltingimus.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5887ae7983fd817a929a185327671b301808b354
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478232"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="dc831-103">Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="dc831-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc831-104">Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage Dynamics 365 Commerce'i keskkonnas, mis on tootesoovituste lubamise eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="dc831-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="dc831-105">Dynamics 365 Commerce lahenduses jälgitakse kogu toote ja kande teavet keskkonna üksuse kaupluses.</span><span class="sxs-lookup"><span data-stu-id="dc831-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="dc831-106">Et muuta need andmed kättesaadavaks teistele Dynamics 365 teenustele, nagu andmeanalüütika, äriteave ja isikupärastatud soovitused, on vaja ühendada keskkond kliendi omanduses oleva Azure Data Lake Storage Gen 2 lahendusega.</span><span class="sxs-lookup"><span data-stu-id="dc831-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="dc831-107">Kuna Azure Data Lake Storage on keskkonnas konfigureeritud, võetakse kõik vajalikud andmed üksusesalvest, mis on endiselt kaitstud ja kliendi kontrolli all.</span><span class="sxs-lookup"><span data-stu-id="dc831-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="dc831-108">Kui tootesoovitused või isikupärastatud soovitused on keskkonnas samuti lubatud, antakse tootesoovituste virnale juurdepääs spetsiaalsele kaustale Azure Data Lake Storage'is, et tuua kliendi andmed ja arvutada nende põhjal soovitusi.</span><span class="sxs-lookup"><span data-stu-id="dc831-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dc831-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="dc831-109">Prerequisites</span></span>

<span data-ttu-id="dc831-110">Klientidel peab olema Azure Data Lake Storage konfigureeritud Azure'i kordustellimuses, mida nad omavad.</span><span class="sxs-lookup"><span data-stu-id="dc831-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="dc831-111">See teema ei hõlma Azure'i kordustellimuse ostmist või Azure Data Lake Storage'i toega salvestusruumi konto seadistamist.</span><span class="sxs-lookup"><span data-stu-id="dc831-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="dc831-112">Lisateavet Azure Data Lake Storage'i kohta vt [Azure Data Lake Storage Gen 2 ametlikust dokumentatsioonist](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="dc831-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="dc831-113">Konfiguratsiooni etapid</span><span class="sxs-lookup"><span data-stu-id="dc831-113">Configuration steps</span></span>

<span data-ttu-id="dc831-114">See jaotis hõlmab konfigureerimistoiminguid, mis on vajalikud Azure Data Lake Storage'i lubamiseks keskkonnas, kuna see on seotud tootesoovitustega.</span><span class="sxs-lookup"><span data-stu-id="dc831-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="dc831-115">Azure Data Lake Storage'i lubamiseks vajalikest toimingutest põhjalikuma ülevaate saamiseks vaadake teemat [Muuda üksusesalv Data Lake’i üksusena saadavaks](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="dc831-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="dc831-116">Azure Data Lake Storage'i lubamine keskkonnas</span><span class="sxs-lookup"><span data-stu-id="dc831-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="dc831-117">Logige sisse keskkonna kontoriportaali.</span><span class="sxs-lookup"><span data-stu-id="dc831-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="dc831-118">Otsige **Süsteemi parameetreid** ja navigeerige vahekaardile **Andmeühendused**.</span><span class="sxs-lookup"><span data-stu-id="dc831-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="dc831-119">Määrake **Luba Data Lake integratsioon** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dc831-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="dc831-120">Määrake **Data Lake värskenduse niristamine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dc831-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="dc831-121">Seejärel sisestage järgmine kohustuslik teave:</span><span class="sxs-lookup"><span data-stu-id="dc831-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="dc831-122">**Rakenduse ID** // **Rakenduse saladus** // **DNS-i nimi** – vajalik ühenduse loomiseks KeyVaultiga, kus on talletatud Azure Data Lake Storage saladus.</span><span class="sxs-lookup"><span data-stu-id="dc831-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="dc831-123">**Salajane nimi** – KeyVaulti salvestatud salajane nimi, mida kasutatakse Azure Data Lake Storage'i autentimiseks.</span><span class="sxs-lookup"><span data-stu-id="dc831-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="dc831-124">Salvestage muudatused lehe ülemises vasakus nurgas.</span><span class="sxs-lookup"><span data-stu-id="dc831-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="dc831-125">Järgmisel pildil on näide Azure Data Lake Storage'i konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="dc831-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Azure Data Lake Storage'i konfiguratsiooni näide](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="dc831-127">Azure Data Lake Storage'i ühenduse kontrollimine</span><span class="sxs-lookup"><span data-stu-id="dc831-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="dc831-128">Testige ühendust KeyVault, kasutades **Testi Azure Key Vault** linki.</span><span class="sxs-lookup"><span data-stu-id="dc831-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="dc831-129">Testige Azure Data Lake Storage'i ühendust lingi **Testi Azure Storage'it** abil.</span><span class="sxs-lookup"><span data-stu-id="dc831-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="dc831-130">Kui testid ebaõnnestuvad, kontrollige, kas kõik ülaltoodud KeyVaulti andmed on õiged ja proovige uuesti.</span><span class="sxs-lookup"><span data-stu-id="dc831-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="dc831-131">Kui ühenduse testid on edukad, peate lubama automaatse värskendamise üksuse kaupluses.</span><span class="sxs-lookup"><span data-stu-id="dc831-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="dc831-132">Üksuse poe automaatse värskendamise lubamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="dc831-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="dc831-133">Otsige **Üksuse kauplust**.</span><span class="sxs-lookup"><span data-stu-id="dc831-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="dc831-134">Liikuge vasakpoolses loendis kirjeni **RetailSales** ja valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc831-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="dc831-135">Veenduge, et **Automaatne värskendamine lubatud** väärtuseks oleks seatud **Jah**, valige **Värskenda** ja seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc831-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="dc831-136">Järgmisel pildil on üksuse kaupluse näide, millel automaatne värskendamine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="dc831-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Üksuse kaupluse näide, millel automaatne värskendamine on lubatud](./media/exampleADLSConfig2.png)

<span data-ttu-id="dc831-138">Azure Data Lake Storage on nüüd keskkonna jaoks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="dc831-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="dc831-139">Kui see ei ole juba lõpule viidud, järgige juhiseid keskkonna [tootesoovituste ja isikupärastamise lubamiseks](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="dc831-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc831-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="dc831-140">Additional resources</span></span>

[<span data-ttu-id="dc831-141">Üksusesalve Data Lake’i üksusena saadavaks muutmine</span><span class="sxs-lookup"><span data-stu-id="dc831-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="dc831-142">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="dc831-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="dc831-143">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="dc831-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="dc831-144">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="dc831-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="dc831-145">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="dc831-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="dc831-146">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="dc831-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="dc831-147">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="dc831-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="dc831-148">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="dc831-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="dc831-149">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="dc831-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="dc831-150">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="dc831-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="dc831-151">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="dc831-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="dc831-152">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="dc831-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
