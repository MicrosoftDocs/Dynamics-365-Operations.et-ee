---
title: 'Kuluobjektide loomine  '
description: See protseduur näitab, kuidas luua kuluobjekte, importides rakenduse Dynamics 365 for Finance and Operations, Enterprise edition kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse.
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
ms.openlocfilehash: 8f63827977f080aa78fb385c60f757ad6b710005
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841245"
---
# <a name="create-cost-objects"></a><span data-ttu-id="1f0e2-103">Kuluobjektide loomine  </span><span class="sxs-lookup"><span data-stu-id="1f0e2-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f0e2-104">See protseduur näitab, kuidas luua kuluobjekte, importides rakenduse Dynamics 365 for Finance and Operations, Enterprise edition kulukeskuse finantsdimensiooni andmekonnektori kaudu kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="1f0e2-105">Selle protseduuri loomiseks kasutati demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="1f0e2-106">See protseduur on kuluarvestuse funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="1f0e2-107">Uute kuluobjektide loomine</span><span class="sxs-lookup"><span data-stu-id="1f0e2-107">Create new cost objects</span></span>
1. <span data-ttu-id="1f0e2-108">Avage Kuluarvestus > Dimensioonid > Kuluobjekti dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="1f0e2-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-109">Click New.</span></span>
3. <span data-ttu-id="1f0e2-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1f0e2-111">Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="1f0e2-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="1f0e2-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="1f0e2-114">Andmekonnektori konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1f0e2-114">Configure the data connector</span></span>
1. <span data-ttu-id="1f0e2-115">Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="1f0e2-116">Valige CostCenter dimensiooni CostCenter importimiseks kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="1f0e2-117">Valige Kulukeskus väljalt Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="1f0e2-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="1f0e2-119">Kulukeskuste importimine</span><span class="sxs-lookup"><span data-stu-id="1f0e2-119">Import cost centers</span></span>
1. <span data-ttu-id="1f0e2-120">Klõpsake valikut Dimensiooniliikmete importimine.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="1f0e2-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="1f0e2-122">Imporditud kulukeskuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="1f0e2-122">View the imported cost centers</span></span>
1. <span data-ttu-id="1f0e2-123">Klõpsake valikut Dimensiooniliikmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-123">Click View dimension members.</span></span>

