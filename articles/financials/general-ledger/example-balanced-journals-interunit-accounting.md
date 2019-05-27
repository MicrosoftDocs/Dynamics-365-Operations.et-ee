---
title: Tasakaalustatud töölehed sisekäibe jaoks
description: See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b596a2332a9ada01df7b4e718a79eb624ee52fc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549100"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="25065-103">Tasakaalustatud töölehed sisekäibe jaoks</span><span class="sxs-lookup"><span data-stu-id="25065-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25065-104">See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon.</span><span class="sxs-lookup"><span data-stu-id="25065-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="25065-105">Kui kontokirjed ei tasakaalust finantsdimensiooni väärtuste tasandil, luuakse automaatselt täiendavad kontokirjed, et töölehte tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="25065-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="25065-106">Need kontokirjed kasutavad lehel **Automaatsete kannete kontod** sisestustüüpe **Üksustevaheline – deebet** ja**Üksustevaheline – kreedit**, et määrata põhikonto.</span><span class="sxs-lookup"><span data-stu-id="25065-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="25065-107">Näiteks on tasakaalustava finantsdimensioonina valitud Äriüksus, mis on pearaamatukonto teine segment, ja loomisel on järgmised raamatupidamiskirjed.</span><span class="sxs-lookup"><span data-stu-id="25065-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="25065-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="25065-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="25065-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="25065-109">100.00 DR</span></span> |
| <span data-ttu-id="25065-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="25065-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="25065-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="25065-111">100.00 DR</span></span> |
| <span data-ttu-id="25065-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="25065-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="25065-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="25065-113">200.00 CR</span></span> |

<span data-ttu-id="25065-114">Sellisel juhul määratakse järgmised saldod.</span><span class="sxs-lookup"><span data-stu-id="25065-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="25065-115">Äriüksusele MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="25065-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="25065-116">Äriüksusele NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="25065-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="25065-117">Seega luuakse järgmised raamatupidamiskirjed automaatselt, et tasakaalustada tööleht finantsdimensiooni väärtuste tasemel.</span><span class="sxs-lookup"><span data-stu-id="25065-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="25065-118">(Üksustevaheline deebet) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="25065-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="25065-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="25065-119">100.00 DR</span></span> |
| <span data-ttu-id="25065-120">(Üksustevaheline kreedit) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="25065-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="25065-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="25065-121">100.00 CR</span></span> |





