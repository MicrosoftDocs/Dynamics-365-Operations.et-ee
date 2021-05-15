---
title: Töö jääb blokeerituks
description: Töö jääb blokeerituks
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924126"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="0fca8-103">Töö jääb blokeerituks</span><span class="sxs-lookup"><span data-stu-id="0fca8-103">Work remains blocked</span></span>

<span data-ttu-id="0fca8-104">Tõrkekood: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="0fca8-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="0fca8-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="0fca8-105">Symptoms</span></span>

<span data-ttu-id="0fca8-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="0fca8-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0fca8-107">Töö %1 jääb blokeerituks, kuna seotud voo %2 olek on %3.</span><span class="sxs-lookup"><span data-stu-id="0fca8-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="0fca8-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="0fca8-108">Cause</span></span>

<span data-ttu-id="0fca8-109">Tööd töödeldakse voos ja sellelt ei saa blokeeringut eemaldada nagu on näidatud ühes järgnevast tingimustest:</span><span class="sxs-lookup"><span data-stu-id="0fca8-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="0fca8-110">Vahekaardil **Blokeerimise põhjused** väli **Töö blokeerimise põhjused** on ühe või mitme rea väärtuseks seatud *Voo töötlemine*.</span><span class="sxs-lookup"><span data-stu-id="0fca8-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="0fca8-111">Kui valite **Voog**  **Seotud teabe** grupist **Seostuva teabe** Tegevuspaani vahekaardil, on **Voo oleku** väli seatud suvandile *Töös*.</span><span class="sxs-lookup"><span data-stu-id="0fca8-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="0fca8-112">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="0fca8-112">Resolution</span></span>

<span data-ttu-id="0fca8-113">Tegevuspaani vahekaardil **Seotud teave** grupis **Seotud teave** valige **Voog**.</span><span class="sxs-lookup"><span data-stu-id="0fca8-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="0fca8-114">Siis valige **Voo** lehel, Tegevuspaanil, **Voo** vahekaardil **Voo** grupis **Vooandmete puhastamine**.</span><span class="sxs-lookup"><span data-stu-id="0fca8-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="0fca8-115">Vastukaal</span><span class="sxs-lookup"><span data-stu-id="0fca8-115">Workaround</span></span>

<span data-ttu-id="0fca8-116">Kui eelmised sammud probleemi ei lahendanud, saate töö järgmiste sammude abil tühistada.</span><span class="sxs-lookup"><span data-stu-id="0fca8-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="0fca8-117">Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="0fca8-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="0fca8-118">Väljal **Töö ID** määrake töö ID, mida soovite tühistada ja millel on **Töö oleku** väärtuseks kas *Ava*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.</span><span class="sxs-lookup"><span data-stu-id="0fca8-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="0fca8-119">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fca8-119">Select **OK**.</span></span>
1. <span data-ttu-id="0fca8-120">Valige **Jah**, et kinnitada, et soovite töö tühistada.</span><span class="sxs-lookup"><span data-stu-id="0fca8-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="0fca8-121">Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="0fca8-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
