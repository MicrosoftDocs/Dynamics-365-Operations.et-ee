---
title: Tulevaste elusündmuste konfigureerimine
description: Saate rakenduses Dynamics 365 Human Resources ajastada tulevasi elusündmuseid.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d52e91e7b050027485b3536f40f6ad80afd90de8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056728"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="403f2-103">Tulevaste elusündmuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="403f2-103">Configure future life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="403f2-104">Saate rakenduses Dynamics 365 Human Resources ajastada tulevasi elusündmuseid.</span><span class="sxs-lookup"><span data-stu-id="403f2-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="403f2-105">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Tulevased elusündmused**.</span><span class="sxs-lookup"><span data-stu-id="403f2-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="403f2-106">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="403f2-106">Select **New**.</span></span>

3. <span data-ttu-id="403f2-107">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="403f2-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="403f2-108">Väli</span><span class="sxs-lookup"><span data-stu-id="403f2-108">Field</span></span> | <span data-ttu-id="403f2-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="403f2-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="403f2-110">Elusündmuse kuupäev</span><span class="sxs-lookup"><span data-stu-id="403f2-110">Life event date</span></span> | <span data-ttu-id="403f2-111">Süsteem töötleb kõiki sündmusi registreerimisperioodil, mis toimuvad kuni selle kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="403f2-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="403f2-112">Elusündmus logitud</span><span class="sxs-lookup"><span data-stu-id="403f2-112">Life event logged</span></span> | <span data-ttu-id="403f2-113">Elusündmuse logimise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="403f2-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="403f2-114">Logitüüp</span><span class="sxs-lookup"><span data-stu-id="403f2-114">Log type</span></span> | <span data-ttu-id="403f2-115">Näitab, kas tegevus on üks järgmiste hulgast.</span><span class="sxs-lookup"><span data-stu-id="403f2-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="403f2-116">- **Värskendamine** – olemasoleva kirje muutmine, mis jälgib elusündmusi</span><span class="sxs-lookup"><span data-stu-id="403f2-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="403f2-117">- **Sisestamine** – uue elusündmuse kirje loomine</span><span class="sxs-lookup"><span data-stu-id="403f2-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="403f2-118">Elusündmuse tüübi ID</span><span class="sxs-lookup"><span data-stu-id="403f2-118">Life event type ID</span></span> | <span data-ttu-id="403f2-119">Elusündmuse tüübi kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="403f2-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="403f2-120">Elusündmuse tüüp</span><span class="sxs-lookup"><span data-stu-id="403f2-120">Life event type</span></span> | <span data-ttu-id="403f2-121">Töövõtja soodustuste registreerimise uuendamise katalüsaator.</span><span class="sxs-lookup"><span data-stu-id="403f2-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="403f2-122">Lisateavet vaadake elusündmuse päästikute jaotisest.</span><span class="sxs-lookup"><span data-stu-id="403f2-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="403f2-123">Olek</span><span class="sxs-lookup"><span data-stu-id="403f2-123">Status</span></span> | <span data-ttu-id="403f2-124">Kas elusündmus on töödeldud või mitte.</span><span class="sxs-lookup"><span data-stu-id="403f2-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="403f2-125">Liin</span><span class="sxs-lookup"><span data-stu-id="403f2-125">Line</span></span> | <span data-ttu-id="403f2-126">Tulevase elusündmuse reanumber.</span><span class="sxs-lookup"><span data-stu-id="403f2-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="403f2-127">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="403f2-127">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]