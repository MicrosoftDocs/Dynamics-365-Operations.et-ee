---
title: Kaubal ei saa olla kooslust ega valemit
description: Kui proovite tellimust kinnitada, kuvatakse kauba kinnitamise ajal tõrketeade. See tähendab, et kaubal ei saa olla kooslust (BOM) ega valemit.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294056"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="aa615-104">Kaubal ei saa olla kooslust ega valemit</span><span class="sxs-lookup"><span data-stu-id="aa615-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="aa615-105">Tõrkekood: PRO2614</span><span class="sxs-lookup"><span data-stu-id="aa615-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="aa615-106">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="aa615-106">Symptoms</span></span>

<span data-ttu-id="aa615-107">Kui proovite tellimust kinnitada, kuvatakse kauba kinnitamise ajal järgnev tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="aa615-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="aa615-108">Kaubal ei saa olla kooslust või valemit</span><span class="sxs-lookup"><span data-stu-id="aa615-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="aa615-109">Lahendus</span><span class="sxs-lookup"><span data-stu-id="aa615-109">Resolution</span></span>

<span data-ttu-id="aa615-110">Koosluse (BOM) või valemiga kaubad peavad olema *plaanimiskauba*, *koosluse* või *valemi* tüüpi.</span><span class="sxs-lookup"><span data-stu-id="aa615-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="aa615-111">Kauba tüübi muutmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="aa615-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="aa615-112">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="aa615-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="aa615-113">Avage asjakohane toode.</span><span class="sxs-lookup"><span data-stu-id="aa615-113">Open the relevant product.</span></span>
1. <span data-ttu-id="aa615-114">Kiirkaardil **Projekteeri** määrake välja **Tootmise tüüp** väärtuseks *Planeeritav kaup*, *kooslus* või *valem*.</span><span class="sxs-lookup"><span data-stu-id="aa615-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
