---
title: Hankija kood pole kindla toote ja kuupäeva jaoks autoriseeritud
description: Kui proovite plaanitud tellimust kinnitada või ostutellimusele rida lisada, saate tõrketeate, mis kinnitab, et hankija kood pole toote ja kuupäeva jaoks autoriseeritud.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294059"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="33196-103">Hankija kood pole kindla toote ja kuupäeva jaoks autoriseeritud</span><span class="sxs-lookup"><span data-stu-id="33196-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="33196-104">Tõrkekood: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="33196-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="33196-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="33196-105">Symptoms</span></span>

<span data-ttu-id="33196-106">Kui proovite plaanitud tellimust kindlustada, kuvatakse järgmine tõrketeade:</span><span class="sxs-lookup"><span data-stu-id="33196-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="33196-107">Hankija kood %1 pole autoriseeritud: %2, %3.</span><span class="sxs-lookup"><span data-stu-id="33196-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="33196-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="33196-108">Cause</span></span>

<span data-ttu-id="33196-109">Tõrge ilmneb, kuna välja **Kinnitatud hankija kontrollmeetod** väärtuseks on määratud toote puhul määratud *ainult Hoiatus* või *Keelatud* ja hankijal pole praegu õigust seda toodet tarnida.</span><span class="sxs-lookup"><span data-stu-id="33196-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="33196-110">Lahendus</span><span class="sxs-lookup"><span data-stu-id="33196-110">Resolution</span></span>

<span data-ttu-id="33196-111">Probleemi lahendamiseks keelake hankijalt vastava toote kontroll või kinnitage hankija.</span><span class="sxs-lookup"><span data-stu-id="33196-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="33196-112">Hankija tootekontrolli keelamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="33196-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="33196-113">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="33196-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="33196-114">Avage asjakohane toode.</span><span class="sxs-lookup"><span data-stu-id="33196-114">Open the relevant product.</span></span>
1. <span data-ttu-id="33196-115">Seadke kiirkaardil **Ost** **Kinnitatud hankija kontrollmeetod** välja väärtuseks, mis pole *ainult Hoiatus* või *Pole lubatud*.</span><span class="sxs-lookup"><span data-stu-id="33196-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="33196-116">Hankija tootekontrolli kinnitamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="33196-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="33196-117">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="33196-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="33196-118">Avage asjakohane kaup.</span><span class="sxs-lookup"><span data-stu-id="33196-118">Open the relevant item.</span></span>
1. <span data-ttu-id="33196-119">Klõpsake jaotise Tegumiriba vahekaardi **Ost** grupis **Kinnitatud hankija** suvandit **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="33196-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="33196-120">Valige loendi lehel **Kinnitatud hankijad**, et lisada rida jaotise ruudustikku ja seejärel määrake sellele järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="33196-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="33196-121">**Hankija** - valige praeguse toote kinnitamiseks hankija.</span><span class="sxs-lookup"><span data-stu-id="33196-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="33196-122">**Jõustumiskuupäev** - valige hankija kinnitatud esimene kuupäev.</span><span class="sxs-lookup"><span data-stu-id="33196-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="33196-123">**Aegumise kuupäev** - valige hankija kinnitatud viimane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="33196-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="33196-124">Lisateabe saamiseks vt jaotist [Kindlate toodete hankijate kinnitamine](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="33196-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
