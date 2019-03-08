---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (4. osa – aruande käivitamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 917eae141bbb8792f02d3323054e2a4096dae551
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "345279"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a><span data-ttu-id="66ac2-103">Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (4. osa: aruande käivitamine)</span><span class="sxs-lookup"><span data-stu-id="66ac2-103">ER Use financial dimensions as a data source (Part 4: Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66ac2-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="66ac2-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="66ac2-105">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="66ac2-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="66ac2-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (3. osa: aruande koostamine).</span><span class="sxs-lookup"><span data-stu-id="66ac2-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="66ac2-107">Peate konfigureerima ka dokumentide vaiketüübid lehel Elektroonilise aruande parameetrid.</span><span class="sxs-lookup"><span data-stu-id="66ac2-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="66ac2-108">Dokumentide vaiketüübid määratakse ka siis, kui mõne elektroonilise aruandluse konfiguratsiooni alla laadite ja impordite.</span><span class="sxs-lookup"><span data-stu-id="66ac2-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="66ac2-109">Aruande käitamine</span><span class="sxs-lookup"><span data-stu-id="66ac2-109">Run report</span></span>
1. <span data-ttu-id="66ac2-110">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="66ac2-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="66ac2-111">Laiendage puul jaotist Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="66ac2-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="66ac2-112">Valige puult Finantsdimensioonide näidismudel \ Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="66ac2-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="66ac2-113">Klõpsake käsku Käita.</span><span class="sxs-lookup"><span data-stu-id="66ac2-113">Click Run.</span></span>
5. <span data-ttu-id="66ac2-114">Sisestage või valige väärtus väljal Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="66ac2-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="66ac2-115">Kõigi praeguse ettevõtte dimensioonide valimiseks sisestage järgmine: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="66ac2-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="66ac2-116">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="66ac2-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="66ac2-117">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="66ac2-117">Click Filter.</span></span>
8. <span data-ttu-id="66ac2-118">Valige tabeli Pearaamatu tööleht rida ja väli Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="66ac2-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="66ac2-119">Tippige väärtus 00057 väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="66ac2-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="66ac2-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66ac2-120">Click OK.</span></span>
11. <span data-ttu-id="66ac2-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66ac2-121">Click OK.</span></span>
    * <span data-ttu-id="66ac2-122">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="66ac2-122">Review the generated output.</span></span> <span data-ttu-id="66ac2-123">Pange tähele, et iga valitud partii kande puhul esitatakse vastava finantsdimensioonikogumi finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="66ac2-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="66ac2-124">Käivitage see aruanne ja valige teistsugused dimensioonid, et näeksite, et aruanne ei sõltu valitud dimensioonide arvust ega rakenduse Dynamics 365 for Finance and Operations, Enterprise edition selle eksemplari jaoks konfigureeritud dimensioonide arvust.</span><span class="sxs-lookup"><span data-stu-id="66ac2-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

