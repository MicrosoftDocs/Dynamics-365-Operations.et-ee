---
title: Tööajaarvestuse palgaarvestuse protsessi lubamine
description: Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c855f388e8afbd12559cd633cfcdebc7740bce6a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977784"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="6d1cf-103">Tööajaarvestuse palgaarvestuse protsessi lubamine</span><span class="sxs-lookup"><span data-stu-id="6d1cf-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d1cf-104">Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="6d1cf-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="6d1cf-106">Seostatud tasumääraga tasutüübi loomine</span><span class="sxs-lookup"><span data-stu-id="6d1cf-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="6d1cf-107">Tööajaarvestus > Seadistus > Palk > Tasutüübid</span><span class="sxs-lookup"><span data-stu-id="6d1cf-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="6d1cf-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-108">Click New.</span></span>
3. <span data-ttu-id="6d1cf-109">Sisestage väärtus väljale Tasutüüp.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="6d1cf-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6d1cf-111">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-111">Click Save.</span></span>
6. <span data-ttu-id="6d1cf-112">Klõpsake valikut Määrad.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-112">Click Rates.</span></span>
    * <span data-ttu-id="6d1cf-113">Tasutüüpide määrad seatakse konkreetseteks ajaperioodideks ja töötajatele saab luua eri tasumäärasid.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="6d1cf-114">Tasumäärade loomine tööajaarvestuse järgi ei ole alati vajalik.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="6d1cf-115">See teave võib juba olemas olla palgaarvestussüsteemis, kus palku luuakse.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="6d1cf-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-116">Click New.</span></span>
8. <span data-ttu-id="6d1cf-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="6d1cf-118">Sisestage arv väljale Määr.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="6d1cf-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="6d1cf-120">Tasuleppe loomine</span><span class="sxs-lookup"><span data-stu-id="6d1cf-120">Create a pay agreement</span></span>
1. <span data-ttu-id="6d1cf-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-121">Close the page.</span></span>
2. <span data-ttu-id="6d1cf-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-122">Close the page.</span></span>
3. <span data-ttu-id="6d1cf-123">Avage Tasulepped.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="6d1cf-124">Tööajaarvestus > Seadistus > Tasulepped</span><span class="sxs-lookup"><span data-stu-id="6d1cf-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="6d1cf-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-125">Click New.</span></span>
5. <span data-ttu-id="6d1cf-126">Sisestage väärtus väljale Tasulepe.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="6d1cf-127">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="6d1cf-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-128">Click Save.</span></span>
8. <span data-ttu-id="6d1cf-129">Klõpsake valikut Lepingu read.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="6d1cf-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-130">Click New.</span></span>
10. <span data-ttu-id="6d1cf-131">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="6d1cf-132">Sisestage või valige väärtus väljal Reeglite tüüp.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="6d1cf-133">Sisestage või valige väärtus väljal Tasutüüp.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="6d1cf-134">Kellaaja registreerimisega töötaja tasuleppe seadistamine</span><span class="sxs-lookup"><span data-stu-id="6d1cf-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="6d1cf-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-135">Close the page.</span></span>
2. <span data-ttu-id="6d1cf-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-136">Close the page.</span></span>
3. <span data-ttu-id="6d1cf-137">Avage jaotis Ajalise registreerimise töötajad.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="6d1cf-138">Tööajaarvestus > Seadistus > Ajalise registreerimise töötajad</span><span class="sxs-lookup"><span data-stu-id="6d1cf-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="6d1cf-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6d1cf-140">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="6d1cf-141">Laiendage jaotist Ajaline registreerimine.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="6d1cf-142">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-142">Click Edit.</span></span>
8. <span data-ttu-id="6d1cf-143">Sisestage või valige väärtus väljal Tasulepe.</span><span class="sxs-lookup"><span data-stu-id="6d1cf-143">In the Pay agreement field, enter or select a value.</span></span>

