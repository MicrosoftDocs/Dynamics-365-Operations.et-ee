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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae36f1436ddd7f41bf0c3510b47cbc440224f484
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890048"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="e1bba-104">Dataverse'i virtuaalsete tabelite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e1bba-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e1bba-105">Dynamics 365 Human Resources on virtuaalne andmeallikas teenuses Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bba-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="e1bba-106">See pakub täielikke loomise, lugemise, värskendamise ja kustutamise (CRUD) toiminguid lahendustes Dataverse ning Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="e1bba-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="e1bba-107">Virtuaalsete tabelite andmeid ei talletata teenuses Dataverse, vaid rakenduse andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="e1bba-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="e1bba-108">Selleks, et lubada rakenduse Human Resources üksuste korral CRUD-toimingud teenuses Dataverse, peate tegema tabelid teenuses Dataverse virtuaalüksustena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="e1bba-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="e1bba-109">See võimaldab teil teha lahendustes Dataverse ja Microsoft Power Platform CRUD-toiminguid andmetega, mis on rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e1bba-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="e1bba-110">Toimingute puhul toetatakse ka rakenduse Human Resources täielikku äriloogika kontrollimist, et tagada andmete terviklikkus andmete kirjutamisel üksustesse.</span><span class="sxs-lookup"><span data-stu-id="e1bba-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="e1bba-111">Human Resourcesi olemid vastavad Dataverse'i tabelitele.</span><span class="sxs-lookup"><span data-stu-id="e1bba-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="e1bba-112">Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="e1bba-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="e1bba-113">Rakenduses Human Resources saadaolevad virtuaalsed tabelid</span><span class="sxs-lookup"><span data-stu-id="e1bba-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="e1bba-114">Kõik avatud andmeprotokolli (OData) üksused rakenduses Human Resources on saadaval virtuaalsete tabelitena teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bba-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="e1bba-115">Need on saadaval ka rakenduses Power Platform.</span><span class="sxs-lookup"><span data-stu-id="e1bba-115">They're also available in Power Platform.</span></span> <span data-ttu-id="e1bba-116">Nüüd saate luua rakendusi ja kogemusi otse rakendusest Human Resources pärit andmetega, mille puhul saate kasutada kõiki CRUD-toiminguid ilma andmete kopeerimise või sünkroonimise vajaduseta teenusega Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bba-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="e1bba-117">Saate kasutada Power Appsi portaale, et luua väljapoole suunatud veebisaite, mis võimaldavad teha äritoimingute puhul rakenduses Human Resources koostööd.</span><span class="sxs-lookup"><span data-stu-id="e1bba-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="e1bba-118">Saate vaadata keskkonnas lubatud virtuaalsete tabelite loendit ja alustada tabelitega tööd rakenduses [Power Apps](https://make.powerapps.com) lahenduses **Dynamics 365 HR-i virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR-i virtuaalsed tabelid Power Appsis](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="e1bba-120">Virtuaalsed tabelid vs. ematabelid</span><span class="sxs-lookup"><span data-stu-id="e1bba-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="e1bba-121">Rakenduse Human Resources virtuaalsed tabelid pole samad, mis teenuse Dataverse ematabelid, mis on loodud rakenduse Human Resources jaoks.</span><span class="sxs-lookup"><span data-stu-id="e1bba-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="e1bba-122">Rakenduse Human Resources ematabelid luuakse eraldi ja neid hallatakse lahenduses HCM Common teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bba-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="e1bba-123">Ematabelite puhul talletatakse andmed teenuses Dataverse ja selle puhul on vajalik sünkroonimine rakenduse Human Resources andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="e1bba-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="e1bba-124">Rakenduse Human Resources jaoks mõeldud teenuse Dataverse ematabelite loendi leiate teemast [Dataverse'i tabelid](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="e1bba-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="e1bba-125">Seadistus</span><span class="sxs-lookup"><span data-stu-id="e1bba-125">Setup</span></span>

<span data-ttu-id="e1bba-126">Järgige neid seadistussamme, et lubada oma keskkonnas virtuaalsed tabelid.</span><span class="sxs-lookup"><span data-stu-id="e1bba-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="e1bba-127">Virtuaalsete tabelite lubamine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="e1bba-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="e1bba-128">Esmalt peate lubama tööruumi **Funktsioonihaldus** kaudu virtuaalsed tabelid lubama.</span><span class="sxs-lookup"><span data-stu-id="e1bba-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="e1bba-129">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e1bba-130">Valige paan **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="e1bba-131">Valige **Virtuaalsete tabelite tugi HR-le rakenduses Dataverse** ja seejärel valige **Luba**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="e1bba-132">Lisateavet eelvaatefunktsioonide lubamise ja keelamise kohta vt jaotisest [Funktsioonide haldus](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="e1bba-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="e1bba-133">Rakenduse registreerimine Microsoft Azure'is</span><span class="sxs-lookup"><span data-stu-id="e1bba-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="e1bba-134">Peate Human Resourcesi eksemplari Azure'i portaalis registreerima, et Microsofti identiteediplatvorm saaks pakkuda rakenduse ja kasutajate jaoks autentimis- ning autoriseerimisteenuseid.</span><span class="sxs-lookup"><span data-stu-id="e1bba-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="e1bba-135">Lisateavet Azure'is rakenduste registreerimise kohta leiate teemast [Lühijuhend: rakenduse registreerimine Microsofti identiteediplatvormis](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="e1bba-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="e1bba-136">Avage [Microsoft Azure'i portaal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="e1bba-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="e1bba-137">Valige Azure'i teenuste loendis **Rakenduste registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="e1bba-138">Valige **Uus registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-138">Select **New registration**.</span></span>

4. <span data-ttu-id="e1bba-139">Sisestage väljale **Nimi** rakendust kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="e1bba-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="e1bba-140">Näiteks **Dynamics 365 Human Resources'i virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="e1bba-141">Sisestage väljale **Ümbersuunamis-URI** oma rakenduse Human Resources eksemplari nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="e1bba-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="e1bba-142">Valige suvand **Registreeri**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-142">Select **Register**.</span></span>

7. <span data-ttu-id="e1bba-143">Registreerimise lõpetamisel kuvatakse Azure'i portaalis rakenduse registreerimise kohta paan **Ülevaade**, mis sisaldab väärtust **Rakenduse (kliendi) ID**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="e1bba-144">Kirjutage väärtus **Rakenduse (kliendi) ID** endale üles.</span><span class="sxs-lookup"><span data-stu-id="e1bba-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="e1bba-145">Te sisestate selle teabe [virtuaalsete tabelite andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="e1bba-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="e1bba-146">Valige vasakpoolsel navigeerimispaanil **Serdid ja saladused**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="e1bba-147">Valige lehe jaotises **Klientrakenduse saladused** suvand **Uus klientrakenduse saladus**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="e1bba-148">Sisestage kirjeldus, valige kestus ja valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="e1bba-149">Saate salvestada saladuse väärtuse tabeli atribuudist **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="e1bba-150">Te sisestate selle teabe [virtuaalsete tabelite andmeallika konfigureerimisel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="e1bba-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e1bba-151">Kirjutage saladuse väärtus kindlasti praegu üles.</span><span class="sxs-lookup"><span data-stu-id="e1bba-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="e1bba-152">Pärast sellelt lehelt lahkumist ei kuvata saladust enam kunagi.</span><span class="sxs-lookup"><span data-stu-id="e1bba-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="e1bba-153">Dynamics 365 HR Virtuaalsete tabelite rakenduse installimine</span><span class="sxs-lookup"><span data-stu-id="e1bba-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="e1bba-154">Installige Dynamics 365 HR Virtuaalse tabeli rakendus oma Power Appsi keskkonda, et juurutada virtuaalse tabeli lahenduse pakett teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1bba-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="e1bba-155">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e1bba-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="e1bba-156">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="e1bba-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="e1bba-157">Valige lehe jaotises **Ressursid** suvand **Dynamics 365 rakendused**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="e1bba-158">Valige tegevus **Installi rakendus**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="e1bba-159">Valige **Dynamics 365 HR Virtuaalne tabel** ja valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="e1bba-160">Vaadake teenusetingimused üle ja märkige, et te nõustute nendega.</span><span class="sxs-lookup"><span data-stu-id="e1bba-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="e1bba-161">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-161">Select **Install**.</span></span>

<span data-ttu-id="e1bba-162">Installimine võtab mõne minuti.</span><span class="sxs-lookup"><span data-stu-id="e1bba-162">The install takes a few minutes.</span></span> <span data-ttu-id="e1bba-163">Kui see on lõpule viidud, jätkake järgmiste sammudega.</span><span class="sxs-lookup"><span data-stu-id="e1bba-163">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtuaalse tabeli rakenduse installimine Power Platformi halduskeskusest](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="e1bba-165">Virtuaalse tabeli andmeallika konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e1bba-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="e1bba-166">Järgmine samm on konfigureerida virtuaalse tabeli andmeallikas Power Appsi keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="e1bba-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="e1bba-167">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e1bba-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="e1bba-168">Valige loendist **Keskkonnad** Power Appsi keskkond, mis on seotud teie rakenduse Human Resources eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="e1bba-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="e1bba-169">Valige lehe jaotisest **Üksikasjad** suvand **Keskkonna URL**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="e1bba-170">Valige jaotises **Lahenduse seisundikeskus** **täpsema otsingu** ikoon, mis asub rakenduse lehe üleval paremal pool.</span><span class="sxs-lookup"><span data-stu-id="e1bba-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="e1bba-171">Valige lehel **Täpsem otsing** ripploendist **Otsitav** suvand **Finance and Operationsi virtuaalse andmeallika konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="e1bba-172">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-172">Select **Results**.</span></span>

7. <span data-ttu-id="e1bba-173">Valige kirje **Microsoft HR-i andmeallikas**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="e1bba-174">Sisestage andmeallika konfiguratsiooni jaoks vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="e1bba-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="e1bba-175">**Siht-URL**: teie rakenduse Human Resources nimeruumi URL.</span><span class="sxs-lookup"><span data-stu-id="e1bba-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="e1bba-176">Siht-URL-i vorming on:</span><span class="sxs-lookup"><span data-stu-id="e1bba-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="e1bba-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="e1bba-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="e1bba-178">Näide:</span><span class="sxs-lookup"><span data-stu-id="e1bba-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="e1bba-179">Tõrketeate kuvamise välistamiseks lisage URL-i lõppu märk „**/**“.</span><span class="sxs-lookup"><span data-stu-id="e1bba-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="e1bba-180">**Rentniku ID**: Azure Active Directory (Azure AD) rentniku ID.</span><span class="sxs-lookup"><span data-stu-id="e1bba-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="e1bba-181">**AAD rakenduse ID**: rakenduse (kliendi) ID, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="e1bba-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="e1bba-182">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="e1bba-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="e1bba-183">**AAD rakenduse saladus**: klientrakenduse saladus, mis loodi Microsoft Azure'i portaalis registreeritud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="e1bba-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="e1bba-184">Selle teabe saite varem sammus [Rakenduse registreerimine Microsoft Azure'is](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="e1bba-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-i andmeallikas](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="e1bba-186">Valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="e1bba-187">Rakenduse õiguste andmine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="e1bba-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="e1bba-188">Andke rakenduses Human Resources õigused kahe Azure AD rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="e1bba-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="e1bba-189">Rakendus, mis loodi teie rentniku jaoks Microsoft Azure'i portaalis</span><span class="sxs-lookup"><span data-stu-id="e1bba-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="e1bba-190">Dynamics 365 HR Virtuaalse tabeli rakendus, mis on installitud Power Appsi keskkonnas</span><span class="sxs-lookup"><span data-stu-id="e1bba-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="e1bba-191">Avage rakenduses Human Resources leht **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="e1bba-192">Valige uue rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="e1bba-193">Sisestage väljale **Kliendi ID** Microsoft Azure'i portaalis registreeritud rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="e1bba-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="e1bba-194">Sisestage väljale **Nimi** Microsoft Azure'i portaalis registreeritud rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="e1bba-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="e1bba-195">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="e1bba-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="e1bba-196">Valige teise rakenduse kirje loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="e1bba-197">**Kliendi ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="e1bba-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="e1bba-198">**Nimi**: Dynamics 365 HR Virtuaalne tabel</span><span class="sxs-lookup"><span data-stu-id="e1bba-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="e1bba-199">Valige väljal **Kasutaja ID** sellise kasutaja ID, kellel rakenduses Human Resources ja Power Appsi keskkonnas administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="e1bba-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="e1bba-200">Virtuaalsete tabelite loomine</span><span class="sxs-lookup"><span data-stu-id="e1bba-200">Generate virtual tables</span></span>

<span data-ttu-id="e1bba-201">Kui seadistus on lõpule viidud, saate valida virtuaalsed tabelid, mille soovite luua ja lubada oma Dataverse'i eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="e1bba-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="e1bba-202">Avage rakenduses Human Resources leht **Dataverse integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="e1bba-203">Valige vahekaart **Virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="e1bba-204">Lüliti **Virtuaalse tabelite lubamine** olekuks seatakse automaatselt **Jah**, kui kogu nõutav seadistus on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e1bba-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="e1bba-205">Kui lüliti olekuks on seatud **Ei**, vaadake läbi selle dokumendi eelmiste jaotiste etapid, et kogu eeltingimuste häälestus oleks lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e1bba-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="e1bba-206">Valige tabel või tabelid, mida soovite luua Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="e1bba-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="e1bba-207">Valige **Loo/värskenda**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-207">Select **Generate/refresh**.</span></span>

![Dataverse’i integratsioon](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="e1bba-209">Tabeli loomise oleku kontrollimine</span><span class="sxs-lookup"><span data-stu-id="e1bba-209">Check table generation status</span></span>

<span data-ttu-id="e1bba-210">Virtuaalseid tabeleid luuakse Dataverse'i asünkroonse taustal töötlemise abil.</span><span class="sxs-lookup"><span data-stu-id="e1bba-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="e1bba-211">Protsessi uuendusi kuvatakse tegevuskeskuses.</span><span class="sxs-lookup"><span data-stu-id="e1bba-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="e1bba-212">Protsessi üksikasju, sh tõrkelogisid, kuvatakse lehel **Protsessi automatiseerimised**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="e1bba-213">Avage rakenduses Human Resources loendi **Protsessi automatiseerimised** leht.</span><span class="sxs-lookup"><span data-stu-id="e1bba-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="e1bba-214">Valige vahekaart **Taustaprotsessid**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="e1bba-215">Valige **Virtuaalse tabeli pollimise asünkroonse toimingu taustaprotsess**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="e1bba-216">Valige **Kuva viimased tulemused**.</span><span class="sxs-lookup"><span data-stu-id="e1bba-216">Select **View most recent results**.</span></span>

<span data-ttu-id="e1bba-217">Liuguripaan kuvab protsessi kõige viimased käivitamise tulemused.</span><span class="sxs-lookup"><span data-stu-id="e1bba-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="e1bba-218">Saate kuvada protsessi logi, sh kõiki tagastatud tõrkeid Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="e1bba-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1bba-219">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e1bba-219">See also</span></span>

[<span data-ttu-id="e1bba-220">Mis on Dataverse?</span><span class="sxs-lookup"><span data-stu-id="e1bba-220">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="e1bba-221">Tabelid rakenduses Dataverse</span><span class="sxs-lookup"><span data-stu-id="e1bba-221">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="e1bba-222">Tabelite seoste ülevaade</span><span class="sxs-lookup"><span data-stu-id="e1bba-222">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="e1bba-223">Välistest andmeallikatest pärit andmeid sisaldavate virtuaalsete tabelite loomine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="e1bba-223">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="e1bba-224">Mis on Power Appsi portaalid?</span><span class="sxs-lookup"><span data-stu-id="e1bba-224">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="e1bba-225">Rakenduste loomise ülevaade Power Appsis</span><span class="sxs-lookup"><span data-stu-id="e1bba-225">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]