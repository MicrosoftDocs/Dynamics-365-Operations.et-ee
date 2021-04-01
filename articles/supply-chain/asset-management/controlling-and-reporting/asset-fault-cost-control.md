---
title: Vara vea kulujuhtimine
description: Selles teemas selgitatakse vara vea kulujuhtimist Varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c25b3efbd0f2f0ec22a08aeac54ffb7fd9398c83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253826"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="fbc53-103">Vara vea kulujuhtimine</span><span class="sxs-lookup"><span data-stu-id="fbc53-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fbc53-104">Varahalduses saate arvutada vara vea registreerimiste kulusid, et saada ülevaate tegelikest kuludest võrreldes eelarvekuludega.</span><span class="sxs-lookup"><span data-stu-id="fbc53-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="fbc53-105">Tegelikud kulud põhinevad sisestatud kannetel.</span><span class="sxs-lookup"><span data-stu-id="fbc53-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="fbc53-106">Kuupäev on vea kuupäev, mil sümptom registreeriti.</span><span class="sxs-lookup"><span data-stu-id="fbc53-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="fbc53-107">Klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vea kulujuhtimine**.</span><span class="sxs-lookup"><span data-stu-id="fbc53-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="fbc53-108">Valige dialoogiaknas **Vara vea kulujuhtimine** finantsdimensioon, mida soovite arvutusse kaasata, kui see on nõutav.</span><span class="sxs-lookup"><span data-stu-id="fbc53-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="fbc53-109">Kui te ei soovi nulli kuluga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.</span><span class="sxs-lookup"><span data-stu-id="fbc53-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="fbc53-110">Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et kulujuhtimise read oleksid seotud töö asukohtadega.</span><span class="sxs-lookup"><span data-stu-id="fbc53-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="fbc53-111">Näiteks kui sisestate väljale numbri "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik vara vea kulujuhtimise read töö asukoha kohta ja seetõttu võib rea tunnid liita töö asukohast, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="fbc53-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="fbc53-112">Kui sisestate numbri "0" väljale **Tase**, näete üksikasjalikku tulemust, mis näitab kõiki vara vea kulujuhtimise ridu kõigi töö asukoha tasemete puhul, millega need on seotud.</span><span class="sxs-lookup"><span data-stu-id="fbc53-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="fbc53-113">Kui soovite otsingut piirata, saate valida kindlad varad, vea kuupäevad ja vea põhjused **Lisamiskirjed** kiirkaardi valikus.</span><span class="sxs-lookup"><span data-stu-id="fbc53-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="fbc53-114">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="fbc53-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="fbc53-115">Valige nupud **Rühmitusalus**, et vaadata arvutuse soovitud üksikasja taset.</span><span class="sxs-lookup"><span data-stu-id="fbc53-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="fbc53-116">Valitud nupud **Rühmitusalus** on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="fbc53-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="fbc53-117">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="fbc53-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="fbc53-118">Näide</span><span class="sxs-lookup"><span data-stu-id="fbc53-118">Example</span></span>

<span data-ttu-id="fbc53-119">Selles näites kuvatakse vara vea kulujuhtimise arvutamist.</span><span class="sxs-lookup"><span data-stu-id="fbc53-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="fbc53-120">**Algne eelarve** väli näitab eelarve kulusid töökäskude prognoosist.</span><span class="sxs-lookup"><span data-stu-id="fbc53-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="fbc53-121">Väljal **Tegelik kulu** kuvatakse töökäskudesse sisestatud kulud.</span><span class="sxs-lookup"><span data-stu-id="fbc53-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="fbc53-122">Väli **Kooskõlastatud kulu** näitab kogukulusid, millele teie ettevõte on pühendunud seoses töökäskudega.</span><span class="sxs-lookup"><span data-stu-id="fbc53-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Joonis 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="fbc53-124">Teavet vigade häälestamise kohta vaadake teemast [Veahaldus](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="fbc53-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]