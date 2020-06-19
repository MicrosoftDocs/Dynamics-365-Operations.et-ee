---
title: Puhkuse ostmise ja müümise põhimõtete haldamine
description: Saate võimaldada töötajatel osta ja müüa puhkust rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429009"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="037c8-103">Puhkuse ostmise ja müümise põhimõtete haldamine</span><span class="sxs-lookup"><span data-stu-id="037c8-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="037c8-104">Saate lubada töötajatel osta puhkust, luues puhkuse ostmise poliitika.</span><span class="sxs-lookup"><span data-stu-id="037c8-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="037c8-105">Töötajatele puhkuse ostu ja müügi lubamine</span><span class="sxs-lookup"><span data-stu-id="037c8-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="037c8-106">Valige lehel **Puhkuste ja puudumiste parameetrid** suvandi **Luba töötajatele puhkuse ostmine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="037c8-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="037c8-107">Puhkuse ostmise poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="037c8-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="037c8-108">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="037c8-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="037c8-109">Valige **Puhkuse ostmise ja müümise poliitika**.</span><span class="sxs-lookup"><span data-stu-id="037c8-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="037c8-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="037c8-110">Select **New**.</span></span>

4. <span data-ttu-id="037c8-111">Sisestage jaotises **Puhkuse ostmise ja müümise poliitika** poliitika **Nimi** ja **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="037c8-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="037c8-112">Valige **Poliitika tüüp**.</span><span class="sxs-lookup"><span data-stu-id="037c8-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="037c8-113">Saadaolevad poliitikatüübid on **Summa** ja **Tundi nädalas**.</span><span class="sxs-lookup"><span data-stu-id="037c8-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="037c8-114">Valige suvand **Summa**, et sisestada töötajale müümiseks ja ostmiseks lubatud maksimumsummade **Fikseeritud summa**.</span><span class="sxs-lookup"><span data-stu-id="037c8-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="037c8-115">Kui valite suvandi **Tundi nädalas**, siis kasutatakse poliitika maksimumsumma kindlaks määramiseks töötajale määratud tööaja kalendris määratletud tööaega.</span><span class="sxs-lookup"><span data-stu-id="037c8-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="037c8-116">Valige poliitika **Alguskuupäev** ja **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="037c8-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="037c8-117">Puhkuse ostmise või müümise taotlused on esitamiseks saadaval vaid antud ajavahemikus.</span><span class="sxs-lookup"><span data-stu-id="037c8-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="037c8-118">Valige jaotises **Ostupoliitika** suvand **Täistööaja vaste**, et kasutada maksimumsumma proportsionaalsuse jaotamiseks töötaja ametikoha kohta määratletud täistööaja vastet.</span><span class="sxs-lookup"><span data-stu-id="037c8-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="037c8-119">Kui poliitika tüüp on **Summa**, siis sisestage **Maksimaalne fikseeritud summa**.</span><span class="sxs-lookup"><span data-stu-id="037c8-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="037c8-120">Töötajale puhkuse ostmiseks saadaolevate puhkuse tüüpide lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="037c8-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="037c8-121">Te saate lisada poliitikale mitu puhkuse tüüpi.</span><span class="sxs-lookup"><span data-stu-id="037c8-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="037c8-122">Sisestage puhkuse tüübi jaoks **Töötatud kuud**, et lubada määratleda töötajale maksimaalne ostetav summa erinevate töötatud kuude alusel.</span><span class="sxs-lookup"><span data-stu-id="037c8-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="037c8-123">Sisestage puhkuse tüübi **Maksimumsumma**.</span><span class="sxs-lookup"><span data-stu-id="037c8-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="037c8-124">Sisestage **Määr**, mille alusel töötaja puhkust ostab.</span><span class="sxs-lookup"><span data-stu-id="037c8-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="037c8-125">Soovi korral sisestage puhkuse ostmisel kasutatav **Tulukood**.</span><span class="sxs-lookup"><span data-stu-id="037c8-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="037c8-126">Soovi korral saate valida, kas soovite kasutada puhkuse tüübi maksimumsumma kindlaks määramiseks täistööaja vastet.</span><span class="sxs-lookup"><span data-stu-id="037c8-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="037c8-127">Puhkuse ostmise ja müümise poliitika lisamine puhkuste ja puudumiste plaanile</span><span class="sxs-lookup"><span data-stu-id="037c8-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="037c8-128">Valige lehel **Puhkus ja puudumine** puhkuste ja puudumiste plaan.</span><span class="sxs-lookup"><span data-stu-id="037c8-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="037c8-129">Valige jaotises **Reeglid** suvand **Puhkuse ostmise ja müümise poliitika**.</span><span class="sxs-lookup"><span data-stu-id="037c8-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="037c8-130">Vt ka</span><span class="sxs-lookup"><span data-stu-id="037c8-130">See also</span></span>

[<span data-ttu-id="037c8-131">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="037c8-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="037c8-132">Puhkuste ja puudumiste tüüpide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="037c8-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="037c8-133">Puhkuse ja puudumise plaanide juurdekasv</span><span class="sxs-lookup"><span data-stu-id="037c8-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="037c8-134">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="037c8-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

