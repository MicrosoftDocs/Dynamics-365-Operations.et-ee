---
title: "Kulujuhtimise mobiilne tööruum"
description: "Teema annab teavet kulujuhtimise mobiilse tööruumi kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6019634c47bd97fb16ea8aaf029ea176f095b8b6
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="d8e62-104">Kulujuhtimise mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="d8e62-104">Cost controlling mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d8e62-105">Teema annab teavet **kulujuhtimise** mobiilse tööruumi kohta.</span><span class="sxs-lookup"><span data-stu-id="d8e62-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="d8e62-106">See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal.</span><span class="sxs-lookup"><span data-stu-id="d8e62-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="d8e62-107">See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="d8e62-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="d8e62-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d8e62-108">Overview</span></span>
<span data-ttu-id="d8e62-109">Mobiilne tööruum **Kulujuhtimine** annab kiire ülevaate kulukeskuste praegusest jõudlusest, võrreldes tegelikke kulusid eelarvestatud kuludega.</span><span class="sxs-lookup"><span data-stu-id="d8e62-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="d8e62-110">Saate üksikute kuluelementide olekut ka sügavuti uurida.</span><span class="sxs-lookup"><span data-stu-id="d8e62-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="d8e62-111">Näiteks saab töövõtja kutse rahvusvahelisele konverentsile, kuid organisatsioon peab tasuma kõik reisikulud.</span><span class="sxs-lookup"><span data-stu-id="d8e62-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="d8e62-112">Töötaja küsib oma juhilt, kas ta saab konverentsil osaleda.</span><span class="sxs-lookup"><span data-stu-id="d8e62-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="d8e62-113">Juht avab oma mobiiltelefonis kiiresti mobiilse tööruumi **Kulujuhtimine**, et näha, kas tal on töövõtja konverentsil osalemiseks olemas piisav eelarve.</span><span class="sxs-lookup"><span data-stu-id="d8e62-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="d8e62-114">Andmeturve</span><span class="sxs-lookup"><span data-stu-id="d8e62-114">Data security</span></span>
<span data-ttu-id="d8e62-115">Mobiilses tööruumis **Kulujuhtimine** olevad andmed on kaitstud kasutaja identimisteabe kaudu.</span><span class="sxs-lookup"><span data-stu-id="d8e62-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="d8e62-116">Kulukeskuse juhtidel on õigus näha vaid oma enda kulukeskuse andmeid.</span><span class="sxs-lookup"><span data-stu-id="d8e62-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="d8e62-117">Juurdepääsu turbetaset hallatakse moodulis **Kuluarvestus**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="d8e62-118">Kuluarvestajad määratlevad mobiilse tööruumi **Kulujuhtimine** konfiguratsiooni moodulis **Kuluarvestus**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="d8e62-119">Kui tööruum on mobiilirakenduses avaldatud, on see rakenduses saadaval.</span><span class="sxs-lookup"><span data-stu-id="d8e62-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="d8e62-120">Seega saavad kõik organisatsiooni kulukeskuse juhid vaadata andmeid samas vormingus.</span><span class="sxs-lookup"><span data-stu-id="d8e62-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="d8e62-121">Toimingud, vaated ja lingid</span><span class="sxs-lookup"><span data-stu-id="d8e62-121">Actions, views, and links</span></span>
<span data-ttu-id="d8e62-122">**Kulujuhtimise** mobiilne tööruum pakub järgmisi toiminguid, vaateid ja linke.</span><span class="sxs-lookup"><span data-stu-id="d8e62-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="d8e62-123">**Tegevused**</span><span class="sxs-lookup"><span data-stu-id="d8e62-123">**Actions:**</span></span>

    -   <span data-ttu-id="d8e62-124">Paigutuse valimine sätte **Vali konfiguratsioon** kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="d8e62-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="d8e62-125">Sätte **Vali kuluobjekt** kasutamine kulukeskuste valimiseks, mille andmeid filtrida.</span><span class="sxs-lookup"><span data-stu-id="d8e62-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="d8e62-126">Loendis ilmuvad kulukeskused sõltuvad moodulis **Kuluarvestus** antud juurdepääsuõigustest.</span><span class="sxs-lookup"><span data-stu-id="d8e62-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="d8e62-127">**Vaated.** Olenevalt moodulis **Kuluarvestus** valitud toimingutest ja konfiguratsiooni häälestusest saate vaadata kaartidel järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="d8e62-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="d8e62-128">Tegelik võrreldes eelarvega (praegune periood)</span><span class="sxs-lookup"><span data-stu-id="d8e62-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="d8e62-129">Tegelik võrreldes parandatud eelarvega (praegune periood)</span><span class="sxs-lookup"><span data-stu-id="d8e62-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="d8e62-130">Tegelik võrreldes eelarvega (eelmine periood)</span><span class="sxs-lookup"><span data-stu-id="d8e62-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="d8e62-131">Tegelik võrreldes parandatud eelarvega (eelmine periood)</span><span class="sxs-lookup"><span data-stu-id="d8e62-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="d8e62-132">Tegelik võrreldes eelarvega (aasta tänaseni)</span><span class="sxs-lookup"><span data-stu-id="d8e62-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="d8e62-133">Tegelik võrreldes parandatud eelarvega (aasta tänaseni)</span><span class="sxs-lookup"><span data-stu-id="d8e62-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="d8e62-134">Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, hälve ja hälbe protsent.</span><span class="sxs-lookup"><span data-stu-id="d8e62-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="d8e62-135">**Lingid**</span><span class="sxs-lookup"><span data-stu-id="d8e62-135">**Links:**</span></span>

    -   <span data-ttu-id="d8e62-136">Praeguse perioodi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="d8e62-136">Details for current period</span></span>
    -   <span data-ttu-id="d8e62-137">Eelmise perioodi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="d8e62-137">Details for previous period</span></span>
    -   <span data-ttu-id="d8e62-138">Aasta tänaseni üksikasjad</span><span class="sxs-lookup"><span data-stu-id="d8e62-138">Details for year to date</span></span>

    <span data-ttu-id="d8e62-139">Lingi valimisel kuvatakse iga kuluelemendi kaart.</span><span class="sxs-lookup"><span data-stu-id="d8e62-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="d8e62-140">Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, eelarvehälve, eelarvehälbe protsent, parandatud eelarve, parandatud eelarvehälve ja parandatud eelarvehälbe protsent.</span><span class="sxs-lookup"><span data-stu-id="d8e62-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="d8e62-141">[![Kuluelemendi kaart ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="d8e62-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d8e62-142">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="d8e62-142">Prerequisites</span></span>
<span data-ttu-id="d8e62-143">Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.</span><span class="sxs-lookup"><span data-stu-id="d8e62-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="d8e62-144">Eeltingimused lahenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni 2017. aasta juuli värskenduse kasutamisel</span><span class="sxs-lookup"><span data-stu-id="d8e62-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span>
<span data-ttu-id="d8e62-145">Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni 2017. aasta juuli värskendus, peab süsteemiadministraator avaldama **kulujuhtimise** mobiilse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="d8e62-145">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="d8e62-146">Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="d8e62-146">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="d8e62-147">Eeltingimused Microsoft Dynamics 365 for Operationsi versiooni 1611 platvormivärskendusega 3 või uuema kasutamisel</span><span class="sxs-lookup"><span data-stu-id="d8e62-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="d8e62-148">Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="d8e62-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d8e62-149">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="d8e62-149">Prerequisite</span></span></th>
<th><span data-ttu-id="d8e62-150">Roll</span><span class="sxs-lookup"><span data-stu-id="d8e62-150">Role</span></span></th>
<th><span data-ttu-id="d8e62-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d8e62-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8e62-152">Rakendage KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="d8e62-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="d8e62-153">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="d8e62-153">System administrator</span></span></td>

<td><span data-ttu-id="d8e62-154">KB 4013633 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Kulujuhtimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8e62-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="d8e62-155">KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d8e62-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="d8e62-156"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="d8e62-156"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="d8e62-157"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</span><span class="sxs-lookup"><span data-stu-id="d8e62-157"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="d8e62-158"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</span><span class="sxs-lookup"><span data-stu-id="d8e62-158"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="d8e62-159"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</span><span class="sxs-lookup"><span data-stu-id="d8e62-159"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8e62-160">Avaldage <strong>kulujuhtimise</strong> mobiilne tööruum.</span><span class="sxs-lookup"><span data-stu-id="d8e62-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="d8e62-161">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="d8e62-161">System administrator</span></span></td>
<td><span data-ttu-id="d8e62-162">Vt jaotist <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="d8e62-162">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d8e62-163">Laadige alla ja installige mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="d8e62-163">Download and install the mobile app</span></span>
<span data-ttu-id="d8e62-164">Laadige alla ja installige Dynamics 365 for Unified Operationsi mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="d8e62-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="d8e62-165">Androidi telefonidele</span><span class="sxs-lookup"><span data-stu-id="d8e62-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d8e62-166">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="d8e62-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d8e62-167">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="d8e62-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="d8e62-168">Käivitage rakendus oma mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="d8e62-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d8e62-169">Sisestage Dynamics 365 URL.</span><span class="sxs-lookup"><span data-stu-id="d8e62-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d8e62-170">Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="d8e62-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d8e62-171">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="d8e62-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="d8e62-172">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="d8e62-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d8e62-173">Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.</span><span class="sxs-lookup"><span data-stu-id="d8e62-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="d8e62-174">[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d8e62-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="d8e62-175">Kasutage oma kulukeskuse jõudluse vaatamiseks mobiilset tööruumi Kulujuhtimine</span><span class="sxs-lookup"><span data-stu-id="d8e62-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="d8e62-176">Valige oma mobiilses seadmes tööruum **Kulujuhtimine**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="d8e62-177">Valige suvand **Kuluobjekti juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="d8e62-178">Valige suvand **Tegevused**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="d8e62-179">Kulujuhtimise paigutuse valimiseks valige **Konfiguratsiooni valimine**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="d8e62-180">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-180">Select **Done**.</span></span>
6.  <span data-ttu-id="d8e62-181">Valige suvand **Tegevused**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="d8e62-182">Valige suvand **Kuluobjekti valimine**, et valida kulukeskused, millele on teile juurdepääs antud.</span><span class="sxs-lookup"><span data-stu-id="d8e62-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="d8e62-183">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-183">Select **Done**.</span></span>
9.  <span data-ttu-id="d8e62-184">Kulukeskuse üldise jõudluse vaatamine.</span><span class="sxs-lookup"><span data-stu-id="d8e62-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="d8e62-185">Valige link **Praeguse perioodi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="d8e62-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="d8e62-186">Saate vaadata üksikute kuluelementide jõudlust.</span><span class="sxs-lookup"><span data-stu-id="d8e62-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="d8e62-187">Samuti saate otsida kindlaid kuluelemente.</span><span class="sxs-lookup"><span data-stu-id="d8e62-187">You can also search for specific cost elements.</span></span>


