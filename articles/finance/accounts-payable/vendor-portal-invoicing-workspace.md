---
title: Hankija koostöö arve tööruum
description: See teema selgitab, kuidas saate vaadata hankijaarveid ja edastada arveid hankija koostöö arveldamise tööruumist.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 73f16b00f2af884387e0b135f3b220179eecad86
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822439"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="a22f8-103">Hankija koostöö arve tööruum</span><span class="sxs-lookup"><span data-stu-id="a22f8-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a22f8-104">See teema selgitab, kuidas saate vaadata hankijaarveid ja edastada arveid hankija koostöö arveldamise tööruumist.</span><span class="sxs-lookup"><span data-stu-id="a22f8-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="a22f8-105">Tööruumi **Hankija koostöö arve abil** saab vaadata hankija arve teavet ja esitada arveid süsteemi, kasutades töövoo võimalusi.</span><span class="sxs-lookup"><span data-stu-id="a22f8-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="a22f8-106">Hankija koostöö arve tööruum</span><span class="sxs-lookup"><span data-stu-id="a22f8-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="a22f8-107">Kokkuvõttepaanid</span><span class="sxs-lookup"><span data-stu-id="a22f8-107">Summary tiles</span></span>

<span data-ttu-id="a22f8-108">Paanid **Kokkuvõte** annavad valitud hankija arvetest ülevaate.</span><span class="sxs-lookup"><span data-stu-id="a22f8-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="a22f8-109">Saate vaadata arveid nende oleku järgi.</span><span class="sxs-lookup"><span data-stu-id="a22f8-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="a22f8-110">Arvemustandeid ei ole edastatud töövoosse.</span><span class="sxs-lookup"><span data-stu-id="a22f8-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="a22f8-111">Esitatud, kuid kinnitamata arved on need arved, mille hankija on edastanud, kuid need pole rakendusse sisestatud.</span><span class="sxs-lookup"><span data-stu-id="a22f8-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="a22f8-112">Esitatud, kuid makstud arved on need arved, mis on rakendusse sisestatud, kuid need pole veel täielikult tasutud.</span><span class="sxs-lookup"><span data-stu-id="a22f8-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="a22f8-113">Tasutud arved on need, mis on rakenduses täielikult tasutud.</span><span class="sxs-lookup"><span data-stu-id="a22f8-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="a22f8-114">Paani klõpsamine avab lehest **Arvete loend** filtreeritud vaate.</span><span class="sxs-lookup"><span data-stu-id="a22f8-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="a22f8-115">Tabelloendid</span><span class="sxs-lookup"><span data-stu-id="a22f8-115">Tabular lists</span></span>

<span data-ttu-id="a22f8-116">Jaotises **Tabelloendid** on arveldamise olek jaotatud sarnaselt kokkuvõttepaanidele. Mustand ja Edastatud, kinnitamata loendid.</span><span class="sxs-lookup"><span data-stu-id="a22f8-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="a22f8-117">Mustandi olekus saab arve edastada töövoosse või kustutada.</span><span class="sxs-lookup"><span data-stu-id="a22f8-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="a22f8-118">Viimane tabelloend on võimalus arvete leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="a22f8-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="a22f8-119">Saate otsides filtreerida, et võimaldada kiiremaid otsinguid.</span><span class="sxs-lookup"><span data-stu-id="a22f8-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="a22f8-120">Kõikide hankijaarvete loendileht</span><span class="sxs-lookup"><span data-stu-id="a22f8-120">All vendor invoices list page</span></span>

<span data-ttu-id="a22f8-121">Saate vaadata kõiki sisestatud ja sisestamata hankijaarveid loendilehel **Hankija koostöö arved**.</span><span class="sxs-lookup"><span data-stu-id="a22f8-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="a22f8-122">Arvete makseoleku vaatamiseks saate kasutada seda loendilehte.</span><span class="sxs-lookup"><span data-stu-id="a22f8-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="a22f8-123">Makseolekud hõlmavad olekuid Sisestamata, Tasumata, Osaliselt makstud ja Täielikult tasutud.</span><span class="sxs-lookup"><span data-stu-id="a22f8-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="a22f8-124">Uue arve loomine ostutellimusest</span><span class="sxs-lookup"><span data-stu-id="a22f8-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="a22f8-125">Saate luua uue hankijaarve, valides tegevuse **Uus** tööruumis **Hankija koostöö arve tööruum**.</span><span class="sxs-lookup"><span data-stu-id="a22f8-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="a22f8-126">Ostutellimuse numbri ja arve numbri peab andma hankija.</span><span class="sxs-lookup"><span data-stu-id="a22f8-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="a22f8-127">Vaikimisi kuvatakse kõik read hankija ostutellimuselt uuel arvel.</span><span class="sxs-lookup"><span data-stu-id="a22f8-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="a22f8-128">Kogust ja kuluteavet saab redigeerida enne hankijaarve töövoole edastamist.</span><span class="sxs-lookup"><span data-stu-id="a22f8-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="a22f8-129">Saate manustada arvele enne selle edastamist faile, märkuseid, pilte ja URL-sid.</span><span class="sxs-lookup"><span data-stu-id="a22f8-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="a22f8-130">Lisateabe saamiseks vaadake teemat [Hankija koostöö väliste hankijatega](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="a22f8-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]