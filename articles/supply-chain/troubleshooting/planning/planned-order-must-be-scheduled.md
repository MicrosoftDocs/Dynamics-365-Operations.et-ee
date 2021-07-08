---
title: Plaanitud tootmistellimus tuleb enne kinnitamist planeerida
description: Kui proovite plaanitud tellimust kinnitada, kuvatakse tõrketeade, mis ütleb, et tellimus tuleb enne kinnitamist ajastada.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294060"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="7b457-103">Plaanitud tootmistellimus tuleb enne kinnitamist planeerida</span><span class="sxs-lookup"><span data-stu-id="7b457-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="7b457-104">Tõrkekood: SYS309802</span><span class="sxs-lookup"><span data-stu-id="7b457-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b457-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="7b457-105">Symptoms</span></span>

<span data-ttu-id="7b457-106">Kui proovite plaanitud tellimust kindlustada, kuvatakse järgmine tõrketeade:</span><span class="sxs-lookup"><span data-stu-id="7b457-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="7b457-107">Plaanitud tootmistellimus peab olema plaanitud enne, kui seda saab kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b457-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="7b457-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="7b457-108">Cause</span></span>

<span data-ttu-id="7b457-109">Ajastatud algus- ja lõppkuupäevad ei tohi olla tühjad.</span><span class="sxs-lookup"><span data-stu-id="7b457-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b457-110">Lahendus</span><span class="sxs-lookup"><span data-stu-id="7b457-110">Resolution</span></span>

<span data-ttu-id="7b457-111">Plaanitud tellimuse algus- ja lõppkuupäevade määramiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7b457-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="7b457-112">Avage **Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused**.</span><span class="sxs-lookup"><span data-stu-id="7b457-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="7b457-113">Avage asjakohane plaanitud tellimus.</span><span class="sxs-lookup"><span data-stu-id="7b457-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="7b457-114">Määrake kiirkaardi **Üldine** jaotises **Ajastatud** kuupäevad väljadel **Alguskuupäev** ja **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="7b457-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
