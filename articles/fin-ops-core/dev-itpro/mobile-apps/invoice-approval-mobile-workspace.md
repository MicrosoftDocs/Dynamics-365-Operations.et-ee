---
title: Arvete kinnitamise mobiilne tööruum
description: See teema annab teavet arvete kinnitamise mobiilse tööruumi kohta.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 1a7aa1a03791b8ccb7050389097d1272f5930a49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127565"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="9e9ea-103">Arvete kinnitamise mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="9e9ea-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e9ea-104">See teema annab teavet **arvete kinnitamise** mobiilse tööruumi kohta.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="9e9ea-105">See tööruum annab loendi arvetest, mis on määratud teile hankija arve päise töövooprotsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="9e9ea-106">See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="9e9ea-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9e9ea-107">Overview</span></span>

<span data-ttu-id="9e9ea-108">**Arvete kinnitamise** mobiilne tööruum võimaldab ostureskontro ametnikel ja juhtidel vaadata arveid, mis on neile hankija arve päise töövooprotsessi käigus määratud.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="9e9ea-109">Saate vaadata arve andmeid ja isegi rea ja jaotuse üksikasju, mis aitab teil teha teadlikke kinnitamisotsuseid.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="9e9ea-110">Tööruumist saab teha toiminguid arve suunamiseks läbi töövooprotsessi.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="9e9ea-111">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="9e9ea-111">Prerequisites</span></span>

<span data-ttu-id="9e9ea-112">Enne selle mobiilse tööruumi kasutamist peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9e9ea-113">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="9e9ea-113">Prerequisite</span></span></th>
<th><span data-ttu-id="9e9ea-114">Roll</span><span class="sxs-lookup"><span data-stu-id="9e9ea-114">Role</span></span></th>
<th><span data-ttu-id="9e9ea-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9e9ea-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e9ea-116">Teie organisatsioonis peab olema juurutatud Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="9e9ea-117">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="9e9ea-117">System administrator</span></span></td>
<td><span data-ttu-id="9e9ea-118">Vt jaotist <a href="../deployment/deploy-demo-environment.md">Demokeskkonna juurutamine</a>.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e9ea-119"><strong>Arvete kinnitamise</strong> mobiilne tööruum tuleb avaldada.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="9e9ea-120">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="9e9ea-120">System administrator</span></span></td>
<td><span data-ttu-id="9e9ea-121">Vt jaotist <a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="9e9ea-122">Laadige alla ja installige mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="9e9ea-122">Download and install the mobile app</span></span>

<span data-ttu-id="9e9ea-123">Laadige alla ja installige Finance and Operationsi mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="9e9ea-124">Androidi telefonide puhul</span><span class="sxs-lookup"><span data-stu-id="9e9ea-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="9e9ea-125">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="9e9ea-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="9e9ea-126">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="9e9ea-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="9e9ea-127">Käivitage rakendus oma mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="9e9ea-128">Sisestage oma Microsoft Dynamics365 URL.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="9e9ea-129">Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="9e9ea-130">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="9e9ea-131">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="9e9ea-132">Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="9e9ea-133">[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="9e9ea-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="9e9ea-134">Arvete kinnitamine, kasutades arvete kinnitamise mobiilset tööruumi</span><span class="sxs-lookup"><span data-stu-id="9e9ea-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="9e9ea-135">Valige oma mobiilses seadmes tööruum **Arvete kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="9e9ea-136">Valige arve, mis on teile hankija arve päise töövooprotsessiga määratud.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="9e9ea-137">Vaadake lehel **Arve üksikasjad** üle arve päise teave, nt hankija ja kuupäeva andmed.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="9e9ea-138">Valige arvel rida, et vaadata selle kohta üksikasjalikumat teavet vaates **Arve rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="9e9ea-139">Tehke vaates **Arve rea üksikasjad** valik **Jaotused** rea jaotuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="9e9ea-140">Siin saate vaadata arve rea arvestust.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="9e9ea-141">Kuvatav teave hõlmab finantsdimensioone ja põhikontot.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="9e9ea-142">Tehke lehel **Arve rea üksikasjad** valik **Jaotused** kõigi jaotuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="9e9ea-143">Siin saate vaadata kogu arve arvestust.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="9e9ea-144">Kuvatav teave hõlmab finantsdimensioone ja põhikontosid.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="9e9ea-145">Valige **Manused** kõigi arvele manustatud märkmete või failide kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="9e9ea-146">Valige lehelt **Arve üksikasjad** sobiv töövoog ülevaatuse protsessi lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="9e9ea-147">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="9e9ea-147">Select **Done**.</span></span>
