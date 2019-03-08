---
title: Ettevõtte kataloogi mobiilne tööruum
description: Selles teemas käsitletakse ettevõtte kataloogi mobiilset tööruumi, mis võimaldab kasutajatel teisi oma organisatsiooni töötajaid vaadata ja nendega ühendust võtta.
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 527d40452bcf52875e3f7b04d328110147417072
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308617"
---
# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="76bd0-103">Ettevõtte kataloogi mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="76bd0-103">Company directory mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76bd0-104">See teema annab teavet **ettevõtte kataloogi** mobiilse tööruumi kohta.</span><span class="sxs-lookup"><span data-stu-id="76bd0-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="76bd0-105">See tööruum võimaldab kasutajatel oma organisatsioonis teisi töötajaid vaadata ja nendega ühendust võtta.</span><span class="sxs-lookup"><span data-stu-id="76bd0-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="76bd0-106">Seda mobiilset tööruumi saab kasutada mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="76bd0-106">This mobile workspace can be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="76bd0-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="76bd0-107">Overview</span></span>
<span data-ttu-id="76bd0-108">**Ettevõtte kataloogi** mobiilne tööruum võimaldab kasutajatel teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="76bd0-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="76bd0-109">Kuvada organisatsiooni töötajate loendi.</span><span class="sxs-lookup"><span data-stu-id="76bd0-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="76bd0-110">Otsida organisatsioonis töötajaid.</span><span class="sxs-lookup"><span data-stu-id="76bd0-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="76bd0-111">Vaadata töötajate kontaktandmeid.</span><span class="sxs-lookup"><span data-stu-id="76bd0-111">View contact information for employees.</span></span>
- <span data-ttu-id="76bd0-112">Võtta töötajatega nende profiiliandmete kaudu ühendust.</span><span class="sxs-lookup"><span data-stu-id="76bd0-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="76bd0-113">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="76bd0-113">Prerequisites</span></span>
<span data-ttu-id="76bd0-114">Enne selle mobiilse tööruumi kasutamist peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="76bd0-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76bd0-115">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="76bd0-115">Prerequisite</span></span></th>
<th><span data-ttu-id="76bd0-116">Roll</span><span class="sxs-lookup"><span data-stu-id="76bd0-116">Role</span></span></th>
<th><span data-ttu-id="76bd0-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="76bd0-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76bd0-118">Teie organisatsioonis peab olema juurutatud üks järgmistest toodetest.</span><span class="sxs-lookup"><span data-stu-id="76bd0-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="76bd0-119">Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="76bd0-119">Microsoft Dynamics 365 for Finance and Operations</span></span></li>
<li><span data-ttu-id="76bd0-120">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="76bd0-120">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="76bd0-121">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="76bd0-121">System administrator</span></span></td>
<td><span data-ttu-id="76bd0-122">Kui teie organisatsioonis pole veel Finance and Operations juurutatud, siis vt teemat <a href="../deployment/deploy-demo-environment.md">Demokeskkonna juurutamine</a>.</span><span class="sxs-lookup"><span data-stu-id="76bd0-122">If you don&#39;t already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="76bd0-123">Kui teie organisatsioonis pole veel Talentit juurutatud, pääseb süsteemiadministraator juurde prooviversioonile <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talenti veebilehel</a>.</span><span class="sxs-lookup"><span data-stu-id="76bd0-123">If you don&#39;t already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="76bd0-124"><strong>Ettevõtte kataloogi</strong> mobiilne tööruum tuleb avaldada.</span><span class="sxs-lookup"><span data-stu-id="76bd0-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="76bd0-125">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="76bd0-125">System administrator</span></span></td>
<td><span data-ttu-id="76bd0-126">Vt jaotist <a href="publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="76bd0-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="76bd0-127">Laadige alla ja installige mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="76bd0-127">Download and install the mobile app</span></span>
<span data-ttu-id="76bd0-128">Laadige alla ja installige Dynamics 365 for Unified Operationsi mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="76bd0-128">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="76bd0-129">Androidi telefonide puhul</span><span class="sxs-lookup"><span data-stu-id="76bd0-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="76bd0-130">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="76bd0-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="76bd0-131">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="76bd0-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="76bd0-132">Käivitage rakendus oma mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="76bd0-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="76bd0-133">Sisestage oma Microsoft Dynamics365 URL.</span><span class="sxs-lookup"><span data-stu-id="76bd0-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="76bd0-134">Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="76bd0-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="76bd0-135">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="76bd0-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="76bd0-136">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="76bd0-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="76bd0-137">Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.</span><span class="sxs-lookup"><span data-stu-id="76bd0-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="76bd0-138">[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="76bd0-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="76bd0-139">Ettevõtte kataloogi vaatamine mobiilse tööruumi abil</span><span class="sxs-lookup"><span data-stu-id="76bd0-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="76bd0-140">Valige mobiilirakendusest tööruum **Ettevõtte kataloog**.</span><span class="sxs-lookup"><span data-stu-id="76bd0-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="76bd0-141">Kuvatakse töötajate loend.</span><span class="sxs-lookup"><span data-stu-id="76bd0-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="76bd0-142">Valige töötaja.</span><span class="sxs-lookup"><span data-stu-id="76bd0-142">Select an employee.</span></span> <span data-ttu-id="76bd0-143">Avaneb leht **Töötaja profiil**.</span><span class="sxs-lookup"><span data-stu-id="76bd0-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="76bd0-144">Sellel lehel oleva teabe hulgas on töötaja eesnimi, perekonnanimi, ametinimetus ja osakond.</span><span class="sxs-lookup"><span data-stu-id="76bd0-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="76bd0-145">Ettevõtte kataloogist otsimine mobiilse tööruumi abil</span><span class="sxs-lookup"><span data-stu-id="76bd0-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="76bd0-146">Valige mobiilirakendusest tööruum **Ettevõtte kataloog**.</span><span class="sxs-lookup"><span data-stu-id="76bd0-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="76bd0-147">Otsingu alustamiseks sisestage väljale **Otsing** töötaja eesnimi, perekonnanimi, ametinimetus või osakond.</span><span class="sxs-lookup"><span data-stu-id="76bd0-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="76bd0-148">Valige töötaja.</span><span class="sxs-lookup"><span data-stu-id="76bd0-148">Select an employee.</span></span> <span data-ttu-id="76bd0-149">Avaneb leht **Töötaja profiil**.</span><span class="sxs-lookup"><span data-stu-id="76bd0-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="76bd0-150">Sellel lehel oleva teabe hulgas on töötaja eesnimi, perekonnanimi, ametinimetus ja osakond.</span><span class="sxs-lookup"><span data-stu-id="76bd0-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
