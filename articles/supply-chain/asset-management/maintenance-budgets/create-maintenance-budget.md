---
title: Hoolduseelarvete loomine
description: Selles teemas tutvustatakse, kuidas luua hoolduseelarvet varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: aa373a1a15c19154e6c822c3a962c2b43b8d9e10
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205295"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="77294-103">Hoolduseelarvete loomine</span><span class="sxs-lookup"><span data-stu-id="77294-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="77294-104">Hoolduseelarveid kasutatakse, et tagada ülevaade ennetava hoolduse eeldatavatest kuludest.</span><span class="sxs-lookup"><span data-stu-id="77294-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="77294-105">Eelarveread arvutatakse nende hooldusgraafiku ridade põhjal, mille eeldatav alguskuupäev on eelarveperioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="77294-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="77294-106">Hoolduseelarved põhinevad kulutüüpidel, mida kasutatakse varahalduses: **Ennetav**, **Parandav** ja **Investeering**.</span><span class="sxs-lookup"><span data-stu-id="77294-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="77294-107">Eelarvekulud investeeringu hoolduseks on kaasatud aktiivsete varade jaoks, millel on asenduskuupäev eelarveperioodi jooksul ja seotud asendusväärtus.</span><span class="sxs-lookup"><span data-stu-id="77294-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="77294-108">Eelarvekulud parandava hoolduse jaoks on kaasatud, kui eelarve arvutusse on kaasatud varasem parandav kuupäev.</span><span class="sxs-lookup"><span data-stu-id="77294-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="77294-109">Sellisel juhul arvutatakse varasema perioodi parandavad kulud sama tulevase perioodi kohta, mille kohta hoolduseelarvet arvutate.</span><span class="sxs-lookup"><span data-stu-id="77294-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="77294-110">Hoolduseelarve loomine</span><span class="sxs-lookup"><span data-stu-id="77294-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="77294-111">Valige **Varahaldus** \> **Päringud** \> **Hoolduseelarve** \> **Eelarve**.</span><span class="sxs-lookup"><span data-stu-id="77294-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="77294-112">Valige käsk **Loo eelarve**.</span><span class="sxs-lookup"><span data-stu-id="77294-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="77294-113">Väljale **Hoolduseelarve** sisestage eelarve ID.</span><span class="sxs-lookup"><span data-stu-id="77294-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="77294-114">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="77294-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="77294-115">Vahekaardi **Periood** väljadele **Kuupäevast** ja **Kuupäevani** sisestage eelarveperioodi algus- ja lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="77294-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="77294-116">Parandavate eelarvekulude kaasamiseks, mis arvutatakse varasema perioodi tegelike kulude põhjal, sisestage väljale **Parandav kuupäevast** perioodi alguskuupäev, mille kohta need kulud peaksid olema kaasatud.</span><span class="sxs-lookup"><span data-stu-id="77294-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="77294-117">Sõltuvalt eelarves nõutavast üksikasjade tasemest seadistage asjakohased suvandid viiel kiirkaardil **Rühmitusalus**.</span><span class="sxs-lookup"><span data-stu-id="77294-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="77294-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="77294-118">Select **OK**.</span></span>
8. <span data-ttu-id="77294-119">Valige **Eelarveread**, et avada leht **Hoolduseelarveread**, kus saate vaadata kõiki eelarveridu, mis on selle perioodi kohta loodud.</span><span class="sxs-lookup"><span data-stu-id="77294-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="77294-120">Eelarve kinnitamiseks valige see lehel **Hoolduseelarved** ja seejärel valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="77294-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="77294-121">Seejärel valige **OK** dialoogiboksis **Kinnita eelarve**.</span><span class="sxs-lookup"><span data-stu-id="77294-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="77294-122">Teie nimi sisestatakse lehe **Hoolduseelarved** väljale **Kinnitaja**.</span><span class="sxs-lookup"><span data-stu-id="77294-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="77294-123">Pärast hoolduseelarve kinnitamist ei saa te enam uuesti arvutada ega kohandada seotud ridu lehel **Hoolduseelarveread**, ilma kinnitust eemaldamata.</span><span class="sxs-lookup"><span data-stu-id="77294-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="77294-124">Hoolduseelarve kinnituse eemaldamiseks valige see lehel **Hoolduseelarved** ja seejärel valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="77294-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="77294-125">Seejärel valige **OK** dialoogiboksis **Kinnita eelarve**.</span><span class="sxs-lookup"><span data-stu-id="77294-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Hoolduseelarved](media/01-maintenance-budgets.png)

<span data-ttu-id="77294-127">Samuti saate luua uue hoolduseelarve olemasoleva eelarve kopeerimisega.</span><span class="sxs-lookup"><span data-stu-id="77294-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="77294-128">Lehel **Hoolduseelarved** ja valige eelarve, mida soovite kopeerida, ja seejärel valige **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="77294-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="77294-129">See lähenemine on kasulik, kui olete näiteks loonud eelarve ühe kuu kohta ja soovite seda kopeerida teistesse kuudesse.</span><span class="sxs-lookup"><span data-stu-id="77294-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="77294-130">Hoolduseelarve arvutab ainult hooldusgraafiku ridadel põhinevad eelarvekulud.</span><span class="sxs-lookup"><span data-stu-id="77294-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="77294-131">Sama perioodi tegelike kulude arvutamiseks saate teha arvutuse lehel **Vara kulu juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="77294-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
