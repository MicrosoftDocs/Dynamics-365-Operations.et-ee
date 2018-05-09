--- 
title: 'Kuluelementide loomine  '
description: "Kuluarvestuses on kuluelementide loomiseks mitu võimalust."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f9eda5f8a2ebf428d7b9b8197a2c8c5f817b9799
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="create-cost-elements"></a><span data-ttu-id="ec765-103">Kuluelementide loomine  </span><span class="sxs-lookup"><span data-stu-id="ec765-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec765-104">Kuluarvestuses on kuluelementide loomiseks mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="ec765-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="ec765-105">See protseduur näitab, kuidas luua kuluelemente, importides põhikontod andmekonnektori kaudu.</span><span class="sxs-lookup"><span data-stu-id="ec765-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="ec765-106">Selle protseduuri loomiseks kasutati demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="ec765-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="ec765-107">See protseduur on kuluarvestuse funktsiooni jaoks, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="ec765-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="ec765-108">Uute kuluelementide loomine</span><span class="sxs-lookup"><span data-stu-id="ec765-108">Create new cost elements</span></span>
1. <span data-ttu-id="ec765-109">Avage Kuluarvestus > Dimensioonid > Kuluelemendi dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="ec765-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="ec765-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ec765-110">Click New.</span></span>
3. <span data-ttu-id="ec765-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ec765-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ec765-112">Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="ec765-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="ec765-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ec765-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ec765-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ec765-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="ec765-115">Andmekonnektori konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ec765-115">Configure the data connector</span></span>
1. <span data-ttu-id="ec765-116">Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="ec765-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="ec765-117">Sisestage väärtus väljale Kontoplaan või valige see.</span><span class="sxs-lookup"><span data-stu-id="ec765-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="ec765-118">Jagatud kontoplaani kasutamiseks valige Jagatud.</span><span class="sxs-lookup"><span data-stu-id="ec765-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="ec765-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ec765-119">Click New.</span></span>
4. <span data-ttu-id="ec765-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ec765-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ec765-121">Saate oma kriteeriumide täitmiseks rakendada kontodele filtreid.</span><span class="sxs-lookup"><span data-stu-id="ec765-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="ec765-122">Sisestage väärtus väljale Põhikontolt või valige see.</span><span class="sxs-lookup"><span data-stu-id="ec765-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="ec765-123">Sisestage väärtus väljale Põhikontole või valige see.</span><span class="sxs-lookup"><span data-stu-id="ec765-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="ec765-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ec765-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="ec765-125">Impordi põhikontod</span><span class="sxs-lookup"><span data-stu-id="ec765-125">Import main accounts</span></span>
1. <span data-ttu-id="ec765-126">Klõpsake valikut Dimensiooniliikmete importimine.</span><span class="sxs-lookup"><span data-stu-id="ec765-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="ec765-127">Põhikontod imporditakse kuluarvestusse ja neid kasutatakse kuluelementidena.</span><span class="sxs-lookup"><span data-stu-id="ec765-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="ec765-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ec765-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="ec765-129">Imporditud kontode vaatamine kuluelementidena</span><span class="sxs-lookup"><span data-stu-id="ec765-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="ec765-130">Klõpsake valikut Dimensiooniliikmete kuvamine.</span><span class="sxs-lookup"><span data-stu-id="ec765-130">Click View dimension members.</span></span>
    * <span data-ttu-id="ec765-131">Kuva imporditud pearaamatukontod kuluelementidena oma ettevõttes, kuhu kuluvoo saab suunata.</span><span class="sxs-lookup"><span data-stu-id="ec765-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  


