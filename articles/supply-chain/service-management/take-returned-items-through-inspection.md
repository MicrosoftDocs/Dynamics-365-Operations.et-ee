---
title: Tagastatud kaupade kontrollist läbi viimine
description: Viige tagastatud kaubad kontrollist läbi.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426419"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="bdc70-103">Tagastatud kaupade kontrollist läbi viimine</span><span class="sxs-lookup"><span data-stu-id="bdc70-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="bdc70-104">Klõpsake valikuid **Varude haldamine** \> **Perioodiline** \> **Kvaliteedijuhtimine** \> **Vahelao orderid**.</span><span class="sxs-lookup"><span data-stu-id="bdc70-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="bdc70-105">Määrake tellimusrea asukoht, mis vastab teie uuritavale tagastatud kaubale.</span><span class="sxs-lookup"><span data-stu-id="bdc70-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="bdc70-106">Vahelao orderi saab seostada ainult ühe kaubakoodiga.</span><span class="sxs-lookup"><span data-stu-id="bdc70-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="bdc70-107">Kui ühe saadetisega tagastatakse kümme kaupa erinevate kaubakoodidega ja saadetakse vahelattu, luuakse kümme individuaalset vahelao orderit.</span><span class="sxs-lookup"><span data-stu-id="bdc70-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="bdc70-108">Pärast kauba läbivaatamist tehke valik väljal **Likvideerimiskood**, et näidata, mida tuleb kaubaga teha ja kuidas tuleb seotud finantskandeid käsitseda.</span><span class="sxs-lookup"><span data-stu-id="bdc70-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="bdc70-109">Näidete hulka kuuluvad kauba tagastamine lattu ja kliendile hüvitamine, kauba mahakandmine ja asenduskauba saatmine kliendile või kauba tagastamine kliendile ilma kreeditita.</span><span class="sxs-lookup"><span data-stu-id="bdc70-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="bdc70-110">Kui mitut tagastatud kaupa üksiku kauba koodi partiis ei saa määrata samale likvideerimiskoodile, peate tükeldama vahelao orderi (<STRONG>Funktsioonid</STRONG> &gt; <STRONG>Tükelda</STRONG>), et määrata igale alampartiile erinev likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="bdc70-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="bdc70-111">Uurimise lõpetamisel klõpsake valikut **Kinnita lõpetamine**, et vabastada tagastatud kaubad ja luua kauba saabumise töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="bdc70-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="bdc70-112">Kaubad saanud isik või osakond töötleb siis töölehte lattu tagastatavate kaupade osas.</span><span class="sxs-lookup"><span data-stu-id="bdc70-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="bdc70-113">või</span><span class="sxs-lookup"><span data-stu-id="bdc70-113">–or–</span></span>
    
    <span data-ttu-id="bdc70-114">Lõpetage vahelao order ja teisaldage kaubad tagasi lattu nupu **Varud** ühe funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="bdc70-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="bdc70-115">Muudatuste salvestamiseks sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="bdc70-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="bdc70-116">Vt ka</span><span class="sxs-lookup"><span data-stu-id="bdc70-116">See also</span></span>

[<span data-ttu-id="bdc70-117">Tagastatud kaupade likvideerimise viisi määratlemine</span><span class="sxs-lookup"><span data-stu-id="bdc70-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


