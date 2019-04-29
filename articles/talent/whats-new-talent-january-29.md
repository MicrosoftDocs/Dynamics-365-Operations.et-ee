---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (31. jaanuar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4504cebb7702c7163c94badeeb06d9af0e5467e
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "857634"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="32088-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (31. jaanuar 2019)</span><span class="sxs-lookup"><span data-stu-id="32088-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32088-104">Selles teemas kirjeldatakse Dynamics 365 for Talenti uusi või muutunud funktsioone</span><span class="sxs-lookup"><span data-stu-id="32088-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="32088-105">**Järk 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="32088-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="32088-106">Core HR-i muudatused</span><span class="sxs-lookup"><span data-stu-id="32088-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="32088-107">Puhkusel olevate inimeste kaardil olev vaba aeg ei võta arvesse puhkuseplaani kuupäevi</span><span class="sxs-lookup"><span data-stu-id="32088-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="32088-108">Nende puhul, kellel on puhkuseplaanid, mida kalendriaastas ei rakendata, kuvatakse nüüd kaardil **Võetud** vaba aeg, mis on võetud määratletud puhkuseplaaniga aastal.</span><span class="sxs-lookup"><span data-stu-id="32088-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="32088-109">Näiteks kui organisatsiooni puhkuseaasta on 1. juunist 30. maini ja töövõtja on võtnud detsembris kolm vaba päeva, kuvatakse 15. jaanuaril kaardil **Võetud** kolm päeva.</span><span class="sxs-lookup"><span data-stu-id="32088-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="32088-110">Kogunenud summad ei vasta järgu kuupäevale</span><span class="sxs-lookup"><span data-stu-id="32088-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="32088-111">Puhkustele ja puudumistele (suvandi **Inimressursid** parameetrid) on lisatud uued suvandid, mis võimaldavad klientidel määrata töövõtjate töötatud kuude kehtivusaja.</span><span class="sxs-lookup"><span data-stu-id="32088-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="32088-112">Mõne organisatsiooni puhul on see kuu lõpus, teiste puhul võib olla järgmise kuu alguses.</span><span class="sxs-lookup"><span data-stu-id="32088-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="32088-113">Näiteks võib üks organisatsioon võimaldada vaba aja 31. detsembril, teine aga 1. jaanuaril.</span><span class="sxs-lookup"><span data-stu-id="32088-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="32088-114">See suvand võimaldab valida vaba aja toimumisaja.</span><span class="sxs-lookup"><span data-stu-id="32088-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="32088-115">Töötaja värbamistoimingud on kinni jäänud olekusse Töövoog on lõpetatud</span><span class="sxs-lookup"><span data-stu-id="32088-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="32088-116">Tehtud on muudatused, et parandada probleem, milles väike hulk töövoogusid lõpevad olekuga Töövoog on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="32088-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="32088-117">Uued töövood peaksid nüüd minema töövoo lõppemisel olekusse Lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="32088-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="32088-118">Kõik töövood, mille olek on Töövoog on lõpetatud, viiakse tõrkeolekusse, et võimaldada selle värskendamist või eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="32088-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
