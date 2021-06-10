---
title: LinkedIn talent Hubiga integreerimine
description: Selles teemas kirjeldatakse, kuidas seadistada Microsoft Dynamics 365 Human Resourcesi ja LinkedIn Talent Hubi vahelist intgratsiooni.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4b8c1467368cbcbed5049561b52b29388ec21a5f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055096"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="c7f34-103">LinkedIn talent Hubiga integreerimine</span><span class="sxs-lookup"><span data-stu-id="c7f34-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c7f34-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) on kandidaadi jälgimise süsteemi (ATS) platvorm.</span><span class="sxs-lookup"><span data-stu-id="c7f34-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="c7f34-105">See võimaldab teil leida, hallata ja palgata töötajaid ühest kohast.</span><span class="sxs-lookup"><span data-stu-id="c7f34-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="c7f34-106">Microsoft Dynamics 365 Human Resourcesi integreerimisel LinkedIn Talent Hubiga saate Human Resourcesis hõlpsalt luua töövõtja kirjed kandidaatide jaoks, kes on palgatud ametikohale.</span><span class="sxs-lookup"><span data-stu-id="c7f34-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="c7f34-107">Seadistus</span><span class="sxs-lookup"><span data-stu-id="c7f34-107">Setup</span></span>

<span data-ttu-id="c7f34-108">Süsteemiadministraator peab lõpule viima seadistustoimingud, et lubada integreerimist LinkedIn Talent Hubiga.</span><span class="sxs-lookup"><span data-stu-id="c7f34-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="c7f34-109">Esmalt peate Power Appsi keskkonnas seadistama kasutaja- ja turberolli, et anda LinkedIn Talent Hubile vajalikud load andmete kirjutamiseks Human Resourcesisse.</span><span class="sxs-lookup"><span data-stu-id="c7f34-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="c7f34-110">Keskkonna linkimine LinkedIn Talent Hubiga</span><span class="sxs-lookup"><span data-stu-id="c7f34-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="c7f34-111">Avage [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="c7f34-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="c7f34-112">Valige kasutaja rippmenüüst **Toote sätted**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="c7f34-113">Valige vasakpoolsel navigeerimispaanil jaotises **Täpsem** suvand **Integratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="c7f34-114">Valige **Autoriseeri** Microsofti Dynamics 365 Human Resourcesi integratsiooniks.</span><span class="sxs-lookup"><span data-stu-id="c7f34-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="c7f34-115">Valige lehel **Dynamics 365 Human Resources** keskkond, millega soovite LinkedIn Talent Hubi linkida ja seejärel valige **Lingi**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hubi sisseelamine](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="c7f34-117">Saate linkida ainult keskkondadega, kus teie kasutajakontol on administraatori juurdepääs nii Human Resourcesi keskkonnale kui ka seostatud Power Appsi keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="c7f34-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="c7f34-118">Kui Human Resourcesi linkide lehel pole loetletud ühtegi keskkonda, veenduge, et teie rentnikus oleks litsentsitud Human Resourcesi keskkond ja et kasutajal, millega olete linkide lehele sissetogitud, oleks administraatori õigused nii Human Resourcesi keskkonnale kui ka Power Appsi keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="c7f34-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="c7f34-119">Power Appsi turberolli loomine</span><span class="sxs-lookup"><span data-stu-id="c7f34-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="c7f34-120">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c7f34-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="c7f34-121">Valige loendist **Keskkonnad** keskkond, mis on seostatud Human Resourcesi keskkonnaga, mida soovite linkida oma LinkedIn Talent Hubi eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="c7f34-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="c7f34-122">Valige **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-122">Select **Settings**.</span></span>

4. <span data-ttu-id="c7f34-123">Laiendage sõlme **Kasutajad + load** ja valige **Turberollid**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="c7f34-124">Valige lehe **Turberollid** tööriistaribal **Uus roll**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="c7f34-125">Sisestage vahekaardil **Üksikasjad** rolli nimi, nt **LinkedIn Talent Hub HRIS-i integreerimine**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="c7f34-126">Valige vahekaardil **Kohandamine** organisatsioonitaseme luba **Lugemine** järgmistele üksustele:</span><span class="sxs-lookup"><span data-stu-id="c7f34-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="c7f34-127">Üksus</span><span class="sxs-lookup"><span data-stu-id="c7f34-127">Entity</span></span>
    - <span data-ttu-id="c7f34-128">Field</span><span class="sxs-lookup"><span data-stu-id="c7f34-128">Field</span></span>
    - <span data-ttu-id="c7f34-129">Suhte tüüp</span><span class="sxs-lookup"><span data-stu-id="c7f34-129">Relationship</span></span>

8. <span data-ttu-id="c7f34-130">Salvestage ja sulgege turberoll.</span><span class="sxs-lookup"><span data-stu-id="c7f34-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="c7f34-131">Power Appsi rakenduse kasutaja loomine</span><span class="sxs-lookup"><span data-stu-id="c7f34-131">Create a Power Apps application user</span></span>

<span data-ttu-id="c7f34-132">Rakenduse kasutaja tuleb luua LinkedIn Talent Hubi adapteris, et anda adapterile load kandidaadi kirjete kirjutamiseks Power Appsi keskkonda.</span><span class="sxs-lookup"><span data-stu-id="c7f34-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="c7f34-133">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c7f34-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="c7f34-134">Valige loendist **Keskkonnad** keskkond, mis on seostatud Human Resourcesi keskkonnaga, mida soovite linkida oma LinkedIn Talent Hubi eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="c7f34-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="c7f34-135">Valige **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-135">Select **Settings**.</span></span>

4. <span data-ttu-id="c7f34-136">Laiendage sõlme **Kasutajad + load** ja valige **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="c7f34-137">Valige **Dynamics 365 kasutajate haldamine**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="c7f34-138">Kasutage ülal olevat ripploendit, et muuta vaikimisi vaade **Lubatud kasutad** vaateks **Rakenduse kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Rakenduse kasutajate vaade](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="c7f34-140">Valige tööriistaribal **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="c7f34-141">Tehke lehel **Uus kasutaja** järgmist.</span><span class="sxs-lookup"><span data-stu-id="c7f34-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="c7f34-142">Muutke välja **Kasutaja Tüüp** väärtuseks **Rakenduse kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="c7f34-143">Seadke välja **Kasutajanimi** väärtuseks **Dynamics365 HR LinkedIn HRIS-i integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="c7f34-144">Määrake välja **Rakenduse ID** väärtuseks **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="c7f34-145">Sisestage mis tahes väärtus väljadele **Eesnimi**, **Perekonnanimi** ja **Esmane meiliaadress**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="c7f34-146">Valige tööriistaribal **Salvesta \& Sule**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="c7f34-147">Turberolli määramine uuele kasutajale</span><span class="sxs-lookup"><span data-stu-id="c7f34-147">Assign a security role to the new user</span></span>

<span data-ttu-id="c7f34-148">Pärast eelmises jaotises uue rakenduse kasutaja salvestamist ja sulgemist naasete lehele **Kasutajate loend**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="c7f34-149">Muutke lehel **Kasutajate loend** vaateks **Rakenduse kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="c7f34-150">Valige eelmises jaotises loodud rakenduse kasutaja.</span><span class="sxs-lookup"><span data-stu-id="c7f34-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="c7f34-151">Valige tööriistaribal **Rollide haldamine**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="c7f34-152">Valige integratsiooni jaoks eelnevalt loodud turberoll.</span><span class="sxs-lookup"><span data-stu-id="c7f34-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="c7f34-153">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="c7f34-154">Azure Active Directory rakenduse lisamine Human Resourcesisse</span><span class="sxs-lookup"><span data-stu-id="c7f34-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="c7f34-155">Avage Dynamics 365 Human Resourcesis leht **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="c7f34-156">Lisage loendisse uus kirje ja määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="c7f34-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="c7f34-157">**Kliendi ID**: sisestage **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="c7f34-158">**Nimi**: sisestage Power Appsi turberolli nimi, mille eelnevalt lõite, nt **LinkedIn Talent Hub HRIS-i integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="c7f34-159">**Kasutaja ID**: valige kasutaja, kellel on õigus kirjutada andmeid personalihalduses.</span><span class="sxs-lookup"><span data-stu-id="c7f34-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="c7f34-160">Tabeli loomine Dataverse'is</span><span class="sxs-lookup"><span data-stu-id="c7f34-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7f34-161">LinkedIn Talent Hubiga integreerimine sõltub Dataverse for Human Resourcesi virtuaalsetest tabelites.</span><span class="sxs-lookup"><span data-stu-id="c7f34-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="c7f34-162">Selle seadistamisetapi eeltingimusena peate konfigureerima virtuaalsed tabeleid.</span><span class="sxs-lookup"><span data-stu-id="c7f34-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="c7f34-163">Lisateavet virtuaalsete tabelite konfigureerimise kohta leiate teemast [Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="c7f34-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

1. <span data-ttu-id="c7f34-164">Avage rakenduses Human Resources leht **Dataverse integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="c7f34-165">Valige vahekaart **Virtuaalsed tabelid**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="c7f34-166">Filtreerige üksuste loendit üksuse sildi järgi, et leida **LinkedIni ekspoditud kandidaat**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="c7f34-167">Valige üksus ja seejärel valige **Loo/värskenda**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="c7f34-168">Kandidaadi kirjete eksportimine</span><span class="sxs-lookup"><span data-stu-id="c7f34-168">Exporting candidate records</span></span>

<span data-ttu-id="c7f34-169">Pärast häälestuse lõpule viimist saavad värbajad ja Human Resourcesi (HR) professionaalid kasutada LinkedIn Talent Hubi funktsiooni **Ekspordi HRIS-i**, et eksportida palgatud kandidaadi kirjeid LinkedIni Talent Hubist Human Resourcesisse.</span><span class="sxs-lookup"><span data-stu-id="c7f34-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="c7f34-170">Kirjete eksportimine LinkedIn Talent Hubist</span><span class="sxs-lookup"><span data-stu-id="c7f34-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="c7f34-171">Kui kandidaat on liikunud värbamisprotsessist edasi ja on palgatud, saate eksportida kandidaadi kirje LinkedIn Talent Hubist Human Resourcesisse.</span><span class="sxs-lookup"><span data-stu-id="c7f34-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="c7f34-172">Avage LinkedIn Talent Hubis projekt, milleks uue töötaja palkasite.</span><span class="sxs-lookup"><span data-stu-id="c7f34-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="c7f34-173">Valige kandidaadi kirje.</span><span class="sxs-lookup"><span data-stu-id="c7f34-173">Select a candidate record.</span></span>

3. <span data-ttu-id="c7f34-174">Valige **Muuda etappi** ja seejärel **Palgatud**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="c7f34-175">Kandidaadi kolmikpunkti menüüs ( **...**) valige **Ekspordi HRIS-i**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="c7f34-176">Sisestage paanil **Ekspordi HRIS-i** teave, mis tuleb eksportida.</span><span class="sxs-lookup"><span data-stu-id="c7f34-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="c7f34-177">Valige väljal **HRIS-i pakkuja** suvand **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="c7f34-178">Valige väljal **Alguskuupäev** väärtus uue töövõtja jaoks.</span><span class="sxs-lookup"><span data-stu-id="c7f34-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="c7f34-179">Sisestage väljale **Ametinimetus** uue töövõtja töö ametinimetus.</span><span class="sxs-lookup"><span data-stu-id="c7f34-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="c7f34-180">Sisestage väljale **Asukoht** asukoht, kus töövõtja hakkab töötama.</span><span class="sxs-lookup"><span data-stu-id="c7f34-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="c7f34-181">Sisestage või kinnitage töövõtja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="c7f34-181">Enter or verify the employee's email address.</span></span>

![HRIS-i paanile eksportimine LinkedIn Talent Hubis](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="c7f34-183">Sisseelamise lõpule viimine Human Resourcesis</span><span class="sxs-lookup"><span data-stu-id="c7f34-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="c7f34-184">Kandidaadi kirjed, mis eksporditakse LinkedIn Talent Hubist Human Resourcesisse, kuvatakse lehe **Personalihaldus** jaotises **Palgatavad kandidaadid**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="c7f34-185">Avage rakenduses Human Resources loendi leht **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="c7f34-186">Valige jaotises **Palgatavad kandidaadid** valitud kandidaadi jaoks suvand **Palka**.</span><span class="sxs-lookup"><span data-stu-id="c7f34-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="c7f34-187">Vaadake dialoogiboksis **Uue töötaja palkamine** kirje läbi ja lisage nõutav teave.</span><span class="sxs-lookup"><span data-stu-id="c7f34-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="c7f34-188">Samuti saate valida ametikoha numbri, millele kandidaat palgati.</span><span class="sxs-lookup"><span data-stu-id="c7f34-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="c7f34-189">Kui nõutav teave on sisestatud, saate jätkata oma standardsete töövõtja kirjete loomise ja töövõtjate sisseelamise protsessidega.</span><span class="sxs-lookup"><span data-stu-id="c7f34-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="c7f34-190">Imporditakse järgmised üksikasjad ja lisatakse uue töötaja kirjesse.</span><span class="sxs-lookup"><span data-stu-id="c7f34-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="c7f34-191">Eesnimi</span><span class="sxs-lookup"><span data-stu-id="c7f34-191">First name</span></span>
- <span data-ttu-id="c7f34-192">Perekonnanimi</span><span class="sxs-lookup"><span data-stu-id="c7f34-192">Last name</span></span>
- <span data-ttu-id="c7f34-193">Töösuhte alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="c7f34-193">Employment start date</span></span>
- <span data-ttu-id="c7f34-194">Meiliaadress</span><span class="sxs-lookup"><span data-stu-id="c7f34-194">Email address</span></span>
- <span data-ttu-id="c7f34-195">Telefoninumber</span><span class="sxs-lookup"><span data-stu-id="c7f34-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="c7f34-196">Vt ka</span><span class="sxs-lookup"><span data-stu-id="c7f34-196">See also</span></span>

[<span data-ttu-id="c7f34-197">Dataverse'i virtuaalsete tabelite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c7f34-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="c7f34-198">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="c7f34-198">What is Microsoft Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]