---
title: Rakenduse Dynamics 365 for Unified Operations Mobile koduleht
description: Selles teemas kirjeldatakse rakendust Microsoft Dynamics 365 for Unified Operations Mobile ja antakse linke ressurssidele, mis aitavad teil seda oma organisatsioonis juurutada.
author: sericks007
manager: AnnBe
ms.date: 10/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 5666bee776e3d97244ce4830ac59971831848e71
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554458"
---
# <a name="dynamics-365-for-unified-operations-mobile-app-home-page"></a><span data-ttu-id="1b5b9-103">Rakenduse Dynamics 365 for Unified Operations Mobile koduleht</span><span class="sxs-lookup"><span data-stu-id="1b5b9-103">Dynamics 365 for Unified Operations mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b5b9-104">Selles teemas kirjeldatakse rakendust Microsoft Dynamics 365 for Unified Operations Mobile ja antakse linke ressurssidele, mis aitavad teil seda oma organisatsioonis juurutada.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="1b5b9-105">Mobiilirakenduse varasem nimi oli *Microsoft Dynamics 365 for Finance and Operations*.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="1b5b9-106">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1b5b9-106">Overview</span></span>
--------

<span data-ttu-id="1b5b9-107">Mobiilirakendus võimaldab teie organisatsioonil teha äriprotsessid kättesaadavaks mobiilsetes seadmetes.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="1b5b9-108">Kui teie IT-administraator on organisatsiooni jaoks mobiilsete tööruumid lubanud, saavad kasutajad rakendusse sisse logida ja hakata äriprotsesse oma mobiilsetest seadmetest kohe käitama.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="1b5b9-109">Mobiilirakendus sisaldab järgmisi funktsioone, mis võivad aidata tootlikkust tõsta.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="1b5b9-110">Kasutajad saavad äriandmeid vaadata, redigeerida ja nendega tegeleda, isegi kui võrguühendus on katkendlik või mobiilne seade on täiesti võrguühenduseta.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="1b5b9-111">Seadme võrguühenduse taastumisel sünkroonitakse võrguühenduseta andmed automaatselt Dynamics 365 for Finance and Operationsiga.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="1b5b9-112">IT-administraatorid või arendajad saavad luua ja avaldada mobiilseid tööruume, mis on kohandatud nende organisatsioonile.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="1b5b9-113">Rakendus kasutab teie olemasolevaid koodilõike.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-113">The app uses your existing code assets.</span></span> <span data-ttu-id="1b5b9-114">Seega ei pea te oma valideerimisprotseduure, äriloogikat ega turbekonfiguratsiooni uuesti juurutama.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="1b5b9-115">IT-administraatorid või arendajad saavad mobiilseid tööruume hõlpsasti kujundada, kasutades veebikliendis sisalduvat klõpsatavat tööruumikujundajat.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="1b5b9-116">IT-administraatorid või arendajad saavad soovi korral optimeerida ka tööruumide võrguühenduseta võimalusi, kasutades äriloogika laiendatavuse raamistikku.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="1b5b9-117">Kuna andmete töötlemine jätkub, kui seade on võrguühenduseta, püsivad teie mobiilsed stsenaariumid rikkalikud ja sujuvad, isegi kui seadmetel pole pidevat võrguühendust.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="1b5b9-118">Mobiilirakenduse elemendid</span><span class="sxs-lookup"><span data-stu-id="1b5b9-118">Elements of the mobile app</span></span>
<span data-ttu-id="1b5b9-119">Mobiilirakenduse navigeerimispaan koosneb neljast peamisest osast: armatuurlaud, tööruumid, lehed ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="1b5b9-120">[![Navigeerimispaani põhimõtted mobiilirakenduses](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="1b5b9-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="1b5b9-121">Rakenduse käivitamisel avaneb **armatuurlaud**.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="1b5b9-122">Armatuurlaual näete avaldatud **tööruumide** loendit.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="1b5b9-123">Igas tööruumis näete loendit **lehtedest**, mis on selle tööruumi jaoks saadaval.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="1b5b9-124">Lehel olles saate teha mitut toimingut.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="1b5b9-125">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-125">Here are some examples:</span></span>

    - <span data-ttu-id="1b5b9-126">Üksikasjalike andmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-126">View detailed data.</span></span>
    - <span data-ttu-id="1b5b9-127">Lehelt teistele lehtedele navigeerimine seotud andmete nägemiseks, nagu üksuse üksikasjad või read.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="1b5b9-128">Selle lehe puhul kasutatavate **toimingute** loendi kuvamine.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="1b5b9-129">Tegevused võimaldavad teil andmeid luua või olemasolevaid andmeid muuta.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="1b5b9-130">Juurutusprotsess</span><span class="sxs-lookup"><span data-stu-id="1b5b9-130">Implementation process</span></span>
<span data-ttu-id="1b5b9-131">Järgmisel joonisel on näidatud nii Microsofti pakutavate kui ka kohandatud mobiilsete tööruumide juurutusprotsess.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="1b5b9-132">[![Mobiilirakenduste juurutamise protsess](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="1b5b9-132">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="1b5b9-133">Järgmises tabelis on lingid ressursside juurde, mis aitavad juurutada nii Microsofti pakutavaid kui ka kohandatud mobiilseid tööruume.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="1b5b9-134">Esimeses veerus toodud numbrid vastavad eelmisel joonisel kujutatud nummerdatud etappidele.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b5b9-135">Etapp</span><span class="sxs-lookup"><span data-stu-id="1b5b9-135">Step</span></span></th>
<th><span data-ttu-id="1b5b9-136">Roll</span><span class="sxs-lookup"><span data-stu-id="1b5b9-136">Role</span></span></th>
<th><span data-ttu-id="1b5b9-137">Tegevus</span><span class="sxs-lookup"><span data-stu-id="1b5b9-137">Action</span></span></th>
<th><span data-ttu-id="1b5b9-138">Ressursid, mis aitavad teil tegevusi lõpule viia</span><span class="sxs-lookup"><span data-stu-id="1b5b9-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b5b9-139">1</span><span class="sxs-lookup"><span data-stu-id="1b5b9-139">1</span></span></td>
<td><span data-ttu-id="1b5b9-140">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="1b5b9-140">System administrator</span></span></td>
<td><span data-ttu-id="1b5b9-141">Juurutage oma organisatsioonis rakendust Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-141">Implement Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="1b5b9-142">Kui te e&#39;i ole veel ühtegi Microsoft Dynamics 365 versiooni juurutanud, vt jaotist <a href="../deployment/deploy-demo-environment.md">Demokeskkonna juurutamine</a>.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-142">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="1b5b9-143">Kasutatavate mobiilsete tööruumide loendi leiate jaotisest <a href="mobile-workspaces-released.md">Hiljuti välja antud mobiilsed tööruumid</a>.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b5b9-144">2</span><span class="sxs-lookup"><span data-stu-id="1b5b9-144">2</span></span></td>
<td><span data-ttu-id="1b5b9-145">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="1b5b9-145">System administrator</span></span></td>
<td><span data-ttu-id="1b5b9-146"><strong>Kui kasutat&#39;e Microsoft Dynamics 365 for Operationsi versiooni 1611:</strong> laadige alla ja installige KB-d, mis lubavad Microsofti pakutavad mobiilsed tööruumid.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-146"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="1b5b9-147">Lisateavet vt järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="1b5b9-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Kulujuhtimise mobiilsed tööruumid</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="1b5b9-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiilse tööruumi varude laoseis</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="1b5b9-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Müügitellimuste mobiilsed tööruumid</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="1b5b9-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Hankija koostöö mobiilne tööruum</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="1b5b9-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Mobiilse tööruumi projekti ajakirje</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="1b5b9-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Kuluhalduse mobiilne tööruum</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b5b9-154">3</span><span class="sxs-lookup"><span data-stu-id="1b5b9-154">3</span></span></td>
<td><span data-ttu-id="1b5b9-155">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="1b5b9-155">System administrator</span></span></td>
<td><span data-ttu-id="1b5b9-156">Avaldage Microsofti pakutavad mobiilsed tööruumid.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="1b5b9-157"><a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>
</span><span class="sxs-lookup"><span data-stu-id="1b5b9-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b5b9-158">4</span><span class="sxs-lookup"><span data-stu-id="1b5b9-158">4</span></span></td>
<td><span data-ttu-id="1b5b9-159">Arendaja või sõltumatu tarkvaratarnija (ISV)</span><span class="sxs-lookup"><span data-stu-id="1b5b9-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="1b5b9-160">Kasutage mobiilset platvormi kohandatud mobiilsete tööruumide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="1b5b9-161"><a href="platform/mobile-platform-home-page.md">Mobiilne platvorm</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b5b9-162">5</span><span class="sxs-lookup"><span data-stu-id="1b5b9-162">5</span></span></td>
<td><span data-ttu-id="1b5b9-163">ISV</span><span class="sxs-lookup"><span data-stu-id="1b5b9-163">ISV</span></span></td>
<td><span data-ttu-id="1b5b9-164">Looge kohandatud mobiilseid tööruume sisaldav juurutatav pakett ja laadige see üles teenusesse Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1b5b9-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="1b5b9-165"><a href="../deployment/create-apply-deployable-package.md">Juurutatava paketi loomine</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b5b9-166">6</span><span class="sxs-lookup"><span data-stu-id="1b5b9-166">6</span></span></td>
<td><span data-ttu-id="1b5b9-167">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="1b5b9-167">System administrator</span></span></td>
<td><span data-ttu-id="1b5b9-168">Rakendage sõltumatu tarkvaratarnija (ISV) pakutavaid kohandatud tööruume sisaldav juurutatav pakett.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="1b5b9-169"><a href="../deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b5b9-170">7</span><span class="sxs-lookup"><span data-stu-id="1b5b9-170">7</span></span></td>
<td><span data-ttu-id="1b5b9-171">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="1b5b9-171">System administrator</span></span></td>
<td><span data-ttu-id="1b5b9-172">Avaldage ISV pakutavad kohandatud mobiilsed tööruumid.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="1b5b9-173"><a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b5b9-174">8</span><span class="sxs-lookup"><span data-stu-id="1b5b9-174">8</span></span></td>
<td><span data-ttu-id="1b5b9-175">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="1b5b9-175">User</span></span></td>
<td><span data-ttu-id="1b5b9-176">Laadige alla ja installige mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-176">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="1b5b9-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Rakendus Unified Operations Androidile</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Unified Operations app for Android</a></span></span><BR/><span data-ttu-id="1b5b9-178">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Rakendus Unified Operations iOS-ile</a></span><span class="sxs-lookup"><span data-stu-id="1b5b9-178">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Unified Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="1b5b9-179">(Windows Phone’i ei toetata)</span><span class="sxs-lookup"><span data-stu-id="1b5b9-179">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b5b9-180">9</span><span class="sxs-lookup"><span data-stu-id="1b5b9-180">9</span></span></td>
<td><span data-ttu-id="1b5b9-181">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="1b5b9-181">User</span></span></td>
<td><span data-ttu-id="1b5b9-182">Logige mobiilirakendusse sisse ja kasutage seda.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-182">Sign in, and use the mobile app.</span></span> <span data-ttu-id="1b5b9-183">Rakendus sisaldab süsteemiadministraatori avaldatud mobiilseid tööruume.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-183">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="1b5b9-184">Microsofti pakutavate mobiilsete tööruumide loendi leiate jaotisest <a href="mobile-workspaces-released.md">Hiljuti välja antud mobiilsed tööruumid</a>.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-184">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>
