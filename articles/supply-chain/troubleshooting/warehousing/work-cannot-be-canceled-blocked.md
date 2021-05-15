---
title: Tööd ei saa tühistada, kuna see on blokeeritud
description: Tööd ei saa tühistada, kuna see on blokeeritud
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924275"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="35be1-103">Tööd ei saa tühistada, kuna see on blokeeritud</span><span class="sxs-lookup"><span data-stu-id="35be1-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="35be1-104">Tõrkekood: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="35be1-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="35be1-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="35be1-105">Symptoms</span></span>

<span data-ttu-id="35be1-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="35be1-106">The system shows the following error message:</span></span>

> <span data-ttu-id="35be1-107">Tööd %1 ei saa tühistada, kuna see on põhjuse tüübi %2tõttu blokeeritud.</span><span class="sxs-lookup"><span data-stu-id="35be1-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="35be1-108">Tööl peab olema blokeering tühistatud enne kui selle saab tühistada.</span><span class="sxs-lookup"><span data-stu-id="35be1-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="35be1-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="35be1-109">Cause</span></span>

<span data-ttu-id="35be1-110">Töö on blokeeritud ja seda ei saa tühistada.</span><span class="sxs-lookup"><span data-stu-id="35be1-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="35be1-111">**Töö** lehel, vahekaardil **Üldine** on suvand **Blokeeritud** seatud väärtusele *Jah*.</span><span class="sxs-lookup"><span data-stu-id="35be1-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="35be1-112">See säte näitab, et töö on blokeeritud.</span><span class="sxs-lookup"><span data-stu-id="35be1-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="35be1-113">Vahekaart **Blokeerimise põhjused** näitab, miks töö blokeeriti.</span><span class="sxs-lookup"><span data-stu-id="35be1-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="35be1-114">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="35be1-114">Resolution</span></span>

<span data-ttu-id="35be1-115">Töö blokeerimise tühistamiseks valige vahekaart **Blokeerimise põhjused** ja järgige seejärel üht järgmistest sammudest:</span><span class="sxs-lookup"><span data-stu-id="35be1-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="35be1-116">Kui **Töö blokeerimise põhjuse** välja väärtuseks on seatud *Määratlemata põhjus*: Valige Tegevuspaanil vahekaardil **Töö** grupis **Töö** suvand **Tühista töö blokeering**.</span><span class="sxs-lookup"><span data-stu-id="35be1-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="35be1-117">Kui **Töö blokeerimise põhjuse** välja väärtuseks on seatud *Voo töötlemine*: valige Tegevuspaanil vahekaardil **Seostuv teabe** jaotises **Seotud teabe** grupis suvand **Voog**.</span><span class="sxs-lookup"><span data-stu-id="35be1-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="35be1-118">Siis valige **Voo** lehel, Tegevuspaanil, **Voo** vahekaardil **Voo** grupis **Vooandmete puhastamine**.</span><span class="sxs-lookup"><span data-stu-id="35be1-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="35be1-119">Vastukaal</span><span class="sxs-lookup"><span data-stu-id="35be1-119">Workaround</span></span>

<span data-ttu-id="35be1-120">Kui eelmised sammud probleemi ei lahendanud, saate töö järgmiste sammude abil tühistada.</span><span class="sxs-lookup"><span data-stu-id="35be1-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="35be1-121">Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="35be1-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="35be1-122">Väljal **Töö ID** määrake töö ID, mida soovite tühistada ja millel on **Töö oleku** väärtuseks kas *Ava*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.</span><span class="sxs-lookup"><span data-stu-id="35be1-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="35be1-123">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="35be1-123">Select **OK**.</span></span>
1. <span data-ttu-id="35be1-124">Valige **Jah**, et kinnitada, et soovite töö tühistada.</span><span class="sxs-lookup"><span data-stu-id="35be1-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="35be1-125">Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="35be1-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
