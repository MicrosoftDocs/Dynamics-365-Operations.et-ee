---
title: Common Data Service'i virtuaalüksuste konfigureerimine
description: Selles teemas kirjeldatakse virtuaalüksuste konfigureerimist rakenduse Dynamics 365 Human Resources jaoks. Looge ja värskendage olemasolevaid virtuaalüksusi ning analüüsige loodud ja saadaolevaid üksusi.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645597"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="d24b6-104">Common Data Service'i virtuaalüksuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d24b6-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d24b6-105">Dynamics 365 Human Resources on virtuaalne andmeallikas teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d24b6-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="d24b6-106">See pakub täielikke loomise, lugemise, värskendamise ja kustutamise (CRUD) toiminguid lahendustes Common Data Service ning Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="d24b6-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="d24b6-107">Virtuaalüksuste andmeid ei talletata teenuses Common Data Service, vaid rakenduse andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="d24b6-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="d24b6-108">Selleks, et lubada rakenduse Human Resources üksuste korral CRUD-toimingud teenuses Common Data Service, peate tegema üksused teenuses Common Data Service virtuaalüksustena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d24b6-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="d24b6-109">See võimaldab teil teha lahendustes Common Data Service ja Microsoft Power Platform CRUD-toiminguid andmetega, mis on rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d24b6-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="d24b6-110">Toimingute puhul toetatakse ka rakenduse Human Resources täielikku äriloogika kontrollimist, et tagada andmete terviklikkus andmete kirjutamisel üksustesse.</span><span class="sxs-lookup"><span data-stu-id="d24b6-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="d24b6-111">Rakenduses Human Resources saadaolevad virtuaalüksused</span><span class="sxs-lookup"><span data-stu-id="d24b6-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="d24b6-112">Kõik avatud andmeprotokolli (OData) üksused rakenduses Human Resources on saadaval virtuaalüksustena teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d24b6-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="d24b6-113">Need on saadaval ka rakenduses Power Platform.</span><span class="sxs-lookup"><span data-stu-id="d24b6-113">They're also available in Power Platform.</span></span> <span data-ttu-id="d24b6-114">Nüüd saate luua rakendusi ja kogemusi otse rakendusest Human Resources pärit andmetega, mille puhul saate kasutada kõiki CRUD-toiminguid ilma andmete kopeerimise või sünkroonimise vajaduseta teenusega Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d24b6-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="d24b6-115">Saate kasutada Power Appsi portaale, et luua väljapoole suunatud veebisaite, mis võimaldavad teha äritoimingute puhul rakenduses Human Resources koostööd.</span><span class="sxs-lookup"><span data-stu-id="d24b6-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="d24b6-116">Saate vaadata keskkonnas lubatud virtuaalüksuste loendit ja alustada üksustega tööd rakenduses [Power Apps](https://make.powerapps.com) lahenduses **Dynamics 365 HR-i virtuaalüksused**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR-i virtuaalüksused Power Appsis](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="d24b6-118">Virtuaal- ja tavaliste üksuste võrdlus</span><span class="sxs-lookup"><span data-stu-id="d24b6-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="d24b6-119">Rakenduse Human Resources virtuaalüksused pole samad, mis tavalised teenuse Common Data Service üksused, mis on loodud rakenduse Human Resources jaoks.</span><span class="sxs-lookup"><span data-stu-id="d24b6-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="d24b6-120">Rakenduse Human Resources tavalised üksused luuakse eraldi ja neid hallatakse lahenduses HCM Common teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d24b6-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="d24b6-121">Tavaliste üksuste puhul talletatakse andmed teenuses Common Data Service ja selle puhul on vajalik sünkroonimine rakenduse Human Resources andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="d24b6-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="d24b6-122">Rakenduse Human Resources jaoks mõeldud teenuse Common Data Service tavaliste üksuste loendi leiate teemast [Common Data Service'i üksused](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="d24b6-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="d24b6-123">Seadistus</span><span class="sxs-lookup"><span data-stu-id="d24b6-123">Setup</span></span>

<span data-ttu-id="d24b6-124">Järgige neid seadistussamme, et lubada oma keskkonnas virtuaalüksused.</span><span class="sxs-lookup"><span data-stu-id="d24b6-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="d24b6-125">Virtuaalüksuste lubamine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="d24b6-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="d24b6-126">Esmalt peate lubama tööruumi **Funktsioonihaldus** kaudu virtuaalüksused lubama.</span><span class="sxs-lookup"><span data-stu-id="d24b6-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="d24b6-127">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="d24b6-128">Valige paan **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="d24b6-129">Valige **Virtuaalüksuse tugi rakenduses HR/CDS** ja seejärel valige **Luba**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="d24b6-130">Lisateavet eelvaatefunktsioonide lubamise ja keelamise kohta vt jaotisest [Funktsioonide haldus](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="d24b6-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="d24b6-131">Rakenduse registreerimine Microsoft Azure'is</span><span class="sxs-lookup"><span data-stu-id="d24b6-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="d24b6-132">Peate Human Resourcesi eksemplari Azure'i portaalis registreerima, et Microsofti identiteediplatvorm saaks pakkuda rakenduse ja kasutajate jaoks autentimis- ning autoriseerimisteenuseid.</span><span class="sxs-lookup"><span data-stu-id="d24b6-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="d24b6-133">Lisateavet Azure'is rakenduste registreerimise kohta leiate teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteediplatvormis](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="d24b6-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="d24b6-134">Avage [Microsoft Azure'i portaal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="d24b6-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="d24b6-135">Valige Azure'i teenuste loendis **Rakenduste registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="d24b6-136">Valige **Uus registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-136">Select **New registration**.</span></span>

4. <span data-ttu-id="d24b6-137">Sisestage väljale **Nimi** rakendust kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="d24b6-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="d24b6-138">Näiteks **Dynamics 365 Human Resources'i virtuaalüksused**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="d24b6-139">Sisestage väljale **Ümbersuunamis-URI** oma rakenduse Human Resources eksemplari nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="d24b6-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="d24b6-140">Valige suvand **Registreeri**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-140">Select **Register**.</span></span>

7. <span data-ttu-id="d24b6-141">Registreerimise lõpetamisel kuvatakse Azure'i portaalis rakenduse registreerimise kohta paan **Ülevaade**, mis sisaldab väärtust **Rakenduse (kliendi) ID**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="d24b6-142">Kirjutage väärtus **Rakenduse (kliendi) ID** endale üles.</span><span class="sxs-lookup"><span data-stu-id="d24b6-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="d24b6-143">Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="d24b6-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="d24b6-144">Valige vasakpoolsel navigeerimispaanil **Serdid ja saladused**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="d24b6-145">Valige lehe jaotises **Klientrakenduse saladused** suvand **Uus klientrakenduse saladus**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="d24b6-146">Sisestage kirjeldus, valige kestus ja valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="d24b6-147">Kirjutage saladuse väärtus üles.</span><span class="sxs-lookup"><span data-stu-id="d24b6-147">Record the secret's value.</span></span> <span data-ttu-id="d24b6-148">Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="d24b6-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d24b6-149">Kirjutage saladuse väärtus kindlasti praegu üles.</span><span class="sxs-lookup"><span data-stu-id="d24b6-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="d24b6-150">Pärast sellelt lehelt lahkumist ei kuvata saladust enam kunagi.</span><span class="sxs-lookup"><span data-stu-id="d24b6-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="d24b6-151">Dynamics 365 HR Virtual Entity rakenduse installimine</span><span class="sxs-lookup"><span data-stu-id="d24b6-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="d24b6-152">Installige Dynamics 365 HR Virtual Entity rakendus oma Power Appsi keskkonda, et juurutada virtuaalüksuse lahenduse pakett teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d24b6-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="d24b6-153">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d24b6-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="d24b6-154">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="d24b6-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="d24b6-155">Valige lehe jaotises **Ressursid** suvand **Dynamics 365 rakendused**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="d24b6-156">Valige tegevus **Installi rakendus**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="d24b6-157">Valige **Dynamics 365 HR Virtual Entity** ja valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="d24b6-158">Vaadake teenusetingimused üle ja märkige, et te nõustute nendega.</span><span class="sxs-lookup"><span data-stu-id="d24b6-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="d24b6-159">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-159">Select **Install**.</span></span>

<span data-ttu-id="d24b6-160">Installimine võtab mõne minuti.</span><span class="sxs-lookup"><span data-stu-id="d24b6-160">The install takes a few minutes.</span></span> <span data-ttu-id="d24b6-161">Kui see on lõpule viidud, jätkake järgmiste sammudega.</span><span class="sxs-lookup"><span data-stu-id="d24b6-161">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Entity rakenduse installimine Power Platformi halduskeskusest](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="d24b6-163">Virtuaalüksuse andmeallika konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d24b6-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="d24b6-164">Järgmine samm on konfigureerida virtuaalüksuse andmeallikas Power Appsi keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="d24b6-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="d24b6-165">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d24b6-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="d24b6-166">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="d24b6-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="d24b6-167">Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="d24b6-168">Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub rakenduse lehe üleval paremal pool.</span><span class="sxs-lookup"><span data-stu-id="d24b6-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="d24b6-169">Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Finance and Operationsi virtuaalse andmeallika konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="d24b6-170">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-170">Select **Results**.</span></span>

7. <span data-ttu-id="d24b6-171">Valige kirje **Microsoft HR-i andmeallikas**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="d24b6-172">Sisestage andmeallika konfiguratsiooni jaoks vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="d24b6-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="d24b6-173">**Siht-URL**: teie rakenduse Human Resources nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="d24b6-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="d24b6-174">Siht-URL-i vorming on:</span><span class="sxs-lookup"><span data-stu-id="d24b6-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="d24b6-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="d24b6-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="d24b6-176">Näide:</span><span class="sxs-lookup"><span data-stu-id="d24b6-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="d24b6-177">Tõrketeate kuvamise välistamiseks lisage URL-i lõppu märk „**/**“.</span><span class="sxs-lookup"><span data-stu-id="d24b6-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="d24b6-178">**Rentniku ID**: Azure Active Directory (Azure AD) rentniku ID.</span><span class="sxs-lookup"><span data-stu-id="d24b6-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="d24b6-179">**AAD rakenduse ID**: rakenduse (kliendi) ID, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d24b6-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="d24b6-180">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="d24b6-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="d24b6-181">**AAD rakenduse saladus**: klientrakenduse saladus, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d24b6-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="d24b6-182">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="d24b6-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-i andmeallikas](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="d24b6-184">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="d24b6-185">Rakenduse õiguste andmine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="d24b6-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="d24b6-186">Andke rakenduses Human Resources õigused kahe Azure AD rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d24b6-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="d24b6-187">Rakendus, mis loodi teie rentniku jaoks Microsoft Azure'i portaalis</span><span class="sxs-lookup"><span data-stu-id="d24b6-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="d24b6-188">Dynamics 365 HR Virtual Entity rakendus, mis on installitud Power Appsi keskkonnas</span><span class="sxs-lookup"><span data-stu-id="d24b6-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="d24b6-189">Avage rakenduses Human Resources leht **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="d24b6-190">Valige uue rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="d24b6-191">Sisestage väljale **Kliendi ID** Microsoft Azure'i portaalis registreeritud rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="d24b6-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="d24b6-192">Sisestage väljale **Nimi** Microsoft Azure'i portaalis registreeritud rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="d24b6-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="d24b6-193">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="d24b6-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="d24b6-194">Valige teise rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="d24b6-195">**Kliendi ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="d24b6-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="d24b6-196">**Nimi**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="d24b6-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="d24b6-197">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="d24b6-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="d24b6-198">Virtuaalüksuste loomine</span><span class="sxs-lookup"><span data-stu-id="d24b6-198">Generate virtual entities</span></span>

<span data-ttu-id="d24b6-199">Kui seadistus on lõpule viidud, saate valida virtuaalüksused, mille soovite luua ja lubada oma Common Data Service'i eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="d24b6-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="d24b6-200">Avage rakenduses Human Resources leht **Common Data Service (CDS) integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="d24b6-201">Valige vahekaart **Virtuaalsed üksused**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="d24b6-202">Lüliti **Virtuaalse üksuse lubamine** olekuks seatakse automaatselt **Jah**, kui kogu nõutav seadistus on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="d24b6-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="d24b6-203">Kui lüliti olekuks on seatud **Ei**, vaadake läbi selle dokumendi eelmiste jaotiste etapid, et kogu eeltingimuste häälestus oleks lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="d24b6-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="d24b6-204">Valige üksus või üksused, mida soovite luua Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="d24b6-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="d24b6-205">Valige **Loo/värskenda**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-205">Select **Generate/refresh**.</span></span>

![Common Data Service’i integratsioon](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="d24b6-207">Üksuse loomise oleku kontrollimine</span><span class="sxs-lookup"><span data-stu-id="d24b6-207">Check entity generation status</span></span>

<span data-ttu-id="d24b6-208">Virtuaalseid üksusi luuakse Common Data Service'i asünkroonse taustal töötlemise abil.</span><span class="sxs-lookup"><span data-stu-id="d24b6-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="d24b6-209">Protsessi uuendusi kuvatakse tegevuskeskuses.</span><span class="sxs-lookup"><span data-stu-id="d24b6-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="d24b6-210">Protsessi üksikasju, sh tõrkelogisid, kuvatakse lehel **Protsessi automatiseerimised**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="d24b6-211">Avage rakenduses Human Resources loendi **Protsessi automatiseerimised** leht.</span><span class="sxs-lookup"><span data-stu-id="d24b6-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="d24b6-212">Valige vahekaart **Taustaprotsessid**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="d24b6-213">Valige **Virtuaalse üksuse pollimise asünkroonse toimingu taustaprotsess**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="d24b6-214">Valige **Kuva viimased tulemused**.</span><span class="sxs-lookup"><span data-stu-id="d24b6-214">Select **View most recent results**.</span></span>

<span data-ttu-id="d24b6-215">Liuguripaan kuvab protsessi kõige viimased käivitamise tulemused.</span><span class="sxs-lookup"><span data-stu-id="d24b6-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="d24b6-216">Saate kuvada protsessi logi, sh kõiki tagastatud tõrkeid Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="d24b6-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="d24b6-217">Vt ka</span><span class="sxs-lookup"><span data-stu-id="d24b6-217">See also</span></span>

[<span data-ttu-id="d24b6-218">Mis on Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="d24b6-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="d24b6-219">Üksuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="d24b6-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="d24b6-220">Üksuse seoste ülevaade</span><span class="sxs-lookup"><span data-stu-id="d24b6-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="d24b6-221">Välistest andmeallikatest pärit andmeid sisaldavate virtuaalüksuste loomine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="d24b6-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="d24b6-222">Mis on Power Appsi portaalid?</span><span class="sxs-lookup"><span data-stu-id="d24b6-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="d24b6-223">Rakenduste loomise ülevaade Power Appsis</span><span class="sxs-lookup"><span data-stu-id="d24b6-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
