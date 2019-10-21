---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (23. jaanuar 2019)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
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
ms.openlocfilehash: f1983d5a58fb2e6b1984727e1d7b44803b94cdce
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023972"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-january-23-2019"></a><span data-ttu-id="a7561-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent: Core HR (23. jaanuar 2019)</span><span class="sxs-lookup"><span data-stu-id="a7561-103">What's new or changed in Dynamics 365 Talent: Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7561-104">**Järk 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="a7561-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="a7561-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="a7561-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="a7561-106">Muudatused</span><span class="sxs-lookup"><span data-stu-id="a7561-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="a7561-107">Töövõtja põhipalga importimine ei toimi uute põhipalga kirjete loomisel</span><span class="sxs-lookup"><span data-stu-id="a7561-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="a7561-108">Töövõtja põhipalga üksust on muudetud, et tuua importimisel kompensatsioonitase.</span><span class="sxs-lookup"><span data-stu-id="a7561-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="a7561-109">Enne seda väljaannet kuvati teade, et tase on nõutav.</span><span class="sxs-lookup"><span data-stu-id="a7561-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="a7561-110">Vaba aja taotluse dialoogiboksist eemaldati minimaalse saldo väli</span><span class="sxs-lookup"><span data-stu-id="a7561-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="a7561-111">Dialoogiboksist **Vaba aja taotlus** on eemaldatud väli **Minimaalne saldo**.</span><span class="sxs-lookup"><span data-stu-id="a7561-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="a7561-112">See muudatus mõjutab kõiki alasid, kus vaba aega saab taotleda.</span><span class="sxs-lookup"><span data-stu-id="a7561-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="a7561-113">Andmete täiendamine kompensatsioonitasemete puhul ei värskendu kõigi stsenaariumide puhul</span><span class="sxs-lookup"><span data-stu-id="a7561-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="a7561-114">Tehtud on muudatus, et värskendada kompensatsioonitaset põhipalga plaanidel.</span><span class="sxs-lookup"><span data-stu-id="a7561-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="a7561-115">See muudatus kannab kompensatsioonitaseme töövõtjale määratud töö põhipalga plaanidele.</span><span class="sxs-lookup"><span data-stu-id="a7561-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="a7561-116">Palgateave lehel Muudatuste haldamine on saadaval ainult süsteemiadministraatorina sisselogimisel</span><span class="sxs-lookup"><span data-stu-id="a7561-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="a7561-117">See muudatus võimaldab palgaarvestuse administraatori rolliga töövõtjatel pääseda ametikoha lehel juurde palgateabele jaotises **Muudatuste ajajoon > Muudatuste haldamine**.</span><span class="sxs-lookup"><span data-stu-id="a7561-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="a7561-118">Töö väljad on ametikoha vaikeväärtused</span><span class="sxs-lookup"><span data-stu-id="a7561-118">Job fields default to positions</span></span>
<span data-ttu-id="a7561-119">Ametikoha töö muutmisel on töö väljad ametikoha vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="a7561-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="a7561-120">Kuvatakse teatis, mis võimaldab kinnitada vaikeväärtused või säilitada nende väljade olemasolevad väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7561-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="a7561-121">Katseaega ja kalendrit ei kuvata tulevikus palgatavate töövõtjate puhul.</span><span class="sxs-lookup"><span data-stu-id="a7561-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="a7561-122">Selle muudatusega on väljad **Katseaeg** ja **Kalender** lisatud lehele **Muudatuste haldamine**, et võimaldada andmete sisestamist tulevaste ja olemasolevate töövõtjate puhul.</span><span class="sxs-lookup"><span data-stu-id="a7561-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="a7561-123">Finance and Operationsi 23. platvormi värskendus</span><span class="sxs-lookup"><span data-stu-id="a7561-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="a7561-124">Finance and Operationsi platvormivärskenduse 23 osana on tehtud väiksemaid veaparandusi.</span><span class="sxs-lookup"><span data-stu-id="a7561-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="a7561-125">Lisateavet vt teemast [Mis on uut või mida on muudetud rakenduse Dynamics 365 Finance and Operations platvormivärskenduses 23 (jaanuar 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="a7561-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
