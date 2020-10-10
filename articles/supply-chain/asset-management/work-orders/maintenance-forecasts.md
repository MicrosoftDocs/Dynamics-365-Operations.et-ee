---
title: Hooldusprognoosid
description: Selles teemas tutvustatakse hooldusprognoose varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6428981fcf560c541634d9466695be7bce4cb453
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888949"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="e5369-103">Hooldusprognoosid</span><span class="sxs-lookup"><span data-stu-id="e5369-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e5369-104">Kui loote töökäsu, loote töökäsu tööd, millel on seotud varad ja hooldustööde tüübid.</span><span class="sxs-lookup"><span data-stu-id="e5369-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="e5369-105">Kui valite hooldusprognoosi sisaldava hooldustöö tüübi, kopeeritakse prognoosid automaatselt töökäsku.</span><span class="sxs-lookup"><span data-stu-id="e5369-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="e5369-106">Võimalik, et saate töökäsule lisada prognoosiread või need töökäsust kustutada.</span><span class="sxs-lookup"><span data-stu-id="e5369-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="e5369-107">Töökäsu töötsükli oleku seadistus, seotud projektitüüp ja seotud projektitüübi oleku reeglid määravad ära, kas saate prognoosi ridu lisada või redigeerida.</span><span class="sxs-lookup"><span data-stu-id="e5369-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="e5369-108">Lisateavet töökäsu elutsükli olekute ja seotud projekti etappide kohta vt teemast [Prognoosid, töökäsud ja projektid](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="e5369-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="e5369-109">Valige **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="e5369-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e5369-110">Valige loendist töökäsk ja seejärel tehke tegumiriba vahekaardi > **Töökäsk** jaotises **Projekt** valik **Prognoos**.</span><span class="sxs-lookup"><span data-stu-id="e5369-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="e5369-111">Lehel **Töökäsu hooldusprognoos** kuvatakse töökäsu tööl valitud hooldustöö tüüpi prognoosi ridu.</span><span class="sxs-lookup"><span data-stu-id="e5369-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="e5369-112">Tundide prognoosi lisamine töökäsule</span><span class="sxs-lookup"><span data-stu-id="e5369-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="e5369-113">Valige lehel **Töökäsu hooldusprognoos** töökäsu töö. millel prognoos lisada.</span><span class="sxs-lookup"><span data-stu-id="e5369-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="e5369-114">Tehke uue rea loomiseks kiirkaardil **Tunnid** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e5369-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="e5369-115">Valige kategooria väljal **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="e5369-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="e5369-116">Sisestage väljale **Tunnid** prognoositud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="e5369-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="e5369-117">Valige real kasutatav kulu tüüp väljal **Rea atribuut**.</span><span class="sxs-lookup"><span data-stu-id="e5369-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="e5369-118">Üksuste prognoosi lisamine töökäsule</span><span class="sxs-lookup"><span data-stu-id="e5369-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="e5369-119">Üksuste lisamiseks töötellimuse hooldusprognoosine on kolm võimalust.</span><span class="sxs-lookup"><span data-stu-id="e5369-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="e5369-120">Võite luua read üksustele (varuosadele), mis ei sisaldu varuosade loendis või vara koosluses (BOM), võite valida varuosi kinnitatud varuosade loendist ja võite valida üksuseid vara kooslusest.</span><span class="sxs-lookup"><span data-stu-id="e5369-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="e5369-121">Valige lehel **Töökäsu hooldusprognoos** töökäsu töö. millel prognoos lisada.</span><span class="sxs-lookup"><span data-stu-id="e5369-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="e5369-122">Lisage kiirkaardil **Üksused** üksused hooldusprognoosi sobiva meetodi abil.</span><span class="sxs-lookup"><span data-stu-id="e5369-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="e5369-123">Varuosade loendis või vara koosluses mittesisalduva varuosa jaoks uue rea loomiseks järgige järgmisi juhendeid.</span><span class="sxs-lookup"><span data-stu-id="e5369-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="e5369-124">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e5369-124">Select **Add**.</span></span>
2. <span data-ttu-id="e5369-125">Valige kaup väljalt **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="e5369-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="e5369-126">Sisestage kogus väljale **Müügikogus**.</span><span class="sxs-lookup"><span data-stu-id="e5369-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="e5369-127">Valige väljal **Ühik** koguse mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="e5369-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="e5369-128">Sisestage sobivad väärtused väljadele **Omahind** ja **Valuuta**</span><span class="sxs-lookup"><span data-stu-id="e5369-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="e5369-129">Valige rea atribuut väljal **Rea atribuut**.</span><span class="sxs-lookup"><span data-stu-id="e5369-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="e5369-130">Üksuse ridadel kuvatavate mõõtude loendi muutmiseks valige **Varud** > **Kuva mõõdud**, valige mõõdud ja seejärel määrake valiku**Salvesta seadistus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e5369-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="e5369-131">Varuosa lisamiseks heakskiidetud varuosade loendist tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e5369-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="e5369-132">Valige **Lisa varuosad**.</span><span class="sxs-lookup"><span data-stu-id="e5369-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="e5369-133">Valige varuosa ja redigeerige vajadusel seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="e5369-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="e5369-134">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5369-134">Select **OK**.</span></span>

<span data-ttu-id="e5369-135">Üksuse lisamiseks põhivara kooslusest toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e5369-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="e5369-136">Valige **Lisa koosluse üksused**.</span><span class="sxs-lookup"><span data-stu-id="e5369-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="e5369-137">Valige üksus ja redigeerige vajadusel seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="e5369-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="e5369-138">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5369-138">Select **OK**.</span></span>

<span data-ttu-id="e5369-139">Et saada ülevaadet sellest, kus varahalduses valitud real olevat kaupa kasutatakse, valige varade, hooldustöö tüübi vaikesätete, varuosade ja töökäskude puhul väärtus **Üksus, kus kasutatud**.</span><span class="sxs-lookup"><span data-stu-id="e5369-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="e5369-140">Lisateavet selle ülevaate kohta vt teemast [Üksus, kus kasutatud](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="e5369-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="e5369-141">Kuluprognoosi lisamine töökäsule</span><span class="sxs-lookup"><span data-stu-id="e5369-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="e5369-142">Valige lehel **Töökäsu hooldusprognoos** töökäsu töö. millel prognoos lisada.</span><span class="sxs-lookup"><span data-stu-id="e5369-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="e5369-143">Tehke uue rea loomiseks kiirkaardil **Kulud** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e5369-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="e5369-144">Valige kategooria väljal **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="e5369-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="e5369-145">Sisestage kogus väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="e5369-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="e5369-146">Sisestage sobivad väärtused väljadele **Omahind**, **Müügivaluuta** ja **Müügihind**.</span><span class="sxs-lookup"><span data-stu-id="e5369-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="e5369-147">Valige real kasutatav kulu tüüp väljal **Rea atribuut**.</span><span class="sxs-lookup"><span data-stu-id="e5369-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="e5369-148">Kiirkaardil **Hooldusprognoosi kogusummad** kuvatakse ülevaade igale kiirkaardile loodud ridade arvust valitud töökäsu töö ja töökäsu jaoks.</span><span class="sxs-lookup"><span data-stu-id="e5369-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="e5369-149">Samuti kuvatakse töökäsu töö ja töökäsu prognoositud töötundide summat.</span><span class="sxs-lookup"><span data-stu-id="e5369-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="e5369-150">Alloleval joonisel kuvatakse lehe **Töökäsu hooldusprognoos** näide.</span><span class="sxs-lookup"><span data-stu-id="e5369-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Joonis 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="e5369-152">Töökäsu prognooside automaatne värskendamine</span><span class="sxs-lookup"><span data-stu-id="e5369-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="e5369-153">Kui tunnikulud, üksuse kulud ja kulud värskendatakse Microsoft Dynamics 365 for Finance and Operationsi muudes moodulites, võidakse varahalduse töökäskude prognoosid automaatselt värskendada nende muudatuste peegeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="e5369-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="e5369-154">See funktsioon aitab tagada, et töökäsu prognoosides kasutatakse alati uusimaid omahindu.</span><span class="sxs-lookup"><span data-stu-id="e5369-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="e5369-155">Sarnaseid värskendusi saate teha ka [hooldustöö tüübi prognoosidele](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="e5369-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="e5369-156">Valige **Varahaldus** > **Perioodiline** > **Prognoos** > **Värskenda töökäsu prognoosi**.</span><span class="sxs-lookup"><span data-stu-id="e5369-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="e5369-157">Dialoogi **Töökäsu prognoosi värskendamine** kiirkaardil **Kaasatavad kirjed** saate vajadusel lisada kindlate töökäskude ja töökäsu tööde valikud.</span><span class="sxs-lookup"><span data-stu-id="e5369-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="e5369-158">Asjakohaste valikute tegemiseks valige **Filtreeri**.</span><span class="sxs-lookup"><span data-stu-id="e5369-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="e5369-159">Vahekaardil **Taustal käitamine** saate vastavalt vajadusele seadistada automaatse värskenduse pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="e5369-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="e5369-160">Valige **OK**, et alustada prognoosi värskendamist.</span><span class="sxs-lookup"><span data-stu-id="e5369-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="e5369-161">Alloleval joonisel kuvatakse dialoogi **Töökäsu prognooside värskendamine** näide.</span><span class="sxs-lookup"><span data-stu-id="e5369-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Joonis 2](media/07-work-orders.png)
