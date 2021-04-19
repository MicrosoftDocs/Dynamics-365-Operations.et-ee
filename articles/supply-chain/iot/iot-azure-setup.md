---
title: Azure'i ressursside seadistamine IoT iseõppimisvõime jaoks
description: Selles teemas selgitatakse, kuidas luua ja konfigureerida Microsoft Azure'i ressursse, mida vajate IoT iseõppimisvõime jaoks.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 722904aa75a9d95b99c83f39a1d79b9c796714b3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821101"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="eeec6-103">Azure'i ressursside seadistamine IoT iseõppimisvõime jaoks</span><span class="sxs-lookup"><span data-stu-id="eeec6-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eeec6-104">Selles teemas selgitatakse, kuidas luua ja konfigureerida Microsoft Azure'i ressursse, mida vajate IoT iseõppimisvõime jaoks.</span><span class="sxs-lookup"><span data-stu-id="eeec6-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="eeec6-105">Azure'i ressursside loomine</span><span class="sxs-lookup"><span data-stu-id="eeec6-105">Create Azure resources</span></span>

<span data-ttu-id="eeec6-106">Järgige neid juhiseid, et luua IoT-keskus, Redis-vahemälu ja võtmehoidla, millele pääseb juurde Microsoft Dynamics 365 Supply Chain Managementiga.</span><span class="sxs-lookup"><span data-stu-id="eeec6-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="eeec6-107">Kinnitage, et teie rentnikus on Microsoft Dynamics ERP mikroteenuste esimese osapoole rakenduse ID</span><span class="sxs-lookup"><span data-stu-id="eeec6-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="eeec6-108">Järgige neid juhiseid, et kinnitada, kas teie rentnikus on Microsoft Dynamics ERP mikroteenuste esimese osapoole rakenduse ID.</span><span class="sxs-lookup"><span data-stu-id="eeec6-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-109">Logige sisse Azure’i portaali lehel<https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="eeec6-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="eeec6-110">Avage **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="eeec6-111">Avage **Ettevõtte rakendused**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="eeec6-112">Valige väljal **Rakenduse tüüp** suvand **Microsofti rakendused**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="eeec6-113">Sisestage otsinguväljale **Microsoft Dynamics ERP mikroteenused**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="eeec6-114">Kinnitage, et loendis oleksid **Microsoft Dynamics ERP mikroteenused**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="eeec6-115">Teiste rakenduste nimed on sarnased.</span><span class="sxs-lookup"><span data-stu-id="eeec6-115">Other applications have similar names.</span></span> <span data-ttu-id="eeec6-116">Seetõttu veenduge, et leiaksite õige rakenduse.</span><span class="sxs-lookup"><span data-stu-id="eeec6-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="eeec6-117">Rakenduse ID on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="eeec6-118">Kui rakendust ei ole loendis, peate lisama selle oma rentnikusse.</span><span class="sxs-lookup"><span data-stu-id="eeec6-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="eeec6-119">Valige Azure'i portaali tööriistaribal nupp Azure Cloud Shelli avamiseks.</span><span class="sxs-lookup"><span data-stu-id="eeec6-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="eeec6-120">Käivitage käsk **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="eeec6-121">Sisestage mooduli installimiseks **Y**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="eeec6-122">Käivitage käsk **Get-InstalledModule -Name "AzureAD"**, et kinnitada, kas moodul on installitud.</span><span class="sxs-lookup"><span data-stu-id="eeec6-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="eeec6-123">Käivitage käsk **Connect-AzureAD -Confirm** autentimise käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="eeec6-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="eeec6-124">Käivitage käsk **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="eeec6-125">Saate nüüd korrata etappe 1–6, et kinnitada, kas rakenduse ID on teie rentnikus.</span><span class="sxs-lookup"><span data-stu-id="eeec6-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="eeec6-126">Võtmehoidla ressursi loomine</span><span class="sxs-lookup"><span data-stu-id="eeec6-126">Create a key vault resource</span></span>

<span data-ttu-id="eeec6-127">Võtmehoidla ressursi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eeec6-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-128">Looge või avage ressursi grupp Azure'i portaalis.</span><span class="sxs-lookup"><span data-stu-id="eeec6-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="eeec6-129">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-129">Select **Add**.</span></span>
3. <span data-ttu-id="eeec6-130">Sisestage lehel **Uus** otsinguväljale **Võtmehoidla**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="eeec6-131">Seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-131">Then select **Create**.</span></span>
4. <span data-ttu-id="eeec6-132">Sisestage lehel **Võtmehoidla loomine** nimi väljale **Võtmehoidla nimi**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="eeec6-133">Vaadake vaikeväärtused üle ja seejärel valige **Ülevaatamine ja loomine**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="eeec6-134">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-134">Select **Create**.</span></span>

<span data-ttu-id="eeec6-135">Võtmehoidla luuakse taustal.</span><span class="sxs-lookup"><span data-stu-id="eeec6-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="eeec6-136">IoT-keskuse ressursi loomine</span><span class="sxs-lookup"><span data-stu-id="eeec6-136">Create an IoT hub resource</span></span>

<span data-ttu-id="eeec6-137">IoT-keskuse ressursi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eeec6-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-138">Looge või avage ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="eeec6-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="eeec6-139">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-139">Select **Add**.</span></span>
3. <span data-ttu-id="eeec6-140">Sisestage lehel **Uus** otsinguväljale **IoT-keskus**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="eeec6-141">Seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-141">Then select **Create**.</span></span>
4. <span data-ttu-id="eeec6-142">Sisestage nimi väljale **IoT-keskuse nimi**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="eeec6-143">Vaadake vaikeväärtused üle ja seejärel valige **Ülevaatamine ja loomine**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="eeec6-144">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-144">Select **Create**.</span></span>

<span data-ttu-id="eeec6-145">IoT-keskus luuakse taustal.</span><span class="sxs-lookup"><span data-stu-id="eeec6-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="eeec6-146">Soovitame luua ainult ühe IoT-keskuse ressurssi keskkonna kohta.</span><span class="sxs-lookup"><span data-stu-id="eeec6-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="eeec6-147">Redis-vahemälu ressursi loomine</span><span class="sxs-lookup"><span data-stu-id="eeec6-147">Create a Redis cache resource</span></span>

<span data-ttu-id="eeec6-148">Redis-vahemälu ressursi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eeec6-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-149">Looge või avage ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="eeec6-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="eeec6-150">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-150">Select **Add**.</span></span>
3. <span data-ttu-id="eeec6-151">Sisestage lehel **Uus** otsinguväljale **Azure'i vahemälu Redise jaoks**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="eeec6-152">Seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-152">Then select **Create**.</span></span>
4. <span data-ttu-id="eeec6-153">Väljale **DNS-i nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="eeec6-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="eeec6-154">Vaadake vaikeväärtused üle ja seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="eeec6-155">Redis-vahemälu luuakse taustal.</span><span class="sxs-lookup"><span data-stu-id="eeec6-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="eeec6-156">Soovitame luua ainult ühe Redis-vahemälu ressurssi keskkonna kohta.</span><span class="sxs-lookup"><span data-stu-id="eeec6-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="eeec6-157">Kõik ressursid on nüüd loodud.</span><span class="sxs-lookup"><span data-stu-id="eeec6-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="eeec6-158">Azure'i ressursside konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="eeec6-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="eeec6-159">IoT-keskuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="eeec6-159">Configure the IoT hub</span></span>

<span data-ttu-id="eeec6-160">IoT-keskuse konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eeec6-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-161">Valige oma ressurssides IoT-keskuse ressurss.</span><span class="sxs-lookup"><span data-stu-id="eeec6-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="eeec6-162">Valige vasakpoolsel navigeerimispaanil **Sisseehitatud lõpp-punktid**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="eeec6-163">Kleepige jaotisesse **Tarbijagrupid** järgmised tarbijagrupid.</span><span class="sxs-lookup"><span data-stu-id="eeec6-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="eeec6-164">Need tarbijagrupid vastavad valmislahenduse stsenaariumidele.</span><span class="sxs-lookup"><span data-stu-id="eeec6-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="eeec6-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="eeec6-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="eeec6-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="eeec6-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="eeec6-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="eeec6-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="eeec6-168">Võtmehoidla konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="eeec6-168">Configure the key vault</span></span>

<span data-ttu-id="eeec6-169">Võtmehoidla konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eeec6-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-170">Valige oma ressurssides võtmehoidla ressurss.</span><span class="sxs-lookup"><span data-stu-id="eeec6-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="eeec6-171">Valige vasakpoolselt navigeerimispaanilt suvand **Juurdepääsupoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="eeec6-172">Valige **Lisa juurdepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="eeec6-173">Valige lehel **Lisa juurdepääsupoliitika** väljal **Salajased load** suvand **Hangi** ja **Loend**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="eeec6-174">Klõpsake suvandit **Subjekti valimine**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="eeec6-175">Otsige üles ja valige dialoogiboksis **Subjekt** suvand **Microsoft Dynamics ERP mikroteenused**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="eeec6-176">Seejärel valige **Vali**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-176">Then select **Select**.</span></span>
7. <span data-ttu-id="eeec6-177">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-177">Select **Add**.</span></span>
8. <span data-ttu-id="eeec6-178">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-178">Select **Save**.</span></span>

<span data-ttu-id="eeec6-179">Rakendusel on nüüd juurdepääs võtmehoidla saladustele.</span><span class="sxs-lookup"><span data-stu-id="eeec6-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="eeec6-180">IoT-keskuse ühenduse stringi saladuse salvestamine</span><span class="sxs-lookup"><span data-stu-id="eeec6-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="eeec6-181">IoT-keskuse ühenduse stringi saladuse salvestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="eeec6-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-182">Valige oma ressurssides IoT-keskuse ressurss.</span><span class="sxs-lookup"><span data-stu-id="eeec6-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="eeec6-183">Valige vasakpoolsel navigeerimispaanil **Sisseehitatud lõpp-punktid**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="eeec6-184">Kopeerige väärtus väljale **Sündmuste keskusega ühilduv lõpp-punkt**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="eeec6-185">Avage võtmehoidla ressurss.</span><span class="sxs-lookup"><span data-stu-id="eeec6-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="eeec6-186">Valige vasakpoolsel navigeerimispaanil suvand **Saladused**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="eeec6-187">Valige **Loo/impordi**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="eeec6-188">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="eeec6-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="eeec6-189">Kleepige väljale **Väärtus** lõpp-punkti väärtus, mille eelnevalt kopeerisite.</span><span class="sxs-lookup"><span data-stu-id="eeec6-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="eeec6-190">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="eeec6-191">Redis-vahemälu ühenduse stringi saladuse salvestamine</span><span class="sxs-lookup"><span data-stu-id="eeec6-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="eeec6-192">Redis-vahemälu ühenduse stringi saladuse salvestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="eeec6-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="eeec6-193">Valige oma ressurssides Redis-vahemälu ressurss.</span><span class="sxs-lookup"><span data-stu-id="eeec6-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="eeec6-194">Valige **Juurdepääsuvõtmed**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="eeec6-195">Kopeerige väärtus väljajalt **Peamine ühenduse string**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="eeec6-196">Avage võtmehoidla ressurss.</span><span class="sxs-lookup"><span data-stu-id="eeec6-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="eeec6-197">Valige vasakpoolsel navigeerimispaanil suvand **Saladused**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="eeec6-198">Valige **Loo/impordi**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="eeec6-199">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="eeec6-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="eeec6-200">Kleepige väljale **Väärtus** ühenduse string, mille eelnevalt kopeerisite.</span><span class="sxs-lookup"><span data-stu-id="eeec6-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="eeec6-201">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="eeec6-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="eeec6-202">Kui värskendate ühte neist ühenduse stringidest, peate värskendama ka salajasi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="eeec6-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="eeec6-203">Olete nüüd lõpetanud nõutavate Azure'i ressursside ettevalmistamise.</span><span class="sxs-lookup"><span data-stu-id="eeec6-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="eeec6-204">Järgmine etapp on [IoT iseõppimisvõime lisandmooduli installimine teenuses Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="eeec6-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]