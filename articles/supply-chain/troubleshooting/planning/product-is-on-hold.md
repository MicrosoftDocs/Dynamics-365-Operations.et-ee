---
title: Toode on kannete jaoks ootel
description: Pärast plaanimistellimuste kinnitamist saate tõrketeate, mis kinnitab, et kaup on kannete jaoks ootel.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301275"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="5c9c5-103">Toode on kannete jaoks ootel</span><span class="sxs-lookup"><span data-stu-id="5c9c5-103">Product is on hold for transactions</span></span>

<span data-ttu-id="5c9c5-104">Tõrkekood: SYS13295</span><span class="sxs-lookup"><span data-stu-id="5c9c5-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="5c9c5-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="5c9c5-105">Symptoms</span></span>

<span data-ttu-id="5c9c5-106">Pärast plaanitud tellimuste kinnitamist kuvatakse järgmine tõrketeade:</span><span class="sxs-lookup"><span data-stu-id="5c9c5-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="5c9c5-107">Kaup %1 on ootel kannete jaoks asukohas %2.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="5c9c5-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="5c9c5-108">Cause</span></span>

<span data-ttu-id="5c9c5-109">Blokeeritud kaupade kirjeldamisel kasutab süsteem tingimusi *blokeeritud*, *peatatud* ja *ootel*.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="5c9c5-110">See tõrge tähendab, et kaup on seatud tellimuse vaikesätetes väärtusele **Peatatud**.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="5c9c5-111">Kui kaup on blokeeritud ja te lisate selle ostu- või müügitellimuse reale, saate hoiatusteate.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="5c9c5-112">Kui kaup on blokeeritud, näiteks saatelehe või arve sisestamisel, ei saa ostu- või müügitellimuse reaga seotud laokandeid muuta.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="5c9c5-113">Saate blokeerida ostetud kauba ja samaaegselt kauba müüa.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="5c9c5-114">Sel juhul on märkeruut **Peatatud** ostutellimusel märgitud, kuid kaup pole laovarudes või müügitellimusel blokeeritud.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="5c9c5-115">Järgnevalt on toodud mõned tingimused, mis võivad põhjustada kaubakoodi blokeerimise müügilt.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="5c9c5-116">Kaup on alles arenduses või tootmises.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="5c9c5-117">Seetõttu ei soovi te seda müüa ega reserveerida.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="5c9c5-118">Olete saanud palju praakkaupu ja vead tuleb parandada enne kauba müümist.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="5c9c5-119">Seda tüüpi juhtumide korral saate vahepealseks ajaks kauba blokeerida, kuni probleem on lahendatud.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="5c9c5-120">Kui kaup on blokeeritud ja koostate tagastustellimuse rea, saate teate.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="5c9c5-121">Te ei saa blokeerida kauba seeriaid ega selle saatepartiid.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="5c9c5-122">Kui kauba osi peab blokeerima, saate seda teha, varusid teisaldades või blokeerides kogu antud perioodi kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="5c9c5-123">Lahendus</span><span class="sxs-lookup"><span data-stu-id="5c9c5-123">Resolution</span></span>

- <span data-ttu-id="5c9c5-124">Avage leht **Kauba tellimuse vaikesätted** leht ja tühjendage märkeruut **Peatatud**.</span><span class="sxs-lookup"><span data-stu-id="5c9c5-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
