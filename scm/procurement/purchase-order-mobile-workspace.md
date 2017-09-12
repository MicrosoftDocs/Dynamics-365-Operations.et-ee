---
title: "Ostutellimuse kinnitamise mobiilne tööruum"
description: "Selles teemas antakse teavet ostutellimuse kinnitamise mobiilse tööruumi kohta, mis võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida. Näiteks võite ostutellimuse kinnitada või tagasi lükata."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 12f710caea987dec9a343774f060e7dd7ca03ec4
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="230f3-104">Ostutellimuse kinnitamise mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="230f3-104">Purchase order approval mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

<span data-ttu-id="230f3-105">See teema annab teavet **ostutellimuse kinnitamise** mobiilse tööruumi kohta.</span><span class="sxs-lookup"><span data-stu-id="230f3-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="230f3-106">See tööruum võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida.</span><span class="sxs-lookup"><span data-stu-id="230f3-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="230f3-107">Näiteks võite ostutellimuse kinnitada või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="230f3-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="230f3-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="230f3-108">Overview</span></span> 
<span data-ttu-id="230f3-109">Kinnitamist nõudvad ostutellimused läbivad kinnitamise töövoo.</span><span class="sxs-lookup"><span data-stu-id="230f3-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="230f3-110">See töövoog võib sisaldada mitmesuguseid samme, mis nõuavad vähemalt ühe inimese tegevusi.</span><span class="sxs-lookup"><span data-stu-id="230f3-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="230f3-111">Näiteks võib inimesel olla vaja mõni ülesanne täita või ostutellimus kinnitada.</span><span class="sxs-lookup"><span data-stu-id="230f3-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="230f3-112">**Ostutellimuse kinnitamise** mobiilne tööruum võimaldab ostutellimusi mobiilselt seadmelt hõlpsasti vaadata ja neile reageerida.</span><span class="sxs-lookup"><span data-stu-id="230f3-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="230f3-113">See tööruum võimaldab teha ka samu töövootegevusi, mida saate teha Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni veebikliendist.</span><span class="sxs-lookup"><span data-stu-id="230f3-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="230f3-114">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="230f3-114">Prerequisites</span></span>
<span data-ttu-id="230f3-115">Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Finance and Operationsi versioonist.</span><span class="sxs-lookup"><span data-stu-id="230f3-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="230f3-116">Eeltingimused lahenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni 2017. aasta juuli värskenduse kasutamisel</span><span class="sxs-lookup"><span data-stu-id="230f3-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span> 
<span data-ttu-id="230f3-117">Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni 2017. aasta juuli värskendus, peab süsteemiadministraator avaldama **ostutellimuse kinnitamise** mobiilse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="230f3-117">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="230f3-118">Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="230f3-118">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="230f3-119">Eeltingimused Microsoft Dynamics 365 for Operationsi versiooni 1611 platvormivärskendusega 3 või uuema kasutamisel</span><span class="sxs-lookup"><span data-stu-id="230f3-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="230f3-120">Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="230f3-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="230f3-121">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="230f3-121">Prerequisite</span></span></th>
<th><span data-ttu-id="230f3-122">Roll</span><span class="sxs-lookup"><span data-stu-id="230f3-122">Role</span></span></th>
<th><span data-ttu-id="230f3-123">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="230f3-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="230f3-124">Rakendage KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="230f3-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="230f3-125">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="230f3-125">System administrator</span></span></td>
<td><span data-ttu-id="230f3-126">KB 4017918 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Ostutellimuse kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="230f3-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="230f3-127">KB 4017918 juurutamiseks peab süsteemiadministraator toimima järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="230f3-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="230f3-128"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="230f3-128"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="230f3-129"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</span><span class="sxs-lookup"><span data-stu-id="230f3-129"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="230f3-130"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</span><span class="sxs-lookup"><span data-stu-id="230f3-130"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="230f3-131"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</span><span class="sxs-lookup"><span data-stu-id="230f3-131"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="230f3-132">Avaldage <strong>ostutellimuse kinnitamise</strong> mobiilne tööruum.</span><span class="sxs-lookup"><span data-stu-id="230f3-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="230f3-133">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="230f3-133">System administrator</span></span></td>
<td><span data-ttu-id="230f3-134">Vt jaotist <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="230f3-134">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="230f3-135">Laadige alla ja installige mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="230f3-135">Download and install the mobile app</span></span>
<span data-ttu-id="230f3-136">Laadige alla ja installige Microsoft Dynamics 365 for Unified Operationsi mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="230f3-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="230f3-137">Androidi telefonidele</span><span class="sxs-lookup"><span data-stu-id="230f3-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="230f3-138">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="230f3-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="230f3-139">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="230f3-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="230f3-140">Käivitage rakendus oma mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="230f3-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="230f3-141">Sisestage Microsoft Dynamics 365 URL.</span><span class="sxs-lookup"><span data-stu-id="230f3-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="230f3-142">Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="230f3-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="230f3-143">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="230f3-143">Enter your credentials.</span></span>
4. <span data-ttu-id="230f3-144">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="230f3-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="230f3-145">Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.</span><span class="sxs-lookup"><span data-stu-id="230f3-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Ostutellimuse kinnitamise tööruum olemasolevate tööruumide loendis](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="230f3-147">Vaadake teile määratud tellimusi</span><span class="sxs-lookup"><span data-stu-id="230f3-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="230f3-148">Valige oma mobiilses seadmes tööruum **Ostutellimuse kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="230f3-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="230f3-149">Valige **Mulle määratud tellimused** kõigi ostutellimuste vaatamiseks, mille puhul teil on palutud ostutellimuse kinnitamise töövoos midagi teha.</span><span class="sxs-lookup"><span data-stu-id="230f3-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="230f3-150">Valige tellimus.</span><span class="sxs-lookup"><span data-stu-id="230f3-150">Select an order.</span></span> <span data-ttu-id="230f3-151">Lehel **Tellimuse üksikasjad** näete tellimuse päise andmeid ja ridu.</span><span class="sxs-lookup"><span data-stu-id="230f3-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="230f3-152">Leiate juhiseid ka töövooülesandest.</span><span class="sxs-lookup"><span data-stu-id="230f3-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="230f3-153">Valige **Arvestuse jaotused** lehe **Arvestuse jaotuse päis** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="230f3-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="230f3-154">Naaske lehele **Tellimuse üksikasjad** ja valige rida.</span><span class="sxs-lookup"><span data-stu-id="230f3-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="230f3-155">Tellimuse rea üksikasjadest saate uurida ka reapõhiseid arvestuse jaotusi.</span><span class="sxs-lookup"><span data-stu-id="230f3-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="230f3-156">Ostutellimusega tegevuse läbiviimine</span><span class="sxs-lookup"><span data-stu-id="230f3-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="230f3-157">Kui olete endale määratud ostutellimust vaadanud ja töövoo juhiseid lugenud, peaksite olema tegutsemiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="230f3-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="230f3-158">Valige oma mobiilses seadmes tööruum **Ostutellimuse kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="230f3-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="230f3-159">Valige **Mulle määratud tellimused** kõigi ostutellimuste vaatamiseks, mille puhul teil on palutud ostutellimuse kinnitamise töövoos midagi teha.</span><span class="sxs-lookup"><span data-stu-id="230f3-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="230f3-160">Valige tellimus ja vaadake üksikasjade lehte.</span><span class="sxs-lookup"><span data-stu-id="230f3-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="230f3-161">Valige **Tegevused** olemasolevate tegevuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="230f3-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="230f3-162">Saadaolevad toimingud olenevad teile määratud ülesandest.</span><span class="sxs-lookup"><span data-stu-id="230f3-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="230f3-163">Ülesande tegevus</span><span class="sxs-lookup"><span data-stu-id="230f3-163">Task action</span></span>    | <span data-ttu-id="230f3-164">Kinnitamise tegevus</span><span class="sxs-lookup"><span data-stu-id="230f3-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="230f3-165">Vii lõpule</span><span class="sxs-lookup"><span data-stu-id="230f3-165">Complete</span></span>       | <span data-ttu-id="230f3-166">Kinnita</span><span class="sxs-lookup"><span data-stu-id="230f3-166">Approve</span></span>          |
    | <span data-ttu-id="230f3-167">Tagasta</span><span class="sxs-lookup"><span data-stu-id="230f3-167">Return</span></span>         | <span data-ttu-id="230f3-168">Lükka tagasi</span><span class="sxs-lookup"><span data-stu-id="230f3-168">Reject</span></span>           |
    | <span data-ttu-id="230f3-169">Taotle muudatust</span><span class="sxs-lookup"><span data-stu-id="230f3-169">Request change</span></span> | <span data-ttu-id="230f3-170">Taotle muudatust</span><span class="sxs-lookup"><span data-stu-id="230f3-170">Request change</span></span>   |
    | <span data-ttu-id="230f3-171">Delegaat</span><span class="sxs-lookup"><span data-stu-id="230f3-171">Delegate</span></span>       | <span data-ttu-id="230f3-172">Delegaat</span><span class="sxs-lookup"><span data-stu-id="230f3-172">Delegate</span></span>         |

5. <span data-ttu-id="230f3-173">Valige sobiv tegevus.</span><span class="sxs-lookup"><span data-stu-id="230f3-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="230f3-174">Sisestage lehele **Ülesande täitmine** kommentaar.</span><span class="sxs-lookup"><span data-stu-id="230f3-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="230f3-175">Pange tähele, et kui valite tegevuse **Delegeeri**, siis peate valima kasutaja, kellele ülesanne delegeerida.</span><span class="sxs-lookup"><span data-stu-id="230f3-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="230f3-176">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="230f3-176">Select **Done**.</span></span> <span data-ttu-id="230f3-177">Kui olete tööruumi uuendanud, ei ole ostutellimust enam teie loendis.</span><span class="sxs-lookup"><span data-stu-id="230f3-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 

