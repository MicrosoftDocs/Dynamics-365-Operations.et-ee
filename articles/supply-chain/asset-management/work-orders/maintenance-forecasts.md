---
title: Hooldusprognoosid
description: Selles teemas tutvustatakse hooldusprognoose varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875612"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="92acf-103">Hooldusprognoosid</span><span class="sxs-lookup"><span data-stu-id="92acf-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="92acf-104">Kui loote töökäsu, loote töökäsu tööd koos asjakohaste varade ja hooldustööde tüüpidega.</span><span class="sxs-lookup"><span data-stu-id="92acf-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="92acf-105">Kui valite hooldusprognoosi sisaldava hooldustöö tüübi, kopeeritakse prognoosid automaatselt töökäsku.</span><span class="sxs-lookup"><span data-stu-id="92acf-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="92acf-106">Saate töökäsule prognoosi ridu lisada või neid kustutada.</span><span class="sxs-lookup"><span data-stu-id="92acf-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="92acf-107">Töökäsu töötsükli oleku, asjakohase projekti tüübi ja projekti tüübiga seotud etapi reeglite seadistus määrab selle, kas saate prognoosi ridu lisada või redigeerida.</span><span class="sxs-lookup"><span data-stu-id="92acf-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="92acf-108">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="92acf-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="92acf-109">Valige loendist töökäsk ja klõpsake **Prognoos**.</span><span class="sxs-lookup"><span data-stu-id="92acf-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="92acf-110">Jaotises **Töökäsu hooldusprognoos** kuvatakse töökäsu tööl valitud hooldustöö tüüpi prognoosi ridu.</span><span class="sxs-lookup"><span data-stu-id="92acf-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="92acf-111">Tundide prognoosi lisamine töökäsule</span><span class="sxs-lookup"><span data-stu-id="92acf-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="92acf-112">Valige töökäsu töö, millele soovite prognoosi lisada.</span><span class="sxs-lookup"><span data-stu-id="92acf-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="92acf-113">Klõpsake uue rea loomiseks kiirkaardil **Tunnid** suvandit **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="92acf-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="92acf-114">Valige kategooria väljal **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="92acf-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="92acf-115">Sisestage väljale **Tunnid** prognoositud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="92acf-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="92acf-116">Valige real kasutatav kulu tüüp väljal **Rea atribuut**.</span><span class="sxs-lookup"><span data-stu-id="92acf-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="92acf-117">Üksuste prognoosi lisamine töökäsule</span><span class="sxs-lookup"><span data-stu-id="92acf-117">Add items forecast to a work order</span></span>

<span data-ttu-id="92acf-118">Üksuste lisamiseks töökäsu hooldusprognoosile on kolm võimalust: võite luua read üksustele (varuosadele), mis ei sisaldu varuosade loendis või vara koosluses, võite valida varuosi kinnitatud varuosade loendist ja võite valida üksuseid vara kooslusest.</span><span class="sxs-lookup"><span data-stu-id="92acf-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="92acf-119">Valige töökäsu töö, millele soovite prognoosi lisada.</span><span class="sxs-lookup"><span data-stu-id="92acf-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="92acf-120">Valige kiirkaart **Üksused**.</span><span class="sxs-lookup"><span data-stu-id="92acf-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="92acf-121">Klõpsake varuosade loendis või vara koosluses mittesisalduva varuosa jaoks uue rea loomiseks suvandil **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="92acf-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="92acf-122">Valige kaup väljal **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="92acf-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="92acf-123">Sisestage kogus väljale **Müügi kogus** ja valige koguse üksus väljal **Üksus**.</span><span class="sxs-lookup"><span data-stu-id="92acf-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="92acf-124">Sisestage omahind ja valuuta vastavatele väljadele ja valige **Rea atribuut**.</span><span class="sxs-lookup"><span data-stu-id="92acf-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="92acf-125">Kui soovite muuta üksuse ridadel kuvatavate mõõtude loendit, klõpsake **Varud** > **Kuva mõõdud**, valige mõõdud ja valige tumblernupul **Salvesta seadistus** suvand "Jah".</span><span class="sxs-lookup"><span data-stu-id="92acf-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="92acf-126">Kui soovite hooldusprognoosile lisada kinnitatud varuosa, klõpsake suvandit **Lisa varuosad**, valige varuosa, redigeerige vajadusel sellega setud andmeid ja klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="92acf-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="92acf-127">Kui soovite hooldusprognoosile lisada vara koosluse üksusi, klõpsake suvandit **Lisa koosluse üksusi**, valige üksus, redigeerige vajadusel sellega setud andmeid ja klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="92acf-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="92acf-128">Kui soovite saada ülevaadet, kus valitud rea üksust varahalduses seoses varade, vaikimisi hooldustöö tüüpide, varuosade ja töökäskudega kasutatakse, klõpsake suvandit **Üksus kus kasutatud**.</span><span class="sxs-lookup"><span data-stu-id="92acf-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="92acf-129">Kuluprognoosi lisamine töökäsule</span><span class="sxs-lookup"><span data-stu-id="92acf-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="92acf-130">Selles teemas kirjeldatakse töökäsule kuluprognoosi lisamist.</span><span class="sxs-lookup"><span data-stu-id="92acf-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="92acf-131">Valige vormi vasakult poolelt töökäsu töö, millele soovite prognoosi lisada.</span><span class="sxs-lookup"><span data-stu-id="92acf-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="92acf-132">Valige kiirkaart **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="92acf-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="92acf-133">Uue rea loomiseks klõpsake **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="92acf-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="92acf-134">Valige kategooria väljal **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="92acf-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="92acf-135">Sisestage kogus väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="92acf-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="92acf-136">Sisestage omahind ja müügi valuuta ja müügihind vastavatele väljadele.</span><span class="sxs-lookup"><span data-stu-id="92acf-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="92acf-137">Valige real kasutatav kulu tüüp väljal **Rea atribuut**.</span><span class="sxs-lookup"><span data-stu-id="92acf-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="92acf-138">Kiirkaardil **Hooldusprognoosi kogusummad** võite näha valitud töökäsu töö ja töökäsu igale vahekaardile loodud ridade arvu ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="92acf-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="92acf-139">Samuti näete töökäsu töö ja töökäsu prognoositud töötundide summat.</span><span class="sxs-lookup"><span data-stu-id="92acf-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Joonis 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="92acf-141">Töökäsu prognooside automaatne värskendamine</span><span class="sxs-lookup"><span data-stu-id="92acf-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="92acf-142">Varahalduses saate mistahes tunnikulude, üksuse kulude ja teistes rakenduse Dynamics 365 for Finance and Operations moodulites värskendatud kuludega seotud töökäsu prognooside muudatusi automaatselt värskendada.</span><span class="sxs-lookup"><span data-stu-id="92acf-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="92acf-143">Seda tehakse selleks, et kindlustada töökäsu prognoosides alati uusimate omahindade kasutamine.</span><span class="sxs-lookup"><span data-stu-id="92acf-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="92acf-144">Sarnaseid värskendusi on võimalik teha ka [hooldustöö tüübi prognoosidele](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="92acf-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="92acf-145">Klõpsake **Varahaldus** > **Perioodiline** > **Prognoos** > **Värskenda töökäsu prognoosi**.</span><span class="sxs-lookup"><span data-stu-id="92acf-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="92acf-146">Rippdialoogis **Töökäsu prognoosi värskendamine** saate vajadusel lisada valikuid seoses konkreetsete töökäskude või töökäsu töödega.</span><span class="sxs-lookup"><span data-stu-id="92acf-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="92acf-147">Nende valikute tegemiseks klõpsake **Filter**.</span><span class="sxs-lookup"><span data-stu-id="92acf-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="92acf-148">Vajadusel saate seadistada automaatse värskenduse pakett-tööna kiirkaardil **Taustal käitamine**.</span><span class="sxs-lookup"><span data-stu-id="92acf-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="92acf-149">Prognoosi värskendamise käivitamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="92acf-149">Click **OK** to start the forecast update.</span></span>


![Joonis 2](media/07-work-orders.png)

