---
title: Protsessi automatiseerimine
description: Selles teemas kirjeldatakse üksikasju selle kohta, kuidas protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508181"
---
# <a name="process-automation"></a><span data-ttu-id="0922f-103">Protsessi automatiseerimine</span><span class="sxs-lookup"><span data-stu-id="0922f-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0922f-104">Protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist.</span><span class="sxs-lookup"><span data-stu-id="0922f-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="0922f-105">Plaanitud töö värskendatud kalendri vaade võimaldab lõppkasutajatel vaadata ja teha toiminguid plaanitud ja lõpule viidud tööga.</span><span class="sxs-lookup"><span data-stu-id="0922f-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="0922f-106">Haldus</span><span class="sxs-lookup"><span data-stu-id="0922f-106">Administration</span></span>

<span data-ttu-id="0922f-107">Kõigi protsessi automatiseerimiste keskse halduse lehe leiate süsteemihalduse mooduli menüü jaotisest **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="0922f-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="0922f-108">Sellel lehel loetletakse kõik süsteemis seadistatud automatiseeritud protsessid (seeriad).</span><span class="sxs-lookup"><span data-stu-id="0922f-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="0922f-109">Saate lisada ka uusi protsessi automatiseerimisi otse sellelt lehelt.</span><span class="sxs-lookup"><span data-stu-id="0922f-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="0922f-110">Pärast seeria seadistamist saate selle loendi kaudu hallata kõiki seeriaid.</span><span class="sxs-lookup"><span data-stu-id="0922f-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="0922f-111">Saate redigeerida tervet seeriat, kustutada, vaadata loendivaatest kõiki esinemisi või keelata seeria, kui soovite plaanitud töö teatud ajavahemikuks peatada.</span><span class="sxs-lookup"><span data-stu-id="0922f-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="0922f-112">Kalendri vaade</span><span class="sxs-lookup"><span data-stu-id="0922f-112">Calendar view</span></span> 
<span data-ttu-id="0922f-113">Protsessi automatiseerimise üks peamisi eeliseid on võimalus kuvada plaanitud tööd lihtsas kalendri vaates.</span><span class="sxs-lookup"><span data-stu-id="0922f-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="0922f-114">See vaade võimaldab teil kuvada tööd nädala kaupa.</span><span class="sxs-lookup"><span data-stu-id="0922f-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="0922f-115">See vaade kuvatakse lehe **Protsessi automatiseerimine** paremal küljel.</span><span class="sxs-lookup"><span data-stu-id="0922f-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="0922f-116">See asustatakse valitud seeria plaanitud tööga.</span><span class="sxs-lookup"><span data-stu-id="0922f-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="0922f-117">[![Protsessi automatiseerimise kalender](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="0922f-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="0922f-118">Esinemiste muudatused</span><span class="sxs-lookup"><span data-stu-id="0922f-118">Occurrence changes</span></span>
<span data-ttu-id="0922f-119">Igat esinemist saab muuta, mõjutamata teisi määratletud esinemisi, mis pärinevad sellest seeriast.</span><span class="sxs-lookup"><span data-stu-id="0922f-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="0922f-120">Plaanitud töö esinemisi saab redigeerida kalendri vaates, valides nupu **Kuva/Redigeeri** ja valides **Esinemised**.</span><span class="sxs-lookup"><span data-stu-id="0922f-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="0922f-121">See annab teile juurdepääsu kõigile seeria häälestuse viisardis algselt kuvatud sätetele ja annab võimaluse teha ühekordne muudatuse valitud esinemisele.</span><span class="sxs-lookup"><span data-stu-id="0922f-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="0922f-122">Plaanitud töö esinemist saab ka välja lülitada, valides kalendri vaates nupu **Keela**.</span><span class="sxs-lookup"><span data-stu-id="0922f-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="0922f-123">Arendaja dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="0922f-123">Developer documentation</span></span> 
<span data-ttu-id="0922f-124">Arendaja dokumentatsiooni kirjutatakse praegu, et lubada arendajatele protsessi automatiseerimise raamistiku laiendamist.</span><span class="sxs-lookup"><span data-stu-id="0922f-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="0922f-125">See dokumentatsioon annab teavet selle kohta, kuidas saate luua kohandatud protsesse, mida on vaja pakktöötlusserveris käitamiseks, mis on plaanitud protsessi automatiseerimise viisardis ja kuvatakse automaatselt kalendri vaates.</span><span class="sxs-lookup"><span data-stu-id="0922f-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
