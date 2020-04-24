---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: Määratlege rakenduses Dynamics 365 Human Resources puhkuste ja puudumiste inimressursside parameetrid.
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
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197977"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="18ccd-103">Puhkuste ja puudumiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="18ccd-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="18ccd-104">Enne puhkuste ja puudumiste plaanide seadistamist rakenduses Dynamics 365 Human Resources on hea mõte kontrollida kõigi seostuvate inimressursside parameetrite sätteid, sealhulgas järgnev.</span><span class="sxs-lookup"><span data-stu-id="18ccd-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="18ccd-105">Puhkusetaotluste numbriseeria</span><span class="sxs-lookup"><span data-stu-id="18ccd-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="18ccd-106">Perekonna meditsiinialase ja puhkuseseaduse (FMLA) sätted</span><span class="sxs-lookup"><span data-stu-id="18ccd-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="18ccd-107">Töövõtja iseteeninduse sätted puhkuste ja puudumiste taotluste jaoks</span><span class="sxs-lookup"><span data-stu-id="18ccd-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="18ccd-108">Puhkuste ja puudumiste parameetrid</span><span class="sxs-lookup"><span data-stu-id="18ccd-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="18ccd-109">Inimressursside parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="18ccd-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="18ccd-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="18ccd-111">Jaotises **Seadistus** valige suvand**Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="18ccd-112">Vahekaardil **Numbriseeriad** kontrollige suvandit **Numbriseeria kood** suvandi **Puhkusetaotluse ID** jaoks ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="18ccd-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="18ccd-113">See säte määrab järjestuse, mida kasutatakse puhkusetaotlustele automaatselt ID-de määramiseks.</span><span class="sxs-lookup"><span data-stu-id="18ccd-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="18ccd-114">Vahekaardil **FMLA** kontrollige FMLA sätteid ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="18ccd-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="18ccd-115">Määrake vahekaardil **Töövõtja iseteenindus**, kas haldurid saavad oma töötajate nimel sisestada puhkuste ja puudumiste taotlusi.</span><span class="sxs-lookup"><span data-stu-id="18ccd-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="18ccd-116">Vahekaardil **Puhkused ja puudumised** kontrollige sätteid ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="18ccd-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="18ccd-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-117">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="18ccd-118">Puhkuste ja puudumiste kalendri parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="18ccd-118">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="18ccd-119">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-119">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="18ccd-120">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-120">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="18ccd-121">Vahekaardil **Üldine** määrake järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="18ccd-121">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="18ccd-122">Määrake **Puhkuste ja puudumiste ühikuks** kas tunnid või päevad.</span><span class="sxs-lookup"><span data-stu-id="18ccd-122">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="18ccd-123">Päevade määramisel saate teha valiku **Luba pooliku päeva määratlus**, et lubada töötajatel puhkusetaotlustes valida kas päeva esimene või teine pool.</span><span class="sxs-lookup"><span data-stu-id="18ccd-123">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="18ccd-124">Valige **Töötatud kuude kehtivusaeg**, et määrata, millal viitvõlgade määrad puhkuseplaanide korral jõustuvad, kasutades töötatud kuude arvu.</span><span class="sxs-lookup"><span data-stu-id="18ccd-124">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="18ccd-125">Saldode kuvamiseks alates tänasest või viitvõlaperioodi algusest valige **Saldo arvutamine**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-125">Select **Balance calculation** to display balances display as of today or as of the accrual period.</span></span> <span data-ttu-id="18ccd-126">Kui valite **Saldo alates tänasest**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="18ccd-126">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="18ccd-127">Kui valite **Saldo alates viitvõlaperioodist**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates puhkuseplaani sagedusega määratletud viitvõlaperioodist.</span><span class="sxs-lookup"><span data-stu-id="18ccd-127">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

## <a name="configure-calendar-parameters"></a><span data-ttu-id="18ccd-128">Kõnekeskuse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="18ccd-128">Configure calendar parameters</span></span>

1. <span data-ttu-id="18ccd-129">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-129">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="18ccd-130">Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-130">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="18ccd-131">Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="18ccd-131">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="18ccd-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="18ccd-132">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="18ccd-133">Vt ka</span><span class="sxs-lookup"><span data-stu-id="18ccd-133">See also</span></span>

- [<span data-ttu-id="18ccd-134">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="18ccd-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
