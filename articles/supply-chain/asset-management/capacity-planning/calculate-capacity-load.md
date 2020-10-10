---
title: Täiskoormuse arvutamine
description: Selles teemas tutvustatakse, kuidas arvutada täiskoormust varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5015955338a4cbc2b51585d6297756f20dccee8b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888734"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="1c65d-103">Arvuta täiskoormus</span><span class="sxs-lookup"><span data-stu-id="1c65d-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1c65d-104">Varahalduses saate arvutada täiskoormust järgmiste näitajate kohta:</span><span class="sxs-lookup"><span data-stu-id="1c65d-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="1c65d-105">hooldusgraafiku read</span><span class="sxs-lookup"><span data-stu-id="1c65d-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="1c65d-106">töökäsud, mida pole veel plaanitud</span><span class="sxs-lookup"><span data-stu-id="1c65d-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="1c65d-107">plaanitud töökäsud</span><span class="sxs-lookup"><span data-stu-id="1c65d-107">scheduled work orders</span></span>

<span data-ttu-id="1c65d-108">See on kasulik, kui soovite saada ülevaate konkreetse perioodi oodatavast täiskoormusest.</span><span class="sxs-lookup"><span data-stu-id="1c65d-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="1c65d-109">Täiskoormuse arvutuse saab teha kõigile varadele või valitud varadele.</span><span class="sxs-lookup"><span data-stu-id="1c65d-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="1c65d-110">Samuti saate teha arvutuse hoolduskatkestuse toimingute või töökäsu kaustade kohta.</span><span class="sxs-lookup"><span data-stu-id="1c65d-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="1c65d-111">Klõpsake **Varahaldus** > **Päringud** > **Täiskoormus** või **Varahaldus** > **Üldine** > **Töökäsu kaustad** > **Kõik töökäsu kaustad** / **Aktiivsed töökäsu kaustad** > valige loendist töökäsu kaust > nupp **Täiskoormus** või **Varahaldus** > **Üldine** > **Hoolduskatkestuse toimingud** > **Kõik hoolduskatkestuse toimingud** / **Aktiivsed hoolduskatkestuse toimingud** > valige loendist hooldustoiming > nupp **Täiskoormus**.</span><span class="sxs-lookup"><span data-stu-id="1c65d-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="1c65d-112">Dialoogiboksis **Arvuta täiskoormus** valige arvutuse periood väljadel **Alguskuupäev/aeg** ja **Lõppkuupäev/aeg**.</span><span class="sxs-lookup"><span data-stu-id="1c65d-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="1c65d-113">Valige "Jah" tumblernupul **Kaasa hooldusgraafik**, kui soovite arvutusse kaasata hooldusgraafiku read.</span><span class="sxs-lookup"><span data-stu-id="1c65d-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="1c65d-114">Valige "Jah" tumblernupul **Kaasa töökäsk**, kui soovite arvutusse kaasata töökäsu tööd.</span><span class="sxs-lookup"><span data-stu-id="1c65d-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="1c65d-115">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade täiskoormuse ridu te soovite.</span><span class="sxs-lookup"><span data-stu-id="1c65d-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="1c65d-116">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ja töökäsud ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="1c65d-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="1c65d-117">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu ja kõiki töökäske kõigi töö asukohtade tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="1c65d-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="1c65d-118">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c65d-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="1c65d-119">Gruppides **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset.</span><span class="sxs-lookup"><span data-stu-id="1c65d-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="1c65d-120">Alloleval kuvatõmmisel on gruppide **Rühmitusalus** nupud esile tõstetud sinise värviga.</span><span class="sxs-lookup"><span data-stu-id="1c65d-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="1c65d-121">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="1c65d-121">Click on a button to activate or deactivate it.</span></span>

    ![Joonis 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="1c65d-123">Kui soovite keskenduda ainult planeeritud töökäskude võimsuse planeerimisele, vaadake teemat [Täiskoormuse arvutamine plaanitud töökäskude kohta](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="1c65d-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

