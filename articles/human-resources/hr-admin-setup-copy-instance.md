---
title: Kopeeri eksemplar
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008704"
---
# <a name="copy-an-instance"></a><span data-ttu-id="e4296-102">Kopeeri eksemplar</span><span class="sxs-lookup"><span data-stu-id="e4296-102">Copy an instance</span></span>

<span data-ttu-id="e4296-103">Saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida rakenduse Microsoft Dynamics 365 Human Resources andmebaas liivakastikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="e4296-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="e4296-104">Kui teil on teine liivakastikeskkond, saate kopeerida andmebaasi ka sellest keskkonnast sihtkohaks olevasse liivakastikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="e4296-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="e4296-105">Eksemplari kopeerimiseks peate tagama järgneva.</span><span class="sxs-lookup"><span data-stu-id="e4296-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="e4296-106">Rakenduse Human Resources eksemplar, mida soovite üle kirjutada, peab olema liivakastikeskkond.</span><span class="sxs-lookup"><span data-stu-id="e4296-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="e4296-107">Keskkonnad, millest ja kuhu soovite kopeerida, peavad olema samas piirkonnas.</span><span class="sxs-lookup"><span data-stu-id="e4296-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="e4296-108">Piirkondade üleselt ei saa kopeerida.</span><span class="sxs-lookup"><span data-stu-id="e4296-108">You can't copy across regions.</span></span>

- <span data-ttu-id="e4296-109">Peate olema sihtkeskkonnas administraator, et saaksite pärast eksemplari kopeerimist sellesse sisse logida.</span><span class="sxs-lookup"><span data-stu-id="e4296-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="e4296-110">Rakenduse Human Resources andmebaasi kopeerimisel ei kopeerita elemente (rakendusi või andmeid), mis sisalduvad keskkonnas Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e4296-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="e4296-111">Teavet PowerAppsi keskkonnas elementide kopeerimise kohta vt teemast [Keskkonna kopeerimine](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="e4296-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="e4296-112">PowerAppsi keskkond, mida soovite üle kirjutada, peab olema liivakastikeskkond.</span><span class="sxs-lookup"><span data-stu-id="e4296-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="e4296-113">PowerAppsi tootmiskeskkonna muutmiseks liivakastikeskkonnaks peate olema rentniku üldadministraator.</span><span class="sxs-lookup"><span data-stu-id="e4296-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="e4296-114">Lisateavet PowerAppsi keskkonna muutmise kohta vt teemast [Eksemplari vahetamine](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="e4296-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="e4296-115">Rakenduse Human Resources andmebaasi kopeerimise mõjud</span><span class="sxs-lookup"><span data-stu-id="e4296-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="e4296-116">Rakenduse Human Resources andmebaasi kopeerimisel esinevad järgmised sündmused.</span><span class="sxs-lookup"><span data-stu-id="e4296-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="e4296-117">Kopeerimisprotsess kustutab sihtkeskkonnas olemasoleva andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="e4296-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="e4296-118">Kui kopeerimisprotsessi lõpetamist ei saa te olemasolevat andmebaasi taastada.</span><span class="sxs-lookup"><span data-stu-id="e4296-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="e4296-119">Sihtkeskkond ei ole saadaval enne, kui kopeerimisprotsess on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e4296-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="e4296-120">Microsoft Azure’i bloobimälu dokumente ei kopeerita ühest keskkonnast teise.</span><span class="sxs-lookup"><span data-stu-id="e4296-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="e4296-121">Seetõttu ei kopeerita ühtegi lisatud dokumenti ega malli ja need jäävad lähtekeskkonda.</span><span class="sxs-lookup"><span data-stu-id="e4296-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="e4296-122">Ükski kasutaja (v.a administraatorkasutajad ja teised sisemised teenusekasutajate kontod) pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="e4296-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="e4296-123">Seega saab administraatorkasutaja andmed kustutada või ebaselgeks muuta enne teiste kasutajate tagasi süsteemi lubamist.</span><span class="sxs-lookup"><span data-stu-id="e4296-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="e4296-124">Administraatorkasutaja peab tegema vajalikud konfiguratsiooni muudatused, nagu integratsiooni lõpp-punktide uuesti ühendamine kindlate teenuste või URL-idega.</span><span class="sxs-lookup"><span data-stu-id="e4296-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="e4296-125">Rakenduse Human Resources andmebaasi kopeerimine</span><span class="sxs-lookup"><span data-stu-id="e4296-125">Copy the Human Resources database</span></span>

<span data-ttu-id="e4296-126">Selle ülesande lõpetamiseks kopeerite esmalt eksemplar ja seejärel logige oma Microsoft Power Platformi halduskeskkonda sisse, et kopeerida PowerAppsi keskkond.</span><span class="sxs-lookup"><span data-stu-id="e4296-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="e4296-127">Eksemplari kopeerimisel andmebaas sihteksemplaris kustutatakse.</span><span class="sxs-lookup"><span data-stu-id="e4296-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="e4296-128">Sihteksemplar ei ole selle protsessi käigus saadaval.</span><span class="sxs-lookup"><span data-stu-id="e4296-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="e4296-129">Logige LCS-i sisse ja valige LCS-i projekt, mis sisaldab eksemplari, mida soovite kopeerida.</span><span class="sxs-lookup"><span data-stu-id="e4296-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="e4296-130">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="e4296-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="e4296-131">Valige kopeeritav eksemplar ja seejärel valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="e4296-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="e4296-132">Valige tööpaanil **Eksemplari kopeerimine** ülekirjutamiseks eksemplar ja seejärel valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="e4296-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="e4296-133">Oodake, kuni välja **Kopeerimise olek** väärtus uuendatakse suvandile **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="e4296-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="e4296-134">Ülekirjutamiseks eksemplari valimine</span><span class="sxs-lookup"><span data-stu-id="e4296-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="e4296-135">Valige **Power Platform** ja logige Microsoft Power Platformi halduskeskusesse sisse.</span><span class="sxs-lookup"><span data-stu-id="e4296-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="e4296-136">Power Platformi valimine</span><span class="sxs-lookup"><span data-stu-id="e4296-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="e4296-137">Valige kopeeritav PowerAppsi keskkond eksemplar ja seejärel valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="e4296-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="e4296-138">Kui kopeerimisprotsess on lõpule viidud, logige sihteksemplari sisse ja lubage Common Data Service’i integratsioon.</span><span class="sxs-lookup"><span data-stu-id="e4296-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="e4296-139">Lisateavet ja juhiseid vt teemast [Common Data Service’i integreerimise konfigureerimine](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="e4296-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="e4296-140">Andmeelemendid ja olekud</span><span class="sxs-lookup"><span data-stu-id="e4296-140">Data elements and statuses</span></span>

<span data-ttu-id="e4296-141">Rakenduse Human Resources eksemplari kopeerimisel järgmisi andmeelemene ei kopeerita.</span><span class="sxs-lookup"><span data-stu-id="e4296-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="e4296-142">Meiliaadressid tabelis **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="e4296-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="e4296-143">Pakett-töö ajalugu tabelites **BatchJobHistory**, **BatchHistory** ja **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="e4296-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="e4296-144">Simple Mail Transfer Protocoli (SMTP) parool tabelis **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="e4296-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="e4296-145">SMTP-edastusserver tabelis **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="e4296-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="e4296-146">Prindihalduse sätted tabelites **PrintMgmtSettings** ja **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="e4296-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="e4296-147">Keskkonnale spetsiifilised kirjed tabelites **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ja **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="e4296-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="e4296-148">Dokumendimanused tabelis DocuValue.</span><span class="sxs-lookup"><span data-stu-id="e4296-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="e4296-149">Need manused sisaldavad mis tahes Microsoft Office’i malle, mis on lähtekeskkonnas üle kirjutatud</span><span class="sxs-lookup"><span data-stu-id="e4296-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="e4296-150">Ühendusstring tabelis **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e4296-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="e4296-151">Osasid neist elementidest ei kopeerita, kuna need on keskkonnale spetsiifilised.</span><span class="sxs-lookup"><span data-stu-id="e4296-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="e4296-152">Näidete hulka kuuluvad kirjed **BatchServerConfig** ja **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="e4296-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="e4296-153">Teisi elemente tugiteenusepiletite mahu tõttu ei kopeerita.</span><span class="sxs-lookup"><span data-stu-id="e4296-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="e4296-154">Näiteks võidakse saata topeltmeile, kuna SMTP on kasutaja aktsepteerimise testimise (liivakasti) keskkonnas endiselt lubatud, kehtetu integreerimise sõnumeid võidakse saata, kuna pakett-tööd on endiselt lubatud, ja kasutajad võivad olla lubatud enne, kui administraatorid saavad teostada värskendamisjärgseid puhastustoiminguid.</span><span class="sxs-lookup"><span data-stu-id="e4296-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="e4296-155">Lisaks muutuvad eksemplari kopeerimisel järgmised olekud.</span><span class="sxs-lookup"><span data-stu-id="e4296-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="e4296-156">Kõik kasutajad peale administraatori seatakse olekusse **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="e4296-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="e4296-157">Kõik pakett-tööd, välja arvatud mõned süsteemi tööd, seatakse olekusse **Kinnipeetud**.</span><span class="sxs-lookup"><span data-stu-id="e4296-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="e4296-158">Kekkonna administraator</span><span class="sxs-lookup"><span data-stu-id="e4296-158">Environment admin</span></span>

<span data-ttu-id="e4296-159">Kõik liivakasti sihtkeskkonna kasutajad (sh administraatorid) asendatakse lähtekeskkonna kasutajatega.</span><span class="sxs-lookup"><span data-stu-id="e4296-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="e4296-160">Enne eksemplari kopeerimist veenduge, et oleksite sihtkeskkonnas administraator.</span><span class="sxs-lookup"><span data-stu-id="e4296-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="e4296-161">Kui te seda ei ole, ei saa te pärast kopeerimise lõpetamist liivakasti sihtkeskkonda sisse logida.</span><span class="sxs-lookup"><span data-stu-id="e4296-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="e4296-162">Kõik mitte-administraatorist kasutajad liivakasti sihtkeskkonnas keelatakse, et välistada liivakasti keskkonnas soovimatuid sisselogimisi.</span><span class="sxs-lookup"><span data-stu-id="e4296-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="e4296-163">Administraatorid saavad vajadusel kasutajaid uuesti lubada.</span><span class="sxs-lookup"><span data-stu-id="e4296-163">Administrators can reenable users if needed.</span></span>
