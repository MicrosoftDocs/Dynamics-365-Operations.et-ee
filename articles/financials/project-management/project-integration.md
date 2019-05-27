---
title: Microsoft Projecti kliendi integreerimine
description: Projektigraafiku kavandamine ja haldamine võib olla keeruline, seega vajavad projektijuhid seda ülesannet hõlbustavaid vahendeid. Microsoft Projecti kliendiga integreerimine aitab projekti tööjaotuse struktuuri avada ja hallata.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 48feb0182c623714b2acffafc42016c0471ba6c1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556571"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="5684f-104">Microsoft Projecti kliendi integreerimine</span><span class="sxs-lookup"><span data-stu-id="5684f-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5684f-105">Projektigraafiku kavandamine ja haldamine võib olla keeruline, seega vajavad projektijuhid seda ülesannet hõlbustavaid vahendeid.</span><span class="sxs-lookup"><span data-stu-id="5684f-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="5684f-106">Microsoft Projecti kliendiga integreerimine aitab projekti tööjaotuse struktuuri avada ja hallata.</span><span class="sxs-lookup"><span data-stu-id="5684f-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="5684f-107">Projektijuht saab muudatusi saata tagasi Finance and Operationsi projekti tööjaotuse struktuuri.</span><span class="sxs-lookup"><span data-stu-id="5684f-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="5684f-108">Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations juulikuu värskendust, peate installima KB 4054797 ja 4055884.</span><span class="sxs-lookup"><span data-stu-id="5684f-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="5684f-109">Microsoft Projecti kliendi lisandmooduli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5684f-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="5684f-110">Microsoft Projecti kliendiga integreerimise lubamiseks tuleb kasutaja Microsoft Projecti klientrakendusse installida Microsoft Dynamics 365 lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="5684f-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="5684f-111">Selleks tuleb avada **Projektihalduse tööruum**.</span><span class="sxs-lookup"><span data-stu-id="5684f-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="5684f-112">•   Klõpsake suvandit **Projecti kliendi lisandmooduli konfigureerimine** tööruumi jaotises **Lingid** > **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="5684f-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="5684f-113">•   Klõpsake käsku **Ava** ning seejärel selle kuvamisel käsku **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="5684f-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="5684f-114">Microsoft Projecti kliendis oleva projekti tööjaotuse struktuuri mustandi avamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="5684f-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="5684f-115">Kui rakenduse Finance and Operations projektis on juba loodud tööjaotuse struktuur, saab seda avada Microsoft Projecti klientrakenduses, kui tööjaotuse struktuur on mustandi olekus.</span><span class="sxs-lookup"><span data-stu-id="5684f-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="5684f-116">Lehelt **Projekt** avamiseks klõpsake vahekaardil **Plaan** linki **Microsoft Projectis avamine**. Selle lehe saate avada ka Microsoft Projecti klientrakenduses, klõpsates vahekaardil **Microsoft Dynamics 365** käsku **Ava**. Valige loendist **Juriidiline isik** ja **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="5684f-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="5684f-117">Kui kasutate brauserina Internet Explorerit, peate faili selle allalaadimise asukohast käsitsi avamiseks klõpsama käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5684f-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="5684f-118">Võite ka faili Microsoft Projecti klientrakenduses avamiseks klõpsata käsku **Salvesta ja ava**.</span><span class="sxs-lookup"><span data-stu-id="5684f-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="5684f-119">Ärge nimetage faili salvestamisel ümber.</span><span class="sxs-lookup"><span data-stu-id="5684f-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="5684f-120">Enne Microsoft Projecti klientrakendust kasutava faili redigeerimist peate selle välja registreerima. Klõpsake vahekaardil **Microsoft Dynamics 365** käsku **Registreeri välja**. See takistab teistel kasutajatel tööjaotuse struktuuri samal ajal rakenduses Finance and Operations redigeerida.</span><span class="sxs-lookup"><span data-stu-id="5684f-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="5684f-121">Tööjaotuse struktuuri avaldamiseks pärast redigeerimist klõpsake vahekaardil **Microsoft Dynamics 365** käsku **Registreeri sisse**.</span><span class="sxs-lookup"><span data-stu-id="5684f-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="5684f-122">Kui projektile on rakenduses Finance and Operations juba lisatud projekti töörühm, täidetakse ressursiloend töörühma liikmetega.</span><span class="sxs-lookup"><span data-stu-id="5684f-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="5684f-123">Kas projekti töörühma ei ole veel projektile lisatud, saate ressursse valida ja töörühma luua Microsoft Projecti klientrakenduses, klõpsates vahekaardil **Microsoft Dynamics 365** nuppu **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="5684f-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="5684f-124">Sisseregistreerimise osana sünkroonitakse järgmised andmed tagasi rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5684f-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="5684f-125">•   Ülesande nimi</span><span class="sxs-lookup"><span data-stu-id="5684f-125">•   Task name</span></span>

<span data-ttu-id="5684f-126">•   Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="5684f-126">•   Start date</span></span>

<span data-ttu-id="5684f-127">•   Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="5684f-127">•   Finish date</span></span>

<span data-ttu-id="5684f-128">•   Eelkäijad</span><span class="sxs-lookup"><span data-stu-id="5684f-128">•   Predecessors</span></span>

<span data-ttu-id="5684f-129">•   Ressursinimed</span><span class="sxs-lookup"><span data-stu-id="5684f-129">•   Resource names</span></span>

<span data-ttu-id="5684f-130">•   Kategooria:</span><span class="sxs-lookup"><span data-stu-id="5684f-130">•   Category</span></span>

<span data-ttu-id="5684f-131">•   Ressursikategooria</span><span class="sxs-lookup"><span data-stu-id="5684f-131">•   Resource category</span></span>

<span data-ttu-id="5684f-132">•   Töötunnid</span><span class="sxs-lookup"><span data-stu-id="5684f-132">•   Work hours</span></span>

<span data-ttu-id="5684f-133">•   Märkmed</span><span class="sxs-lookup"><span data-stu-id="5684f-133">•   Notes</span></span>

<span data-ttu-id="5684f-134">•   Prioriteet</span><span class="sxs-lookup"><span data-stu-id="5684f-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="5684f-135">Microsoft Projecti klientrakendusse veergude lisamisel ei salvestata neid faili ega kuvata faili uuesti avamisel.</span><span class="sxs-lookup"><span data-stu-id="5684f-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="5684f-136">Microsoft Projecti klientrakenduse abil olemasoleva projekti tööjaotuse struktuuri loomine</span><span class="sxs-lookup"><span data-stu-id="5684f-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="5684f-137">Microsoft Projecti klientrakenduse abil olemasoleva projekti tööjaotuse struktuuri loomiseks tehke läbi järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="5684f-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="5684f-138">Avage Microsoft Projecti klient.</span><span class="sxs-lookup"><span data-stu-id="5684f-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5684f-139">Klõpsake vahekaardil **Microsoft Dynamics 365** käsku **Ava**.</span><span class="sxs-lookup"><span data-stu-id="5684f-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="5684f-140">Valige projekti jaoks **Juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="5684f-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="5684f-141">Valige **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="5684f-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="5684f-142">Klõpsake vahekaardil **Microsoft Dynamics 365** valikut **Registreeri välja**.</span><span class="sxs-lookup"><span data-stu-id="5684f-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="5684f-143">Kui olete valmis seda rakenduses Finance and Operations avaldama, klõpsake vahekaardil **Microsoft Dynamics 365**  käsku **Registreeri sisse**.</span><span class="sxs-lookup"><span data-stu-id="5684f-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="5684f-144">Microsoft Projecti klientrakenduse abil olemasoleva projekti tööjaotuse asendamine</span><span class="sxs-lookup"><span data-stu-id="5684f-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="5684f-145">Microsoft Projecti klientrakenduse abil uue tööjaotuse struktuuri loomiseks ja olemasoleva projekti tööjaotuse asendamiseks tehke läbi järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="5684f-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="5684f-146">Avage Microsoft Projecti klient.</span><span class="sxs-lookup"><span data-stu-id="5684f-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5684f-147">Looge Microsoft Projecti kliendil graafik.</span><span class="sxs-lookup"><span data-stu-id="5684f-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="5684f-148">Klõpsake vahekaardil **Microsoft Dynamics 365** käske **Salvesta muudatused** > **Asenda olemasolev projekt**.</span><span class="sxs-lookup"><span data-stu-id="5684f-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="5684f-149">Valige projekti jaoks **Juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="5684f-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="5684f-150">Valige **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="5684f-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="5684f-151">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="5684f-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="5684f-152">Uue projekti loomine Microsoft Projecti klientrakenduses</span><span class="sxs-lookup"><span data-stu-id="5684f-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="5684f-153">Avage Microsoft Projecti klient.</span><span class="sxs-lookup"><span data-stu-id="5684f-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5684f-154">Looge Microsoft Projecti kliendil graafik.</span><span class="sxs-lookup"><span data-stu-id="5684f-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="5684f-155">Klõpsake vahekaardil **Microsoft Dynamics 365** käske **Salvesta muudatused** > **Salvesta uude projekti**.</span><span class="sxs-lookup"><span data-stu-id="5684f-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="5684f-156">Valige projekti jaoks **Juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="5684f-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="5684f-157">Vajaduse korral sisestage **Projekti ID**.</span><span class="sxs-lookup"><span data-stu-id="5684f-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="5684f-158">Sisestage **Projekti nimi**.</span><span class="sxs-lookup"><span data-stu-id="5684f-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="5684f-159">Valige **Projekti tüüp**, **Projektigrupp** ja **Projektilepingu ID**.</span><span class="sxs-lookup"><span data-stu-id="5684f-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="5684f-160">Teise võimalusena saate luua uue projektilepingu, klõpsates suvandit **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5684f-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="5684f-161">Valige ressurssideks kasutatav **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="5684f-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="5684f-162">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="5684f-162">Click **OK**.</span></span>
