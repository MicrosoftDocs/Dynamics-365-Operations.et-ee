---
title: Üldine tõrkeotsing
description: See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c3352afd93dfc7c37a8af9dabaf85b7a1debad30
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997250"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="f7679-103">Üldine tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="f7679-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f7679-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="f7679-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7679-105">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="f7679-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="f7679-106">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="f7679-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="f7679-107">Kui üritate installida tööriista Package Deployer abil topeltkirjutuse paketti, ei kuvata ühtegi saadaolevat lahendust</span><span class="sxs-lookup"><span data-stu-id="f7679-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="f7679-108">Mõni tööriista Package Deployer versioon ei ühildu topeltkirjutuse lahenduse paketiga.</span><span class="sxs-lookup"><span data-stu-id="f7679-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="f7679-109">Paketi edukaks installimiseks kasutage kindlasti tööriista Package Deployer [versiooni 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) või uuemat.</span><span class="sxs-lookup"><span data-stu-id="f7679-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="f7679-110">Pärast tööriista Package Deployer installimist installige lahendusepakett, järgides neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="f7679-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="f7679-111">Uusima lahenduse paketi faili saate alla laadida lehelt Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="f7679-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="f7679-112">Pärast paketi ZIP-faili allalaadimist paremklõpsake seda ja valige **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="f7679-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="f7679-113">Valige märkeruut **Tühista blokeerimine** ja valige seejärel **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="f7679-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="f7679-114">Kui märkeruutu **Tühista blokeerimine** ei kuvata, on ZIP-fail juba blokeeritud ja võite selle toimingu vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="f7679-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Atribuutide dialoogiboks](media/unblock_option.png)

2. <span data-ttu-id="f7679-116">Ekstraktige paketi ZIP-fail ja kopeerige kõik failid kaustas **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="f7679-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Kausta Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 sisu](media/extract_package.png)

3. <span data-ttu-id="f7679-118">Kleepige kõik kopeeritud failid tööriista Package Deployer kausta **Tööriistad**.</span><span class="sxs-lookup"><span data-stu-id="f7679-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="f7679-119">Käivitage **PackageDeployer.exe** Common Data Service'i keskkonna valimiseks ja lahenduste installimiseks.</span><span class="sxs-lookup"><span data-stu-id="f7679-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Kausta Tööriistad sisu](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="f7679-121">Common Data Service'i lisandmooduli jälituslogide lubamine ja kuvamine tõrke üksikasjade kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="f7679-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="f7679-122">**Jälituslogi sisselülitamiseks ja tõrgete kuvamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="f7679-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="f7679-123">Jälituslogi sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f7679-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="f7679-124">Logige sisse mudelipõhisesse rakendusse Dynamics 365, avage leht **Sätted** ja valige seejärel jaotises **Süsteem** suvand **Haldus**.</span><span class="sxs-lookup"><span data-stu-id="f7679-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System** , select **Administration**.</span></span>
2. <span data-ttu-id="f7679-125">Valige lehelt **Haldus** suvand **Süsteemisätted**.</span><span class="sxs-lookup"><span data-stu-id="f7679-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="f7679-126">Lisandmooduli jälituslogi lubamiseks valige vahekaardil **Kohandamine** väljal **Lisandmooduli ja kohandatud töövoo tegevuse jälgimine** suvand **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="f7679-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="f7679-127">Kui soovite logida jälituslogisid ainult erandite ilmnemisel, saate teha valiku **Erand**.</span><span class="sxs-lookup"><span data-stu-id="f7679-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="f7679-128">Jälituslogi kuvamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f7679-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="f7679-129">Logige sisse mudelipõhisesse rakendusse Dynamics 365, avage leht **Sätted** ja valige seejärel jaotises **Kohandamine** suvand **Lisandmooduli jälituslogi**.</span><span class="sxs-lookup"><span data-stu-id="f7679-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization** , select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="f7679-130">Leiate jälituslogid siis, kui välja **Tüübi nimi** väärtuseks on seatud **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="f7679-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="f7679-131">Täieliku logi vaatamiseks topeltklõpsake üksust ja seejärel vaadake üle kiirkaardil **Käivitamine** tekst **Teateplokk**.</span><span class="sxs-lookup"><span data-stu-id="f7679-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="f7679-132">Silumisrežiim lubamine tõrkeotsingu reaalajas sünkroonimise probleemide korral Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="f7679-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="f7679-133">**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator. Common Data Service'ist pärinevaid topeltkirjutuse tõrkeid võidakse kuvada Finance and Operationsi rakenduses.</span><span class="sxs-lookup"><span data-stu-id="f7679-133">**Required role to view the errors:** System admin Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="f7679-134">Mõnel juhul ei ole tõrketeate täistekst saadaval, kuna sõnum on liiga pikk või sisaldab tuvastamist võimaldavaid andmeid (PII).</span><span class="sxs-lookup"><span data-stu-id="f7679-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="f7679-135">Verbose tõrgete logimise saate sisse lülitada järgmiste juhiste abil.</span><span class="sxs-lookup"><span data-stu-id="f7679-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="f7679-136">Kõigil Finance and Operationsi rakenduste projekti konfiguratsioonidel on atribuut **IsDebugMode** üksusel **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f7679-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="f7679-137">Üksuse **DualWriteProjectConfiguration** avamine Exceli lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="f7679-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="f7679-138">Kõige lihtsam on üksust avada režiimi **Kujundus** sisselülitamisel Exceli lisandmoodulis ja seejärel lisada töölehele üksus **DualWriteProjectConfigurationEntity**.</span><span class="sxs-lookup"><span data-stu-id="f7679-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="f7679-139">Lisateabe saamiseks vt [Üksuse andmete avamine Excelis ja andmete värskendamine Exceli lisandmooduliga](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="f7679-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="f7679-140">Seadke projekti atribuudi **IsDebugMode** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f7679-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="f7679-141">Käivitage stsenaarium, mis tekitab tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="f7679-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="f7679-142">Verbose logid on saadaval tabelis DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="f7679-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="f7679-143">Tabeli brauseris andmete otsimiseks kasutage järgmist URL-i (asendage **XXX** vastavalt vajadusele):</span><span class="sxs-lookup"><span data-stu-id="f7679-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="f7679-144">Rakenduse Finance and Operations virtuaalarvuti sünkroonimistõrgete kontrollimine</span><span class="sxs-lookup"><span data-stu-id="f7679-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="f7679-145">**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="f7679-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="f7679-146">Microsoft Dynamics Lifecycle Services’i (LCS) sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="f7679-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="f7679-147">Avage LCS-i projekt, mille valisite topeltkirjutamise testimiseks.</span><span class="sxs-lookup"><span data-stu-id="f7679-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="f7679-148">Valige paan **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="f7679-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="f7679-149">Kasutage rakenduse Finance and Operations virtuaalarvutisse (VM) sisselogimiseks kaugtöölauda.</span><span class="sxs-lookup"><span data-stu-id="f7679-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="f7679-150">Kasutage LCS-is kuvatud kohalikku kontot.</span><span class="sxs-lookup"><span data-stu-id="f7679-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="f7679-151">Avage sündmusevaatur.</span><span class="sxs-lookup"><span data-stu-id="f7679-151">Open Event viewer.</span></span>
6. <span data-ttu-id="f7679-152">Valige **Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> AX-DualWriteSync \> Toiming**.</span><span class="sxs-lookup"><span data-stu-id="f7679-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="f7679-153">Vaadake läbi hiljutiste tõrgete loend.</span><span class="sxs-lookup"><span data-stu-id="f7679-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="f7679-154">Linkimise tühistamine ja teise Common Data Service'i keskkonna linkimine Finance and Operationsi rakendusest</span><span class="sxs-lookup"><span data-stu-id="f7679-154">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="f7679-155">**Keskkonna linkimise tühistamiseks nõutav roll:** kas Finance and Operationsi rakenduse või teenuse Common Data Service süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="f7679-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Common Data Service.</span></span>

1. <span data-ttu-id="f7679-156">Logige rakendusse Finance and Operations sisse.</span><span class="sxs-lookup"><span data-stu-id="f7679-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="f7679-157">Avage **Tööruumid \>Andmehaldus** ja valige paan **Topeltkirjutus**.</span><span class="sxs-lookup"><span data-stu-id="f7679-157">Go to **Workspaces \> Data management** , and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="f7679-158">Valige kõik töötavad vastendused ja valige **Peata**.</span><span class="sxs-lookup"><span data-stu-id="f7679-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="f7679-159">Valige nupp **Tühista keskkonna link**.</span><span class="sxs-lookup"><span data-stu-id="f7679-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="f7679-160">Toimingu kinnitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f7679-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="f7679-161">Nüüd saate linkida uue keskkonna.</span><span class="sxs-lookup"><span data-stu-id="f7679-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="f7679-162">Müügitellimuse rea teabevormi ei saa kuvada</span><span class="sxs-lookup"><span data-stu-id="f7679-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="f7679-163">Kui loote müügitellimuse rakenduses Dynamics 365 Sales, võib nupu **+ Lisa tooted** klõpsamine suunata teid rakenduse Dynamics 365 Project Operation tellimuserea vormile.</span><span class="sxs-lookup"><span data-stu-id="f7679-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="f7679-164">Sellel vormil ei saa vaadata müügitellimuse rea vormi **Teave**.</span><span class="sxs-lookup"><span data-stu-id="f7679-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="f7679-165">Ripploendis ei kuvata suvandi **Uus tellimuse rida** all suvandit **Teave**.</span><span class="sxs-lookup"><span data-stu-id="f7679-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="f7679-166">See juhtub, kuna teie keskkonnas on installitud rakendus Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f7679-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="f7679-167">Vormisuvandi **Teave** uuesti lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f7679-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="f7679-168">Avage üksus **Tellimuse rida**.</span><span class="sxs-lookup"><span data-stu-id="f7679-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="f7679-169">Leidke vormide sõlme alt vorm **Teave**.</span><span class="sxs-lookup"><span data-stu-id="f7679-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="f7679-170">Valige vorm **Teave** ja klõpsake **Luba turberollid**.</span><span class="sxs-lookup"><span data-stu-id="f7679-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="f7679-171">Seadke turbesäte väärtusele **Kuva kõigile**.</span><span class="sxs-lookup"><span data-stu-id="f7679-171">Change the security setting to **Display to everyone**.</span></span>
