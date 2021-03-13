---
title: Isikliku kontakti sobivuse suvandite konfigureerimine
description: Isiklike kontaktide sobivuse suvandite konfigureerimine rakenduses Microsoft Dynamics 365 Human Resources. Isiklikud kontaktid võivad olla kasusaajad või sõltuvad.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 137416477928fd4d6b4438f25df5afea93972027
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112236"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="06a2a-104">Isikliku kontakti sobivuse suvandite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="06a2a-104">Configure personal contact eligibility options</span></span>

<span data-ttu-id="06a2a-105">See artikkel näitab, kuidas konfigureerida soodustuste kasutamiseks isiklike kontaktide tüüpe rakenduses Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="06a2a-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="06a2a-106">Isiklikud kontaktid võivad olla kasusaajad või sõltuvad.</span><span class="sxs-lookup"><span data-stu-id="06a2a-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="06a2a-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Isikliku kontakti sobivuse suvandid**.</span><span class="sxs-lookup"><span data-stu-id="06a2a-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="06a2a-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="06a2a-108">Select **New**.</span></span>

3. <span data-ttu-id="06a2a-109">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="06a2a-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="06a2a-110">Väli</span><span class="sxs-lookup"><span data-stu-id="06a2a-110">Field</span></span> | <span data-ttu-id="06a2a-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="06a2a-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="06a2a-112">**Sobivuse suvand**</span><span class="sxs-lookup"><span data-stu-id="06a2a-112">**Eligibility option**</span></span> | <span data-ttu-id="06a2a-113">Kordumatu sobivuse suvandi nimi või kood, et tuvastada sobivuse suvandit.</span><span class="sxs-lookup"><span data-stu-id="06a2a-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="06a2a-114">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="06a2a-114">**Description**</span></span> | <span data-ttu-id="06a2a-115">Sobivuse suvandi lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="06a2a-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="06a2a-116">**Kontakti sobivuskood**</span><span class="sxs-lookup"><span data-stu-id="06a2a-116">**Contact eligibility code**</span></span> | <span data-ttu-id="06a2a-117">Isikliku sobivuse suvandit kõige paremini kirjeldav süsteemikood.</span><span class="sxs-lookup"><span data-stu-id="06a2a-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="06a2a-118">Saate valida järgneva seast.</span><span class="sxs-lookup"><span data-stu-id="06a2a-118">You can choose from:</span></span> <ul><li><span data-ttu-id="06a2a-119">Seos</span><span class="sxs-lookup"><span data-stu-id="06a2a-119">Relationship</span></span></li><li><span data-ttu-id="06a2a-120">Üliõpilane</span><span class="sxs-lookup"><span data-stu-id="06a2a-120">Student</span></span></li><li><span data-ttu-id="06a2a-121">Liiga vana sõltuv</span><span class="sxs-lookup"><span data-stu-id="06a2a-121">Overage dependent</span></span></li><li><span data-ttu-id="06a2a-122">Liiga vana invaliidist sõltuv</span><span class="sxs-lookup"><span data-stu-id="06a2a-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="06a2a-123">**Olek**</span><span class="sxs-lookup"><span data-stu-id="06a2a-123">**Status**</span></span> | <span data-ttu-id="06a2a-124">Sobivuse suvandi olek.</span><span class="sxs-lookup"><span data-stu-id="06a2a-124">The status of the eligibility option.</span></span> <span data-ttu-id="06a2a-125">Kui sobivuse suvandi olek on seatud passiivseks, ei saa te seda isiklike kontaktide abikõlblikkuse valikut isiklike kontaktide jaoks valida.</span><span class="sxs-lookup"><span data-stu-id="06a2a-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="06a2a-126">**Seos**</span><span class="sxs-lookup"><span data-stu-id="06a2a-126">**Relationship**</span></span> | <span data-ttu-id="06a2a-127">Määrab seose isikliku kontakti ja töövõtja vahel.</span><span class="sxs-lookup"><span data-stu-id="06a2a-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="06a2a-128">See väli on aktiivne ainult juhul, kui kontakti sobivuse kood on seatud suvandile Seos.</span><span class="sxs-lookup"><span data-stu-id="06a2a-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="06a2a-129">**Vanus**</span><span class="sxs-lookup"><span data-stu-id="06a2a-129">**Age**</span></span> | <span data-ttu-id="06a2a-130">Soodustuse plaani sobiva isikliku kontakti maksimaalne vanus.</span><span class="sxs-lookup"><span data-stu-id="06a2a-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="06a2a-131">See väli on aktiivne ainult siis, kui valite seose.</span><span class="sxs-lookup"><span data-stu-id="06a2a-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="06a2a-132">Seda vanust võrreldakse isikliku kontakti arvutatud vanusega.</span><span class="sxs-lookup"><span data-stu-id="06a2a-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="06a2a-133">Arvutatud vanus on: (katvuse kuupäev – isiklik kontakti sünnikuupäev / 365).</span><span class="sxs-lookup"><span data-stu-id="06a2a-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="06a2a-134">See number on alati täisarv.</span><span class="sxs-lookup"><span data-stu-id="06a2a-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="06a2a-135">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="06a2a-135">Select **Save**.</span></span> 
