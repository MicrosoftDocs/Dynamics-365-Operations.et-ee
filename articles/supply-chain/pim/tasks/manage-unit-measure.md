--- 
title: "Mõõtühiku haldamine"
description: "See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid."
author: sorenva
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 43e645eaf6d301379182c8279dd3657a36384d5e
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="11894-103">Mõõtühiku haldamine</span><span class="sxs-lookup"><span data-stu-id="11894-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11894-104">See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.</span><span class="sxs-lookup"><span data-stu-id="11894-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="11894-105">Saate selle protseduuriga tutvuda demoandmeid või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="11894-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="11894-106">Avage Väljastatud toote haldus.</span><span class="sxs-lookup"><span data-stu-id="11894-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="11894-107">Klõpsake suvandit Ühikud.</span><span class="sxs-lookup"><span data-stu-id="11894-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="11894-108">Mõõtühiku loomine</span><span class="sxs-lookup"><span data-stu-id="11894-108">Create a unit of measure</span></span>
1. <span data-ttu-id="11894-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="11894-109">Click New.</span></span>
2. <span data-ttu-id="11894-110">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="11894-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="11894-111">Sisestage mõõtühikule viitamisel kasutatav ID või sümbol.</span><span class="sxs-lookup"><span data-stu-id="11894-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="11894-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="11894-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="11894-113">Sisestage mõõtühikule süsteemikeeles kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="11894-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="11894-114">Valige suvand väljalt Ühiku klass.</span><span class="sxs-lookup"><span data-stu-id="11894-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="11894-115">Ühiku klass määratleb, millisesse loogilisse grupeerimisse, nagu ala, mass või kogus, mõõtühik kuulub.</span><span class="sxs-lookup"><span data-stu-id="11894-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="11894-116">Sisestage number väljale Kümnendarvuline täpsus.</span><span class="sxs-lookup"><span data-stu-id="11894-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="11894-117">Määrake komakohtade arv, milleni teisendatud mõõtühik tuleb ümardada, kui arvutamine on mõõtühiku puhul lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="11894-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="11894-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="11894-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="11894-119">Ühiku teisenduste määratlemine</span><span class="sxs-lookup"><span data-stu-id="11894-119">Define unit translations</span></span>
1. <span data-ttu-id="11894-120">Klõpsake suvandit Ühiku tekstid.</span><span class="sxs-lookup"><span data-stu-id="11894-120">Click Unit texts.</span></span>
2. <span data-ttu-id="11894-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="11894-121">Click New.</span></span>
    * <span data-ttu-id="11894-122">Kasutage ühiku teksti mõõtühikut esindava ID või sümboli ümberarvestuse loomiseks kliendi- või hankijapõhises keeles välisdokumentidel kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="11894-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="11894-123">Sisestage väärtus väljale Keel või valige see.</span><span class="sxs-lookup"><span data-stu-id="11894-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="11894-124">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="11894-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="11894-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="11894-125">Click Save.</span></span>
6. <span data-ttu-id="11894-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="11894-126">Close the page.</span></span>
7. <span data-ttu-id="11894-127">Klõpsake suvandit Ümberarvestatud ühiku kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="11894-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="11894-128">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="11894-128">Click New.</span></span>
    * <span data-ttu-id="11894-129">Määratlege mõõtühiku keelepõhised kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="11894-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="11894-130">Sisestage väärtus väljale Keel või valige see.</span><span class="sxs-lookup"><span data-stu-id="11894-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="11894-131">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="11894-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="11894-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="11894-132">Click Save.</span></span>
12. <span data-ttu-id="11894-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="11894-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="11894-134">Ühiku teisendamise reeglite määratlemine</span><span class="sxs-lookup"><span data-stu-id="11894-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="11894-135">Klõpsake suvandit Ühiku teisendused.</span><span class="sxs-lookup"><span data-stu-id="11894-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="11894-136">Määratlege reeglid mõõtühiku teisendamiseks muudesse mõõtühikutesse ja neist valitud ühiku klassis.</span><span class="sxs-lookup"><span data-stu-id="11894-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="11894-137">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="11894-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="11894-138">Sisestage number väljale Tegur.</span><span class="sxs-lookup"><span data-stu-id="11894-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="11894-139">Sihtühiku ja lähteühiku vaheline teisendustegur.</span><span class="sxs-lookup"><span data-stu-id="11894-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="11894-140">Näiteks teisendustegur sentimeetrilt meetrile on 100, sest ühes meetris on 100 sentimeetrit.</span><span class="sxs-lookup"><span data-stu-id="11894-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="11894-141">Sisestage väärtus väljale Sihtühik või valige see.</span><span class="sxs-lookup"><span data-stu-id="11894-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="11894-142">Valige suvand väljalt Ümardamine.</span><span class="sxs-lookup"><span data-stu-id="11894-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="11894-143">Määratlege, kuidas teisendatud väärtust ümardada.</span><span class="sxs-lookup"><span data-stu-id="11894-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="11894-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="11894-144">Click OK.</span></span>
7. <span data-ttu-id="11894-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="11894-145">Close the page.</span></span>


