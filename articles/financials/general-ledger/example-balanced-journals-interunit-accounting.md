---
title: "Tasakaalustatud töölehed sisekäibe jaoks"
description: "See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon."
author: twheeloc
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5b1d788ebd5617a1d3f1c8ca36f5ae3c29b534c5
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="57ef6-103">Tasakaalustatud töölehed sisekäibe jaoks</span><span class="sxs-lookup"><span data-stu-id="57ef6-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="57ef6-104">See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon.</span><span class="sxs-lookup"><span data-stu-id="57ef6-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="57ef6-105">Kui kontokirjed ei tasakaalust finantsdimensiooni väärtuste tasandil, luuakse automaatselt täiendavad kontokirjed, et töölehte tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="57ef6-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="57ef6-106">Need kontokirjed kasutavad lehel **Automaatsete kannete kontod** sisestustüüpe **Üksustevaheline – deebet** ja**Üksustevaheline – kreedit**, et määrata põhikonto.</span><span class="sxs-lookup"><span data-stu-id="57ef6-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="57ef6-107">Näiteks on tasakaalustava finantsdimensioonina valitud Äriüksus, mis on pearaamatukonto teine segment, ja loomisel on järgmised raamatupidamiskirjed.</span><span class="sxs-lookup"><span data-stu-id="57ef6-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="57ef6-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="57ef6-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="57ef6-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="57ef6-109">100.00 DR</span></span> |
| <span data-ttu-id="57ef6-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="57ef6-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="57ef6-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="57ef6-111">100.00 DR</span></span> |
| <span data-ttu-id="57ef6-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="57ef6-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="57ef6-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="57ef6-113">200.00 CR</span></span> |

<span data-ttu-id="57ef6-114">Sellisel juhul määratakse järgmised saldod.</span><span class="sxs-lookup"><span data-stu-id="57ef6-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="57ef6-115">Äriüksusele MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="57ef6-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="57ef6-116">Äriüksusele NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="57ef6-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="57ef6-117">Seega luuakse järgmised raamatupidamiskirjed automaatselt, et tasakaalustada tööleht finantsdimensiooni väärtuste tasemel.</span><span class="sxs-lookup"><span data-stu-id="57ef6-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="57ef6-118">(Üksustevaheline deebet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="57ef6-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="57ef6-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="57ef6-119">100.00 DR</span></span> |
| <span data-ttu-id="57ef6-120">(Üksustevaheline kreedit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="57ef6-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="57ef6-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="57ef6-121">100.00 CR</span></span> |






