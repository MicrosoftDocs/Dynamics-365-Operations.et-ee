---
title: Finantsperioodi hulgisulgemine
description: Selles teemas näidatakse, kuidas panna periood ootele või sulgeda periood lõplikult korraga rohkem kui ühel juriidilisel isikul.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 398a62e575010501291af3016553fc72fbc891de
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186091"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="8fae4-103">Finantsperioodi hulgisulgemine</span><span class="sxs-lookup"><span data-stu-id="8fae4-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8fae4-104">Selles teemas näidatakse, kuidas panna periood ootele või sulgeda periood lõplikult korraga rohkem kui ühel juriidilisel isikul.</span><span class="sxs-lookup"><span data-stu-id="8fae4-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="8fae4-105">Lisaks näitab see ülesanne, kuidas piirata kasutajagrupil konkreetsetesse moodulitesse sisestamist.</span><span class="sxs-lookup"><span data-stu-id="8fae4-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="8fae4-106">Avage navigeerimispaanil **Moodulid > Pearaamat > Perioodi sulgemine > Pearaamatu kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="8fae4-107">Pange tähele, et kuvatav juriidiliste isikute loend oleneb lehel valitud rahanduskalendrist.</span><span class="sxs-lookup"><span data-stu-id="8fae4-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="8fae4-108">Kuvatakse ainult valitud rahanduskalendrit kasutavad juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="8fae4-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="8fae4-109">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-109">Select **Edit**.</span></span>
3. <span data-ttu-id="8fae4-110">Valige periood, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="8fae4-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="8fae4-111">Valige juriidilised isikud, mille olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="8fae4-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="8fae4-112">Võite valida kiiresti kõik juriidilised isikud, valides ruudustiku ülemisel vasakul poolel küsimärgi.</span><span class="sxs-lookup"><span data-stu-id="8fae4-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="8fae4-113">Valitud mooduli sisestamise juurdepääsu määramiseks valige suvand **Värskenda mooduli juurdepääsu**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="8fae4-114">Mooduli olekut saab muuta ka ühekaupa, muutes ruudustiku kirjeid.</span><span class="sxs-lookup"><span data-stu-id="8fae4-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="8fae4-115">Nupust on abi siis, kui soovite muuta kiiresti juriidilise isiku mitut kirjet.</span><span class="sxs-lookup"><span data-stu-id="8fae4-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="8fae4-116">Valige moodulis **Rakendus** see moodul, mille olekut soovite värskendada.</span><span class="sxs-lookup"><span data-stu-id="8fae4-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="8fae4-117">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-117">Click **Select**.</span></span>
7. <span data-ttu-id="8fae4-118">Valige **Juurdepääsu** tasemel kas **Kõik**, **Mitte keegi** või konkreetne kasutajate rühm.</span><span class="sxs-lookup"><span data-stu-id="8fae4-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="8fae4-119">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-119">Click **Select**.</span></span> <span data-ttu-id="8fae4-120">Suvand Kõik näitab, et kõik mooduli redigeerimisõigusega kasutajad saavad sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="8fae4-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="8fae4-121">Suvand Mitte ükski näitab, et kasutajad ei saa moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="8fae4-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="8fae4-122">Kindel kasutajagrupp näitab, et ainult selles grupis olevad kasutajad saavad moodulisse sisestada, kui periood on avatud.</span><span class="sxs-lookup"><span data-stu-id="8fae4-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="8fae4-123">Tehke valik **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-123">Select **Update**.</span></span>
9. <span data-ttu-id="8fae4-124">Valige oleku uuendamiseks teine periood.</span><span class="sxs-lookup"><span data-stu-id="8fae4-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="8fae4-125">Valige juriidilised isikud, mille perioodi olekut soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="8fae4-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="8fae4-126">Valige suvand **Värskenda perioodi olek** ja seadistage olekuks kas **Ootel**, **Avatud** või **Jäädavalt suletud**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="8fae4-127">**Avatud** näitab, et perioodi saab sisestada, kui kasutajal on juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="8fae4-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="8fae4-128">**Ootel** tähendab, et perioodi ei saa sisestada, aga perioodi saab uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="8fae4-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="8fae4-129">**Jäädavalt suletud** tähendab, et periood on suletud ja seda ei saa kunagi avada.</span><span class="sxs-lookup"><span data-stu-id="8fae4-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="8fae4-130">Korrigeerimisi ei saa sisestada.</span><span class="sxs-lookup"><span data-stu-id="8fae4-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="8fae4-131">Me ei soovita seadistada perioodi olekuks **Jäädavalt suletud** enne, kui kõik kohandused ja auditid on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="8fae4-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="8fae4-132">Tehke valik **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="8fae4-132">Select **Update**.</span></span>

