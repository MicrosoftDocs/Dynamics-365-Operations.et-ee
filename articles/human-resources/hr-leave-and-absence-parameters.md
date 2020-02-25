---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: Määratlege rakenduses Dynamics 365 Human Resources puhkuste ja puudumiste inimressursside parameetrid.
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
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008733"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="4bf67-103">Puhkuste ja puudumiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4bf67-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="4bf67-104">Enne puhkuste ja puudumiste plaanide seadistamist rakenduses Dynamics 365 Human Resources on hea mõte kontrollida kõigi seostuvate inimressursside parameetrite sätteid, sealhulgas järgnev.</span><span class="sxs-lookup"><span data-stu-id="4bf67-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="4bf67-105">Puhkusetaotluste numbriseeria</span><span class="sxs-lookup"><span data-stu-id="4bf67-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="4bf67-106">Perekonna meditsiinialase ja puhkuseseaduse (FMLA) sätted</span><span class="sxs-lookup"><span data-stu-id="4bf67-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="4bf67-107">Töövõtja iseteeninduse sätted puhkuste ja puudumiste taotluste jaoks</span><span class="sxs-lookup"><span data-stu-id="4bf67-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="4bf67-108">Puhkuste ja puudumiste parameetrid</span><span class="sxs-lookup"><span data-stu-id="4bf67-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="4bf67-109">Inimressursside parameetrite kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="4bf67-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="4bf67-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="4bf67-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4bf67-111">Jaotises **Seadistus** valige suvand**Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4bf67-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="4bf67-112">Vahekaardil **Numbriseeriad** kontrollige suvandit **Numbriseeria kood** suvandi **Puhkusetaotluse ID** jaoks ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4bf67-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="4bf67-113">See säte määrab järjestuse, mida kasutatakse puhkusetaotlustele automaatselt ID-de määramiseks.</span><span class="sxs-lookup"><span data-stu-id="4bf67-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="4bf67-114">Vahekaardil **FMLA** kontrollige FMLA sätteid ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4bf67-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="4bf67-115">Määrake vahekaardil **Töövõtja iseteenindus**, kas haldurid saavad oma töötajate nimel sisestada puhkuste ja puudumiste taotlusi.</span><span class="sxs-lookup"><span data-stu-id="4bf67-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="4bf67-116">Vahekaardil **Puhkused ja puudumised** kontrollige sätteid ja muutke vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4bf67-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="4bf67-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4bf67-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="4bf67-118">Kõnekeskuse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4bf67-118">Configure calendar parameters</span></span>

<span data-ttu-id="4bf67-119">Kui olete eelvaatefunktsiooni Puhkuste ja puudumiste kalender lubanud, peate konfigureerima täiendavad parameetrid.</span><span class="sxs-lookup"><span data-stu-id="4bf67-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="4bf67-120">3. veebruari 2020 eelväljaandes on ainult suvand **Ootel puhkusetaotlused** lubatud.</span><span class="sxs-lookup"><span data-stu-id="4bf67-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="4bf67-121">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="4bf67-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4bf67-122">Jaotises **Seadistus** valige suvand**Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4bf67-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="4bf67-123">Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4bf67-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="4bf67-124">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4bf67-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bf67-125">Vt ka</span><span class="sxs-lookup"><span data-stu-id="4bf67-125">See also</span></span>

- [<span data-ttu-id="4bf67-126">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="4bf67-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
