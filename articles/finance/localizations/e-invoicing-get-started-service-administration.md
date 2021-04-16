---
title: Elektroonilise arvelduse teenusehaldusega alustamine
description: Selles teemas selgitatakse, kuidas elektroonilise arveldusega alustada.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840144"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="e459b-103">Elektroonilise arvelduse teenusehaldusega alustamine</span><span class="sxs-lookup"><span data-stu-id="e459b-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e459b-104">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e459b-104">Prerequisites</span></span>

<span data-ttu-id="e459b-105">Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="e459b-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="e459b-106">Teil peab olema juurdepääs oma Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kontole.</span><span class="sxs-lookup"><span data-stu-id="e459b-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="e459b-107">Teil peab olema LCS-projekt, mis hõlmab Microsofti teenuste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management versiooni 10.0.17 või uuemat versiooni.</span><span class="sxs-lookup"><span data-stu-id="e459b-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e459b-108">Peale selle peavad need rakendused olema juurutatud ühes järgmistest Azure'i geograafilistest piirkondadest.</span><span class="sxs-lookup"><span data-stu-id="e459b-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="e459b-109">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="e459b-109">East US</span></span>
    - <span data-ttu-id="e459b-110">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="e459b-110">West US</span></span>
    - <span data-ttu-id="e459b-111">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="e459b-111">North EU</span></span>
    - <span data-ttu-id="e459b-112">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="e459b-112">West EU</span></span>

- <span data-ttu-id="e459b-113">Teil peab olema juurdepääs oma Dynamics 365 teenuse Regulatory Configuration Services (RCS) kontole.</span><span class="sxs-lookup"><span data-stu-id="e459b-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="e459b-114">Te peate mooduli Funktsioonihaldus kaudu oma RCS-i konto jaoks globaliseerimisfunktsiooni aktiveerima.</span><span class="sxs-lookup"><span data-stu-id="e459b-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="e459b-115">Lisateavet vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="e459b-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="e459b-116">Peate looma Azure'is võtmehoidla ja salvestamiskonto.</span><span class="sxs-lookup"><span data-stu-id="e459b-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="e459b-117">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e459b-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="e459b-118">Installi Lifecycle Services-is lisandmodul mikroteenuste jaoks</span><span class="sxs-lookup"><span data-stu-id="e459b-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="e459b-119">Logige oma LCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="e459b-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="e459b-120">Valige paan **Eelvaate funktsiooni haldamine**.</span><span class="sxs-lookup"><span data-stu-id="e459b-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="e459b-121">Valige jaotises **Avaliku eelvaateversiooni funktsioonid** suvand **E-arvelduse teenus**.</span><span class="sxs-lookup"><span data-stu-id="e459b-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="e459b-122">Veenduge, et suvandi **Funktsiooni eelversioon on lubatud** väärtuseks oleks valitud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e459b-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="e459b-123">Valige LCS-i armatuurlaudal oma LCS-i juurutusprojekt.</span><span class="sxs-lookup"><span data-stu-id="e459b-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="e459b-124">LCS-projekt peab töötama.</span><span class="sxs-lookup"><span data-stu-id="e459b-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="e459b-125">Valige kiirkaardil **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="e459b-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="e459b-126">Valige **e-arveldusteenused**.</span><span class="sxs-lookup"><span data-stu-id="e459b-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="e459b-127">Väljale **AAD-rakenduse ID** sisestage **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="e459b-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="e459b-128">See väärtus ei muutu.</span><span class="sxs-lookup"><span data-stu-id="e459b-128">This is a fixed value.</span></span>
10. <span data-ttu-id="e459b-129">Sisestage väljale **AAD rentniku ID** oma Azure'i tellimuse konto ID.</span><span class="sxs-lookup"><span data-stu-id="e459b-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="e459b-130">Tingimustega nõustumiseks valige märkeruut.</span><span class="sxs-lookup"><span data-stu-id="e459b-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="e459b-131">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="e459b-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="e459b-132">Määrake parameetrid RCS integratsioonile koos Elekrtoonilise arveldusega</span><span class="sxs-lookup"><span data-stu-id="e459b-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="e459b-133">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="e459b-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e459b-134">Tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** valige suvand **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e459b-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="e459b-135">Sisestage vahekaardil **E-arvelduse teenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.</span><span class="sxs-lookup"><span data-stu-id="e459b-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="e459b-136">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="e459b-136">Datacenter Azure geography</span></span> | <span data-ttu-id="e459b-137">Teenuse lõpp-punkti URI</span><span class="sxs-lookup"><span data-stu-id="e459b-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="e459b-138">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="e459b-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e459b-139">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="e459b-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e459b-140">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="e459b-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e459b-141">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="e459b-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="e459b-142">Veenduge, et välja **Rakenduse ID** väärtuseks oleks määratud **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="e459b-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="e459b-143">See väärtus ei muutu.</span><span class="sxs-lookup"><span data-stu-id="e459b-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="e459b-144">Väljale **LCS-i keskkonna id** sisestage oma LCS-i keskkonna ID.</span><span class="sxs-lookup"><span data-stu-id="e459b-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="e459b-145">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="e459b-146">Võtmehoidla viite loomine</span><span class="sxs-lookup"><span data-stu-id="e459b-146">Create Key Vault references</span></span>

1. <span data-ttu-id="e459b-147">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="e459b-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e459b-148">Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige paan **Elektrooniline arveldus**.</span><span class="sxs-lookup"><span data-stu-id="e459b-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="e459b-149">Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Teenusekeskkond** ja seejärel valige **Võtmehoidla parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e459b-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="e459b-150">Võtmehoidla viite loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e459b-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="e459b-151">Väljale **Nimi** sisestage võtmehoidla viite nimi.</span><span class="sxs-lookup"><span data-stu-id="e459b-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="e459b-152">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e459b-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="e459b-153">Väljale **Võtmehoidla URL** kleepige võtmehoidja saladus Azure'i võtmehoidlast.</span><span class="sxs-lookup"><span data-stu-id="e459b-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="e459b-154">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e459b-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="e459b-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e459b-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="e459b-156">Salvestuskonto saladuse loomine</span><span class="sxs-lookup"><span data-stu-id="e459b-156">Create Storage account secret</span></span>

1. <span data-ttu-id="e459b-157">Lehel **Keskkonna häälestus** Tegevuspaanil, valige **Teenusekeskkond** > **Võtmehoidla parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e459b-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="e459b-158">Valige **Võtmehoidla viide** ja jaotisest **Sertifikaadid** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e459b-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="e459b-159">Väljal **Nimi** sisesta salvestuskonto saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="e459b-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="e459b-160">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e459b-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="e459b-161">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e459b-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e459b-162">Väljalt **Tüüp** valige **Vali**.</span><span class="sxs-lookup"><span data-stu-id="e459b-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="e459b-163">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="e459b-164">Digitaalserdi saladuse loomine</span><span class="sxs-lookup"><span data-stu-id="e459b-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="e459b-165">Lehelt **Keskkonna seadistused** tegevuspaanil valige **Teenusekeskkond** ja seejärel valige **Võtmehoidla parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e459b-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="e459b-166">Valige **Võtmehoidla viide** ja seejärel jaotisest **Sertifikaadid** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e459b-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="e459b-167">Väljal **Nimi** sisestage digitaalse sertifikaadi saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="e459b-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="e459b-168">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e459b-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="e459b-169">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e459b-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e459b-170">Tehke väljal **Tüüp** valik **Sertifikaat**.</span><span class="sxs-lookup"><span data-stu-id="e459b-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="e459b-171">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="e459b-172">Teenusekeskkonna loomine</span><span class="sxs-lookup"><span data-stu-id="e459b-172">Create a service environment</span></span>

1. <span data-ttu-id="e459b-173">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="e459b-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e459b-174">Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige paan **Elektrooniline arveldus**.</span><span class="sxs-lookup"><span data-stu-id="e459b-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="e459b-175">Lehel **Keskkondade seadistused** valige toimingupaanil suvand **Teenusekeskkond**.</span><span class="sxs-lookup"><span data-stu-id="e459b-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="e459b-176">Valige uue teenusekeskkonna loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e459b-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="e459b-177">Sisestage väljale **Nimi** e-arvelduse keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="e459b-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="e459b-178">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e459b-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="e459b-179">Valige väljal **Salvestuskonto SAS-tõendi saladus** salvestuskonto juurdepääsu autentimiseks kasutatava serdi nimi.</span><span class="sxs-lookup"><span data-stu-id="e459b-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="e459b-180">Valige jaotises **Kasutajad** käsk **Lisa**, et lisada kasutaja, kellel on lubatud keskkonna kaudu elektroonilisi arveid edastada ning salvestuskontoga ühendus luua.</span><span class="sxs-lookup"><span data-stu-id="e459b-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="e459b-181">Sisestage väljale **Kasutaja ID** kasutaja pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="e459b-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="e459b-182">Sisestage väljale **E-post** kasutaja e-posti aadress.</span><span class="sxs-lookup"><span data-stu-id="e459b-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="e459b-183">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e459b-183">Select **Save**.</span></span>
10. <span data-ttu-id="e459b-184">Kui teie riigi-/regioonipõhiste arvete puhul on digiallkirjade rakendamiseks vaja serdiahelat, valige toimingupaanil suvand **Võtmehoidla parameetrid** ja seejärel valige **Serdiahel** ning toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e459b-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="e459b-185">Serdiahela loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e459b-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="e459b-186">Sisestage väljale **Nimi** serdiahela nimi.</span><span class="sxs-lookup"><span data-stu-id="e459b-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="e459b-187">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e459b-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="e459b-188">Valige jaotises **Serdid** käsk **Lisa**, et ahelale sert lisada.</span><span class="sxs-lookup"><span data-stu-id="e459b-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="e459b-189">Kasutage nuppu **Üles** või **Alla**, et ahelas serdi asukohta muuta.</span><span class="sxs-lookup"><span data-stu-id="e459b-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="e459b-190">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="e459b-191">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-191">Close the page.</span></span>
11. <span data-ttu-id="e459b-192">Valige lehe **Teenusekeskkond** toimingupaanil käsk **Avalda**, et keskkond pilves avaldada.</span><span class="sxs-lookup"><span data-stu-id="e459b-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="e459b-193">Välja **Olek** väärtuseks määratakse **Avaldatud**.</span><span class="sxs-lookup"><span data-stu-id="e459b-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="e459b-194">Ühendatud rakenduse loomine</span><span class="sxs-lookup"><span data-stu-id="e459b-194">Create a connected application</span></span>

1. <span data-ttu-id="e459b-195">Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Ühendatud rakendused**.</span><span class="sxs-lookup"><span data-stu-id="e459b-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="e459b-196">Valige ühendatud rakenduse loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e459b-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="e459b-197">Sisestage väljale **Nimi** ühendatava rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="e459b-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="e459b-198">Sisestage väljale **Rakendus** ühendatava teenuse Finance ja Supply Chain Management keskkonna URL.</span><span class="sxs-lookup"><span data-stu-id="e459b-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="e459b-199">Sisestage väljale **Rentnik** ühendatava teenuse Finance ja Supply Chain Management keskkonna rentnik.</span><span class="sxs-lookup"><span data-stu-id="e459b-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="e459b-200">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e459b-200">Select **Save**.</span></span>
6. <span data-ttu-id="e459b-201">Keskkonnaga lodud ühenduse testimiseks valige toimingupaanil käsk **Kontrolli ühendust**.</span><span class="sxs-lookup"><span data-stu-id="e459b-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="e459b-202">Seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="e459b-203">Ühendatud rakenduste keskkondadega linkimine</span><span class="sxs-lookup"><span data-stu-id="e459b-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="e459b-204">Valige lehel **Keskkondade seadistused** suvand **Uus**, et ühendatud rakendus keskkonnale määrata.</span><span class="sxs-lookup"><span data-stu-id="e459b-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="e459b-205">Valige väljal **Ühendatud rakendus** ühendatud rakendus.</span><span class="sxs-lookup"><span data-stu-id="e459b-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="e459b-206">Valige väljal **Teenusekeskkond** teenusekeskkond.</span><span class="sxs-lookup"><span data-stu-id="e459b-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="e459b-207">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="e459b-208">Elektroonilise arvelduse integratsiooni seadistamine Finantsis ja Supply Chain Management -is</span><span class="sxs-lookup"><span data-stu-id="e459b-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="e459b-209">Elektroonilise arvelduse integratsioonifunktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="e459b-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="e459b-210">Logige oma teenuse Finance või Supply Chain Management eksemplari sisse.</span><span class="sxs-lookup"><span data-stu-id="e459b-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="e459b-211">Tööruumis **Funktsioonihaldus** otsige üles funktsioon **Elektroonilise arvelduse integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="e459b-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="e459b-212">Kui seda funktsiooni lehel ei kuvata, valige käsk **Kontrolli värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="e459b-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="e459b-213">Valige funktsioon ja seejärel valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="e459b-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="e459b-214">Teenuse lõpp-punkti URL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="e459b-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="e459b-215">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e459b-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="e459b-216">Sisestage vahekaardil **Edastusteenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.</span><span class="sxs-lookup"><span data-stu-id="e459b-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="e459b-217">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="e459b-217">Datacenter Azure geography</span></span> | <span data-ttu-id="e459b-218">Teenuse lõpp-punkti URL</span><span class="sxs-lookup"><span data-stu-id="e459b-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="e459b-219">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="e459b-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e459b-220">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="e459b-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e459b-221">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="e459b-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e459b-222">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="e459b-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="e459b-223">Väljale **Keskkond** sisestage teenusekeskkonna nimi, mis on avaldatud Elektroonilises arvelduses.</span><span class="sxs-lookup"><span data-stu-id="e459b-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="e459b-224">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="e459b-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="e459b-225">Lennuvõtmete lubamine</span><span class="sxs-lookup"><span data-stu-id="e459b-225">Enable Flighting keys</span></span>

<span data-ttu-id="e459b-226">Lubage Lennuvõtmed Microsoft Dynamics 365 Finance -ile või Microsoft Dynamics 365 Supply Chain Management versioonidele 10.0.17 või varasematele.</span><span class="sxs-lookup"><span data-stu-id="e459b-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="e459b-227">Käivitage järgmine SQL-i käsk.</span><span class="sxs-lookup"><span data-stu-id="e459b-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="e459b-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="e459b-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="e459b-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="e459b-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="e459b-230">Käivitage käsk IISreset kõigi AOS-ite jaoks.</span><span class="sxs-lookup"><span data-stu-id="e459b-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
