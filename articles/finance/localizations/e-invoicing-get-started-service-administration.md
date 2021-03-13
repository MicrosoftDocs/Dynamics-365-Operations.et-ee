---
title: Elektroonilise arvelduse lisandmooduli teenuse halduse kasutamise alustamine
description: Selles teemas selgitatakse, kuidas elektroonilise arvelduse lisandmooduli kasutamist alustada.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104368"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="9e80f-103">Elektroonilise arvelduse lisandmooduli teenuse halduse kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="9e80f-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="9e80f-104">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="9e80f-104">Prerequisites</span></span>

<span data-ttu-id="9e80f-105">Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="9e80f-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="9e80f-106">Teil peab olema juurdepääs oma Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kontole.</span><span class="sxs-lookup"><span data-stu-id="9e80f-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="9e80f-107">Teil peab olema LCS-projekt, mis hõlmab Microsofti teenuste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management versiooni 10.0.13 või uuemat versiooni.</span><span class="sxs-lookup"><span data-stu-id="9e80f-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9e80f-108">Peale selle peavad need rakendused olema juurutatud ühes järgmistest Azure'i geograafilistest piirkondadest.</span><span class="sxs-lookup"><span data-stu-id="9e80f-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="9e80f-109">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="9e80f-109">East US</span></span>
    - <span data-ttu-id="9e80f-110">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="9e80f-110">West US</span></span>
    - <span data-ttu-id="9e80f-111">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="9e80f-111">North EU</span></span>
    - <span data-ttu-id="9e80f-112">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="9e80f-112">West EU</span></span>

- <span data-ttu-id="9e80f-113">Teil peab olema juurdepääs oma Dynamics 365 teenuse Regulatory Configuration Services (RCS) kontole.</span><span class="sxs-lookup"><span data-stu-id="9e80f-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="9e80f-114">Te peate mooduli Funktsioonihaldus kaudu oma RCS-i konto jaoks globaliseerimisfunktsiooni aktiveerima.</span><span class="sxs-lookup"><span data-stu-id="9e80f-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="9e80f-115">Lisateavet vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="9e80f-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="9e80f-116">Peate looma Azure'is võtmehoidla ja salvestamiskonto.</span><span class="sxs-lookup"><span data-stu-id="9e80f-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="9e80f-117">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="9e80f-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="9e80f-118">Teenuses Lifecycle Services mikroteenuste jaoks lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="9e80f-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="9e80f-119">Logige oma LCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="9e80f-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="9e80f-120">Valige paan **Eelvaate funktsiooni haldamine**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="9e80f-121">Valige jaotises **Avaliku eelvaateversiooni funktsioonid** suvand **E-arvelduse teenus**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="9e80f-122">Veenduge, et suvandi **Funktsiooni eelversioon on lubatud** väärtuseks oleks valitud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="9e80f-123">RCS-i elektroonilise arvelduse lisandmooduliga integratsiooni parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="9e80f-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="9e80f-124">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="9e80f-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9e80f-125">Tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** valige suvand **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="9e80f-126">Sisestage vahekaardil **E-arvelduse teenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.</span><span class="sxs-lookup"><span data-stu-id="9e80f-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="9e80f-127">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="9e80f-127">Datacenter Azure geography</span></span> | <span data-ttu-id="9e80f-128">Teenuse lõpp-punkti URI</span><span class="sxs-lookup"><span data-stu-id="9e80f-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9e80f-129">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="9e80f-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9e80f-130">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="9e80f-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9e80f-131">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="9e80f-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9e80f-132">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="9e80f-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="9e80f-133">Veenduge, et välja **Rakenduse ID** väärtuseks oleks määratud **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="9e80f-134">See väärtus ei muutu.</span><span class="sxs-lookup"><span data-stu-id="9e80f-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="9e80f-135">Sisestage väljale **LCS-i keskkonna ID** oma LCS-i tellimuse konto ID.</span><span class="sxs-lookup"><span data-stu-id="9e80f-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="9e80f-136">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="9e80f-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="9e80f-137">Võtmehoidla saladuse loomine</span><span class="sxs-lookup"><span data-stu-id="9e80f-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="9e80f-138">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="9e80f-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9e80f-139">Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkonnad** paan **E-arveldus**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="9e80f-140">Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Teenusekeskkond** ja seejärel valige **Võtmehoidla parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="9e80f-141">Võtmehoidla saladuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="9e80f-142">Sisestage väljale **Nimi** võtmehoidla saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="9e80f-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="9e80f-143">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9e80f-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="9e80f-144">Kleepige väljale **Võtmehoidla URL** Azure'i võtmehoidlast saladus.</span><span class="sxs-lookup"><span data-stu-id="9e80f-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="9e80f-145">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="9e80f-146">Salvestuskonto saladuse loomine</span><span class="sxs-lookup"><span data-stu-id="9e80f-146">Create Storage account secret</span></span>

1. <span data-ttu-id="9e80f-147">Valige lehe **Võtmehoidla parameetrid** jaotises **Sertifikaadid** käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="9e80f-148">Sisestage väljale **Nimi** sama salvestuskonto saladus.</span><span class="sxs-lookup"><span data-stu-id="9e80f-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="9e80f-149">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9e80f-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="9e80f-150">Tehke väljal **Tüüp** valik **Sertifikaat**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="9e80f-151">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="9e80f-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="9e80f-152">Elektroonilise arvelduse lisandmooduli keskkonna loomine</span><span class="sxs-lookup"><span data-stu-id="9e80f-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="9e80f-153">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="9e80f-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9e80f-154">Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkonnad** paan **E-arveldus**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="9e80f-155">Teenusekeskkonna loomine</span><span class="sxs-lookup"><span data-stu-id="9e80f-155">Create a service environment</span></span>

1. <span data-ttu-id="9e80f-156">Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Teenusekeskkond**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="9e80f-157">Valige uue teenusekeskkonna loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="9e80f-158">Sisestage väljale **Nimi** e-arvelduse keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="9e80f-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="9e80f-159">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9e80f-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="9e80f-160">Valige väljal **Salvestuskonto SAS-tõendi saladus** salvestuskonto juurdepääsu autentimiseks kasutatava serdi nimi.</span><span class="sxs-lookup"><span data-stu-id="9e80f-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="9e80f-161">Valige jaotises **Kasutajad** käsk **Lisa**, et lisada kasutaja, kellel on lubatud keskkonna kaudu elektroonilisi arveid edastada ning salvestuskontoga ühendus luua.</span><span class="sxs-lookup"><span data-stu-id="9e80f-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="9e80f-162">Sisestage väljale **Kasutaja ID** kasutaja pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="9e80f-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="9e80f-163">Sisestage väljale **E-post** kasutaja e-posti aadress.</span><span class="sxs-lookup"><span data-stu-id="9e80f-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="9e80f-164">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-164">Select **Save**.</span></span>
8. <span data-ttu-id="9e80f-165">Kui teie riigi-/regioonipõhiste arvete puhul on digiallkirjade rakendamiseks vaja serdiahelat, valige toimingupaanil suvand **Võtmehoidla parameetrid** ja seejärel valige **Serdiahel** ning toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9e80f-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="9e80f-166">Serdiahela loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="9e80f-167">Sisestage väljale **Nimi** serdiahela nimi.</span><span class="sxs-lookup"><span data-stu-id="9e80f-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="9e80f-168">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9e80f-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="9e80f-169">Valige jaotises **Serdid** käsk **Lisa**, et ahelale sert lisada.</span><span class="sxs-lookup"><span data-stu-id="9e80f-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="9e80f-170">Kasutage nuppu **Üles** või **Alla**, et ahelas serdi asukohta muuta.</span><span class="sxs-lookup"><span data-stu-id="9e80f-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="9e80f-171">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="9e80f-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="9e80f-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9e80f-172">Close the page.</span></span>
9. <span data-ttu-id="9e80f-173">Valige lehe **Teenusekeskkond** toimingupaanil käsk **Avalda**, et keskkond pilves avaldada.</span><span class="sxs-lookup"><span data-stu-id="9e80f-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="9e80f-174">Välja **Olek** väärtuseks määratakse **Avaldatud**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="9e80f-175">Ühendatud rakenduse loomine</span><span class="sxs-lookup"><span data-stu-id="9e80f-175">Create a connected application</span></span>

1. <span data-ttu-id="9e80f-176">Valige lehe **Keskkondade seadistused** toimingupaanil suvand **Ühendatud rakendused**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="9e80f-177">Valige ühendatud rakenduse loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="9e80f-178">Sisestage väljale **Nimi** ühendatava rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="9e80f-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="9e80f-179">Sisestage väljale **Rakendus** ühendatava teenuse Finance ja Supply Chain Management keskkonna URL.</span><span class="sxs-lookup"><span data-stu-id="9e80f-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="9e80f-180">Sisestage väljale **Rentnik** ühendatava teenuse Finance ja Supply Chain Management keskkonna rentnik.</span><span class="sxs-lookup"><span data-stu-id="9e80f-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="9e80f-181">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-181">Select **Save**.</span></span>
6. <span data-ttu-id="9e80f-182">Keskkonnaga lodud ühenduse testimiseks valige toimingupaanil käsk **Kontrolli ühendust**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="9e80f-183">Seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9e80f-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="9e80f-184">Ühendatud rakenduste keskkondadega linkimine</span><span class="sxs-lookup"><span data-stu-id="9e80f-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="9e80f-185">Valige lehel **Keskkondade seadistused** suvand **Uus**, et ühendatud rakendus keskkonnale määrata.</span><span class="sxs-lookup"><span data-stu-id="9e80f-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="9e80f-186">Valige väljal **Ühendatud rakendus** ühendatud rakendus.</span><span class="sxs-lookup"><span data-stu-id="9e80f-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="9e80f-187">Valige väljal **Teenusekeskkond** teenusekeskkond.</span><span class="sxs-lookup"><span data-stu-id="9e80f-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="9e80f-188">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="9e80f-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="9e80f-189">Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine teenustes Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9e80f-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="9e80f-190">Elektroonilise arvelduse lisandmooduli integratsioonifunktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="9e80f-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="9e80f-191">Logige oma teenuse Finance või Supply Chain Management eksemplari sisse.</span><span class="sxs-lookup"><span data-stu-id="9e80f-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="9e80f-192">Otsige tööruumis **Funktsioonihaldus** üles funktsioon **Elektroonilise arvelduse lisandmooduli integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="9e80f-193">Kui seda funktsiooni lehel ei kuvata, valige käsk **Kontrolli värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="9e80f-194">Valige funktsioon ja seejärel valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="9e80f-195">Teenuse lõpp-punkti URL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="9e80f-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="9e80f-196">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9e80f-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="9e80f-197">Sisestage vahekaardil **Edastusteenus** väljale **Teenuse lõpp-punkti URL** teie Azure'i geograafilise piirkonna jaoks sobiv teenuse lõpp-punkt, nagu järgmises tabelis näidatud.</span><span class="sxs-lookup"><span data-stu-id="9e80f-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="9e80f-198">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="9e80f-198">Datacenter Azure geography</span></span> | <span data-ttu-id="9e80f-199">Teenuse lõpp-punkti URL</span><span class="sxs-lookup"><span data-stu-id="9e80f-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9e80f-200">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="9e80f-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9e80f-201">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="9e80f-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9e80f-202">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="9e80f-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9e80f-203">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="9e80f-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="9e80f-204">Sisestage väljale **Keskkond** elektroonilise arvelduse lisandmooduli keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="9e80f-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="9e80f-205">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="9e80f-205">Select **Save**, and then close the page.</span></span>
