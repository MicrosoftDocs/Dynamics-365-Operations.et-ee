---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: Määratlege rakenduses Dynamics 365 Human Resources puhkuste ja puudumiste inimressursside parameetrid.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712372"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="54a7e-103">Puhkuste ja puudumiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="54a7e-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="54a7e-104">Enne puhkuste ja puudumiste plaanide seadistamist rakenduses Dynamics 365 Human Resources on hea mõte kontrollida kõigi seostuvate inimressursside parameetrite sätteid, sealhulgas järgnev.</span><span class="sxs-lookup"><span data-stu-id="54a7e-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="54a7e-105">Puhkusetaotluste numbriseeria</span><span class="sxs-lookup"><span data-stu-id="54a7e-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="54a7e-106">Perekonna meditsiinialase ja puhkuseseaduse (FMLA) sätted</span><span class="sxs-lookup"><span data-stu-id="54a7e-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="54a7e-107">Töövõtja iseteeninduse sätted puhkuste ja puudumiste taotluste jaoks</span><span class="sxs-lookup"><span data-stu-id="54a7e-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="54a7e-108">Puhkuste ja puudumiste parameetrid</span><span class="sxs-lookup"><span data-stu-id="54a7e-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="54a7e-109">Inimressursside parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="54a7e-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="54a7e-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="54a7e-111">Jaotises **Seadistus** valige suvand**Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="54a7e-112">Vahekaardil **Numbriseeriad** kontrollige suvandit **Numbriseeria kood** suvandi **Puhkusetaotluse ID** jaoks ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="54a7e-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="54a7e-113">See säte määrab järjestuse, mida kasutatakse puhkusetaotlustele automaatselt ID-de määramiseks.</span><span class="sxs-lookup"><span data-stu-id="54a7e-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="54a7e-114">Vahekaardil **FMLA** kontrollige FMLA sätteid ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="54a7e-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="54a7e-115">Määrake vahekaardil **Töövõtja iseteenindus**, kas haldurid saavad oma töötajate nimel sisestada puhkuste ja puudumiste taotlusi.</span><span class="sxs-lookup"><span data-stu-id="54a7e-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="54a7e-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="54a7e-117">Puhkuste ja puudumiste kalendri parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="54a7e-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="54a7e-118">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="54a7e-119">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="54a7e-120">Vahekaardil **Üldine** määrake järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="54a7e-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="54a7e-121">Määrake **Puhkuste ja puudumiste ühikuks** kas tunnid või päevad.</span><span class="sxs-lookup"><span data-stu-id="54a7e-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="54a7e-122">Päevade määramisel saate teha valiku **Luba pooliku päeva määratlus**, et lubada töötajatel puhkusetaotlustes valida kas päeva esimene või teine pool.</span><span class="sxs-lookup"><span data-stu-id="54a7e-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="54a7e-123">Valige **Töötatud kuude kehtivusaeg**, et määrata, millal viitvõlgade määrad puhkuseplaanide korral jõustuvad, kasutades töötatud kuude arvu.</span><span class="sxs-lookup"><span data-stu-id="54a7e-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="54a7e-124">Saldode kuvamiseks alates tänasest või viitvõlaperioodi algusest valige **Saldo arvutamine**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="54a7e-125">Kui valite **Saldo alates tänasest**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="54a7e-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="54a7e-126">Kui valite **Saldo alates viitvõlaperioodist**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates puhkuseplaani sagedusega määratletud viitvõlaperioodist.</span><span class="sxs-lookup"><span data-stu-id="54a7e-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="54a7e-127">Saate seadistada pakett-töö edasikandmise aegumise algusaja.</span><span class="sxs-lookup"><span data-stu-id="54a7e-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="54a7e-128">Valige **Jah** suvanditele **Luba töötajatele puhkuse ostmine** ja **Luba töötajatele puhkuse müümine**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="54a7e-129">Kui valite nende suvandite jaoks **Jah**, saate luua puhkuse ostu- ja müügipoliitikad ja võimaldada töövõtjatel esitada puhkuse ostu-ja müügitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="54a7e-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="54a7e-130">Kõnekeskuse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="54a7e-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="54a7e-131">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="54a7e-132">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="54a7e-133">Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="54a7e-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="54a7e-134">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="54a7e-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="54a7e-135">Vt ka</span><span class="sxs-lookup"><span data-stu-id="54a7e-135">See also</span></span>

- [<span data-ttu-id="54a7e-136">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="54a7e-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
