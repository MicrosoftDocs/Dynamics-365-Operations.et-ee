--- 
title: "Elektrooniline aruandlus. Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (2. osa – vormingu käivitamine)"
description: "Järgmistes etappides selgitatakse, kuidas kasutaja, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll, saab konfigureerida elektroonilise aruandluse vormingut, et luua aruandeid OPENXML-i töölehtede (Exceli) failidena, milles saab luua dünaamiliselt vajalikke veerge horisontaalselt laiendatavate vahemikena."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 33c1a3134659bb66a67166fec3d7f53af0aa4c6c
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2-run-format"></a><span data-ttu-id="e0569-103">Elektrooniline aruandlus Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (2. osa: vormingu käivitamine)</span><span class="sxs-lookup"><span data-stu-id="e0569-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0569-104">Järgmistes etappides selgitatakse, kuidas kasutaja, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll, saab konfigureerida elektroonilise aruandluse vormingut, et luua aruandeid OPENXML-i töölehtede (Exceli) failidena, milles saab luua dünaamiliselt vajalikke veerge horisontaalselt laiendatavate vahemikena.</span><span class="sxs-lookup"><span data-stu-id="e0569-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="e0569-105">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="e0569-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="e0569-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris „Elektrooniline aruandlus Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (1. osa: vormingu koostamine)”.</span><span class="sxs-lookup"><span data-stu-id="e0569-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="e0569-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="e0569-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="e0569-108">Loodud vormingu otsimine</span><span class="sxs-lookup"><span data-stu-id="e0569-108">Find created format</span></span>
1. <span data-ttu-id="e0569-109">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="e0569-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e0569-110">Laiendage puul jaotist Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="e0569-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="e0569-111">Valige puult Finantsdimensioonide näidismudel \ Näidisaruanne horisontaalselt laiendatavate vahemikega.</span><span class="sxs-lookup"><span data-stu-id="e0569-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="e0569-112">Käivitage vorming Exceli väljundi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e0569-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="e0569-113">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="e0569-113">Click Run.</span></span>
2. <span data-ttu-id="e0569-114">Tippige väljale Dimensiooni nimi väärtus BusinessUnit;CostCenter;Department.</span><span class="sxs-lookup"><span data-stu-id="e0569-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="e0569-115">Valige või sisestage väärtus väljal Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="e0569-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="e0569-116">Kõigi praeguse ettevõtte dimensioonide valimiseks sisestage järgmine: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="e0569-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="e0569-117">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="e0569-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="e0569-118">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="e0569-118">Click Filter.</span></span>
5. <span data-ttu-id="e0569-119">Valige tabeli Pearaamatu tööleht rida ja väli Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="e0569-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="e0569-120">Tippige väljale Kriteeriumid väärtus 00057..00058.</span><span class="sxs-lookup"><span data-stu-id="e0569-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="e0569-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="e0569-121">00057..00058</span></span>  
7. <span data-ttu-id="e0569-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e0569-122">Click OK.</span></span>
8. <span data-ttu-id="e0569-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e0569-123">Click OK.</span></span>
    * <span data-ttu-id="e0569-124">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="e0569-124">Review the generated output.</span></span> <span data-ttu-id="e0569-125">Pange tähele, et äsja loodud Exceli fail sisaldab sama veergude arvu, mis finantsdimensioonide jaoks valiti.</span><span class="sxs-lookup"><span data-stu-id="e0569-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="e0569-126">Aruande päis nendes veergudes tähistab finantsdimensioonide nimesid.</span><span class="sxs-lookup"><span data-stu-id="e0569-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="e0569-127">Kannete read nendes veergudes tähistavad finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="e0569-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="e0569-128">Käivitage see aruanne ja valige teistsugused dimensioonid nägemaks, et aruanne ei sõltu valitud dimensioonide arvust ega rakenduse Dynamics 365 for Finance and Operations, Enterprise edition selle eksemplari jaoks konfigureeritud dimensioonide arvust.</span><span class="sxs-lookup"><span data-stu-id="e0569-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


