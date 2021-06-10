---
title: Töötaja puhkuse haldamine
description: Rakenduses Dynamics 365 Human Resources saate hallata töövõtja puhkust.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33080fc5ca43f3d83ee9d17565f4c229ced7b94f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055624"
---
# <a name="manage-employee-leave"></a><span data-ttu-id="567c8-103">Töötaja puhkuse haldamine</span><span class="sxs-lookup"><span data-stu-id="567c8-103">Manage employee leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="567c8-104">Saate hallata töötaja puhkust puhkuse tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="567c8-104">You can manage an employee's leave by leave type.</span></span> <span data-ttu-id="567c8-105">See hõlmab puhkuse registreerimise aegumist ja puhkuse tüübi saldode korrigeerimist.</span><span class="sxs-lookup"><span data-stu-id="567c8-105">This includes expiring leave enrollment and adjusting leave type balances.</span></span> 

## <a name="adjust-leave-balances"></a><span data-ttu-id="567c8-106">Puhkusesaldode korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="567c8-106">Adjust leave balances</span></span>

1. <span data-ttu-id="567c8-107">Töövõtja kirjes valige suvand **Puhkus**.</span><span class="sxs-lookup"><span data-stu-id="567c8-107">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="567c8-108">Valige suvand **Puhkuste ja puudumiste seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="567c8-108">Select **Leave and absence setup**.</span></span>

3. <span data-ttu-id="567c8-109">Valige **Saldo korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="567c8-109">Select **Adjust balance**.</span></span>

4. <span data-ttu-id="567c8-110">Valige **Puhkuse tüüp**.</span><span class="sxs-lookup"><span data-stu-id="567c8-110">Select the **Leave type**.</span></span>

5. <span data-ttu-id="567c8-111">Sisestage **Korrigeeritud summa**.</span><span class="sxs-lookup"><span data-stu-id="567c8-111">Enter an **Adjustment amount**.</span></span> 

6. <span data-ttu-id="567c8-112">Lisaks saate soovi korral valida suvandi **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="567c8-112">Optionally, you can select a **Date**.</span></span> 

<span data-ttu-id="567c8-113">Te võite töötaja puhkusesaldot korrigeerides lisada põhjusekoodi ja kommentaari.</span><span class="sxs-lookup"><span data-stu-id="567c8-113">You can include a reason code and comment when adjusting an employee's leave balance.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="567c8-114">Puhkusesaldode lisateabe vaatamisel on eelversioon.</span><span class="sxs-lookup"><span data-stu-id="567c8-114">Viewing additional information about leave balances is in preview.</span></span> <span data-ttu-id="567c8-115">Peate selle lubama keskkonnas **Liivakast**.</span><span class="sxs-lookup"><span data-stu-id="567c8-115">You'll need to enable it in your **Sandbox** environment.</span></span> <span data-ttu-id="567c8-116">Lisateavet eelvaatefunktsioonide lubamise kohta vt [Funktsioonide haldus](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="567c8-116">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br>
><span data-ttu-id="567c8-117">Kui viite kursori puhkusesaldo kohale, kuvatakse nüüd järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="567c8-117">When hovering over any leave balance, you will now see:</span></span><br>
>- <span data-ttu-id="567c8-118">**Saadaval**: sellel aastal kokku – sellel aastal võetud</span><span class="sxs-lookup"><span data-stu-id="567c8-118">**Available**: Total this year - Take this year</span></span>
>- <span data-ttu-id="567c8-119">**Sellel aastal kokku**: kõik viitvõlad, korrigeerimised ja aasta edasikanded</span><span class="sxs-lookup"><span data-stu-id="567c8-119">**Total this year**: All accruals, adjustments, and carry forward for the year</span></span>
>- <span data-ttu-id="567c8-120">**Sellel aastal võetud**: kogu kinnitatud vaba aeg</span><span class="sxs-lookup"><span data-stu-id="567c8-120">**Taken this year**: All approved time off</span></span>

## <a name="see-also"></a><span data-ttu-id="567c8-121">Vt ka</span><span class="sxs-lookup"><span data-stu-id="567c8-121">See also</span></span>

- [<span data-ttu-id="567c8-122">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="567c8-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="567c8-123">Puhkuste ja puudumiste taotluste haldamine</span><span class="sxs-lookup"><span data-stu-id="567c8-123">Manage leave and absence requests</span></span>](hr-employee-self-service-manage-requests.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]