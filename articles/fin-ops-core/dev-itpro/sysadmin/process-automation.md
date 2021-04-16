---
title: Protsessi automatiseerimine
description: Selles teemas kirjeldatakse üksikasju selle kohta, kuidas protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist.
author: RyanCCarlson2
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 509decec3c3d3b598a2457cddba4896730480ec6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745921"
---
# <a name="process-automation"></a><span data-ttu-id="0659e-103">Protsessi automatiseerimine</span><span class="sxs-lookup"><span data-stu-id="0659e-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0659e-104">Protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist.</span><span class="sxs-lookup"><span data-stu-id="0659e-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="0659e-105">Plaanitud töö värskendatud kalendri vaade võimaldab lõppkasutajatel vaadata ja teha toiminguid plaanitud ja lõpule viidud tööga.</span><span class="sxs-lookup"><span data-stu-id="0659e-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="0659e-106">Haldus</span><span class="sxs-lookup"><span data-stu-id="0659e-106">Administration</span></span>

<span data-ttu-id="0659e-107">Kõigi protsessi automatiseerimiste keskse halduse lehe leiate süsteemihalduse mooduli menüü jaotisest **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="0659e-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="0659e-108">Sellel lehel loetletakse kõik süsteemis seadistatud automatiseeritud protsessid (seeriad).</span><span class="sxs-lookup"><span data-stu-id="0659e-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="0659e-109">Saate lisada ka uusi protsessi automatiseerimisi otse sellelt lehelt.</span><span class="sxs-lookup"><span data-stu-id="0659e-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="0659e-110">Pärast seeria seadistamist saate selle loendi kaudu hallata kõiki seeriaid.</span><span class="sxs-lookup"><span data-stu-id="0659e-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="0659e-111">Saate redigeerida tervet seeriat, seda kustutada, vaadata loendivaatest kõiki esinemisi või keelata seeria, kui soovite plaanitud töö mõneks ajaks peatada.</span><span class="sxs-lookup"><span data-stu-id="0659e-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="0659e-112">Funktsioonihalduses keelatud protsesse ei näidata, kui funktsioon on keelatud.</span><span class="sxs-lookup"><span data-stu-id="0659e-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="0659e-113">Lisaks ei ajasta protsessi automatiseerimise ajastamise mootor keelatud funktsiooni jaoks ühtegi esinemiskorda ega taustaprotsessi.</span><span class="sxs-lookup"><span data-stu-id="0659e-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="0659e-114">Funktsiooni uuesti lubamisel käivitatakse kohe varem ajastatud esinemiskorrad või taustaprotsessid.</span><span class="sxs-lookup"><span data-stu-id="0659e-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="0659e-115">Kalendri vaade</span><span class="sxs-lookup"><span data-stu-id="0659e-115">Calendar view</span></span>

<span data-ttu-id="0659e-116">Protsessi automatiseerimise üks peamisi eeliseid on võimalus kuvada plaanitud tööd lihtsas kalendri vaates.</span><span class="sxs-lookup"><span data-stu-id="0659e-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="0659e-117">See vaade võimaldab teil kuvada tööd nädala kaupa.</span><span class="sxs-lookup"><span data-stu-id="0659e-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="0659e-118">See vaade kuvatakse lehe **Protsessi automatiseerimine** paremal küljel.</span><span class="sxs-lookup"><span data-stu-id="0659e-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="0659e-119">See asustatakse valitud seeria plaanitud tööga.</span><span class="sxs-lookup"><span data-stu-id="0659e-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="0659e-120">[![Protsessi automatiseerimise kalender](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="0659e-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="0659e-121">Esinemiste muudatused</span><span class="sxs-lookup"><span data-stu-id="0659e-121">Occurrence changes</span></span>

<span data-ttu-id="0659e-122">Igat esinemist saab muuta, mõjutamata teisi määratletud esinemisi, mis pärinevad sellest seeriast.</span><span class="sxs-lookup"><span data-stu-id="0659e-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="0659e-123">Plaanitud töö esinemisi saab redigeerida kalendri vaates, valides nupu **Kuva/Redigeeri** ja valides **Esinemised**.</span><span class="sxs-lookup"><span data-stu-id="0659e-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="0659e-124">See leht annab teile juurdepääsu kõigile seeria häälestuse viisardis algselt kuvatud sätetele ja annab võimaluse muuta valituid esinemisi üks kord.</span><span class="sxs-lookup"><span data-stu-id="0659e-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="0659e-125">Plaanitud töö esinemist saab ka välja lülitada, valides kalendri vaates nupu **Keela**.</span><span class="sxs-lookup"><span data-stu-id="0659e-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="0659e-126">Arendaja dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="0659e-126">Developer documentation</span></span>

<span data-ttu-id="0659e-127">Protsessi automatiseerimise raamistik võimaldab arendajatel laiendada protsessi automatiseerimise raamistikku.</span><span class="sxs-lookup"><span data-stu-id="0659e-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="0659e-128">[Protsessi automatiseerimise raamistiku](../process-automation/process-automation-framework.md) dokumentatsioonis antakse teavet selle kohta, kuidas saate luua kohandatud protsesse, mida on vaja pakktöötlusserveris käitamiseks, mis on plaanitud protsessi automatiseerimise viisardis ja kuvatakse automaatselt kalendri vaates.</span><span class="sxs-lookup"><span data-stu-id="0659e-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]