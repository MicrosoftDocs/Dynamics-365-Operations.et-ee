---
title: Veose käsitsi vastavusseviimine
description: See protseduur näitab, kuidas veost käsitsi tasakaalustada.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee2d114b0a725b947add3e155cc6445021fee998
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "351880"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="49728-103">Veose käsitsi vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="49728-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49728-104">See protseduur näitab, kuidas veost käsitsi tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="49728-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="49728-105">Seda teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="49728-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="49728-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="49728-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="49728-107">Valige vastavusseviimiseks koorem</span><span class="sxs-lookup"><span data-stu-id="49728-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="49728-108">Avage Transpordihaldus > Plaanimine > Koorma plaanimise töölaud.</span><span class="sxs-lookup"><span data-stu-id="49728-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="49728-109">Tühjendage märkeruut Peida saadetud ja vastuvõetud.</span><span class="sxs-lookup"><span data-stu-id="49728-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="49728-110">Valige loendist koorem, mille koorma ID on 00006.</span><span class="sxs-lookup"><span data-stu-id="49728-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="49728-111">Vedaja arve loomine</span><span class="sxs-lookup"><span data-stu-id="49728-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="49728-112">Kui viite veose käsitsi vastavusse ega saa automaatselt vedaja arveid, võite luua arve veoarve põhjal.</span><span class="sxs-lookup"><span data-stu-id="49728-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="49728-113">Klõpsake valikut Seostuv teave.</span><span class="sxs-lookup"><span data-stu-id="49728-113">Click Related information.</span></span>
2. <span data-ttu-id="49728-114">Klõpsake valikut Veoarve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="49728-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="49728-115">Klõpsake valikut Veoarve loomine.</span><span class="sxs-lookup"><span data-stu-id="49728-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="49728-116">Sisestage väärtus väljale Arve.</span><span class="sxs-lookup"><span data-stu-id="49728-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="49728-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="49728-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="49728-118">Arve vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="49728-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="49728-119">Vedaja arve ja veoarve tasakaalustamisel tehakse seda reakaupa.</span><span class="sxs-lookup"><span data-stu-id="49728-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="49728-120">Klõpsake valikut Vastenda veoarved ja arved.</span><span class="sxs-lookup"><span data-stu-id="49728-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="49728-121">Laiendage jaotist Arve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="49728-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="49728-122">Laiendage jaotist Vastendamata veoarve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="49728-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="49728-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="49728-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="49728-124">Klõpsake nuppu Vastenda.</span><span class="sxs-lookup"><span data-stu-id="49728-124">Click Match.</span></span>
6. <span data-ttu-id="49728-125">Laiendage jaotist Vastendatud veoarve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="49728-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="49728-126">Esita arve kinnitamiseks</span><span class="sxs-lookup"><span data-stu-id="49728-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="49728-127">Klõpsake valikut Edasta kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="49728-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="49728-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="49728-128">Close the page.</span></span>
3. <span data-ttu-id="49728-129">Tühjendage märkeruut Peida kinnitatud üksused.</span><span class="sxs-lookup"><span data-stu-id="49728-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="49728-130">Klõpsake nuppu Hankijaarvete töölehed.</span><span class="sxs-lookup"><span data-stu-id="49728-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="49728-131">Klõpsake linki väljal Viitetöölehe number.</span><span class="sxs-lookup"><span data-stu-id="49728-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="49728-132">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="49728-132">Click Lines.</span></span>

