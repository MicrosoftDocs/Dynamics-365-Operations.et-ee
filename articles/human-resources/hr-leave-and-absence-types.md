---
title: Puhkuste ja puudumiste tüüpide konfigureerimine
description: Seadistage puhkuse tüübid, mida töötajad saavad rakenduses Dynamics 365 Human Resources valida.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198046"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="dd7eb-103">Puhkuste ja puudumiste tüüpide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dd7eb-103">Configure leave and absence types</span></span>

<span data-ttu-id="dd7eb-104">Rakenduse Dynamics 365 Human Resources puhkuse tüübid määratlevad puhkuste tüübid, millest töötajal on võimalik teada anda.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="dd7eb-105">Saate kohandada puhkuse tüüpe vastavalt teie organisatsiooni vajadustele.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="dd7eb-106">Puhkuse tüübid hõlmavad järgmisi.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-106">Examples of leave types include:</span></span>

- <span data-ttu-id="dd7eb-107">Tasustatav puhkus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="dd7eb-108">Tasustamata puhkus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-108">Unpaid leave</span></span>
- <span data-ttu-id="dd7eb-109">Tasustatav puhkus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-109">Paid vacation</span></span>
- <span data-ttu-id="dd7eb-110">Haiguspuhkus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-110">Sick leave</span></span>
- <span data-ttu-id="dd7eb-111">Meditsiiniline puhkus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-111">Medical leave</span></span>
- <span data-ttu-id="dd7eb-112">Perekondlik puhkus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-112">Family leave</span></span>
- <span data-ttu-id="dd7eb-113">Lühiajaline invaliidsus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-113">Short-term disability</span></span>
- <span data-ttu-id="dd7eb-114">Lähedase kaotuse puhkus</span><span class="sxs-lookup"><span data-stu-id="dd7eb-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="dd7eb-115">Puhkuse tüübi lisamine</span><span class="sxs-lookup"><span data-stu-id="dd7eb-115">Add a leave type</span></span>

1. <span data-ttu-id="dd7eb-116">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dd7eb-117">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste tüübid**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="dd7eb-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-118">Select **New**.</span></span>

4. <span data-ttu-id="dd7eb-119">Sisestage puhkuse tüübi nimi suvandis **Tüüp**, valige töövoog suvandist **Töövoo ID** ja sisestage kirjeldus suvandisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="dd7eb-120">Jaotises **Üldine** valige suvand **Puudub**, **Plaanipärane** või **Plaaniväline** ripploendis **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="dd7eb-121">Valige tulukood ripploendist **Tulukood**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="dd7eb-122">Jaotises **Põhjuse kood nõutav** valige, kas soovite nõuda põhjuse koodi.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="dd7eb-123">Kui soovite põhjuse koode nõuda, peate võib-olla need lisama.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="dd7eb-124">Jaotises **Põhjuse koodid** valige suvand **Lisa**, valige põhjuse kood ja seejärel valige selle kõrval märkeruut **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="dd7eb-125">Jaotises **Valitud rollide juurdepääsu piiramine** valige, kas soovite juurdepääsu piirata.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="dd7eb-126">Seejärel valige turberollid jaotises **Selle puhkuse tüübi turberollid**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="dd7eb-127">Turberollid määratletakse töövoos, mille valisite selles toimingus varem jaotises **Töövoo ID**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="dd7eb-128">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="dd7eb-129">Puhkuse tüübi reeglite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dd7eb-129">Configure leave type rules</span></span>

1. <span data-ttu-id="dd7eb-130">Määrake puhkuse tüübi ümardamise suvandid.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="dd7eb-131">Valikud hõlmavad suvandeid **Puudub**, **Üles**, **Alla** ja **Lähim**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="dd7eb-132">Saate määrata ka puhkuse tüübi ümardamise täpsuse.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="dd7eb-133">Määrake puhkuse tüübiks **Puhkuse parandused**.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="dd7eb-134">Kui valite selle suvandi, kasutab rakendus Human Resources pühade arvu, mis langevate tööpäevadele, et määratleda, kuidas lisada puhkuse tüübile vaba aeg.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="dd7eb-135">Näiteks kui jõulupüha langeb esmaspäevale, lahutab rakendus Human Resources lisandumiste töötlemisel puhkuse tüübist ühe päeva.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="dd7eb-136">Pühad määrate tööajakalendris.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="dd7eb-137">Lisateavet vt teemast [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="dd7eb-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="dd7eb-138">Eelvaatefunktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dd7eb-138">Configure preview features</span></span>

<span data-ttu-id="dd7eb-139">Kui olete puhkuste ja puudumiste jaoks lubanud eelvaate funktsioonid, peate konfigureerima ka nende sätted.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="dd7eb-140">Valige edasikantava summa edastamiseks puhkuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="dd7eb-141">Saate luua ka uue edasikantava puhkuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="dd7eb-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="dd7eb-142">Vt ka</span><span class="sxs-lookup"><span data-stu-id="dd7eb-142">See also</span></span>

- [<span data-ttu-id="dd7eb-143">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="dd7eb-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="dd7eb-144">Puhkuste ja puudumiste plaani loomine</span><span class="sxs-lookup"><span data-stu-id="dd7eb-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="dd7eb-145">Tööajakalendri loomine</span><span class="sxs-lookup"><span data-stu-id="dd7eb-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
