---
title: Finantsperioodi hulgisulgemine
description: See protseduur näitab, kuidas korraga mitmel juriidilisel isikul perioodi ootele panna või jäädavalt sulgeda.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbe2d3f7d623384e1b356d9bb683db8046a85220
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846339"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="53808-103">Finantsperioodi hulgisulgemine</span><span class="sxs-lookup"><span data-stu-id="53808-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53808-104">See protseduur näitab, kuidas korraga mitmel juriidilisel isikul perioodi ootele panna või jäädavalt sulgeda.</span><span class="sxs-lookup"><span data-stu-id="53808-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="53808-105">Lisaks näitab see ülesanne, kuidas piirata kasutajagrupil konkreetsetesse moodulitesse sisestamist.</span><span class="sxs-lookup"><span data-stu-id="53808-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="53808-106">Avage Pearaamat > Perioodi sulgemine > Pearaamatu kalendrid.</span><span class="sxs-lookup"><span data-stu-id="53808-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="53808-107">Pange tähele, et kuvatav juriidiliste isikute loend oleneb lehel valitud rahanduskalendrist.</span><span class="sxs-lookup"><span data-stu-id="53808-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="53808-108">Kuvatakse ainult valitud rahanduskalendrit kasutavad juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="53808-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="53808-109">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="53808-109">Click Edit.</span></span>
3. <span data-ttu-id="53808-110">Valige periood, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="53808-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="53808-111">Valige juriidilised isikud, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="53808-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="53808-112">Saate valida kiiresti kõik juriidilised isikud, valides üleval, ruudustiku vasakul poolel oleva märgi.</span><span class="sxs-lookup"><span data-stu-id="53808-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="53808-113">Valige Uuenda mooduli juurdepääsu, et määratleda juurdepääs valitud moodulisse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="53808-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="53808-114">Mooduli olekut saab muuta ka ühekaupa, muutes ruudustiku kirjeid.</span><span class="sxs-lookup"><span data-stu-id="53808-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="53808-115">Nupust on abi siis, kui soovite muuta kiiresti juriidilise isiku mitut kirjet.</span><span class="sxs-lookup"><span data-stu-id="53808-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="53808-116">Sisestage või valige väljal Rakendusemoodul see moodul, mille olekut soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="53808-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="53808-117">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="53808-117">Click Select.</span></span>
7. <span data-ttu-id="53808-118">Tehke jaotises Juurdepääsu tase valik Kõik, Pole või konkreetne kasutajagrupp.</span><span class="sxs-lookup"><span data-stu-id="53808-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="53808-119">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="53808-119">Click Select.</span></span>
    * <span data-ttu-id="53808-120">Suvand Kõik näitab, et kõik mooduli redigeerimisõigusega kasutajad saavad sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="53808-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="53808-121">Suvand Mitte ükski näitab, et kasutajad ei saa moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="53808-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="53808-122">Kindel kasutajagrupp näitab, et ainult selles grupis olevad kasutajad saavad moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="53808-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="53808-123">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="53808-123">Click Update.</span></span>
9. <span data-ttu-id="53808-124">Valige oleku uuendamiseks teine periood.</span><span class="sxs-lookup"><span data-stu-id="53808-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="53808-125">Valige juriidilised isikud, mille perioodi olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="53808-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="53808-126">Valige Uuenda perioodi olekut ja määrake olekuks Ootel, Avatud või Jäädavalt suletud.</span><span class="sxs-lookup"><span data-stu-id="53808-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="53808-127">Suvand Avatud näitab, et perioodile saab sisestada, eeldusel, et kasutajal on juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="53808-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="53808-128">Ootel tähendab, et perioodi ei saa sisestada, kuid perioodi saab uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="53808-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="53808-129">Jäädavalt suletud tähendab, et periood on suletud ja seda ei saa enam kunagi avada.</span><span class="sxs-lookup"><span data-stu-id="53808-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="53808-130">Korrigeerimisi ei saa sisestada.</span><span class="sxs-lookup"><span data-stu-id="53808-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="53808-131">Me ei soovita määrata perioodi olekuks Jäädavalt suletud, enne kui kõik korrigeerimised ja auditid on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="53808-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="53808-132">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="53808-132">Click Update.</span></span>

