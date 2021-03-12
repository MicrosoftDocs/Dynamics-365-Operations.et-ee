---
title: Avaldise piirangu lisamine toote konfiguratsioonimudelile
description: See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 411e20bd8631b70df981c5785f502693d5ba3705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987125"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="e6d4f-103">Avaldise piirangu lisamine toote konfiguratsioonimudelile</span><span class="sxs-lookup"><span data-stu-id="e6d4f-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6d4f-104">See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="e6d4f-105">See näitab, kuidas saate lasta lisada kõlarile nurgakaitsme, kui kasutaja on valinud metallist esivõre.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="e6d4f-106">See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="e6d4f-107">Avaldise piirangu loomine</span><span class="sxs-lookup"><span data-stu-id="e6d4f-107">Create an expression constraint</span></span>
1. <span data-ttu-id="e6d4f-108">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e6d4f-109">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="e6d4f-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e6d4f-111">Selles näites kasutatakse tipptasemel kõlari mudelit.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="e6d4f-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e6d4f-113">Laiendage jaotist Piirangud.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="e6d4f-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-114">Click Add.</span></span>
7. <span data-ttu-id="e6d4f-115">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-115">Click Create.</span></span>
8. <span data-ttu-id="e6d4f-116">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="e6d4f-117">Sisesta avaldis</span><span class="sxs-lookup"><span data-stu-id="e6d4f-117">Enter expression</span></span>
1. <span data-ttu-id="e6d4f-118">Klõpsake käsku Muuda avaldist.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-118">Click Edit expression.</span></span>
    * <span data-ttu-id="e6d4f-119">Kui avate selles etapis ülesande salvestises kasutajaliidese, saate kasutada piiranguavaldise koostamiseks IntelliSense’i ja sümbolite loendit.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="e6d4f-120">Sisestage väljale ConstraintBody tekst Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="e6d4f-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="e6d4f-121">See avaldise loogika väidab: kui esivõre on metallist, tuleb valida nurkade kaitse suvand.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="e6d4f-122">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-122">Click Validate.</span></span>
    * <span data-ttu-id="e6d4f-123">Kontrollimisfunktsioon vaatab piiranguavaldise läbi ja kontrollib süntaksivigu.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="e6d4f-124">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-124">Click Close.</span></span>
5. <span data-ttu-id="e6d4f-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e6d4f-125">Click OK.</span></span>

