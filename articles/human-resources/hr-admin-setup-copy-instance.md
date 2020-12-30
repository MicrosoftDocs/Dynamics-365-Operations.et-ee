---
title: Kopeeri eksemplar
description: Saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida rakenduse Microsoft Dynamics 365 Human Resources andmebaas liivakastikeskkonda.
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40ca0a4d9733fc2a163daa4ea1c27a3bfae6d3bf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527833"
---
# <a name="copy-an-instance"></a><span data-ttu-id="3768d-103">Kopeeri eksemplar</span><span class="sxs-lookup"><span data-stu-id="3768d-103">Copy an instance</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3768d-104">Saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida rakenduse Microsoft Dynamics 365 Human Resources andmebaas liivakastikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="3768d-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="3768d-105">Kui teil on teine liivakastikeskkond, saate kopeerida andmebaasi ka sellest keskkonnast sihtkohaks olevasse liivakastikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="3768d-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="3768d-106">Eksemplari kopeerimiseks pidage meeles järgmisi nõuandeid.</span><span class="sxs-lookup"><span data-stu-id="3768d-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="3768d-107">Rakenduse Human Resources eksemplar, mida soovite üle kirjutada, peab olema liivakastikeskkond.</span><span class="sxs-lookup"><span data-stu-id="3768d-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="3768d-108">Keskkonnad, millest ja kuhu soovite kopeerida, peavad olema samas piirkonnas.</span><span class="sxs-lookup"><span data-stu-id="3768d-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="3768d-109">Piirkondade üleselt ei saa kopeerida.</span><span class="sxs-lookup"><span data-stu-id="3768d-109">You can't copy across regions.</span></span>

- <span data-ttu-id="3768d-110">Peate olema sihtkeskkonnas administraator, et saaksite pärast eksemplari kopeerimist sellesse sisse logida.</span><span class="sxs-lookup"><span data-stu-id="3768d-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="3768d-111">Rakenduse Human Resources andmebaasi kopeerimisel ei kopeerita elemente (rakendusi või andmeid), mis sisalduvad keskkonnas Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3768d-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="3768d-112">Teavet Power Appsi keskkonnas elementide kopeerimise kohta vt teemast [Keskkonna kopeerimine](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="3768d-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="3768d-113">Power Appsi keskkond, mida soovite üle kirjutada, peab olema liivakastikeskkond.</span><span class="sxs-lookup"><span data-stu-id="3768d-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="3768d-114">Power Appsi tootmiskeskkonna muutmiseks liivakastikeskkonnaks peate olema rentniku üldadministraator.</span><span class="sxs-lookup"><span data-stu-id="3768d-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="3768d-115">Lisateavet Power Appsi keskkonna muutmise kohta vt teemast [Eksemplari vahetamine](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="3768d-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="3768d-116">Kui kopeerite eksemplari oma liivakastikeskkonda ja soovite oma liivakastikeskkonda integreerida Common Data Service'iga, peate uuesti rakendama kohandatud väljad Common Data Service'i üksustele.</span><span class="sxs-lookup"><span data-stu-id="3768d-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span> <span data-ttu-id="3768d-117">Lugege teemat [Kohandatud väljade rakendamine teenuses Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="3768d-117">See [Apply custom fields to Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="3768d-118">Rakenduse Human Resources andmebaasi kopeerimise mõjud</span><span class="sxs-lookup"><span data-stu-id="3768d-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="3768d-119">Rakenduse Human Resources andmebaasi kopeerimisel esinevad järgmised sündmused.</span><span class="sxs-lookup"><span data-stu-id="3768d-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="3768d-120">Kopeerimisprotsess kustutab sihtkeskkonnas olemasoleva andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="3768d-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="3768d-121">Kui kopeerimisprotsessi lõpetamist ei saa te olemasolevat andmebaasi taastada.</span><span class="sxs-lookup"><span data-stu-id="3768d-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="3768d-122">Sihtkeskkond ei ole saadaval enne, kui kopeerimisprotsess on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="3768d-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="3768d-123">Microsoft Azure’i bloobimälu dokumente ei kopeerita ühest keskkonnast teise.</span><span class="sxs-lookup"><span data-stu-id="3768d-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="3768d-124">Selle tulemusena ei kopeerita ühtegi lisatud dokumenti ega malli ja need jäävad lähtekeskkonda.</span><span class="sxs-lookup"><span data-stu-id="3768d-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="3768d-125">Ükski kasutaja (v.a administraatorkasutajad ja teised sisemised teenusekasutajate kontod) pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="3768d-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="3768d-126">Administraatorkasutaja andmed kustutada või ebaselgeks muuta enne teiste kasutajate tagasi süsteemi lubamist.</span><span class="sxs-lookup"><span data-stu-id="3768d-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="3768d-127">Administraatorkasutaja peab tegema vajalikud konfiguratsiooni muudatused, nagu integratsiooni lõpp-punktide uuesti ühendamine kindlate teenuste või URL-idega.</span><span class="sxs-lookup"><span data-stu-id="3768d-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="3768d-128">Rakenduse Human Resources andmebaasi kopeerimine</span><span class="sxs-lookup"><span data-stu-id="3768d-128">Copy the Human Resources database</span></span>

<span data-ttu-id="3768d-129">Selle ülesande lõpetamiseks kopeerite esmalt eksemplar ja seejärel logige oma Microsoft Power Platformi halduskeskkonda sisse, et kopeerida Power Appsi keskkond.</span><span class="sxs-lookup"><span data-stu-id="3768d-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="3768d-130">Eksemplari kopeerimisel andmebaas sihteksemplaris kustutatakse.</span><span class="sxs-lookup"><span data-stu-id="3768d-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="3768d-131">Sihteksemplar ei ole selle protsessi käigus saadaval.</span><span class="sxs-lookup"><span data-stu-id="3768d-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="3768d-132">Logige LCS-i sisse ja valige LCS-i projekt, mis sisaldab eksemplari, mida soovite kopeerida.</span><span class="sxs-lookup"><span data-stu-id="3768d-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="3768d-133">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="3768d-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="3768d-134">Valige kopeeritav eksemplar ja seejärel valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="3768d-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="3768d-135">Valige tööpaanil **Eksemplari kopeerimine** ülekirjutamiseks eksemplar ja seejärel valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="3768d-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="3768d-136">Oodake, kuni välja **Kopeerimise olek** väärtus uuendatakse suvandile **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="3768d-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="3768d-137">Ülekirjutamiseks eksemplari valimine</span><span class="sxs-lookup"><span data-stu-id="3768d-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="3768d-138">Valige **Power Platform** ja logige Microsoft Power Platformi halduskeskusesse sisse.</span><span class="sxs-lookup"><span data-stu-id="3768d-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="3768d-139">Power Platformi valimine</span><span class="sxs-lookup"><span data-stu-id="3768d-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="3768d-140">Valige kopeeritav Power Appsi keskkond eksemplar ja seejärel valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="3768d-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="3768d-141">Kui kopeerimisprotsess on lõpule viidud, logige sihteksemplari sisse ja lubage Common Data Service’i integratsioon.</span><span class="sxs-lookup"><span data-stu-id="3768d-141">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="3768d-142">Lisateavet ja juhiseid vt teemast [Common Data Service’i integreerimise konfigureerimine](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="3768d-142">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="3768d-143">Andmeelemendid ja olekud</span><span class="sxs-lookup"><span data-stu-id="3768d-143">Data elements and statuses</span></span>

<span data-ttu-id="3768d-144">Rakenduse Human Resources eksemplari kopeerimisel järgmisi andmeelemene ei kopeerita.</span><span class="sxs-lookup"><span data-stu-id="3768d-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="3768d-145">Meiliaadressid tabelis **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="3768d-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="3768d-146">Pakett-töö ajalugu tabelites **BatchJobHistory**, **BatchHistory** ja **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="3768d-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="3768d-147">Simple Mail Transfer Protocoli (SMTP) parool tabelis **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="3768d-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="3768d-148">SMTP-edastusserver tabelis **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="3768d-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="3768d-149">Prindihalduse sätted tabelites **PrintMgmtSettings** ja **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="3768d-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="3768d-150">Keskkonnale spetsiifilised kirjed tabelites **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ja **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="3768d-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="3768d-151">Dokumendimanused tabelis DocuValue.</span><span class="sxs-lookup"><span data-stu-id="3768d-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="3768d-152">Need manused sisaldavad mis tahes Microsoft Office’i malle, mis on lähtekeskkonnas üle kirjutatud</span><span class="sxs-lookup"><span data-stu-id="3768d-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="3768d-153">Ühendusstring tabelis **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3768d-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="3768d-154">Osasid neist elementidest ei kopeerita, kuna need on keskkonnale spetsiifilised.</span><span class="sxs-lookup"><span data-stu-id="3768d-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="3768d-155">Näidete hulka kuuluvad kirjed **BatchServerConfig** ja **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="3768d-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="3768d-156">Teisi elemente tugiteenusepiletite mahu tõttu ei kopeerita.</span><span class="sxs-lookup"><span data-stu-id="3768d-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="3768d-157">Näide:</span><span class="sxs-lookup"><span data-stu-id="3768d-157">For example:</span></span>

- <span data-ttu-id="3768d-158">Topeltmeile võidakse saata, kuna SMTP on kasutaja nõusoleku testimise (liivakasti) keskkonnas endiselt lubatud.</span><span class="sxs-lookup"><span data-stu-id="3768d-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="3768d-159">Sobimatuid integratsiooniteated võidakse saata, kuna pakett-tööd on endiselt lubatud.</span><span class="sxs-lookup"><span data-stu-id="3768d-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="3768d-160">Kasutajad võivad olla lubatud enne, kui administraatorid saavad teha värskendamisjärgseid puhastustoiminguid.</span><span class="sxs-lookup"><span data-stu-id="3768d-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="3768d-161">Samuti muutuvad eksemplari kopeerimisel järgmised olekud.</span><span class="sxs-lookup"><span data-stu-id="3768d-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="3768d-162">Kõik kasutajad peale administraatori seatakse olekusse **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="3768d-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="3768d-163">Kõik pakett-tööd, välja arvatud mõned süsteemi tööd, seatakse olekusse **Kinnipeetud**.</span><span class="sxs-lookup"><span data-stu-id="3768d-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="3768d-164">Kekkonna administraator</span><span class="sxs-lookup"><span data-stu-id="3768d-164">Environment admin</span></span>

<span data-ttu-id="3768d-165">Kõik liivakasti sihtkeskkonna kasutajad (sh administraatorid) asendatakse lähtekeskkonna kasutajatega.</span><span class="sxs-lookup"><span data-stu-id="3768d-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="3768d-166">Enne eksemplari kopeerimist veenduge, et oleksite lähtekeskkonnas administraator.</span><span class="sxs-lookup"><span data-stu-id="3768d-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="3768d-167">Kui te seda ei ole, ei saa te pärast kopeerimise lõpetamist liivakasti sihtkeskkonda sisse logida.</span><span class="sxs-lookup"><span data-stu-id="3768d-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="3768d-168">Kõik mitte-administraatorist kasutajad liivakasti sihtkeskkonnas keelatakse, et välistada liivakasti keskkonnas soovimatuid sisselogimisi.</span><span class="sxs-lookup"><span data-stu-id="3768d-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="3768d-169">Administraatorid saavad vajadusel kasutajaid uuesti lubada.</span><span class="sxs-lookup"><span data-stu-id="3768d-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-common-data-service"></a><span data-ttu-id="3768d-170">Kohandatud väljade rakendamine teenuses Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3768d-170">Apply custom fields to Common Data Service</span></span>

<span data-ttu-id="3768d-171">Kui kopeerite eksemplari oma liivakastikeskkonda ja soovite oma liivakastikeskkonda integreerida Common Data Service'iga, peate uuesti rakendama kohandatud väljad Common Data Service'i üksustele.</span><span class="sxs-lookup"><span data-stu-id="3768d-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span>

<span data-ttu-id="3768d-172">Iga Common Data Service'i üksustes avatud kohandatud välja puhul tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3768d-172">For each custom field that's exposed on Common Data Service entities, do the following steps:</span></span>

1. <span data-ttu-id="3768d-173">Minge kohandatud väljale ja valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3768d-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="3768d-174">Tühistage väli **Lubatud** iga cdm_\* üksuse jaoks, millel kohandatud väli on lubatud.</span><span class="sxs-lookup"><span data-stu-id="3768d-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="3768d-175">Valige **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="3768d-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="3768d-176">Valige uuesti käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3768d-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="3768d-177">Valige väli **Lubatud** iga cdm_\* üksuse jaoks, millel kohandatud väli on lubatud.</span><span class="sxs-lookup"><span data-stu-id="3768d-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="3768d-178">Valige uuesti **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="3768d-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="3768d-179">Valiku tühistamine, muudatuste rakendamine, uuesti valimine ja muudatuste uuesti rakendamine palub skeemil teha teenuses Common Data Service värskendusi kohandatud väljade kaasamiseks.</span><span class="sxs-lookup"><span data-stu-id="3768d-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Common Data Service to include the custom fields.</span></span>

<span data-ttu-id="3768d-180">Lisateavet kohandatud väljade kohta leiate teemast [Kohandatud väljade loomine ja nendega töötamine](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="3768d-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="3768d-181">Vt ka</span><span class="sxs-lookup"><span data-stu-id="3768d-181">See also</span></span>

[<span data-ttu-id="3768d-182">Human Resources ettevalmistus</span><span class="sxs-lookup"><span data-stu-id="3768d-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="3768d-183">Eemalda eksemplar</span><span class="sxs-lookup"><span data-stu-id="3768d-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="3768d-184">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="3768d-184">Update process</span></span>](hr-admin-setup-update-process.md)

