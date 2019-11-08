---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (16. oktoober 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0d7c6562ca8b5e7cfa0071ec408955e13a46cb6e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551699"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a><span data-ttu-id="7e6bd-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (16. oktoober 2018)</span><span class="sxs-lookup"><span data-stu-id="7e6bd-103">What's new or changed in Dynamics 365 Talent - Core HR (October 16, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="7e6bd-104">**Järk 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="7e6bd-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="7e6bd-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="7e6bd-106">Lubage juhatajatel värskendada vabade päevade taotluseid</span><span class="sxs-lookup"><span data-stu-id="7e6bd-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="7e6bd-107">Töövõtjate vabade päevade taotlused võivad pärast töövoos heakskiitmist uuendamist vajada.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="7e6bd-108">Paljudel juhtudel teeb juhataja need uuendused töövõtja nimel.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="7e6bd-109">See uus funktsioon võimaldab juhatajatel värskendada või tühistada vabade päevade taotlusi oma töövõtjate nimel.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="7e6bd-110">Seda võimalust juhib **Töötamine kellegi nimel** parameeter, mida saab seadistada **Inimressursside parameetrite** lehel.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="7e6bd-111">Lubage personaliosakonnal värskendada vabade päevade taotluseid</span><span class="sxs-lookup"><span data-stu-id="7e6bd-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="7e6bd-112">Sarnaselt ülalolevale funktsioonile saab personaliosakond värskendada vabade päevade taotlused, kui need on eelnevalt läbi töövoo heaks kiidetud.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="7e6bd-113">See funktsioon võimaldab personaliosakonna kasutajatel värskendada vabade päevade taotlusi.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="7e6bd-114">Võimaluse saab lubada **Inimeste** tööruumis ja **Töötaja** lehel, kasutades uut suvandit nimega **Kuva vabad päevad**.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="7e6bd-115">Nendel lehtedel saavad personaliosakonna kasutajad vaadata ja värskendada vabade päeavade kandeid, sarnaselt sellele, kuidas juhatajad neid tegevusi teevad.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="7e6bd-116">Turbekohustus, mis kontrollib selle funktsionaalsuse ligipääsu on järgmine.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="7e6bd-117">Kohustus: töötajapõhiste puhkuste ja puudumiste protsesside haldamine.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="7e6bd-118">Privileeg: kõigi töötajate puhkuste ja puudumiste taotluste haldamine.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="7e6bd-119">Muud muudatused</span><span class="sxs-lookup"><span data-stu-id="7e6bd-119">Other changes</span></span>
<span data-ttu-id="7e6bd-120">Selles väljaandes on tehtud järgmised uuendused.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="7e6bd-121">Muutused töötaja palkamise toimingutes, et nad ei ole enam "kinni" **Töövoog on lõpetatud** olekus.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="7e6bd-122">Töösuhte kirje saab nüüd luua ilma töösuhte alguskuupäevata.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="7e6bd-123">Dynamics 365 Talenti registreerimiskuupäev Töövõtja iseteeninduses kuvatud kursusele rakendab nüüd ajavööndi nihke kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="7e6bd-124">Exceli faile saab importida mitu korda ilma vigadeta, kasutades **Töötaja üksust**.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="7e6bd-125">Teadaolev probleem</span><span class="sxs-lookup"><span data-stu-id="7e6bd-125">Known issue</span></span>

- <span data-ttu-id="7e6bd-126">**Probleemi**: uuele töötajale seotuse lisamisel on nupud **Uus** ja **Redigeeri** hallid.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="7e6bd-127">**Lahendus:** veenduge enne manuse lehe avamist, et **Töötaja** lehe kiirinfod oleksid suletud.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="7e6bd-128">Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud.</span><span class="sxs-lookup"><span data-stu-id="7e6bd-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="7e6bd-129">(See probleem lahendatakse järgmisel platvormivärskendusel.)</span><span class="sxs-lookup"><span data-stu-id="7e6bd-129">(This issue will be fixed in the next platform update.)</span></span>
