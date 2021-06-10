---
title: Puhkuste ja puudumiste tüüpide konfigureerimine
description: Seadistage puhkuse tüübid, mida töötajad saavad rakenduses Dynamics 365 Human Resources valida.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 098f614da80a1e7e3e31b30cea707ecfbd5b0a70
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056608"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="54983-103">Puhkuste ja puudumiste tüüpide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="54983-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="54983-104">Rakenduse Dynamics 365 Human Resources puhkuse tüübid määratlevad puhkuste tüübid, millest töötajal on võimalik teada anda.</span><span class="sxs-lookup"><span data-stu-id="54983-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="54983-105">Saate kohandada puhkuse tüüpe vastavalt teie organisatsiooni vajadustele.</span><span class="sxs-lookup"><span data-stu-id="54983-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="54983-106">Puhkuse tüübid hõlmavad järgmisi.</span><span class="sxs-lookup"><span data-stu-id="54983-106">Examples of leave types include:</span></span>

- <span data-ttu-id="54983-107">Tasustatav puhkus</span><span class="sxs-lookup"><span data-stu-id="54983-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="54983-108">Tasustamata puhkus</span><span class="sxs-lookup"><span data-stu-id="54983-108">Unpaid leave</span></span>
- <span data-ttu-id="54983-109">Tasustatav puhkus</span><span class="sxs-lookup"><span data-stu-id="54983-109">Paid vacation</span></span>
- <span data-ttu-id="54983-110">Haiguspuhkus</span><span class="sxs-lookup"><span data-stu-id="54983-110">Sick leave</span></span>
- <span data-ttu-id="54983-111">Meditsiiniline puhkus</span><span class="sxs-lookup"><span data-stu-id="54983-111">Medical leave</span></span>
- <span data-ttu-id="54983-112">Perekondlik puhkus</span><span class="sxs-lookup"><span data-stu-id="54983-112">Family leave</span></span>
- <span data-ttu-id="54983-113">Lühiajaline invaliidsus</span><span class="sxs-lookup"><span data-stu-id="54983-113">Short-term disability</span></span>
- <span data-ttu-id="54983-114">Lähedase kaotuse puhkus</span><span class="sxs-lookup"><span data-stu-id="54983-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="54983-115">Puhkuse tüübi lisamine</span><span class="sxs-lookup"><span data-stu-id="54983-115">Add a leave type</span></span>

1. <span data-ttu-id="54983-116">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="54983-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="54983-117">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste tüübid**.</span><span class="sxs-lookup"><span data-stu-id="54983-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="54983-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="54983-118">Select **New**.</span></span>

4. <span data-ttu-id="54983-119">Sisestage puhkuse tüübi nimi suvandis **Tüüp**, valige töövoog suvandist **Töövoo ID** ja sisestage kirjeldus suvandisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="54983-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="54983-120">Jaotises **Üldine** valige suvand **Puudub**, **Plaanipärane** või **Plaaniväline** ripploendis **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="54983-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="54983-121">Valige tulukood ripploendist **Tulukood**.</span><span class="sxs-lookup"><span data-stu-id="54983-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="54983-122">Jaotises **Põhjuse kood nõutav** valige, kas soovite nõuda põhjuse koodi.</span><span class="sxs-lookup"><span data-stu-id="54983-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="54983-123">Kui soovite põhjuse koode nõuda, peate võib-olla need lisama.</span><span class="sxs-lookup"><span data-stu-id="54983-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="54983-124">Jaotises **Põhjuse koodid** valige suvand **Lisa**, valige põhjuse kood ja seejärel valige selle kõrval märkeruut **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="54983-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="54983-125">Jaotises **Valitud rollide juurdepääsu piiramine** valige, kas soovite juurdepääsu piirata.</span><span class="sxs-lookup"><span data-stu-id="54983-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="54983-126">Seejärel valige turberollid jaotises **Selle puhkuse tüübi turberollid**.</span><span class="sxs-lookup"><span data-stu-id="54983-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="54983-127">Turberollid määratletakse töövoos, mille valisite selles toimingus varem jaotises **Töövoo ID**.</span><span class="sxs-lookup"><span data-stu-id="54983-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="54983-128">Valige jaotises **Kalendri värv**, millist värvi selle puhkusetüübi puhul puhkuste ja puudumiste kalendrites kuvada.</span><span class="sxs-lookup"><span data-stu-id="54983-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="54983-129">Valige jaotises **Peatamise suhted**, kas soovite, et see puhkusetüüp peataks mõne teise puhkusetüübi või et selle puhkusetüübi peataks mõni teine puhkusetüüp.</span><span class="sxs-lookup"><span data-stu-id="54983-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="54983-130">Kui puhkusetaotlus esitatakse peatava puhkusetüübi kohta, siis luuakse peatatud puhkusetüübi kohta automaatselt puhkuse peatamise kanne.</span><span class="sxs-lookup"><span data-stu-id="54983-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="54983-131">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="54983-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="54983-132">Puhkuse tüübi reeglite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="54983-132">Configure leave type rules</span></span>

1. <span data-ttu-id="54983-133">Määrake puhkuse tüübi ümardamise suvandid.</span><span class="sxs-lookup"><span data-stu-id="54983-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="54983-134">Valikud hõlmavad suvandeid **Puudub**, **Üles**, **Alla** ja **Lähim**.</span><span class="sxs-lookup"><span data-stu-id="54983-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="54983-135">Saate määrata ka puhkuse tüübi ümardamise täpsuse.</span><span class="sxs-lookup"><span data-stu-id="54983-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="54983-136">Määrake puhkuse tüübiks **Puhkuse parandused**.</span><span class="sxs-lookup"><span data-stu-id="54983-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="54983-137">Kui valite selle suvandi, kasutab rakendus Human Resources pühade arvu, mis langevate tööpäevadele, et määratleda, kuidas lisada puhkuse tüübile vaba aeg.</span><span class="sxs-lookup"><span data-stu-id="54983-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="54983-138">Näiteks kui jõulupüha langeb esmaspäevale, lahutab rakendus Human Resources lisandumiste töötlemisel puhkuse tüübist ühe päeva.</span><span class="sxs-lookup"><span data-stu-id="54983-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="54983-139">Pühad määrate tööajakalendris.</span><span class="sxs-lookup"><span data-stu-id="54983-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="54983-140">Lisateavet vt teemast [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="54983-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="54983-141">Seadistage puhkusetüübi kohta **Ülekantav puhkusetüüp**.</span><span class="sxs-lookup"><span data-stu-id="54983-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="54983-142">Selle valiku korral kantakse ülekantavad saldod üle konkreetsele puhkusetüübile.</span><span class="sxs-lookup"><span data-stu-id="54983-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="54983-143">Samuti tuleb ülekantava puhkuse tüüp lisada puhkuse ja puudumiste plaanile.</span><span class="sxs-lookup"><span data-stu-id="54983-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="54983-144">Määratlege puhkusetüübi kohta **Aegumisreeglid**.</span><span class="sxs-lookup"><span data-stu-id="54983-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="54983-145">Selle valiku konfigureerimisel saate valida päevade või kuude üksuse ja määrata aegumise kestuse.</span><span class="sxs-lookup"><span data-stu-id="54983-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="54983-146">Samuti saate seadistada aegumisreegli kehtivuse alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="54983-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="54983-147">Jõustumiskuupäeva kasutatakse selleks, et määrata, millal puhkuse aegumist töötlev pakett-töö käivitada, või millisel kuupäeval reegel jõustub.</span><span class="sxs-lookup"><span data-stu-id="54983-147">The effective date is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="54983-148">Kui pakett-töö käivitamine on määratud, toimub aegumine ise alati puhkuse plaani alguskuupäeval.</span><span class="sxs-lookup"><span data-stu-id="54983-148">The expiration itself will always happen on the leave plan start date once the batch job is set to process.</span></span> <span data-ttu-id="54983-149">Plaani alguskuupäev võib näiteks olla 01.01.2020, kuid reegel loodi alles 01.06.2020.</span><span class="sxs-lookup"><span data-stu-id="54983-149">For example, the plan start date may be 1/1/2020, but the rule wasn't created until 6/1/2020.</span></span> <span data-ttu-id="54983-150">Kui jõustumiskuupäevaks määrata 01.06.2020, töödeldakse reegel järgmise aasta saabumisel ehk 01.01.2021.</span><span class="sxs-lookup"><span data-stu-id="54983-150">By setting the effective date to 6/1/2020, the rule will be processed on the next year boundary, so 1/1/2021.</span></span> <span data-ttu-id="54983-151">Kõik aegumiskuupäeval eksisteerivad puhkusesaldod arvatakse puhkusetüübist maha ning need kajastuvad puhkusesaldos.</span><span class="sxs-lookup"><span data-stu-id="54983-151">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
## <a name="see-also"></a><span data-ttu-id="54983-152">Vt ka</span><span class="sxs-lookup"><span data-stu-id="54983-152">See also</span></span>

- [<span data-ttu-id="54983-153">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="54983-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="54983-154">Puhkuste ja puudumiste plaani loomine</span><span class="sxs-lookup"><span data-stu-id="54983-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="54983-155">Looge töögraafik</span><span class="sxs-lookup"><span data-stu-id="54983-155">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="54983-156">Puhkuse katkestamine</span><span class="sxs-lookup"><span data-stu-id="54983-156">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
