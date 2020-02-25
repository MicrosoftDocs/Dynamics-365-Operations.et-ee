---
title: Kassa loagruppide loomine
description: Selles teemas tutvustatakse, kuidas luua kassa loagruppe.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6f9f8f970f336a0cce6bcac78e32a1b7fe0a252
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022257"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="8d931-103">Kassa loagruppide loomine</span><span class="sxs-lookup"><span data-stu-id="8d931-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8d931-104">Selles teemas tutvustatakse, kuidas luua kassa loagruppe.</span><span class="sxs-lookup"><span data-stu-id="8d931-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="8d931-105">Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="8d931-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="8d931-106">See ülesanne on mõeldud kaubandustoimingute halduri rolli jaoks.</span><span class="sxs-lookup"><span data-stu-id="8d931-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="8d931-107">Avage navigeerimispaanil **Moodulid > Jaemüük ja kaubandus > Töötajad > Loagrupid**.</span><span class="sxs-lookup"><span data-stu-id="8d931-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="8d931-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8d931-108">Select **New**.</span></span>
3. <span data-ttu-id="8d931-109">Väljale **Kassa loagrupi ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="8d931-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="8d931-110">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="8d931-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="8d931-111">Valige väärtus **Jah** väljal **Kellaaja kirjete kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="8d931-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="8d931-112">Saate nüüd oma kassalubade grupile erinevaid lube anda või neid eemaldada.</span><span class="sxs-lookup"><span data-stu-id="8d931-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="8d931-113">Mõne loa jaoks saate määrata väärtuse, mida kasutatakse hindamiseks, kas kassa kasutaja saab seda toimingut teha.</span><span class="sxs-lookup"><span data-stu-id="8d931-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="8d931-114">See tegevusjuhend annab mõned load, mida kassapidajale võidakse määrata.</span><span class="sxs-lookup"><span data-stu-id="8d931-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="8d931-115">Valige väärtus **Jah** väljal **Luba tellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="8d931-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="8d931-116">Valige väärtus **Jah** väljal **Luba tellimuse redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="8d931-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="8d931-117">Valige väärtus **Jah** väljal **Luba tellimuse toomine**.</span><span class="sxs-lookup"><span data-stu-id="8d931-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="8d931-118">Valige väärtus **Jah** väljal **Luba parooli muutmine**.</span><span class="sxs-lookup"><span data-stu-id="8d931-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="8d931-119">Valige väärtus **Jah** väljal **Luba pimedalt sulgemine**.</span><span class="sxs-lookup"><span data-stu-id="8d931-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="8d931-120">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8d931-120">Select **Save**.</span></span> <span data-ttu-id="8d931-121">Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused ärikanalitesse edastada.</span><span class="sxs-lookup"><span data-stu-id="8d931-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="8d931-122">Navigeerimispaanil avage **Moodulid > Personaliosakond > Tööd > Tööd**.</span><span class="sxs-lookup"><span data-stu-id="8d931-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="8d931-123">Järgmisena määrame kassalubade grupi töö järgi.</span><span class="sxs-lookup"><span data-stu-id="8d931-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="8d931-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="8d931-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8d931-125">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="8d931-125">Select **Edit**.</span></span>
15. <span data-ttu-id="8d931-126">Laiendage jaotist **Töö klassifikatsioon**.</span><span class="sxs-lookup"><span data-stu-id="8d931-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="8d931-127">Sisestage või valige väärtus väljal POS permission group (Kassalubade grupp).</span><span class="sxs-lookup"><span data-stu-id="8d931-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="8d931-128">Kõik töötajad, kelle ametikohad sellele tööle vastavad, kasutavad selle kassalubade grupi sätteid, kui töötajate kassalube ei ole nende ametikoha tasemel tühistatud.</span><span class="sxs-lookup"><span data-stu-id="8d931-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="8d931-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8d931-129">Select **Save**.</span></span> <span data-ttu-id="8d931-130">Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused kanalitesse edastada.</span><span class="sxs-lookup"><span data-stu-id="8d931-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

