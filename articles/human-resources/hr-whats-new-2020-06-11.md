---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (11. juuni 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 6/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cba6e48899ec39fc4de6656f8151a42b8aa43261
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555191"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="a12f9-103">Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (11. juuni 2020)</span><span class="sxs-lookup"><span data-stu-id="a12f9-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="a12f9-104">Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="a12f9-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a12f9-105">Muudatused rakenduvad versioonile number 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="a12f9-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="a12f9-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="a12f9-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="a12f9-107">Sujuva töövõtjavormi tõttu ei tööta mõnikord tütarvormi sulgemise (X) nupud (442369)</span><span class="sxs-lookup"><span data-stu-id="a12f9-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="a12f9-108">Kui lubati uus **Töötaja** vorm, ei töötanud mõnikord tütarvormide sulgemise (**X**) nupp.</span><span class="sxs-lookup"><span data-stu-id="a12f9-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="a12f9-109">See probleem oli hootine.</span><span class="sxs-lookup"><span data-stu-id="a12f9-109">This problem was intermittent.</span></span> <span data-ttu-id="a12f9-110">Pärast vormi juurest lahkumist ja selle juurde naasmist oli võimalik vorm sulgeda.</span><span class="sxs-lookup"><span data-stu-id="a12f9-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="a12f9-111">Näiteks võisite valida vasakpoolsest menüüst üksuse ja liikuda tagasi **Töötaja** vormile ning seejärel selle sulgeda.</span><span class="sxs-lookup"><span data-stu-id="a12f9-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="a12f9-112">Selle nädala väljaanne lahendab selle probleemi.</span><span class="sxs-lookup"><span data-stu-id="a12f9-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="a12f9-113">Töötaja isikliku kontaktisiku üksus ei ekspordi isiklikke kontakte, millel on emaseosetüüp</span><span class="sxs-lookup"><span data-stu-id="a12f9-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="a12f9-114">Selle väljaande järel ekspordib üksus **Töötaja isikliku kontaktisik** kõiki seosetüüpe.</span><span class="sxs-lookup"><span data-stu-id="a12f9-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="a12f9-115">HcmPositionWorkerAssignmentV2Entity peaks kuuluma vaikimisi Ceridiani palgaarvestuse integreerimise paketi juurde (448506)</span><span class="sxs-lookup"><span data-stu-id="a12f9-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="a12f9-116">Selle muudatuse järel on **HcmPositionWorkerAssignmentV2Entity** saadaval Ceridiani palgaarvestuse integreerimise paketis.</span><span class="sxs-lookup"><span data-stu-id="a12f9-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="a12f9-117">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="a12f9-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="a12f9-118">Andmebaasi logimine</span><span class="sxs-lookup"><span data-stu-id="a12f9-118">Database logging</span></span>

<span data-ttu-id="a12f9-119">Andmebaasi logimise funktsioon võimaldab teil kindlaks määrata, milliseid tabeleid ja välju tuleks jälgida.</span><span class="sxs-lookup"><span data-stu-id="a12f9-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="a12f9-120">Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise.</span><span class="sxs-lookup"><span data-stu-id="a12f9-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="a12f9-121">Saate kasutada andmebaasi logimise võimalusi, et aja jooksul neid muutusi näha.</span><span class="sxs-lookup"><span data-stu-id="a12f9-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="a12f9-122">Lisateavet leiate teemast [Andmebaasi logimise konfigureerimine ja haldamine](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="a12f9-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="a12f9-123">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="a12f9-123">Human Resources application in Teams</span></span>

<span data-ttu-id="a12f9-124">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a12f9-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="a12f9-125">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="a12f9-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="a12f9-126">Lisateavet vt teemast [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="a12f9-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="a12f9-127">Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks</span><span class="sxs-lookup"><span data-stu-id="a12f9-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="a12f9-128">Välja tulevad soodustuste haldamise üksused.</span><span class="sxs-lookup"><span data-stu-id="a12f9-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="a12f9-129">DMF-üksused võimaldavad teil andmeid importida ja eksportida, et lihtsalt soodustuste haldamist konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="a12f9-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="a12f9-130">Soodustuste haldamise mall on saadaval andmete teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="a12f9-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="a12f9-131">Mall ekspordib ja impordib andmeid andmesõltuvuste arvestamiseks järjestikku.</span><span class="sxs-lookup"><span data-stu-id="a12f9-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="a12f9-132">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="a12f9-132">Buy and sell leave</span></span> 

<span data-ttu-id="a12f9-133">Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta.</span><span class="sxs-lookup"><span data-stu-id="a12f9-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="a12f9-134">Seda protsessi hallatakse sageli käsitsi.</span><span class="sxs-lookup"><span data-stu-id="a12f9-134">This process is often managed manually.</span></span> <span data-ttu-id="a12f9-135">See funktsioon muudab personaliosakonna jaoks poliitikate ja taotluste haldamise automaatseks.</span><span class="sxs-lookup"><span data-stu-id="a12f9-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="a12f9-136">See muudab puhkusehalduse protsessi sujuvamaks ja aitab kõrvaldada vigu.</span><span class="sxs-lookup"><span data-stu-id="a12f9-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="a12f9-137">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="a12f9-137">For more information, see:</span></span>

- [<span data-ttu-id="a12f9-138">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="a12f9-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="a12f9-139">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="a12f9-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="a12f9-140">Puhkuse lisandumine üksiku ettevõtte või plaani puhul</span><span class="sxs-lookup"><span data-stu-id="a12f9-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="a12f9-141">Kliendid saavad töödelda lisandumisi üksiku ettevõtte või üksiku puhkuste ja puudumiste plaani puhul.</span><span class="sxs-lookup"><span data-stu-id="a12f9-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="a12f9-142">See võimalus muudab lisandumisprotsessi selgemaks selliste klientide puhul, kellel on eri puhkuseaastad või puhkuse lisandumise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="a12f9-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="a12f9-143">Lisateavet leiate teemast [Puhkuse lisandumine ettevõtte või puhkuseplaani alusel](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="a12f9-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="a12f9-144">Eemalolekuaja taotlustele manuste lisamine</span><span class="sxs-lookup"><span data-stu-id="a12f9-144">Add attachments to time off requests</span></span>

<span data-ttu-id="a12f9-145">Manuste lisamise võimalus kinnitatud puhkusetaotlustele on praegust COVID-19 olukorda arvestades väga oluline.</span><span class="sxs-lookup"><span data-stu-id="a12f9-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="a12f9-146">Töövõtjad saavad nüüd neid manuseid lisada.</span><span class="sxs-lookup"><span data-stu-id="a12f9-146">Employees can now add these attachments.</span></span> <span data-ttu-id="a12f9-147">Samuti on neil rohkem teavet selle kohta, kuidas puhkusetaotlusi uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="a12f9-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="a12f9-148">Lisateavet leiate teemast [Olemasolevale taotlusele manuse lisamine](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="a12f9-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="a12f9-149">Lisandumise peatamisele põhjusekoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="a12f9-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="a12f9-150">Lisandumise peatamisele on lisatud põhjusekoodid.</span><span class="sxs-lookup"><span data-stu-id="a12f9-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="a12f9-151">Edasikandmise reeglid</span><span class="sxs-lookup"><span data-stu-id="a12f9-151">Carry forward rules</span></span> 

<span data-ttu-id="a12f9-152">Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="a12f9-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="a12f9-153">Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="a12f9-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="a12f9-154">Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="a12f9-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="a12f9-155">Puhkuse lisandumise peatamine kindlate puhkusetüüpide puhul</span><span class="sxs-lookup"><span data-stu-id="a12f9-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="a12f9-156">Saate luua reegli, et peatada selliste töötajate puhkuse lisandumine, kes on esitanud tasustamata puhkuse taotluse.</span><span class="sxs-lookup"><span data-stu-id="a12f9-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="a12f9-157">Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla.</span><span class="sxs-lookup"><span data-stu-id="a12f9-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="a12f9-158">Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.</span><span class="sxs-lookup"><span data-stu-id="a12f9-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="a12f9-159">DMF-üksus on saadaval lisandumise peatamiseks</span><span class="sxs-lookup"><span data-stu-id="a12f9-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="a12f9-160">Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.</span><span class="sxs-lookup"><span data-stu-id="a12f9-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="a12f9-161">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="a12f9-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="a12f9-162">Uued platvormi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="a12f9-162">New platform capabilities</span></span> 

<span data-ttu-id="a12f9-163">Saate muuta väljad kohustuslikuks isikupärastamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="a12f9-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="a12f9-164">Selle funktsiooni jaoks peate lubama **Salvestatud vaated**.</span><span class="sxs-lookup"><span data-stu-id="a12f9-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="a12f9-165">Töövõtja iseteeninduse nime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a12f9-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="a12f9-166">Rakenduse Human Resources parameetrites on saadaval uus suvand, et muuta töövõtja iseteeninduse tööruumi nimi iseteeninduseks.</span><span class="sxs-lookup"><span data-stu-id="a12f9-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="a12f9-167">Vt ka</span><span class="sxs-lookup"><span data-stu-id="a12f9-167">See also</span></span>

[<span data-ttu-id="a12f9-168">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="a12f9-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="a12f9-169">Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="a12f9-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="a12f9-170">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="a12f9-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="a12f9-171">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="a12f9-171">Manage features</span></span>](hr-admin-manage-features.md)