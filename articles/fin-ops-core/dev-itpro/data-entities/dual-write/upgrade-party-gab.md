---
title: Üleminek osapoole ja globaalse aadressiraamatu mudelile
description: See teema kirjeldab, kuidas uuendada kahekirjutajalisi andmeid osalise ja globaalse aadressiraamatu mudelile.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112669"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="d2580-103">Üleminek osapoole ja globaalse aadressiraamatu mudelile</span><span class="sxs-lookup"><span data-stu-id="d2580-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d2580-104">[Microsoft Azure Data Factory mall](https://aka.ms/dual-write-gab-adf) aitab teil täiendada olemasolevaid **Konto**, **Kontakt** ja **Hankija** tabeli andmeid kahekirjutamisel osapoole ja globaalse aadressiraamatu mudelile.</span><span class="sxs-lookup"><span data-stu-id="d2580-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="d2580-105">Mall sobitab nii reconciles rakenduste kui ka finance and operations ja customer engagement rakenduste andmed.</span><span class="sxs-lookup"><span data-stu-id="d2580-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="d2580-106">Protsessi lõpus luuakse **osapoole** kirjete **osapoole**- ja **kontakti** väljad ning seostatakse need kliendikaasamise rakenduste kirjetega **Konto**, **Kontakt** ja **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="d2580-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="d2580-107">.csv fail (`FONewParty.csv`) on loodud uue **Osapoole** kirjete loomiseks rakenduses finance and operations.</span><span class="sxs-lookup"><span data-stu-id="d2580-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="d2580-108">Selles teemas on juhised Data Factory malli kasutamiseks ja andmete täiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d2580-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="d2580-109">Kui teil kohandusi pole, saate malli kasutada nii, nagu see on.</span><span class="sxs-lookup"><span data-stu-id="d2580-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="d2580-110">Kui teil on kohandusi kirjetes **Konto**, **Kontakt** ja **Hankija**, peate malli muutma järgmiste juhiste abil.</span><span class="sxs-lookup"><span data-stu-id="d2580-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="d2580-111">Mall aitab uuendada ainult **Osapoole** andmeid.</span><span class="sxs-lookup"><span data-stu-id="d2580-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="d2580-112">Tulevases väljaandes lisatakse posti- ja elektroonilised aadressid.</span><span class="sxs-lookup"><span data-stu-id="d2580-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d2580-113">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="d2580-113">Prerequisites</span></span>

<span data-ttu-id="d2580-114">Osapoole ja globaalse aadressiraamatu mudeli täiendamiseks on nõutavad järgmised eeltingimused:</span><span class="sxs-lookup"><span data-stu-id="d2580-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="d2580-115">Azure'i tellimus</span><span class="sxs-lookup"><span data-stu-id="d2580-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="d2580-116">Juurdepääs mallile</span><span class="sxs-lookup"><span data-stu-id="d2580-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="d2580-117">Olete olemasolev topeltkirjutamise klient.</span><span class="sxs-lookup"><span data-stu-id="d2580-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="d2580-118">Täienduseks ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="d2580-118">Prepare for the upgrade</span></span>
<span data-ttu-id="d2580-119">Täienduse ettevalmistamiseks on tarvis järgmisi tegevusi:</span><span class="sxs-lookup"><span data-stu-id="d2580-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="d2580-120">**Täielikult sünkroonitud**: mõlemas keskkonnas on kirjed **Konto (klient)**, **Kontakt** ja **Hankija** täielikult sünkroonitud olekuga.</span><span class="sxs-lookup"><span data-stu-id="d2580-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="d2580-121">**Integratsioonivõtmed**: kliendikaasamise rakenduste tabeleid **Konto (klient)**, **Kontakt** ja **Hankija** kasutavad väljaminekuks saadetud integratsioonivõtmeid.</span><span class="sxs-lookup"><span data-stu-id="d2580-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="d2580-122">Kui kohandasite integratsioonivõtmeid, peate malli kohandama.</span><span class="sxs-lookup"><span data-stu-id="d2580-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="d2580-123">**Osapoole number**: kõigil täiendamisele minevatel kirjetel **Konto (Klient)**, **Kontakt** ja **Hankija** on **osapoole number**.</span><span class="sxs-lookup"><span data-stu-id="d2580-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="d2580-124">**Osapoole** numbrita kirjeid ignoreeritakse.</span><span class="sxs-lookup"><span data-stu-id="d2580-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="d2580-125">Kui soovite neid kirjeid täiendada, lisage neile enne täiendusprotsessi alustamist **osapoole** number.</span><span class="sxs-lookup"><span data-stu-id="d2580-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="d2580-126">**Süsteemi katkestus**: versiooniuuendusprotsessi ajal peate kasutama nii finance and operations kui customer engagement keskkondi võrguühenduseta.</span><span class="sxs-lookup"><span data-stu-id="d2580-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="d2580-127">**Hetktõmmis**: tehke hetktõmmiseid nii finance and operations rakenduses kui customer engagement rakenduses.</span><span class="sxs-lookup"><span data-stu-id="d2580-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="d2580-128">Kasutage vajadusel hetktõmmiseid eelmise oleku taastamiseks.</span><span class="sxs-lookup"><span data-stu-id="d2580-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="d2580-129">Juurutamine</span><span class="sxs-lookup"><span data-stu-id="d2580-129">Deployment</span></span>

1. <span data-ttu-id="d2580-130">Laadige mall alla rakendusest [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="d2580-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="d2580-131">Logige sisse rakendusse [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="d2580-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="d2580-132">Looge [ressursigrupp](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="d2580-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="d2580-133">Looge loodud ressursirühmas [talletuskonto](/azure/storage/common/storage-account-create?tabs=azure-portal).</span><span class="sxs-lookup"><span data-stu-id="d2580-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="d2580-134">Looge ülal loodud ressursirühmas [andmevabrik](/azure/data-factory/quickstart-create-data-factory-portal).</span><span class="sxs-lookup"><span data-stu-id="d2580-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="d2580-135">Avage andmevabrik ja valige paan **Autor ja monitor**.</span><span class="sxs-lookup"><span data-stu-id="d2580-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="d2580-136">Klõpsake menüüs **Haldamine** nuppu **ARM-mall**.</span><span class="sxs-lookup"><span data-stu-id="d2580-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="d2580-137">**Osapoole** malli importimiseks valige **Impordi ARM mall**.</span><span class="sxs-lookup"><span data-stu-id="d2580-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="d2580-138">Importige mall andmevabrikusse.</span><span class="sxs-lookup"><span data-stu-id="d2580-138">Import the template into the data factory.</span></span> <span data-ttu-id="d2580-139">Sisestage **projekti üksikasjade** ja **eksemplari üksikasjade** jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d2580-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="d2580-140">Field</span><span class="sxs-lookup"><span data-stu-id="d2580-140">Field</span></span> | <span data-ttu-id="d2580-141">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d2580-141">Value</span></span>
    ---|---
    <span data-ttu-id="d2580-142">Kordustellimus</span><span class="sxs-lookup"><span data-stu-id="d2580-142">Subscription</span></span> | <span data-ttu-id="d2580-143">Azure'i tellimus</span><span class="sxs-lookup"><span data-stu-id="d2580-143">Azure subscription</span></span>
    <span data-ttu-id="d2580-144">Ressursigrupp</span><span class="sxs-lookup"><span data-stu-id="d2580-144">Resource group</span></span> | <span data-ttu-id="d2580-145">Sisestage sama ressurss, mille all salvestusruumikonto luuakse.</span><span class="sxs-lookup"><span data-stu-id="d2580-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="d2580-146">Regioon</span><span class="sxs-lookup"><span data-stu-id="d2580-146">Region</span></span> | <span data-ttu-id="d2580-147">Määrake piirkond.</span><span class="sxs-lookup"><span data-stu-id="d2580-147">Specify region.</span></span>
    <span data-ttu-id="d2580-148">Vabriku nimi</span><span class="sxs-lookup"><span data-stu-id="d2580-148">Factory Name</span></span> | <span data-ttu-id="d2580-149">Määrake vabriku nimi.</span><span class="sxs-lookup"><span data-stu-id="d2580-149">Specify factory name.</span></span>
    <span data-ttu-id="d2580-150">FO lingitud Service_service põhivõti</span><span class="sxs-lookup"><span data-stu-id="d2580-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="d2580-151">Määrake rakenduse võti.</span><span class="sxs-lookup"><span data-stu-id="d2580-151">Specify the application's key.</span></span>
    <span data-ttu-id="d2580-152">Azure Blobi Storage_connection string</span><span class="sxs-lookup"><span data-stu-id="d2580-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="d2580-153">Azure Blobi hoidla ühenduse string.</span><span class="sxs-lookup"><span data-stu-id="d2580-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="d2580-154">Dynamics Crm-iga lingitud Service_password</span><span class="sxs-lookup"><span data-stu-id="d2580-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="d2580-155">Kasutajanimeks määratud kasutajakonto parool.</span><span class="sxs-lookup"><span data-stu-id="d2580-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="d2580-156">FO lingitud Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="d2580-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="d2580-157">FO lingitud Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="d2580-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="d2580-158">Määrake üürniku teave (domeeninimi või üürniku ID), mille all teie rakendus asub.</span><span class="sxs-lookup"><span data-stu-id="d2580-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="d2580-159">FO lingitud Service_properties_type Properties_aad resursi ID</span><span class="sxs-lookup"><span data-stu-id="d2580-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="d2580-160">FO lingitud Service_properties_type Properties_service põhi-ID</span><span class="sxs-lookup"><span data-stu-id="d2580-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="d2580-161">Määrake rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="d2580-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="d2580-162">Dynamics Crm-iga lingitud Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="d2580-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="d2580-163">Kasutajanimi ühenduse loomiseks rakenduses Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d2580-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="d2580-164">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="d2580-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="d2580-165">Kasutage Resource Manager malli iga keskkonna puhul käsitsi</span><span class="sxs-lookup"><span data-stu-id="d2580-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="d2580-166">Lingitud teenuse atribuudid</span><span class="sxs-lookup"><span data-stu-id="d2580-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="d2580-167">Andmete kopeerimine Azure Data Factory abil</span><span class="sxs-lookup"><span data-stu-id="d2580-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="d2580-168">Pärast juurutamist valideerige andmevabriku andmekogumid, andmevoog ja lingitud teenus.</span><span class="sxs-lookup"><span data-stu-id="d2580-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Andmekogumid, andmevoog ja lingitud teenus](media/data-factory-validate.png)

11. <span data-ttu-id="d2580-170">Liikuge jaotisse **Haldamine**.</span><span class="sxs-lookup"><span data-stu-id="d2580-170">Navigate to **Manage**.</span></span> <span data-ttu-id="d2580-171">Valige jaotises **Ühendused** väärtus **Lingitud teenus**.</span><span class="sxs-lookup"><span data-stu-id="d2580-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="d2580-172">Valige **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="d2580-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="d2580-173">Sisestage vormil **Lingitud teenuse redigeerimine (Dynamics CRM)** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d2580-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="d2580-174">Field</span><span class="sxs-lookup"><span data-stu-id="d2580-174">Field</span></span> | <span data-ttu-id="d2580-175">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d2580-175">Value</span></span>
    ---|---
    <span data-ttu-id="d2580-176">Nimi</span><span class="sxs-lookup"><span data-stu-id="d2580-176">Name</span></span> | <span data-ttu-id="d2580-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="d2580-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="d2580-178">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d2580-178">Description</span></span> | <span data-ttu-id="d2580-179">Lingitud teenused CRM-i eksemplariga ühenduse loomiseks olemite andmete toomiseks</span><span class="sxs-lookup"><span data-stu-id="d2580-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="d2580-180">Ühenduse loomine integratsiooni käitusaja kaudu</span><span class="sxs-lookup"><span data-stu-id="d2580-180">Connect via integration runtime</span></span> | <span data-ttu-id="d2580-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d2580-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="d2580-182">Juurutamistüüp</span><span class="sxs-lookup"><span data-stu-id="d2580-182">Deployment type</span></span> | <span data-ttu-id="d2580-183">Võrgus</span><span class="sxs-lookup"><span data-stu-id="d2580-183">Online</span></span>
    <span data-ttu-id="d2580-184">Teenuse Uri</span><span class="sxs-lookup"><span data-stu-id="d2580-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="d2580-185">Autentimise tüüp</span><span class="sxs-lookup"><span data-stu-id="d2580-185">Authentication type</span></span> | <span data-ttu-id="d2580-186">Office365</span><span class="sxs-lookup"><span data-stu-id="d2580-186">Office365</span></span>
    <span data-ttu-id="d2580-187">Kasutajanimi</span><span class="sxs-lookup"><span data-stu-id="d2580-187">User name</span></span> |
    <span data-ttu-id="d2580-188">Parool või Azure'i võtmehoidla</span><span class="sxs-lookup"><span data-stu-id="d2580-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="d2580-189">Parool</span><span class="sxs-lookup"><span data-stu-id="d2580-189">Password</span></span>
    <span data-ttu-id="d2580-190">Parool</span><span class="sxs-lookup"><span data-stu-id="d2580-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="d2580-191">Käitage mall</span><span class="sxs-lookup"><span data-stu-id="d2580-191">Run the template</span></span>

1. <span data-ttu-id="d2580-192">Rakenduse Finance and Operations abil saate peatada järgmiste kaartide **konto**, **kontakt** ja **hankija** topeltkirjutamise.</span><span class="sxs-lookup"><span data-stu-id="d2580-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="d2580-193">Kliendid V3 (kontod)</span><span class="sxs-lookup"><span data-stu-id="d2580-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="d2580-194">Kliendi V3 (kontaktid)</span><span class="sxs-lookup"><span data-stu-id="d2580-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="d2580-195">CDS'i kontakti V2 (kontaktid)</span><span class="sxs-lookup"><span data-stu-id="d2580-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="d2580-196">CDS'i kontakti V2 (kontaktid)</span><span class="sxs-lookup"><span data-stu-id="d2580-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="d2580-197">Hankija V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="d2580-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="d2580-198">Veenduge, et kaardid on Dataverse tabelist `msdy_dualwriteruntimeconfig` eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="d2580-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="d2580-199">Installige [kahekirjutajalised osapoole ja globaalse aadressiraamatu lahendused](https://aka.ms/dual-write-gab) AppSource rakendusest.</span><span class="sxs-lookup"><span data-stu-id="d2580-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="d2580-200">Rakenduses finance and operations sisaldavad andmeid järgmised tabelid, käivitage nende jaoks **esmane sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="d2580-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="d2580-201">Tervitused</span><span class="sxs-lookup"><span data-stu-id="d2580-201">Salutations</span></span>
    + <span data-ttu-id="d2580-202">Isiklikud märgitüübid</span><span class="sxs-lookup"><span data-stu-id="d2580-202">Personal character types</span></span>
    + <span data-ttu-id="d2580-203">Viisakusväljend</span><span class="sxs-lookup"><span data-stu-id="d2580-203">Complimentary closing</span></span>
    + <span data-ttu-id="d2580-204">Kontaktisiku tiitlid</span><span class="sxs-lookup"><span data-stu-id="d2580-204">Contact person titles</span></span>
    + <span data-ttu-id="d2580-205">Otsustamisrollid</span><span class="sxs-lookup"><span data-stu-id="d2580-205">Decision making roles</span></span>
    + <span data-ttu-id="d2580-206">Püsikliendi tasemed</span><span class="sxs-lookup"><span data-stu-id="d2580-206">Loyalty levels</span></span>

5. <span data-ttu-id="d2580-207">Keelake customer engagement rakenduses järgmised plugina juhised.</span><span class="sxs-lookup"><span data-stu-id="d2580-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="d2580-208">Konto uuendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-208">Account Update</span></span>
         + <span data-ttu-id="d2580-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="d2580-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="d2580-211">Kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-211">Contact Update</span></span>
         + <span data-ttu-id="d2580-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="d2580-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="d2580-214">msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-214">msdyn_party Update</span></span>
         + <span data-ttu-id="d2580-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="d2580-216">msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="d2580-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="d2580-218">Keelake kliendi kaasamise rakenduses järgmised töövood.</span><span class="sxs-lookup"><span data-stu-id="d2580-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="d2580-219">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d2580-220">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d2580-221">Isiku tüübiga hankijate loomine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="d2580-222">Isiku tüübiga hankijate loomine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="d2580-223">Hankijate värskendamine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d2580-224">Hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="d2580-225">Isiku tüübiga hankijate värskendamine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="d2580-226">Isiku tüübiga hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="d2580-227">Käivitage mall andmevabrikus, valides käsu **Käivita kohe**, nagu on näidatud järgmisel pildil.</span><span class="sxs-lookup"><span data-stu-id="d2580-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="d2580-228">Selle protsessi lõpuleviimiseks võib andmemahu põhjal kuluda mõni tund.</span><span class="sxs-lookup"><span data-stu-id="d2580-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Päästiku käivitamine](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="d2580-230">Kui teil on kohandusi kirjetes **Konto**, **Kontakt** ja **Hankija**, peate malli muutma.</span><span class="sxs-lookup"><span data-stu-id="d2580-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="d2580-231">Importige rakenduses Finance and Operations uued **osapoole** kirjed.</span><span class="sxs-lookup"><span data-stu-id="d2580-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="d2580-232">Laadige `FONewParty.csv` fail alla Azure'i bloobimälust.</span><span class="sxs-lookup"><span data-stu-id="d2580-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="d2580-233">Vorming on `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="d2580-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="d2580-234">Teisendage `FONewParty.csv` fail Exceli failiks ja importige Exceli fail finance and operations rakendusse.</span><span class="sxs-lookup"><span data-stu-id="d2580-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="d2580-235">Kui cvs import teie jaoks töötab, saate importida csv faili otse.</span><span class="sxs-lookup"><span data-stu-id="d2580-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="d2580-236">Sõltuvalt andmemahust võib importimiseks kuluda mõni tund.</span><span class="sxs-lookup"><span data-stu-id="d2580-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="d2580-237">Lisateavet vt [Andmete importimis- ja eksportimistööde ülevaade](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="d2580-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Dataversi osapoole kirjete importimine](media/data-factory-import-party.png)

9. <span data-ttu-id="d2580-239">Lubage customer engagement rakenduses järgmised plugina juhised:</span><span class="sxs-lookup"><span data-stu-id="d2580-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="d2580-240">Konto uuendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-240">Account Update</span></span>
         + <span data-ttu-id="d2580-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="d2580-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konto värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="d2580-243">Kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-243">Contact Update</span></span>
         + <span data-ttu-id="d2580-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="d2580-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontakti värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="d2580-246">msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-246">msdyn_party Update</span></span>
         + <span data-ttu-id="d2580-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="d2580-248">msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="d2580-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor värskendamine</span><span class="sxs-lookup"><span data-stu-id="d2580-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="d2580-250">Aktiveerige kliendikaasamise rakendustes järgmised töövood, kui desaktiveerisite need eelmistes juhistes.</span><span class="sxs-lookup"><span data-stu-id="d2580-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="d2580-251">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d2580-252">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d2580-253">Isiku tüübiga hankijate loomine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="d2580-254">Isiku tüübiga hankijate loomine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="d2580-255">Hankijate värskendamine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="d2580-256">Hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="d2580-257">Isiku tüübiga hankijate värskendamine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="d2580-258">Isiku tüübiga hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="d2580-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="d2580-259">Käivitage **osapoolega** seotud kaardid, nagu on juhendatud [osapoole- ja globaalses aadressiraamatus](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="d2580-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d2580-260">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="d2580-260">Troubleshooting</span></span>

1. <span data-ttu-id="d2580-261">Kui protsess ebaõnnestub, käivitage andmevabrik uuesti, alustades ebaõnnestunud tegevusest.</span><span class="sxs-lookup"><span data-stu-id="d2580-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="d2580-262">Mõned failid loob andmevabrik, mida saate kasutada andmete valideerimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="d2580-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="d2580-263">Andmevabrik töötab komaeraldusega CSV-failide põhjal.</span><span class="sxs-lookup"><span data-stu-id="d2580-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="d2580-264">Kui on välja väärtus, millel on koma, võib see tulemusi häirida.</span><span class="sxs-lookup"><span data-stu-id="d2580-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="d2580-265">Te peate komad eemaldama.</span><span class="sxs-lookup"><span data-stu-id="d2580-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="d2580-266">Vahekaart **Jälgimine** sisaldab teavet kõigi töödeldavate toimingute ja andmete kohta.</span><span class="sxs-lookup"><span data-stu-id="d2580-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="d2580-267">Valige selle silumiseks kindel juhis.</span><span class="sxs-lookup"><span data-stu-id="d2580-267">Select a specific step to debug it.</span></span>

    ![Vahekaart Jälgimine](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="d2580-269">Lisateave malli kohta</span><span class="sxs-lookup"><span data-stu-id="d2580-269">Learn more about the template</span></span>

<span data-ttu-id="d2580-270">Malli kohta leiate lisateavet [Kommentaarid Azure Data Factory malli lugemise kohta](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="d2580-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
