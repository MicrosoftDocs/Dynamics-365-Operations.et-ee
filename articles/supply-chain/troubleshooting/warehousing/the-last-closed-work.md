---
title: Viimane suletud töörida peab olema pane
description: Viimane suletud töörida peab olema pane
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924371"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="f9b9f-103">Viimane suletud töörida peab olema pane</span><span class="sxs-lookup"><span data-stu-id="f9b9f-103">The last closed work line must be a put</span></span>

<span data-ttu-id="f9b9f-104">Tõrkekood: WAX1285</span><span class="sxs-lookup"><span data-stu-id="f9b9f-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="f9b9f-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="f9b9f-105">Symptoms</span></span>

<span data-ttu-id="f9b9f-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="f9b9f-106">The system shows the following error message:</span></span>

> <span data-ttu-id="f9b9f-107">Viimane suletud töörida peab olema pane.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="f9b9f-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="f9b9f-108">Cause</span></span>

<span data-ttu-id="f9b9f-109">Tööd ei saa praeguses olekus tühistada.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="f9b9f-110">Viimasel tööreal on väli **Töö olek** seatud *Suletud*, kuid välja **Töö tüüp** väärtuseks pole seatud *Pane*.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="f9b9f-111">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="f9b9f-111">Resolution</span></span>

<span data-ttu-id="f9b9f-112">Loa tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="f9b9f-113">Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="f9b9f-114">Väljal **Töö ID** määrake töö ID, mida soovite tühistada.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="f9b9f-115">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-115">Select **OK**.</span></span>
1. <span data-ttu-id="f9b9f-116">Valige **Jah**, et kinnitada, et soovite töö tühistada.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="f9b9f-117">Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="f9b9f-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
