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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959571"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="21449-104">Common Data Service'i virtuaalüksuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="21449-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="21449-105">Dynamics 365 Human Resources on virtuaalne andmeallikas teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21449-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="21449-106">See pakub täielikke loomise, lugemise, värskendamise ja kustutamise (CRUD) toiminguid lahendustes Common Data Service ning Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="21449-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="21449-107">Virtuaalüksuste andmeid ei talletata teenuses Common Data Service, vaid rakenduse andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="21449-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="21449-108">Selleks, et lubada rakenduse Human Resources üksuste korral CRUD-toimingud teenuses Common Data Service, peate tegema üksused teenuses Common Data Service virtuaalüksustena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="21449-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="21449-109">See võimaldab teil teha lahendustes Common Data Service ja Microsoft Power Platform CRUD-toiminguid andmetega, mis on rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="21449-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="21449-110">Toimingute puhul toetatakse ka rakenduse Human Resources täielikku äriloogika kontrollimist, et tagada andmete terviklikkus andmete kirjutamisel üksustesse.</span><span class="sxs-lookup"><span data-stu-id="21449-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="21449-111">Rakenduses Human Resources saadaolevad virtuaalüksused</span><span class="sxs-lookup"><span data-stu-id="21449-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="21449-112">Kõik avatud andmeprotokolli (OData) üksused rakenduses Human Resources on saadaval virtuaalüksustena teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21449-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="21449-113">Need on saadaval ka rakenduses Power Platform.</span><span class="sxs-lookup"><span data-stu-id="21449-113">They're also available in Power Platform.</span></span> <span data-ttu-id="21449-114">Nüüd saate luua rakendusi ja kogemusi otse rakendusest Human Resources pärit andmetega, mille puhul saate kasutada kõiki CRUD-toiminguid ilma andmete kopeerimise või sünkroonimise vajaduseta teenusega Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21449-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="21449-115">Saate kasutada Power Appsi portaale, et luua väljapoole suunatud veebisaite, mis võimaldavad teha äritoimingute puhul rakenduses Human Resources koostööd.</span><span class="sxs-lookup"><span data-stu-id="21449-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="21449-116">Saate vaadata keskkonnas lubatud virtuaalüksuste loendit ja alustada üksustega tööd rakenduses [Power Apps](https://make.powerapps.com) lahenduses **Dynamics 365 HR-i virtuaalüksused**.</span><span class="sxs-lookup"><span data-stu-id="21449-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR-i virtuaalüksused Power Appsis](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="21449-118">Virtuaal- ja tavaliste üksuste võrdlus</span><span class="sxs-lookup"><span data-stu-id="21449-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="21449-119">Rakenduse Human Resources virtuaalüksused pole samad, mis tavalised teenuse Common Data Service üksused, mis on loodud rakenduse Human Resources jaoks.</span><span class="sxs-lookup"><span data-stu-id="21449-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="21449-120">Rakenduse Human Resources tavalised üksused luuakse eraldi ja neid hallatakse lahenduses HCM Common teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21449-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="21449-121">Tavaliste üksuste puhul talletatakse andmed teenuses Common Data Service ja selle puhul on vajalik sünkroonimine rakenduse Human Resources andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="21449-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="21449-122">Rakenduse Human Resources jaoks mõeldud teenuse Common Data Service tavaliste üksuste loendi leiate teemast [Common Data Service'i üksused](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="21449-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="21449-123">Seadistus</span><span class="sxs-lookup"><span data-stu-id="21449-123">Setup</span></span>

<span data-ttu-id="21449-124">Järgige neid seadistussamme, et lubada oma keskkonnas virtuaalüksused.</span><span class="sxs-lookup"><span data-stu-id="21449-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="21449-125">Rakenduse registreerimine Microsoft Azure'is</span><span class="sxs-lookup"><span data-stu-id="21449-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="21449-126">Esmalt peate rakenduse Azure'i portaalis registreerima, et Microsofti identiteediplatvorm saaks pakkuda rakenduse ja kasutajate jaoks autentimis- ning autoriseerimisteenuseid.</span><span class="sxs-lookup"><span data-stu-id="21449-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="21449-127">Lisateavet Azure'is rakenduste registreerimise kohta leiate teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteediplatvormis](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="21449-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="21449-128">Avage [Microsoft Azure'i portaal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="21449-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="21449-129">Valige Azure'i teenuste loendis **Rakenduste registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="21449-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="21449-130">Valige **Uus registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="21449-130">Select **New registration**.</span></span>

4. <span data-ttu-id="21449-131">Sisestage väljale **Nimi** rakendust kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="21449-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="21449-132">Näiteks **Dynamics 365 Human Resources'i virtuaalüksused**.</span><span class="sxs-lookup"><span data-stu-id="21449-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="21449-133">Sisestage väljale **Ümbersuunamis-URI** oma rakenduse Human Resources eksemplari nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="21449-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="21449-134">Valige suvand **Registreeri**.</span><span class="sxs-lookup"><span data-stu-id="21449-134">Select **Register**.</span></span>

7. <span data-ttu-id="21449-135">Registreerimise lõpetamisel kuvatakse Azure'i portaalis rakenduse registreerimise kohta paan **Ülevaade**, mis sisaldab väärtust **Rakenduse (kliendi) ID**.</span><span class="sxs-lookup"><span data-stu-id="21449-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="21449-136">Kirjutage väärtus **Rakenduse (kliendi) ID** endale üles.</span><span class="sxs-lookup"><span data-stu-id="21449-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="21449-137">Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="21449-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="21449-138">Valige vasakpoolsel navigeerimispaanil **Serdid ja saladused**.</span><span class="sxs-lookup"><span data-stu-id="21449-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="21449-139">Valige lehe jaotises **Klientrakenduse saladused** suvand **Uus klientrakenduse saladus**.</span><span class="sxs-lookup"><span data-stu-id="21449-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="21449-140">Sisestage kirjeldus, valige kestus ja valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="21449-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="21449-141">Kirjutage saladuse väärtus üles.</span><span class="sxs-lookup"><span data-stu-id="21449-141">Record the secret's value.</span></span> <span data-ttu-id="21449-142">Te sisestate selle teabe [virtuaalüksuse andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="21449-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="21449-143">Kirjutage saladuse väärtus kindlasti praegu üles.</span><span class="sxs-lookup"><span data-stu-id="21449-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="21449-144">Pärast sellelt lehelt lahkumist ei kuvata saladust enam kunagi.</span><span class="sxs-lookup"><span data-stu-id="21449-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="21449-145">Dynamics 365 HR Virtual Entity rakenduse installimine</span><span class="sxs-lookup"><span data-stu-id="21449-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="21449-146">Installige Dynamics 365 HR Virtual Entity rakendus oma Power Appsi keskkonda, et juurutada virtuaalüksuse lahenduse pakett teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21449-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="21449-147">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="21449-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="21449-148">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="21449-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="21449-149">Valige lehe jaotises **Ressursid** suvand **Dynamics 365 rakendused**.</span><span class="sxs-lookup"><span data-stu-id="21449-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="21449-150">Valige tegevus **Installi rakendus**.</span><span class="sxs-lookup"><span data-stu-id="21449-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="21449-151">Valige **Dynamics 365 HR Virtual Entity** ja valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="21449-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="21449-152">Vaadake teenusetingimused üle ja märkige, et te nõustute nendega.</span><span class="sxs-lookup"><span data-stu-id="21449-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="21449-153">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="21449-153">Select **Install**.</span></span>

<span data-ttu-id="21449-154">Installimine võtab mõne minuti.</span><span class="sxs-lookup"><span data-stu-id="21449-154">The install takes a few minutes.</span></span> <span data-ttu-id="21449-155">Kui see on lõpule viidud, jätkake järgmiste sammudega.</span><span class="sxs-lookup"><span data-stu-id="21449-155">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Entity rakenduse installimine Power Platformi halduskeskusest](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="21449-157">Virtuaalüksuse andmeallika konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="21449-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="21449-158">Järgmine samm on konfigureerida virtuaalüksuse andmeallikas Power Appsi keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="21449-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="21449-159">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="21449-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="21449-160">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="21449-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="21449-161">Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.</span><span class="sxs-lookup"><span data-stu-id="21449-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="21449-162">Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub rakenduse lehe üleval paremal pool.</span><span class="sxs-lookup"><span data-stu-id="21449-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="21449-163">Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Finance and Operationsi virtuaalse andmeallika konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="21449-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="21449-164">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="21449-164">Select **Results**.</span></span>

7. <span data-ttu-id="21449-165">Valige kirje **Microsoft HR-i andmeallikas**.</span><span class="sxs-lookup"><span data-stu-id="21449-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="21449-166">Sisestage andmeallika konfiguratsiooni jaoks vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="21449-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="21449-167">**Siht-URL**: teie rakenduse Human Resources nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="21449-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="21449-168">**Rentniku ID**: Azure Active Directory (Azure AD) rentniku ID.</span><span class="sxs-lookup"><span data-stu-id="21449-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="21449-169">**AAD rakenduse ID**: rakenduse (kliendi) ID, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="21449-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="21449-170">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="21449-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="21449-171">**AAD rakenduse saladus**: klientrakenduse saladus, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="21449-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="21449-172">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="21449-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="21449-173">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="21449-173">Select **Save & Close**.</span></span>

   ![Microsoft HR-i andmeallikas](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="21449-175">Rakenduse õiguste andmine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="21449-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="21449-176">Andke rakenduses Human Resources õigused kahe Azure AD rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="21449-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="21449-177">Rakendus, mis loodi teie rentniku jaoks Microsoft Azure'i portaalis</span><span class="sxs-lookup"><span data-stu-id="21449-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="21449-178">Dynamics 365 HR Virtual Entity rakendus, mis on installitud Power Appsi keskkonnas</span><span class="sxs-lookup"><span data-stu-id="21449-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="21449-179">Avage rakenduses Human Resources leht **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="21449-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="21449-180">Valige uue rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="21449-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="21449-181">Sisestage väljale **Kliendi ID** Microsoft Azure'i portaalis registreeritud rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="21449-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="21449-182">Sisestage väljale **Nimi** Microsoft Azure'i portaalis registreeritud rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="21449-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="21449-183">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="21449-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="21449-184">Valige teise rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="21449-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="21449-185">**Kliendi ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="21449-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="21449-186">**Nimi**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="21449-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="21449-187">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="21449-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="21449-188">Virtuaalüksuste loomine</span><span class="sxs-lookup"><span data-stu-id="21449-188">Generate virtual entities</span></span>

<span data-ttu-id="21449-189">Kui seadistus on lõpule viidud, saate valida virtuaalüksused, mille soovite luua ja lubada oma Common Data Service'i eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="21449-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="21449-190">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="21449-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="21449-191">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="21449-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="21449-192">Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.</span><span class="sxs-lookup"><span data-stu-id="21449-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="21449-193">Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub lehe üleval paremal pool.</span><span class="sxs-lookup"><span data-stu-id="21449-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="21449-194">Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Saadaval HR-i üksused**.</span><span class="sxs-lookup"><span data-stu-id="21449-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="21449-195">Kasutage filtrisuvandeid, et leida üksus või üksused, mille soovite lubada.</span><span class="sxs-lookup"><span data-stu-id="21449-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="21449-196">Valige loendist üksus.</span><span class="sxs-lookup"><span data-stu-id="21449-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="21449-197">Muutke üksuse lehel üksuse puhul atribuudi **On loodud** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="21449-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="21449-198">Salvestage ja sulgege üksuse leht.</span><span class="sxs-lookup"><span data-stu-id="21449-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="21449-199">Saate luua korraga mitu virtuaalüksust, kasutades lehte **Mitme kirje muutmine**.</span><span class="sxs-lookup"><span data-stu-id="21449-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="21449-200">Valige lehel mitu kirjet ja valige ribal suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="21449-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="21449-201">Seejärel saate muuta kõigi valitud kirjete atribuuti **On loodud**.</span><span class="sxs-lookup"><span data-stu-id="21449-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Saadaval HR-i üksused](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="21449-203">Et muuta virtuaalüksuste loomise protsess tulevastes versioonides sujuvamaks, toimub protsess rakenduse Human Resources lehel.</span><span class="sxs-lookup"><span data-stu-id="21449-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="21449-204">Vt ka</span><span class="sxs-lookup"><span data-stu-id="21449-204">See also</span></span>

[<span data-ttu-id="21449-205">Mis on Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="21449-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="21449-206">Üksuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="21449-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="21449-207">Üksuse seoste ülevaade</span><span class="sxs-lookup"><span data-stu-id="21449-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="21449-208">Välistest andmeallikatest pärit andmeid sisaldavate virtuaalüksuste loomine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="21449-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="21449-209">Mis on Power Appsi portaalid?</span><span class="sxs-lookup"><span data-stu-id="21449-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="21449-210">Rakenduste loomise ülevaade Power Appsis</span><span class="sxs-lookup"><span data-stu-id="21449-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
