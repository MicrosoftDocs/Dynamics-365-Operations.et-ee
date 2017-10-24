--- 
title: Finantsperioodi hulgisulgemine
description: "See protseduur näitab, kuidas korraga mitmel juriidilisel isikul perioodi ootele panna või jäädavalt sulgeda."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d7151cbcd02f9312ca6b0de5e27231a0b0dc9d6
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="mass-financial-period-close"></a><span data-ttu-id="19f37-103">Finantsperioodi hulgisulgemine</span><span class="sxs-lookup"><span data-stu-id="19f37-103">Mass financial period close</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19f37-104">See protseduur näitab, kuidas korraga mitmel juriidilisel isikul perioodi ootele panna või jäädavalt sulgeda.</span><span class="sxs-lookup"><span data-stu-id="19f37-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="19f37-105">Lisaks näitab see ülesanne, kuidas piirata kasutajagrupil konkreetsetesse moodulitesse sisestamist.</span><span class="sxs-lookup"><span data-stu-id="19f37-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="19f37-106">Avage Pearaamat > Perioodi sulgemine > Pearaamatu kalendrid.</span><span class="sxs-lookup"><span data-stu-id="19f37-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="19f37-107">Pange tähele, et kuvatav juriidiliste isikute loend oleneb lehel valitud rahanduskalendrist.</span><span class="sxs-lookup"><span data-stu-id="19f37-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="19f37-108">Kuvatakse ainult valitud rahanduskalendrit kasutavad juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="19f37-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="19f37-109">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="19f37-109">Click Edit.</span></span>
3. <span data-ttu-id="19f37-110">Valige periood, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="19f37-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="19f37-111">Valige juriidilised isikud, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="19f37-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="19f37-112">Saate valida kiiresti kõik juriidilised isikud, valides üleval, ruudustiku vasakul poolel oleva märgi.</span><span class="sxs-lookup"><span data-stu-id="19f37-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="19f37-113">Valige Uuenda mooduli juurdepääsu, et määratleda juurdepääs valitud moodulisse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="19f37-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="19f37-114">Mooduli olekut saab muuta ka ühekaupa, muutes ruudustiku kirjeid.</span><span class="sxs-lookup"><span data-stu-id="19f37-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="19f37-115">Nupust on abi siis, kui soovite muuta kiiresti juriidilise isiku mitut kirjet.</span><span class="sxs-lookup"><span data-stu-id="19f37-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="19f37-116">Sisestage või valige väljal Rakendusemoodul see moodul, mille olekut soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="19f37-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="19f37-117">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="19f37-117">Click Select.</span></span>
7. <span data-ttu-id="19f37-118">Tehke jaotises Juurdepääsu tase valik Kõik, Pole või konkreetne kasutajagrupp.</span><span class="sxs-lookup"><span data-stu-id="19f37-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="19f37-119">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="19f37-119">Click Select.</span></span>
    * <span data-ttu-id="19f37-120">Suvand Kõik näitab, et kõik mooduli redigeerimisõigusega kasutajad saavad sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="19f37-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="19f37-121">Suvand Mitte ükski näitab, et kasutajad ei saa moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="19f37-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="19f37-122">Kindel kasutajagrupp näitab, et ainult selles grupis olevad kasutajad saavad moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="19f37-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="19f37-123">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="19f37-123">Click Update.</span></span>
9. <span data-ttu-id="19f37-124">Valige oleku uuendamiseks teine periood.</span><span class="sxs-lookup"><span data-stu-id="19f37-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="19f37-125">Valige juriidilised isikud, mille perioodi olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="19f37-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="19f37-126">Valige Uuenda perioodi olekut ja määrake olekuks Ootel, Avatud või Jäädavalt suletud.</span><span class="sxs-lookup"><span data-stu-id="19f37-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="19f37-127">Suvand Avatud näitab, et perioodile saab sisestada, eeldusel, et kasutajal on juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="19f37-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="19f37-128">Ootel tähendab, et perioodi ei saa sisestada, kuid perioodi saab uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="19f37-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="19f37-129">Jäädavalt suletud tähendab, et periood on suletud ja seda ei saa enam kunagi avada.</span><span class="sxs-lookup"><span data-stu-id="19f37-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="19f37-130">Korrigeerimisi ei saa sisestada.</span><span class="sxs-lookup"><span data-stu-id="19f37-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="19f37-131">Me ei soovita määrata perioodi olekuks Jäädavalt suletud, enne kui kõik korrigeerimised ja auditid on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="19f37-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="19f37-132">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="19f37-132">Click Update.</span></span>


