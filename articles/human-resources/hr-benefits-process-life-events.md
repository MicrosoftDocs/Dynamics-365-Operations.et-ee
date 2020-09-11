---
title: Elusündmuste töötlemine
description: Töövõtja töötsükli ajal rakenduses Microsoft Dynamics 365 Human Resources võib igal töövõtjal esineda mitmesuguseid elusündmuste muudatusi.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ada986888a22afe83885985a694cd00ff94c9217
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741407"
---
# <a name="process-life-events"></a><span data-ttu-id="05cf6-103">Elusündmuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="05cf6-103">Process life events</span></span>

<span data-ttu-id="05cf6-104">Töövõtja töötsükli ajal rakenduses Microsoft Dynamics 365 Human Resources võib igal töövõtjal esineda mitmesuguseid elusündmuste muudatusi.</span><span class="sxs-lookup"><span data-stu-id="05cf6-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="05cf6-105">Näiteks abielu, tööhõive muutus või sõltuva isiku / kasusaaja muutus.</span><span class="sxs-lookup"><span data-stu-id="05cf6-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="05cf6-106">Elusündmuste kasutamiseks peate lubama elusündmused soodustuste parameetrite vormil, häälestama elusündmuse tüübid ja seadistama plaani tüüpide jaoks elusündmuse valikud.</span><span class="sxs-lookup"><span data-stu-id="05cf6-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="05cf6-107">Enne kui saate elusündmusi töödelda, peate olema käitanud avatud registreerimist vähemalt üks kord värbamise ajavahemikus.</span><span class="sxs-lookup"><span data-stu-id="05cf6-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="05cf6-108">Ameerika Ühendriikides on avatud registreerimine tavaliselt üks kord aastas.</span><span class="sxs-lookup"><span data-stu-id="05cf6-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="05cf6-109">Väljaspool Ameerika Ühendriike võib avatud registreerimine toimuda värbamise ajal.</span><span class="sxs-lookup"><span data-stu-id="05cf6-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="05cf6-110">Töötaja ei pea valima elusündmuste töötlemiseks soodustuse plaani, kuid nad peavad olema avatud registreerimise töötlemisse kaasatud.</span><span class="sxs-lookup"><span data-stu-id="05cf6-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="05cf6-111">Kasutage elusündmuse töötlemist, kui teil on töötajad, kellel toimuvad elusündmused kuupäeval, mis on tulevikus.</span><span class="sxs-lookup"><span data-stu-id="05cf6-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="05cf6-112">See sündmus töötleb kõiki elusündmusi, mida pole töödeldud (nt tulevased elusündmused või lisatud elusündmused, mis ei ole ühelegi töötajale spetsiifilised – üks näide on uus soodustus).</span><span class="sxs-lookup"><span data-stu-id="05cf6-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="05cf6-113">Reaalajas elusündmused on peidetud.</span><span class="sxs-lookup"><span data-stu-id="05cf6-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="05cf6-114">Näiteks, kui täna on 1. veebruar ja 14. veebruaril töötaja Erki Sepal on plaanis muuta juriidilist isikut, kui käivitate elusündmuse töötluse 15. veebruaril, siis töötleb süsteem kõiki sündmusi kuni 15. veebruarini.</span><span class="sxs-lookup"><span data-stu-id="05cf6-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="05cf6-115">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Elusündmuse töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="05cf6-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="05cf6-116">Dialoogiaknas **Elusündmuse registreerimise protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="05cf6-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="05cf6-117">Väli</span><span class="sxs-lookup"><span data-stu-id="05cf6-117">Field</span></span> | <span data-ttu-id="05cf6-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="05cf6-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="05cf6-119">**Registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="05cf6-119">**Enrollment period**</span></span> | <span data-ttu-id="05cf6-120">Registreerimisperiood, mille jaoks elusündmusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="05cf6-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="05cf6-121">**Juriidiline isik**</span><span class="sxs-lookup"><span data-stu-id="05cf6-121">**Legal entity**</span></span> | <span data-ttu-id="05cf6-122">Juriidiline isik, mille jaoks elusündmusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="05cf6-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="05cf6-123">**Elusündmuse kuupäev**</span><span class="sxs-lookup"><span data-stu-id="05cf6-123">**Life event date**</span></span> | <span data-ttu-id="05cf6-124">Süsteem töötleb kõiki sündmusi registreerimisperioodil, mis toimuvad kuni selle kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="05cf6-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="05cf6-125">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="05cf6-125">**Worker**</span></span> | <span data-ttu-id="05cf6-126">Töötaja, kelle jaoks elusündmusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="05cf6-126">The worker to process life events for.</span></span> <span data-ttu-id="05cf6-127">Kui jätate selle välja tühjaks, töödeldakse elusündmusi kõigi töötajate puhul.</span><span class="sxs-lookup"><span data-stu-id="05cf6-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="05cf6-128">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="05cf6-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="05cf6-129">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="05cf6-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="05cf6-130">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="05cf6-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="05cf6-131">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="05cf6-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="05cf6-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="05cf6-132">Select **OK**.</span></span> <span data-ttu-id="05cf6-133">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="05cf6-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="05cf6-134">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="05cf6-134">Select **OK**.</span></span>
