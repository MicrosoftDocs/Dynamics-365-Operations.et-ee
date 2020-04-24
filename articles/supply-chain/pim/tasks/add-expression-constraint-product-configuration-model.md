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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab158a9f96054f7478a331b6165c01432311eb7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213373"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="124ef-103">Avaldise piirangu lisamine toote konfiguratsioonimudelile</span><span class="sxs-lookup"><span data-stu-id="124ef-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="124ef-104">See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.</span><span class="sxs-lookup"><span data-stu-id="124ef-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="124ef-105">See näitab, kuidas saate lasta lisada kõlarile nurgakaitsme, kui kasutaja on valinud metallist esivõre.</span><span class="sxs-lookup"><span data-stu-id="124ef-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="124ef-106">See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="124ef-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="124ef-107">Avaldise piirangu loomine</span><span class="sxs-lookup"><span data-stu-id="124ef-107">Create an expression constraint</span></span>
1. <span data-ttu-id="124ef-108">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="124ef-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="124ef-109">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="124ef-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="124ef-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="124ef-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="124ef-111">Selles näites kasutatakse tipptasemel kõlari mudelit.</span><span class="sxs-lookup"><span data-stu-id="124ef-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="124ef-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="124ef-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="124ef-113">Laiendage jaotist Piirangud.</span><span class="sxs-lookup"><span data-stu-id="124ef-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="124ef-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="124ef-114">Click Add.</span></span>
7. <span data-ttu-id="124ef-115">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="124ef-115">Click Create.</span></span>
8. <span data-ttu-id="124ef-116">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="124ef-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="124ef-117">Sisesta avaldis</span><span class="sxs-lookup"><span data-stu-id="124ef-117">Enter expression</span></span>
1. <span data-ttu-id="124ef-118">Klõpsake käsku Muuda avaldist.</span><span class="sxs-lookup"><span data-stu-id="124ef-118">Click Edit expression.</span></span>
    * <span data-ttu-id="124ef-119">Kui avate selles etapis ülesande salvestises kasutajaliidese, saate kasutada piiranguavaldise koostamiseks IntelliSense’i ja sümbolite loendit.</span><span class="sxs-lookup"><span data-stu-id="124ef-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="124ef-120">Sisestage väljale ConstraintBody tekst Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="124ef-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="124ef-121">See avaldise loogika väidab: kui esivõre on metallist, tuleb valida nurkade kaitse suvand.</span><span class="sxs-lookup"><span data-stu-id="124ef-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="124ef-122">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="124ef-122">Click Validate.</span></span>
    * <span data-ttu-id="124ef-123">Kontrollimisfunktsioon vaatab piiranguavaldise läbi ja kontrollib süntaksivigu.</span><span class="sxs-lookup"><span data-stu-id="124ef-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="124ef-124">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="124ef-124">Click Close.</span></span>
5. <span data-ttu-id="124ef-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="124ef-125">Click OK.</span></span>

