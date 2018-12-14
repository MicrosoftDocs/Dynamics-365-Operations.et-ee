--- 
title: "Arvete ja võtmeandmete audit ostureskontro süsteemis"
description: "Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cc995b474e86272b49629f97e1b4d4b4fb597b9d
ms.openlocfilehash: 946076d682a10becdc2c4a8baff7f52de7893119
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="54dcb-103">Arvete ja võtmeandmete audit ostureskontro süsteemis</span><span class="sxs-lookup"><span data-stu-id="54dcb-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54dcb-104">Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud.</span><span class="sxs-lookup"><span data-stu-id="54dcb-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="54dcb-105">Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine.</span><span class="sxs-lookup"><span data-stu-id="54dcb-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="54dcb-106">Veenduge lehel Ostureskontro parameetrid, et valitud on suvand Lubage arvete võrdlemise kontrollimine, suvand Nõua kinnitust väljal Lahknevustega arvete sisestamine ning suvand Kolmesuunaline vastavusse viimine väljal Rea vastavusse viimise poliitika.</span><span class="sxs-lookup"><span data-stu-id="54dcb-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="54dcb-107">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="54dcb-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="54dcb-108">Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli.</span><span class="sxs-lookup"><span data-stu-id="54dcb-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="54dcb-109">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="54dcb-109">Create a purchase order</span></span>
1. <span data-ttu-id="54dcb-110">Avage valik **Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="54dcb-111">Klõpsake **Uus**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-111">Click **New**.</span></span>
3. <span data-ttu-id="54dcb-112">Sisestage väärtus väljale **Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="54dcb-113">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-113">Click **OK**.</span></span>
5. <span data-ttu-id="54dcb-114">Klõpsake käsku **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-114">Click **Add line**.</span></span>
6. <span data-ttu-id="54dcb-115">Sisestage väärtus väljale **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="54dcb-116">Klõpsake toimingupaanil valikut **Ost**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="54dcb-117">Klõpsake käsku **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="54dcb-118">Toote sissetuleku sisestamine</span><span class="sxs-lookup"><span data-stu-id="54dcb-118">Post a product receipt</span></span>
1. <span data-ttu-id="54dcb-119">Klõpsake toimingupaanil valikut **Vastuvõtt**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="54dcb-120">Klõpsake valikut **Toote sissetulek**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="54dcb-121">Sisestage väärtus väljale **Toote sissetulek**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="54dcb-122">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="54dcb-123">Hankija arve salvestamine ja vastendamine toote sissetulekuga</span><span class="sxs-lookup"><span data-stu-id="54dcb-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="54dcb-124">Klõpsake toimingupaanil valikut **Arve > Arve**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="54dcb-125">Sisestage väärtus väljale **Arv**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="54dcb-126">Rippdialoogi avamiseks klõpsake valikut **Vaikimisi asukohast: tellitud kogus**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="54dcb-127">Valige suvand väljal **Ridade vaikekogus**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="54dcb-128">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-128">Click **OK**.</span></span>
6. <span data-ttu-id="54dcb-129">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-129">Click **Yes**.</span></span>
7. <span data-ttu-id="54dcb-130">Klõpsake valikut **Toote sissetulekute vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="54dcb-131">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-131">Click **OK**.</span></span>
9. <span data-ttu-id="54dcb-132">Klõpsake toimingupaanil valikut **Vaata üle**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="54dcb-133">Klõpsake valikut **Vastanduvad üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="54dcb-133">Click **Matching details**.</span></span>


