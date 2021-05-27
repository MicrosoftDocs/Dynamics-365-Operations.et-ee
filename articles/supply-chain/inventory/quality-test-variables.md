---
title: Kvaliteedijuhtimise testi muutujad
description: See teema kirjeldab, kuidas luua testi muutujaid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021704"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="c2e1c-103">Kvaliteedijuhtimise testi muutujad</span><span class="sxs-lookup"><span data-stu-id="c2e1c-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2e1c-104">See teema kirjeldab, kuidas luua testi muutujaid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="c2e1c-105">Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel **Testid**.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="c2e1c-106">(Kvalitatiivsete testide puhul on **Tüüp** väljal lehel **Testid** määratud *Suvand*.)</span><span class="sxs-lookup"><span data-stu-id="c2e1c-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="c2e1c-107">Kvalitatiivse testiga seotud testmuutuja võimalike tulemuste seadistamiseks, muutmiseks ja vaatamiseks kasutage lehte **Testi muutujad**.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="c2e1c-108">Iga tulemuse jaoks määrate te väljundolekuks *Läbitud* või *Nurjunud*, mis näitab, kas test on läbitud või nurjunud, kui see tulemus on testi tulemusena valitud.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="c2e1c-109">Kasutage lehte **Testgrupid** katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivse katse väljundile.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="c2e1c-110">Iga testmuutuja jaoks soovitame määratleda vähemalt kaks tulemust: ühe, mille väljundolek on *Läbitud* ja teine, mille väljundolek on *Nurjunud*.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="c2e1c-111">Muutujate ja väljundite koguarvu, mida saab määratleda, ei ole piiratud.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="c2e1c-112">Lisaks võivad mitmed testid tulemuste registreerimiseks kasutada samu testimuutujaid.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="c2e1c-113">Testmuutujate näited</span><span class="sxs-lookup"><span data-stu-id="c2e1c-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="c2e1c-114">Näide 1</span><span class="sxs-lookup"><span data-stu-id="c2e1c-114">Example 1</span></span>

<span data-ttu-id="c2e1c-115">Tootmisettevõte sooritab kaks katset toodetud materjalidega.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="c2e1c-116">Ühes testis seostatakse pH-tase värviribaga.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="c2e1c-117">Vastuvõetav pH-tase on heledamates värvides ja vastuvõetamatud pH-tasemed on tumedates värvides.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="c2e1c-118">Teises testis viiakse läbi mitu visuaalset kontrolli ja kvaliteettöötajad kasutavad oma hinnangut, et teha kindlaks, kas kaup läbib või nurjub visuaalse kontrolli.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="c2e1c-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="c2e1c-119">Example 2</span></span>

<span data-ttu-id="c2e1c-120">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="c2e1c-121">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-121">This inspection test has several variables.</span></span> <span data-ttu-id="c2e1c-122">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="c2e1c-123">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="c2e1c-124">Uue testmuutuja loomine</span><span class="sxs-lookup"><span data-stu-id="c2e1c-124">Create a test variable</span></span>

<span data-ttu-id="c2e1c-125">Testmuutuja loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="c2e1c-126">Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Testmuutujad**.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="c2e1c-127">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c2e1c-128">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c2e1c-129">**Muutuja** – Sisestage muutuja kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="c2e1c-130">**Kirjeldus** – Sisestage muutuja detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="c2e1c-131">Kui uus rida on endiselt valitud, valige tegevuspaanil **Väljundid**.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="c2e1c-132">Ruudustiku rea lisamiseks valige **Testmuutujate väljundid** lehe tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c2e1c-133">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c2e1c-134">**Väljund** – Sisestage väljundi kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="c2e1c-135">**Kirjeldus** – Sisestage väljundi detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="c2e1c-136">**Väljundi olek** – Iga tulemuse jaoks määrate te väljundolekuks *Läbitud* või *Nurjunud*, mis näitab, kas test on läbitud või nurjunud, kui see tulemus on testi tulemusena valitud.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="c2e1c-137">Korrake eelmist sammu iga täiendava väljundi puhul.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="c2e1c-138">Veenduge, et vähemalt ühel väljundil on väljundolek *Läbitud* ja vähemalt ühel on väljundolek *Nurjunud*.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="c2e1c-139">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="c2e1c-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2e1c-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c2e1c-140">Additional resources</span></span>

- [<span data-ttu-id="c2e1c-141">Kvaliteedijuhtimise testvahendid</span><span class="sxs-lookup"><span data-stu-id="c2e1c-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="c2e1c-142">Kvaliteedijuhtimise testid</span><span class="sxs-lookup"><span data-stu-id="c2e1c-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="c2e1c-143">Kvaliteedijuhtimise testgrupid</span><span class="sxs-lookup"><span data-stu-id="c2e1c-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
