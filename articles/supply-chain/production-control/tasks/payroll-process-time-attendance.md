---
title: Tööajaarvestuse palgaarvestuse protsessi lubamine
description: Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a52ad77d3f03898d26c225900fe79ca30493a67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843525"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="e05e6-103">Tööajaarvestuse palgaarvestuse protsessi lubamine</span><span class="sxs-lookup"><span data-stu-id="e05e6-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e05e6-104">Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="e05e6-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="e05e6-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e05e6-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="e05e6-106">Seostatud tasumääraga tasutüübi loomine</span><span class="sxs-lookup"><span data-stu-id="e05e6-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="e05e6-107">Tööajaarvestus > Seadistus > Palk > Tasutüübid</span><span class="sxs-lookup"><span data-stu-id="e05e6-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="e05e6-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e05e6-108">Click New.</span></span>
3. <span data-ttu-id="e05e6-109">Sisestage väärtus väljale Tasutüüp.</span><span class="sxs-lookup"><span data-stu-id="e05e6-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="e05e6-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e05e6-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e05e6-111">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e05e6-111">Click Save.</span></span>
6. <span data-ttu-id="e05e6-112">Klõpsake valikut Määrad.</span><span class="sxs-lookup"><span data-stu-id="e05e6-112">Click Rates.</span></span>
    * <span data-ttu-id="e05e6-113">Tasutüüpide määrad seatakse konkreetseteks ajaperioodideks ja töötajatele saab luua eri tasumäärasid.</span><span class="sxs-lookup"><span data-stu-id="e05e6-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="e05e6-114">Tasumäärade loomine tööajaarvestuse järgi ei ole alati vajalik.</span><span class="sxs-lookup"><span data-stu-id="e05e6-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="e05e6-115">See teave võib juba olemas olla palgaarvestussüsteemis, kus palku luuakse.</span><span class="sxs-lookup"><span data-stu-id="e05e6-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="e05e6-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e05e6-116">Click New.</span></span>
8. <span data-ttu-id="e05e6-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e05e6-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e05e6-118">Sisestage arv väljale Määr.</span><span class="sxs-lookup"><span data-stu-id="e05e6-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="e05e6-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e05e6-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="e05e6-120">Tasuleppe loomine</span><span class="sxs-lookup"><span data-stu-id="e05e6-120">Create a pay agreement</span></span>
1. <span data-ttu-id="e05e6-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e05e6-121">Close the page.</span></span>
2. <span data-ttu-id="e05e6-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e05e6-122">Close the page.</span></span>
3. <span data-ttu-id="e05e6-123">Avage Tasulepped.</span><span class="sxs-lookup"><span data-stu-id="e05e6-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="e05e6-124">Tööajaarvestus > Seadistus > Tasulepped</span><span class="sxs-lookup"><span data-stu-id="e05e6-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="e05e6-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e05e6-125">Click New.</span></span>
5. <span data-ttu-id="e05e6-126">Sisestage väärtus väljale Tasulepe.</span><span class="sxs-lookup"><span data-stu-id="e05e6-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="e05e6-127">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e05e6-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="e05e6-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e05e6-128">Click Save.</span></span>
8. <span data-ttu-id="e05e6-129">Klõpsake valikut Lepingu read.</span><span class="sxs-lookup"><span data-stu-id="e05e6-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="e05e6-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e05e6-130">Click New.</span></span>
10. <span data-ttu-id="e05e6-131">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e05e6-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="e05e6-132">Sisestage või valige väärtus väljal Reeglite tüüp.</span><span class="sxs-lookup"><span data-stu-id="e05e6-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="e05e6-133">Sisestage või valige väärtus väljal Tasutüüp.</span><span class="sxs-lookup"><span data-stu-id="e05e6-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="e05e6-134">Kellaaja registreerimisega töötaja tasuleppe seadistamine</span><span class="sxs-lookup"><span data-stu-id="e05e6-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="e05e6-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e05e6-135">Close the page.</span></span>
2. <span data-ttu-id="e05e6-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e05e6-136">Close the page.</span></span>
3. <span data-ttu-id="e05e6-137">Avage jaotis Ajalise registreerimise töötajad.</span><span class="sxs-lookup"><span data-stu-id="e05e6-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="e05e6-138">Tööajaarvestus > Seadistus > Ajalise registreerimise töötajad</span><span class="sxs-lookup"><span data-stu-id="e05e6-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="e05e6-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e05e6-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e05e6-140">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="e05e6-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="e05e6-141">Laiendage jaotist Ajaline registreerimine.</span><span class="sxs-lookup"><span data-stu-id="e05e6-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="e05e6-142">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e05e6-142">Click Edit.</span></span>
8. <span data-ttu-id="e05e6-143">Sisestage või valige väärtus väljal Tasulepe.</span><span class="sxs-lookup"><span data-stu-id="e05e6-143">In the Pay agreement field, enter or select a value.</span></span>

