---
title: Tagastatud kauba kontrolli edastamine
description: Tagastatud kauba registreerimisel määrake, kas kaup saadetakse enne lattu tagasi saatmist kontrolli või likvideeritakse mõnel muul viisil.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e8205db277715f4f4f9c1ee589f264c0ded6617
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426283"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="1841f-103">Tagastatud kauba kontrolli edastamine</span><span class="sxs-lookup"><span data-stu-id="1841f-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1841f-104">Tagastatud kauba registreerimisel võite määrata, et kaup saadetaks enne lattu tagasi saatmist kontrolli või likvideeritakse mõnel muul viisil.</span><span class="sxs-lookup"><span data-stu-id="1841f-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="1841f-105">Klõpsake valikuid **Laohaldus** \> **Töölehed** \> **Kauba saabumine** \> **Kauba saabumine**.</span><span class="sxs-lookup"><span data-stu-id="1841f-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="1841f-106">\-Või-</span><span class="sxs-lookup"><span data-stu-id="1841f-106">\-or-</span></span>
    
    <span data-ttu-id="1841f-107">Klõpsake valikuid **Laohaldus** \> **Töölehed** \> **Kauba saabumine** \> **Materjalid tootmisse**.</span><span class="sxs-lookup"><span data-stu-id="1841f-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="1841f-108">Registreerige kauba sissetulek nagu tavaliselt vormil **Asukoha tööleht**.</span><span class="sxs-lookup"><span data-stu-id="1841f-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="1841f-109">Lisateavet tagastatud kaupade sissetuleku registreerimise kohta vt teemast <A href="register-the-receipt-of-returned-items.md">Tagastatud kauba sissetuleku registreerimine</A></span><span class="sxs-lookup"><span data-stu-id="1841f-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="1841f-110">Valige vahekaardil **Vaikeväärtused** alas **Töötlusviis** lahter **Vahelao haldus**.</span><span class="sxs-lookup"><span data-stu-id="1841f-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="1841f-111">See paneb süsteemi vahelao orderit looma ja kontrolli teostav isik või osakond vastab sellele orderile vormi **Vahelao order** abil.</span><span class="sxs-lookup"><span data-stu-id="1841f-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="1841f-112">Vt ka</span><span class="sxs-lookup"><span data-stu-id="1841f-112">See also</span></span>

[<span data-ttu-id="1841f-113">Tagastatud kaupade kontrollist läbi viimine</span><span class="sxs-lookup"><span data-stu-id="1841f-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="1841f-114">Tagastatud kaupade likvideerimise viisi määratlemine</span><span class="sxs-lookup"><span data-stu-id="1841f-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

