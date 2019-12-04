---
title: Uue soodustuse loomine
description: Selles ülesandes näitlikustatakse, kuidas luua soodustuse elemente, mida uue soodustuse loomisel kasutakse.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a74900f288fb5ce145f89e0ccad509deaac505cb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177458"
---
# <a name="create-a-new-benefit"></a><span data-ttu-id="23dfe-103">Uue soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="23dfe-103">Create a new benefit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23dfe-104">Selles ülesandes näitlikustatakse, kuidas luua soodustuse elemente, mida uue soodustuse loomisel kasutakse.</span><span class="sxs-lookup"><span data-stu-id="23dfe-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="23dfe-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="23dfe-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="23dfe-106">See ülesanne on mõeldud hüvitise ja eeliste haldurile.</span><span class="sxs-lookup"><span data-stu-id="23dfe-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="23dfe-107">Soodustuse elementide loomine</span><span class="sxs-lookup"><span data-stu-id="23dfe-107">Create benefit elements</span></span>
1. <span data-ttu-id="23dfe-108">Avage Inimressursid > Soodustused > Häälestamine > Soodustuse elemendid.</span><span class="sxs-lookup"><span data-stu-id="23dfe-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="23dfe-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="23dfe-109">Click New.</span></span>
3. <span data-ttu-id="23dfe-110">Sisestage loodava soodustuse tüüp väljale Tüüp.</span><span class="sxs-lookup"><span data-stu-id="23dfe-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="23dfe-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="23dfe-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23dfe-112">Valige suvand väljal Samaaegne registreerimine.</span><span class="sxs-lookup"><span data-stu-id="23dfe-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="23dfe-113">Töötajate mitmesse meditsiiniplaani registreerumise vältimiseks valige Üks registreerimine tüübi kohta.</span><span class="sxs-lookup"><span data-stu-id="23dfe-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="23dfe-114">Valige suvand väljal Palgakategooria.</span><span class="sxs-lookup"><span data-stu-id="23dfe-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="23dfe-115">Klõpsake vahekaardil Plaanid.</span><span class="sxs-lookup"><span data-stu-id="23dfe-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="23dfe-116">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="23dfe-116">Click New.</span></span>
9. <span data-ttu-id="23dfe-117">Sisestage väärtus väljale Plaan.</span><span class="sxs-lookup"><span data-stu-id="23dfe-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="23dfe-118">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="23dfe-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="23dfe-119">Sisestage või valige väärtus väljal Tüüp.</span><span class="sxs-lookup"><span data-stu-id="23dfe-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="23dfe-120">Valige suvand väljal Palga mõju.</span><span class="sxs-lookup"><span data-stu-id="23dfe-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="23dfe-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="23dfe-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="23dfe-122">Soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="23dfe-122">Create a benefit</span></span>
1. <span data-ttu-id="23dfe-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="23dfe-123">Close the page.</span></span>
2. <span data-ttu-id="23dfe-124">Avage Personaliarvestus > Soodustused > Soodustused.</span><span class="sxs-lookup"><span data-stu-id="23dfe-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="23dfe-125">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="23dfe-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="23dfe-126">Valige või sisestage väärtus väljal Plaan.</span><span class="sxs-lookup"><span data-stu-id="23dfe-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="23dfe-127">Sisestage või valige väärtus väljal Suvand.</span><span class="sxs-lookup"><span data-stu-id="23dfe-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="23dfe-128">Sisestage jõustumiskuupäev ja -kellaaeg väljale Jõustunud.</span><span class="sxs-lookup"><span data-stu-id="23dfe-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="23dfe-129">Klõpsake valikut Loo soodustus.</span><span class="sxs-lookup"><span data-stu-id="23dfe-129">Click Create benefit.</span></span>
