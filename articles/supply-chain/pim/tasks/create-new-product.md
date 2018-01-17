--- 
title: Uue toote loomine
description: "Selles ülesandes selgitatakse, kuidas luua uut ühiskasutuses toodet."
author: YuyuScheller
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 0ea85775e7be86eead716e88ef9d51cae9c007f3
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---
# <a name="create-a-new-product"></a><span data-ttu-id="6f55e-103">Uue toote loomine</span><span class="sxs-lookup"><span data-stu-id="6f55e-103">Create a new product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f55e-104">Selles ülesandes selgitatakse, kuidas luua uut ühiskasutuses toodet.</span><span class="sxs-lookup"><span data-stu-id="6f55e-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="6f55e-105">Tavaliselt teeb seda toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="6f55e-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="6f55e-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="6f55e-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="6f55e-107">Avage Tooteteabe haldus > Tooted > Tooted.</span><span class="sxs-lookup"><span data-stu-id="6f55e-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="6f55e-108">Toote loomine</span><span class="sxs-lookup"><span data-stu-id="6f55e-108">Create a product</span></span>
1. <span data-ttu-id="6f55e-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6f55e-109">Click New.</span></span>
2. <span data-ttu-id="6f55e-110">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="6f55e-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="6f55e-111">Kui toote koodile ei ole numbriseeriat seadistatud, tuleb see sisestada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="6f55e-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="6f55e-112">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="6f55e-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="6f55e-113">Toote nimi on vaikimisi otsingu nimi.</span><span class="sxs-lookup"><span data-stu-id="6f55e-113">The product name defaults to the search name.</span></span> <span data-ttu-id="6f55e-114">Saate seda vajaduse korral muuta.</span><span class="sxs-lookup"><span data-stu-id="6f55e-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="6f55e-115">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6f55e-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="6f55e-116">Dimensioonigruppide seadistamine</span><span class="sxs-lookup"><span data-stu-id="6f55e-116">Set up dimension groups</span></span>
1. <span data-ttu-id="6f55e-117">Klõpsake rippdialoogi avamiseks suvandit Dimensioonigrupid.</span><span class="sxs-lookup"><span data-stu-id="6f55e-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="6f55e-118">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="6f55e-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f55e-119">Laoala dimensiooni grupp määrab, millised laoala dimensioonid peate sisestama iga toote kande kohta ja kuidas seda varudes jälgitakse.</span><span class="sxs-lookup"><span data-stu-id="6f55e-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="6f55e-120">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="6f55e-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f55e-121">Jälgimisdimensiooni grupp määrab, millised jälgimisdimensioonid peate sisestama iga toote kande kohta ja kuidas seda varudes käsitletakse.</span><span class="sxs-lookup"><span data-stu-id="6f55e-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="6f55e-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6f55e-122">Click OK.</span></span>


