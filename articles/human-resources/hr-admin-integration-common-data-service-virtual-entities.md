---
title: Dataverse'i virtuaalsete tabelite konfigureerimine
description: Selles teemas kirjeldatakse virtuaalsete tabelite konfigureerimist rakenduse Dynamics 365 Human Resources jaoks. Looge ja värskendage olemasolevaid virtuaalseid tabeleid ning analüüsige loodud ja saadaolevaid tabeleid.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c2e207efe0eeec6fc7e679a6ae12edcb21b291f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058580"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="63db8-104">Dataverse'i virtuaalsete tabelite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="63db8-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="63db8-105">Dynamics 365 Human Resources on virtuaalne andmeallikas teenuses Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="63db8-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="63db8-106">See pakub täielikke loomise, lugemise, värskendamise ja kustutamise (CRUD) toiminguid lahendustes Dataverse ning Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="63db8-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="63db8-107">Virtuaalsete tabelite andmeid ei talletata teenuses Dataverse, vaid rakenduse andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="63db8-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="63db8-108">Selleks, et lubada rakenduse Human Resources üksuste korral CRUD-toimingud teenuses Dataverse, peate tegema tabelid teenuses Dataverse virtuaalüksustena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="63db8-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="63db8-109">See võimaldab teil teha lahendustes Dataverse ja Microsoft Power Platform CRUD-toiminguid andmetega, mis on rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63db8-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="63db8-110">Toimingute puhul toetatakse ka rakenduse Human Resources täielikku äriloogika kontrollimist, et tagada andmete terviklikkus andmete kirjutamisel üksustesse.</span><span class="sxs-lookup"><span data-stu-id="63db8-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="63db8-111">Human Resourcesi olemid vastavad Dataverse'i tabelitele.</span><span class="sxs-lookup"><span data-stu-id="63db8-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="63db8-112">Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="63db8-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="63db8-113">Rakenduses Human Resources saadaolevad virtuaalsed tabelid</span><span class="sxs-lookup"><span data-stu-id="63db8-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="63db8-114">Kõik avatud andmeprotokolli (OData) üksused rakenduses Human Resources on saadaval virtuaalsete tabelitena teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="63db8-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="63db8-115">Need on saadaval ka rakenduses Power Platform.</span><span class="sxs-lookup"><span data-stu-id="63db8-115">They're also available in Power Platform.</span></span> <span data-ttu-id="63db8-116">Nüüd saate luua rakendusi ja kogemusi otse rakendusest Human Resources pärit andmetega, mille puhul saate kasutada kõiki CRUD-toiminguid ilma andmete kopeerimise või sünkroonimise vajaduseta teenusega Dataverse.</span><span class="sxs-lookup"><span data-stu-id="63db8-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="63db8-117">Saate kasutada Power Appsi portaale, et luua väljapoole suunatud veebisaite, mis võimaldavad teha äritoimingute puhul rakenduses Human Resources koostööd.</span><span class="sxs-lookup"><span data-stu-id="63db8-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="63db8-118">Saate vaadata keskkonnas lubatud virtuaalsete tabelite loendit ja alustada tabelitega tööd rakenduses [Power Apps](https://make.powerapps.com) lahenduses **Dynamics 365 HR-i virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="63db8-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR-i virtuaalsed tabelid Power Appsis](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="63db8-120">Virtuaalsed tabelid vs. ematabelid</span><span class="sxs-lookup"><span data-stu-id="63db8-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="63db8-121">Rakenduse Human Resources virtuaalsed tabelid pole samad, mis teenuse Dataverse ematabelid, mis on loodud rakenduse Human Resources jaoks.</span><span class="sxs-lookup"><span data-stu-id="63db8-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="63db8-122">Rakenduse Human Resources ematabelid luuakse eraldi ja neid hallatakse lahenduses HCM Common teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="63db8-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="63db8-123">Ematabelite puhul talletatakse andmed teenuses Dataverse ja selle puhul on vajalik sünkroonimine rakenduse Human Resources andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="63db8-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="63db8-124">Rakenduse Human Resources jaoks mõeldud teenuse Dataverse ematabelite loendi leiate teemast [Dataverse'i tabelid](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="63db8-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="63db8-125">Seadistus</span><span class="sxs-lookup"><span data-stu-id="63db8-125">Setup</span></span>

<span data-ttu-id="63db8-126">Järgige neid seadistussamme, et lubada oma keskkonnas virtuaalsed tabelid.</span><span class="sxs-lookup"><span data-stu-id="63db8-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="63db8-127">Virtuaalsete tabelite lubamine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="63db8-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="63db8-128">Esmalt peate lubama tööruumi **Funktsioonihaldus** kaudu virtuaalsed tabelid lubama.</span><span class="sxs-lookup"><span data-stu-id="63db8-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="63db8-129">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="63db8-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="63db8-130">Valige paan **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="63db8-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="63db8-131">Valige **Virtuaalsete tabelite tugi HR-le rakenduses Dataverse** ja seejärel valige **Luba**.</span><span class="sxs-lookup"><span data-stu-id="63db8-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="63db8-132">Lisateavet eelvaatefunktsioonide lubamise ja keelamise kohta vt jaotisest [Funktsioonide haldus](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="63db8-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="63db8-133">Rakenduse registreerimine Microsoft Azure'is</span><span class="sxs-lookup"><span data-stu-id="63db8-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="63db8-134">Peate Human Resourcesi eksemplari Azure'i portaalis registreerima, et Microsofti identiteediplatvorm saaks pakkuda rakenduse ja kasutajate jaoks autentimis- ning autoriseerimisteenuseid.</span><span class="sxs-lookup"><span data-stu-id="63db8-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="63db8-135">Lisateavet Azure'is rakenduste registreerimise kohta leiate teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteediplatvormis](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="63db8-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="63db8-136">Avage [Microsoft Azure'i portaal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="63db8-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="63db8-137">Valige Azure'i teenuste loendis **Rakenduste registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="63db8-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="63db8-138">Valige **Uus registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="63db8-138">Select **New registration**.</span></span>

4. <span data-ttu-id="63db8-139">Sisestage väljale **Nimi** rakendust kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="63db8-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="63db8-140">Näiteks **Dynamics 365 Human Resources'i virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="63db8-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="63db8-141">Sisestage väljale **Ümbersuunamis-URI** oma rakenduse Human Resources eksemplari nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="63db8-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="63db8-142">Valige suvand **Registreeri**.</span><span class="sxs-lookup"><span data-stu-id="63db8-142">Select **Register**.</span></span>

7. <span data-ttu-id="63db8-143">Registreerimise lõpetamisel kuvatakse Azure'i portaalis rakenduse registreerimise kohta paan **Ülevaade**, mis sisaldab väärtust **Rakenduse (kliendi) ID**.</span><span class="sxs-lookup"><span data-stu-id="63db8-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="63db8-144">Kirjutage väärtus **Rakenduse (kliendi) ID** endale üles.</span><span class="sxs-lookup"><span data-stu-id="63db8-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="63db8-145">Te sisestate selle teabe [virtuaalsete tabelite andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="63db8-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="63db8-146">Valige vasakpoolsel navigeerimispaanil **Serdid ja saladused**.</span><span class="sxs-lookup"><span data-stu-id="63db8-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="63db8-147">Valige lehe jaotises **Klientrakenduse saladused** suvand **Uus klientrakenduse saladus**.</span><span class="sxs-lookup"><span data-stu-id="63db8-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="63db8-148">Sisestage kirjeldus, valige kestus ja valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="63db8-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="63db8-149">Saate salvestada saladuse väärtuse tabeli atribuudist **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="63db8-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="63db8-150">Te sisestate selle teabe [virtuaalsete tabelite andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="63db8-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="63db8-151">Kirjutage saladuse väärtus kindlasti praegu üles.</span><span class="sxs-lookup"><span data-stu-id="63db8-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="63db8-152">Pärast sellelt lehelt lahkumist ei kuvata saladust enam kunagi.</span><span class="sxs-lookup"><span data-stu-id="63db8-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="63db8-153">Dynamics 365 HR Virtuaalsete tabelite rakenduse installimine</span><span class="sxs-lookup"><span data-stu-id="63db8-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="63db8-154">Installige Dynamics 365 HR Virtuaalse tabeli rakendus oma Power Appsi keskkonda, et juurutada virtuaalse tabeli lahenduse pakett teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="63db8-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="63db8-155">Avage rakenduses Human Resources leht **Microsoft Dataverse integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="63db8-155">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="63db8-156">Valige vahekaart **Virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="63db8-156">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="63db8-157">Valige suvand **Installi virtuaaltabeli rakendus**.</span><span class="sxs-lookup"><span data-stu-id="63db8-157">Select **Install virtual table app**.</span></span>

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="63db8-158">Virtuaalse tabeli andmeallika konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="63db8-158">Configure the virtual table data source</span></span>

<span data-ttu-id="63db8-159">Järgmine samm on konfigureerida virtuaalse tabeli andmeallikas Power Appsi keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="63db8-159">The next step is to configure the virtual table data source in the Power Apps environment.</span></span>

1. <span data-ttu-id="63db8-160">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="63db8-160">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="63db8-161">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="63db8-161">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="63db8-162">Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.</span><span class="sxs-lookup"><span data-stu-id="63db8-162">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="63db8-163">Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub rakenduse lehe üleval paremal pool.</span><span class="sxs-lookup"><span data-stu-id="63db8-163">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="63db8-164">Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Finance and Operationsi virtuaalse andmeallika konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="63db8-164">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="63db8-165">Eelmise häälestussammu virtuaaltabeli rakenduse installimine võib võtta mitu minutit.</span><span class="sxs-lookup"><span data-stu-id="63db8-165">The installation of the virtual table app from the previous setup step can take a few minutes.</span></span> <span data-ttu-id="63db8-166">Kui **Finance and Operations virtuaalse andmeallika konfiguratsioonid** ei ole loendis saadaval, oodake minut ja värskendage siis loendit.</span><span class="sxs-lookup"><span data-stu-id="63db8-166">If **Finance and Operations Virtual Data Source Configurations** isn't available in the list, wait for a minute and refresh the list.</span></span>

6. <span data-ttu-id="63db8-167">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="63db8-167">Select **Results**.</span></span>

7. <span data-ttu-id="63db8-168">Valige kirje **Microsoft HR-i andmeallikas**.</span><span class="sxs-lookup"><span data-stu-id="63db8-168">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="63db8-169">Sisestage andmeallika konfiguratsiooni jaoks vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="63db8-169">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="63db8-170">**Siht-URL**: teie rakenduse Human Resources nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="63db8-170">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="63db8-171">Siht-URL-i vorming on:</span><span class="sxs-lookup"><span data-stu-id="63db8-171">The format of the target URL is:</span></span>
     
     <span data-ttu-id="63db8-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="63db8-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="63db8-173">Näide:</span><span class="sxs-lookup"><span data-stu-id="63db8-173">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="63db8-174">Tõrketeate kuvamise välistamiseks lisage URL-i lõppu märk „**/**“.</span><span class="sxs-lookup"><span data-stu-id="63db8-174">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="63db8-175">**Rentniku ID**: Azure Active Directory (Azure AD) rentniku ID.</span><span class="sxs-lookup"><span data-stu-id="63db8-175">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="63db8-176">**AAD rakenduse ID**: rakenduse (kliendi) ID, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="63db8-176">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="63db8-177">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="63db8-177">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="63db8-178">**AAD rakenduse saladus**: klientrakenduse saladus, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="63db8-178">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="63db8-179">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="63db8-179">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-i andmeallikas](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="63db8-181">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="63db8-181">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="63db8-182">Rakenduse õiguste andmine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="63db8-182">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="63db8-183">Andke rakenduses Human Resources õigused kahe Azure AD rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="63db8-183">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="63db8-184">Rakendus, mis loodi teie rentniku jaoks Microsoft Azure'i portaalis</span><span class="sxs-lookup"><span data-stu-id="63db8-184">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="63db8-185">Dynamics 365 HR Virtuaalse tabeli rakendus, mis on installitud Power Appsi keskkonnas</span><span class="sxs-lookup"><span data-stu-id="63db8-185">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="63db8-186">Avage rakenduses Human Resources leht **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="63db8-186">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="63db8-187">Valige uue rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="63db8-187">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="63db8-188">Sisestage väljale **Kliendi ID** Microsoft Azure'i portaalis registreeritud rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="63db8-188">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="63db8-189">Sisestage väljale **Nimi** Microsoft Azure'i portaalis registreeritud rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="63db8-189">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="63db8-190">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="63db8-190">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="63db8-191">Valige teise rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="63db8-191">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="63db8-192">**Kliendi ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="63db8-192">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="63db8-193">**Nimi**: Dynamics 365 HR Virtuaalne tabel</span><span class="sxs-lookup"><span data-stu-id="63db8-193">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="63db8-194">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="63db8-194">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="63db8-195">Virtuaalsete tabelite loomine</span><span class="sxs-lookup"><span data-stu-id="63db8-195">Generate virtual tables</span></span>

<span data-ttu-id="63db8-196">Kui seadistus on lõpule viidud, saate valida virtuaalsed tabelid, mille soovite luua ja lubada oma Dataverse'i eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="63db8-196">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="63db8-197">Avage rakenduses Human Resources leht **Microsoft Dataverse integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="63db8-197">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="63db8-198">Valige vahekaart **Virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="63db8-198">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="63db8-199">Lüliti **Virtuaalse tabelite lubamine** olekuks seatakse automaatselt **Jah**, kui kogu nõutav seadistus on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="63db8-199">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="63db8-200">Kui lüliti olekuks on seatud **Ei**, vaadake läbi selle dokumendi eelmiste jaotiste etapid, et kogu eeltingimuste häälestus oleks lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="63db8-200">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="63db8-201">Valige tabel või tabelid, mida soovite luua Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="63db8-201">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="63db8-202">Valige **Loo/värskenda**.</span><span class="sxs-lookup"><span data-stu-id="63db8-202">Select **Generate/refresh**.</span></span>

![Dataverse’i integratsioon](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a><span data-ttu-id="63db8-204">Tabeli loomise oleku kontrollimine</span><span class="sxs-lookup"><span data-stu-id="63db8-204">Check table generation status</span></span>

<span data-ttu-id="63db8-205">Virtuaalseid tabeleid luuakse Dataverse'i asünkroonse taustal töötlemise abil.</span><span class="sxs-lookup"><span data-stu-id="63db8-205">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="63db8-206">Protsessi uuendusi kuvatakse tegevuskeskuses.</span><span class="sxs-lookup"><span data-stu-id="63db8-206">Updates on the process display in the action center.</span></span> <span data-ttu-id="63db8-207">Protsessi üksikasju, sh tõrkelogisid, kuvatakse lehel **Protsessi automatiseerimised**.</span><span class="sxs-lookup"><span data-stu-id="63db8-207">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="63db8-208">Avage rakenduses Human Resources loendi **Protsessi automatiseerimised** leht.</span><span class="sxs-lookup"><span data-stu-id="63db8-208">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="63db8-209">Valige vahekaart **Taustaprotsessid**.</span><span class="sxs-lookup"><span data-stu-id="63db8-209">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="63db8-210">Valige **Virtuaalse tabeli pollimise asünkroonse toimingu taustaprotsess**.</span><span class="sxs-lookup"><span data-stu-id="63db8-210">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="63db8-211">Valige **Kuva viimased tulemused**.</span><span class="sxs-lookup"><span data-stu-id="63db8-211">Select **View most recent results**.</span></span>

<span data-ttu-id="63db8-212">Liuguripaan kuvab protsessi kõige viimased käivitamise tulemused.</span><span class="sxs-lookup"><span data-stu-id="63db8-212">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="63db8-213">Saate kuvada protsessi logi, sh kõiki tagastatud tõrkeid Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="63db8-213">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="63db8-214">Vt ka</span><span class="sxs-lookup"><span data-stu-id="63db8-214">See also</span></span>

[<span data-ttu-id="63db8-215">Mis on Dataverse?</span><span class="sxs-lookup"><span data-stu-id="63db8-215">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="63db8-216">Tabelid rakenduses Dataverse</span><span class="sxs-lookup"><span data-stu-id="63db8-216">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="63db8-217">Tabelite seoste ülevaade</span><span class="sxs-lookup"><span data-stu-id="63db8-217">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="63db8-218">Välistest andmeallikatest pärit andmeid sisaldavate virtuaalsete tabelite loomine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="63db8-218">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="63db8-219">Mis on Power Appsi portaalid?</span><span class="sxs-lookup"><span data-stu-id="63db8-219">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="63db8-220">Rakenduste loomise ülevaade Power Appsis</span><span class="sxs-lookup"><span data-stu-id="63db8-220">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
