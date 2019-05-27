---
title: Hankija koostöö arve tööruum
description: See teema selgitab, kuidas saate vaadata hankijaarveid ja edastada arveid hankija koostöö arveldamise tööruumist.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1f9e57e95a03b3e6f8bd940d38a426e9db559624
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1508501"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="5e8e2-103">Hankija koostöö arve tööruum</span><span class="sxs-lookup"><span data-stu-id="5e8e2-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e8e2-104">See teema selgitab, kuidas saate vaadata hankijaarveid ja edastada arveid hankija koostöö arveldamise tööruumist.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="5e8e2-105">Tööruumi **Hankija koostöö arve** abil saab vaadata hankija arve teavet ja esitada arveid rakendusse Microsoft Dynamics 365 for Finance and Operations, kasutades töövoo võimalusi.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="5e8e2-106">Hankija koostöö arve tööruum</span><span class="sxs-lookup"><span data-stu-id="5e8e2-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="5e8e2-107">Kokkuvõttepaanid</span><span class="sxs-lookup"><span data-stu-id="5e8e2-107">Summary tiles</span></span>

<span data-ttu-id="5e8e2-108">Paanid **Kokkuvõte** annavad valitud hankija arvetest ülevaate.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="5e8e2-109">Saate vaadata arveid nende oleku järgi.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="5e8e2-110">Arvemustandeid ei ole edastatud töövoosse.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="5e8e2-111">Esitatud, kuid kinnitamata arved on need arved, mille hankija on edastanud, kuid need pole sisestatud rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="5e8e2-112">Esitatud, kuid makstud arved on need arved, mis on sisestatud rakendusse Finance and Operations, kuid need pole veel täielikult tasutud.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="5e8e2-113">Tasutud arved on need, mis on rakenduses Finance and Operations täielikult tasutud.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="5e8e2-114">Paani klõpsamine avab lehest **Arvete loend** filtreeritud vaate.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="5e8e2-115">Tabelloendid</span><span class="sxs-lookup"><span data-stu-id="5e8e2-115">Tabular lists</span></span>

<span data-ttu-id="5e8e2-116">Jaotises **Tabelloendid** on arveldamise olek jaotatud sarnaselt kokkuvõttepaanidele. Mustand ja Edastatud, kinnitamata loendid.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="5e8e2-117">Mustandi olekus saab arve edastada töövoosse või kustutada.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="5e8e2-118">Viimane tabelloend on võimalus arvete leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="5e8e2-119">Saate otsides filtreerida, et võimaldada kiiremaid otsinguid.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="5e8e2-120">Kõikide hankijaarvete loendileht</span><span class="sxs-lookup"><span data-stu-id="5e8e2-120">All vendor invoices list page</span></span>

<span data-ttu-id="5e8e2-121">Saate vaadata kõiki sisestatud ja sisestamata hankijaarveid loendilehel **Hankija koostöö arved**.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="5e8e2-122">Arvete makseoleku vaatamiseks saate kasutada seda loendilehte.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="5e8e2-123">Makseolekud hõlmavad olekuid Sisestamata, Tasumata, Osaliselt makstud ja Täielikult tasutud.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="5e8e2-124">Uue arve loomine ostutellimusest</span><span class="sxs-lookup"><span data-stu-id="5e8e2-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="5e8e2-125">Saate luua uue hankijaarve, valides tegevuse **Uus** tööruumis **Hankija koostöö arve tööruum**.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="5e8e2-126">Ostutellimuse numbri ja arve numbri peab andma hankija.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="5e8e2-127">Vaikimisi kuvatakse kõik read hankija ostutellimuselt uuel arvel.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="5e8e2-128">Kogust ja kuluteavet saab redigeerida enne hankijaarve töövoole edastamist.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="5e8e2-129">Saate manustada arvele enne selle edastamist faile, märkuseid, pilte ja URL-sid.</span><span class="sxs-lookup"><span data-stu-id="5e8e2-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="5e8e2-130">Lisateabe saamiseks vaadake teemat [Hankija koostöö väliste hankijatega](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="5e8e2-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>



