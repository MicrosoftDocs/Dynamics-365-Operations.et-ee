---
title: Puhkuse ostmise ja müümise põhimõtete haldamine
description: Saate võimaldada töötajatel osta ja müüa puhkust rakenduses Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 491d1654bd219b487f95a1eb328e574114ec1f9f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051373"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="106a8-103">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="106a8-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="106a8-104">Saate lubada töötajatel osta ja müüa puhkust, luues puhkuse ostmise ja müümise poliitika.</span><span class="sxs-lookup"><span data-stu-id="106a8-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="106a8-105">Saate konfigureerida need poliitikad töövoogude kinnitamiseks kasutamiseks, maksimaalsete summade ja määrade ja ostmise ning müümise määrade määramiseks.</span><span class="sxs-lookup"><span data-stu-id="106a8-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="106a8-106">Töötajatele puhkuse ostu ja müügi lubamine</span><span class="sxs-lookup"><span data-stu-id="106a8-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="106a8-107">Valige lehel **Puhkuste ja puudumiste parameetrid** suvandite **Luba töötajatele puhkuse ostmine** ja **Luba töötajatele puhkuse müümine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="106a8-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="106a8-108">Puhkuse ostmise ja müümise poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="106a8-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="106a8-109">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="106a8-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="106a8-110">Valige **Puhkuse ostmise ja müümise poliitika**.</span><span class="sxs-lookup"><span data-stu-id="106a8-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="106a8-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="106a8-111">Select **New**.</span></span>

4. <span data-ttu-id="106a8-112">Sisestage jaotises **Puhkuse ostmise ja müümise poliitika** poliitika **Nimi** ja **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="106a8-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="106a8-113">Valige **Poliitika tüüp**.</span><span class="sxs-lookup"><span data-stu-id="106a8-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="106a8-114">Saadaolevad poliitikatüübid on **Summa** ja **Tundi nädalas**.</span><span class="sxs-lookup"><span data-stu-id="106a8-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="106a8-115">Valige suvand **Summa**, et sisestada töötajale müümiseks ja ostmiseks lubatud maksimumsummade **Fikseeritud summa**.</span><span class="sxs-lookup"><span data-stu-id="106a8-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="106a8-116">Kui valite suvandi **Tundi nädalas**, siis kasutatakse poliitika maksimumsumma kindlaks määramiseks töötajale määratud tööaja kalendris määratletud tööaega.</span><span class="sxs-lookup"><span data-stu-id="106a8-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="106a8-117">Valige poliitika **Alguskuupäev** ja **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="106a8-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="106a8-118">Puhkuse ostmise või müümise taotlused on esitamiseks saadaval vaid antud ajavahemikus.</span><span class="sxs-lookup"><span data-stu-id="106a8-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="106a8-119">Valige poliitika jaoks **Töövoo ID**.</span><span class="sxs-lookup"><span data-stu-id="106a8-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="106a8-120">Kõik ostu- ja müügitaotlused kasutavad seda töövoogu ülevaatamiseks ja kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="106a8-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="106a8-121">Valige jaotises **Ostupoliitika** suvand **Täistööaja vaste**, et kasutada maksimumsumma proportsionaalsuse jaotamiseks töötaja ametikoha kohta määratletud täistööaja vastet.</span><span class="sxs-lookup"><span data-stu-id="106a8-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="106a8-122">Kui poliitika tüüp on **Summa**, siis sisestage **Maksimaalne fikseeritud summa**.</span><span class="sxs-lookup"><span data-stu-id="106a8-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="106a8-123">Töötajale puhkuse ostmiseks saadaolevate puhkuse tüüpide lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="106a8-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="106a8-124">Te saate lisada poliitikale mitu puhkuse tüüpi.</span><span class="sxs-lookup"><span data-stu-id="106a8-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="106a8-125">Sisestage puhkuse tüübi jaoks **Töötatud kuud**, et lubada määratleda töötajale maksimaalne ostetav summa erinevate töötatud kuude alusel.</span><span class="sxs-lookup"><span data-stu-id="106a8-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="106a8-126">Sisestage puhkuse tüübi **Maksimumsumma**.</span><span class="sxs-lookup"><span data-stu-id="106a8-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="106a8-127">Sisestage **Määr**, mille alusel töötaja puhkust ostab.</span><span class="sxs-lookup"><span data-stu-id="106a8-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="106a8-128">Soovi korral sisestage puhkuse ostmisel kasutatav **Tulukood**.</span><span class="sxs-lookup"><span data-stu-id="106a8-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="106a8-129">Soovi korral saate valida, kas soovite kasutada puhkuse tüübi maksimumsumma kindlaks määramiseks täistööaja vastet.</span><span class="sxs-lookup"><span data-stu-id="106a8-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="106a8-130">Müügipoliitika loomiseks järgige jaotise **Müügipoliitika** toiminguid 8 kuni 14.</span><span class="sxs-lookup"><span data-stu-id="106a8-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="106a8-131">Puhkuse ostmise ja müümise poliitika lisamine puhkuste ja puudumiste plaanile</span><span class="sxs-lookup"><span data-stu-id="106a8-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="106a8-132">Valige lehel **Puhkus ja puudumine** puhkuste ja puudumiste plaan.</span><span class="sxs-lookup"><span data-stu-id="106a8-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="106a8-133">Valige jaotises **Reeglid** suvand **Puhkuse ostmise ja müümise poliitika**.</span><span class="sxs-lookup"><span data-stu-id="106a8-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="106a8-134">Vt ka</span><span class="sxs-lookup"><span data-stu-id="106a8-134">See also</span></span>

[<span data-ttu-id="106a8-135">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="106a8-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="106a8-136">Puhkuste ja puudumiste tüüpide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="106a8-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="106a8-137">Puhkuse ja puudumise plaanide juurdekasv</span><span class="sxs-lookup"><span data-stu-id="106a8-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="106a8-138">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="106a8-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]