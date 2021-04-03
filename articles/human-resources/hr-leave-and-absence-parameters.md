---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: Määratlege rakenduses Dynamics 365 Human Resources puhkuste ja puudumiste inimressursside parameetrid.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: db96073f0a16f1c710fbfebb2d08a1d693eab1e1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463378"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="6c649-103">Puhkuste ja puudumiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6c649-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6c649-104">Enne puhkuste ja puudumiste plaanide seadistamist rakenduses Dynamics 365 Human Resources on hea mõte kontrollida kõigi seostuvate inimressursside parameetrite sätteid, sealhulgas järgnev.</span><span class="sxs-lookup"><span data-stu-id="6c649-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="6c649-105">Puhkusetaotluste numbriseeria</span><span class="sxs-lookup"><span data-stu-id="6c649-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="6c649-106">Perekonna meditsiinialase ja puhkuseseaduse (FMLA) sätted</span><span class="sxs-lookup"><span data-stu-id="6c649-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="6c649-107">Töövõtja iseteeninduse sätted puhkuste ja puudumiste taotluste jaoks</span><span class="sxs-lookup"><span data-stu-id="6c649-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="6c649-108">Puhkuste ja puudumiste parameetrid</span><span class="sxs-lookup"><span data-stu-id="6c649-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="6c649-109">Inimressursside parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="6c649-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="6c649-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6c649-111">Jaotises **Seadistus** valige suvand **Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="6c649-112">Vahekaardil **Numbriseeriad** kontrollige suvandit **Numbriseeria kood** suvandi **Puhkusetaotluse ID** jaoks ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="6c649-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="6c649-113">See säte määrab järjestuse, mida kasutatakse puhkusetaotlustele automaatselt ID-de määramiseks.</span><span class="sxs-lookup"><span data-stu-id="6c649-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="6c649-114">Vahekaardil **FMLA** kontrollige FMLA sätteid ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="6c649-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="6c649-115">Määrake vahekaardil **Töövõtja iseteenindus**, kas haldurid saavad oma töötajate nimel sisestada puhkuste ja puudumiste taotlusi.</span><span class="sxs-lookup"><span data-stu-id="6c649-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="6c649-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6c649-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="6c649-117">Puhkuste ja puudumiste kuvamine ettevõtete lõikes on praegu eelversioonis.</span><span class="sxs-lookup"><span data-stu-id="6c649-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="6c649-118">Peate selle lubama keskkonnas **Liivakast**, et kuvada puhkuse ja puudumise suvand.</span><span class="sxs-lookup"><span data-stu-id="6c649-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="6c649-119">Lisateavet eelvaatefunktsioonide lubamise kohta vt [Funktsioonide haldus](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="6c649-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="6c649-120">Human Resourcesi ühiskasutuses parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="6c649-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="6c649-121">Lehel **Personalihaldus** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6c649-122">Jaotises **Häälestus** valige suvand **Human Resourcesi ühiskasutuses parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="6c649-123">Valige vahekaardil **Eeljuurdepääs** suvandi **Luba ettevõtteülene puhkuste vaade** jaoks väärtus **Jah**, et lubada puhkuste kuvamine kogu ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="6c649-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="6c649-124">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6c649-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="6c649-125">Puhkuste ja puudumiste kalendri parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="6c649-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="6c649-126">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6c649-127">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="6c649-128">Vahekaardil **Üldine** määrake järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="6c649-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="6c649-129">Määrake **Puhkuste ja puudumiste ühikuks** kas tunnid või päevad.</span><span class="sxs-lookup"><span data-stu-id="6c649-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="6c649-130">Päevade määramisel saate teha valiku **Luba pooliku päeva määratlus**, et lubada töötajatel puhkusetaotlustes valida kas päeva esimene või teine pool.</span><span class="sxs-lookup"><span data-stu-id="6c649-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="6c649-131">Valige **Töötatud kuude kehtivusaeg**, et määrata, millal viitvõlgade määrad puhkuseplaanide korral jõustuvad, kasutades töötatud kuude arvu.</span><span class="sxs-lookup"><span data-stu-id="6c649-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="6c649-132">Saldode kuvamiseks alates tänasest või viitvõlaperioodi algusest valige **Saldo arvutamine**.</span><span class="sxs-lookup"><span data-stu-id="6c649-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="6c649-133">Kui valite **Saldo alates tänasest**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="6c649-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="6c649-134">Kui valite **Saldo alates viitvõlaperioodist**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates puhkuseplaani sagedusega määratletud viitvõlaperioodist.</span><span class="sxs-lookup"><span data-stu-id="6c649-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="6c649-135">Saate seadistada pakett-töö edasikandmise aegumise algusaja.</span><span class="sxs-lookup"><span data-stu-id="6c649-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="6c649-136">Valige **Jah** suvanditele **Luba töötajatele puhkuse ostmine** ja **Luba töötajatele puhkuse müümine**.</span><span class="sxs-lookup"><span data-stu-id="6c649-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="6c649-137">Kui valite nende suvandite jaoks **Jah**, saate luua puhkuse ostu- ja müügipoliitikad ja võimaldada töövõtjatel esitada puhkuse ostu-ja müügitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="6c649-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="6c649-138">Kõnekeskuse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6c649-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="6c649-139">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6c649-140">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="6c649-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="6c649-141">Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="6c649-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="6c649-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6c649-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c649-143">Vt ka</span><span class="sxs-lookup"><span data-stu-id="6c649-143">See also</span></span>

- [<span data-ttu-id="6c649-144">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="6c649-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]