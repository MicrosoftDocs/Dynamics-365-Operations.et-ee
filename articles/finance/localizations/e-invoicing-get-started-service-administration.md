---
title: Elektroonilise arvelduse lisandmooduli teenuse halduse kasutamise alustamine
description: Selles teemas selgitatakse, kuidas elektroonilise arvelduse lisandmooduli kasutamist alustada.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592522"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="76682-103">Elektroonilise arvelduse lisandmooduli teenuse halduse kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="76682-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="76682-104">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="76682-104">Prerequisites</span></span>

<span data-ttu-id="76682-105">Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="76682-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="76682-106">Teil peab olema juurdepääs oma Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kontole.</span><span class="sxs-lookup"><span data-stu-id="76682-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="76682-107">Teil peab olema LCS-projekt, mis hõlmab Microsofti teenuste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management versiooni 10.0.17 või uuemat versiooni.</span><span class="sxs-lookup"><span data-stu-id="76682-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="76682-108">Peale selle peavad need rakendused olema juurutatud ühes järgmistest Azure'i geograafilistest piirkondadest.</span><span class="sxs-lookup"><span data-stu-id="76682-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="76682-109">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="76682-109">East US</span></span>
    - <span data-ttu-id="76682-110">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="76682-110">West US</span></span>
    - <span data-ttu-id="76682-111">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="76682-111">North EU</span></span>
    - <span data-ttu-id="76682-112">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="76682-112">West EU</span></span>

- <span data-ttu-id="76682-113">Teil peab olema juurdepääs oma Dynamics 365 teenuse Regulatory Configuration Services (RCS) kontole.</span><span class="sxs-lookup"><span data-stu-id="76682-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="76682-114">Te peate mooduli Funktsioonihaldus kaudu oma RCS-i konto jaoks globaliseerimisfunktsiooni aktiveerima.</span><span class="sxs-lookup"><span data-stu-id="76682-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="76682-115">Lisateavet vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="76682-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="76682-116">Peate looma Azure'is võtmehoidla ja salvestamiskonto.</span><span class="sxs-lookup"><span data-stu-id="76682-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="76682-117">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="76682-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="76682-118">Teenuses Lifecycle Services mikroteenuste jaoks lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="76682-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="76682-119">Logige oma LCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="76682-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="76682-120">Valige paan **Eelvaate funktsiooni haldamine**.</span><span class="sxs-lookup"><span data-stu-id="76682-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="76682-121">Valige jaotises **Avaliku eelvaateversiooni funktsioonid** suvand **E-arvelduse teenus**.</span><span class="sxs-lookup"><span data-stu-id="76682-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="76682-122">Veenduge, et suvandi **Funktsiooni eelversioon on lubatud** väärtuseks oleks valitud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="76682-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="76682-123">Valige LCS-i armatuurlaudal oma LCS-i juurutusprojekt.</span><span class="sxs-lookup"><span data-stu-id="76682-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="76682-124">LCS-projekt peab töötama.</span><span class="sxs-lookup"><span data-stu-id="76682-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="76682-125">Valige kiirkaardil **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="76682-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="76682-126">Valige **e-arveteenused** ja sisestage **AAD-rakenduse ID** väljale **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="76682-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="76682-127">See väärtus ei muutu.</span><span class="sxs-lookup"><span data-stu-id="76682-127">This is a fixed value.</span></span>
10. <span data-ttu-id="76682-128">Sisestage väljale **AAD rentniku ID** oma Azure'i tellimuse konto ID.</span><span class="sxs-lookup"><span data-stu-id="76682-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="76682-129">Tingimustega nõustumiseks valige märkeruut.</span><span class="sxs-lookup"><span data-stu-id="76682-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="76682-130">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="76682-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="76682-131">RCS-i elektroonilise arvelduse lisandmooduliga integratsiooni parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="76682-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="76682-132">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="76682-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="76682-133">Tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** valige suvand **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="76682-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="76682-134">Sisestage vahekaardil **E-arvelduse teenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.</span><span class="sxs-lookup"><span data-stu-id="76682-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="76682-135">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="76682-135">Datacenter Azure geography</span></span> | <span data-ttu-id="76682-136">Teenuse lõpp-punkti URI</span><span class="sxs-lookup"><span data-stu-id="76682-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="76682-137">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="76682-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="76682-138">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="76682-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="76682-139">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="76682-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="76682-140">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="76682-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="76682-141">Veenduge, et välja **Rakenduse ID** väärtuseks oleks määratud **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="76682-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="76682-142">See väärtus ei muutu.</span><span class="sxs-lookup"><span data-stu-id="76682-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="76682-143">Sisestage väljale **LCS-i keskkonna ID** oma LCS-i tellimuse konto ID.</span><span class="sxs-lookup"><span data-stu-id="76682-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="76682-144">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="76682-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="76682-145">Võtmehoidla saladuse loomine</span><span class="sxs-lookup"><span data-stu-id="76682-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="76682-146">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="76682-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="76682-147">Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige **Elektroonilise arvelduse lisandmooduli** plaan.</span><span class="sxs-lookup"><span data-stu-id="76682-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="76682-148">Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Teenusekeskkond** ja seejärel valige **Võtmehoidla parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="76682-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="76682-149">Võtmehoidla saladuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="76682-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="76682-150">Sisestage väljale **Nimi** võtmehoidla saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="76682-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="76682-151">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="76682-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="76682-152">Kleepige väljale **Võtmehoidla URL** Azure'i võtmehoidlast saladus.</span><span class="sxs-lookup"><span data-stu-id="76682-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="76682-153">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="76682-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="76682-154">Salvestuskonto saladuse loomine</span><span class="sxs-lookup"><span data-stu-id="76682-154">Create Storage account secret</span></span>

1. <span data-ttu-id="76682-155">Minge **Süsteemihaldus** > **Seadistus** > **Võtme hoidla parameetritesse** ja valige võtme hoidla saladus.</span><span class="sxs-lookup"><span data-stu-id="76682-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="76682-156">Jaotises **Sertifikaadid** valige suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="76682-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="76682-157">Sisestage **Nimi** väljale ladustamiskonto saladuse nimi ja kirjeldus **Kirjeldus** väljale.</span><span class="sxs-lookup"><span data-stu-id="76682-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="76682-158">Tehke väljal **Tüüp** valik **Sertifikaat**.</span><span class="sxs-lookup"><span data-stu-id="76682-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="76682-159">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="76682-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="76682-160">Digitaalserdi saladuse loomine</span><span class="sxs-lookup"><span data-stu-id="76682-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="76682-161">Minge **Süsteemihaldus** > **Seadistus** > **Võtme hoidla parameetritesse** ja valige võtme hoidla saladus.</span><span class="sxs-lookup"><span data-stu-id="76682-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="76682-162">Jaotises **Sertifikaadid** valige suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="76682-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="76682-163">Sisestage **Nimi** väljale ladustamiskonto saladuse nimi ja kirjeldus **Kirjeldus** väljale.</span><span class="sxs-lookup"><span data-stu-id="76682-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="76682-164">Tehke väljal **Tüüp** valik **Sertifikaat**.</span><span class="sxs-lookup"><span data-stu-id="76682-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="76682-165">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="76682-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="76682-166">Elektroonilise arvelduse lisandmooduli keskkonna loomine</span><span class="sxs-lookup"><span data-stu-id="76682-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="76682-167">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="76682-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="76682-168">Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige **Elektroonilise arvelduse lisandmooduli** plaan.</span><span class="sxs-lookup"><span data-stu-id="76682-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="76682-169">Teenusekeskkonna loomine</span><span class="sxs-lookup"><span data-stu-id="76682-169">Create a service environment</span></span>

1. <span data-ttu-id="76682-170">Lehel **Keskkondade seadistused** valige toimingupaanil suvand **Teenusekeskkond**.</span><span class="sxs-lookup"><span data-stu-id="76682-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="76682-171">Valige uue teenusekeskkonna loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="76682-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="76682-172">Sisestage väljale **Nimi** e-arvelduse keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="76682-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="76682-173">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="76682-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="76682-174">Valige väljal **Salvestuskonto SAS-tõendi saladus** salvestuskonto juurdepääsu autentimiseks kasutatava serdi nimi.</span><span class="sxs-lookup"><span data-stu-id="76682-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="76682-175">Valige jaotises **Kasutajad** käsk **Lisa**, et lisada kasutaja, kellel on lubatud keskkonna kaudu elektroonilisi arveid edastada ning salvestuskontoga ühendus luua.</span><span class="sxs-lookup"><span data-stu-id="76682-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="76682-176">Sisestage väljale **Kasutaja ID** kasutaja pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="76682-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="76682-177">Sisestage väljale **E-post** kasutaja e-posti aadress.</span><span class="sxs-lookup"><span data-stu-id="76682-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="76682-178">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="76682-178">Select **Save**.</span></span>
8. <span data-ttu-id="76682-179">Kui teie riigi-/regioonipõhiste arvete puhul on digiallkirjade rakendamiseks vaja serdiahelat, valige toimingupaanil suvand **Võtmehoidla parameetrid** ja seejärel valige **Serdiahel** ning toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="76682-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="76682-180">Serdiahela loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="76682-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="76682-181">Sisestage väljale **Nimi** serdiahela nimi.</span><span class="sxs-lookup"><span data-stu-id="76682-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="76682-182">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="76682-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="76682-183">Valige jaotises **Serdid** käsk **Lisa**, et ahelale sert lisada.</span><span class="sxs-lookup"><span data-stu-id="76682-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="76682-184">Kasutage nuppu **Üles** või **Alla**, et ahelas serdi asukohta muuta.</span><span class="sxs-lookup"><span data-stu-id="76682-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="76682-185">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="76682-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="76682-186">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="76682-186">Close the page.</span></span>
9. <span data-ttu-id="76682-187">Valige lehe **Teenusekeskkond** toimingupaanil käsk **Avalda**, et keskkond pilves avaldada.</span><span class="sxs-lookup"><span data-stu-id="76682-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="76682-188">Välja **Olek** väärtuseks määratakse **Avaldatud**.</span><span class="sxs-lookup"><span data-stu-id="76682-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="76682-189">Ühendatud rakenduse loomine</span><span class="sxs-lookup"><span data-stu-id="76682-189">Create a connected application</span></span>

1. <span data-ttu-id="76682-190">Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Ühendatud rakendused**.</span><span class="sxs-lookup"><span data-stu-id="76682-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="76682-191">Valige ühendatud rakenduse loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="76682-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="76682-192">Sisestage väljale **Nimi** ühendatava rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="76682-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="76682-193">Sisestage väljale **Rakendus** ühendatava teenuse Finance ja Supply Chain Management keskkonna URL.</span><span class="sxs-lookup"><span data-stu-id="76682-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="76682-194">Sisestage väljale **Rentnik** ühendatava teenuse Finance ja Supply Chain Management keskkonna rentnik.</span><span class="sxs-lookup"><span data-stu-id="76682-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="76682-195">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="76682-195">Select **Save**.</span></span>
6. <span data-ttu-id="76682-196">Keskkonnaga lodud ühenduse testimiseks valige toimingupaanil käsk **Kontrolli ühendust**.</span><span class="sxs-lookup"><span data-stu-id="76682-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="76682-197">Seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="76682-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="76682-198">Ühendatud rakenduste keskkondadega linkimine</span><span class="sxs-lookup"><span data-stu-id="76682-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="76682-199">Valige lehel **Keskkondade seadistused** suvand **Uus**, et ühendatud rakendus keskkonnale määrata.</span><span class="sxs-lookup"><span data-stu-id="76682-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="76682-200">Valige väljal **Ühendatud rakendus** ühendatud rakendus.</span><span class="sxs-lookup"><span data-stu-id="76682-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="76682-201">Valige väljal **Teenusekeskkond** teenusekeskkond.</span><span class="sxs-lookup"><span data-stu-id="76682-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="76682-202">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="76682-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="76682-203">Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine teenustes Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="76682-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="76682-204">Elektroonilise arvelduse lisandmooduli integratsioonifunktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="76682-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="76682-205">Logige oma teenuse Finance või Supply Chain Management eksemplari sisse.</span><span class="sxs-lookup"><span data-stu-id="76682-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="76682-206">Otsige tööruumis **Funktsioonihaldus** üles funktsioon **Elektroonilise arvelduse lisandmooduli integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="76682-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="76682-207">Kui seda funktsiooni lehel ei kuvata, valige käsk **Kontrolli värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="76682-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="76682-208">Valige funktsioon ja seejärel valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="76682-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="76682-209">Teenuse lõpp-punkti URL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="76682-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="76682-210">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="76682-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="76682-211">Sisestage vahekaardil **Edastusteenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.</span><span class="sxs-lookup"><span data-stu-id="76682-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="76682-212">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="76682-212">Datacenter Azure geography</span></span> | <span data-ttu-id="76682-213">Teenuse lõpp-punkti URL</span><span class="sxs-lookup"><span data-stu-id="76682-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="76682-214">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="76682-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="76682-215">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="76682-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="76682-216">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="76682-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="76682-217">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="76682-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="76682-218">Sisestage väljale **Keskkond** elektroonilise arvelduse lisandmooduli keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="76682-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="76682-219">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="76682-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
