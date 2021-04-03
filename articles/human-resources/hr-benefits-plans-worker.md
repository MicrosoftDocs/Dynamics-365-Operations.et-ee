---
title: Töötaja soodustuse plaanide loomine
description: Saate luua rakenduses Microsoft Dynamics 365 Human Resources töötaja soodustuse plaanid, et valida töövõtjate jaoks soodustuse plaanid ja kinnitada soodustuse plaani valikud.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ac357bbef4bf84b9eaf153834bc7a609240c45e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464222"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="83d83-103">Töötaja soodustuse plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="83d83-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="83d83-104">Saate luua rakenduses Microsoft Dynamics 365 Human Resources töötaja soodustuse plaanid, et valida töövõtjate jaoks soodustuse plaanid ja kinnitada soodustuse plaani valikud.</span><span class="sxs-lookup"><span data-stu-id="83d83-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="83d83-105">Tavaliselt valivad töötajad soodustuse plaanid ise, kasutades töötaja iseteenindust, ja seejärel kinnitab soodustuste haldur valikud.</span><span class="sxs-lookup"><span data-stu-id="83d83-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="83d83-106">Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Töötaja soodustuse plaanid**.</span><span class="sxs-lookup"><span data-stu-id="83d83-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="83d83-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="83d83-107">Select **New**.</span></span>

3. <span data-ttu-id="83d83-108">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="83d83-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="83d83-109">Väli</span><span class="sxs-lookup"><span data-stu-id="83d83-109">Field</span></span> | <span data-ttu-id="83d83-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="83d83-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="83d83-111">Periood</span><span class="sxs-lookup"><span data-stu-id="83d83-111">Period</span></span> | <span data-ttu-id="83d83-112">Määrab soodustuste perioodi, mida kasutatakse kiirkaardil Plaanid plaanide filtreerimiseks. Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="83d83-113">Näiteks valige periood, mille lõite nimega 2015, et kinnitada kõik soodustuse registreerimise valikud 2015 jaoks.</span><span class="sxs-lookup"><span data-stu-id="83d83-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="83d83-114">Töötaja</span><span class="sxs-lookup"><span data-stu-id="83d83-114">Worker</span></span> | <span data-ttu-id="83d83-115">Määrab töötaja, keda kasutatakse kiirkaardil Plaanid plaanide filtreerimiseks. Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="83d83-116">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="83d83-116">Legal entity</span></span> | <span data-ttu-id="83d83-117">Määrab juriidilise isiku, keda kasutatakse kiirkaardil Plaanid plaanide filtreerimiseks. Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="83d83-118">Kindlustussuvand</span><span class="sxs-lookup"><span data-stu-id="83d83-118">Coverage option</span></span> | <span data-ttu-id="83d83-119">Määrab katvuse valiku, mida kasutatakse kiirkaardil Plaanid plaanide filtreerimiseks. Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="83d83-120">Vaikimisi</span><span class="sxs-lookup"><span data-stu-id="83d83-120">Default</span></span> | <span data-ttu-id="83d83-121">Filtreerib soodustuse plaane selle alusel, kas need on vaikeplaanid.</span><span class="sxs-lookup"><span data-stu-id="83d83-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="83d83-122">Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="83d83-123">Olek</span><span class="sxs-lookup"><span data-stu-id="83d83-123">Status</span></span> | <span data-ttu-id="83d83-124">Filtreerib soodustuse plaanid nende oleku põhjal.</span><span class="sxs-lookup"><span data-stu-id="83d83-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="83d83-125">Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="83d83-126">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="83d83-126">Confirmation</span></span> | <span data-ttu-id="83d83-127">Määrab kinnitamise oleku, mida kasutatakse kiirkaardil Plaanid plaanide filtreerimiseks. Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="83d83-128">Tühistamine</span><span class="sxs-lookup"><span data-stu-id="83d83-128">Cancellation</span></span> | <span data-ttu-id="83d83-129">Määrab tühistamise oleku, mida kasutatakse kiirkaardil Plaanid plaanide filtreerimiseks. Filtreerige plaanid, et aidata teil valida kõigi plaani kirjete alamkogum, et saaksite alamkogumi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="83d83-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="83d83-130">Kehtivuskuupäeva filter</span><span class="sxs-lookup"><span data-stu-id="83d83-130">Effective date filter</span></span> | <span data-ttu-id="83d83-131">Filtreerib plaanid selle põhjal, kas need on aegunud, aktiivsed või tulevikus aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="83d83-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="83d83-132">Märkige ruudud, mis vastavad plaanidele, mida soovite kiirkaardil Plaanid näha.</span><span class="sxs-lookup"><span data-stu-id="83d83-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="83d83-133">Plaanid</span><span class="sxs-lookup"><span data-stu-id="83d83-133">Plans</span></span> | <span data-ttu-id="83d83-134">Kiirkaart Plaanid sisaldab plaane, mis vastavad teie määratud filtri kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="83d83-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="83d83-135">Seotud konfigureerimise suvandid, mille personaliosakond on määranud, ja registreerimise valikud, mille töövõtjad valisid, on igal real kaasatud.</span><span class="sxs-lookup"><span data-stu-id="83d83-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="83d83-136">Väli Kvalifitseeritud määrab, kas plaani valikuga on seotud kinnitamise konflikt.</span><span class="sxs-lookup"><span data-stu-id="83d83-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="83d83-137">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="83d83-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]