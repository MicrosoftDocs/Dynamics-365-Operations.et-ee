---
title: Tulevaste elusündmuste konfigureerimine
description: Saate rakenduses Dynamics 365 Human Resources ajastada tulevasi elusündmuseid.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418109"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="4c8ef-103">Tulevaste elusündmuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4c8ef-103">Configure future life events</span></span>

<span data-ttu-id="4c8ef-104">Saate rakenduses Dynamics 365 Human Resources ajastada tulevasi elusündmuseid.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="4c8ef-105">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Tulevased elusündmused**.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="4c8ef-106">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-106">Select **New**.</span></span>

3. <span data-ttu-id="4c8ef-107">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4c8ef-108">Väli</span><span class="sxs-lookup"><span data-stu-id="4c8ef-108">Field</span></span> | <span data-ttu-id="4c8ef-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4c8ef-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4c8ef-110">Elusündmuse kuupäev</span><span class="sxs-lookup"><span data-stu-id="4c8ef-110">Life event date</span></span> | <span data-ttu-id="4c8ef-111">Süsteem töötleb kõiki sündmusi registreerimisperioodil, mis toimuvad kuni selle kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="4c8ef-112">Elusündmus logitud</span><span class="sxs-lookup"><span data-stu-id="4c8ef-112">Life event logged</span></span> | <span data-ttu-id="4c8ef-113">Elusündmuse logimise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="4c8ef-114">Logitüüp</span><span class="sxs-lookup"><span data-stu-id="4c8ef-114">Log type</span></span> | <span data-ttu-id="4c8ef-115">Näitab, kas tegevus on üks järgmiste hulgast.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="4c8ef-116">- **Värskendamine** – olemasoleva kirje muutmine, mis jälgib elusündmusi</span><span class="sxs-lookup"><span data-stu-id="4c8ef-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="4c8ef-117">- **Sisestamine** – uue elusündmuse kirje loomine</span><span class="sxs-lookup"><span data-stu-id="4c8ef-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="4c8ef-118">Elusündmuse tüübi ID</span><span class="sxs-lookup"><span data-stu-id="4c8ef-118">Life event type ID</span></span> | <span data-ttu-id="4c8ef-119">Elusündmuse tüübi kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="4c8ef-120">Elusündmuse tüüp</span><span class="sxs-lookup"><span data-stu-id="4c8ef-120">Life event type</span></span> | <span data-ttu-id="4c8ef-121">Töövõtja soodustuste registreerimise uuendamise katalüsaator.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="4c8ef-122">Lisateavet vaadake elusündmuse päästikute jaotisest.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="4c8ef-123">Olek</span><span class="sxs-lookup"><span data-stu-id="4c8ef-123">Status</span></span> | <span data-ttu-id="4c8ef-124">Kas elusündmus on töödeldud või mitte.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="4c8ef-125">Liin</span><span class="sxs-lookup"><span data-stu-id="4c8ef-125">Line</span></span> | <span data-ttu-id="4c8ef-126">Tulevase elusündmuse reanumber.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="4c8ef-127">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4c8ef-127">Select **Save**.</span></span> 
