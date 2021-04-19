---
title: Ohutuspiirid
description: Selles teemas kirjeldatakse, kuidas saab kasutada ohutuspiire Microsoft Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmooduliga.
author: ChristianRytt
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b66951b9c742af4aa11f681af8f9583a2d97d8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841859"
---
# <a name="safety-margins"></a><span data-ttu-id="13e85-103">Ohutuspiirid</span><span class="sxs-lookup"><span data-stu-id="13e85-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13e85-104">Selles teemas kirjeldatakse, kuidas saab kasutada ohutuspiire Microsoft Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="13e85-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="13e85-105">Ohutuspiiride ülevaade</span><span class="sxs-lookup"><span data-stu-id="13e85-105">Safety margins overview</span></span>

<span data-ttu-id="13e85-106">Ohutuspiiride eesmärk on lubada seadistus, mis annab tavalisele täitmisajale lisaks veidi rohkem puhveraega.</span><span class="sxs-lookup"><span data-stu-id="13e85-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="13e85-107">Näiteks kui materjal tuleb pärast hankijalt saabumist pakendist lahti pakkida või üle vaadata, ei saa te lihtsalt lisaaega ostu täitmisajale lisada, sest see lähenemine annab tarnijale täiendava puhveraja.</span><span class="sxs-lookup"><span data-stu-id="13e85-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="13e85-108">Selles näites saab sissetuleku ohutusvaru kasutada selleks, et tarnija tarniks varem.</span><span class="sxs-lookup"><span data-stu-id="13e85-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="13e85-109">Selline lähenemine annab puhveraja, et kaupu saaks ettevõttesiseselt käsitleda.</span><span class="sxs-lookup"><span data-stu-id="13e85-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="13e85-110">Ohutuspiire on kolme tüüpi.</span><span class="sxs-lookup"><span data-stu-id="13e85-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="13e85-111">**Lisatellimuse ohutusvaru** – tarne tellimuse tegemise puhveraeg</span><span class="sxs-lookup"><span data-stu-id="13e85-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="13e85-112">**Sissetuleku ohutusvaru** – sissetuleva tarne käsitlemise puhveraeg</span><span class="sxs-lookup"><span data-stu-id="13e85-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="13e85-113">**Väljamineku ohutusvaru** – saadetiste käsitlemise puhveraeg</span><span class="sxs-lookup"><span data-stu-id="13e85-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="13e85-114">Järgmisel illustratsioonil on näidatud, kuidas need ohutuspiirid aja jooksul rakenduvad.</span><span class="sxs-lookup"><span data-stu-id="13e85-114">The following illustration shows how these safety margins apply over time.</span></span>

![Ohutuspiirid](media/safety-margins-1.png)

<span data-ttu-id="13e85-116">Kõik piirid määratletakse päevades.</span><span class="sxs-lookup"><span data-stu-id="13e85-116">All margins are defined in days.</span></span> <span data-ttu-id="13e85-117">Vaikeväärtus *0* (null) tähendab, et piire pole rakendatud.</span><span class="sxs-lookup"><span data-stu-id="13e85-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="13e85-118">Kui seadistate mitu piiri, lisatakse need kõik koondajale alates pakkumise *tellimuse kuupäevast* kuni nõudluse *vajaduse kuupäevani*.</span><span class="sxs-lookup"><span data-stu-id="13e85-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="13e85-119">Näiteks pole seadistusel täitmisaega ja kõigi kolme piiri tüübi väärtuseks on määratud üks päev.</span><span class="sxs-lookup"><span data-stu-id="13e85-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="13e85-120">Sel juhul on tarne tellimuse kuupäeva ja nõudluse vajaduse kuupäeva vahel kolm päeva, seega kui tellimuse kuupäev on 1. juuli, siis on vajaduse kuupäev 4. juuli.</span><span class="sxs-lookup"><span data-stu-id="13e85-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="13e85-121">Sissetuleku ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-121">Receipt margin</span></span>

<span data-ttu-id="13e85-122">Sissetuleku ohutusvaru on kolmest ohutuspiirist tõenäoliselt kõige kasutatavam.</span><span class="sxs-lookup"><span data-stu-id="13e85-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="13e85-123">See rakendatakse *tarnekuupäevale* ja *vajaduse kuupäevast* tagasi.</span><span class="sxs-lookup"><span data-stu-id="13e85-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="13e85-124">Teisisõnu tuleks tooted kätte saada kindlaksmääratud arv ohutusvaru päevi enne nende nõudmist.</span><span class="sxs-lookup"><span data-stu-id="13e85-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="13e85-125">Järgmine illustratsioon tõstab esile sissetuleku ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="13e85-125">The following illustration highlights the receipt margin.</span></span>

![Sissetuleku ohutusvaru](media/safety-margins-2.png)

<span data-ttu-id="13e85-127">Sissetuleku ohutusvaru kasutatakse tavaliselt puhvrina, et varuda aega lao registreerimiseks või muudeks aeganõudvateks protsessideks, mida ei arvestata süsteemis üldise täitmisaja osana.</span><span class="sxs-lookup"><span data-stu-id="13e85-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="13e85-128">Ostude korral on üheks eeliseks see, et ostutellimuse *tarnekuupäev* lükatakse edasi sellele vastavalt.</span><span class="sxs-lookup"><span data-stu-id="13e85-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="13e85-129">Kui suurendate täitmisaega ohutuspiiri kasutamise aja asemel, palutakse viimasel minutil hankijal tarnida.</span><span class="sxs-lookup"><span data-stu-id="13e85-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="13e85-130">Pange tähele, et sissetuleku ohutusvaru ei muuda tarne *vajaduse kuupäeva*.</span><span class="sxs-lookup"><span data-stu-id="13e85-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="13e85-131">Seetõttu pole sissetuleku ohutusvaru nõudluse ja pakkumise vajaduse kuupäevade võrdlemisel otseselt nähtav (nt lehel **Netovajadused**).</span><span class="sxs-lookup"><span data-stu-id="13e85-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="13e85-132">Näiteks, kui sissetuleku varuks on seatud neli päeva ja ostutellimuse rida on planeeritud sissetulekuks 15. kuupäeval, siis koondplaneerimine arvutab korrigeeritud sissetuleku ajaks 19. kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="13e85-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="13e85-133">Pange tähele, et sissetuleku ohutusvaru ei rakendata, kui varuna kasutatakse vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="13e85-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="13e85-134">Eeldatakse, et kogu vaba kaubavaru on saadaval kohe, olenemata sellest, millal see tegelikult vastu võeti.</span><span class="sxs-lookup"><span data-stu-id="13e85-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="13e85-135">Lisatellimuse ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="13e85-136">**Peagi tulekul:** seda funktsiooni ei toetata hetkel planeerimise optimeerimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="13e85-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="13e85-137">Kuni seda veel ei toetata, käsitletakse kõiki väljale **Kauba täitmisajale lisatud lisatellimuse ohutusvaru** lisatud väärtusi väärtustena *0* (null).</span><span class="sxs-lookup"><span data-stu-id="13e85-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="13e85-138">Järgmine illustratsioon tõstab esile lisatellimuse ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="13e85-138">The following illustration highlights the reorder margin.</span></span>

![Lisatellimuse ohutusvaru](media/safety-margins-3.png)

<span data-ttu-id="13e85-140">Lisatellimuse ohutusvaru lisatakse koondplaneerimise käigus kõigile plaanitud tellimustele enne kauba täitmisaega.</span><span class="sxs-lookup"><span data-stu-id="13e85-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="13e85-141">Seetõttu tagab see lisaaja tarne tellimuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="13e85-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="13e85-142">Seda varu kasutatakse tavaliselt puhvrina, et tagada piisavalt aega kinnitamisprotsessideks või muudeks sisemisteks protsessideks, mis on vajalikud tarnetellimuste loomisel.</span><span class="sxs-lookup"><span data-stu-id="13e85-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="13e85-143">Lisatellimuse ohutusvaru lisatakse tarne *tellimuse kuupäeva* ja *alguskuupäeva* vahele.</span><span class="sxs-lookup"><span data-stu-id="13e85-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="13e85-144">Väljamineku ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="13e85-145">**Peagi tulekul:** seda funktsiooni ei toetata hetkel planeerimise optimeerimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="13e85-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="13e85-146">Kuni seda veel ei toetata, käsitletakse kõiki väljale **Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru** lisatud väärtusi väärtustena *0* (null).</span><span class="sxs-lookup"><span data-stu-id="13e85-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="13e85-147">Järgmine illustratsioon tõstab esile väljamineku ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="13e85-147">The following illustration highlights the issue margin.</span></span>

![Väljamineku ohutusvaru](media/safety-margins-4.png)

<span data-ttu-id="13e85-149">Väljamineku ohutusvaru arvestatakse koondplaneerimise käigus nõudluse vajaduse kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="13e85-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="13e85-150">See aitab tagada, et teil on piisavalt aega reageerimiseks ja sissetulevatele nõudlustellimuste tarnimiseks.</span><span class="sxs-lookup"><span data-stu-id="13e85-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="13e85-151">Seda ohutusvaru kasutatakse tavaliselt puhvrina, et varuda aega saadetise saatmiseks ja sellega seotud väljaminevateks laoprotsessideks.</span><span class="sxs-lookup"><span data-stu-id="13e85-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="13e85-152">Pange tähele, et väljamineku ohutusvaru rakendamisel ei ühti seotud nõudluse ja pakkumise vajaduse kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="13e85-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="13e85-153">Selle asemel erinevad nende väljamineku ohutusvarud, kuna väljamineku ohutusvaru lisatakse tarne *vajaduse kuupäeva* ja nõudluse *vajaduse kuupäeva* vahele.</span><span class="sxs-lookup"><span data-stu-id="13e85-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="13e85-154">Ohutuspiiride seadistamine</span><span class="sxs-lookup"><span data-stu-id="13e85-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="13e85-155">Ohutuspiiride sisselülitamine funktsioonihalduses</span><span class="sxs-lookup"><span data-stu-id="13e85-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="13e85-156">Enne selle funktsiooni kasutamist koos planeerimise optimeerimisega peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="13e85-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="13e85-157">Administraatorid saavad kasutada [funktsioonihalduse](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="13e85-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="13e85-158">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="13e85-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="13e85-159">**Moodul:** _Koondplaneerimine_</span><span class="sxs-lookup"><span data-stu-id="13e85-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="13e85-160">**Funktsiooni nimi:** _planeerimise optimeerimise ohutuspiirid_</span><span class="sxs-lookup"><span data-stu-id="13e85-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="13e85-161">Ohutuspiiride määratlemine</span><span class="sxs-lookup"><span data-stu-id="13e85-161">Define safety margins</span></span>

<span data-ttu-id="13e85-162">Ohutuspiirid on paindlikult seadistatud.</span><span class="sxs-lookup"><span data-stu-id="13e85-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="13e85-163">Neid saab seada nii *laovarude grupis* kui ka *koondplaanis*.</span><span class="sxs-lookup"><span data-stu-id="13e85-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="13e85-164">Oluline on mõista, et ohutuspiire lisatakse üksteise peale.</span><span class="sxs-lookup"><span data-stu-id="13e85-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="13e85-165">Näiteks laovarude grupi kahe päeva ja koondplaani kolme päeva sissetuleku ohutusvaru annab efektiivse sissetuleku ohutusvaru viieks päevaks.</span><span class="sxs-lookup"><span data-stu-id="13e85-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="13e85-166">Võimalus määrata koondplaanile ohutuspiir võib olla kasulik, kui soovite simuleerida mõne kindla plaani pikemaid täitmisaegu või määramatust igapäevast planeerimist mõjutamata.</span><span class="sxs-lookup"><span data-stu-id="13e85-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="13e85-167">Ohutusvarudega laovarude grupp</span><span class="sxs-lookup"><span data-stu-id="13e85-167">Coverage group safety margins</span></span>

<span data-ttu-id="13e85-168">Ohutusvaru rakendamiseks laovarude grupile toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="13e85-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="13e85-169">Valige **Koondplaneerimine \> Seadistus \> Laovarude grupid**.</span><span class="sxs-lookup"><span data-stu-id="13e85-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="13e85-170">Valige loendipaanil soovitud laovarude grupp.</span><span class="sxs-lookup"><span data-stu-id="13e85-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="13e85-171">Kasutage kiirkaardi **Muu** jaotises **Ohutuspiirid päevades** nõutavate ohutuspiiride (päevades) seadmiseks järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="13e85-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="13e85-172">Vajaduse kuupäevale lisatud sissetuleku ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="13e85-173">Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="13e85-174">Kauba täitmisajale lisatud lisatellimuse ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="13e85-175">Ohutusvarudega koondplaan</span><span class="sxs-lookup"><span data-stu-id="13e85-175">Master plan safety margins</span></span>

<span data-ttu-id="13e85-176">Ohutusvaru rakendamiseks koondplaanile toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="13e85-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="13e85-177">Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.</span><span class="sxs-lookup"><span data-stu-id="13e85-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="13e85-178">Valige loendipaanil soovitud koondplaan.</span><span class="sxs-lookup"><span data-stu-id="13e85-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="13e85-179">Kasutage kiirkaardil **Ohutuspiirid päevades** nõutavate ohutuspiiride (päevades) seadmiseks järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="13e85-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="13e85-180">Vajaduse kuupäevale lisatud sissetuleku ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="13e85-181">Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="13e85-182">Kauba täitmisajale lisatud lisatellimuse ohutusvaru</span><span class="sxs-lookup"><span data-stu-id="13e85-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="13e85-183">Saate määratleda, kas arvutused põhinevad kalendripäevadel või tööpäevadel</span><span class="sxs-lookup"><span data-stu-id="13e85-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="13e85-184">Saate seada kõik ohutuspiirid nii, et need arvutatakse kas kalendripäevade või tööpäevade põhjal.</span><span class="sxs-lookup"><span data-stu-id="13e85-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="13e85-185">Avage **Koondplaneerimine \> Seadistus \> Koondplaneerimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="13e85-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="13e85-186">Ohutuspiiride arvutamiseks tööpäevade põhjal seadke vahekaardi **Üldine** jaotises **Ohutuspiirid päevades** suvandi **Tööpäevad** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="13e85-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="13e85-187">Ohutuspiiride arvutamiseks kalendripäevade põhjal seadke suvandi väärtuseks *Ei*.</span><span class="sxs-lookup"><span data-stu-id="13e85-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="13e85-188">Näiteks on kalender avatud esmaspäevast reedeni ja suletud laupäevast pühapäevani.</span><span class="sxs-lookup"><span data-stu-id="13e85-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="13e85-189">Kui olemas on ühe päeva sissetuleku ohutusvaru, loob esmaspäevane vajaduse kuupäev tarnekuupäeva elmise reede jaoks, kuna laupäev ja pühapäev pole tööpäevad.</span><span class="sxs-lookup"><span data-stu-id="13e85-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="13e85-190">Tööpäevade määramiseks kasutatav kalender sõltub seadistusest ja tarne tüübist.</span><span class="sxs-lookup"><span data-stu-id="13e85-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="13e85-191">Seda saab juhtida laovarude grupi, lao- ja hankijakalendriga.</span><span class="sxs-lookup"><span data-stu-id="13e85-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="13e85-192">Kui *ladu* ei kuulu laovarude dimensiooni (teisisõnu, planeerimine põhineb ainult *saidil*), siis laokalendrit ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="13e85-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="13e85-193">Süsteem saab hallata seadistust, kus on määratletud üks või mitu kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="13e85-194">Järgmistes alamjaotistes kirjeldatakse võimalikke kombinatsioone, mida saab tulemuse juhtimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="13e85-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="13e85-195">Kestuse jaoks kasutatav kalender</span><span class="sxs-lookup"><span data-stu-id="13e85-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="13e85-196">Määratletud kalendrid juhivad tegelikku summaarset kalendripäevades täitmisaega alates tarne tellimuse kuupäevast kuni nõudluse vajaduse kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="13e85-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="13e85-197">Kasutatakse järgmist kalendri prioritiseerimist.</span><span class="sxs-lookup"><span data-stu-id="13e85-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="13e85-198">**Ostu täitmisaeg** – võetakse arvesse ainult laovarude grupi kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="13e85-199">**Sissetuleku ohutusvaru** – kasutatakse laovarude grupi kalendrit, kui see on määratletud.</span><span class="sxs-lookup"><span data-stu-id="13e85-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="13e85-200">Muul juhul kasutatakse laovarude kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="13e85-201">**Väljamineku ohutusvaru** – kasutatakse laovarude grupi kalendrit, kui see on määratletud.</span><span class="sxs-lookup"><span data-stu-id="13e85-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="13e85-202">Muul juhul kasutatakse laovarude kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="13e85-203">**Lisatellimuse ohutusvaru** – võetakse arvesse ainult laovarude grupi kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="13e85-204">Lõppkuupäeva jaoks kasutatav kalender</span><span class="sxs-lookup"><span data-stu-id="13e85-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="13e85-205">Selleks et teha kindlaks, kas planeerimismootor saab kasutada antud kuupäeva teatud kuupäeva tüübi korral, rakendatakse järgmisi reegleid.</span><span class="sxs-lookup"><span data-stu-id="13e85-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="13e85-206">**Ostu sissetuleku kuupäev** – kasutatakse hankijakalendrit, kui see on määratletud.</span><span class="sxs-lookup"><span data-stu-id="13e85-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="13e85-207">Muul juhul kasutatakse laovarude grupi kalendrit, kui see on määratletud.</span><span class="sxs-lookup"><span data-stu-id="13e85-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="13e85-208">Kui ükski neist kalendritest pole määratletud, kasutatakse laokalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="13e85-209">**Üleviimistarne kuupäev** – kasutatakse laovarude grupi kalendrit, kui see on määratletud.</span><span class="sxs-lookup"><span data-stu-id="13e85-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="13e85-210">Muul juhul kasutatakse laovarude kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="13e85-211">**Tootmise sissetuleku kuupäev** – kasutatakse laovarude grupi kalendrit, kui see on määratletud.</span><span class="sxs-lookup"><span data-stu-id="13e85-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="13e85-212">Muul juhul kasutatakse laovarude kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="13e85-213">**Nõutava väljamineku avatud kuupäev** – kasutatakse laokalendrit, kui see on määratletud.</span><span class="sxs-lookup"><span data-stu-id="13e85-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="13e85-214">Muul juhul kasutatakse laovarude grupi kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="13e85-215">**Tellimuse avatud päev** – kasutatakse laovarude grupi kalendri ja hankijakalendri kombinatsiooni (ühisosa).</span><span class="sxs-lookup"><span data-stu-id="13e85-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="13e85-216">Kuupäeva kasutamiseks peavad mõlemad kalendrid olema avatud.</span><span class="sxs-lookup"><span data-stu-id="13e85-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="13e85-217">Kui ainult üks kalendritest on määratletud, kasutatakse ainult seda kalendrit.</span><span class="sxs-lookup"><span data-stu-id="13e85-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="13e85-218">Kalendri seadistamise ülevaatlik maatriks</span><span class="sxs-lookup"><span data-stu-id="13e85-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="13e85-219">Järgmisel illustratsioonil on kujutatud maatriks, mis annab kokkuvõtlikku teavet selle kohta, milliseid kalendreid ohutuspiiride arvutamisel rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="13e85-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="13e85-220">(Valige pilt, et avada selle suure eraldusvõimega versioon.) Iga kalendritüübi asukoha näitamiseks kasutatakse järgmiseid lühendeid ja värve.</span><span class="sxs-lookup"><span data-stu-id="13e85-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="13e85-221">**Laovarude grupp (CG):** roheline</span><span class="sxs-lookup"><span data-stu-id="13e85-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="13e85-222">**Ladu (WH):** kollane</span><span class="sxs-lookup"><span data-stu-id="13e85-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="13e85-223">**Hankija (V):** sinine</span><span class="sxs-lookup"><span data-stu-id="13e85-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="13e85-224">[![Kalendri seadistamise ülevaatlik maatriks](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="13e85-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="13e85-225">Hilinemiste arvutamine</span><span class="sxs-lookup"><span data-stu-id="13e85-225">Calculating delays</span></span>

<span data-ttu-id="13e85-226">Kui süsteem määrab, kas tellimus hilineb või mitte, kaasatakse kõik kolm ohutuspiiri tüüpi.</span><span class="sxs-lookup"><span data-stu-id="13e85-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="13e85-227">Näiteks on kaubal tarneaeg üks päev ja sissetuleku ohutusvaru kolm päeva.</span><span class="sxs-lookup"><span data-stu-id="13e85-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="13e85-228">Selle kauba müügitellimus on seatud nõutavaks täna.</span><span class="sxs-lookup"><span data-stu-id="13e85-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="13e85-229">Sel juhul arvutatakse hilinemine järgmiselt: *täitmisaeg* + *sissetuleku ohutusvaru* = neli päeva.</span><span class="sxs-lookup"><span data-stu-id="13e85-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="13e85-230">Seega, kui täna on 14. august, on tarneaeg neljapäevase hilinemise tõttu 18. august.</span><span class="sxs-lookup"><span data-stu-id="13e85-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="13e85-231">Järgmisel illustratsioonil on toodud see näide.</span><span class="sxs-lookup"><span data-stu-id="13e85-231">The following illustration shows this example.</span></span>

![Hilinemise arvutamise näide](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="13e85-233">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="13e85-233">Additional resources</span></span>

[<span data-ttu-id="13e85-234">Planeerimise optimeerimisega alustamine</span><span class="sxs-lookup"><span data-stu-id="13e85-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="13e85-235">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="13e85-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]