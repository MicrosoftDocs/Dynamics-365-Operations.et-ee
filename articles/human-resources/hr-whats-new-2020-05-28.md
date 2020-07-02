---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (28. mai 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37f21fffe209e17a6fe89c2661e49fc0dc8b9655
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443460"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="5ceba-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (28. mai 2020)</span><span class="sxs-lookup"><span data-stu-id="5ceba-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="5ceba-104">Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="5ceba-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5ceba-105">Muudatused rakenduvad versioonile number 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="5ceba-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="5ceba-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="5ceba-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="5ceba-107">Üksus LeaveRequest ei tööta, kui lubate puhkuseplaani kohta mitu tüüpi (447498)</span><span class="sxs-lookup"><span data-stu-id="5ceba-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="5ceba-108">Antud muudatusega seoses on nüüd mitme puhkusetüübi lubamisel antud tõrke parandamiseks saadaval üksus **LeaveEnrollmentV2Entity**.</span><span class="sxs-lookup"><span data-stu-id="5ceba-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="5ceba-109">Partiisisalduse vähendamise funktsioon (eelvaade) (446619)</span><span class="sxs-lookup"><span data-stu-id="5ceba-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="5ceba-110">Antud funktsiooni lubamisel võite oodata partii raamistiku tabelites blokeerimise vähenemist ülesannete valimisel ja tööde lõpetamisel.</span><span class="sxs-lookup"><span data-stu-id="5ceba-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="5ceba-111">UpdateConflict takistab töötaja salvestamisel kirje redigeerimist jaotises Inimesed (427915)</span><span class="sxs-lookup"><span data-stu-id="5ceba-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="5ceba-112">See muudatus parandab tõrke, mis esineb uue töötaja lisamisel, aadressi uuendamisel ja keele-eelistuse muutmisel.</span><span class="sxs-lookup"><span data-stu-id="5ceba-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="5ceba-113">Selles ainulaadses stsenaariumis kuvatakse tõrge, mis näitab, et kirjet ei õnnestunud värskendada.</span><span class="sxs-lookup"><span data-stu-id="5ceba-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="5ceba-114">Kinnitatud puhkusetaotlusele ei saa lisada manust uuesti esitamiseks (425407)</span><span class="sxs-lookup"><span data-stu-id="5ceba-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="5ceba-115">See muudatus võimaldab nüüd lisada kinnitatud puhkusetaotlustele lisasid.</span><span class="sxs-lookup"><span data-stu-id="5ceba-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="5ceba-116">Kasutaja saab sisestada töötaja hüvituse muu juriidilise isiku vormil (409529)</span><span class="sxs-lookup"><span data-stu-id="5ceba-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="5ceba-117">See muudatus keelab hüvituse valikud, vältimaks kogemata vale juriidilise isiku jaoks hüvituse kirjete lisamist.</span><span class="sxs-lookup"><span data-stu-id="5ceba-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="5ceba-118">Tõrge töötaja ülekandmisel, kui töötaja ametikohale määramise kuupäev on enne ametikoha kestuse ajavahemikku (429402)</span><span class="sxs-lookup"><span data-stu-id="5ceba-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="5ceba-119">Antud stsenaariumis töötaja ülekandmisega seotud tõrketeateid on värskendatud, et anda paremini edasi probleemi lahendamiseks vajalikke muudatusi.</span><span class="sxs-lookup"><span data-stu-id="5ceba-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="5ceba-120">Manuse võimalus töötaja iseteeninduses soodustuste registreerimisel</span><span class="sxs-lookup"><span data-stu-id="5ceba-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="5ceba-121">Nüüd saate lisada soodustuste registreerimise protsessi käigus manuseid iga plaani kohta, millesse töötaja registreerub.</span><span class="sxs-lookup"><span data-stu-id="5ceba-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="5ceba-122">Seejärel saate manuseid kuvada vormis **Töötaja registreeritud soodustus**.</span><span class="sxs-lookup"><span data-stu-id="5ceba-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5ceba-123">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="5ceba-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="5ceba-124">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="5ceba-124">Human Resources application in Teams</span></span>

<span data-ttu-id="5ceba-125">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5ceba-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="5ceba-126">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="5ceba-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="5ceba-127">Lisateavet vt teemast [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="5ceba-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="5ceba-128">Puhkuse peatamine</span><span class="sxs-lookup"><span data-stu-id="5ceba-128">Leave suspension</span></span>

<span data-ttu-id="5ceba-129">Saate peatada töövõtja puhkuse Human Resourcesis.</span><span class="sxs-lookup"><span data-stu-id="5ceba-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="5ceba-130">Puhkuse peatamine lõpetab puhkuse viitvõlad valitud puhkusetüüpide puhul.</span><span class="sxs-lookup"><span data-stu-id="5ceba-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="5ceba-131">Kui peatamine toimub pärast viitvõla töötlemist, loob peatatav puhkus eelmääratud korrigeerimise töötaja puhkusesaldo jaoks.</span><span class="sxs-lookup"><span data-stu-id="5ceba-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="5ceba-132">Lisateabe saamiseks vt [Puhkuse peatamine](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="5ceba-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="5ceba-133">Kasutajakogemuse uuendamine viitvõla näitamiseks on peatatud (429550)</span><span class="sxs-lookup"><span data-stu-id="5ceba-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="5ceba-134">Kasutajakogemuses on nüüd näidatud, et plaani viitvõlg on peatatud.</span><span class="sxs-lookup"><span data-stu-id="5ceba-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="5ceba-135">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="5ceba-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="5ceba-136">Andmebaasi logimine (eelvaates juunis)</span><span class="sxs-lookup"><span data-stu-id="5ceba-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="5ceba-137">Andmebaasi logimise funktsioon võimaldab teil kindlaks määrata, millist tabelit ja milliseid välju tuleks jälgida.</span><span class="sxs-lookup"><span data-stu-id="5ceba-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="5ceba-138">Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise.</span><span class="sxs-lookup"><span data-stu-id="5ceba-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="5ceba-139">Muudatuste ajas muutumise nägemiseks on saadaval päringu võimalused.</span><span class="sxs-lookup"><span data-stu-id="5ceba-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="5ceba-140">Puhkuse ost ja müük (eelvaates 1. juunil)</span><span class="sxs-lookup"><span data-stu-id="5ceba-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="5ceba-141">Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta.</span><span class="sxs-lookup"><span data-stu-id="5ceba-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="5ceba-142">Seda protsessi hallatakse sageli käsitsi.</span><span class="sxs-lookup"><span data-stu-id="5ceba-142">This process is often managed manually.</span></span> <span data-ttu-id="5ceba-143">See funktsioon pakub personaliosakonnale auomaatsemat viisi poliiside ja taotluste haldamiseks ja aitab kõrvaldada vigasid, korrastades puhkusehalduse protsessi.</span><span class="sxs-lookup"><span data-stu-id="5ceba-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="5ceba-144">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="5ceba-144">For more information, see:</span></span>

- [<span data-ttu-id="5ceba-145">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="5ceba-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="5ceba-146">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="5ceba-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="5ceba-147">Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks</span><span class="sxs-lookup"><span data-stu-id="5ceba-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="5ceba-148">Välja tulevad soodustuste haldamise üksused.</span><span class="sxs-lookup"><span data-stu-id="5ceba-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="5ceba-149">DMF-üksused võimaldavad andmeid importida ja eksportida soodustuste halduse lihtsaks konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="5ceba-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="5ceba-150">Soodustuste haldamise mall on saadaval ka andmete teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="5ceba-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="5ceba-151">Mall ekspordib ja impordib andmeid järjestikusel moel vastavalt andmesõltuvustele.</span><span class="sxs-lookup"><span data-stu-id="5ceba-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="5ceba-152">Lisa viitvõlgade peatamisele põhjusekood (1. juuni)</span><span class="sxs-lookup"><span data-stu-id="5ceba-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="5ceba-153">Viitvõla peatamisele on lisatud põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="5ceba-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="5ceba-154">Edasikandmise reeglid (1. juuni)</span><span class="sxs-lookup"><span data-stu-id="5ceba-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="5ceba-155">Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="5ceba-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="5ceba-156">Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="5ceba-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="5ceba-157">Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="5ceba-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="5ceba-158">Kindlate puhkusetüüpide puhkuse viitvõla peatamine (1. juuni)</span><span class="sxs-lookup"><span data-stu-id="5ceba-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="5ceba-159">Selles väljalaskes saab inimressursside haldur luua reegli, et peatada selliste töötajate puhkuse viitvõlg, kes on esitanud tasustamata puhkuse taotluse.</span><span class="sxs-lookup"><span data-stu-id="5ceba-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="5ceba-160">Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla.</span><span class="sxs-lookup"><span data-stu-id="5ceba-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="5ceba-161">Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.</span><span class="sxs-lookup"><span data-stu-id="5ceba-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="5ceba-162">DMF-üksus on saadaval viitvõlgade peatamiseks (1. juuni)</span><span class="sxs-lookup"><span data-stu-id="5ceba-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="5ceba-163">Nüüdsest on viitvõlgade peatamiseks saadaval DMF-üksus.</span><span class="sxs-lookup"><span data-stu-id="5ceba-163">A DMF entity is now available for accrual suspensions.</span></span>