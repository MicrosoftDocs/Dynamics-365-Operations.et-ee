---
title: "Põhivarade likvideerimine Eesti ja Leedu puhul"
description: "See teema pakub teavet Eestis ja Leedus asuvate juriidiliste isikute kasutajate puhul vabas vormis arvete sisestatud põhivarade likvideerimise kreeditarvete kohta."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeCreditNote_W, CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266944
ms.search.region: Estonia, Lithuania
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b7688f6121cc6e518281aa56f310d1cfb08edfc0
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="fixed-assets-disposal-for-estonia-and-lithuania"></a><span data-ttu-id="e4c2f-103">Põhivarade likvideerimine Eesti ja Leedu puhul</span><span class="sxs-lookup"><span data-stu-id="e4c2f-103">Fixed assets disposal for Estonia and Lithuania</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e4c2f-104">See teema pakub teavet Eestis ja Leedus asuvate juriidiliste isikute kasutajate puhul vabas vormis arvete sisestatud põhivarade likvideerimise kreeditarvete kohta.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-104">This topic provides information about credit notes for fixed assets disposal posted by a free text invoice for users in legal entities in Estonia and Lithuania.</span></span>

<span data-ttu-id="e4c2f-105">Põhivarasid saab müüa likvideerimisfunktsiooni abil vabas vormis arve, põhivara töölehe või päevaraamatu kaudu pearaamatus.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-105">Fixed assets can be sold using disposal functionality through a free text invoice, fixed asset journal, or general journal in General ledger.</span></span> <span data-ttu-id="e4c2f-106">Lisateavet vt teemast [Põhivara likvideerimise sisestuskontod](../fixed-assets/fixed-asset-disposal-posting-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="e4c2f-106">For more information, see [Fixed asset disposal posting accounts](../fixed-assets/fixed-asset-disposal-posting-accounts.md).</span></span> <span data-ttu-id="e4c2f-107">Põhivarade likvideerimise kreeditarve funktsioon võimaldab Eestis ja Leedus asuvate juriidiliste isikute kasutajatel luua koos põhivara müügiga kreeditarve vabas vormis arve jaoks ja selle siis sisestada.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-107">Fixed assets disposal credit note functionality allows users in legal entities in Estonia and Latvia to create a credit note for a free text invoice with sales of a fixed asset and then post it.</span></span> <span data-ttu-id="e4c2f-108">Kreeditarve loomiseks. et tühistada vabas vormis arve, mis loodi põhivara müügi alusel, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-108">To create a credit note to reverse a free text invoice that was generated for the sale of a fixed asset, complete the following steps:</span></span>

1.  <span data-ttu-id="e4c2f-109">Klõpsake valikuid **Müügireskontro** &gt; **Arved** &gt; **Kõik vabas vormis arved**.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-109">Click **Accounts receivable** &gt; **Invoices** &gt; **All free text invoices**.</span></span>
2.  <span data-ttu-id="e4c2f-110">Valige vabas vormis arve, mille jaoks loote kreeditarvet.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-110">Select the free text invoice that you are creating a credit note for.</span></span>
3.  <span data-ttu-id="e4c2f-111">Klõpsake toimingupaanil vahekaardi **Arve** grupis **Tühista** valikut **Loo kreeditarve**.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-111">On the Action Pane, in the **Cancel** group of the **Invoice** tab, click **Create credit note**.</span></span> <span data-ttu-id="e4c2f-112">**Märkus.** Kui loote kreeditarve, peate kaasama vabas vormis arve kõik kanderead.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-112">**Note:** When you create a credit note, you must include each transaction line from the free text invoice.</span></span>
4.  <span data-ttu-id="e4c2f-113">Märkige ruut **Loo parandusread**, et lisada kreeditarvele tühistamisrida ja parandusrida vabas vormis arve iga kanderea kohta.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-113">Select the **Create corrective lines** check box to add a reversal line and a corrective line to the credit note for each transaction line in the original free text invoice.</span></span>
5.  <span data-ttu-id="e4c2f-114">Sisestage kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-114">Post the credit note.</span></span>

<span data-ttu-id="e4c2f-115">Põhivara likvideerimise kanded, mis loodi kreeditarve sisestamisel, tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-115">The fixed asset disposal transactions, created when you posted the credit note, are reversed.</span></span> <span data-ttu-id="e4c2f-116">Põhivara olekuks jääb **Müüdud**.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-116">The status of the fixed asset remains **Sold**.</span></span> <span data-ttu-id="e4c2f-117">Vajaduse korral saate siiski põhivara olekut käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="e4c2f-117">You can still change the status of the fixed asset manually, if necessary.</span></span>




