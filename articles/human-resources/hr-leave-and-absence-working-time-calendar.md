---
title: Tööajakalendri loomine
description: Määratlege rakenduses Dynamics 365 Human Resources tööajakalender, pühad ja mittetöised ajad.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bedbe65f146c4159c2a809de8f683815fd4a01f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428798"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="0042c-103">Tööajakalendri loomine</span><span class="sxs-lookup"><span data-stu-id="0042c-103">Create a working time calendar</span></span>

<span data-ttu-id="0042c-104">Rakenduse Dynamics 365 Human Resources tööajakalender kuvab päevad ja tunnid, mil töövõtjad teie organisatsioonis töötavad.</span><span class="sxs-lookup"><span data-stu-id="0042c-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="0042c-105">Kui töötaja esitab vaba aja taotluse, ei pea nad puhkuste ja kinniolekuaegade pärast muretsema.</span><span class="sxs-lookup"><span data-stu-id="0042c-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="0042c-106">Vaba aja taotluste sujuvamaks muutmiseks konfigureerige järgmised üksused oma organisatsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="0042c-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="0042c-107">Tööajakalender</span><span class="sxs-lookup"><span data-stu-id="0042c-107">Working time calendar</span></span>
- <span data-ttu-id="0042c-108">Pühad ja kinniolekuajad</span><span class="sxs-lookup"><span data-stu-id="0042c-108">Holidays and closures</span></span>
- <span data-ttu-id="0042c-109">Mittetöötamise aeg</span><span class="sxs-lookup"><span data-stu-id="0042c-109">Non-work time</span></span>

<span data-ttu-id="0042c-110">Saate tööajakalendri seadistamisel lisada vähemalt kaks üksust.</span><span class="sxs-lookup"><span data-stu-id="0042c-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="0042c-111">Lisaks saate neid eraldi konfigureerida või uuendada.</span><span class="sxs-lookup"><span data-stu-id="0042c-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="0042c-112">Tööajakalendri seadistamine</span><span class="sxs-lookup"><span data-stu-id="0042c-112">Set up a working time calendar</span></span>

<span data-ttu-id="0042c-113">Seadistage vähemalt üks tööajakalender, mis kuvab teie töötamise päevad ja tunnid.</span><span class="sxs-lookup"><span data-stu-id="0042c-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="0042c-114">Kui teil on asukohad mitmes riigis ja regioonis, võite soovida seadistada tööajakalendri iga piirkonna jaoks.</span><span class="sxs-lookup"><span data-stu-id="0042c-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="0042c-115">Valige lehel **Organisatsiooni haldus** suvand **Kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="0042c-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="0042c-116">Valige suvand **Uus** ja sisestage oma kalendri nimi ning kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="0042c-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="0042c-117">Jaotises **Loomissuvandid** valige oma organisatsiooni tööpäevad ja sisestage tööajad.</span><span class="sxs-lookup"><span data-stu-id="0042c-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="0042c-118">Puhkuse või kinniolekuaja lisamiseks valige nupp **Lisa** suvandi **Pühad ja kinniolekuajad** kõrval.</span><span class="sxs-lookup"><span data-stu-id="0042c-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="0042c-119">Mittetöötamise aja (nt lõunad või pausid) lisamiseks valige käsk **Lisa** jaotises **MITTETÖÖTAMISE AEG** ja sisestage nimi ning ajavahemik.</span><span class="sxs-lookup"><span data-stu-id="0042c-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="0042c-120">Jaotises **Päevad** valige suvand **Loo**, et luua kalendrisse päevad.</span><span class="sxs-lookup"><span data-stu-id="0042c-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="0042c-121">Sisestage kalendri kuupäevavahemik ja valige seejärel suvand **Loo päevad**.</span><span class="sxs-lookup"><span data-stu-id="0042c-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="0042c-122">Töögraafikute lisamiseks valige suvandis **Töögraafik** käsk **Lisa** ja sisestage iga töögraafiku ajad.</span><span class="sxs-lookup"><span data-stu-id="0042c-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="0042c-123">Pühade ja kinniolekuaegade konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0042c-123">Configure holidays and closures</span></span>

<span data-ttu-id="0042c-124">Saate pühasid ja kinniolekuaegu lisada või muuta tööajakalendris eraldi.</span><span class="sxs-lookup"><span data-stu-id="0042c-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="0042c-125">Valige lehel **Organisatsiooni haldus** suvand **Pühad ja kinniolekuajad**.</span><span class="sxs-lookup"><span data-stu-id="0042c-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="0042c-126">Valige suvand **Uus** ja sisestage püha või kinniolekuaja nimi ja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="0042c-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="0042c-127">Mittetöötamise aja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0042c-127">Configure non-work time</span></span>

<span data-ttu-id="0042c-128">Saate mittetöötamise aegu lisada või muuta tööajakalendris eraldi.</span><span class="sxs-lookup"><span data-stu-id="0042c-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="0042c-129">Valige lehel **Organisatsiooni haldus** suvand **Mittetöötamise aeg**.</span><span class="sxs-lookup"><span data-stu-id="0042c-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="0042c-130">Valige suvand **Uus** ja sisestage mittetöötamise aja nimi ja ajavahemik.</span><span class="sxs-lookup"><span data-stu-id="0042c-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="0042c-131">Kui olete kuvanud puhkuste ja puudumiste riigipühade korrigeerimiste eelvaatefunktsiooni, kasutab rakendus Human Resources pühasid ja kinnioleku kuupäevasid, et kalendris registreeritud töövõtjate reguleerimiseks määrata päevade arv.</span><span class="sxs-lookup"><span data-stu-id="0042c-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="0042c-132">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0042c-132">See also</span></span>

- [<span data-ttu-id="0042c-133">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="0042c-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="0042c-134">Puhkuste ja puudumiste tüüpide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0042c-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
