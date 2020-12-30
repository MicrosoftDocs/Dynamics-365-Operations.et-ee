---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. juuli 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 23. juuli 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0672e3039f54a4591db49eee00d69bf5e4278fd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528445"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="bddb5-103">Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. juuli 2020)</span><span class="sxs-lookup"><span data-stu-id="bddb5-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bddb5-104">Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="bddb5-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bddb5-105">Muudatused rakenduvad versioonile number 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="bddb5-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="bddb5-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="bddb5-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="bddb5-107">Finantsdimensioonide kustutamine positsioonil ei tööta ootuspäraselt (445476)</span><span class="sxs-lookup"><span data-stu-id="bddb5-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="bddb5-108">Dimensioonide eemaldamine positsioonilt eemaldab nüüd need samad positsioonid Common Data Service'ist.</span><span class="sxs-lookup"><span data-stu-id="bddb5-108">Removing dimensions from a position now removes those same positions from Common Data Service.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="bddb5-109">Positsioonide puhul, mis pole hierarhias, näidatakse passiivseid positsioone (397257)</span><span class="sxs-lookup"><span data-stu-id="bddb5-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="bddb5-110">Positsioonid, mis on passiivsed (kestus on aegunud), ei ole enam positsioonihierarhias kuvatud **positsioonidena, mis pole hierarhias**.</span><span class="sxs-lookup"><span data-stu-id="bddb5-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="bddb5-111">Üksuste LeaveEnrollmentEntity ja HcmWorkerEntity vahel toimuv kontrollimine andmehaldusraamistiku (DMF) importimisel muudab andmete laadimise aeglaseks (442324)</span><span class="sxs-lookup"><span data-stu-id="bddb5-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="bddb5-112">Selles väljalaskes tehtud muudatused suurendavad üksuse **LeaveEnrollmentEntity** jõudlust.</span><span class="sxs-lookup"><span data-stu-id="bddb5-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="bddb5-113">Organisatsioonihalduses pole võimalik isikupärastada (447490)</span><span class="sxs-lookup"><span data-stu-id="bddb5-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="bddb5-114">Selle muudatuse tõttu saate nüüd **organisatsioonihalduses** linke isikupärastada.</span><span class="sxs-lookup"><span data-stu-id="bddb5-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="bddb5-115">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="bddb5-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="bddb5-116">Kohustuslikud väljad</span><span class="sxs-lookup"><span data-stu-id="bddb5-116">Mandatory fields</span></span> 

<span data-ttu-id="bddb5-117">Saate nüüd muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil.</span><span class="sxs-lookup"><span data-stu-id="bddb5-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="bddb5-118">See funktsioon nõuab **Salvestatud vaateid**.</span><span class="sxs-lookup"><span data-stu-id="bddb5-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="bddb5-119">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="bddb5-119">Human Resources application in Teams</span></span>

<span data-ttu-id="bddb5-120">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bddb5-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="bddb5-121">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="bddb5-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="bddb5-122">Lisateavet vt teemast [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="bddb5-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="bddb5-123">Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks</span><span class="sxs-lookup"><span data-stu-id="bddb5-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="bddb5-124">Välja tulevad soodustuste haldamise üksused.</span><span class="sxs-lookup"><span data-stu-id="bddb5-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="bddb5-125">DMF-üksused võimaldavad teil andmeid importida ja eksportida, et lihtsalt soodustuste haldamist konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="bddb5-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="bddb5-126">Soodustuste haldamise mall on saadaval andmete teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="bddb5-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="bddb5-127">Mall ekspordib ja impordib andmeid andmesõltuvuste arvestamiseks järjestikku.</span><span class="sxs-lookup"><span data-stu-id="bddb5-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="bddb5-128">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="bddb5-128">Buy and sell leave</span></span> 

<span data-ttu-id="bddb5-129">Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta.</span><span class="sxs-lookup"><span data-stu-id="bddb5-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="bddb5-130">Seda protsessi hallatakse sageli käsitsi.</span><span class="sxs-lookup"><span data-stu-id="bddb5-130">This process is often managed manually.</span></span> <span data-ttu-id="bddb5-131">See funktsioon muudab personaliosakonna jaoks poliitikate ja taotluste haldamise automaatseks.</span><span class="sxs-lookup"><span data-stu-id="bddb5-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="bddb5-132">See muudab puhkusehalduse protsessi sujuvamaks ja aitab kõrvaldada vigu.</span><span class="sxs-lookup"><span data-stu-id="bddb5-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="bddb5-133">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="bddb5-133">For more information, see:</span></span>

- [<span data-ttu-id="bddb5-134">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="bddb5-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="bddb5-135">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="bddb5-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="bddb5-136">Puhkuse lisandumine üksiku ettevõtte või plaani puhul</span><span class="sxs-lookup"><span data-stu-id="bddb5-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="bddb5-137">Kliendid saavad töödelda lisandumisi üksiku ettevõtte või üksiku puhkuste ja puudumiste plaani puhul.</span><span class="sxs-lookup"><span data-stu-id="bddb5-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="bddb5-138">See võimalus muudab lisandumisprotsessi selgemaks selliste klientide puhul, kellel on eri puhkuseaastad või puhkuse lisandumise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="bddb5-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="bddb5-139">Lisateavet leiate teemast [Puhkuse lisandumine ettevõtte või puhkuseplaani alusel](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="bddb5-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="bddb5-140">Puhkusetaotlustele manuste lisamine</span><span class="sxs-lookup"><span data-stu-id="bddb5-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="bddb5-141">Manuste lisamise võimalus kinnitatud puhkusetaotlustele on praegust COVID-19 olukorda arvestades väga oluline.</span><span class="sxs-lookup"><span data-stu-id="bddb5-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="bddb5-142">Töövõtjad saavad nüüd neid manuseid lisada.</span><span class="sxs-lookup"><span data-stu-id="bddb5-142">Employees can now add these attachments.</span></span> <span data-ttu-id="bddb5-143">Samuti on neil rohkem teavet selle kohta, kuidas puhkusetaotlusi uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="bddb5-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="bddb5-144">Lisateavet leiate teemast [Olemasolevale taotlusele manuse lisamine](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="bddb5-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="bddb5-145">Lisandumise peatamisele põhjusekoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="bddb5-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="bddb5-146">Lisandumise peatamisele on lisatud põhjusekoodid.</span><span class="sxs-lookup"><span data-stu-id="bddb5-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="bddb5-147">Edasikandmise reeglid</span><span class="sxs-lookup"><span data-stu-id="bddb5-147">Carry forward rules</span></span> 

<span data-ttu-id="bddb5-148">Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="bddb5-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="bddb5-149">Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="bddb5-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="bddb5-150">Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="bddb5-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="bddb5-151">Puhkuse lisandumise peatamine kindlate puhkusetüüpide puhul</span><span class="sxs-lookup"><span data-stu-id="bddb5-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="bddb5-152">Saate luua reegli, et peatada selliste töötajate puhkuse lisandumine, kes on esitanud tasustamata puhkuse taotluse.</span><span class="sxs-lookup"><span data-stu-id="bddb5-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="bddb5-153">Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla.</span><span class="sxs-lookup"><span data-stu-id="bddb5-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="bddb5-154">Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.</span><span class="sxs-lookup"><span data-stu-id="bddb5-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="bddb5-155">DMF-üksus on saadaval lisandumise peatamiseks</span><span class="sxs-lookup"><span data-stu-id="bddb5-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="bddb5-156">Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.</span><span class="sxs-lookup"><span data-stu-id="bddb5-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="bddb5-157">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="bddb5-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="bddb5-158">Common Data Service'is kaasatud kontroll-loendi üksused</span><span class="sxs-lookup"><span data-stu-id="bddb5-158">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="bddb5-159">Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="bddb5-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="bddb5-160">Platvormi muudatused</span><span class="sxs-lookup"><span data-stu-id="bddb5-160">Platform changes</span></span>

<span data-ttu-id="bddb5-161">Platvormi värskendus 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="bddb5-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="bddb5-162">Vt ka</span><span class="sxs-lookup"><span data-stu-id="bddb5-162">See also</span></span>

[<span data-ttu-id="bddb5-163">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="bddb5-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="bddb5-164">Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="bddb5-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="bddb5-165">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="bddb5-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="bddb5-166">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="bddb5-166">Manage features</span></span>](hr-admin-manage-features.md)
