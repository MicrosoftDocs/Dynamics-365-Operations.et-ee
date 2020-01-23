---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (11. jaanuar 2019)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899170"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a><span data-ttu-id="76b36-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (11. jaanuar 2019)</span><span class="sxs-lookup"><span data-stu-id="76b36-103">What's new or changed in Dynamics 365 Talent - Core HR (January 11, 2019)</span></span>

<span data-ttu-id="76b36-104">**Järk 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="76b36-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="76b36-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="76b36-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="76b36-106">Muudatused</span><span class="sxs-lookup"><span data-stu-id="76b36-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="76b36-107">Puhkusetaotluste valideerimine, prognoosides saadaolevat saldot</span><span class="sxs-lookup"><span data-stu-id="76b36-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="76b36-108">Selles versioonis tehtud muudatused võimaldavad töövõtjatel taotleda tulevast puhkust seda praegusest saldost lahutamata.</span><span class="sxs-lookup"><span data-stu-id="76b36-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="76b36-109">Kõigis tulevastes taotlustes kasutatakse standardseid töövooge.</span><span class="sxs-lookup"><span data-stu-id="76b36-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="76b36-110">Lisateavet vt teemast [Töötundidel põhinev kumulatiivne puhkuseaeg](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="76b36-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="76b36-111">Prognoositud puhkusesaldo kuvamine rakendustes Töövõtja iseteenindus ja Inimesed</span><span class="sxs-lookup"><span data-stu-id="76b36-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="76b36-112">See funktsioon võimaldab personaliosakonnal, juhtidel ja töövõtjatel vaadata saldosid tulevasteks puhkuseperioodideks.</span><span class="sxs-lookup"><span data-stu-id="76b36-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="76b36-113">Töövõtjad saavad tulevasi saldosid vaadata tööruumis **Töövõtja iseteenindus** ja personaliosakond pääseb samale teabele juurde tööruumis **Inimesed**.</span><span class="sxs-lookup"><span data-stu-id="76b36-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="76b36-114">Teatised puhkusesaldode muutmise kohta</span><span class="sxs-lookup"><span data-stu-id="76b36-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="76b36-115">Puhkusesaldod kuvavad töövõtjate jooksva saldo.</span><span class="sxs-lookup"><span data-stu-id="76b36-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="76b36-116">Tulevased saldod on saadaval tööruumides **Töövõtja iseteenindus** ja **Inimesed**, sisestades prognoositud saldo arvutamiseks kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="76b36-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="76b36-117">Prognoositud saldode kuvamiseks on lisatud navigeerimisfunktsioon järgmistele aladele.</span><span class="sxs-lookup"><span data-stu-id="76b36-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="76b36-118">Kaart **Vaba aeg** tööruumis **Töövõtja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="76b36-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="76b36-119">Kaart **Puhkused ja puudumised** tööruumis **Juhi iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="76b36-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="76b36-120">Leht **Puhkused ja puudumised** tööruumis **Inimesed**.</span><span class="sxs-lookup"><span data-stu-id="76b36-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="76b36-121">Kümnendkohtade lubamine ergutussüsteemi plaanides (sularahaplaanid)</span><span class="sxs-lookup"><span data-stu-id="76b36-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="76b36-122">Ergutussüsteemi sularahapreemiatel ja plaanidel on nüüd täiendav paindlikkus kümnendkohtadega summade ja väärtuste tühistamise suhtes.</span><span class="sxs-lookup"><span data-stu-id="76b36-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="76b36-123">Ergutussüsteemi registreerimistel ei saa kuupäevi pärast plaani salvestamist muuta</span><span class="sxs-lookup"><span data-stu-id="76b36-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="76b36-124">See muudatus võimaldab plaani lõppkuupäeva värskendada (pikendatud või aegunud) pärast plaani salvestamist.</span><span class="sxs-lookup"><span data-stu-id="76b36-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="76b36-125">Plaane saab algus- ja kuupäevadest sõltumatult siiski aktiveerida või inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="76b36-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="76b36-126">Palgateave on saadaval, kui on määratud palgaarvestuse administraatori turberoll</span><span class="sxs-lookup"><span data-stu-id="76b36-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="76b36-127">Palgaarvestuse administraatori rolli on värskendatud juurdepääsuga palgateabele taotlusprotsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="76b36-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="76b36-128">Töövõtja iseteenindus | Ametikohahierarhia süvitsiminek paanilt emasõlme toomiseks nurjub</span><span class="sxs-lookup"><span data-stu-id="76b36-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="76b36-129">Tehtud on muudatused kõrvaldamaks tõrge, mis ilmneb ametikohtade hierarhia lisamisel uutesse tööruumidesse ja organisatsiooni struktuuris navigeerimisel.</span><span class="sxs-lookup"><span data-stu-id="76b36-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="76b36-130">Uus valideerimisteade, kui personalinumbrite seeria on kasutusel</span><span class="sxs-lookup"><span data-stu-id="76b36-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="76b36-131">Tehtud on muudatus selgitamaks probleemi, mis ilmneb, kui palkate töövõtja ja järgmine personalinumber on kasutusel.</span><span class="sxs-lookup"><span data-stu-id="76b36-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="76b36-132">Esmase käivituslehena on valitud töövõtja iseteeninduse tööruum</span><span class="sxs-lookup"><span data-stu-id="76b36-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="76b36-133">Kui kasutaja esmase käivituslehena on valitud tööruum **Töötaja iseteenindus** ja kasutajale ei ole töövõtja rolli määratud, suunab süsteem ta edasi vaikearmatuurlauale.</span><span class="sxs-lookup"><span data-stu-id="76b36-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="76b36-134">Lõpetamise põhjusekood värskendab ametikoha määramise kirjet</span><span class="sxs-lookup"><span data-stu-id="76b36-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="76b36-135">Lõpetamise põhjusekood värskendab nüüd ametikoha määramist töövõtjaga töösuhte lõpetamisel ja ametikoha sulgemisel.</span><span class="sxs-lookup"><span data-stu-id="76b36-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
