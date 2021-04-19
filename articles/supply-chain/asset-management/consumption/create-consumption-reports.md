---
title: Loo tarbimise aruandeid
description: Selles teemas tutvustatakse, kuidas luua tarbimise aruandeid varahalduses.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8add0602e0ebe7a5c0cf2c76de6fa2f4f21a2f72
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837917"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="e1de7-103">Loo tarbimise aruandeid</span><span class="sxs-lookup"><span data-stu-id="e1de7-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e1de7-104">Kui olete loonud ja sisestanud töökäskude tarbimise registreeringud varahalduses, on tarbimise üksikasjade kuvamiseks saadaval kaks aruannet.</span><span class="sxs-lookup"><span data-stu-id="e1de7-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="e1de7-105">Vara tarbimise aruanne</span><span class="sxs-lookup"><span data-stu-id="e1de7-105">Asset consumption report</span></span>

<span data-ttu-id="e1de7-106">Kui olete sisestanud töökäskude tarbimise, saate vara tarbimise aruande printida.</span><span class="sxs-lookup"><span data-stu-id="e1de7-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="e1de7-107">Aruanne kuvab tunde, tunni kulusid, kauba kulusid ja varade kohta sisestatud kulusid.</span><span class="sxs-lookup"><span data-stu-id="e1de7-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="e1de7-108">Klõpsake **Varahaldus** > **Aruanded** > **Varad** > **Vara tarbimine**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="e1de7-109">Dialoogiboksis **Vara tarbimine** valige parameetrid ja üksikasja tase, mida soovite näha, valides **Jah** asjakohastel tumblernuppudel ja sisestades töö asukoha taseme jaotisesse **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="e1de7-110">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade vara ridu te soovite.</span><span class="sxs-lookup"><span data-stu-id="e1de7-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="e1de7-111">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha varad ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="e1de7-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="e1de7-112">Kui sisestate väljale **Tasemed** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki varasid kõigi töö asukoha tasemete kohta, millega need on seotud.</span><span class="sxs-lookup"><span data-stu-id="e1de7-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="e1de7-113">Valige **Jah** tumblernupul **Kõigi alamvarade summa**, et näha iga alamvara summat aruandes.</span><span class="sxs-lookup"><span data-stu-id="e1de7-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="e1de7-114">Valige kuupäevaintervall jaotises **Kuupäevad**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="e1de7-115">Kiirkaardil **Sihtkoht** valige, kas soovite aruande kuvada ekraanil, printida või salvestada faili või meilina.</span><span class="sxs-lookup"><span data-stu-id="e1de7-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="e1de7-116">Vajaduse korral saate valida, milliseid konkreetseid varasid aruandes kuvada.</span><span class="sxs-lookup"><span data-stu-id="e1de7-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="e1de7-117">Kiirkaardil **Kaasatavad kirjed** klõpsake **Filter** ja lisage varad, mida soovite aruandesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="e1de7-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="e1de7-118">Aruande loomiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="e1de7-119">Töökäsu tarbimise aruanne</span><span class="sxs-lookup"><span data-stu-id="e1de7-119">Work order consumption report</span></span>

<span data-ttu-id="e1de7-120">Kui olete sisestanud töökäskude tarbimise, saate töökäsu tarbimise aruande printida.</span><span class="sxs-lookup"><span data-stu-id="e1de7-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="e1de7-121">Aruanne kuvab tunde, tunni kulusid, kauba kulusid ja töökäskude kohta sisestatud kulusid.</span><span class="sxs-lookup"><span data-stu-id="e1de7-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="e1de7-122">Klõpsake **Varahaldus** > **Aruanded** > **Töökäsud** > **Töökäsu tarbimine**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="e1de7-123">Dialoogiboksis **Töökäsu tarbimine** valige parameetrid ja üksikasja tase, mida soovite aruandesse kaasata, valides **Jah** asjakohastel tumblernuppudel ja sisestades töö asukoha taseme jaotisesse **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="e1de7-124">Valige kuupäevaintervall jaotises **Kuupäevad**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="e1de7-125">Kiirkaardil **Sihtkoht** valige, kas soovite aruande kuvada ekraanil, printida või salvestada faili või meilina.</span><span class="sxs-lookup"><span data-stu-id="e1de7-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="e1de7-126">Vajaduse korral saate valida, milliseid konkreetseid töökäske aruandes kuvada.</span><span class="sxs-lookup"><span data-stu-id="e1de7-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="e1de7-127">Kiirkaardil **Kaasatavad kirjed** klõpsake **Filter** ja lisage töökäsud, mida soovite aruandesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="e1de7-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="e1de7-128">Aruande loomiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1de7-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="e1de7-129">Samuti saate luua [töökäsu aruande](../work-orders/work-order-report.md), mis sisaldab rohkem töökäsu üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e1de7-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]