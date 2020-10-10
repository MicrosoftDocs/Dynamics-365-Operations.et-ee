---
title: Kauba prognoosi arvutamine
description: Selles teemas tutvustatakse, kuidas arvutada kauba prognoosi varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f8f38ac7bfb270f648cd561da50ee5477721ab47
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888709"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="219dd-103">Kauba prognoosi arvutamine</span><span class="sxs-lookup"><span data-stu-id="219dd-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="219dd-104">Nii nagu saate teha eelmises jaotises kirjeldatud täiskoormuse arvutusi, saate samuti teha kauba prognoosi arvutusi järgmiste näitajate põhjal:</span><span class="sxs-lookup"><span data-stu-id="219dd-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="219dd-105">hooldusgraafiku read</span><span class="sxs-lookup"><span data-stu-id="219dd-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="219dd-106">töökäsud, mida pole veel plaanitud</span><span class="sxs-lookup"><span data-stu-id="219dd-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="219dd-107">plaanitud töökäsud</span><span class="sxs-lookup"><span data-stu-id="219dd-107">scheduled work orders</span></span>

<span data-ttu-id="219dd-108">See on kasulik, kui soovite saada ülevaadet konkreetse perioodi oodatavast kauba tarbimisest (nii varuosad kui ka muu kaup, mis on vajalik töökäsu lõpetamiseks).</span><span class="sxs-lookup"><span data-stu-id="219dd-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="219dd-109">Kauba prognoosi arvutuse saab teha kõigile varadele või valitud varadele.</span><span class="sxs-lookup"><span data-stu-id="219dd-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="219dd-110">Samuti saate teha arvutuse hoolduskatkestuse toimingule (**Kõik hoolduskatkestuse toimingud** või **Aktiivsed hoolduskatkestuse toimingud**) või töökäsu kaustale (**Kõik töökäsu kaustad** või **Aktiivsed töökäsu kaustad**).</span><span class="sxs-lookup"><span data-stu-id="219dd-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="219dd-111">Klõpsake **Varahaldus** > **Päringud** > **Kauba prognoos** või **Varahaldus** > **Üldine** > **Töökäsu kaustad** > **Kõik töökäsu kaustad** / **Aktiivsed töökäsu kaustad** > valige loendist töökäsu kaust > nupp **Kauba prognoos** või **Varahaldus** > **Üldine** > **Hoolduskatkestuse toimingud** > **Kõik hoolduskatkestuse toimingud** / **Aktiivsed hoolduskatkestuse toimingud** > valige loendist hoolduskatkestuse toiming > nupp **Kauba prognoos**.</span><span class="sxs-lookup"><span data-stu-id="219dd-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="219dd-112">Dialoogiboksis **Arvuta kauba prognoos** valige arvutuse periood väljadel **Alguskuupäev/aeg** ja **Lõppkuupäev/aeg**.</span><span class="sxs-lookup"><span data-stu-id="219dd-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="219dd-113">Valige "Jah" tumblernupul **Kaasa hooldusgraafik**, kui soovite prognoosi arvutusse kaasata hooldusgraafiku read.</span><span class="sxs-lookup"><span data-stu-id="219dd-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="219dd-114">Valige "Jah" tumblernupul **Kaasa töökäsk**, kui soovite prognoosi arvutusse kaasata töökäsu tööd.</span><span class="sxs-lookup"><span data-stu-id="219dd-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="219dd-115">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade kauba prognoosi ridu te soovite.</span><span class="sxs-lookup"><span data-stu-id="219dd-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="219dd-116">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ja töökäsud ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="219dd-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="219dd-117">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu ja kõiki töökäske kõigi töö asukoha tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="219dd-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="219dd-118">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="219dd-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="219dd-119">Gruppides **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset.</span><span class="sxs-lookup"><span data-stu-id="219dd-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="219dd-120">Alloleval kuvatõmmisel on gruppide **Rühmitusalus** nupud esile tõstetud sinise värviga.</span><span class="sxs-lookup"><span data-stu-id="219dd-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="219dd-121">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="219dd-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="219dd-122">Klõpsake nuppu **Kuva dimensioonid**, kui soovite näha kaubaga seotud toote, lao ja jälgimise dimensioone.</span><span class="sxs-lookup"><span data-stu-id="219dd-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="219dd-123">Valige sobivad märkeruudud ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="219dd-123">Select the relevant check boxes, and click **OK**.</span></span>

![Joonis 1](media/02-capacity-planning.png)
