---
title: Avalduse andmetega dokumentide loomine
description: Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (4. osa – vormingu muutmine)“.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d95feb3395c36f9cf8a23770dc3173377067d9b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184872"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="c65e7-103">Avalduse andmetega dokumentide loomine</span><span class="sxs-lookup"><span data-stu-id="c65e7-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c65e7-104">Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (4. osa: vormingu muutmine)“.</span><span class="sxs-lookup"><span data-stu-id="c65e7-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="c65e7-105">Selles protseduuris demonstreeritakse, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks ja avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="c65e7-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="c65e7-106">Käesolevas näites kasutate ER vormingu konfiguratsiooni Intrastati aruande loomiseks ja avalduse andmete värskendamiseks arhiivimisdetailide ja aruandlusprotsessi jaoks.</span><span class="sxs-lookup"><span data-stu-id="c65e7-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="c65e7-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="c65e7-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c65e7-108">Need toimingud saab lõpule viia DEMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="c65e7-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="c65e7-109">Enne alustamist veenduge, et ettevõtte DEMF riigikontekst on BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="c65e7-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="c65e7-110">Väliskaubanduse parameetrite häälestamine</span><span class="sxs-lookup"><span data-stu-id="c65e7-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="c65e7-111">Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="c65e7-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="c65e7-112">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="c65e7-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="c65e7-113">Intrastat-aruandlusprotsessi üksikasjade arhiivimiseks tuleb tuvastada iga loodud arhiivi kirjed.</span><span class="sxs-lookup"><span data-stu-id="c65e7-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="c65e7-114">Selleks peab olema konfigureeritud spetsiaalne numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="c65e7-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="c65e7-115">Valige viide "Intrastat archive ID”.</span><span class="sxs-lookup"><span data-stu-id="c65e7-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="c65e7-116">Tippige väärtus väljale Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="c65e7-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="c65e7-117">Sisestage või valige väärtus Fore_2’ väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="c65e7-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="c65e7-118">Numbriseeria koodi ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="c65e7-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="c65e7-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c65e7-119">Click Save.</span></span>
7. <span data-ttu-id="c65e7-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c65e7-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="c65e7-121">Muudetud ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="c65e7-121">Run modified ER format</span></span>
1. <span data-ttu-id="c65e7-122">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="c65e7-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c65e7-123">Laiendage puul valikut „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="c65e7-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="c65e7-124">Tehke puul valik „Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="c65e7-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="c65e7-125">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="c65e7-125">Click Run.</span></span>
5. <span data-ttu-id="c65e7-126">Sisestage valiku Sisesta fail nimeväljale „intrastat2.xml".</span><span class="sxs-lookup"><span data-stu-id="c65e7-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="c65e7-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="c65e7-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="c65e7-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c65e7-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="c65e7-129">Vaadake üle ER-vormingu käivitamise tulemused</span><span class="sxs-lookup"><span data-stu-id="c65e7-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="c65e7-130">Vaadake genereeritud XML-fail üle.</span><span class="sxs-lookup"><span data-stu-id="c65e7-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="c65e7-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c65e7-131">Close the page.</span></span>
2. <span data-ttu-id="c65e7-132">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c65e7-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="c65e7-133">Avage vorm, mis sisaldab Intrastati kandeid, mis on kaasatud genereeritud elektroonilisse dokumenti.</span><span class="sxs-lookup"><span data-stu-id="c65e7-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="c65e7-134">Klõpsake valikut „Intrastat archive".</span><span class="sxs-lookup"><span data-stu-id="c65e7-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="c65e7-135">Kuna käivitatud elektroonilise aruandluse vorming sisaldab nüüd avalduse andmete värskenduse sätet, on lõpule viidud Intrastat-aruande üksikasjad arhiivitud.</span><span class="sxs-lookup"><span data-stu-id="c65e7-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="c65e7-136">Sellel vormil saate vaadata loodud arhiivi päisekirjet.</span><span class="sxs-lookup"><span data-stu-id="c65e7-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="c65e7-137">Klõpsake käsku Details (Üksikasjad).</span><span class="sxs-lookup"><span data-stu-id="c65e7-137">Click Details.</span></span>
    * <span data-ttu-id="c65e7-138">Sellel vormil saate vaadata loodud arhiivi üksikasju.</span><span class="sxs-lookup"><span data-stu-id="c65e7-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="c65e7-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c65e7-139">Close the page.</span></span>
6. <span data-ttu-id="c65e7-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c65e7-140">Close the page.</span></span>
7. <span data-ttu-id="c65e7-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c65e7-141">Close the page.</span></span>

