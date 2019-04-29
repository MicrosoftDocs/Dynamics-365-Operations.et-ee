---
title: Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod
description: See teema aitab teil otsustada, kuhu peaksite arve töölehtede vaikekontod määrama.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cf772a0f0f9f99519322be1f37f961dc0ab2500
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/25/2019
ms.locfileid: "896760"
---
# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="0b4e8-103">Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod</span><span class="sxs-lookup"><span data-stu-id="0b4e8-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b4e8-104">Vaikevastaskontosid kasutatakse järgmistel hankija arve töölehe lehekülgedel:</span><span class="sxs-lookup"><span data-stu-id="0b4e8-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="0b4e8-105">Arve tööleht</span><span class="sxs-lookup"><span data-stu-id="0b4e8-105">Invoice journal</span></span>
-   <span data-ttu-id="0b4e8-106">Arve kinnitamise tööleht</span><span class="sxs-lookup"><span data-stu-id="0b4e8-106">Invoice approval journal</span></span>

<span data-ttu-id="0b4e8-107">Kasutage järgmist tabelit, mis aitab teil otsustada, kuhu peaksite arve töölehtede vaikekontod määrama.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b4e8-108">Seadistage vaikekontod siin</span><span class="sxs-lookup"><span data-stu-id="0b4e8-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="0b4e8-109">Kus vaikekontod saadaval on?</span><span class="sxs-lookup"><span data-stu-id="0b4e8-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="0b4e8-110">Kuidas see valik mõjutab töötlemist?</span><span class="sxs-lookup"><span data-stu-id="0b4e8-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="0b4e8-111">Millal peaksite seda valikut kasutama?</span><span class="sxs-lookup"><span data-stu-id="0b4e8-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b4e8-112"><strong>Hankijagrupp</strong> – seadistage hankijagruppide vaikevastaskontod leheküljel <strong>Kontode vaikeseadistus</strong>, mille saate avada lehelt <strong>Hankijagrupid</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="0b4e8-113">Hankija konto</span><span class="sxs-lookup"><span data-stu-id="0b4e8-113">Vendor account</span></span></li>
<li><span data-ttu-id="0b4e8-114">Hankijagrupi hankija kontode töölehe kanded, kui hankijakontodele pole vaikekontosid määratud</span><span class="sxs-lookup"><span data-stu-id="0b4e8-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="0b4e8-115">Hankijagruppide vaikevastaskontod on näidatud hankijate vaikevastaskontodena lehel <strong>Kontode vaikeseadistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="0b4e8-116">Selle lehe saate avada loendilehelt <strong>Kõik hankijad</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="0b4e8-117">Valige see suvand, kui te tavaliselt aja jooksul maksate sama tüüpi asjad eest samadele hankijagruppidele.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b4e8-118"><strong>Hankija konto</strong> – seadistage hankija kontode vaikekontod leheküljel <strong>Kontode vaikeseadistus</strong>, mille saate avada lehelt <strong>Hankijad</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="0b4e8-119">Hankijakonto töölehekanded</span><span class="sxs-lookup"><span data-stu-id="0b4e8-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="0b4e8-120">Hankijakontode vaikevastaskontod on näidatud hankijakonto töölehekannete vaikevastaskontodena.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="0b4e8-121">Valige see suvand, kui te tavaliselt aja jooksul maksate sama tüüpi asjad eest samadele hankijatele.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b4e8-122"><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="0b4e8-123">Valige suvand <strong>Fikseeritud vastaskonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="0b4e8-124">Pange tähele, et te ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="0b4e8-125">Töölehe päis, mis kasutab töölehe nime</span><span class="sxs-lookup"><span data-stu-id="0b4e8-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="0b4e8-126">Töölehekanded töölehe nime kasutavatel töölehtedel</span><span class="sxs-lookup"><span data-stu-id="0b4e8-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="0b4e8-127">Kui lehel <strong>Töölehe nimed</strong> on valitud suvand <strong>Fikseeritud vastaskonto</strong>, tühistab töölehe nime vastaskonto hankija või hankijategrupi vaikevastaskonto.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="0b4e8-128">Selle valiku abil saate seadistada spetsiifiliste väljaminekute ja kulude töölehed, mis arvestatakse konkreetsetele kontodele, olenemata hankijast või hankijagrupist, millesse hankija kuulub.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b4e8-129"><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="0b4e8-130">Tühjendage suvand <strong>Fikseeritud vastaskonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="0b4e8-131">Pange tähele, et te ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="0b4e8-132">Töölehe päis</span><span class="sxs-lookup"><span data-stu-id="0b4e8-132">Journal header</span></span></li>
<li><span data-ttu-id="0b4e8-133">Töölehekanded töölehe nime kasutavatel töölehtedel</span><span class="sxs-lookup"><span data-stu-id="0b4e8-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="0b4e8-134">Neid vaikekirjeid kasutatakse töölehe päise lehtedel ja töölehe päise lehel olevat vastaskontot vaikekirjena töölehe kande lehtedel.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="0b4e8-135">Vaikekontosid lehel <strong>Töölehe nimed </strong>kasutatakse ainult siis, kui hankijakontole pole vaikekontosid seadistatud.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="0b4e8-136">Selle valiku abil saate seadistada vaikekontod, mida kasutatakse, kui hankija vaikevastaskontot pole määratud.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b4e8-137"><strong>Töölehe päis</strong> – seadistage töölehe vaikevastaskonto töölehe kande lehtedel vaikekirjena.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="0b4e8-138">Pange tähele, et te ei saa määrata vaikevastaskontosid töölehe päisele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="0b4e8-139">Töölehe kanded töölehel</span><span class="sxs-lookup"><span data-stu-id="0b4e8-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="0b4e8-140">Töölehe vaikevastaskontot kasutatakse töölehe kande lehtedel vaikekirjena.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="0b4e8-141">Selle valiku abil saate kiirendada andmesisestust, kui enamikul töölehe kirjetest on sama vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>





