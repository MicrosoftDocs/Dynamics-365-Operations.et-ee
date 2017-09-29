---
title: "Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="3044e-102">Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod</span><span class="sxs-lookup"><span data-stu-id="3044e-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="3044e-103">Vaikevastaskontosid kasutatakse järgmistel hankija arve töölehe lehekülgedel:</span><span class="sxs-lookup"><span data-stu-id="3044e-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="3044e-104">Arve tööleht</span><span class="sxs-lookup"><span data-stu-id="3044e-104">Invoice journal</span></span>
-   <span data-ttu-id="3044e-105">Arve kinnitamise tööleht</span><span class="sxs-lookup"><span data-stu-id="3044e-105">Invoice approval journal</span></span>

<span data-ttu-id="3044e-106">Kasutage järgmist tabelit, mis aitab teil otsustada, kuhu peaksite arve töölehtede vaikekontod määrama.</span><span class="sxs-lookup"><span data-stu-id="3044e-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3044e-107">Seadistage vaikekontod siin</span><span class="sxs-lookup"><span data-stu-id="3044e-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="3044e-108">Kus vaikekontod saadaval on?</span><span class="sxs-lookup"><span data-stu-id="3044e-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="3044e-109">Kuidas see valik mõjutab töötlemist?</span><span class="sxs-lookup"><span data-stu-id="3044e-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="3044e-110">Millal peaksite seda valikut kasutama?</span><span class="sxs-lookup"><span data-stu-id="3044e-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3044e-111"><strong>Hankijagrupp</strong> – seadistage hankijagruppide vaikevastaskontod leheküljel <strong>Kontode vaikeseadistus</strong>, mille saate avada lehelt <strong>Hankijagrupid</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="3044e-112">Hankija konto</span><span class="sxs-lookup"><span data-stu-id="3044e-112">Vendor account</span></span></li>
<li><span data-ttu-id="3044e-113">Hankijagrupi hankija kontode töölehe kanded, kui hankijakontodele pole vaikekontosid määratud</span><span class="sxs-lookup"><span data-stu-id="3044e-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="3044e-114">Hankijagruppide vaikevastaskontod on näidatud hankijate vaikevastaskontodena lehel <strong>Kontode vaikeseadistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="3044e-115">Selle lehe saate avada loendilehelt <strong>Kõik hankijad</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="3044e-116">Valige see suvand, kui te tavaliselt aja jooksul maksate sama tüüpi asjad eest samadele hankijagruppidele.</span><span class="sxs-lookup"><span data-stu-id="3044e-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3044e-117"><strong>Hankija konto</strong> – seadistage hankija kontode vaikekontod leheküljel <strong>Kontode vaikeseadistus</strong>, mille saate avada lehelt <strong>Hankijad</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="3044e-118">Hankijakonto töölehekanded</span><span class="sxs-lookup"><span data-stu-id="3044e-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="3044e-119">Hankijakontode vaikevastaskontod on näidatud hankijakonto töölehekannete vaikevastaskontodena.</span><span class="sxs-lookup"><span data-stu-id="3044e-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="3044e-120">Valige see suvand, kui te tavaliselt aja jooksul maksate sama tüüpi asjad eest samadele hankijatele.</span><span class="sxs-lookup"><span data-stu-id="3044e-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3044e-121"><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="3044e-122">Valige suvand <strong>Fikseeritud vastaskonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="3044e-123">Pange tähele, et ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="3044e-124">Töölehe päis, mis kasutab töölehe nime</span><span class="sxs-lookup"><span data-stu-id="3044e-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="3044e-125">Töölehekanded töölehe nime kasutavatel töölehtedel</span><span class="sxs-lookup"><span data-stu-id="3044e-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="3044e-126">Kui lehel <strong>Töölehe nimed</strong> on valitud suvand <strong>Fikseeritud vastaskonto</strong>, tühistab töölehe nime vastaskonto hankija või hankijategrupi vaikevastaskonto.</span><span class="sxs-lookup"><span data-stu-id="3044e-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="3044e-127">Selle valiku abil saate seadistada spetsiifiliste väljaminekute ja kulude töölehed, mis arvestatakse konkreetsetele kontodele, olenemata hankijast või hankijagrupist, millesse hankija kuulub.</span><span class="sxs-lookup"><span data-stu-id="3044e-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3044e-128"><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="3044e-129">Tühjendage suvand <strong>Fikseeritud vastaskonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="3044e-130">Pange tähele, et ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="3044e-131">Töölehe päis</span><span class="sxs-lookup"><span data-stu-id="3044e-131">Journal header</span></span></li>
<li><span data-ttu-id="3044e-132">Töölehekanded töölehe nime kasutavatel töölehtedel</span><span class="sxs-lookup"><span data-stu-id="3044e-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="3044e-133">Neid vaikekirjeid kasutatakse töölehe päise lehtedel ja töölehe päise lehel olevat vastaskontot vaikekirjena töölehe kande lehtedel.</span><span class="sxs-lookup"><span data-stu-id="3044e-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="3044e-134">Vaikekontosid lehel <strong>Töölehe nimed </strong>kasutatakse ainult siis, kui hankijakontole pole vaikekontosid seadistatud.</span><span class="sxs-lookup"><span data-stu-id="3044e-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="3044e-135">Selle valiku abil saate seadistada vaikekontod, mida kasutatakse, kui hankija vaikevastaskontot pole määratud.</span><span class="sxs-lookup"><span data-stu-id="3044e-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3044e-136"><strong>Töölehe päis</strong> – seadistage töölehe vaikevastaskonto töölehe kande lehtedel vaikekirjena.</span><span class="sxs-lookup"><span data-stu-id="3044e-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="3044e-137">Pange tähele, et ei saa määrata vaikevastaskontosid töölehe päisele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="3044e-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="3044e-138">Töölehe kanded töölehel</span><span class="sxs-lookup"><span data-stu-id="3044e-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="3044e-139">Töölehe vaikevastaskontot kasutatakse töölehe kande lehtedel vaikekirjena.</span><span class="sxs-lookup"><span data-stu-id="3044e-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="3044e-140">Selle valiku abil saate kiirendada andmesisestust, kui enamikul töölehe kirjetest on sama vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="3044e-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






