---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (4. osa – aruande käivitamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit kasutama finantsdimensioone andmeallikana ER-i aruannetele. (4. osa)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7cc1a60234ef09b80950cbf0c7f18b0d65709d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565210"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="a4612-104">Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (4. osa – aruande käivitamine)</span><span class="sxs-lookup"><span data-stu-id="a4612-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4612-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="a4612-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a4612-106">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="a4612-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a4612-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (3. osa: aruande koostamine)”.</span><span class="sxs-lookup"><span data-stu-id="a4612-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="a4612-108">Peate konfigureerima ka dokumentide vaiketüübid lehel Elektroonilise aruande parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a4612-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="a4612-109">Dokumentide vaiketüübid määratakse ka siis, kui mõne elektroonilise aruandluse konfiguratsiooni alla laadite ja impordite.</span><span class="sxs-lookup"><span data-stu-id="a4612-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="a4612-110">Aruande käitamine</span><span class="sxs-lookup"><span data-stu-id="a4612-110">Run report</span></span>
1. <span data-ttu-id="a4612-111">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a4612-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a4612-112">Laiendage puul jaotist Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="a4612-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a4612-113">Valige puult Finantsdimensioonide näidismudel \ Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="a4612-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="a4612-114">Klõpsake käsku Käita.</span><span class="sxs-lookup"><span data-stu-id="a4612-114">Click Run.</span></span>
<span data-ttu-id="a4612-115">![ER-seadete leht](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="a4612-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="a4612-116">Valige või sisestage väärtus väljal Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="a4612-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="a4612-117">Kõigi praeguse ettevõtte dimensioonide valimiseks sisestage järgmine teave: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="a4612-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER-seadete leht](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="a4612-119">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="a4612-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a4612-120">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="a4612-120">Click Filter.</span></span>
8. <span data-ttu-id="a4612-121">Valige tabeli Pearaamatu tööleht rida ja väli Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="a4612-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="a4612-122">Tippige väärtus 00057 väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="a4612-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="a4612-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a4612-123">Click OK.</span></span>
11. <span data-ttu-id="a4612-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a4612-124">Click OK.</span></span>
<span data-ttu-id="a4612-125">![ER-seadete leht](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="a4612-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="a4612-126">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="a4612-126">Review the generated output.</span></span> <span data-ttu-id="a4612-127">Iga valitud partii kande puhul esitatakse asjakohase finantsdimensioonikogumi finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="a4612-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="a4612-128">Käivitage see aruanne ja valige teistsugused dimensioonid nägemiseks, et aruanne ei sõltu valitud dimensioonide arvust ega selle eksemplari jaoks konfigureeritud dimensioonide arvust.</span><span class="sxs-lookup"><span data-stu-id="a4612-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER-seadete leht](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]