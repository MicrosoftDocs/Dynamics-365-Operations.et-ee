---
title: Mõõtühiku haldamine
description: See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71b478ca294719c20af9de16c27139aeca36bf07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992291"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="56c02-103">Mõõtühiku haldamine</span><span class="sxs-lookup"><span data-stu-id="56c02-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56c02-104">See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.</span><span class="sxs-lookup"><span data-stu-id="56c02-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="56c02-105">Saate selle protseduuriga tutvuda demoandmeid või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="56c02-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="56c02-106">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="56c02-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="56c02-107">Klõpsake suvandit **Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="56c02-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="56c02-108">Mõõtühiku loomine</span><span class="sxs-lookup"><span data-stu-id="56c02-108">Create a unit of measure</span></span>
1. <span data-ttu-id="56c02-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="56c02-109">Click **New**.</span></span>
2. <span data-ttu-id="56c02-110">Sisestage väärtus väljale **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="56c02-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="56c02-111">Sisestage mõõtühikule viitamisel kasutatav ID või sümbol.</span><span class="sxs-lookup"><span data-stu-id="56c02-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="56c02-112">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="56c02-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="56c02-113">Sisestage mõõtühikule süsteemikeeles kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="56c02-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="56c02-114">Valige suvand väljalt **Ühiku klass**.</span><span class="sxs-lookup"><span data-stu-id="56c02-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="56c02-115">Ühiku klass määratleb, millisesse loogilisse grupeerimisse, nagu ala, mass või kogus, mõõtühik kuulub.</span><span class="sxs-lookup"><span data-stu-id="56c02-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="56c02-116">Sisestage number väljale **Kümnendarvuline täpsus**.</span><span class="sxs-lookup"><span data-stu-id="56c02-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="56c02-117">Määrake komakohtade arv, milleni teisendatud mõõtühik tuleb ümardada, kui arvutamine on mõõtühiku puhul lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="56c02-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="56c02-118">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="56c02-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="56c02-119">Ühiku teisenduste määratlemine</span><span class="sxs-lookup"><span data-stu-id="56c02-119">Define unit translations</span></span>
1. <span data-ttu-id="56c02-120">**Toimingupaanil** klõpsake **Ühiku tekstid**.</span><span class="sxs-lookup"><span data-stu-id="56c02-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="56c02-121">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="56c02-121">Click **New**.</span></span> <span data-ttu-id="56c02-122">Kasutage ühiku teksti mõõtühikut esindava ID või sümboli ümberarvestuse loomiseks kliendi- või hankijapõhises keeles välisdokumentidel kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="56c02-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="56c02-123">Sisestage väärtus väljale **Keel** või valige see.</span><span class="sxs-lookup"><span data-stu-id="56c02-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="56c02-124">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="56c02-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="56c02-125">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="56c02-125">Click **Save**.</span></span>
6. <span data-ttu-id="56c02-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56c02-126">Close the page.</span></span>
7. <span data-ttu-id="56c02-127">Klõpsake **Toimingupaanil** **Ümberarvestatud ühku kirjeldused**.</span><span class="sxs-lookup"><span data-stu-id="56c02-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="56c02-128">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="56c02-128">Click **New**.</span></span> <span data-ttu-id="56c02-129">Määratlege mõõtühiku keelepõhised kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="56c02-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="56c02-130">Sisestage väärtus väljale **Keel** või valige see.</span><span class="sxs-lookup"><span data-stu-id="56c02-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="56c02-131">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="56c02-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="56c02-132">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="56c02-132">Click **Save**.</span></span>
12. <span data-ttu-id="56c02-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56c02-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="56c02-134">Ühiku teisendamise reeglite määratlemine</span><span class="sxs-lookup"><span data-stu-id="56c02-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="56c02-135">Klõpsake **Toimingupaanil** **Ühiku teisendused**.</span><span class="sxs-lookup"><span data-stu-id="56c02-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="56c02-136">Määratlege reeglid mõõtühiku teisendamiseks muudesse mõõtühikutesse ja neist valitud ühiku klassis.</span><span class="sxs-lookup"><span data-stu-id="56c02-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="56c02-137">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="56c02-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="56c02-138">Sisestage number väljale **Tegur**.</span><span class="sxs-lookup"><span data-stu-id="56c02-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="56c02-139">Sihtühiku ja lähteühiku vaheline teisendustegur.</span><span class="sxs-lookup"><span data-stu-id="56c02-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="56c02-140">Näiteks teisendustegur sentimeetrilt meetrile on 100, sest ühes meetris on 100 sentimeetrit.</span><span class="sxs-lookup"><span data-stu-id="56c02-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="56c02-141">Sisestage või valige väärtus väljale **Kuni ühikuni**.</span><span class="sxs-lookup"><span data-stu-id="56c02-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="56c02-142">Valige suvand väljal **Ümardamine**.</span><span class="sxs-lookup"><span data-stu-id="56c02-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="56c02-143">Määratlege, kuidas teisendatud väärtust ümardada.</span><span class="sxs-lookup"><span data-stu-id="56c02-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="56c02-144">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="56c02-144">Click **OK**.</span></span>
7. <span data-ttu-id="56c02-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56c02-145">Close the page.</span></span>

