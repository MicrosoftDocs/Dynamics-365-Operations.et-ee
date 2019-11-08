---
title: Täiskoormuse arvutamine plaanitud töökäskude kohta
description: Selles teemas tutvustatakse, kuidas arvutada täiskoormust plaanitud töökäskude kohta varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d7684d1a4f78c95ebc7fd0a88f1c7dc7fead0303
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652099"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="b2bb6-103">Täiskoormuse arvutamine plaanitud töökäskude kohta</span><span class="sxs-lookup"><span data-stu-id="b2bb6-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b2bb6-104">Saate arvutada täiskoormuse plaanitud töökäskude kohta, et saada ülevaate ressursside töökoormuse kohta konkreetsel perioodil.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="b2bb6-105">Arvutused võivad olla järgmiste ressursside kohta: hooldustöötajad, töötajate grupid, tööriistad ja varad.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="b2bb6-106">Klõpsake **Varahaldus** > **Päringud** > **Ajakava** > **Täiskoormus**.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="b2bb6-107">Dialoogiboksis **Arvuta täiskoormus** > väljal **Kuva** valige millist koormuse tüüpi soovite arvutada: **Võimsus**, **Reserveeritud** või **Jääk**.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="b2bb6-108">Valige **Jah** tumblernupul **Eira 0-ridu**, kui te ei soovi näha tulemusi, milles on null.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="b2bb6-109">Valige ressursi tüübid, mille kohta soovite täiskoormust arvutada, valides **Jah** asjakohasel tumblernupul: **Töötaja**, **Hooldustöötaja grupp**, **Tööriist** ja **Vara**.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="b2bb6-110">Valige arvutuse jaoks alguskuupäev väljal **Kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="b2bb6-111">Väljal **Intervalli tüüp** valige arvutuse intervall: **Päev**, **Nädal**, **Kuu** või **Kvartal**.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="b2bb6-112">Väljale **Perioodi sagedus** sisestage intervallide arv, mida soovite arvutada.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="b2bb6-113">Kui olete valinud intervalli tüübiks näiteks **Päev** ja sisestate sellele väljale arvu "5", tehakse arvutus viie päeva kohta, alates alguskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="b2bb6-114">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="b2bb6-115">Allolev joonis näitab arvutuse tulemust koormuse tüübi **Reserveeritud** kohta, mis katab kolmenädalast perioodi.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Joonis 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="b2bb6-117">Kui valite oma arvutuse jaoks koormuse tüübid **Võimsus** või **Jääk**, kuvatakse sama tulemus, kui valitud perioodil pole ressursside kohta broneeringuid tehtud.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="b2bb6-118">Teavet selle kohta, kuidas arvutada täiskoormus hooldusgraafiku ridade ja planeerimata töökäskude kohta, leiate teemast [Täiskoormuse arvutamine](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="b2bb6-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

