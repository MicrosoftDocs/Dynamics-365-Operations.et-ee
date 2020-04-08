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
ms.openlocfilehash: 2df4695b796b4e96e01fe5dac538b344cb76b910
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146717"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="b67dd-103">Tööajaarvestuse palgaarvestuse protsessi lubamine</span><span class="sxs-lookup"><span data-stu-id="b67dd-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b67dd-104">Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="b67dd-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="b67dd-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b67dd-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="b67dd-106">Seostatud tasumääraga tasutüübi loomine</span><span class="sxs-lookup"><span data-stu-id="b67dd-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="b67dd-107">Tööajaarvestus > Seadistus > Palk > Tasutüübid</span><span class="sxs-lookup"><span data-stu-id="b67dd-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="b67dd-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b67dd-108">Click New.</span></span>
3. <span data-ttu-id="b67dd-109">Sisestage väärtus väljale Tasutüüp.</span><span class="sxs-lookup"><span data-stu-id="b67dd-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="b67dd-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b67dd-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b67dd-111">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b67dd-111">Click Save.</span></span>
6. <span data-ttu-id="b67dd-112">Klõpsake valikut Määrad.</span><span class="sxs-lookup"><span data-stu-id="b67dd-112">Click Rates.</span></span>
    * <span data-ttu-id="b67dd-113">Tasutüüpide määrad seatakse konkreetseteks ajaperioodideks ja töötajatele saab luua eri tasumäärasid.</span><span class="sxs-lookup"><span data-stu-id="b67dd-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="b67dd-114">Tasumäärade loomine tööajaarvestuse järgi ei ole alati vajalik.</span><span class="sxs-lookup"><span data-stu-id="b67dd-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="b67dd-115">See teave võib juba olemas olla palgaarvestussüsteemis, kus palku luuakse.</span><span class="sxs-lookup"><span data-stu-id="b67dd-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="b67dd-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b67dd-116">Click New.</span></span>
8. <span data-ttu-id="b67dd-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b67dd-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b67dd-118">Sisestage arv väljale Määr.</span><span class="sxs-lookup"><span data-stu-id="b67dd-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="b67dd-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b67dd-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="b67dd-120">Tasuleppe loomine</span><span class="sxs-lookup"><span data-stu-id="b67dd-120">Create a pay agreement</span></span>
1. <span data-ttu-id="b67dd-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b67dd-121">Close the page.</span></span>
2. <span data-ttu-id="b67dd-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b67dd-122">Close the page.</span></span>
3. <span data-ttu-id="b67dd-123">Avage Tasulepped.</span><span class="sxs-lookup"><span data-stu-id="b67dd-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="b67dd-124">Tööajaarvestus > Seadistus > Tasulepped</span><span class="sxs-lookup"><span data-stu-id="b67dd-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="b67dd-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b67dd-125">Click New.</span></span>
5. <span data-ttu-id="b67dd-126">Sisestage väärtus väljale Tasulepe.</span><span class="sxs-lookup"><span data-stu-id="b67dd-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="b67dd-127">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b67dd-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="b67dd-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b67dd-128">Click Save.</span></span>
8. <span data-ttu-id="b67dd-129">Klõpsake valikut Lepingu read.</span><span class="sxs-lookup"><span data-stu-id="b67dd-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="b67dd-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b67dd-130">Click New.</span></span>
10. <span data-ttu-id="b67dd-131">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b67dd-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b67dd-132">Sisestage või valige väärtus väljal Reeglite tüüp.</span><span class="sxs-lookup"><span data-stu-id="b67dd-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="b67dd-133">Sisestage või valige väärtus väljal Tasutüüp.</span><span class="sxs-lookup"><span data-stu-id="b67dd-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="b67dd-134">Kellaaja registreerimisega töötaja tasuleppe seadistamine</span><span class="sxs-lookup"><span data-stu-id="b67dd-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="b67dd-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b67dd-135">Close the page.</span></span>
2. <span data-ttu-id="b67dd-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b67dd-136">Close the page.</span></span>
3. <span data-ttu-id="b67dd-137">Avage jaotis Ajalise registreerimise töötajad.</span><span class="sxs-lookup"><span data-stu-id="b67dd-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="b67dd-138">Tööajaarvestus > Seadistus > Ajalise registreerimise töötajad</span><span class="sxs-lookup"><span data-stu-id="b67dd-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="b67dd-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b67dd-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b67dd-140">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="b67dd-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="b67dd-141">Laiendage jaotist Ajaline registreerimine.</span><span class="sxs-lookup"><span data-stu-id="b67dd-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="b67dd-142">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="b67dd-142">Click Edit.</span></span>
8. <span data-ttu-id="b67dd-143">Sisestage või valige väärtus väljal Tasulepe.</span><span class="sxs-lookup"><span data-stu-id="b67dd-143">In the Pay agreement field, enter or select a value.</span></span>

