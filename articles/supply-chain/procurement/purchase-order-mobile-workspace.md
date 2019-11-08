---
title: Ostutellimuse kinnitamise mobiilne tööruum
description: Selles teemas antakse teavet ostutellimuse kinnitamise mobiilse tööruumi kohta, mis võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida. Näiteks võite ostutellimuse kinnitada või tagasi lükata.
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 33e5993f57a8c0248ac2e314f91cc40a2b355858
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653460"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="55064-104">Ostutellimuse kinnitamise mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="55064-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55064-105">See teema annab teavet **ostutellimuse kinnitamise** mobiilse tööruumi kohta.</span><span class="sxs-lookup"><span data-stu-id="55064-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="55064-106">See tööruum võimaldab ostutellimusi vaadata ja neile tegevuste kaudu reageerida.</span><span class="sxs-lookup"><span data-stu-id="55064-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="55064-107">Näiteks võite ostutellimuse kinnitada või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="55064-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="55064-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="55064-108">Overview</span></span> 
<span data-ttu-id="55064-109">Kinnitamist nõudvad ostutellimused läbivad kinnitamise töövoo.</span><span class="sxs-lookup"><span data-stu-id="55064-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="55064-110">See töövoog võib sisaldada mitmesuguseid samme, mis nõuavad vähemalt ühe inimese tegevusi.</span><span class="sxs-lookup"><span data-stu-id="55064-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="55064-111">Näiteks võib inimesel olla vaja mõni ülesanne täita või ostutellimus kinnitada.</span><span class="sxs-lookup"><span data-stu-id="55064-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="55064-112">**Ostutellimuse kinnitamise** mobiilne tööruum võimaldab ostutellimusi mobiilselt seadmelt hõlpsasti vaadata ja neile reageerida.</span><span class="sxs-lookup"><span data-stu-id="55064-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="55064-113">See tööruum võimaldab teha ka samu töövootegevusi, mida saate teha rakenduse veebikliendist.</span><span class="sxs-lookup"><span data-stu-id="55064-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="55064-114">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="55064-114">Prerequisites</span></span>
<span data-ttu-id="55064-115">Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Supply Chain Managementi versioonist.</span><span class="sxs-lookup"><span data-stu-id="55064-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="55064-116">Eeltingimused, kui kasutate Supply Chain Managementi</span><span class="sxs-lookup"><span data-stu-id="55064-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="55064-117">Kui teie organisatsioonis on juurutatud Supply Chain Management, peab süsteemiadministraator avaldama mobiilse tööruumi **Ostutellimuse heakskiitmine**.</span><span class="sxs-lookup"><span data-stu-id="55064-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="55064-118">Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="55064-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="55064-119">Eeltingimused, kui kasutate rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 platvormivärskendusega 3 või uuemat</span><span class="sxs-lookup"><span data-stu-id="55064-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="55064-120">Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="55064-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="55064-121">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="55064-121">Prerequisite</span></span></th>
<th><span data-ttu-id="55064-122">Roll</span><span class="sxs-lookup"><span data-stu-id="55064-122">Role</span></span></th>
<th><span data-ttu-id="55064-123">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="55064-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55064-124">Rakendage KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="55064-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="55064-125">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="55064-125">System administrator</span></span></td>
<td><span data-ttu-id="55064-126">KB 4017918 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Ostutellimuse kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="55064-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="55064-127">KB 4017918 juurutamiseks peab süsteemiadministraator toimima järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="55064-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="55064-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="55064-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="55064-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</span><span class="sxs-lookup"><span data-stu-id="55064-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="55064-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</span><span class="sxs-lookup"><span data-stu-id="55064-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="55064-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</span><span class="sxs-lookup"><span data-stu-id="55064-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55064-132">Avaldage <strong>ostutellimuse kinnitamise</strong> mobiilne tööruum.</span><span class="sxs-lookup"><span data-stu-id="55064-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="55064-133">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="55064-133">System administrator</span></span></td>
<td><span data-ttu-id="55064-134">Vt jaotist <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="55064-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="55064-135">Laadige alla ja installige mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="55064-135">Download and install the mobile app</span></span>
<span data-ttu-id="55064-136">Laadige alla ja installige Finance and Operationsi mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="55064-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="55064-137">Androidi telefonide puhul</span><span class="sxs-lookup"><span data-stu-id="55064-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="55064-138">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="55064-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="55064-139">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="55064-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="55064-140">Käivitage rakendus oma mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="55064-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="55064-141">Sisestage oma Microsoft Dynamics365 URL.</span><span class="sxs-lookup"><span data-stu-id="55064-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="55064-142">Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="55064-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="55064-143">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="55064-143">Enter your credentials.</span></span>
4. <span data-ttu-id="55064-144">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="55064-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="55064-145">Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.</span><span class="sxs-lookup"><span data-stu-id="55064-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Ostutellimuse kinnitamise tööruum olemasolevate tööruumide loendis](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="55064-147">Vaadake teile määratud tellimusi</span><span class="sxs-lookup"><span data-stu-id="55064-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="55064-148">Valige oma mobiilses seadmes tööruum **Ostutellimuse kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="55064-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="55064-149">Valige **Mulle määratud tellimused** kõigi ostutellimuste vaatamiseks, mille puhul teil on palutud ostutellimuse kinnitamise töövoos midagi teha.</span><span class="sxs-lookup"><span data-stu-id="55064-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="55064-150">Valige tellimus.</span><span class="sxs-lookup"><span data-stu-id="55064-150">Select an order.</span></span> <span data-ttu-id="55064-151">Lehel **Tellimuse üksikasjad** näete tellimuse päise andmeid ja ridu.</span><span class="sxs-lookup"><span data-stu-id="55064-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="55064-152">Leiate juhiseid ka töövooülesandest.</span><span class="sxs-lookup"><span data-stu-id="55064-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="55064-153">Valige **Arvestuse jaotused** lehe **Arvestuse jaotuse päis** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="55064-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="55064-154">Naaske lehele **Tellimuse üksikasjad** ja valige rida.</span><span class="sxs-lookup"><span data-stu-id="55064-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="55064-155">Tellimuse rea üksikasjadest saate uurida ka reapõhiseid arvestuse jaotusi.</span><span class="sxs-lookup"><span data-stu-id="55064-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="55064-156">Ostutellimusega tegevuse läbiviimine</span><span class="sxs-lookup"><span data-stu-id="55064-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="55064-157">Kui olete endale määratud ostutellimust vaadanud ja töövoo juhiseid lugenud, peaksite olema tegutsemiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="55064-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="55064-158">Valige oma mobiilses seadmes tööruum **Ostutellimuse kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="55064-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="55064-159">Valige **Mulle määratud tellimused** kõigi ostutellimuste vaatamiseks, mille puhul teil on palutud ostutellimuse kinnitamise töövoos midagi teha.</span><span class="sxs-lookup"><span data-stu-id="55064-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="55064-160">Valige tellimus ja vaadake üksikasjade lehte.</span><span class="sxs-lookup"><span data-stu-id="55064-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="55064-161">Valige **Tegevused** olemasolevate tegevuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="55064-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="55064-162">Saadaolevad toimingud olenevad teile määratud ülesandest.</span><span class="sxs-lookup"><span data-stu-id="55064-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="55064-163">Ülesande tegevus</span><span class="sxs-lookup"><span data-stu-id="55064-163">Task action</span></span>    | <span data-ttu-id="55064-164">Kinnitamise tegevus</span><span class="sxs-lookup"><span data-stu-id="55064-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="55064-165">Vii lõpule</span><span class="sxs-lookup"><span data-stu-id="55064-165">Complete</span></span>       | <span data-ttu-id="55064-166">Kinnita</span><span class="sxs-lookup"><span data-stu-id="55064-166">Approve</span></span>          |
    | <span data-ttu-id="55064-167">Tagasta</span><span class="sxs-lookup"><span data-stu-id="55064-167">Return</span></span>         | <span data-ttu-id="55064-168">Lükka tagasi</span><span class="sxs-lookup"><span data-stu-id="55064-168">Reject</span></span>           |
    | <span data-ttu-id="55064-169">Taotle muudatust</span><span class="sxs-lookup"><span data-stu-id="55064-169">Request change</span></span> | <span data-ttu-id="55064-170">Taotle muudatust</span><span class="sxs-lookup"><span data-stu-id="55064-170">Request change</span></span>   |
    | <span data-ttu-id="55064-171">Delegaat</span><span class="sxs-lookup"><span data-stu-id="55064-171">Delegate</span></span>       | <span data-ttu-id="55064-172">Delegaat</span><span class="sxs-lookup"><span data-stu-id="55064-172">Delegate</span></span>         |

5. <span data-ttu-id="55064-173">Valige sobiv tegevus.</span><span class="sxs-lookup"><span data-stu-id="55064-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="55064-174">Sisestage lehele **Ülesande täitmine** kommentaar.</span><span class="sxs-lookup"><span data-stu-id="55064-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="55064-175">Pange tähele, et kui valite tegevuse **Delegeeri**, siis peate valima kasutaja, kellele ülesanne delegeerida.</span><span class="sxs-lookup"><span data-stu-id="55064-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="55064-176">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="55064-176">Select **Done**.</span></span> <span data-ttu-id="55064-177">Kui olete tööruumi uuendanud, ei ole ostutellimust enam teie loendis.</span><span class="sxs-lookup"><span data-stu-id="55064-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 
