---
title: Arvete kinnitamise mobiilne tööruum
description: See teema annab teavet arvete kinnitamise mobiilse tööruumi kohta. See tööruum annab loendi arvetest, mis on määratud teile hankija arve päise töövooprotsessi kaudu.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d4ea1d81b0e4f92974ceb7d46386c9d9f6e48979
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248999"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="e750d-104">Arvete kinnitamise mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="e750d-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e750d-105">See teema annab teavet **arvete kinnitamise** mobiilse tööruumi kohta.</span><span class="sxs-lookup"><span data-stu-id="e750d-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="e750d-106">See tööruum annab loendi arvetest, mis on määratud teile hankija arve päise töövooprotsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="e750d-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="e750d-107">See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e750d-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="e750d-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e750d-108">Overview</span></span>

<span data-ttu-id="e750d-109">**Arvete kinnitamise** mobiilne tööruum võimaldab ostureskontro ametnikel ja juhtidel vaadata arveid, mis on neile hankija arve päise töövooprotsessi käigus määratud.</span><span class="sxs-lookup"><span data-stu-id="e750d-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="e750d-110">Saate vaadata arve andmeid ja isegi rea ja jaotuse üksikasju, mis aitab teil teha teadlikke kinnitamisotsuseid.</span><span class="sxs-lookup"><span data-stu-id="e750d-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="e750d-111">Tööruumist saab teha toiminguid arve suunamiseks läbi töövooprotsessi.</span><span class="sxs-lookup"><span data-stu-id="e750d-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="e750d-112">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e750d-112">Prerequisites</span></span>

<span data-ttu-id="e750d-113">Enne selle mobiilse tööruumi kasutamist peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="e750d-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e750d-114">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="e750d-114">Prerequisite</span></span></th>
<th><span data-ttu-id="e750d-115">Roll</span><span class="sxs-lookup"><span data-stu-id="e750d-115">Role</span></span></th>
<th><span data-ttu-id="e750d-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e750d-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e750d-117">Teie organisatsioonis peab olema juurutatud Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e750d-117">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="e750d-118">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="e750d-118">System administrator</span></span></td>
<td><span data-ttu-id="e750d-119">Vt jaotist <a href="../deployment/deploy-demo-environment.md">Demokeskkonna juurutamine</a>.</span><span class="sxs-lookup"><span data-stu-id="e750d-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e750d-120"><strong>Arvete kinnitamise</strong> mobiilne tööruum tuleb avaldada.</span><span class="sxs-lookup"><span data-stu-id="e750d-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="e750d-121">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="e750d-121">System administrator</span></span></td>
<td><span data-ttu-id="e750d-122">Vt jaotist <a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="e750d-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="e750d-123">Laadige alla ja installige mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="e750d-123">Download and install the mobile app</span></span>

<span data-ttu-id="e750d-124">Laadige alla ja installige Finance and Operationsi mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="e750d-124">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="e750d-125">Androidi telefonide puhul</span><span class="sxs-lookup"><span data-stu-id="e750d-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="e750d-126">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="e750d-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="e750d-127">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="e750d-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="e750d-128">Käivitage rakendus oma mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="e750d-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="e750d-129">Sisestage oma Microsoft Dynamics365 URL.</span><span class="sxs-lookup"><span data-stu-id="e750d-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="e750d-130">Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="e750d-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="e750d-131">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="e750d-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="e750d-132">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="e750d-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="e750d-133">Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.</span><span class="sxs-lookup"><span data-stu-id="e750d-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="e750d-134">[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="e750d-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="e750d-135">Arvete kinnitamine, kasutades arvete kinnitamise mobiilset tööruumi</span><span class="sxs-lookup"><span data-stu-id="e750d-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="e750d-136">Valige oma mobiilses seadmes tööruum **Arvete kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="e750d-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="e750d-137">Valige arve, mis on teile hankija arve päise töövooprotsessiga määratud.</span><span class="sxs-lookup"><span data-stu-id="e750d-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="e750d-138">Vaadake lehel **Arve üksikasjad** üle arve päise teave, nt hankija ja kuupäeva andmed.</span><span class="sxs-lookup"><span data-stu-id="e750d-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="e750d-139">Valige arvel rida, et vaadata selle kohta üksikasjalikumat teavet vaates **Arve rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="e750d-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="e750d-140">Tehke vaates **Arve rea üksikasjad** valik **Jaotused** rea jaotuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="e750d-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="e750d-141">Siin saate vaadata arve rea arvestust.</span><span class="sxs-lookup"><span data-stu-id="e750d-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="e750d-142">Kuvatav teave hõlmab finantsdimensioone ja põhikontot.</span><span class="sxs-lookup"><span data-stu-id="e750d-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="e750d-143">Tehke lehel **Arve rea üksikasjad** valik **Jaotused** kõigi jaotuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="e750d-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="e750d-144">Siin saate vaadata kogu arve arvestust.</span><span class="sxs-lookup"><span data-stu-id="e750d-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="e750d-145">Kuvatav teave hõlmab finantsdimensioone ja põhikontosid.</span><span class="sxs-lookup"><span data-stu-id="e750d-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="e750d-146">Valige **Manused** kõigi arvele manustatud märkmete või failide kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="e750d-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="e750d-147">Valige lehelt **Arve üksikasjad** sobiv töövoog ülevaatuse protsessi lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="e750d-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="e750d-148">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="e750d-148">Select **Done**.</span></span>