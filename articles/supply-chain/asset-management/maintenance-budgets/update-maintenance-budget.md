---
title: Hoolduseelarvete värskendamine
description: Selles teemas selgitatakse, kuidas luua värskendada hoolduseelarvet varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e43abd4644eec8c91606ec48bbecf30f12600856
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205272"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="68254-103">Hoolduseelarvete värskendamine</span><span class="sxs-lookup"><span data-stu-id="68254-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="68254-104">Lehel **hoolduse eelarve read** kuvatakse kõik eelarveread, mis on loodud eelarve jaoks, mis on valitud lehel **Hoolduse eelarved**.</span><span class="sxs-lookup"><span data-stu-id="68254-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="68254-105">(Lisateavet vt teemast [Loo hoolduse eelarved](create-maintenance-budget.md).) Hoolduse eelarve ridu saate ümber arvutada ja korrigeerida, kuni hoolduse eelarve on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="68254-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="68254-106">Pärast eelarveperioodi möödumist ja vara haldusse sisestatud kulude sisestamist saate eelarve ridu ka tegelike kuludega värskendada.</span><span class="sxs-lookup"><span data-stu-id="68254-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="68254-107">Hoolduse eelarve ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="68254-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="68254-108">Hoolduse eelarvet saate ümber arvutada lehel **Hoolduse eelarve read**.</span><span class="sxs-lookup"><span data-stu-id="68254-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="68254-109">Hoolduse eelarve ümberarvutamisel kustutatakse olemasolevad eelarveread ja tehakse uus arvutus.</span><span class="sxs-lookup"><span data-stu-id="68254-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="68254-110">Lehel **Hoolduse eelarve read** valige **Arvuta ümber**.</span><span class="sxs-lookup"><span data-stu-id="68254-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="68254-111">Dialoogiaknas **Arvuta eelarve ümber** tehke uue arvutuse jaoks vajalikud muudatused ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="68254-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="68254-112">Uued eelarveread luuakse vastavalt teie määratud väärtustele.</span><span class="sxs-lookup"><span data-stu-id="68254-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="68254-113">Kohanda eelarveridu</span><span class="sxs-lookup"><span data-stu-id="68254-113">Adjust budget lines</span></span>

<span data-ttu-id="68254-114">Kogu hoolduse eelarve ümberarvutamise asemel saate korrigeerida valitud ridu, mis on seotud eelarve kuludega.</span><span class="sxs-lookup"><span data-stu-id="68254-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="68254-115">Valige lehel **Hoolduse eelarve read** read, mille jaoks eelarve kulu värskendada.</span><span class="sxs-lookup"><span data-stu-id="68254-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="68254-116">Valige **Kohanda**.</span><span class="sxs-lookup"><span data-stu-id="68254-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="68254-117">Summa lisamiseks valitud ridadele valige märkekast **Lisa kulu** ja sisestage väärtus väljale **Lisa väärtus**.</span><span class="sxs-lookup"><span data-stu-id="68254-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="68254-118">Et korrutada eelarve kulu valitud eelarveridadele teguriga, märkige ruut **Korruta kulu** ja sisestage tegur väljale **Korruta väärtus**.</span><span class="sxs-lookup"><span data-stu-id="68254-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="68254-119">Näiteks kui sisestate **1,2** väljale **Korruta väärtus**, suurendate eelarve kulu valitud ridadel 20 protsendi võrra.</span><span class="sxs-lookup"><span data-stu-id="68254-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="68254-120">Kui sisestate **0,7**, vähendate eelarve kulu valitud ridadel 30 protsendi võrra.</span><span class="sxs-lookup"><span data-stu-id="68254-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="68254-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="68254-121">Select **OK**.</span></span>

<span data-ttu-id="68254-122">Valitud eelarve ridu värskendatakse vastavalt väärtustele, mille seate sammus 3 või 4.</span><span class="sxs-lookup"><span data-stu-id="68254-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="68254-123">Tegelike kulude värskendamine</span><span class="sxs-lookup"><span data-stu-id="68254-123">Update actual costs</span></span>

<span data-ttu-id="68254-124">Pärast eelarveridade kuupäevade möödumist ja varahaldusse tegelike kulude sisestamist saate hoolduse eelarvet tegelike kuludega värskendada.</span><span class="sxs-lookup"><span data-stu-id="68254-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="68254-125">Lehel **Hoolduse eelarve read** valige **Värskenda kulu**.</span><span class="sxs-lookup"><span data-stu-id="68254-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="68254-126">Dialoogiaknas **Arvuta tegelik kulu** valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="68254-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="68254-127">Eelarveridade väljad **Tegelik kulu** värskendatakse, kui eelarveridade tegelik kulu on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="68254-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="68254-128">Uued eelarveread võidakse luua, kui uute varade tüübid on loodud eelarve loomisest saadik ja kui neid varatüüpe on kasutatud varade puhul, mille jaoks on loodud töökäsud ja seotud kulud on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="68254-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="68254-129">Uued eelarveread näitavad ainult tegelikke kulusid, kuna nende jaoks ei arvutatud eelarve kulusid.</span><span class="sxs-lookup"><span data-stu-id="68254-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="68254-130">Et näha ülevaadet tegelikest kuludest, mis on jagatud ennetus-, parandus- ja investeerimiskuludeks, saate teha arvutuse sama perioodi kohta, mis on esitatud lehel **Vara kulude kontroll**.</span><span class="sxs-lookup"><span data-stu-id="68254-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="68254-131">Eelarveridade käsitsi lisamine</span><span class="sxs-lookup"><span data-stu-id="68254-131">Manually add budget lines</span></span>

<span data-ttu-id="68254-132">Lehel **Hoolduse eelarveread** saate uue eelarverea käsitsi lisada, valides **Uus** ja seejärel tehes tehes valikud real.</span><span class="sxs-lookup"><span data-stu-id="68254-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="68254-133">Siin on mõned näited olukordadest, kus selline lähenemine võib olla kasulik:</span><span class="sxs-lookup"><span data-stu-id="68254-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="68254-134">Te teate, et mõnede varade renoveerimine on praegu planeerimise faasis, kuid seotud tööd pole veel varahalduses loodud.</span><span class="sxs-lookup"><span data-stu-id="68254-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="68254-135">Siiski soovite nende tööde eelarvete kulusid kaasata hoolduse eelarvesse.</span><span class="sxs-lookup"><span data-stu-id="68254-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="68254-136">Pärast hoolduse eelarvet on loodud uusi varasid või varatüüpe, kuid hoolduse plaane pole nende varade või varatüüpide puhul veel seadistatud.</span><span class="sxs-lookup"><span data-stu-id="68254-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="68254-137">Siiski soovite nende varatüüpide eelarvete kulusid kaasata hoolduse eelarvesse.</span><span class="sxs-lookup"><span data-stu-id="68254-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
