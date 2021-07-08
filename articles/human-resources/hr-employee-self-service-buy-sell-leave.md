---
title: Puhkuse ostmine ja müümine
description: Dynamics 365 Human Resources aitab edastada puhkuse ostmise ja müümise taotlusi teie ettevõttes häälestatud puhkuse ostmis- ja müümispoliitika alusel.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271477"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="48ab5-103">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="48ab5-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="48ab5-104">Dynamics 365 Human Resources aitab edastada puhkuse ostmise ja müümise taotlusi teie ettevõttes häälestatud puhkuse ostmis- ja müümispoliitika alusel.</span><span class="sxs-lookup"><span data-stu-id="48ab5-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="48ab5-105">Puhkuse ostmise taotlus</span><span class="sxs-lookup"><span data-stu-id="48ab5-105">Request to buy leave</span></span>

1. <span data-ttu-id="48ab5-106">Tööruumis **Töövõtja iseteenindus** valige suvand **Puhkuse ostmise taotlemine** paanil **Vaba aja saldod**.</span><span class="sxs-lookup"><span data-stu-id="48ab5-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="48ab5-107">Lisage **Puhkuse tüüp** ja sisestage **Summa**, mille eest soovite puhkust osta.</span><span class="sxs-lookup"><span data-stu-id="48ab5-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="48ab5-108">Kui olete taotluse esitamiseks valmis, valige suvand **Esita**.</span><span class="sxs-lookup"><span data-stu-id="48ab5-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="48ab5-109">Teie saldod kas värskendatakse automaatselt või need läbivad enne värskendamist kinnitustoimingu.</span><span class="sxs-lookup"><span data-stu-id="48ab5-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="48ab5-110">See oleneb sellest, kuidas on ostupoliitika konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="48ab5-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="48ab5-111">Puhkuse müümise taotlus</span><span class="sxs-lookup"><span data-stu-id="48ab5-111">Request to sell leave</span></span>

1. <span data-ttu-id="48ab5-112">Tööruumis **Töövõtja iseteenindus** valige suvand **Puhkuse müümise taotlemine** paanil **Vaba aja saldod**.</span><span class="sxs-lookup"><span data-stu-id="48ab5-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="48ab5-113">Lisage **Puhkuse tüüp** ja sisestage **Summa**, mille eest soovite puhkust müüa.</span><span class="sxs-lookup"><span data-stu-id="48ab5-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="48ab5-114">Kui olete taotluse esitamiseks valmis, valige suvand **Esita**.</span><span class="sxs-lookup"><span data-stu-id="48ab5-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="48ab5-115">Teie saldod kas värskendatakse automaatselt või need läbivad enne värskendamist kinnitustoimingu.</span><span class="sxs-lookup"><span data-stu-id="48ab5-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="48ab5-116">See oleneb sellest, kuidas on ostupoliitika konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="48ab5-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="48ab5-117">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="48ab5-117">Troubleshooting</span></span> 

<span data-ttu-id="48ab5-118">Kui ostu või müügi puhkuse taotluse töövoog nurjub, saavad kasutajad, kellel on **EssLeaveBuySellRequestApprover** privileeg, vaadata üle kõikide puhkuse ostu- ja müügitaotluste teatelogi.</span><span class="sxs-lookup"><span data-stu-id="48ab5-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="48ab5-119">Selleks minge **Puhkus ja puudumine > Link > Ostu- ja müügitaotluste päringud >Teatelogi** (vasakul üleval).</span><span class="sxs-lookup"><span data-stu-id="48ab5-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="48ab5-120">**Teatelogi** näitab kasutajatele, kuidas kandeid töödeldakse ja seostatud töövoo ajalugu.</span><span class="sxs-lookup"><span data-stu-id="48ab5-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="48ab5-121">Vt ka</span><span class="sxs-lookup"><span data-stu-id="48ab5-121">See also</span></span>

[<span data-ttu-id="48ab5-122">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="48ab5-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="48ab5-123">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="48ab5-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
