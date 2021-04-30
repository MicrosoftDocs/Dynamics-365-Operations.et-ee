---
title: Üleminek osapoole ja globaalse aadressiraamatu mudelile
description: See teema kirjeldab, kuidas uuendada kahekirjutajalisi andmeid osalise ja globaalse aadressiraamatu mudelile.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857366"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="9f4c7-103">Üleminek osapoole ja globaalse aadressiraamatu mudelile</span><span class="sxs-lookup"><span data-stu-id="9f4c7-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9f4c7-104">[Azure'i andmetehase mall](https://aka.ms/dual-write-gab-adf) aitab teil täiendada olemasolevaid tabelite **Konto**, **Kontakt** ja **Hankija** andmeid kahekirjutamisel osapoole ja globaalse aadressiraamatu mudelile.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="9f4c7-105">Mall sobitab nii Finance and Operations rakenduste kui ka kliendikaasamise rakenduste andmed.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="9f4c7-106">Protsessi lõpus luuakse **osapoole** kirjete **osapoole**- ja **kontakti** väljad ning seostatakse need kliendikaasamise rakenduste kirjetega **Konto**, **Kontakt** ja **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="9f4c7-107">Finance and Operations rakenduses uute **osapoole** kirjete loomiseks luuakse .csv fail (`FONewParty.csv`). </span><span class="sxs-lookup"><span data-stu-id="9f4c7-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="9f4c7-108">Selles teemas on juhised malli Data Factory malli kasutamiseks ja andmete täiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="9f4c7-109">Kui teil kohandusi pole, saate malli kasutada nii, nagu see on.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="9f4c7-110">Kui teil on kohandusi kirjetes **Konto**, **Kontakt** ja **Hankija**, peate malli muutma järgmiste juhiste abil.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="9f4c7-111">Mall aitab uuendada ainult **osapoole** andmeid.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="9f4c7-112">Tulevases väljaandes lisatakse posti- ja elektroonilised aadressid.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9f4c7-113">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="9f4c7-113">Prerequisites</span></span>

<span data-ttu-id="9f4c7-114">Järgmised eeldused on vajalikud.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="9f4c7-115">Azure'i tellimus</span><span class="sxs-lookup"><span data-stu-id="9f4c7-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="9f4c7-116">Juurdepääs mallile</span><span class="sxs-lookup"><span data-stu-id="9f4c7-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="9f4c7-117">Olete olemasolev topeltkirjutamise klient.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="9f4c7-118">Täienduseks ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="9f4c7-119">**Täielikult sünkroonitud**: mõlemas keskkonnas on kirjed **Konto (klient)**, **Kontakt** ja **Hankija** täielikult sünkroonitud olekuga.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="9f4c7-120">**Integratsioonivõtmed**: kliendikaasamise rakenduste tabeleid **Konto (klient)**, **Kontakt** ja **Hankija** kasutavad väljaminekuks saadetud integratsioonivõtmeid.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="9f4c7-121">Kui kohandasite integratsioonivõtmeid, peate malli kohandama.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="9f4c7-122">**Osapoole number**: kõigil täiendamisele minevatel kirjetel **Konto (Klient)**, **Kontakt** ja **Hankija** on **osapoole number**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="9f4c7-123">**Osapoole** numbrita kirjeid ignoreeritakse.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="9f4c7-124">Kui soovite neid kirjeid täiendada, lisage neile enne täiendusprotsessi alustamist **osapoole** number.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="9f4c7-125">**Süsteemi katkestus**: versiooniuuendusprotsessi ajal peate kasutama nii Finance and Operations ja kliendikaasamise keskkondi võrguühenduseta.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="9f4c7-126">**Hetktõmmis**: tehke hetktõmmiseid nii klientide kaasamise kui ka Finance and Operations rakendustest.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="9f4c7-127">Kasutage vajadusel hetktõmmiseid eelmise oleku taastamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="9f4c7-128">Juurutamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-128">Deployment</span></span>

1. <span data-ttu-id="9f4c7-129">Laadige mall alla rakendusest [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="9f4c7-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="9f4c7-130">Logige sisse rakendusse [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="9f4c7-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="9f4c7-131">Looge [ressursigrupp](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="9f4c7-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="9f4c7-132">Looge loodud ressursirühmas [talletuskonto](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal).</span><span class="sxs-lookup"><span data-stu-id="9f4c7-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="9f4c7-133">Looge ülal loodud ressursirühmas [andmevabrik](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal).</span><span class="sxs-lookup"><span data-stu-id="9f4c7-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="9f4c7-134">Avage andmevabrik ja valige paan **Autor ja monitor**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="9f4c7-135">Klõpsake menüüs **Haldamine** nuppu **ARM-mall**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="9f4c7-136">**Osapoole** malli importimiseks valige **Impordi ARM mall**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="9f4c7-137">Importige mall andmevabrikusse.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-137">Import the template into the data factory.</span></span> <span data-ttu-id="9f4c7-138">Sisestage **projekti üksikasjade** ja **eksemplari üksikasjade** jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="9f4c7-139">Field</span><span class="sxs-lookup"><span data-stu-id="9f4c7-139">Field</span></span> | <span data-ttu-id="9f4c7-140">Väärtus</span><span class="sxs-lookup"><span data-stu-id="9f4c7-140">Value</span></span>
    ---|---
    <span data-ttu-id="9f4c7-141">Kordustellimus</span><span class="sxs-lookup"><span data-stu-id="9f4c7-141">Subscription</span></span> | <span data-ttu-id="9f4c7-142">Azure'i tellimus</span><span class="sxs-lookup"><span data-stu-id="9f4c7-142">Azure subscription</span></span>
    <span data-ttu-id="9f4c7-143">Ressursigrupp</span><span class="sxs-lookup"><span data-stu-id="9f4c7-143">Resource group</span></span> | <span data-ttu-id="9f4c7-144">Sisestage sama ressurss, mille all salvestusruumikonto luuakse.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="9f4c7-145">Regioon</span><span class="sxs-lookup"><span data-stu-id="9f4c7-145">Region</span></span> | <span data-ttu-id="9f4c7-146">Määrake piirkond.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-146">Specify region.</span></span>
    <span data-ttu-id="9f4c7-147">Vabriku nimi</span><span class="sxs-lookup"><span data-stu-id="9f4c7-147">Factory Name</span></span> | <span data-ttu-id="9f4c7-148">Määrake vabriku nimi.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-148">Specify factory name.</span></span>
    <span data-ttu-id="9f4c7-149">FO lingitud Service_service põhivõti</span><span class="sxs-lookup"><span data-stu-id="9f4c7-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="9f4c7-150">Määrake rakenduse võti.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-150">Specify the application's key.</span></span>
    <span data-ttu-id="9f4c7-151">Azure Blobi Storage_connection string</span><span class="sxs-lookup"><span data-stu-id="9f4c7-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="9f4c7-152">Azure Blobi hoidla ühenduse string.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="9f4c7-153">Dynamics Crm-iga lingitud Service_password</span><span class="sxs-lookup"><span data-stu-id="9f4c7-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="9f4c7-154">Kasutajanimeks määratud kasutajakonto parool.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="9f4c7-155">FO lingitud Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="9f4c7-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="9f4c7-156">FO lingitud Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="9f4c7-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="9f4c7-157">Määrake üürniku teave (domeeninimi või üürniku ID), mille all teie rakendus asub.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="9f4c7-158">FO lingitud Service_properties_type Properties_aad resursi ID</span><span class="sxs-lookup"><span data-stu-id="9f4c7-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="9f4c7-159">FO lingitud Service_properties_type Properties_service põhi-ID</span><span class="sxs-lookup"><span data-stu-id="9f4c7-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="9f4c7-160">Määrake rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="9f4c7-161">Dynamics Crm-iga lingitud Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="9f4c7-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="9f4c7-162">Kasutajanimi Dynamicsiga ühenduse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="9f4c7-163">Lisateavet leiate teemast [Ressursihalduri malli käsitsi reklaamimine iga keskkonna jaoks ](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Lingitud teenuse atribuudid ](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties)ja [Andmete kopeerimine Azure'i andmevabriku abil](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="9f4c7-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="9f4c7-164">Pärast juurutamist valideerige andmevabriku andmekogumid, andmevoog ja lingitud teenus.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Andmekogumid, andmevoog ja lingitud teenus](media/data-factory-validate.png)

11. <span data-ttu-id="9f4c7-166">Liikuge jaotisse **Haldamine**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-166">Navigate to **Manage**.</span></span> <span data-ttu-id="9f4c7-167">Valige jaotises **Ühendused** väärtus **Lingitud teenus**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="9f4c7-168">Valige **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="9f4c7-169">Sisestage vormil **Lingitud teenuse redigeerimine (Dynamics CRM)** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="9f4c7-170">Field</span><span class="sxs-lookup"><span data-stu-id="9f4c7-170">Field</span></span> | <span data-ttu-id="9f4c7-171">Väärtus</span><span class="sxs-lookup"><span data-stu-id="9f4c7-171">Value</span></span>
    ---|---
    <span data-ttu-id="9f4c7-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="9f4c7-172">Name</span></span> | <span data-ttu-id="9f4c7-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="9f4c7-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="9f4c7-174">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9f4c7-174">Description</span></span> | <span data-ttu-id="9f4c7-175">Lingitud teenused CRM-i eksemplariga ühenduse loomiseks olemite andmete toomiseks</span><span class="sxs-lookup"><span data-stu-id="9f4c7-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="9f4c7-176">Ühenduse loomine integratsiooni käitusaja kaudu</span><span class="sxs-lookup"><span data-stu-id="9f4c7-176">Connect via integration runtime</span></span> | <span data-ttu-id="9f4c7-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9f4c7-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="9f4c7-178">Juurutamistüüp</span><span class="sxs-lookup"><span data-stu-id="9f4c7-178">Deployment type</span></span> | <span data-ttu-id="9f4c7-179">Võrgus</span><span class="sxs-lookup"><span data-stu-id="9f4c7-179">Online</span></span>
    <span data-ttu-id="9f4c7-180">Teenuse Uri</span><span class="sxs-lookup"><span data-stu-id="9f4c7-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="9f4c7-181">Autentimise tüüp</span><span class="sxs-lookup"><span data-stu-id="9f4c7-181">Authentication type</span></span> | <span data-ttu-id="9f4c7-182">Office365</span><span class="sxs-lookup"><span data-stu-id="9f4c7-182">Office365</span></span>
    <span data-ttu-id="9f4c7-183">Kasutajanimi</span><span class="sxs-lookup"><span data-stu-id="9f4c7-183">User name</span></span> |
    <span data-ttu-id="9f4c7-184">Parool või Azure'i võtmehoidla</span><span class="sxs-lookup"><span data-stu-id="9f4c7-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="9f4c7-185">Parool</span><span class="sxs-lookup"><span data-stu-id="9f4c7-185">Password</span></span>
    <span data-ttu-id="9f4c7-186">Parool</span><span class="sxs-lookup"><span data-stu-id="9f4c7-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="9f4c7-187">Käitage mall</span><span class="sxs-lookup"><span data-stu-id="9f4c7-187">Run the template</span></span>

1. <span data-ttu-id="9f4c7-188">Finance and Operations rakenduse abil saate peatada järgmiste **konto**, **kontakti** ja **hankija** topeltkirjutamise.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="9f4c7-189">Kliendid V3 (kontod)</span><span class="sxs-lookup"><span data-stu-id="9f4c7-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="9f4c7-190">Kliendi V3 (kontaktid)</span><span class="sxs-lookup"><span data-stu-id="9f4c7-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="9f4c7-191">CDS'i kontakti V2 (kontaktid)</span><span class="sxs-lookup"><span data-stu-id="9f4c7-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="9f4c7-192">CDS'i kontakti V2 (kontaktid)</span><span class="sxs-lookup"><span data-stu-id="9f4c7-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="9f4c7-193">Hankija V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="9f4c7-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="9f4c7-194">Veenduge, et kaardid on Dataverse tabelist `msdy_dualwriteruntimeconfig` eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="9f4c7-195">Installige [kahekirjutajalised osapoole ja globaalse aadressiraamatu lahendused](https://aka.ms/dual-write-gab) AppSource rakendusest.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="9f4c7-196">Kui Finance and Operations rakenduses sisaldavad andmeid järgmised tabelid, käivitage nende jaoks **esmane sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="9f4c7-197">Tervitused</span><span class="sxs-lookup"><span data-stu-id="9f4c7-197">Salutations</span></span>
    + <span data-ttu-id="9f4c7-198">Isiklikud märgitüübid</span><span class="sxs-lookup"><span data-stu-id="9f4c7-198">Personal character types</span></span>
    + <span data-ttu-id="9f4c7-199">Viisakusväljend</span><span class="sxs-lookup"><span data-stu-id="9f4c7-199">Complimentary closing</span></span>
    + <span data-ttu-id="9f4c7-200">Kontaktisiku tiitlid</span><span class="sxs-lookup"><span data-stu-id="9f4c7-200">Contact person titles</span></span>
    + <span data-ttu-id="9f4c7-201">Otsustamisrollid</span><span class="sxs-lookup"><span data-stu-id="9f4c7-201">Decision making roles</span></span>
    + <span data-ttu-id="9f4c7-202">Püsikliendi tasemed</span><span class="sxs-lookup"><span data-stu-id="9f4c7-202">Loyalty levels</span></span>

5. <span data-ttu-id="9f4c7-203">Keelake kliendi kaasamise rakenduses järgmised plugina juhised.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="9f4c7-204">Konto uuendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-204">Account Update</span></span>
         + <span data-ttu-id="9f4c7-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="9f4c7-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="9f4c7-207">Kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-207">Contact Update</span></span>
         + <span data-ttu-id="9f4c7-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="9f4c7-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="9f4c7-210">msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-210">msdyn_party Update</span></span>
         + <span data-ttu-id="9f4c7-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="9f4c7-212">msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="9f4c7-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="9f4c7-214">Keelake kliendi kaasamise rakenduses järgmised töövood.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="9f4c7-215">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9f4c7-216">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9f4c7-217">Isiku tüübiga hankijate loomine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="9f4c7-218">Isiku tüübiga hankijate loomine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="9f4c7-219">Hankijate värskendamine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9f4c7-220">Hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="9f4c7-221">Isiku tüübiga hankijate värskendamine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="9f4c7-222">Isiku tüübiga hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="9f4c7-223">Käivitage mall andmevabrikus, valides käsu **Käivita kohe**, nagu on näidatud järgmisel pildil.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="9f4c7-224">Selle protsessi lõpuleviimiseks võib andmemahu põhjal kuluda mõni tund.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Päästiku käivitamine](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="9f4c7-226">Kui teil on kohandusi kirjetes **Konto**, **Kontakt** ja **Hankija**, peate malli muutma.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="9f4c7-227">Importige rakenduses Finance and Operations uued **osapoole** kirjed.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="9f4c7-228">Laadige `FONewParty.csv` fail alla Azure'i bloobimälust.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="9f4c7-229">Vorming on `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="9f4c7-230">Teisendage `FONewParty.csv` fail Exceli failiks ja importige Exceli fail Finance and Operations rakendusse.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="9f4c7-231">Kui CSV import töötab teie jaoks, saate importida CSV faili otse.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="9f4c7-232">Sõltuvalt andmemahust võib importimiseks kuluda mõni tund.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="9f4c7-233">Lisateavet vt [Andmete importimis- ja eksportimistööde ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span><span class="sxs-lookup"><span data-stu-id="9f4c7-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![Dataversi osapoole kirjete importimine](media/data-factory-import-party.png)

9. <span data-ttu-id="9f4c7-235">Lubage kliendi kaasamise rakenduses järgmised plugina juhised.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="9f4c7-236">Konto uuendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-236">Account Update</span></span>
         + <span data-ttu-id="9f4c7-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="9f4c7-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="9f4c7-239">Kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-239">Contact Update</span></span>
         + <span data-ttu-id="9f4c7-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="9f4c7-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="9f4c7-242">msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-242">msdyn_party Update</span></span>
         + <span data-ttu-id="9f4c7-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="9f4c7-244">msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="9f4c7-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="9f4c7-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="9f4c7-246">Aktiveerige kliendikaasamise rakendustes järgmised töövood, kui desaktiveerisite need eelmistes juhistes.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="9f4c7-247">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9f4c7-248">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9f4c7-249">Isiku tüübiga hankijate loomine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="9f4c7-250">Isiku tüübiga hankijate loomine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="9f4c7-251">Hankijate värskendamine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="9f4c7-252">Hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="9f4c7-253">Isiku tüübiga hankijate värskendamine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="9f4c7-254">Isiku tüübiga hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="9f4c7-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="9f4c7-255">Käivitage **osapoolega** seotud kaardid, nagu on juhendatud [osapoole- ja globaalses aadressiraamatus](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="9f4c7-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9f4c7-256">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="9f4c7-256">Troubleshooting</span></span>

1. <span data-ttu-id="9f4c7-257">Kui protsess ebaõnnestub, käivitage vabrik uuesti, alustades ebaõnnestunud tegevusest.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="9f4c7-258">Mõned failid loob andmevabrik, mida saate kasutada andmete valideerimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="9f4c7-259">Andmevabrik töötab komaeraldusega CSV-failide põhjal.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="9f4c7-260">Kui on välja väärtus, millel on koma, võib see tulemusi häirida.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="9f4c7-261">Te peate komad eemaldama.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="9f4c7-262">Vahekaart **Jälgimine** sisaldab teavet kõigi töödeldavate toimingute ja andmete kohta.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="9f4c7-263">Valige selle silumiseks kindel juhis.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-263">Select a specific step to debug it.</span></span>

    ![Vahekaart Jälgimine](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="9f4c7-265">Lisateave malli kohta</span><span class="sxs-lookup"><span data-stu-id="9f4c7-265">Learn more about the template</span></span>

<span data-ttu-id="9f4c7-266">Leiate [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) faili kohta kommentaare.</span><span class="sxs-lookup"><span data-stu-id="9f4c7-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>
