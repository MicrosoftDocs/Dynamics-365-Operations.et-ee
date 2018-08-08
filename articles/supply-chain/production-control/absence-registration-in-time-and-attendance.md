---
title: "Puudumiste registreerimine jaotises Tööajaarvestus"
description: "Teema kirjeldab, kuidas hallata puudumiste registreerimisi jaotises Tööajaarvestus."
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7ef244d5abf762bcaab426cf1cefb232383a8109
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="59c87-103">Puudumiste registreerimine jaotises Tööajaarvestus</span><span class="sxs-lookup"><span data-stu-id="59c87-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59c87-104">Selles teemas kirjeldatakse puudumise mõisteid ja selgitatakse, kuidas käsitleda puudumisi jaotises Tööajaarvestus.</span><span class="sxs-lookup"><span data-stu-id="59c87-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="59c87-105">Puudumine, mis põhineb tavapärastel töötundidel</span><span class="sxs-lookup"><span data-stu-id="59c87-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="59c87-106">Puudumiseks peetakse aega, mille jooksul töötajad tavapärase tööaja jooksul tööd ei tee.</span><span class="sxs-lookup"><span data-stu-id="59c87-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="59c87-107">Tavapärane tööaeg on määratud töötaja standardses tööajareeglis.</span><span class="sxs-lookup"><span data-stu-id="59c87-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="59c87-108">Näiteks on töötajal päevapõhine reegel, mis hõlmab sisseregistreerimist kell 07:00 ja väljaregistreerimist kell 15:00.</span><span class="sxs-lookup"><span data-stu-id="59c87-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="59c87-109">Kui töötaja registreerub sisse kell 09:00, märgitakse ta sel päeval vahemikus 07:00–09:00 puudunuks.</span><span class="sxs-lookup"><span data-stu-id="59c87-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="59c87-110">Sel juhul palutakse töötajatel sisestada puudumise põhjus.</span><span class="sxs-lookup"><span data-stu-id="59c87-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="59c87-111">Põhjuse määramiseks saavad töötajad valida puudumiskoodi.</span><span class="sxs-lookup"><span data-stu-id="59c87-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="59c87-112">Puudumiste koodid</span><span class="sxs-lookup"><span data-stu-id="59c87-112">Absence codes</span></span>

<span data-ttu-id="59c87-113">Puudumiskoodid määratlevad mitmesugust tüüpi puudumisi.</span><span class="sxs-lookup"><span data-stu-id="59c87-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="59c87-114">Puudumiskoodid määrab ettevõte.</span><span class="sxs-lookup"><span data-stu-id="59c87-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="59c87-115">Puudumiskoodidele saab rakendada mitmesuguseid reegleid.</span><span class="sxs-lookup"><span data-stu-id="59c87-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="59c87-116">Näiteks saab konfigureerida puudumiskoodi nii, et see vähendaks või suurendaks palka.</span><span class="sxs-lookup"><span data-stu-id="59c87-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="59c87-117">Näiteks määratleb ettevõte puudumiskoodi **Hilinemine**, mida töötajad kasutavad põhjuseta hilinemise puhul.</span><span class="sxs-lookup"><span data-stu-id="59c87-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="59c87-118">Ettevõte määratleb ka puudumiskoodi **Ettevõttesisene kursus**, millega töötajad märgivad ettevõttesisestel kursustel osalemisele kuluva aja.</span><span class="sxs-lookup"><span data-stu-id="59c87-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="59c87-119">Puudumiskoodid saab seadistada nii, et koodi **Hilinemine** puhul vähendatakse töötaja tasu, ent koodi **Ettevõttesisene kursus** puhul mitte.</span><span class="sxs-lookup"><span data-stu-id="59c87-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="59c87-120">Saate seadistada automaatsed puudumiskoodid.</span><span class="sxs-lookup"><span data-stu-id="59c87-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="59c87-121">Neid puudumiskoode saab kasutada töötaja aja arvutamiseks juhul, kui puudumist ei registreerita.</span><span class="sxs-lookup"><span data-stu-id="59c87-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="59c87-122">Töötaja tööajareegel määrab, kas kasutatakse standard- või paindaja puudumiskoodi.</span><span class="sxs-lookup"><span data-stu-id="59c87-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="59c87-123">Standard- ja paindaja seadistamine</span><span class="sxs-lookup"><span data-stu-id="59c87-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="59c87-124">Konfigureerige standard- ja paindaja parameetrid lehe **Tööajaarvestus** valikutega **Puudumise automaatne sisestamine** ja **Paindaja automaatne sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="59c87-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="59c87-125">Puudumistegrupid</span><span class="sxs-lookup"><span data-stu-id="59c87-125">Absence groups</span></span>

<span data-ttu-id="59c87-126">Puudumiskoodid rühmitatakse puudumisgruppidesse.</span><span class="sxs-lookup"><span data-stu-id="59c87-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="59c87-127">Puudumisgrupid võimaldavad rühmitada sarnaste omadustega puudumiskoode.</span><span class="sxs-lookup"><span data-stu-id="59c87-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="59c87-128">Näiteks võite rühmitada põhjusega puudumiste koodid või arsti juures käimise, vandekohtunikukohustuse ja lapse haigusega seotud puudumise koodid.</span><span class="sxs-lookup"><span data-stu-id="59c87-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="59c87-129">Planeeritud puudumine</span><span class="sxs-lookup"><span data-stu-id="59c87-129">Planned absence</span></span>

<span data-ttu-id="59c87-130">Kui teate, et töötaja puudub konkreetse perioodi jooksul, näiteks puhkuse tõttu, võite kasutada planeeritud puudumist.</span><span class="sxs-lookup"><span data-stu-id="59c87-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="59c87-131">Planeeritud puudumise seadistamiseks konfigureerige puudumiskood nii, et see võtaks arvesse planeeritud puudumist.</span><span class="sxs-lookup"><span data-stu-id="59c87-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="59c87-132">Kui seadistate planeeritud puudumise, ei küsita teilt puudumise perioodi ajal kasutaja registreeritud tööaja arvestamisel puudumiskoodi.</span><span class="sxs-lookup"><span data-stu-id="59c87-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="59c87-133">Planeeritud puudumise saab määratleda üksiku töötaja jaoks või määrata pakett-töö, mis võimaldab töötajate planeeritud puudumisi hulgi värskendada.</span><span class="sxs-lookup"><span data-stu-id="59c87-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="59c87-134">Planeeritud puudumise seadistamine</span><span class="sxs-lookup"><span data-stu-id="59c87-134">Set up planned absence</span></span>

1. <span data-ttu-id="59c87-135">Valige **Inimressursid** &gt; **Töötajad** &gt; **Töövõtjad** ja seejärel valige töövõtja.</span><span class="sxs-lookup"><span data-stu-id="59c87-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="59c87-136">Valige **Aeg** &gt; **Ajamäärangud** &gt; **Puudumisaja registreerimine** ja seadistage planeeritud puudumine.</span><span class="sxs-lookup"><span data-stu-id="59c87-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="59c87-137">Katkestatud plaanitud puudumine</span><span class="sxs-lookup"><span data-stu-id="59c87-137">Interrupted planned absence</span></span>

<span data-ttu-id="59c87-138">Kui rakendate planeeritud puudumise seadistamisel suvandi **Katkesta** ja töötaja logib planeeritud puudumise perioodi jooksul sisse, siis planeeritud puudumine katkestatakse.</span><span class="sxs-lookup"><span data-stu-id="59c87-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="59c87-139">Planeeritud puudumisele lisatakse märge **Katkestatud** ja see ei mõjuta tulevasi arvutusi.</span><span class="sxs-lookup"><span data-stu-id="59c87-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="59c87-140">Planeeritud puudumise katkestamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="59c87-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="59c87-141">Avage leht **Puudumisaja registreerimine**, nagu on kirjeldatud planeeritud puudumise seadistamise protseduuris.</span><span class="sxs-lookup"><span data-stu-id="59c87-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="59c87-142">Valige suvand **Katkesta**.</span><span class="sxs-lookup"><span data-stu-id="59c87-142">Select **Interrupt**.</span></span>

<span data-ttu-id="59c87-143">Suvand **Katkesta** rakendub juhul, kui aeg registreeritakse tööde juhtimise terminalis või seadmes.</span><span class="sxs-lookup"><span data-stu-id="59c87-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="59c87-144">Suvand ei kehti juhul, kui registreerimised sisestatakse arvutus- ja kinnituslehtedel või lehel **Elektrooniline kellakaart**.</span><span class="sxs-lookup"><span data-stu-id="59c87-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="59c87-145">Puudumise kasutamise näited paindreegli puhul</span><span class="sxs-lookup"><span data-stu-id="59c87-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="59c87-146">Järgmised kolm näidet selgitavad, kuidas arvutatakse puudumist paindperioode hõlmava reegli puhul.</span><span class="sxs-lookup"><span data-stu-id="59c87-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="59c87-147">Näited kasutavad järgmist reeglit.</span><span class="sxs-lookup"><span data-stu-id="59c87-147">The examples use the following profile.</span></span>

| <span data-ttu-id="59c87-148">Sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="59c87-148">Clock-in</span></span> | <span data-ttu-id="59c87-149">Standardaeg</span><span class="sxs-lookup"><span data-stu-id="59c87-149">Standard time</span></span>    | <span data-ttu-id="59c87-150">Paus</span><span class="sxs-lookup"><span data-stu-id="59c87-150">Break</span></span>             | <span data-ttu-id="59c87-151">Standardaeg</span><span class="sxs-lookup"><span data-stu-id="59c87-151">Standard time</span></span> | <span data-ttu-id="59c87-152">Paind-</span><span class="sxs-lookup"><span data-stu-id="59c87-152">Flex-</span></span>        | <span data-ttu-id="59c87-153">Väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="59c87-153">Clock-out</span></span> | <span data-ttu-id="59c87-154">Paind+</span><span class="sxs-lookup"><span data-stu-id="59c87-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="59c87-155">08:00</span><span class="sxs-lookup"><span data-stu-id="59c87-155">8 AM</span></span>     | <span data-ttu-id="59c87-156">09:00–11:30</span><span class="sxs-lookup"><span data-stu-id="59c87-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="59c87-157">11.30–12.00</span><span class="sxs-lookup"><span data-stu-id="59c87-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="59c87-158">12.00–15.00</span><span class="sxs-lookup"><span data-stu-id="59c87-158">12 PM to 3 PM</span></span> | <span data-ttu-id="59c87-159">15.00–16.00</span><span class="sxs-lookup"><span data-stu-id="59c87-159">3 PM to 4 PM</span></span> | <span data-ttu-id="59c87-160">16.00</span><span class="sxs-lookup"><span data-stu-id="59c87-160">4 PM</span></span>      | <span data-ttu-id="59c87-161">16.00–18.00</span><span class="sxs-lookup"><span data-stu-id="59c87-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="59c87-162">1. näide: väljalogimine paindaja jooksul</span><span class="sxs-lookup"><span data-stu-id="59c87-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="59c87-163">Töötaja teeb sisseregistreerimise kell 08:00 ja väljaregistreerimise kell 15:30.</span><span class="sxs-lookup"><span data-stu-id="59c87-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="59c87-164">Kuna töötaja teeb väljaregistreerimise paindaja miinusperioodi jooksul, ei arvutata sel juhul puudumist ning töötaja paindaja saldost lahutatakse pool tundi.</span><span class="sxs-lookup"><span data-stu-id="59c87-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="59c87-165">2. näide: väljalogimine standardaja jooksul</span><span class="sxs-lookup"><span data-stu-id="59c87-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="59c87-166">Töötaja teeb sisseregistreerimise kell 08:00 ja väljaregistreerimise kell 14:30.</span><span class="sxs-lookup"><span data-stu-id="59c87-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="59c87-167">Kuna töötaja teeb väljaregistreerumise standardajal, arvutatakse puudumine vahemikus 14.30–16.00 ja registreeritakse puudumisaeg 1,5 tundi.</span><span class="sxs-lookup"><span data-stu-id="59c87-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="59c87-168">Perioodi puudumiskood on nõutav.</span><span class="sxs-lookup"><span data-stu-id="59c87-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="59c87-169">3. näide: väljalogimine paindaja plussperioodi jooksul</span><span class="sxs-lookup"><span data-stu-id="59c87-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="59c87-170">Töötaja teeb sisseregistreerimise kell 08:00 ja väljaregistreerimise kell 16:30.</span><span class="sxs-lookup"><span data-stu-id="59c87-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="59c87-171">Kuna töötaja teeb väljaregistreerimise paindaja plussperioodi jooksul, ei arvutata sel juhul puudumist ning töötaja paindaja saldole lisatakse pool tundi.</span><span class="sxs-lookup"><span data-stu-id="59c87-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="59c87-172">Puudumine arvutamis- ja kinnitamisprotsessis</span><span class="sxs-lookup"><span data-stu-id="59c87-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="59c87-173">Töötaja registreeritud tööaeg tuleb arvutada ja kinnitada, enne kui selle saab tasuüksusena palgasüsteemi edastada.</span><span class="sxs-lookup"><span data-stu-id="59c87-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="59c87-174">Kinnitaja saab muuta töötaja registreeritud tööaega.</span><span class="sxs-lookup"><span data-stu-id="59c87-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="59c87-175">Kinnitaja saab isegi muuta töötaja registreeritud puudumisi.</span><span class="sxs-lookup"><span data-stu-id="59c87-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="59c87-176">Kui kinnitaja sisestab käsitsi puudumiskoodiga ajaperioodi, ei tühista tööajaarvestuse parameetrite vaikepuudumiskood selle perioodi puudumiskoodi.</span><span class="sxs-lookup"><span data-stu-id="59c87-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="59c87-177">Näiteks teeb töötaja sisseregistreerimise kell 10:00 ja valib puudumiskood, mis näitab, et ta jäi hiljaks.</span><span class="sxs-lookup"><span data-stu-id="59c87-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="59c87-178">Hiljem teavitab töötaja juhatajat sellest, et ta käis 08:00–10:00 arsti juures.</span><span class="sxs-lookup"><span data-stu-id="59c87-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="59c87-179">Arsti juures käimine ei peaks põhjustama töötaja palga vähendamist.</span><span class="sxs-lookup"><span data-stu-id="59c87-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="59c87-180">Seetõttu võib juhataja sellisel juhul kaht puudutud tundi (08:00–10:00) muuta, sisestades käsitsi puudumiskoodi, mis viitab haigusele.</span><span class="sxs-lookup"><span data-stu-id="59c87-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="59c87-181">Puudumisaja arvutamine ja kinnitamine</span><span class="sxs-lookup"><span data-stu-id="59c87-181">Calculate and approve absence</span></span>

- <span data-ttu-id="59c87-182">Valige **Tööajaarvestus** &gt; **Ülevaatamine ja kinnitamine** &gt; **Kinnitamine või arvutamine**.</span><span class="sxs-lookup"><span data-stu-id="59c87-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>

