---
title: Aja ja kohaloleku haldus rakenduses Retail
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Commerce aja ja kohaloleku halduse puhul toetatud stsenaariume.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cca5e3232450e75f931a621b278c134129fc745c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411792"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="ffdd8-103">Aja ja kohaloleku haldus rakenduses Retail</span><span class="sxs-lookup"><span data-stu-id="ffdd8-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ffdd8-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Commerce aja ja kohaloleku halduse puhul toetatud stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="ffdd8-105">Töötaja seadistus ja tööaeg</span><span class="sxs-lookup"><span data-stu-id="ffdd8-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="ffdd8-106"> Algne konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="ffdd8-106">Initial configuration</span></span>

- <span data-ttu-id="ffdd8-107">Käitage konfiguratsiooniviisardit.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="ffdd8-108">Registreerige töötajad aja registreerimisega töötajatena.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="ffdd8-109">Töötaja graafikute planeerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-109">Plan worker schedules</span></span>

- <span data-ttu-id="ffdd8-110">Rakendage tööplaanija abil reeglid.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="ffdd8-111">Lisateavet tööde loendite kasutamise kohta vt teemast [Tööplaneerija profiilide rakendamine](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="ffdd8-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="ffdd8-112">Konfiguratsiooni sammude kohta leiate teemast [Aja ja kohaloleku seadistamine](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="ffdd8-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="ffdd8-113">Kaubandusele spetsiifiline konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="ffdd8-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="ffdd8-114">Lubage funktsiooniprofiili Kell töötajate, kellele soovite aja registreerimist lubada.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="ffdd8-115">Klõpsake valikuid **Kassa funktsiooniprofiilid** &gt; **Funktsioonid** &gt; **Kassa ajaregistreerimised** &gt; **Luba aja registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="ffdd8-116">Konfigureerige kassa (POS) õiguste gruppe, et kuvada Kellaaja kirjete vaatamisõigused.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="ffdd8-117">See luba võimaldab kasutajal vaadata kaupluse teiste töötajate (ja mistahes teise kaupluse töötajate, millega kasutaja aadressiraamatus seostatud on) aja registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="ffdd8-118">Võite ehk tahta anda seda luba juhataja rollile, kuid mitte kassapidaja rollile.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="ffdd8-119">Klõpsake valikut **Kassa loagrupid** &gt; **Kellaaja kirjete vaatamine**.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="ffdd8-120">Registreerimise aeg</span><span class="sxs-lookup"><span data-stu-id="ffdd8-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="ffdd8-121">Kassa ja kassavälise aja registreerimised</span><span class="sxs-lookup"><span data-stu-id="ffdd8-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="ffdd8-122">Kassas</span><span class="sxs-lookup"><span data-stu-id="ffdd8-122">On POS:</span></span>

    - <span data-ttu-id="ffdd8-123">Sisseregistreerimise toimingud:</span><span class="sxs-lookup"><span data-stu-id="ffdd8-123">Clock-in operations:</span></span>

        - <span data-ttu-id="ffdd8-124">logige sisse kassavälise toiminguga või uue vahetusega;</span><span class="sxs-lookup"><span data-stu-id="ffdd8-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="ffdd8-125">valige kellaaja toiming;</span><span class="sxs-lookup"><span data-stu-id="ffdd8-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="ffdd8-126">valige soovitud toiming:</span><span class="sxs-lookup"><span data-stu-id="ffdd8-126">Select a desired operation:</span></span>

            - <span data-ttu-id="ffdd8-127">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-127">Clock-in</span></span>
            - <span data-ttu-id="ffdd8-128">tööpaus,</span><span class="sxs-lookup"><span data-stu-id="ffdd8-128">Break for Work</span></span>
            - <span data-ttu-id="ffdd8-129">Lõunapaus</span><span class="sxs-lookup"><span data-stu-id="ffdd8-129">Break for Lunch</span></span>
            - <span data-ttu-id="ffdd8-130">Väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="ffdd8-131">Praegune olek</span><span class="sxs-lookup"><span data-stu-id="ffdd8-131">Current state</span></span></th>
        <th><span data-ttu-id="ffdd8-132">Saadavalolevad toimingud</span><span class="sxs-lookup"><span data-stu-id="ffdd8-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="ffdd8-133">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="ffdd8-134">tööpaus,</span><span class="sxs-lookup"><span data-stu-id="ffdd8-134">Break for Work</span></span></li>
        <li><span data-ttu-id="ffdd8-135">Lõunapaus</span><span class="sxs-lookup"><span data-stu-id="ffdd8-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="ffdd8-136">Väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="ffdd8-137">tööpaus,</span><span class="sxs-lookup"><span data-stu-id="ffdd8-137">Break for Work</span></span></td>
        <td><span data-ttu-id="ffdd8-138">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="ffdd8-139">Lõunapaus</span><span class="sxs-lookup"><span data-stu-id="ffdd8-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="ffdd8-140">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="ffdd8-141">Väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-141">Clock-out</span></span></td>
        <td><span data-ttu-id="ffdd8-142">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="ffdd8-143">[![Kellaaeg kella järgi](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="ffdd8-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="ffdd8-144">Vaadake kinnitusteadet ja kontrollige, kas praeguse toimingu kellaaeg on õige.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="ffdd8-145">Logiraamat</span><span class="sxs-lookup"><span data-stu-id="ffdd8-145">Logbook:</span></span>

    - <span data-ttu-id="ffdd8-146">Klõpsake kellaaja tegevuste vaatamiseks valikut **Logiraamat**.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="ffdd8-147">Muude kellaaja akende valimiseks kasutage ajafiltreid.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="ffdd8-148">Kui töötate mitmes kaupluses, näete kõiki oma aja registreerimisi kõigis kauplustes, kus olete aja registreerinud.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="ffdd8-149">Valitud kaupluse ajaregistreerimiste vaatamiseks kasutage kaupluse filtrit.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="ffdd8-150">Erinevad ajavööndid</span><span class="sxs-lookup"><span data-stu-id="ffdd8-150">Different time zones:</span></span>

    - <span data-ttu-id="ffdd8-151">Kui vaatate aega mõnest teisest kohast (kassapidaja puhul logiraamatust või juhi stsenaariumi puhul valikut **Kellaaja kirjete vaatamine** kasutades) ja see koht on teises ajavööndis, on vaadeldavad kellaaja kirjed teisendatud teie kohalikku ajavööndisse.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="ffdd8-152">Näiteks olete kahe kaupluse juhataja, üks neist asub Arizonas ja teine Nevadas.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="ffdd8-153">Kassapidaja Arizonas registreerib sisse kell 9.00</span><span class="sxs-lookup"><span data-stu-id="ffdd8-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="ffdd8-154">.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-154">in Arizona.</span></span> <span data-ttu-id="ffdd8-155">Sel ajal on kell Nevadas 8.00.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="ffdd8-156">Seega, kui olete Nevada kaupluses ja vaatate registreerimiskirjeid, on registreerimise ajaks märgitud kell 8.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="ffdd8-157">Töötaja aja registreerimise kuvamine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="ffdd8-158">Töötaja ajaregistreerimiste vaatamine ning kaupluse või tegevuse tüübi filtreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="ffdd8-159">Kassas:</span><span class="sxs-lookup"><span data-stu-id="ffdd8-159">On POS:</span></span>

- <span data-ttu-id="ffdd8-160">valige **Kellaaja kirjete vaatamine**;</span><span class="sxs-lookup"><span data-stu-id="ffdd8-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="ffdd8-161">kuvatakse kõikide teiega samasse kauplusesse määratud töötajate ajaregistreerimise tegevused;</span><span class="sxs-lookup"><span data-stu-id="ffdd8-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="ffdd8-162">ajaregistreerimiste filtreerimiseks saate kasutada tegevuse tüübi ja kaupluse filtreid.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="ffdd8-163">Aja registreerimiste töötlemine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-163">Process and manage time registrations</span></span>

<span data-ttu-id="ffdd8-164">Commerce’i kasutaja jälgib töövoogu ajaregistreerimiste arvutamiseks, kinnitamiseks ja palgaarvestusse ülekandmiseks.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="ffdd8-165">Esmased toimingud</span><span class="sxs-lookup"><span data-stu-id="ffdd8-165">Primary operations</span></span>

- <span data-ttu-id="ffdd8-166">Arvuta</span><span class="sxs-lookup"><span data-stu-id="ffdd8-166">Calculate</span></span>
- <span data-ttu-id="ffdd8-167">Kinnita</span><span class="sxs-lookup"><span data-stu-id="ffdd8-167">Approve</span></span>
- <span data-ttu-id="ffdd8-168">Esita palgaarvestuseks</span><span class="sxs-lookup"><span data-stu-id="ffdd8-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="ffdd8-169">Muud tavapärased toimingud</span><span class="sxs-lookup"><span data-stu-id="ffdd8-169">Other common operations</span></span>

- <span data-ttu-id="ffdd8-170">Hulgiväljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-170">Bulk Clock-out</span></span>
- <span data-ttu-id="ffdd8-171">Puudumise registreerimine</span><span class="sxs-lookup"><span data-stu-id="ffdd8-171">Register Absence</span></span>

<span data-ttu-id="ffdd8-172">Protsessi aja ja kohaloleku registreerimised kohta lisateabe saamiseks vt [Protsessiaja ja kohaloleku registreerimine](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="ffdd8-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
