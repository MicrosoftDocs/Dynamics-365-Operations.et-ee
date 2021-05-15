---
title: Tööd ei saa tema oleku tõttu tühistada
description: Tööd ei saa tema oleku tõttu tühistada
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924251"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="d520f-103">Tööd ei saa tema oleku tõttu tühistada</span><span class="sxs-lookup"><span data-stu-id="d520f-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="d520f-104">Tõrkekood: WAX2190</span><span class="sxs-lookup"><span data-stu-id="d520f-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="d520f-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="d520f-105">Symptoms</span></span>

<span data-ttu-id="d520f-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="d520f-106">The system shows the following error message:</span></span>

> <span data-ttu-id="d520f-107">Tööd %1 ei saa tühistada, sest selle olek on %2.</span><span class="sxs-lookup"><span data-stu-id="d520f-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="d520f-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="d520f-108">Cause</span></span>

<span data-ttu-id="d520f-109">Tööd ei saa praeguses olekus tühistada.</span><span class="sxs-lookup"><span data-stu-id="d520f-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="d520f-110">Töö päisel või töö ridadel ei ole eeldatavat **Töö oleku** väärtust.</span><span class="sxs-lookup"><span data-stu-id="d520f-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="d520f-111">**Töö oleku** väli pole tööpäises seatud *Avatud* või *Pooleli*.</span><span class="sxs-lookup"><span data-stu-id="d520f-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="d520f-112">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="d520f-112">Resolution</span></span>

<span data-ttu-id="d520f-113">Loa tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d520f-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="d520f-114">Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="d520f-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="d520f-115">Väljal **Töö ID** määrake töö ID, mida soovite tühistada.</span><span class="sxs-lookup"><span data-stu-id="d520f-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="d520f-116">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d520f-116">Select **OK**.</span></span>
1. <span data-ttu-id="d520f-117">Valige **Jah**, et kinnitada, et soovite töö tühistada.</span><span class="sxs-lookup"><span data-stu-id="d520f-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="d520f-118">Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="d520f-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
