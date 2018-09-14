--- 
title: 'Kuluobjektide loomine  '
description: "See protseduur näitab, kuidas luua kuluobjekte rakenduse Dynamics 365 for Finance and Operations, Enterprise edition kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse importimise teel."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="301f6-103">Kuluobjektide loomine  </span><span class="sxs-lookup"><span data-stu-id="301f6-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="301f6-104">See protseduur näitab, kuidas luua kuluobjekte rakenduse Dynamics 365 for Finance and Operations, Enterprise edition kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse importimise teel.</span><span class="sxs-lookup"><span data-stu-id="301f6-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="301f6-105">Selle protseduuri loomiseks kasutati demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="301f6-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="301f6-106">See protseduur on kuluarvestuse funktsiooni jaoks, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="301f6-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="301f6-107">Uute kuluobjektide loomine</span><span class="sxs-lookup"><span data-stu-id="301f6-107">Create new cost objects</span></span>
1. <span data-ttu-id="301f6-108">Avage Kuluarvestus > Dimensioonid > Kuluobjekti dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="301f6-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="301f6-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="301f6-109">Click New.</span></span>
3. <span data-ttu-id="301f6-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="301f6-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="301f6-111">Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="301f6-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="301f6-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="301f6-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="301f6-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="301f6-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="301f6-114">Andmekonnektori konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="301f6-114">Configure the data connector</span></span>
1. <span data-ttu-id="301f6-115">Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="301f6-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="301f6-116">Valige CostCenter dimensiooni CostCenter importimiseks kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="301f6-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="301f6-117">Valige Kulukeskus väljalt Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="301f6-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="301f6-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="301f6-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="301f6-119">Kulukeskuste importimine</span><span class="sxs-lookup"><span data-stu-id="301f6-119">Import cost centers</span></span>
1. <span data-ttu-id="301f6-120">Klõpsake valikut Dimensiooniliikmete importimine.</span><span class="sxs-lookup"><span data-stu-id="301f6-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="301f6-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="301f6-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="301f6-122">Imporditud kulukeskuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="301f6-122">View the imported cost centers</span></span>
1. <span data-ttu-id="301f6-123">Klõpsake valikut Dimensiooniliikmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="301f6-123">Click View dimension members.</span></span>


