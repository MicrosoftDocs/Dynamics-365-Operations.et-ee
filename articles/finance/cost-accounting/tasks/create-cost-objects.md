---
title: 'Kuluobjektide loomine  '
description: See protseduur näitab, kuidas luua kuluobjekte, importides kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810050"
---
# <a name="create-cost-objects"></a><span data-ttu-id="c0df6-103">Kuluobjektide loomine  </span><span class="sxs-lookup"><span data-stu-id="c0df6-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0df6-104">See protseduur näitab, kuidas luua kuluobjekte, importides kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="c0df6-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="c0df6-105">Selle protseduuri loomiseks kasutati demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="c0df6-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="c0df6-106">Uute kuluobjektide loomine</span><span class="sxs-lookup"><span data-stu-id="c0df6-106">Create new cost objects</span></span>
1. <span data-ttu-id="c0df6-107">Avage Kuluarvestus > Dimensioonid > Kuluobjekti dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="c0df6-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="c0df6-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c0df6-108">Click New.</span></span>
3. <span data-ttu-id="c0df6-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c0df6-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c0df6-110">Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="c0df6-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="c0df6-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c0df6-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c0df6-112">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c0df6-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="c0df6-113">Andmekonnektori konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c0df6-113">Configure the data connector</span></span>
1. <span data-ttu-id="c0df6-114">Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="c0df6-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="c0df6-115">Valige CostCenter dimensiooni CostCenter importimiseks kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="c0df6-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="c0df6-116">Valige Kulukeskus väljalt Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="c0df6-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="c0df6-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c0df6-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="c0df6-118">Kulukeskuste importimine</span><span class="sxs-lookup"><span data-stu-id="c0df6-118">Import cost centers</span></span>
1. <span data-ttu-id="c0df6-119">Klõpsake valikut Dimensiooniliikmete importimine.</span><span class="sxs-lookup"><span data-stu-id="c0df6-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="c0df6-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c0df6-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="c0df6-121">Imporditud kulukeskuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="c0df6-121">View the imported cost centers</span></span>
1. <span data-ttu-id="c0df6-122">Klõpsake valikut Dimensiooniliikmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="c0df6-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]