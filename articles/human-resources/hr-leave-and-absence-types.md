---
title: Puhkuste ja puudumiste tüüpide konfigureerimine
description: Seadistage puhkuse tüübid, mida töötajad saavad rakenduses Dynamics 365 Human Resources valida.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008790"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="5454b-103">Puhkuste ja puudumiste tüüpide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5454b-103">Configure leave and absence types</span></span>

<span data-ttu-id="5454b-104">Rakenduse Dynamics 365 Human Resources puhkuse tüübid määratlevad puhkuste tüübid, millest töötajal on võimalik teada anda.</span><span class="sxs-lookup"><span data-stu-id="5454b-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="5454b-105">Saate kohandada puhkuse tüüpe vastavalt teie organisatsiooni vajadustele.</span><span class="sxs-lookup"><span data-stu-id="5454b-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="5454b-106">Puhkuse tüübid hõlmavad järgmisi.</span><span class="sxs-lookup"><span data-stu-id="5454b-106">Examples of leave types include:</span></span>

- <span data-ttu-id="5454b-107">Tasustatav puhkus</span><span class="sxs-lookup"><span data-stu-id="5454b-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="5454b-108">Tasustamata puhkus</span><span class="sxs-lookup"><span data-stu-id="5454b-108">Unpaid leave</span></span>
- <span data-ttu-id="5454b-109">Tasustatav puhkus</span><span class="sxs-lookup"><span data-stu-id="5454b-109">Paid vacation</span></span>
- <span data-ttu-id="5454b-110">Haiguspuhkus</span><span class="sxs-lookup"><span data-stu-id="5454b-110">Sick leave</span></span>
- <span data-ttu-id="5454b-111">Meditsiiniline puhkus</span><span class="sxs-lookup"><span data-stu-id="5454b-111">Medical leave</span></span>
- <span data-ttu-id="5454b-112">Perekondlik puhkus</span><span class="sxs-lookup"><span data-stu-id="5454b-112">Family leave</span></span>
- <span data-ttu-id="5454b-113">Lühiajaline invaliidsus</span><span class="sxs-lookup"><span data-stu-id="5454b-113">Short-term disability</span></span>
- <span data-ttu-id="5454b-114">Lähedase kaotuse puhkus</span><span class="sxs-lookup"><span data-stu-id="5454b-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="5454b-115">Puhkuse tüübi lisamine</span><span class="sxs-lookup"><span data-stu-id="5454b-115">Add a leave type</span></span>

1. <span data-ttu-id="5454b-116">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="5454b-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="5454b-117">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste tüübid**.</span><span class="sxs-lookup"><span data-stu-id="5454b-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="5454b-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5454b-118">Select **New**.</span></span>

4. <span data-ttu-id="5454b-119">Sisestage puhkuse tüübi nimi suvandis **Tüüp**, valige töövoog suvandist **Töövoo ID** ja sisestage kirjeldus suvandisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="5454b-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="5454b-120">Jaotises **Üldine** valige suvand **Puudub**, **Plaanipärane** või **Plaaniväline** ripploendis **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="5454b-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="5454b-121">Valige tulukood ripploendist **Tulukood**.</span><span class="sxs-lookup"><span data-stu-id="5454b-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="5454b-122">Jaotises **Põhjuse kood nõutav** valige, kas soovite nõuda põhjuse koodi.</span><span class="sxs-lookup"><span data-stu-id="5454b-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="5454b-123">Kui soovite põhjuse koode nõuda, peate võib-olla need lisama.</span><span class="sxs-lookup"><span data-stu-id="5454b-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="5454b-124">Jaotises **Põhjuse koodid** valige suvand **Lisa**, valige põhjuse kood ja seejärel valige selle kõrval märkeruut **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="5454b-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="5454b-125">Jaotises **Valitud rollide juurdepääsu piiramine** valige, kas soovite juurdepääsu piirata.</span><span class="sxs-lookup"><span data-stu-id="5454b-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="5454b-126">Seejärel valige turberollid jaotises **Selle puhkuse tüübi turberollid**.</span><span class="sxs-lookup"><span data-stu-id="5454b-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="5454b-127">Turberollid määratletakse töövoos, mille valisite selles toimingus varem jaotises **Töövoo ID**.</span><span class="sxs-lookup"><span data-stu-id="5454b-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="5454b-128">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5454b-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="5454b-129">Eelvaatefunktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5454b-129">Configure preview features</span></span>

<span data-ttu-id="5454b-130">Kui olete puhkuste ja puudumiste jaoks lubanud eelvaate funktsioonid, peate konfigureerima ka nende sätted.</span><span class="sxs-lookup"><span data-stu-id="5454b-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="5454b-131">Määrake puhkuse tüübi ümardamise suvandid.</span><span class="sxs-lookup"><span data-stu-id="5454b-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="5454b-132">Valikud hõlmavad suvandeid **Puudub**, **Üles**, **Alla** ja **Lähim**.</span><span class="sxs-lookup"><span data-stu-id="5454b-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="5454b-133">Saate määrata ka puhkuse tüübi ümardamise täpsuse.</span><span class="sxs-lookup"><span data-stu-id="5454b-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="5454b-134">Määrake puhkuse tüübiks **Puhkuse parandused**.</span><span class="sxs-lookup"><span data-stu-id="5454b-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="5454b-135">Kui valite selle suvandi, kasutab rakendus Human Resources pühade arvu, mis langevate tööpäevadele, et määratleda, kuidas lisada puhkuse tüübile vaba aeg.</span><span class="sxs-lookup"><span data-stu-id="5454b-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="5454b-136">Näiteks kui jõulupüha langeb esmaspäevale, lahutab rakendus Human Resources lisandumiste töötlemisel puhkuse tüübist ühe päeva.</span><span class="sxs-lookup"><span data-stu-id="5454b-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="5454b-137">Pühad määrate tööajakalendris.</span><span class="sxs-lookup"><span data-stu-id="5454b-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="5454b-138">Lisateavet vt teemast [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="5454b-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="5454b-139">Vt ka</span><span class="sxs-lookup"><span data-stu-id="5454b-139">See also</span></span>

- [<span data-ttu-id="5454b-140">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="5454b-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="5454b-141">Puhkuse ja puudumise plaani loomine</span><span class="sxs-lookup"><span data-stu-id="5454b-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="5454b-142">Tööajakalendri loomine</span><span class="sxs-lookup"><span data-stu-id="5454b-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)