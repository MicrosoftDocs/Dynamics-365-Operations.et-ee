--- 
title: Finantsperioodi hulgisulgemine
description: "See protseduur näitab, kuidas korraga mitmel juriidilisel isikul perioodi ootele panna või jäädavalt sulgeda."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 83ecd06c1bb0b2179251fdccb3898fb3edbca51f
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="mass-financial-period-close"></a><span data-ttu-id="6c732-103">Finantsperioodi hulgisulgemine</span><span class="sxs-lookup"><span data-stu-id="6c732-103">Mass financial period close</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c732-104">See protseduur näitab, kuidas korraga mitmel juriidilisel isikul perioodi ootele panna või jäädavalt sulgeda.</span><span class="sxs-lookup"><span data-stu-id="6c732-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="6c732-105">Lisaks näitab see ülesanne, kuidas piirata kasutajagrupil konkreetsetesse moodulitesse sisestamist.</span><span class="sxs-lookup"><span data-stu-id="6c732-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="6c732-106">Avage Pearaamat > Perioodi sulgemine > Pearaamatu kalendrid.</span><span class="sxs-lookup"><span data-stu-id="6c732-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="6c732-107">Pange tähele, et kuvatav juriidiliste isikute loend oleneb lehel valitud rahanduskalendrist.</span><span class="sxs-lookup"><span data-stu-id="6c732-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="6c732-108">Kuvatakse ainult valitud rahanduskalendrit kasutavad juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="6c732-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="6c732-109">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="6c732-109">Click Edit.</span></span>
3. <span data-ttu-id="6c732-110">Valige periood, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="6c732-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="6c732-111">Valige juriidilised isikud, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="6c732-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="6c732-112">Saate valida kiiresti kõik juriidilised isikud, valides üleval, ruudustiku vasakul poolel oleva märgi.</span><span class="sxs-lookup"><span data-stu-id="6c732-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="6c732-113">Valige Uuenda mooduli juurdepääsu, et määratleda juurdepääs valitud moodulisse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="6c732-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="6c732-114">Mooduli olekut saab muuta ka ühekaupa, muutes ruudustiku kirjeid.</span><span class="sxs-lookup"><span data-stu-id="6c732-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="6c732-115">Nupust on abi siis, kui soovite muuta kiiresti juriidilise isiku mitut kirjet.</span><span class="sxs-lookup"><span data-stu-id="6c732-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="6c732-116">Sisestage või valige väljal Rakendusemoodul see moodul, mille olekut soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="6c732-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="6c732-117">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="6c732-117">Click Select.</span></span>
7. <span data-ttu-id="6c732-118">Tehke jaotises Juurdepääsu tase valik Kõik, Pole või konkreetne kasutajagrupp.</span><span class="sxs-lookup"><span data-stu-id="6c732-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="6c732-119">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="6c732-119">Click Select.</span></span>
    * <span data-ttu-id="6c732-120">Suvand Kõik näitab, et kõik mooduli redigeerimisõigusega kasutajad saavad sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="6c732-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="6c732-121">Suvand Mitte ükski näitab, et kasutajad ei saa moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="6c732-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="6c732-122">Kindel kasutajagrupp näitab, et ainult selles grupis olevad kasutajad saavad moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="6c732-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="6c732-123">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="6c732-123">Click Update.</span></span>
9. <span data-ttu-id="6c732-124">Valige oleku uuendamiseks teine periood.</span><span class="sxs-lookup"><span data-stu-id="6c732-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="6c732-125">Valige juriidilised isikud, mille perioodi olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="6c732-125">Select the legal entities for which you want to update the period status.</span></span>
11. <span data-ttu-id="6c732-126">Valige Uuenda perioodi olekut ja määrake olekuks Ootel, Avatud või Jäädavalt suletud.</span><span class="sxs-lookup"><span data-stu-id="6c732-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="6c732-127">Suvand Avatud näitab, et perioodile saab sisestada, eeldusel, et kasutajal on juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="6c732-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="6c732-128">Ootel tähendab, et perioodi ei saa sisestada, kuid perioodi saab uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="6c732-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="6c732-129">Jäädavalt suletud tähendab, et periood on suletud ja seda ei saa enam kunagi avada.</span><span class="sxs-lookup"><span data-stu-id="6c732-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="6c732-130">Korrigeerimisi ei saa sisestada.</span><span class="sxs-lookup"><span data-stu-id="6c732-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="6c732-131">Me ei soovita määrata perioodi olekuks Jäädavalt suletud, enne kui kõik korrigeerimised ja auditid on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="6c732-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="6c732-132">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="6c732-132">Click Update.</span></span>


