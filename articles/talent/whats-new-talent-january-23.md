---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (23. jaanuar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talent Core HR-i uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4e492095d5269ec81c0c22145b7af356937c256b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742512"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="18081-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (23. jaanuar 2019)</span><span class="sxs-lookup"><span data-stu-id="18081-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18081-104">**Järk 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="18081-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="18081-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="18081-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="18081-106">Muudatused</span><span class="sxs-lookup"><span data-stu-id="18081-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="18081-107">Töövõtja põhipalga importimine ei toimi uute põhipalga kirjete loomisel</span><span class="sxs-lookup"><span data-stu-id="18081-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="18081-108">Töövõtja põhipalga üksust on muudetud, et tuua importimisel kompensatsioonitase.</span><span class="sxs-lookup"><span data-stu-id="18081-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="18081-109">Enne seda väljaannet kuvati teade, et tase on nõutav.</span><span class="sxs-lookup"><span data-stu-id="18081-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="18081-110">Vaba aja taotluse dialoogiboksist eemaldati minimaalse saldo väli</span><span class="sxs-lookup"><span data-stu-id="18081-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="18081-111">Dialoogiboksist **Vaba aja taotlus** on eemaldatud väli **Minimaalne saldo**.</span><span class="sxs-lookup"><span data-stu-id="18081-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="18081-112">See muudatus mõjutab kõiki alasid, kus vaba aega saab taotleda.</span><span class="sxs-lookup"><span data-stu-id="18081-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="18081-113">Andmete täiendamine kompensatsioonitasemete puhul ei värskendu kõigi stsenaariumide puhul</span><span class="sxs-lookup"><span data-stu-id="18081-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="18081-114">Tehtud on muudatus, et värskendada kompensatsioonitaset põhipalga plaanidel.</span><span class="sxs-lookup"><span data-stu-id="18081-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="18081-115">See muudatus kannab kompensatsioonitaseme töövõtjale määratud töö põhipalga plaanidele.</span><span class="sxs-lookup"><span data-stu-id="18081-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="18081-116">Palgateave lehel Muudatuste haldamine on saadaval ainult süsteemiadministraatorina sisselogimisel</span><span class="sxs-lookup"><span data-stu-id="18081-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="18081-117">See muudatus võimaldab palgaarvestuse administraatori rolliga töövõtjatel pääseda ametikoha lehel juurde palgateabele jaotises **Muudatuste ajajoon > Muudatuste haldamine**.</span><span class="sxs-lookup"><span data-stu-id="18081-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="18081-118">Töö väljad on ametikoha vaikeväärtused</span><span class="sxs-lookup"><span data-stu-id="18081-118">Job fields default to positions</span></span>
<span data-ttu-id="18081-119">Ametikoha töö muutmisel on töö väljad ametikoha vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="18081-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="18081-120">Kuvatakse teatis, mis võimaldab kinnitada vaikeväärtused või säilitada nende väljade olemasolevad väärtused.</span><span class="sxs-lookup"><span data-stu-id="18081-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="18081-121">Katseaega ja kalendrit ei kuvata tulevikus palgatavate töövõtjate puhul.</span><span class="sxs-lookup"><span data-stu-id="18081-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="18081-122">Selle muudatusega on väljad **Katseaeg** ja **Kalender** lisatud lehele **Muudatuste haldamine**, et võimaldada andmete sisestamist tulevaste ja olemasolevate töövõtjate puhul.</span><span class="sxs-lookup"><span data-stu-id="18081-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="18081-123">Platvormivärskendus update 23</span><span class="sxs-lookup"><span data-stu-id="18081-123">Platform update 23</span></span>
<span data-ttu-id="18081-124">Platvormivärskenduse 23 osana on tehtud väiksemaid veaparandusi.</span><span class="sxs-lookup"><span data-stu-id="18081-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="18081-125">Lisateavet vt teemast [Mis on uut või mida on muudetud rakenduse Dynamics 365 for Finance and Operations platvormivärskenduses 23 (jaanuar 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="18081-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
