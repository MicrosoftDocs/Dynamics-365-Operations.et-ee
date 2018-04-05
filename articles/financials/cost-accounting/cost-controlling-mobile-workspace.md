---
title: "Kulujuhtimise mobiilne tööruum"
description: "Teema annab teavet kulujuhtimise mobiilse tööruumi kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal."
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 39578744654215795f43fec8dcc70c264b66fb0b
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="45ab0-104">Kulujuhtimise mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="45ab0-104">Cost controlling mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="45ab0-105">Teema annab teavet **kulujuhtimise** mobiilse tööruumi kohta.</span><span class="sxs-lookup"><span data-stu-id="45ab0-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="45ab0-106">See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal.</span><span class="sxs-lookup"><span data-stu-id="45ab0-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="45ab0-107">See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="45ab0-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="45ab0-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="45ab0-108">Overview</span></span>
<span data-ttu-id="45ab0-109">Mobiilne tööruum **Kulujuhtimine** annab kiire ülevaate kulukeskuste praegusest jõudlusest, võrreldes tegelikke kulusid eelarvestatud kuludega.</span><span class="sxs-lookup"><span data-stu-id="45ab0-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="45ab0-110">Saate üksikute kuluelementide olekut ka sügavuti uurida.</span><span class="sxs-lookup"><span data-stu-id="45ab0-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="45ab0-111">Näiteks saab töövõtja kutse rahvusvahelisele konverentsile, kuid organisatsioon peab tasuma kõik reisikulud.</span><span class="sxs-lookup"><span data-stu-id="45ab0-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="45ab0-112">Töötaja küsib oma juhilt, kas ta saab konverentsil osaleda.</span><span class="sxs-lookup"><span data-stu-id="45ab0-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="45ab0-113">Juht avab oma mobiiltelefonis kiiresti mobiilse tööruumi **Kulujuhtimine**, et näha, kas tal on töövõtja konverentsil osalemiseks olemas piisav eelarve.</span><span class="sxs-lookup"><span data-stu-id="45ab0-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="45ab0-114">Andmeturve</span><span class="sxs-lookup"><span data-stu-id="45ab0-114">Data security</span></span>
<span data-ttu-id="45ab0-115">Mobiilses tööruumis **Kulujuhtimine** olevad andmed on kaitstud kasutaja identimisteabe kaudu.</span><span class="sxs-lookup"><span data-stu-id="45ab0-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="45ab0-116">Kulukeskuse juhtidel on õigus näha vaid oma enda kulukeskuse andmeid.</span><span class="sxs-lookup"><span data-stu-id="45ab0-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="45ab0-117">Juurdepääsu turbetaset hallatakse moodulis **Kuluarvestus**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="45ab0-118">Kuluarvestajad määratlevad mobiilse tööruumi **Kulujuhtimine** konfiguratsiooni moodulis **Kuluarvestus**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="45ab0-119">Kui tööruum on mobiilirakenduses avaldatud, on see rakenduses saadaval.</span><span class="sxs-lookup"><span data-stu-id="45ab0-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="45ab0-120">Seega saavad kõik organisatsiooni kulukeskuse juhid vaadata andmeid samas vormingus.</span><span class="sxs-lookup"><span data-stu-id="45ab0-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="45ab0-121">Toimingud, vaated ja lingid</span><span class="sxs-lookup"><span data-stu-id="45ab0-121">Actions, views, and links</span></span>
<span data-ttu-id="45ab0-122">**Kulujuhtimise** mobiilne tööruum pakub järgmisi toiminguid, vaateid ja linke.</span><span class="sxs-lookup"><span data-stu-id="45ab0-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="45ab0-123">**Tegevused**</span><span class="sxs-lookup"><span data-stu-id="45ab0-123">**Actions:**</span></span>

    -   <span data-ttu-id="45ab0-124">Paigutuse valimine sätte **Vali konfiguratsioon** kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="45ab0-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="45ab0-125">Sätte **Vali kuluobjekt** kasutamine kulukeskuste valimiseks, mille andmeid filtrida.</span><span class="sxs-lookup"><span data-stu-id="45ab0-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="45ab0-126">Loendis ilmuvad kulukeskused sõltuvad moodulis **Kuluarvestus** antud juurdepääsuõigustest.</span><span class="sxs-lookup"><span data-stu-id="45ab0-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="45ab0-127">**Vaated.** Olenevalt moodulis **Kuluarvestus** valitud toimingutest ja konfiguratsiooni häälestusest saate vaadata kaartidel järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="45ab0-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="45ab0-128">Tegelik võrreldes eelarvega (praegune periood)</span><span class="sxs-lookup"><span data-stu-id="45ab0-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="45ab0-129">Tegelik võrreldes parandatud eelarvega (praegune periood)</span><span class="sxs-lookup"><span data-stu-id="45ab0-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="45ab0-130">Tegelik võrreldes eelarvega (eelmine periood)</span><span class="sxs-lookup"><span data-stu-id="45ab0-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="45ab0-131">Tegelik võrreldes parandatud eelarvega (eelmine periood)</span><span class="sxs-lookup"><span data-stu-id="45ab0-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="45ab0-132">Tegelik võrreldes eelarvega (aasta tänaseni)</span><span class="sxs-lookup"><span data-stu-id="45ab0-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="45ab0-133">Tegelik võrreldes parandatud eelarvega (aasta tänaseni)</span><span class="sxs-lookup"><span data-stu-id="45ab0-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="45ab0-134">Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, hälve ja hälbe protsent.</span><span class="sxs-lookup"><span data-stu-id="45ab0-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="45ab0-135">**Lingid**</span><span class="sxs-lookup"><span data-stu-id="45ab0-135">**Links:**</span></span>

    -   <span data-ttu-id="45ab0-136">Praeguse perioodi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="45ab0-136">Details for current period</span></span>
    -   <span data-ttu-id="45ab0-137">Eelmise perioodi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="45ab0-137">Details for previous period</span></span>
    -   <span data-ttu-id="45ab0-138">Aasta tänaseni üksikasjad</span><span class="sxs-lookup"><span data-stu-id="45ab0-138">Details for year to date</span></span>

    <span data-ttu-id="45ab0-139">Lingi valimisel kuvatakse iga kuluelemendi kaart.</span><span class="sxs-lookup"><span data-stu-id="45ab0-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="45ab0-140">Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, eelarvehälve, eelarvehälbe protsent, parandatud eelarve, parandatud eelarvehälve ja parandatud eelarvehälbe protsent.</span><span class="sxs-lookup"><span data-stu-id="45ab0-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="45ab0-141">[![Kuluelemendi kaart ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="45ab0-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="45ab0-142">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="45ab0-142">Prerequisites</span></span>
<span data-ttu-id="45ab0-143">Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.</span><span class="sxs-lookup"><span data-stu-id="45ab0-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="45ab0-144">Eeltingimused Microsoft Dynamics 365 for Finance and Operationsi kasutamisel</span><span class="sxs-lookup"><span data-stu-id="45ab0-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="45ab0-145">Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, peab süsteemiadministraator avaldama **kulujuhtimise** mobiilse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="45ab0-145">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="45ab0-146">Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="45ab0-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="45ab0-147">Eeltingimused Microsoft Dynamics 365 for Operationsi versiooni 1611 platvormivärskendusega 3 või uuema kasutamisel</span><span class="sxs-lookup"><span data-stu-id="45ab0-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="45ab0-148">Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="45ab0-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="45ab0-149">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="45ab0-149">Prerequisite</span></span></th>
<th><span data-ttu-id="45ab0-150">Roll</span><span class="sxs-lookup"><span data-stu-id="45ab0-150">Role</span></span></th>
<th><span data-ttu-id="45ab0-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="45ab0-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45ab0-152">Rakendage KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="45ab0-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="45ab0-153">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="45ab0-153">System administrator</span></span></td>

<td><span data-ttu-id="45ab0-154">KB 4013633 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Kulujuhtimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="45ab0-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="45ab0-155">KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ab0-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="45ab0-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="45ab0-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="45ab0-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</span><span class="sxs-lookup"><span data-stu-id="45ab0-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="45ab0-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</span><span class="sxs-lookup"><span data-stu-id="45ab0-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="45ab0-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</span><span class="sxs-lookup"><span data-stu-id="45ab0-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45ab0-160">Avaldage <strong>kulujuhtimise</strong> mobiilne tööruum.</span><span class="sxs-lookup"><span data-stu-id="45ab0-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="45ab0-161">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="45ab0-161">System administrator</span></span></td>
<td><span data-ttu-id="45ab0-162">Vt jaotist <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="45ab0-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="45ab0-163">Laadige alla ja installige mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="45ab0-163">Download and install the mobile app</span></span>
<span data-ttu-id="45ab0-164">Laadige alla ja installige Dynamics 365 for Unified Operationsi mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="45ab0-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="45ab0-165">Androidi telefonidele</span><span class="sxs-lookup"><span data-stu-id="45ab0-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="45ab0-166">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="45ab0-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="45ab0-167">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="45ab0-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="45ab0-168">Käivitage rakendus oma mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="45ab0-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="45ab0-169">Sisestage Dynamics 365 URL.</span><span class="sxs-lookup"><span data-stu-id="45ab0-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="45ab0-170">Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="45ab0-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="45ab0-171">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="45ab0-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="45ab0-172">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="45ab0-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="45ab0-173">Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.</span><span class="sxs-lookup"><span data-stu-id="45ab0-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="45ab0-174">[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="45ab0-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="45ab0-175">Kasutage oma kulukeskuse jõudluse vaatamiseks mobiilset tööruumi Kulujuhtimine</span><span class="sxs-lookup"><span data-stu-id="45ab0-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="45ab0-176">Valige oma mobiilses seadmes tööruum **Kulujuhtimine**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="45ab0-177">Valige suvand **Kuluobjekti juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="45ab0-178">Valige suvand **Tegevused**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="45ab0-179">Kulujuhtimise paigutuse valimiseks valige **Konfiguratsiooni valimine**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="45ab0-180">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-180">Select **Done**.</span></span>
6.  <span data-ttu-id="45ab0-181">Valige suvand **Tegevused**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="45ab0-182">Valige suvand **Kuluobjekti valimine**, et valida kulukeskused, millele on teile juurdepääs antud.</span><span class="sxs-lookup"><span data-stu-id="45ab0-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="45ab0-183">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-183">Select **Done**.</span></span>
9.  <span data-ttu-id="45ab0-184">Kulukeskuse üldise jõudluse vaatamine.</span><span class="sxs-lookup"><span data-stu-id="45ab0-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="45ab0-185">Valige link **Praeguse perioodi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="45ab0-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="45ab0-186">Saate vaadata üksikute kuluelementide jõudlust.</span><span class="sxs-lookup"><span data-stu-id="45ab0-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="45ab0-187">Samuti saate otsida kindlaid kuluelemente.</span><span class="sxs-lookup"><span data-stu-id="45ab0-187">You can also search for specific cost elements.</span></span>


