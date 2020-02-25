---
title: Isikliku kontakti sobivuse suvandite konfigureerimine
description: Isiklike kontaktide sobivuse suvandite konfigureerimine rakenduses Microsoft Dynamics 365 Human Resources. Isiklikud kontaktid võivad olla kasusaajad või sõltuvad.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008773"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="a004e-104">Isikliku kontakti sobivuse suvandite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a004e-104">Configure personal contact eligibility options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a004e-105">See artikkel näitab, kuidas konfigureerida soodustuste kasutamiseks isiklike kontaktide tüüpe rakenduses Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a004e-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a004e-106">Isiklikud kontaktid võivad olla kasusaajad või sõltuvad.</span><span class="sxs-lookup"><span data-stu-id="a004e-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="a004e-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Isikliku kontakti sobivuse suvandid**.</span><span class="sxs-lookup"><span data-stu-id="a004e-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="a004e-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a004e-108">Select **New**.</span></span>

3. <span data-ttu-id="a004e-109">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="a004e-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a004e-110">Väli</span><span class="sxs-lookup"><span data-stu-id="a004e-110">Field</span></span> | <span data-ttu-id="a004e-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a004e-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a004e-112">**Sobivuse suvand**</span><span class="sxs-lookup"><span data-stu-id="a004e-112">**Eligibility option**</span></span> | <span data-ttu-id="a004e-113">Kordumatu sobivuse suvandi nimi või kood, et tuvastada sobivuse suvandit.</span><span class="sxs-lookup"><span data-stu-id="a004e-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="a004e-114">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="a004e-114">**Description**</span></span> | <span data-ttu-id="a004e-115">Sobivuse suvandi lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="a004e-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="a004e-116">**Kontakti sobivuskood**</span><span class="sxs-lookup"><span data-stu-id="a004e-116">**Contact eligibility code**</span></span> | <span data-ttu-id="a004e-117">Isikliku sobivuse suvandit kõige paremini kirjeldav süsteemikood.</span><span class="sxs-lookup"><span data-stu-id="a004e-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="a004e-118">Saate valida järgneva seast.</span><span class="sxs-lookup"><span data-stu-id="a004e-118">You can choose from:</span></span> <ul><li><span data-ttu-id="a004e-119">Seos</span><span class="sxs-lookup"><span data-stu-id="a004e-119">Relationship</span></span></li><li><span data-ttu-id="a004e-120">Üliõpilane</span><span class="sxs-lookup"><span data-stu-id="a004e-120">Student</span></span></li><li><span data-ttu-id="a004e-121">Liiga vana sõltuv</span><span class="sxs-lookup"><span data-stu-id="a004e-121">Overage dependent</span></span></li><li><span data-ttu-id="a004e-122">Liiga vana invaliidist sõltuv</span><span class="sxs-lookup"><span data-stu-id="a004e-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="a004e-123">**Olek**</span><span class="sxs-lookup"><span data-stu-id="a004e-123">**Status**</span></span> | <span data-ttu-id="a004e-124">Sobivuse suvandi olek.</span><span class="sxs-lookup"><span data-stu-id="a004e-124">The status of the eligibility option.</span></span> <span data-ttu-id="a004e-125">Kui sobivuse suvandi olek on seatud passiivseks, ei saa te seda isiklike kontaktide abikõlblikkuse valikut isiklike kontaktide jaoks valida.</span><span class="sxs-lookup"><span data-stu-id="a004e-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="a004e-126">**Seos**</span><span class="sxs-lookup"><span data-stu-id="a004e-126">**Relationship**</span></span> | <span data-ttu-id="a004e-127">Määrab seose isikliku kontakti ja töövõtja vahel.</span><span class="sxs-lookup"><span data-stu-id="a004e-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="a004e-128">See väli on aktiivne ainult juhul, kui kontakti sobivuse kood on seatud suvandile Seos.</span><span class="sxs-lookup"><span data-stu-id="a004e-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="a004e-129">**Vanus**</span><span class="sxs-lookup"><span data-stu-id="a004e-129">**Age**</span></span> | <span data-ttu-id="a004e-130">Soodustuse plaani sobiva isikliku kontakti maksimaalne vanus.</span><span class="sxs-lookup"><span data-stu-id="a004e-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="a004e-131">See väli on aktiivne ainult siis, kui valite seose.</span><span class="sxs-lookup"><span data-stu-id="a004e-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="a004e-132">Seda vanust võrreldakse isikliku kontakti arvutatud vanusega.</span><span class="sxs-lookup"><span data-stu-id="a004e-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="a004e-133">Arvutatud vanus on: (katvuse kuupäev – isiklik kontakti sünnikuupäev / 365).</span><span class="sxs-lookup"><span data-stu-id="a004e-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="a004e-134">See number on alati täisarv.</span><span class="sxs-lookup"><span data-stu-id="a004e-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="a004e-135">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a004e-135">Select **Save**.</span></span> 