---
title: Lahendaja strateegia toote konfiguratsiooni jaoks
description: "Selles teemas kirjeldatakse, kuidas kasutada lahendaja strateegiat toote konfiguratsiooni jõudluse parandamiseks."
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 4544128e580b30b14a6236a9a6147ff0a8641d72
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="844ca-103">Lahendaja strateegia toote konfiguratsiooni jaoks</span><span class="sxs-lookup"><span data-stu-id="844ca-103">Solver strategy for product configuration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="844ca-104">Selles teemas kirjeldatakse, kuidas kasutada lahendaja strateegiat toote konfiguratsiooni jõudluse parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="844ca-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="844ca-105">Lahendaja strateegia mõiste võeti esimest korda kasutusele rakenduse Microsoft Dynamics AX 2012 R2 kumulatiivses värskenduses 7 (CU7).</span><span class="sxs-lookup"><span data-stu-id="844ca-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="844ca-106">Seda laiendati rakenduste Microsoft Dynamics AX 2012 R3 ja Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 kumulatiivses värskenduses 8 (CU8).</span><span class="sxs-lookup"><span data-stu-id="844ca-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="844ca-107">Lahendaja strateegia mõiste hõlmab nüüd järgmisi strateegiaid.</span><span class="sxs-lookup"><span data-stu-id="844ca-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="844ca-108">Vaikimisi</span><span class="sxs-lookup"><span data-stu-id="844ca-108">Default</span></span>
- <span data-ttu-id="844ca-109">Minimaalsed domeenid kõigepealt</span><span class="sxs-lookup"><span data-stu-id="844ca-109">Minimal domains first</span></span>
- <span data-ttu-id="844ca-110">Ülevalt alla</span><span class="sxs-lookup"><span data-stu-id="844ca-110">Top-down</span></span>
- <span data-ttu-id="844ca-111">Z3</span><span class="sxs-lookup"><span data-stu-id="844ca-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="844ca-112">Lahendaja strateegia</span><span class="sxs-lookup"><span data-stu-id="844ca-112">Solver strategy</span></span> 

<span data-ttu-id="844ca-113">Toote konfiguratsioonimudeli on [piirangu rahulolu probleem](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span><span class="sxs-lookup"><span data-stu-id="844ca-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="844ca-114">Microsoft Solver Foundation (MSF) pakub toote konfiguratsioonimudelite kaudu kasutatavate piirangu rahuldamise probleemide lahendamiseks kahte tüüpi lahendaja strateegiaid.</span><span class="sxs-lookup"><span data-stu-id="844ca-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="844ca-115">Need lahendaja strateegiad sõltuvad [heuristikast](https://techterms.com/definition/heuristic), mida kasutatakse probleemi lahendamisel piirandu rahuldamise probleemide muutujate järjekorra kindlaks määramiseks.</span><span class="sxs-lookup"><span data-stu-id="844ca-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="844ca-116">Heuristika võib oluliselt mõjutada probleemi või probleemide klassi lahendamise jõudlust.</span><span class="sxs-lookup"><span data-stu-id="844ca-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="844ca-117">Rakenduses Finance and Operations määrab toote konfiguratsioonimudelite lahendaja strateegia selle, millist lahendajat heuristikas kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="844ca-117">In Finance and Operations, the solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="844ca-118">Strateegiad **Vaikimisi**, **Minimaalsed domeenid kõigepealt** ja **Ülevalt alla** kasutavad kahte MSF-i lahendajat, kusjuures strateegia **Z3** kasutab lahendajat Z3.</span><span class="sxs-lookup"><span data-stu-id="844ca-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="844ca-119">Tõelised kliendijuurutamisuuringud on näidanud, et toote konfiguratsioonimudeli lahendaja strateegiate muutmine võib vähendada reageerimisaega minutitelt millisekunditele.</span><span class="sxs-lookup"><span data-stu-id="844ca-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="844ca-120">Seetõttu on tasub toote konfiguratsioonimudeli tõhusaimi strateegia leidmiseks proovida eri lahendaja strateegiaid.</span><span class="sxs-lookup"><span data-stu-id="844ca-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="844ca-121">Lahendaja strateegia sätete muutmine</span><span class="sxs-lookup"><span data-stu-id="844ca-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="844ca-122">Lahendaja strateegia muutmiseks tehke lehe **Toote konfiguratsioonimudelid** toimingupaanil valik **Mudeli atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="844ca-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="844ca-123">Seejärel valige dialoogiboksis **Mudeli üksikasjade redigeerimine** lahendaja strateegia.</span><span class="sxs-lookup"><span data-stu-id="844ca-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="844ca-124">[![Lahendaja strateegia muutmine](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="844ca-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="844ca-125">Praegu ei ole olemas loogikat, mis tuvastaks automaatselt, milline lahendaja strateegia on piirangupõhiste toote konfiguratsioonimudelite jaoks kõige tõhusam.</span><span class="sxs-lookup"><span data-stu-id="844ca-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="844ca-126">Seetõttu tuleb proovida lahendaja strateegiaid ükshaaval.</span><span class="sxs-lookup"><span data-stu-id="844ca-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="844ca-127">Järgmine tabel pakub soovitusi lahendaja strateegia kasutamiseks eri stsenaariumide korral.</span><span class="sxs-lookup"><span data-stu-id="844ca-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="844ca-128">Lahendaja strateegia</span><span class="sxs-lookup"><span data-stu-id="844ca-128">Solver strategy</span></span>      | <span data-ttu-id="844ca-129">Stsenaarium, milles strateegiat saab kasutada</span><span class="sxs-lookup"><span data-stu-id="844ca-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="844ca-130">Vaikimisi</span><span class="sxs-lookup"><span data-stu-id="844ca-130">Default</span></span>              | <span data-ttu-id="844ca-131">Strateegia **Vaikimisi** on optimeeritud lahendama mudeleid, mis sõltuvad tabeli piirangutest.</span><span class="sxs-lookup"><span data-stu-id="844ca-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="844ca-132">Kliendijuurutamisuuringud on näidanud, et see strateegia on kõige tõhusam stsenaariumides, kus tabeli piiranguid kasutatakse ulatuslikult.</span><span class="sxs-lookup"><span data-stu-id="844ca-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="844ca-133">Minimaalne domeen kõigepealt</span><span class="sxs-lookup"><span data-stu-id="844ca-133">Minimal domain first</span></span> | <span data-ttu-id="844ca-134">Strateegiad **Minimaalne domeen kõigepealt** ja **Ülalt alla** on omavahel tihedalt seotud.</span><span class="sxs-lookup"><span data-stu-id="844ca-134">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="844ca-135">Kliendijuurutamisuuringud on näidanud, et CUB-s kasutusele võetud strateegia **Ülalt alla** on strateegiast **Minimaalne domeen kõigepealt** tõhusam.</span><span class="sxs-lookup"><span data-stu-id="844ca-135">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="844ca-136">Strateegiat **Minimaalne domeen kõigepealt** hoitakse tootes tagasiühilduvuseks.</span><span class="sxs-lookup"><span data-stu-id="844ca-136">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="844ca-137">Mõlemad lahendaja strateegiad on tõhusamad selliste mudelite lahendamises, mis sisaldavad mitut aritmeetilist avaldist, kus ei kasutata tabelipiiranguid.</span><span class="sxs-lookup"><span data-stu-id="844ca-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="844ca-138">Mõnel juhul on aga strateegia **Vaikimisi** neist kahest tõhusam.</span><span class="sxs-lookup"><span data-stu-id="844ca-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="844ca-139">Seetõttu on oluline proovida kõiki strateegiaid.</span><span class="sxs-lookup"><span data-stu-id="844ca-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="844ca-140">Ülevalt alla</span><span class="sxs-lookup"><span data-stu-id="844ca-140">Top-down</span></span>             | <span data-ttu-id="844ca-141">Strateegiad **Minimaalne domeen kõigepealt** ja **Ülalt alla** on omavahel tihedalt seotud.</span><span class="sxs-lookup"><span data-stu-id="844ca-141">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="844ca-142">Kliendijuurutamisuuringud on näidanud, et CUB-s kasutusele võetud strateegia **Ülalt alla** on strateegiast **Minimaalne domeen kõigepealt** tõhusam.</span><span class="sxs-lookup"><span data-stu-id="844ca-142">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="844ca-143">Strateegiat **Minimaalne domeen kõigepealt** hoitakse tootes tagasiühilduvuseks.</span><span class="sxs-lookup"><span data-stu-id="844ca-143">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="844ca-144">Mõlemad lahendaja strateegiad on tõhusamad selliste mudelite lahendamises, mis sisaldavad mitut aritmeetilist avaldist, kus ei kasutata tabelipiiranguid.</span><span class="sxs-lookup"><span data-stu-id="844ca-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="844ca-145">Mõnel juhul on aga strateegia **Vaikimisi** neist kahest tõhusam.</span><span class="sxs-lookup"><span data-stu-id="844ca-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="844ca-146">Seetõttu on oluline proovida kõiki strateegiaid.</span><span class="sxs-lookup"><span data-stu-id="844ca-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="844ca-147">Z3</span><span class="sxs-lookup"><span data-stu-id="844ca-147">Z3</span></span>                   | <span data-ttu-id="844ca-148">Strateegiat **Z3** soovitame kasutada lahendaja vaikestrateegiana.</span><span class="sxs-lookup"><span data-stu-id="844ca-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="844ca-149">Kui muretsete jõudluse ja mastaabitavuse pärast, saate hinnata teisi strateegiaid.</span><span class="sxs-lookup"><span data-stu-id="844ca-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="844ca-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="844ca-150">Additional resources</span></span>

[<span data-ttu-id="844ca-151">Toote konfiguratsioonimudeli koostamine</span><span class="sxs-lookup"><span data-stu-id="844ca-151">Build product configuration model</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="844ca-152">Heuristika</span><span class="sxs-lookup"><span data-stu-id="844ca-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="844ca-153">Piirangu rahuldamise probleem</span><span class="sxs-lookup"><span data-stu-id="844ca-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)

