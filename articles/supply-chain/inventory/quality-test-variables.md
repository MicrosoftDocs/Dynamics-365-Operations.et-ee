---
title: Kvaliteedijuhtimise testi muutujad
description: See teema kirjeldab, kuidas luua testi muutujaid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956624"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="b97a3-103">Kvaliteedijuhtimise testi muutujad</span><span class="sxs-lookup"><span data-stu-id="b97a3-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b97a3-104">See teema kirjeldab, kuidas luua testi muutujaid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b97a3-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b97a3-105">Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel **Testid**.</span><span class="sxs-lookup"><span data-stu-id="b97a3-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="b97a3-106">(Kvalitatiivsete testide puhul on **Tüüp** väljal lehel **Testid** määratud *Suvand*.)</span><span class="sxs-lookup"><span data-stu-id="b97a3-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="b97a3-107">Kvalitatiivse testiga seotud testmuutuja võimalike tulemuste seadistamiseks, muutmiseks ja vaatamiseks kasutage lehte **Testi muutujad**.</span><span class="sxs-lookup"><span data-stu-id="b97a3-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="b97a3-108">Iga tulemuse jaoks määrate te väljundolekuks *Läbitud* või *Nurjunud*, mis näitab, kas test on läbitud või nurjunud, kui see tulemus on testi tulemusena valitud.</span><span class="sxs-lookup"><span data-stu-id="b97a3-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="b97a3-109">Kasutage lehte **Testgrupid** katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivse katse väljundile.</span><span class="sxs-lookup"><span data-stu-id="b97a3-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="b97a3-110">Iga testmuutuja jaoks soovitame määratleda vähemalt kaks tulemust: ühe, mille väljundolek on *Läbitud* ja teine, mille väljundolek on *Nurjunud*.</span><span class="sxs-lookup"><span data-stu-id="b97a3-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="b97a3-111">Muutujate ja väljundite koguarvu, mida saab määratleda, ei ole piiratud.</span><span class="sxs-lookup"><span data-stu-id="b97a3-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="b97a3-112">Lisaks võivad mitmed testid tulemuste registreerimiseks kasutada samu testimuutujaid.</span><span class="sxs-lookup"><span data-stu-id="b97a3-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="b97a3-113">Testmuutujate näited</span><span class="sxs-lookup"><span data-stu-id="b97a3-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="b97a3-114">Näide 1</span><span class="sxs-lookup"><span data-stu-id="b97a3-114">Example 1</span></span>

<span data-ttu-id="b97a3-115">Tootmisettevõte sooritab kaks katset toodetud materjalidega.</span><span class="sxs-lookup"><span data-stu-id="b97a3-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="b97a3-116">Ühes testis seostatakse pH-tase värviribaga.</span><span class="sxs-lookup"><span data-stu-id="b97a3-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="b97a3-117">Vastuvõetav pH-tase on heledamates värvides ja vastuvõetamatud pH-tasemed on tumedates värvides.</span><span class="sxs-lookup"><span data-stu-id="b97a3-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="b97a3-118">Teises testis viiakse läbi mitu visuaalset kontrolli ja kvaliteettöötajad kasutavad oma hinnangut, et teha kindlaks, kas kaup läbib või nurjub visuaalse kontrolli.</span><span class="sxs-lookup"><span data-stu-id="b97a3-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="b97a3-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="b97a3-119">Example 2</span></span>

<span data-ttu-id="b97a3-120">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="b97a3-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b97a3-121">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="b97a3-121">This inspection test has several variables.</span></span> <span data-ttu-id="b97a3-122">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="b97a3-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="b97a3-123">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="b97a3-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="b97a3-124">Uue testmuutuja loomine</span><span class="sxs-lookup"><span data-stu-id="b97a3-124">Create a test variable</span></span>

<span data-ttu-id="b97a3-125">Testmuutuja loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b97a3-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="b97a3-126">Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Testmuutujad**.</span><span class="sxs-lookup"><span data-stu-id="b97a3-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="b97a3-127">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="b97a3-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b97a3-128">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="b97a3-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b97a3-129">**Muutuja** – Sisestage muutuja kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="b97a3-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="b97a3-130">**Kirjeldus** – Sisestage muutuja detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b97a3-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="b97a3-131">Kui uus rida on endiselt valitud, valige tegevuspaanil **Väljundid**.</span><span class="sxs-lookup"><span data-stu-id="b97a3-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="b97a3-132">Ruudustiku rea lisamiseks valige **Testmuutujate väljundid** lehe tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b97a3-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b97a3-133">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="b97a3-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b97a3-134">**Väljund** – Sisestage väljundi kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="b97a3-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="b97a3-135">**Kirjeldus** – Sisestage väljundi detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b97a3-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="b97a3-136">**Väljundi olek** – Iga tulemuse jaoks määrate te väljundolekuks *Läbitud* või *Nurjunud*, mis näitab, kas test on läbitud või nurjunud, kui see tulemus on testi tulemusena valitud.</span><span class="sxs-lookup"><span data-stu-id="b97a3-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="b97a3-137">Korrake eelmist sammu iga täiendava väljundi puhul.</span><span class="sxs-lookup"><span data-stu-id="b97a3-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="b97a3-138">Veenduge, et vähemalt ühel väljundil on väljundolek *Läbitud* ja vähemalt ühel on väljundolek *Nurjunud*.</span><span class="sxs-lookup"><span data-stu-id="b97a3-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="b97a3-139">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="b97a3-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b97a3-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b97a3-140">Additional resources</span></span>

- [<span data-ttu-id="b97a3-141">Kvaliteedijuhtimise testvahendid</span><span class="sxs-lookup"><span data-stu-id="b97a3-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="b97a3-142">Kvaliteedijuhtimise testid</span><span class="sxs-lookup"><span data-stu-id="b97a3-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="b97a3-143">Kvaliteedijuhtimise testgrupid</span><span class="sxs-lookup"><span data-stu-id="b97a3-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
