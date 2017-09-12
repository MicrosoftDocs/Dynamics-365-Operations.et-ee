---
title: "Hüvitusplaanid"
description: "Hüvitise ja eeliste haldurid saavad kasutada hüvituste haldust, et hallata ning töödelda organisatsiooni töötajate fikseeritud ja ergutussüsteemi plaane."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 5a24ccf124d1f3a078fe98b90301597f70bc41c4
ms.contentlocale: et-ee
ms.lasthandoff: 06/29/2017


---

# <a name="compensation-plans"></a><span data-ttu-id="74a81-103">Hüvitusplaanid</span><span class="sxs-lookup"><span data-stu-id="74a81-103">Compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="74a81-104">Hüvitise ja eeliste haldurid saavad kasutada hüvituste haldust, et hallata ning töödelda organisatsiooni töötajate fikseeritud ja ergutussüsteemi plaane.</span><span class="sxs-lookup"><span data-stu-id="74a81-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="74a81-105">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="74a81-105">Introduction</span></span>

<span data-ttu-id="74a81-106">Tasuhaldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="74a81-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="74a81-107">Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="74a81-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="74a81-108">Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="74a81-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="74a81-109">Töötajaid saab registreerida ühes või mitmes mõlemat tüüpi plaanis.</span><span class="sxs-lookup"><span data-stu-id="74a81-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="74a81-110">Töötaja peab vastama järgmistele nõuetele, et tal oleks õigus tasuplaanis registreeruda.</span><span class="sxs-lookup"><span data-stu-id="74a81-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="74a81-111">Töötaja peab olema määratud aktiivsele ametikohale.</span><span class="sxs-lookup"><span data-stu-id="74a81-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="74a81-112">Töötaja peab vastama tasuplaani sobivusreeglitega määratletud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="74a81-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="74a81-113"> Tasu seadistamine</span><span class="sxs-lookup"><span data-stu-id="74a81-113">Compensation setup</span></span>
<span data-ttu-id="74a81-114">Järgmises tabelis on tasuprotsessi komponendid, mis võivad kuuluda teie ettevõtte tasuplaanide seadistusse.</span><span class="sxs-lookup"><span data-stu-id="74a81-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="74a81-115">Komponent</span><span class="sxs-lookup"><span data-stu-id="74a81-115">Component</span></span></th>
<th><span data-ttu-id="74a81-116">Lisateave ...</span><span class="sxs-lookup"><span data-stu-id="74a81-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74a81-117">Põhipalga tegevused</span><span class="sxs-lookup"><span data-stu-id="74a81-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="74a81-118">Põhipalga toimingutel on kaks eesmärki.</span><span class="sxs-lookup"><span data-stu-id="74a81-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="74a81-119">Tegevused võivad määrata teabe liigi, mida tuleb salvestada, kui töötaja tasu muutub.</span><span class="sxs-lookup"><span data-stu-id="74a81-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="74a81-120">Näiteks võite nõuda, et salvestatakse muudatuse põhjus (nt edutamine või madalamale ametikohale viimine).</span><span class="sxs-lookup"><span data-stu-id="74a81-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="74a81-121">Tegevused saavad tagada arvutuse rakendamise põhipalga plaanide töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="74a81-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="74a81-122">Näiteks võrdlevad tegevused, mille tüüp on Omakapital, töötajate palka töötaja taseme minimaalse võrdluspunktiga ja tagavad, et töötajale makstakse vähemalt miinimum.</span><span class="sxs-lookup"><span data-stu-id="74a81-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee's and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-123">Tasemed</span><span class="sxs-lookup"><span data-stu-id="74a81-123">Levels</span></span></td>
<td><span data-ttu-id="74a81-124">Tasemed seostatakse töödega ning kõigi töö viitega seotud ametikohtadega.</span><span class="sxs-lookup"><span data-stu-id="74a81-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="74a81-125">Saate luua diskreetseid tasemeid kolme tüüpi tasuplaanidele: klass, astmik ja etapp.</span><span class="sxs-lookup"><span data-stu-id="74a81-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74a81-126">Palgavahemiku kasutusastme maatriks</span><span class="sxs-lookup"><span data-stu-id="74a81-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="74a81-127">Vahemiku kasutusmaatriks aitab viia töötajaid üle nende töö kontrollpunkti.</span><span class="sxs-lookup"><span data-stu-id="74a81-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="74a81-128">Vahemiku kasutust saate kasutada ka ettevõttesiseste tasumäärade õigluse kontrollimiseks, pööramata tähelepanu töötaja individuaalsetele tulemustele või ettevõtte üldistele tulemustele.</span><span class="sxs-lookup"><span data-stu-id="74a81-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee's performance or the overall performance of the company.</span></span> <span data-ttu-id="74a81-129">Näiteks oma vahemikus väiksemapalgalised töötajad saavad kõrgema protsendiga palgatõuse, kui selles vahemikus suuremapalgalised töötajad.</span><span class="sxs-lookup"><span data-stu-id="74a81-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="74a81-130">Sel viisil saate tasakaalustada süstemaatiliselt omakapitali erinevusi.</span><span class="sxs-lookup"><span data-stu-id="74a81-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="74a81-131">Vahemikukasutus arvutatakse järgmiselt: (fikseeritud palgamäär – vahemiku miinimum) ÷ (vahemiku maksimum – vahemiku miinimum).</span><span class="sxs-lookup"><span data-stu-id="74a81-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-132">Viitepunktide seadistus</span><span class="sxs-lookup"><span data-stu-id="74a81-132">Reference point setups</span></span></td>
<td><span data-ttu-id="74a81-133">Viitepunkti seadistus hõlmab viitepunktide komplekti, mis kajastavad tasumäära maatriksi vahemikke.</span><span class="sxs-lookup"><span data-stu-id="74a81-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="74a81-134">Iga vahemikku saab seostada tasumääraga.</span><span class="sxs-lookup"><span data-stu-id="74a81-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="74a81-135">Näiteks on klassiplaanide viitepunktid sageli miinimum, keskpunkt ja maksimum.</span><span class="sxs-lookup"><span data-stu-id="74a81-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74a81-136">Tasumaatriks</span><span class="sxs-lookup"><span data-stu-id="74a81-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="74a81-137">Tasumaatriks on viitepunktide ja tasemete kogum, mida kasutatakse tasustruktuuri loomiseks.</span><span class="sxs-lookup"><span data-stu-id="74a81-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-138">Kompensatsiooni struktuur</span><span class="sxs-lookup"><span data-stu-id="74a81-138">Compensation structure</span></span></td>
<td><span data-ttu-id="74a81-139">Tasustruktuur on tasumaatriks, mille tasumäärad on seotud iga taseme viitepunktidega.</span><span class="sxs-lookup"><span data-stu-id="74a81-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74a81-140">Sobivuse reeglid</span><span class="sxs-lookup"><span data-stu-id="74a81-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="74a81-141">Sobivusreegleid kasutatakse konkreetsete tasuplaanidega kaetud tööde, tööfunktsioonide, töö tüüpide, osakondade, ametiühingute või tasupiirkondadega seotud töötajate tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="74a81-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="74a81-142">Sobivusreeglid tuleb luua nii ergutussüsteemi kui ka põhipalga plaanide jaoks, et töötajaid plaani registreerida.</span><span class="sxs-lookup"><span data-stu-id="74a81-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="74a81-143">Kui tasuplaani sobivusreeglid on määratud, saab määratleda tasemed, mida tuleb plaaniga hõlmatud tööde puhul rakendada.</span><span class="sxs-lookup"><span data-stu-id="74a81-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-144">Tasusagedused</span><span class="sxs-lookup"><span data-stu-id="74a81-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="74a81-145">Maksmise sagedusi kasutatakse ajaperioodi määratlemiseks, millele tasu on määratud.</span><span class="sxs-lookup"><span data-stu-id="74a81-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="74a81-146">Näiteks aitab maksmise sagedus aru saada, kas tasusumma on määratud iga-aastase palgana või tunnitasu määrana.</span><span class="sxs-lookup"><span data-stu-id="74a81-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="74a81-147">Maksmise sagedust kasutatakse ka teisendustegurite seadistamiseks, et teisendada kuu, nädala, kahe nädala ja tunni tasusummad iga-aastaseks maksesageduseks.</span><span class="sxs-lookup"><span data-stu-id="74a81-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74a81-148">Hüvitise regioonid</span><span class="sxs-lookup"><span data-stu-id="74a81-148">Compensation regions</span></span></td>
<td><span data-ttu-id="74a81-149">Tasupiirkondi kasutatakse töötaja tasu määramiseks töökoha asukoha põhjal.</span><span class="sxs-lookup"><span data-stu-id="74a81-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-150">kontrollpunkt</span><span class="sxs-lookup"><span data-stu-id="74a81-150">Control point</span></span></td>
<td><span data-ttu-id="74a81-151">Kontrollpunkt näitab, seda, mida peetakse tasu tasemel ideaalseks tasumääraks kõigi töötajate puhul.</span><span class="sxs-lookup"><span data-stu-id="74a81-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="74a81-152">Taseme plaanide struktuuride puhul on kontrollpunktid tavaliselt vahemike keskpunktid.</span><span class="sxs-lookup"><span data-stu-id="74a81-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="74a81-153">Palgaastmikuga struktuurid kasutavad kontrollpunkte harva.</span><span class="sxs-lookup"><span data-stu-id="74a81-153">Band structures rarely use control points.</span></span> <span data-ttu-id="74a81-154">Põhipalgaplaani kontrollpunkti saab määrata vormil Põhipalgaplaanid.</span><span class="sxs-lookup"><span data-stu-id="74a81-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74a81-155">Tööfunktsioonid</span><span class="sxs-lookup"><span data-stu-id="74a81-155">Job functions</span></span></td>
<td><span data-ttu-id="74a81-156">Tööfunktsioonide abil klassifitseeritakse ja filtreeritakse konkreetsete tööde tasuplaane.</span><span class="sxs-lookup"><span data-stu-id="74a81-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-157">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="74a81-157">Job types</span></span></td>
<td><span data-ttu-id="74a81-158">Töötüüpide abil klassifitseeritakse ja filtreeritakse konkreetsete tööde tasuplaane.</span><span class="sxs-lookup"><span data-stu-id="74a81-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74a81-159">Tulemustasu tüübid</span><span class="sxs-lookup"><span data-stu-id="74a81-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="74a81-160">Tulemustasu tüüpe (nt aktsiapreemia või sularahapreemia) seadistatakse mitmesuguste tasuplaanide korral.</span><span class="sxs-lookup"><span data-stu-id="74a81-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-161">Tasuruudustikud</span><span class="sxs-lookup"><span data-stu-id="74a81-161">Compensation grids</span></span></td>
<td><span data-ttu-id="74a81-162">Tasuruudustikud sisaldavad tasustruktuuri.</span><span class="sxs-lookup"><span data-stu-id="74a81-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="74a81-163">Tasuruudustikke saab kasutada ühes või mitmes tasuplaanis.</span><span class="sxs-lookup"><span data-stu-id="74a81-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74a81-164">Jõudlusplaanid</span><span class="sxs-lookup"><span data-stu-id="74a81-164">Performance plans</span></span></td>
<td><span data-ttu-id="74a81-165">Tulemusplaane kasutatakse tulemuse seostamiseks eraldamismaatriksiga, et saaksite kasutada plaani tulemustasu strateegia korral.</span><span class="sxs-lookup"><span data-stu-id="74a81-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74a81-166">Jõudluse hinnangud</span><span class="sxs-lookup"><span data-stu-id="74a81-166">Performance ratings</span></span></td>
<td><span data-ttu-id="74a81-167">Tulemuste hinnanguid kasutatakse tulemusplaanides lisatasu või tulemustasu summa määramiseks.</span><span class="sxs-lookup"><span data-stu-id="74a81-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="74a81-168">Protsessi sündmused</span><span class="sxs-lookup"><span data-stu-id="74a81-168">Process events</span></span>
<span data-ttu-id="74a81-169">Protsessisündmus arvutab tasuteabe kindlal perioodi jaoks kõigi ühte või mitmesse fikseeritud või muutuvasse tasuplaani registreerunud töötajate puhul.</span><span class="sxs-lookup"><span data-stu-id="74a81-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="74a81-170">Saate protsessisündmust käivitada korduvalt kalkuleeritud tasutulemuste testimiseks või uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="74a81-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="74a81-171">Kompensatsiooni sündmused</span><span class="sxs-lookup"><span data-stu-id="74a81-171">Compensation events</span></span>
-------------------

<span data-ttu-id="74a81-172">Iga kord, kui protsessisündmus käivitatakse, luuakse tasusündmus.</span><span class="sxs-lookup"><span data-stu-id="74a81-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="74a81-173">Tasusündmused sisaldavad tasuprotsessi tulemusi iga protsessisündmusesse kaasatud töötaja kohta</span><span class="sxs-lookup"><span data-stu-id="74a81-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="74a81-174">Kui arvutused on õiged, saate laadida tasusündmuse, et uuendada protsessisündmusest mõjutatud töötajate tasukirjeid.</span><span class="sxs-lookup"><span data-stu-id="74a81-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="74a81-175"> Soovitused</span><span class="sxs-lookup"><span data-stu-id="74a81-175">Recommendations</span></span>
<span data-ttu-id="74a81-176">Pärast protsessisündmuse käitamist võite soovitada korrigeerimisi töötaja lisatasu või preemiasumma suurendamiseks, tuginedes protsessisündmuse arvutatud juhistele.</span><span class="sxs-lookup"><span data-stu-id="74a81-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="74a81-177">Töötajate kohta soovituste edastamiseks tuleb tasuplaanide või protsessisündmuse seadistamisel soovitused lubada.</span><span class="sxs-lookup"><span data-stu-id="74a81-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>




