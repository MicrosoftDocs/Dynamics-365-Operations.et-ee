---
title: "Põhivarakannete valikud"
description: "Selles artiklis kirjeldatakse põhivara kannete loomiseks saadaolevaid erinevaid viise."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2a7fa7a28437e29f390efdf566e946c6a1082370
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="49ca1-103">Põhivarakannete valikud</span><span class="sxs-lookup"><span data-stu-id="49ca1-103">Fixed asset transaction options</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="49ca1-104">Selles artiklis kirjeldatakse põhivara kannete loomiseks saadaolevaid erinevaid viise.</span><span class="sxs-lookup"><span data-stu-id="49ca1-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="49ca1-105">Põhivarad on võimalik integreerida ostureskontroga, müügireskontroga, hanke ja pearaamatuga.</span><span class="sxs-lookup"><span data-stu-id="49ca1-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="49ca1-106">Samuti saate kaupu laohalduses põhivaradesse üle viia, kui soovite neid kaupu ettevõttesiseselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="49ca1-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="49ca1-107">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="49ca1-107">Accounts payable</span></span>
<span data-ttu-id="49ca1-108">Saate sisestada põhivarakanded lehele Töölehe kanne.</span><span class="sxs-lookup"><span data-stu-id="49ca1-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="49ca1-109">Selle lehe saab avada lehelt Arve tööleht.</span><span class="sxs-lookup"><span data-stu-id="49ca1-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="49ca1-110">Saate avada lehe Töölehe kanne ka lehelt Arve kinnitamise tööleht.</span><span class="sxs-lookup"><span data-stu-id="49ca1-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="49ca1-111">Tehke väljal Vastaskonto tüüp valik Põhivara.</span><span class="sxs-lookup"><span data-stu-id="49ca1-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="49ca1-112">Seejärel valige väljalt Vastaskonto põhivara number.</span><span class="sxs-lookup"><span data-stu-id="49ca1-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="49ca1-113">Sisestage vahekaardil Põhivarad väärtused väljadele Kande tüüp ja Raamat.</span><span class="sxs-lookup"><span data-stu-id="49ca1-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="49ca1-114">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="49ca1-114">Accounts receivable</span></span>
<span data-ttu-id="49ca1-115">Saate sisestada põhivarakanded lehele Vabas vormis arve.</span><span class="sxs-lookup"><span data-stu-id="49ca1-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="49ca1-116">Valige vabas vormis arve lehe ruudustikus Arve read reaüksus.</span><span class="sxs-lookup"><span data-stu-id="49ca1-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="49ca1-117">Klõpsake kiirkaarti Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="49ca1-117">Click the Line details FastTab.</span></span> <span data-ttu-id="49ca1-118">Sisestage likvideerimiskandele põhivara number ja raamat.</span><span class="sxs-lookup"><span data-stu-id="49ca1-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="49ca1-119">Vabas vormis arvete puhul on põhivarakande tüübiks alati Likvideerimine – müük.</span><span class="sxs-lookup"><span data-stu-id="49ca1-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="49ca1-120">Hanked</span><span class="sxs-lookup"><span data-stu-id="49ca1-120">Procurement and sourcing</span></span>
<span data-ttu-id="49ca1-121">Saate sisestada põhivarakanded lehele Ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="49ca1-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="49ca1-122">Sisestage ostutellimuse loomiseks vajalik teave ja klõpsake seejärel nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="49ca1-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="49ca1-123">Klõpsake lehel Ostutellimus kiirkaarti Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="49ca1-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="49ca1-124">Seejärel sisestage vahekaardile Põhivara teave põhivara kohta.</span><span class="sxs-lookup"><span data-stu-id="49ca1-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="49ca1-125">Olemasolevale põhivarale soetuskande sisestamiseks määrake põhivara number, raamat ja kande tüüp.</span><span class="sxs-lookup"><span data-stu-id="49ca1-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="49ca1-126">Põhivara ei saa sisestada, kui osa sellest teabest on puudu.</span><span class="sxs-lookup"><span data-stu-id="49ca1-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="49ca1-127">Uuele põhivarale soetuskande sisestamiseks tehke valik Uus põhivara? ja valige siis põhivaragrupp uuele põhivarale määramiseks.</span><span class="sxs-lookup"><span data-stu-id="49ca1-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="49ca1-128">Ükski põhivara väli ei ole rea jaoks saadaval, kui kaup on laomudeligrupis, mis kasutab standardkulu laomudelit.</span><span class="sxs-lookup"><span data-stu-id="49ca1-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="49ca1-129">Suvandid, mis on määratud lehel Põhivara parameetrid, määravad selle, kas saate ostumoodulitest soetuskandeid sisestada.</span><span class="sxs-lookup"><span data-stu-id="49ca1-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="49ca1-130">Kui põhivara soetamiseks kasutatakse ostutellimust või töölehte Põhivara varud, mõjutab see laoväärtust.</span><span class="sxs-lookup"><span data-stu-id="49ca1-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="49ca1-131">Pearaamat</span><span class="sxs-lookup"><span data-stu-id="49ca1-131">General ledger</span></span>
<span data-ttu-id="49ca1-132">Kõiki põhivara kandetüüpe saab sisestada lehele Päevaraamat.</span><span class="sxs-lookup"><span data-stu-id="49ca1-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="49ca1-133">Samuti saate põhivarade puhul töölehti kasutada põhivarakannete sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="49ca1-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="49ca1-134">Põhivara kandetüüpide sisestamise suvandid</span><span class="sxs-lookup"><span data-stu-id="49ca1-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="49ca1-135">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="49ca1-135">Transaction type</span></span>                    | <span data-ttu-id="49ca1-136">Moodul</span><span class="sxs-lookup"><span data-stu-id="49ca1-136">Module</span></span>                   | <span data-ttu-id="49ca1-137">Suvandid</span><span class="sxs-lookup"><span data-stu-id="49ca1-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="49ca1-138">Soetamine, Soetamise korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="49ca1-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="49ca1-139">Põhivarad</span><span class="sxs-lookup"><span data-stu-id="49ca1-139">Fixed assets</span></span>             | <span data-ttu-id="49ca1-140">Põhivara, Põhivara varud</span><span class="sxs-lookup"><span data-stu-id="49ca1-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="49ca1-141">Pearaamat</span><span class="sxs-lookup"><span data-stu-id="49ca1-141">General ledger</span></span>           | <span data-ttu-id="49ca1-142">Päevaraamat</span><span class="sxs-lookup"><span data-stu-id="49ca1-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="49ca1-143">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="49ca1-143">Accounts payable</span></span>         | <span data-ttu-id="49ca1-144">Arve tööleht, Arve kinnitamise tööleht</span><span class="sxs-lookup"><span data-stu-id="49ca1-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="49ca1-145">Hanked</span><span class="sxs-lookup"><span data-stu-id="49ca1-145">Procurement and sourcing</span></span> | <span data-ttu-id="49ca1-146">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="49ca1-146">Purchase order</span></span>                            |
| <span data-ttu-id="49ca1-147">Kulum</span><span class="sxs-lookup"><span data-stu-id="49ca1-147">Depreciation</span></span>                        | <span data-ttu-id="49ca1-148">Põhivarad</span><span class="sxs-lookup"><span data-stu-id="49ca1-148">Fixed assets</span></span>             | <span data-ttu-id="49ca1-149">Põhivarad</span><span class="sxs-lookup"><span data-stu-id="49ca1-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="49ca1-150">Pearaamat</span><span class="sxs-lookup"><span data-stu-id="49ca1-150">General ledger</span></span>           | <span data-ttu-id="49ca1-151">Päevaraamat</span><span class="sxs-lookup"><span data-stu-id="49ca1-151">General journal</span></span>                           |
| <span data-ttu-id="49ca1-152">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="49ca1-152">Disposal</span></span>                            | <span data-ttu-id="49ca1-153">Põhivarad</span><span class="sxs-lookup"><span data-stu-id="49ca1-153">Fixed assets</span></span>             | <span data-ttu-id="49ca1-154">Põhivarad</span><span class="sxs-lookup"><span data-stu-id="49ca1-154">Fixed assets</span></span>                              |
| <span data-ttu-id="49ca1-155">** **</span><span class="sxs-lookup"><span data-stu-id="49ca1-155">** **</span></span>                               | <span data-ttu-id="49ca1-156">Pearaamat</span><span class="sxs-lookup"><span data-stu-id="49ca1-156">General ledger</span></span>           | <span data-ttu-id="49ca1-157">Päevaraamat</span><span class="sxs-lookup"><span data-stu-id="49ca1-157">General journal</span></span>                           |
| <span data-ttu-id="49ca1-158">** **</span><span class="sxs-lookup"><span data-stu-id="49ca1-158">** **</span></span>                               | <span data-ttu-id="49ca1-159">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="49ca1-159">Accounts receivable</span></span>      | <span data-ttu-id="49ca1-160">Vabas vormis arve</span><span class="sxs-lookup"><span data-stu-id="49ca1-160">Free text invoice</span></span>                         |



<span data-ttu-id="49ca1-161">Lisateavet leiate jaotisest [Põhivarade integreerimine](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="49ca1-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




