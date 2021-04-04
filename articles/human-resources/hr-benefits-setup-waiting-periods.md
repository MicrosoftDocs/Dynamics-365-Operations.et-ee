---
title: Ooteperioodide konfigureerimine
description: Rakenduses Microsoft Dynamics 365 Human Resources moodustavad ootepäevad vahe-eesmärgid, mida soodustuse plaanide jaoks kasutada.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e08c0c02393506e1e292676c954bdf3850029f7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468295"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="6842f-103">Ooteperioodide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6842f-103">Configure waiting periods</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6842f-104">Rakenduses Microsoft Dynamics 365 Human Resources moodustavad ootepäevad vahe-eesmärgid, mida soodustuse plaanide jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="6842f-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="6842f-105">Näiteks kolm kuud alates palkamise kuupäevast, iga kuu esimene või kuus kuud.</span><span class="sxs-lookup"><span data-stu-id="6842f-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="6842f-106">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Ooteajad**.</span><span class="sxs-lookup"><span data-stu-id="6842f-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="6842f-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6842f-107">Select **New**.</span></span>

3. <span data-ttu-id="6842f-108">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="6842f-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6842f-109">Väli</span><span class="sxs-lookup"><span data-stu-id="6842f-109">Field</span></span> | <span data-ttu-id="6842f-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6842f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6842f-111">**Ootekood**</span><span class="sxs-lookup"><span data-stu-id="6842f-111">**Waiting code**</span></span> | <span data-ttu-id="6842f-112">Ooteaja kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="6842f-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="6842f-113">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="6842f-113">**Description**</span></span> | <span data-ttu-id="6842f-114">Ooteaja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6842f-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="6842f-115">**Ootemeetod**</span><span class="sxs-lookup"><span data-stu-id="6842f-115">**Waiting method**</span></span> | <span data-ttu-id="6842f-116">Valige väärtuste ripploendist sobiv ootemeetod.</span><span class="sxs-lookup"><span data-stu-id="6842f-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="6842f-117">Valikud on neto, see kuu, see kvartal, see aasta ja see nädal.</span><span class="sxs-lookup"><span data-stu-id="6842f-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="6842f-118">**Kuud**</span><span class="sxs-lookup"><span data-stu-id="6842f-118">**Months**</span></span> | <span data-ttu-id="6842f-119">Sisestage oodatava kuupäeva arvutamiseks ootemeetodile lisatavate kuude arv.</span><span class="sxs-lookup"><span data-stu-id="6842f-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="6842f-120">**Päevad**</span><span class="sxs-lookup"><span data-stu-id="6842f-120">**Days**</span></span> | <span data-ttu-id="6842f-121">Sisestage oodatava kuupäeva arvutamiseks ootemeetodile lisatavate päevade arv.</span><span class="sxs-lookup"><span data-stu-id="6842f-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="6842f-122">**Ootepäev**</span><span class="sxs-lookup"><span data-stu-id="6842f-122">**Waiting day**</span></span> | <span data-ttu-id="6842f-123">Valige ootamise päev, mida kasutatakse ootamise kuupäeva arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="6842f-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="6842f-124">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6842f-124">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]