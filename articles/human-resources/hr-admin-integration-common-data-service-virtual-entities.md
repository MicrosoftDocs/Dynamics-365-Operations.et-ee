---
title: Common Data Service'i virtuaalüksuste konfigureerimine
description: Selles teemas kirjeldatakse virtuaalüksuste konfigureerimist rakenduse Dynamics 365 Human Resources jaoks. Looge ja värskendage olemasolevaid virtuaalüksusi ning analüüsige loodud ja saadaolevaid üksusi.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
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
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058150"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="beb2d-104">Common Data Service'i virtuaalüksuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="beb2d-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="beb2d-105">Dynamics 365 Human Resources on virtuaalne andmeallikas teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="beb2d-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="beb2d-106">See pakub täielikke loomise, lugemise, värskendamise ja kustutamise (CRUD) toiminguid lahendustes Common Data Service ning Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="beb2d-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="beb2d-107">Virtuaalüksuste andmeid ei talletata teenuses Common Data Service, vaid rakenduse andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="beb2d-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="beb2d-108">Selleks, et lubada rakenduse Human Resources üksuste korral CRUD-toimingud teenuses Common Data Service, peate tegema üksused teenuses Common Data Service virtuaalüksustena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="beb2d-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="beb2d-109">See võimaldab teil teha lahendustes Common Data Service ja Microsoft Power Platform CRUD-toiminguid andmetega, mis on rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="beb2d-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="beb2d-110">Toimingute puhul toetatakse ka rakenduse Human Resources täielikku äriloogika kontrollimist, et tagada andmete terviklikkus andmete kirjutamisel üksustesse.</span><span class="sxs-lookup"><span data-stu-id="beb2d-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="beb2d-111">Rakenduses Human Resources saadaolevad virtuaalüksused</span><span class="sxs-lookup"><span data-stu-id="beb2d-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="beb2d-112">Kõik avatud andmeprotokolli (OData) üksused rakenduses Human Resources on saadaval virtuaalüksustena teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="beb2d-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="beb2d-113">Need on saadaval ka rakenduses Power Platform.</span><span class="sxs-lookup"><span data-stu-id="beb2d-113">They're also available in Power Platform.</span></span> <span data-ttu-id="beb2d-114">Nüüd saate luua rakendusi ja kogemusi otse rakendusest Human Resources pärit andmetega, mille puhul saate kasutada kõiki CRUD-toiminguid ilma andmete kopeerimise või sünkroonimise vajaduseta teenusega Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="beb2d-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="beb2d-115">Saate kasutada Power Appsi portaale, et luua väljapoole suunatud veebisaite, mis võimaldavad teha äritoimingute puhul rakenduses Human Resources koostööd.</span><span class="sxs-lookup"><span data-stu-id="beb2d-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="beb2d-116">Saate vaadata keskkonnas lubatud virtuaalüksuste loendit ja alustada üksustega tööd rakenduses [Power Apps](https://make.powerapps.com) lahenduses **Dynamics 365 HR-i virtuaalüksused**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR-i virtuaalüksused Power Appsis](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="beb2d-118">Virtuaal- ja tavaliste üksuste võrdlus</span><span class="sxs-lookup"><span data-stu-id="beb2d-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="beb2d-119">Rakenduse Human Resources virtuaalüksused pole samad, mis tavalised teenuse Common Data Service üksused, mis on loodud rakenduse Human Resources jaoks.</span><span class="sxs-lookup"><span data-stu-id="beb2d-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="beb2d-120">Rakenduse Human Resources tavalised üksused luuakse eraldi ja neid hallatakse lahenduses HCM Common teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="beb2d-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="beb2d-121">Tavaliste üksuste puhul talletatakse andmed teenuses Common Data Service ja selle puhul on vajalik sünkroonimine rakenduse Human Resources andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="beb2d-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="beb2d-122">Rakenduse Human Resources jaoks mõeldud teenuse Common Data Service tavaliste üksuste loendi leiate teemast [Common Data Service'i üksused](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="beb2d-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="beb2d-123">Seadistus</span><span class="sxs-lookup"><span data-stu-id="beb2d-123">Setup</span></span>

<span data-ttu-id="beb2d-124">Järgige neid seadistussamme, et lubada oma keskkonnas virtuaalüksused.</span><span class="sxs-lookup"><span data-stu-id="beb2d-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="beb2d-125">Rakenduse registreerimine Microsoft Azure'is</span><span class="sxs-lookup"><span data-stu-id="beb2d-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="beb2d-126">Esmalt peate rakenduse Azure'i portaalis registreerima, et Microsofti identiteediplatvorm saaks pakkuda rakenduse ja kasutajate jaoks autentimis- ning autoriseerimisteenuseid.</span><span class="sxs-lookup"><span data-stu-id="beb2d-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="beb2d-127">Lisateavet Azure'is rakenduste registreerimise kohta leiate teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteediplatvormis](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="beb2d-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="beb2d-128">Avage [Microsoft Azure'i portaal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="beb2d-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="beb2d-129">Valige Azure'i teenuste loendis **Rakenduste registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="beb2d-130">Valige **Uus registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-130">Select **New registration**.</span></span>

4. <span data-ttu-id="beb2d-131">Sisestage väljale **Nimi** rakendust kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="beb2d-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="beb2d-132">Näiteks **Dynamics 365 Human Resources'i virtuaalüksused**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="beb2d-133">Sisestage väljale **Ümbersuunamis-URI** oma rakenduse Human Resources eksemplari nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="beb2d-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="beb2d-134">Valige suvand **Registreeri**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-134">Select **Register**.</span></span>

7. <span data-ttu-id="beb2d-135">Registreerimise lõpetamisel kuvatakse Azure'i portaalis rakenduse registreerimise kohta paan **Ülevaade** , mis sisaldab väärtust **Rakenduse (kliendi) ID**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="beb2d-136">Kirjutage väärtus **Rakenduse (kliendi) ID** endale üles.</span><span class="sxs-lookup"><span data-stu-id="beb2d-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="beb2d-137">Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="beb2d-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="beb2d-138">Valige vasakpoolsel navigeerimispaanil **Serdid ja saladused**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="beb2d-139">Valige lehe jaotises **Klientrakenduse saladused** suvand **Uus klientrakenduse saladus**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="beb2d-140">Sisestage kirjeldus, valige kestus ja valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="beb2d-141">Kirjutage saladuse väärtus üles.</span><span class="sxs-lookup"><span data-stu-id="beb2d-141">Record the secret's value.</span></span> <span data-ttu-id="beb2d-142">Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="beb2d-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="beb2d-143">Kirjutage saladuse väärtus kindlasti praegu üles.</span><span class="sxs-lookup"><span data-stu-id="beb2d-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="beb2d-144">Pärast sellelt lehelt lahkumist ei kuvata saladust enam kunagi.</span><span class="sxs-lookup"><span data-stu-id="beb2d-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="beb2d-145">Dynamics 365 HR Virtual Entity rakenduse installimine</span><span class="sxs-lookup"><span data-stu-id="beb2d-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="beb2d-146">Installige Dynamics 365 HR Virtual Entity rakendus oma Power Appsi keskkonda, et juurutada virtuaalüksuse lahenduse pakett teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="beb2d-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="beb2d-147">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="beb2d-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="beb2d-148">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="beb2d-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="beb2d-149">Valige lehe jaotises **Ressursid** suvand **Dynamics 365 rakendused**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="beb2d-150">Valige tegevus **Installi rakendus**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="beb2d-151">Valige **Dynamics 365 HR Virtual Entity** ja valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="beb2d-152">Vaadake teenusetingimused üle ja märkige, et te nõustute nendega.</span><span class="sxs-lookup"><span data-stu-id="beb2d-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="beb2d-153">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-153">Select **Install**.</span></span>

<span data-ttu-id="beb2d-154">Installimine võtab mõne minuti.</span><span class="sxs-lookup"><span data-stu-id="beb2d-154">The install takes a few minutes.</span></span> <span data-ttu-id="beb2d-155">Kui see on lõpule viidud, jätkake järgmiste sammudega.</span><span class="sxs-lookup"><span data-stu-id="beb2d-155">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Entity rakenduse installimine Power Platformi halduskeskusest](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="beb2d-157">Virtuaalüksuse andmeallika konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="beb2d-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="beb2d-158">Järgmine samm on konfigureerida virtuaalüksuse andmeallikas Power Appsi keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="beb2d-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="beb2d-159">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="beb2d-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="beb2d-160">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="beb2d-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="beb2d-161">Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="beb2d-162">Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub rakenduse lehe üleval paremal pool.</span><span class="sxs-lookup"><span data-stu-id="beb2d-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="beb2d-163">Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Finance and Operationsi virtuaalse andmeallika konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="beb2d-164">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-164">Select **Results**.</span></span>

7. <span data-ttu-id="beb2d-165">Valige kirje **Microsoft HR-i andmeallikas**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="beb2d-166">Sisestage andmeallika konfiguratsiooni jaoks vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="beb2d-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="beb2d-167">**Siht-URL** : teie rakenduse Human Resources nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="beb2d-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="beb2d-168">**Rentniku ID** : Azure Active Directory (Azure AD) rentniku ID.</span><span class="sxs-lookup"><span data-stu-id="beb2d-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="beb2d-169">**AAD rakenduse ID** : rakenduse (kliendi) ID, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="beb2d-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="beb2d-170">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="beb2d-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="beb2d-171">**AAD rakenduse saladus** : klientrakenduse saladus, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="beb2d-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="beb2d-172">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="beb2d-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="beb2d-173">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-173">Select **Save & Close**.</span></span>

   ![Microsoft HR-i andmeallikas](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="beb2d-175">Rakenduse õiguste andmine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="beb2d-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="beb2d-176">Andke rakenduses Human Resources õigused kahe Azure AD rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="beb2d-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="beb2d-177">Rakendus, mis loodi teie rentniku jaoks Microsoft Azure'i portaalis</span><span class="sxs-lookup"><span data-stu-id="beb2d-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="beb2d-178">Dynamics 365 HR Virtual Entity rakendus, mis on installitud Power Appsi keskkonnas</span><span class="sxs-lookup"><span data-stu-id="beb2d-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="beb2d-179">Avage rakenduses Human Resources leht **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="beb2d-180">Valige uue rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="beb2d-181">Sisestage väljale **Kliendi ID** Microsoft Azure'i portaalis registreeritud rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="beb2d-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="beb2d-182">Sisestage väljale **Nimi** Microsoft Azure'i portaalis registreeritud rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="beb2d-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="beb2d-183">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="beb2d-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="beb2d-184">Valige teise rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="beb2d-185">**Kliendi ID** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="beb2d-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="beb2d-186">**Nimi** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="beb2d-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="beb2d-187">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="beb2d-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="beb2d-188">Virtuaalüksuste loomine</span><span class="sxs-lookup"><span data-stu-id="beb2d-188">Generate virtual entities</span></span>

<span data-ttu-id="beb2d-189">Kui seadistus on lõpule viidud, saate valida virtuaalüksused, mille soovite luua ja lubada oma Common Data Service'i eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="beb2d-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="beb2d-190">Avage rakenduses Human Resources leht **Common Data Service (CDS) integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="beb2d-191">Valige vahekaart **Virtuaalsed üksused**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="beb2d-192">Lüliti **Virtuaalse üksuse lubamine** olekuks seatakse automaatselt **Jah** , kui kogu nõutav seadistus on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="beb2d-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="beb2d-193">Kui lüliti olekuks on seatud **Ei** , vaadake läbi selle dokumendi eelmiste jaotiste etapid, et kogu eeltingimuste häälestus oleks lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="beb2d-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="beb2d-194">Valige üksus või üksused, mida soovite luua Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="beb2d-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="beb2d-195">Valige **Loo/värskenda**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-195">Select **Generate/refresh**.</span></span>

![Common Data Service’i integratsioon](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="beb2d-197">Üksuse loomise oleku kontrollimine</span><span class="sxs-lookup"><span data-stu-id="beb2d-197">Check entity generation status</span></span>

<span data-ttu-id="beb2d-198">Virtuaalseid üksusi luuakse Common Data Service'i asünkroonse taustal töötlemise abil.</span><span class="sxs-lookup"><span data-stu-id="beb2d-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="beb2d-199">Protsessi uuendusi kuvatakse tegevuskeskuses.</span><span class="sxs-lookup"><span data-stu-id="beb2d-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="beb2d-200">Protsessi üksikasju, sh tõrkelogisid, kuvatakse lehel **Protsessi automatiseerimised**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="beb2d-201">Avage rakenduses Human Resources loendi **Protsessi automatiseerimised** leht.</span><span class="sxs-lookup"><span data-stu-id="beb2d-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="beb2d-202">Valige vahekaart **Taustaprotsessid**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="beb2d-203">Valige **Virtuaalse üksuse pollimise asünkroonse toimingu taustaprotsess**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="beb2d-204">Valige **Kuva viimased tulemused**.</span><span class="sxs-lookup"><span data-stu-id="beb2d-204">Select **View most recent results**.</span></span>

<span data-ttu-id="beb2d-205">Liuguripaan kuvab protsessi kõige viimased käivitamise tulemused.</span><span class="sxs-lookup"><span data-stu-id="beb2d-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="beb2d-206">Saate kuvada protsessi logi, sh kõiki tagastatud tõrkeid Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="beb2d-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="beb2d-207">Vt ka</span><span class="sxs-lookup"><span data-stu-id="beb2d-207">See also</span></span>

[<span data-ttu-id="beb2d-208">Mis on Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="beb2d-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="beb2d-209">Üksuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="beb2d-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="beb2d-210">Üksuse seoste ülevaade</span><span class="sxs-lookup"><span data-stu-id="beb2d-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="beb2d-211">Välistest andmeallikatest pärit andmeid sisaldavate virtuaalüksuste loomine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="beb2d-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="beb2d-212">Mis on Power Appsi portaalid?</span><span class="sxs-lookup"><span data-stu-id="beb2d-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="beb2d-213">Rakenduste loomise ülevaade Power Appsis</span><span class="sxs-lookup"><span data-stu-id="beb2d-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
