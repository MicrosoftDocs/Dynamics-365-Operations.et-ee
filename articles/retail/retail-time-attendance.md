---
title: "Tööajaarvestus jaemüügis"
description: "Selles teemas kirjeldatakse jaemüügi aja ja kohaloleku haldamise puhul toetatud stsenaariume rakenduses Microsoft Dynamics 365 for Retail."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ebbf3c72b4c34cba95ecd2fb3ce506af393acc34
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="retail-time-and-attendance"></a><span data-ttu-id="27f8b-103">Jaemüügi aeg ja kohalviibimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-103">Retail time and attendance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="27f8b-104">Selles teemas kirjeldatakse jaemüügi aja ja kohaloleku haldamise puhul toetatud stsenaariume rakenduses Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="27f8b-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="27f8b-105">Töötaja seadistus ja tööaeg</span><span class="sxs-lookup"><span data-stu-id="27f8b-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="27f8b-106"> Algne konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="27f8b-106">Initial configuration</span></span>

-   <span data-ttu-id="27f8b-107">Käitage konfiguratsiooniviisardit.</span><span class="sxs-lookup"><span data-stu-id="27f8b-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="27f8b-108">Registreerige töötajad aja registreerimisega töötajatena.</span><span class="sxs-lookup"><span data-stu-id="27f8b-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="27f8b-109">Töötaja graafikute planeerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-109">Plan worker schedules</span></span>

-   <span data-ttu-id="27f8b-110">Rakendage tööplaanija abil reeglid.</span><span class="sxs-lookup"><span data-stu-id="27f8b-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="27f8b-111">Lisateabe saamiseks vt <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="27f8b-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="27f8b-112">Lisateavet konfiguratsioonitoimingute kohta vt <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="27f8b-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="27f8b-113">Jaemüügispetsiifiline konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="27f8b-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="27f8b-114">Lubage funktsiooniprofiili Kell töötajate, kellele soovite aja registreerimist lubada.</span><span class="sxs-lookup"><span data-stu-id="27f8b-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="27f8b-115">Klõpsake valikuid **Kassa funktsiooniprofiilid** &gt; **Funktsioonid** &gt; **Kassa ajaregistreerimised** &gt; **Luba aja registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="27f8b-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="27f8b-116">Konfigureerige kassa (POS) õiguste gruppe, et kuvada Kellaaja kirjete vaatamisõigused.</span><span class="sxs-lookup"><span data-stu-id="27f8b-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="27f8b-117">See luba võimaldab kasutajal vaadata kaupluse teiste töötajate (ja mistahes teise kaupluse töötajate, millega kasutaja aadressiraamatus seostatud on) aja registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="27f8b-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="27f8b-118">Võite ehk tahta anda seda luba juhataja rollile, kuid mitte kassapidaja rollile.</span><span class="sxs-lookup"><span data-stu-id="27f8b-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="27f8b-119">Klõpsake valikut **Kassa loagrupid** &gt; **Kellaaja kirjete vaatamine**.</span><span class="sxs-lookup"><span data-stu-id="27f8b-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="27f8b-120">Registreerimise aeg</span><span class="sxs-lookup"><span data-stu-id="27f8b-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="27f8b-121">Kassa ja kassavälise aja registreerimised</span><span class="sxs-lookup"><span data-stu-id="27f8b-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="27f8b-122">Kassas</span><span class="sxs-lookup"><span data-stu-id="27f8b-122">On POS:</span></span>
    -   <span data-ttu-id="27f8b-123">Sisseregistreerimise toimingud:</span><span class="sxs-lookup"><span data-stu-id="27f8b-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="27f8b-124">logige sisse kassavälise toiminguga või uue vahetusega;</span><span class="sxs-lookup"><span data-stu-id="27f8b-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="27f8b-125">valige kellaaja toiming;</span><span class="sxs-lookup"><span data-stu-id="27f8b-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="27f8b-126">valige soovitud toiming:</span><span class="sxs-lookup"><span data-stu-id="27f8b-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="27f8b-127">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-127">Clock-in</span></span>
            -   <span data-ttu-id="27f8b-128">tööpaus,</span><span class="sxs-lookup"><span data-stu-id="27f8b-128">Break for Work</span></span>
            -   <span data-ttu-id="27f8b-129">Lõunapaus</span><span class="sxs-lookup"><span data-stu-id="27f8b-129">Break for Lunch</span></span>
            -   <span data-ttu-id="27f8b-130">Väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="27f8b-131">Praegune olek</span><span class="sxs-lookup"><span data-stu-id="27f8b-131">Current state</span></span></th>
    <th><span data-ttu-id="27f8b-132">Saadavalolevad toimingud</span><span class="sxs-lookup"><span data-stu-id="27f8b-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="27f8b-133">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="27f8b-134">tööpaus,</span><span class="sxs-lookup"><span data-stu-id="27f8b-134">Break for Work</span></span></li>
    <li><span data-ttu-id="27f8b-135">Lõunapaus</span><span class="sxs-lookup"><span data-stu-id="27f8b-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="27f8b-136">Väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="27f8b-137">tööpaus,</span><span class="sxs-lookup"><span data-stu-id="27f8b-137">Break for Work</span></span></td>
    <td><span data-ttu-id="27f8b-138">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="27f8b-139">Lõunapaus</span><span class="sxs-lookup"><span data-stu-id="27f8b-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="27f8b-140">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="27f8b-141">Väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-141">Clock-out</span></span></td>
    <td><span data-ttu-id="27f8b-142">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="27f8b-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="27f8b-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="27f8b-144">Vaadake kinnitusteadet ja kontrollige, kas praeguse toimingu kellaaeg on õige.</span><span class="sxs-lookup"><span data-stu-id="27f8b-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="27f8b-145">Logiraamat</span><span class="sxs-lookup"><span data-stu-id="27f8b-145">Logbook:</span></span>
    -   <span data-ttu-id="27f8b-146">Klõpsake kellaaja tegevuste vaatamiseks valikut **Logiraamat**.</span><span class="sxs-lookup"><span data-stu-id="27f8b-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="27f8b-147">Muude kellaaja akende valimiseks kasutage ajafiltreid.</span><span class="sxs-lookup"><span data-stu-id="27f8b-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="27f8b-148">Kui töötate mitmes kaupluses, näete kõiki oma aja registreerimisi kõigis kauplustes, kus olete aja registreerinud.</span><span class="sxs-lookup"><span data-stu-id="27f8b-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="27f8b-149">Valitud kaupluse ajaregistreerimiste vaatamiseks kasutage kaupluse filtrit.</span><span class="sxs-lookup"><span data-stu-id="27f8b-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="27f8b-150">Erinevad ajavööndid</span><span class="sxs-lookup"><span data-stu-id="27f8b-150">Different time zones:</span></span>
    -   <span data-ttu-id="27f8b-151">Kui vaatate aega mõnest teisest kohast (kassapidaja puhul logiraamatust või juhi stsenaariumi puhul valikut **Kellaaja kirjete vaatamine** kasutades) ja see koht on teises ajavööndis, on vaadeldavad kellaaja kirjed teisendatud teie kohalikku ajavööndisse.</span><span class="sxs-lookup"><span data-stu-id="27f8b-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="27f8b-152">Näiteks olete kahe kaupluse juhataja, üks neist asub Arizonas ja teine Nevadas.</span><span class="sxs-lookup"><span data-stu-id="27f8b-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="27f8b-153">Kassapidaja Arizonas registreerib sisse kell 9.00</span><span class="sxs-lookup"><span data-stu-id="27f8b-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="27f8b-154">.</span><span class="sxs-lookup"><span data-stu-id="27f8b-154">in Arizona.</span></span> <span data-ttu-id="27f8b-155">Sel ajal on kell Nevadas 8.00.</span><span class="sxs-lookup"><span data-stu-id="27f8b-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="27f8b-156">Seega, kui olete Nevada kaupluses ja vaatate registreerimiskirjeid, on registreerimise ajaks märgitud kell 8.</span><span class="sxs-lookup"><span data-stu-id="27f8b-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="27f8b-157">Töötaja aja registreerimise kuvamine</span><span class="sxs-lookup"><span data-stu-id="27f8b-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="27f8b-158">Töötaja ajaregistreerimiste vaatamine ning kaupluse või tegevuse tüübi filtreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="27f8b-159">Kassas:</span><span class="sxs-lookup"><span data-stu-id="27f8b-159">On POS:</span></span>

-   <span data-ttu-id="27f8b-160">valige **Kellaaja kirjete vaatamine**;</span><span class="sxs-lookup"><span data-stu-id="27f8b-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="27f8b-161">kuvatakse kõikide teiega samasse kauplusesse määratud töötajate ajaregistreerimise tegevused;</span><span class="sxs-lookup"><span data-stu-id="27f8b-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="27f8b-162">ajaregistreerimiste filtreerimiseks saate kasutada tegevuse tüübi ja kaupluse filtreid.</span><span class="sxs-lookup"><span data-stu-id="27f8b-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="27f8b-163">Aja registreerimiste töötlemine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="27f8b-163">Process and manage time registrations</span></span>
<span data-ttu-id="27f8b-164">Dynamics 365 for Retaili kasutaja jälgib töövoogu ajaregistreerimiste arvutamiseks, kinnitamiseks ja palgaarvestusse ülekandmiseks.</span><span class="sxs-lookup"><span data-stu-id="27f8b-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="27f8b-165">Esmased toimingud</span><span class="sxs-lookup"><span data-stu-id="27f8b-165">Primary operations</span></span>

-   <span data-ttu-id="27f8b-166">Arvuta</span><span class="sxs-lookup"><span data-stu-id="27f8b-166">Calculate</span></span>
-   <span data-ttu-id="27f8b-167">Kinnita</span><span class="sxs-lookup"><span data-stu-id="27f8b-167">Approve</span></span>
-   <span data-ttu-id="27f8b-168">Esita palgaarvestuseks</span><span class="sxs-lookup"><span data-stu-id="27f8b-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="27f8b-169">Muud tavapärased toimingud</span><span class="sxs-lookup"><span data-stu-id="27f8b-169">Other common operations</span></span>

-   <span data-ttu-id="27f8b-170">Hulgiväljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="27f8b-171">Puudumise registreerimine</span><span class="sxs-lookup"><span data-stu-id="27f8b-171">Register Absence</span></span>

<span data-ttu-id="27f8b-172">Tööajaarvestuse kohta vt lisateavet <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="27f8b-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




