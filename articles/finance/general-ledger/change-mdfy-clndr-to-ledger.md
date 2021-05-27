---
title: Pearaamatu kalendri muutmine ja ümbermääramine
description: Selles teemas selgitatakse, kuidas muuta pearaamatule praegu määratud kalendrit ja pearaamatule uue kalendri määramist.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039946"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="0f9ce-103">Pearaamatu kalendri muutmine ja ümbermääramine</span><span class="sxs-lookup"><span data-stu-id="0f9ce-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f9ce-104">Selles teemas selgitatakse, kuidas muuta pearaamatule praegu määratud kalendrit ja pearaamatule uue kalendri määramist.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="0f9ce-105">Probleem</span><span class="sxs-lookup"><span data-stu-id="0f9ce-105">Issue</span></span>

<span data-ttu-id="0f9ce-106">Mõnikord peavad ettevõtted kas muutma olemasolevat kalendrit, mis on pearaamatule määratud, või määrama uue kalendri.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="0f9ce-107">Lahendus</span><span class="sxs-lookup"><span data-stu-id="0f9ce-107">Resolution</span></span>

<span data-ttu-id="0f9ce-108">Pearaamatu kalendri muutmiseks või uuestimääramiseks on kaks stsenaariumit.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="0f9ce-109">Esimene stsenaarium hõlmab olemasoleva kalendri muutmist, mis on juba pearaamatule määratud.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="0f9ce-110">Teine stsenaarium hõlmab uue kalendri loomist ja selle määramist pearaamatule.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="0f9ce-111">Mõlemaid muudatusi saab teha igal ajal pärast kannete sisestamist pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="0f9ce-112">Olemasoleva rahanduskalendri muutmine</span><span class="sxs-lookup"><span data-stu-id="0f9ce-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="0f9ce-113">Olemasoleva kalendri muutmiseks, mis on määratud teie pearaamatule, avage **Pearaamat \> Pearaamatu seadistus \> Pearaamat** ja valige rahanduskalendri link, et avada leht **Pearaamatu kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="0f9ce-114">Kalendris tehtavatel muudatustel on piirangud.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="0f9ce-115">Näiteks saate muuta aasta *perioodide* algus- ja lõppkuupäevi, kuid te ei saa kalendris muuta *aasta* algus- ja lõppkuupäevi.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="0f9ce-116">Aasta perioode muutmiseks valige asjakohane kalender ja aasta.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="0f9ce-117">Esmalt kustutage nupu **Kustuta periood** abil mõned või kõik olemasolevad tegevusperioodid.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="0f9ce-118">Kustutada saab kõik tegevusperioodid, välja arvatud esimese.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="0f9ce-119">Seejärel jagage nupu **Jaga periood** abil järelejäänud periood või perioodid uuteks perioodideks, sisestades järgmise perioodi jaoks asjakohase alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="0f9ce-120">Pärast kalendri perioodide muutmist peate käitama protsessi **Pearaamatu perioodide ümberarvutamine** igas juriidilises isikus (ettevõttes), millele see kalender on määratud.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="0f9ce-121">Kuigi ükski hoiatusteade ei tuleta teile selle etapi lõpuleviimist meelde, on ümberarvutusprotsess nõutav igale pearaamatusse sisestatud kandele määratud perioodi uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="0f9ce-122">Ümberarvutusprotsessi käitamiseks valige iga ettevõtte lehel **Pearaamatu seadistus** protsess **Pearaamatu perioodide ümberarvutamine**.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="0f9ce-123">Kui ümberarvutusprotsessi ei käitata, võidakse proovibilansi või finantsaruande kandesaldod kaasata perioodidesse valesti.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="0f9ce-124">Sel juhul saate ümberarvutusprotsessi käitamise abil saldosid igal ajal korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="0f9ce-125">Uue rahanduskalendri määramine</span><span class="sxs-lookup"><span data-stu-id="0f9ce-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="0f9ce-126">Uue rahanduskalendri määramiseks avage **Pearaamat \> Pearaamatu seadistus \> Pearaamat** ja valige käsk **Redigeeri**, et seada leht **Pearaamat** redigeerimisrežiimi.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="0f9ce-127">Seejärel valige väljal **Rahanduskalender** uus rahanduskalender.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="0f9ce-128">Pärast pearaamatu rahanduskalendri muutmist peate käitama protsessi **Pearaamatu perioodide ümberarvutamine**.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="0f9ce-129">Kui määrate pearaamatule uue rahanduskalendri, tuletatakse teile teatega selle etapi lõpuleviimist meelde.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="0f9ce-130">Kuigi see teade võib jätta mulje, et ümberarvutamisprotsess on valikuline, pole see nii.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="0f9ce-131">See on nõutav igale pearaamatusse sisestatud kandele määratud perioodi uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="0f9ce-132">Ümberarvutusprotsessi käitamiseks valige lehel **Pearaamatu seadistus** protsess **Pearaamatu perioodide ümberarvutamine**.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="0f9ce-133">Kui ümberarvutusprotsessi ei käitata, võidakse proovibilansi või finantsaruande kandesaldod kaasata perioodidesse valesti.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="0f9ce-134">Sel juhul saate ümberarvutusprotsessi käitamise abil saldosid igal ajal korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="0f9ce-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
