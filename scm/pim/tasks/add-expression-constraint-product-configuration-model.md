--- 
title: Avaldise piirangu lisamine toote konfiguratsioonimudelile
description: "See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="25b1d-103">Avaldise piirangu lisamine toote konfiguratsioonimudelile</span><span class="sxs-lookup"><span data-stu-id="25b1d-103">Add an expression constraint to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25b1d-104">See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.</span><span class="sxs-lookup"><span data-stu-id="25b1d-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="25b1d-105">See näitab, kuidas saate lasta lisada kõlarile nurgakaitsme, kui kasutaja on valinud metallist esivõre.</span><span class="sxs-lookup"><span data-stu-id="25b1d-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="25b1d-106">See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="25b1d-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="25b1d-107">Avaldise piirangu loomine</span><span class="sxs-lookup"><span data-stu-id="25b1d-107">Create an expression constraint</span></span>
1. <span data-ttu-id="25b1d-108">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="25b1d-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="25b1d-109">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="25b1d-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="25b1d-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25b1d-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="25b1d-111">Selles näites kasutatakse tipptasemel kõlari mudelit.</span><span class="sxs-lookup"><span data-stu-id="25b1d-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="25b1d-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25b1d-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="25b1d-113">Laiendage jaotist Piirangud.</span><span class="sxs-lookup"><span data-stu-id="25b1d-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="25b1d-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="25b1d-114">Click Add.</span></span>
7. <span data-ttu-id="25b1d-115">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="25b1d-115">Click Create.</span></span>
8. <span data-ttu-id="25b1d-116">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="25b1d-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="25b1d-117">Sisesta avaldis</span><span class="sxs-lookup"><span data-stu-id="25b1d-117">Enter expression</span></span>
1. <span data-ttu-id="25b1d-118">Klõpsake käsku Muuda avaldist.</span><span class="sxs-lookup"><span data-stu-id="25b1d-118">Click Edit expression.</span></span>
    * <span data-ttu-id="25b1d-119">Kui avate selles etapis ülesande salvestises kasutajaliidese, saate kasutada piiranguavaldise koostamiseks IntelliSense’i ja sümbolite loendit.</span><span class="sxs-lookup"><span data-stu-id="25b1d-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="25b1d-120">Sisestage väljale ConstraintBody tekst Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="25b1d-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="25b1d-121">See avaldise loogika väidab: kui esivõre on metallist, tuleb valida nurkade kaitse suvand.</span><span class="sxs-lookup"><span data-stu-id="25b1d-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="25b1d-122">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="25b1d-122">Click Validate.</span></span>
    * <span data-ttu-id="25b1d-123">Kontrollimisfunktsioon vaatab piiranguavaldise läbi ja kontrollib süntaksivigu.</span><span class="sxs-lookup"><span data-stu-id="25b1d-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="25b1d-124">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="25b1d-124">Click Close.</span></span>
5. <span data-ttu-id="25b1d-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="25b1d-125">Click OK.</span></span>


