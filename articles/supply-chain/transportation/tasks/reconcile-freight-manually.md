---
title: Veose käsitsi vastavusseviimine
description: See protseduur näitab, kuidas veost käsitsi tasakaalustada.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc4fc51955544df4d0156a4c83bcc5b5a0e13df3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426632"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="8c980-103">Veose käsitsi vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="8c980-103">Reconcile freight manually</span></span>

<span data-ttu-id="8c980-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="8c980-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="8c980-105">See protseduur näitab, kuidas veost käsitsi tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="8c980-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="8c980-106">Seda teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="8c980-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="8c980-107">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="8c980-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="8c980-108">Valige vastavusseviimiseks koorem</span><span class="sxs-lookup"><span data-stu-id="8c980-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="8c980-109">Avage Transpordihaldus > Plaanimine > Koorma plaanimise töölaud.</span><span class="sxs-lookup"><span data-stu-id="8c980-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="8c980-110">Tühjendage märkeruut Peida saadetud ja vastuvõetud.</span><span class="sxs-lookup"><span data-stu-id="8c980-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="8c980-111">Valige loendist koorem, mille koorma ID on 00006.</span><span class="sxs-lookup"><span data-stu-id="8c980-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="8c980-112">Vedaja arve loomine</span><span class="sxs-lookup"><span data-stu-id="8c980-112">Create a carrier invoice</span></span>
<span data-ttu-id="8c980-113">Kui viite veose käsitsi vastavusse ega saa automaatselt vedaja arveid, võite luua arve veoarve põhjal.</span><span class="sxs-lookup"><span data-stu-id="8c980-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="8c980-114">Klõpsake valikut Seostuv teave.</span><span class="sxs-lookup"><span data-stu-id="8c980-114">Click Related information.</span></span>
2. <span data-ttu-id="8c980-115">Klõpsake valikut Veoarve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="8c980-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="8c980-116">Klõpsake valikut Veoarve loomine.</span><span class="sxs-lookup"><span data-stu-id="8c980-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="8c980-117">Sisestage väärtus väljale Arve.</span><span class="sxs-lookup"><span data-stu-id="8c980-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="8c980-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8c980-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="8c980-119">Arve vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="8c980-119">Reconcile the invoice</span></span>
<span data-ttu-id="8c980-120">Vedaja arve ja veoarve tasakaalustamisel tehakse seda reakaupa.</span><span class="sxs-lookup"><span data-stu-id="8c980-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="8c980-121">Klõpsake valikut Vastenda veoarved ja arved.</span><span class="sxs-lookup"><span data-stu-id="8c980-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="8c980-122">Laiendage jaotist Arve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="8c980-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="8c980-123">Laiendage jaotist Vastendamata veoarve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="8c980-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="8c980-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="8c980-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8c980-125">Klõpsake nuppu Vastenda.</span><span class="sxs-lookup"><span data-stu-id="8c980-125">Click Match.</span></span>
6. <span data-ttu-id="8c980-126">Laiendage jaotist Vastendatud veoarve üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="8c980-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="8c980-127">Esita arve kinnitamiseks</span><span class="sxs-lookup"><span data-stu-id="8c980-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="8c980-128">Klõpsake valikut Edasta kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="8c980-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="8c980-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8c980-129">Close the page.</span></span>
3. <span data-ttu-id="8c980-130">Tühjendage märkeruut Peida kinnitatud üksused.</span><span class="sxs-lookup"><span data-stu-id="8c980-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="8c980-131">Klõpsake nuppu Hankijaarvete töölehed.</span><span class="sxs-lookup"><span data-stu-id="8c980-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="8c980-132">Klõpsake linki väljal Viitetöölehe number.</span><span class="sxs-lookup"><span data-stu-id="8c980-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="8c980-133">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="8c980-133">Click Lines.</span></span>

