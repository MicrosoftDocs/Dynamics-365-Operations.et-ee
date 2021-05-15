---
title: Kasutajale määratud tööd ei saa tühistada
description: Kasutajale määratud tööd ei saa tühistada
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924397"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="d5cb3-103">Kasutajale määratud tööd ei saa tühistada</span><span class="sxs-lookup"><span data-stu-id="d5cb3-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="d5cb3-104">Tõrkekood: WAX708</span><span class="sxs-lookup"><span data-stu-id="d5cb3-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="d5cb3-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="d5cb3-105">Symptoms</span></span>

<span data-ttu-id="d5cb3-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="d5cb3-106">The system shows the following error message:</span></span>

> <span data-ttu-id="d5cb3-107">Kasutajale määratud tööd ei saa tühistada.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="d5cb3-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="d5cb3-108">Cause</span></span>

<span data-ttu-id="d5cb3-109">Töö on blokeeritud ja seda ei saa tühistada.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="d5cb3-110">Selle kinnitamiseks avage töö ID ja seejärel avage **Üldine** vahekaart. Kui töö on lukustatud, seatakse välja **Töö olek** *Pooleli* ja väljale **Lukustus** seatakse kasutaja ID.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="d5cb3-111">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="d5cb3-111">Resolution</span></span>

<span data-ttu-id="d5cb3-112">Loa tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="d5cb3-113">Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="d5cb3-114">Väljal **Töö ID** määrake töö ID, mida soovite tühistada.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="d5cb3-115">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-115">Select **OK**.</span></span>
1. <span data-ttu-id="d5cb3-116">Valige **Jah**, et kinnitada, et soovite töö tühistada.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="d5cb3-117">Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="d5cb3-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
