---
title: Täiskoormuse arvutamine
description: Selles teemas tutvustatakse, kuidas arvutada täiskoormust varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886789"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="6c9ea-103">Täiskoormuse arvutamine</span><span class="sxs-lookup"><span data-stu-id="6c9ea-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6c9ea-104">Varahalduses saate arvutada täiskoormust järgmiste näitajate kohta:</span><span class="sxs-lookup"><span data-stu-id="6c9ea-104">In Asset Management, you can calculate capacity load on</span></span>

- <span data-ttu-id="6c9ea-105">hooldusgraafiku read</span><span class="sxs-lookup"><span data-stu-id="6c9ea-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="6c9ea-106">töökäsud, mida pole veel plaanitud</span><span class="sxs-lookup"><span data-stu-id="6c9ea-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="6c9ea-107">plaanitud töökäsud</span><span class="sxs-lookup"><span data-stu-id="6c9ea-107">scheduled work orders</span></span>

<span data-ttu-id="6c9ea-108">See on kasulik, kui soovite saada ülevaate konkreetse perioodi oodatavast täiskoormusest.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="6c9ea-109">Täiskoormuse arvutuse saab teha kõigile varadele või valitud varadele.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="6c9ea-110">Samuti saate teha arvutuse hoolduskatkestuse toimingute või töökäsu kaustade kohta.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="6c9ea-111">Klõpsake **Varahaldus** > **Päringud** > **Täiskoormus** või **Varahaldus** > **Üldine** > **Töökäsu kaustad** > **Kõik töökäsu kaustad** / **Aktiivsed töökäsu kaustad** > valige loendist töökäsu kaust > nupp **Täiskoormus** või **Varahaldus** > **Üldine** > **Hoolduskatkestuse toimingud** > **Kõik hoolduskatkestuse toimingud** / **Aktiivsed hoolduskatkestuse toimingud** > valige loendist hooldustoiming > nupp **Täiskoormus**.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="6c9ea-112">Dialoogiboksis **Arvuta täiskoormus** valige arvutuse periood väljadel **Alguskuupäev/aeg** ja **Lõppkuupäev/aeg**.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="6c9ea-113">Valige "Jah" tumblernupul **Kaasa hooldusgraafik**, kui soovite arvutusse kaasata hooldusgraafiku read.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="6c9ea-114">Valige "Jah" tumblernupul **Kaasa töökäsk**, kui soovite arvutusse kaasata töökäsu tööd.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="6c9ea-115">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade täiskoormuse ridu te soovite.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> <span data-ttu-id="6c9ea-116">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ja töökäsud ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="6c9ea-117">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu ja kõiki töökäske kõigi töö asukohtade tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="6c9ea-118">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="6c9ea-119">Toimingupaani rühmades **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="6c9ea-120">Valitud toimingupaani grupi nupud on sinise värviga esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="6c9ea-121">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-121">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="6c9ea-122">Alloleval joonisel kuvatakse näidet liidesest.</span><span class="sxs-lookup"><span data-stu-id="6c9ea-122">The figure below shows an example of the interface.</span></span>

![Joonis 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="6c9ea-124">Kui soovite keskenduda ainult planeeritud töökäskude võimsuse planeerimisele, vaadake teemat [Täiskoormuse arvutamine plaanitud töökäskude kohta](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="6c9ea-124">If you want to focus only on capacity planning regarding scheduled work orders, refer to [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

