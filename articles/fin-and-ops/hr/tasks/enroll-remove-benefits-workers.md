---
title: Töötajate soodustuste registreerimine ja eemaldamine
description: See protseduur näitab, kuidas ühe töötaja saab registreerida vähemalt ühe soodustuse saajaks ning kuidas mitu töötajat saab soodustuse saajaks registreerida.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32f0e641f5e6824df89112aa5ea21dc3a708efa0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "341852"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="234dc-103">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="234dc-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="234dc-104">See protseduur näitab, kuidas ühe töötaja saab registreerida vähemalt ühe soodustuse saajaks ning kuidas mitu töötajat saab soodustuse saajaks registreerida.</span><span class="sxs-lookup"><span data-stu-id="234dc-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="234dc-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="234dc-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="234dc-106">Ühe töötaja registreerimine soodustustes</span><span class="sxs-lookup"><span data-stu-id="234dc-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="234dc-107">Avage Personaliarvestus > Töötajad > Töötajad</span><span class="sxs-lookup"><span data-stu-id="234dc-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="234dc-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="234dc-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="234dc-109">Klõpsake suvandit Soodustused.</span><span class="sxs-lookup"><span data-stu-id="234dc-109">Click Benefits.</span></span>
4. <span data-ttu-id="234dc-110">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="234dc-110">Click New.</span></span>
5. <span data-ttu-id="234dc-111">Valige või sisestage väärtus väljal Soodustus.</span><span class="sxs-lookup"><span data-stu-id="234dc-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="234dc-112">Sisestage kuupäev ja kellaaeg väljale Kehtivuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="234dc-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="234dc-113">Sisestage kuupäev ja kellaaeg väljale Kehtivuse lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="234dc-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="234dc-114">Laiendage jaotist Kasusaajad, kui soodustusele on vaja kasusaajaid lisada.</span><span class="sxs-lookup"><span data-stu-id="234dc-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="234dc-115">Saate lisada sellel lehel ka sõltuvaid üksusi, kui seda on soodustuse puhul vaja.</span><span class="sxs-lookup"><span data-stu-id="234dc-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="234dc-116">Samuti saab sellel lehel redigeerida soodustuse saamiseks registreerimise üksikasju või kustutada registreerimise.</span><span class="sxs-lookup"><span data-stu-id="234dc-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="234dc-117">Kui olete soodustuse registreerimise muudatuste tegemise lõpetanud, sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="234dc-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="234dc-118">Mitme töötaja registreerimine soodustuses</span><span class="sxs-lookup"><span data-stu-id="234dc-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="234dc-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="234dc-119">Close the page.</span></span>
2. <span data-ttu-id="234dc-120">Avage Personaliarvestus > Töötajad > Töötajad</span><span class="sxs-lookup"><span data-stu-id="234dc-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="234dc-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="234dc-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="234dc-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="234dc-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="234dc-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="234dc-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="234dc-124">Klõpsake valikut Soodustuste registreerimine.</span><span class="sxs-lookup"><span data-stu-id="234dc-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="234dc-125">Valige või sisestage väärtus väljal Soodustus.</span><span class="sxs-lookup"><span data-stu-id="234dc-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="234dc-126">Sisestage kuupäev ja kellaaeg väljale Kehtivuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="234dc-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="234dc-127">Sisestage kuupäev ja kellaaeg väljale Kehtivuse lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="234dc-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="234dc-128">Klõpsake valikut Registreeri.</span><span class="sxs-lookup"><span data-stu-id="234dc-128">Click Enroll.</span></span>
11. <span data-ttu-id="234dc-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="234dc-129">Close the page.</span></span>
12. <span data-ttu-id="234dc-130">Avage Personaliarvestus > Soodustused > Registreerimine > Soodustuse registreerimise tulemused</span><span class="sxs-lookup"><span data-stu-id="234dc-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="234dc-131">Otsige üles vajalik soodustuse tulemuste kirje.</span><span class="sxs-lookup"><span data-stu-id="234dc-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="234dc-132">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="234dc-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="234dc-133">Sellel lehel saate vaadata, millised töötajad on soodustuse saamiseks registreeritud ja millised mitte.</span><span class="sxs-lookup"><span data-stu-id="234dc-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

