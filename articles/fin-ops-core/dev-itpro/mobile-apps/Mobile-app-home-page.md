---
title: Mobiilirakenduse avaleht
description: Selles teemas kirjeldatakse mobiilirakendust Finance and Operations (Dynamics 365) ja antakse linke ressurssidele, mis aitavad teil seda oma organisatsioonis juurutada.
author: ChrisGarty
manager: AnnBe
ms.date: 01/22/2020
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
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 65254ac09a01e1ed2486d8f1324f564b3cd800c6
ms.sourcegitcommit: 9a053d020e672a87b660f27009a492544e6c81a9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/30/2020
ms.locfileid: "3641468"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="956ad-103">Mobiilirakenduse avaleht</span><span class="sxs-lookup"><span data-stu-id="956ad-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="956ad-104">Selles teemas kirjeldatakse mobiilirakendust **Finance and Operations (Dynamics 365)** ja antakse linke ressurssidele, mis aitavad teil seda oma organisatsioonis juurutada.</span><span class="sxs-lookup"><span data-stu-id="956ad-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="956ad-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="956ad-105">Overview</span></span>
--------

<span data-ttu-id="956ad-106">Mobiilirakendus võimaldab teie organisatsioonil teha äriprotsessid kättesaadavaks mobiilsetes seadmetes.</span><span class="sxs-lookup"><span data-stu-id="956ad-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="956ad-107">Kui teie IT-administraator on organisatsiooni jaoks mobiilsete tööruumid lubanud, saavad kasutajad rakendusse sisse logida ja hakata äriprotsesse oma mobiilsetest seadmetest kohe käitama.</span><span class="sxs-lookup"><span data-stu-id="956ad-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="956ad-108">Mobiilirakendus sisaldab järgmisi funktsioone, mis võivad aidata tootlikkust tõsta.</span><span class="sxs-lookup"><span data-stu-id="956ad-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="956ad-109">Kasutajad saavad äriandmeid vaadata, redigeerida ja nendega tegeleda, isegi kui võrguühendus on katkendlik või mobiilne seade on täiesti võrguühenduseta.</span><span class="sxs-lookup"><span data-stu-id="956ad-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="956ad-110">Seadme võrguühenduse taastumisel sünkroonitakse võrguühenduseta andmed automaatselt.</span><span class="sxs-lookup"><span data-stu-id="956ad-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="956ad-111">IT-administraatorid või arendajad saavad luua ja avaldada mobiilseid tööruume, mis on kohandatud nende organisatsioonile.</span><span class="sxs-lookup"><span data-stu-id="956ad-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="956ad-112">Rakendus kasutab teie olemasolevaid koodilõike.</span><span class="sxs-lookup"><span data-stu-id="956ad-112">The app uses your existing code assets.</span></span> <span data-ttu-id="956ad-113">Seega ei pea te oma valideerimisprotseduure, äriloogikat ega turbekonfiguratsiooni uuesti juurutama.</span><span class="sxs-lookup"><span data-stu-id="956ad-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="956ad-114">IT-administraatorid või arendajad saavad mobiilseid tööruume hõlpsasti kujundada, kasutades veebikliendis sisalduvat klõpsatavat tööruumikujundajat.</span><span class="sxs-lookup"><span data-stu-id="956ad-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="956ad-115">IT-administraatorid või arendajad saavad soovi korral optimeerida ka tööruumide võrguühenduseta võimalusi, kasutades äriloogika laiendatavuse raamistikku.</span><span class="sxs-lookup"><span data-stu-id="956ad-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="956ad-116">Kuna andmete töötlemine jätkub, kui seade on võrguühenduseta, püsivad teie mobiilsed stsenaariumid rikkalikud ja sujuvad, isegi kui seadmetel pole pidevat võrguühendust.</span><span class="sxs-lookup"><span data-stu-id="956ad-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="956ad-117">Mobiilirakenduse elemendid</span><span class="sxs-lookup"><span data-stu-id="956ad-117">Elements of the mobile app</span></span>
<span data-ttu-id="956ad-118">Mobiilirakenduse navigeerimispaan koosneb neljast peamisest osast: armatuurlaud, tööruumid, lehed ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="956ad-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="956ad-119">[![Navigeerimispaani põhimõtted mobiilirakenduses](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="956ad-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="956ad-120">Rakenduse käivitamisel avaneb **armatuurlaud**.</span><span class="sxs-lookup"><span data-stu-id="956ad-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="956ad-121">Armatuurlaual näete avaldatud **tööruumide** loendit.</span><span class="sxs-lookup"><span data-stu-id="956ad-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="956ad-122">Igas tööruumis näete loendit **lehtedest**, mis on selle tööruumi jaoks saadaval.</span><span class="sxs-lookup"><span data-stu-id="956ad-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="956ad-123">Lehel olles saate teha mitut toimingut.</span><span class="sxs-lookup"><span data-stu-id="956ad-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="956ad-124">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="956ad-124">Here are some examples:</span></span>

    - <span data-ttu-id="956ad-125">Üksikasjalike andmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="956ad-125">View detailed data.</span></span>
    - <span data-ttu-id="956ad-126">Lehelt teistele lehtedele navigeerimine seotud andmete nägemiseks, nagu üksuse üksikasjad või read.</span><span class="sxs-lookup"><span data-stu-id="956ad-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="956ad-127">Selle lehe puhul kasutatavate **toimingute** loendi kuvamine.</span><span class="sxs-lookup"><span data-stu-id="956ad-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="956ad-128">Tegevused võimaldavad teil andmeid luua või olemasolevaid andmeid muuta.</span><span class="sxs-lookup"><span data-stu-id="956ad-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="956ad-129">Juurutusprotsess</span><span class="sxs-lookup"><span data-stu-id="956ad-129">Implementation process</span></span>
<span data-ttu-id="956ad-130">Järgmisel joonisel on näidatud nii Microsofti pakutavate kui ka kohandatud mobiilsete tööruumide juurutusprotsess.</span><span class="sxs-lookup"><span data-stu-id="956ad-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="956ad-131">[![Mobiilirakenduste juurutamise protsess](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="956ad-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="956ad-132">Järgmises tabelis on lingid ressursside juurde, mis aitavad juurutada nii Microsofti pakutavaid kui ka kohandatud mobiilseid tööruume.</span><span class="sxs-lookup"><span data-stu-id="956ad-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="956ad-133">Esimeses veerus toodud numbrid vastavad eelmisel joonisel kujutatud nummerdatud etappidele.</span><span class="sxs-lookup"><span data-stu-id="956ad-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="956ad-134">Etapp</span><span class="sxs-lookup"><span data-stu-id="956ad-134">Step</span></span></th>
<th><span data-ttu-id="956ad-135">Roll</span><span class="sxs-lookup"><span data-stu-id="956ad-135">Role</span></span></th>
<th><span data-ttu-id="956ad-136">Tegevus</span><span class="sxs-lookup"><span data-stu-id="956ad-136">Action</span></span></th>
<th><span data-ttu-id="956ad-137">Ressursid, mis aitavad teil tegevusi lõpule viia</span><span class="sxs-lookup"><span data-stu-id="956ad-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="956ad-138">1</span><span class="sxs-lookup"><span data-stu-id="956ad-138">1</span></span></td>
<td><span data-ttu-id="956ad-139">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="956ad-139">System administrator</span></span></td>
<td><span data-ttu-id="956ad-140">Juurutage rakendus Finance and Operations oma organisatsioonis.</span><span class="sxs-lookup"><span data-stu-id="956ad-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="956ad-141">Kui te e&#39;i ole veel ühtegi Microsoft Dynamics 365 versiooni juurutanud, vt jaotist <a href="../deployment/deploy-demo-environment.md">Demokeskkonna juurutamine</a>.</span><span class="sxs-lookup"><span data-stu-id="956ad-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="956ad-142">Kasutatavate mobiilsete tööruumide loendi leiate jaotisest <a href="mobile-workspaces-released.md">Hiljuti välja antud mobiilsed tööruumid</a>.</span><span class="sxs-lookup"><span data-stu-id="956ad-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="956ad-143">2</span><span class="sxs-lookup"><span data-stu-id="956ad-143">2</span></span></td>
<td><span data-ttu-id="956ad-144">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="956ad-144">System administrator</span></span></td>
<td><span data-ttu-id="956ad-145"><strong>Kui kasutat&#39;e Microsoft Dynamics 365 for Operationsi versiooni 1611:</strong> laadige alla ja installige KB-d, mis lubavad Microsofti pakutavad mobiilsed tööruumid.</span><span class="sxs-lookup"><span data-stu-id="956ad-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="956ad-146">Lisateavet vt järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="956ad-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="956ad-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Kulujuhtimise mobiilsed tööruumid</a></span><span class="sxs-lookup"><span data-stu-id="956ad-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="956ad-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiilse tööruumi varude laoseis</a></span><span class="sxs-lookup"><span data-stu-id="956ad-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="956ad-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Müügitellimuste mobiilsed tööruumid</a></span><span class="sxs-lookup"><span data-stu-id="956ad-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="956ad-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Hankija koostöö mobiilne tööruum</a></span><span class="sxs-lookup"><span data-stu-id="956ad-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="956ad-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Mobiilse tööruumi projekti ajakirje</a></span><span class="sxs-lookup"><span data-stu-id="956ad-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="956ad-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Kuluhalduse mobiilne tööruum</a></span><span class="sxs-lookup"><span data-stu-id="956ad-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="956ad-153">3</span><span class="sxs-lookup"><span data-stu-id="956ad-153">3</span></span></td>
<td><span data-ttu-id="956ad-154">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="956ad-154">System administrator</span></span></td>
<td><span data-ttu-id="956ad-155">Avaldage Microsofti pakutavad mobiilsed tööruumid.</span><span class="sxs-lookup"><span data-stu-id="956ad-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="956ad-156"><a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>
</span><span class="sxs-lookup"><span data-stu-id="956ad-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="956ad-157">4</span><span class="sxs-lookup"><span data-stu-id="956ad-157">4</span></span></td>
<td><span data-ttu-id="956ad-158">Arendaja või sõltumatu tarkvaratarnija (ISV)</span><span class="sxs-lookup"><span data-stu-id="956ad-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="956ad-159">Kasutage mobiilset platvormi kohandatud mobiilsete tööruumide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="956ad-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="956ad-160"><a href="platform/mobile-platform-home-page.md">Mobiilne platvorm</a></span><span class="sxs-lookup"><span data-stu-id="956ad-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="956ad-161">5</span><span class="sxs-lookup"><span data-stu-id="956ad-161">5</span></span></td>
<td><span data-ttu-id="956ad-162">ISV</span><span class="sxs-lookup"><span data-stu-id="956ad-162">ISV</span></span></td>
<td><span data-ttu-id="956ad-163">Looge kohandatud mobiilseid tööruume sisaldav juurutatav pakett ja laadige see üles teenusesse Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="956ad-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="956ad-164"><a href="../deployment/create-apply-deployable-package.md">Juurutatava paketi loomine</a></span><span class="sxs-lookup"><span data-stu-id="956ad-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="956ad-165">6</span><span class="sxs-lookup"><span data-stu-id="956ad-165">6</span></span></td>
<td><span data-ttu-id="956ad-166">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="956ad-166">System administrator</span></span></td>
<td><span data-ttu-id="956ad-167">Rakendage sõltumatu tarkvaratarnija (ISV) pakutavaid kohandatud tööruume sisaldav juurutatav pakett.</span><span class="sxs-lookup"><span data-stu-id="956ad-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="956ad-168"><a href="../deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a></span><span class="sxs-lookup"><span data-stu-id="956ad-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="956ad-169">7</span><span class="sxs-lookup"><span data-stu-id="956ad-169">7</span></span></td>
<td><span data-ttu-id="956ad-170">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="956ad-170">System administrator</span></span></td>
<td><span data-ttu-id="956ad-171">Avaldage ISV pakutavad kohandatud mobiilsed tööruumid.</span><span class="sxs-lookup"><span data-stu-id="956ad-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="956ad-172"><a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a></span><span class="sxs-lookup"><span data-stu-id="956ad-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="956ad-173">8</span><span class="sxs-lookup"><span data-stu-id="956ad-173">8</span></span></td>
<td><span data-ttu-id="956ad-174">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="956ad-174">User</span></span></td>
<td><span data-ttu-id="956ad-175">Laadige alla ja installige mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="956ad-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="956ad-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Rakendus Finance and Operations Androidile</a></span><span class="sxs-lookup"><span data-stu-id="956ad-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="956ad-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Rakendus Finance and Operations iOS-ile</a></span><span class="sxs-lookup"><span data-stu-id="956ad-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="956ad-178">(Windows Phone’i ei toetata)</span><span class="sxs-lookup"><span data-stu-id="956ad-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="956ad-179">9</span><span class="sxs-lookup"><span data-stu-id="956ad-179">9</span></span></td>
<td><span data-ttu-id="956ad-180">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="956ad-180">User</span></span></td>
<td><span data-ttu-id="956ad-181">Logige mobiilirakendusse sisse ja kasutage seda.</span><span class="sxs-lookup"><span data-stu-id="956ad-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="956ad-182">Rakendus sisaldab süsteemiadministraatori avaldatud mobiilseid tööruume.</span><span class="sxs-lookup"><span data-stu-id="956ad-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="956ad-183">Microsofti pakutavate mobiilsete tööruumide loendi leiate jaotisest <a href="mobile-workspaces-released.md">Hiljuti välja antud mobiilsed tööruumid</a>.</span><span class="sxs-lookup"><span data-stu-id="956ad-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="956ad-184">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="956ad-184">Troubleshooting</span></span>
[<span data-ttu-id="956ad-185">Mobiiliplatvormi ressursid</span><span class="sxs-lookup"><span data-stu-id="956ad-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)
