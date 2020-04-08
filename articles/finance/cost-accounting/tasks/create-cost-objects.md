---
title: 'Kuluobjektide loomine  '
description: See protseduur näitab, kuidas luua kuluobjekte, importides kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142313"
---
# <a name="create-cost-objects"></a><span data-ttu-id="2b47f-103">Kuluobjektide loomine  </span><span class="sxs-lookup"><span data-stu-id="2b47f-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b47f-104">See protseduur näitab, kuidas luua kuluobjekte, importides kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="2b47f-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="2b47f-105">Selle protseduuri loomiseks kasutati demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="2b47f-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="2b47f-106">Uute kuluobjektide loomine</span><span class="sxs-lookup"><span data-stu-id="2b47f-106">Create new cost objects</span></span>
1. <span data-ttu-id="2b47f-107">Avage Kuluarvestus > Dimensioonid > Kuluobjekti dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="2b47f-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="2b47f-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2b47f-108">Click New.</span></span>
3. <span data-ttu-id="2b47f-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2b47f-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2b47f-110">Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b47f-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="2b47f-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="2b47f-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2b47f-112">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2b47f-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="2b47f-113">Andmekonnektori konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2b47f-113">Configure the data connector</span></span>
1. <span data-ttu-id="2b47f-114">Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="2b47f-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="2b47f-115">Valige CostCenter dimensiooni CostCenter importimiseks kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="2b47f-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="2b47f-116">Valige Kulukeskus väljalt Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="2b47f-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="2b47f-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2b47f-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="2b47f-118">Kulukeskuste importimine</span><span class="sxs-lookup"><span data-stu-id="2b47f-118">Import cost centers</span></span>
1. <span data-ttu-id="2b47f-119">Klõpsake valikut Dimensiooniliikmete importimine.</span><span class="sxs-lookup"><span data-stu-id="2b47f-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="2b47f-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2b47f-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="2b47f-121">Imporditud kulukeskuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="2b47f-121">View the imported cost centers</span></span>
1. <span data-ttu-id="2b47f-122">Klõpsake valikut Dimensiooniliikmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="2b47f-122">Click View dimension members.</span></span>

