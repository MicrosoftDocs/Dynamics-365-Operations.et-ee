--- 
title: "Elektroonilise aruandluse (ER) finantsdimensioone andmeallikana kasutava aruande käitamine"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: c5aefc44adc24f9d216f9470e4307a3723690173
ms.contentlocale: et-ee
ms.lasthandoff: 11/02/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="dee17-103">Elektroonilise aruandluse (ER) finantsdimensioone andmeallikana kasutava aruande käitamine</span><span class="sxs-lookup"><span data-stu-id="dee17-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dee17-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="dee17-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="dee17-105">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="dee17-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="dee17-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (3. osa: aruande koostamine).</span><span class="sxs-lookup"><span data-stu-id="dee17-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="dee17-107">Peate konfigureerima ka dokumentide vaiketüübid lehel Elektroonilise aruande parameetrid.</span><span class="sxs-lookup"><span data-stu-id="dee17-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="dee17-108">Dokumentide vaiketüübid määratakse ka siis, kui mõne elektroonilise aruandluse konfiguratsiooni alla laadite ja impordite.</span><span class="sxs-lookup"><span data-stu-id="dee17-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="dee17-109">Aruande käitamine</span><span class="sxs-lookup"><span data-stu-id="dee17-109">Run report</span></span>
1. <span data-ttu-id="dee17-110">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="dee17-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="dee17-111">Laiendage puul jaotist Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="dee17-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="dee17-112">Valige puult Finantsdimensioonide näidismudel \ Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="dee17-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="dee17-113">Klõpsake käsku Käita.</span><span class="sxs-lookup"><span data-stu-id="dee17-113">Click Run.</span></span>
5. <span data-ttu-id="dee17-114">Sisestage või valige väärtus väljal Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="dee17-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="dee17-115">Kõigi praeguse ettevõtte dimensioonide valimiseks sisestage järgmine: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="dee17-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="dee17-116">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="dee17-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="dee17-117">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="dee17-117">Click Filter.</span></span>
8. <span data-ttu-id="dee17-118">Valige tabeli Pearaamatu tööleht rida ja väli Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="dee17-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="dee17-119">Tippige väärtus 00057 väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="dee17-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="dee17-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dee17-120">Click OK.</span></span>
11. <span data-ttu-id="dee17-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dee17-121">Click OK.</span></span>
    * <span data-ttu-id="dee17-122">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="dee17-122">Review the generated output.</span></span> <span data-ttu-id="dee17-123">Pange tähele, et iga valitud partii kande puhul esitatakse vastava finantsdimensioonikogumi finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="dee17-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="dee17-124">Käivitage see aruanne ja valige teistsugused dimensioonid nägemaks, et aruanne ei sõltu valitud dimensioonide arvust ega rakenduse Dynamics 365 for Finance and Operations, Enterprise edition selle eksemplari jaoks konfigureeritud dimensioonide arvust.</span><span class="sxs-lookup"><span data-stu-id="dee17-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


