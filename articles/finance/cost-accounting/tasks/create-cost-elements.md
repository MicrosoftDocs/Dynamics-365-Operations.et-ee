---
title: 'Kuluelementide loomine  '
description: Kuluarvestuses on kuluelementide loomiseks mitu võimalust.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f58b6896dd5b9e257bf6066e56142dcd2d8fb45
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990788"
---
# <a name="create-cost-elements"></a><span data-ttu-id="b3c46-103">Kuluelementide loomine  </span><span class="sxs-lookup"><span data-stu-id="b3c46-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3c46-104">Kuluarvestuses on kuluelementide loomiseks mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="b3c46-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="b3c46-105">See protseduur näitab, kuidas luua kuluelemente, importides põhikontod andmekonnektori kaudu.</span><span class="sxs-lookup"><span data-stu-id="b3c46-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="b3c46-106">Selle protseduuri loomiseks kasutati demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="b3c46-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="b3c46-107">See protseduur on kuluarvestuse funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="b3c46-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="b3c46-108">Uute kuluelementide loomine</span><span class="sxs-lookup"><span data-stu-id="b3c46-108">Create new cost elements</span></span>
1. <span data-ttu-id="b3c46-109">Avage Kuluarvestus > Dimensioonid > Kuluelemendi dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="b3c46-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="b3c46-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b3c46-110">Click New.</span></span>
3. <span data-ttu-id="b3c46-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="b3c46-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b3c46-112">Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="b3c46-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b3c46-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b3c46-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b3c46-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b3c46-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b3c46-115">Andmekonnektori konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b3c46-115">Configure the data connector</span></span>
1. <span data-ttu-id="b3c46-116">Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="b3c46-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="b3c46-117">Sisestage väärtus väljale Kontoplaan või valige see.</span><span class="sxs-lookup"><span data-stu-id="b3c46-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="b3c46-118">Jagatud kontoplaani kasutamiseks valige Jagatud.</span><span class="sxs-lookup"><span data-stu-id="b3c46-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="b3c46-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b3c46-119">Click New.</span></span>
4. <span data-ttu-id="b3c46-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b3c46-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b3c46-121">Saate oma kriteeriumide täitmiseks rakendada kontodele filtreid.</span><span class="sxs-lookup"><span data-stu-id="b3c46-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="b3c46-122">Sisestage väärtus väljale Põhikontolt või valige see.</span><span class="sxs-lookup"><span data-stu-id="b3c46-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="b3c46-123">Sisestage väärtus väljale Põhikontole või valige see.</span><span class="sxs-lookup"><span data-stu-id="b3c46-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="b3c46-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b3c46-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="b3c46-125">Impordi põhikontod</span><span class="sxs-lookup"><span data-stu-id="b3c46-125">Import main accounts</span></span>
1. <span data-ttu-id="b3c46-126">Klõpsake valikut Dimensiooniliikmete importimine.</span><span class="sxs-lookup"><span data-stu-id="b3c46-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="b3c46-127">Põhikontod imporditakse kuluarvestusse ja neid kasutatakse kuluelementidena.</span><span class="sxs-lookup"><span data-stu-id="b3c46-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="b3c46-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b3c46-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="b3c46-129">Imporditud kontode vaatamine kuluelementidena</span><span class="sxs-lookup"><span data-stu-id="b3c46-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="b3c46-130">Klõpsake valikut Dimensiooniliikmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="b3c46-130">Click View dimension members.</span></span>
    * <span data-ttu-id="b3c46-131">Kuva imporditud pearaamatukontod kuluelementidena oma ettevõttes, kuhu kuluvoo saab suunata.</span><span class="sxs-lookup"><span data-stu-id="b3c46-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

