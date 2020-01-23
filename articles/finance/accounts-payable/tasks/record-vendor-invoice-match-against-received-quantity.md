---
title: Hankija arve kirjendamine ja sissetulnud kogusega vastendamine
description: Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66d84f497775ce4f988242dd2b327bf4854faef5
ms.sourcegitcommit: ba1c76497acc9afba85257976f0d4e96836871d1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2019
ms.locfileid: "2890415"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="741db-103">Hankija arve kirjendamine ja sissetulnud kogusega vastendamine</span><span class="sxs-lookup"><span data-stu-id="741db-103">Record vendor invoice and match against received quantity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="741db-104">Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud.</span><span class="sxs-lookup"><span data-stu-id="741db-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="741db-105">Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine.</span><span class="sxs-lookup"><span data-stu-id="741db-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="741db-106">Veenduge lehel Ostureskontro parameetrid, et valitud on suvand Lubage arvete võrdlemise kontrollimine, suvand Nõua kinnitust väljal Lahknevustega arvete sisestamine ning suvand Kolmesuunaline vastavusse viimine väljal Rea vastavusse viimise poliitika.</span><span class="sxs-lookup"><span data-stu-id="741db-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="741db-107">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="741db-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="741db-108">Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli.</span><span class="sxs-lookup"><span data-stu-id="741db-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="741db-109">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="741db-109">Create a purchase order</span></span>
1. <span data-ttu-id="741db-110">Avage valik Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="741db-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="741db-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="741db-111">Click New.</span></span>
3. <span data-ttu-id="741db-112">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="741db-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="741db-113">Sisestage väärtus väljale Hankija konto.</span><span class="sxs-lookup"><span data-stu-id="741db-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="741db-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="741db-114">Click OK.</span></span>
6. <span data-ttu-id="741db-115">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="741db-115">Click Add line.</span></span>
7. <span data-ttu-id="741db-116">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="741db-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="741db-117">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="741db-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="741db-118">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="741db-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="741db-119">Toote sissetuleku sisestamine</span><span class="sxs-lookup"><span data-stu-id="741db-119">Post a product receipt</span></span>
1. <span data-ttu-id="741db-120">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="741db-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="741db-121">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="741db-121">Click Product receipt.</span></span>
3. <span data-ttu-id="741db-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="741db-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="741db-123">Sisestage väärtus väljale Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="741db-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="741db-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="741db-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="741db-125">Hankija arve salvestamine ja vastendamine toote sissetulekuga</span><span class="sxs-lookup"><span data-stu-id="741db-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="741db-126">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="741db-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="741db-127">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="741db-127">Click Invoice.</span></span>
3. <span data-ttu-id="741db-128">Sisestage väärtus väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="741db-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="741db-129">Rippdialoogi avamiseks klõpsake valikut Vaikimis asukohast: tellitud kogus.</span><span class="sxs-lookup"><span data-stu-id="741db-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="741db-130">Valige suvand väljal Ridade vaikekogus.</span><span class="sxs-lookup"><span data-stu-id="741db-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="741db-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="741db-131">Click OK.</span></span>
7. <span data-ttu-id="741db-132">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="741db-132">Click Yes.</span></span>
8. <span data-ttu-id="741db-133">Klõpsake valikut Toote sissetulekute vastendamine.</span><span class="sxs-lookup"><span data-stu-id="741db-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="741db-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="741db-134">Click OK.</span></span>
10. <span data-ttu-id="741db-135">Klõpsake toimingupaanil valikut Vaata üle.</span><span class="sxs-lookup"><span data-stu-id="741db-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="741db-136">Klõpsake valikut Vastanduvad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="741db-136">Click Matching details.</span></span>
