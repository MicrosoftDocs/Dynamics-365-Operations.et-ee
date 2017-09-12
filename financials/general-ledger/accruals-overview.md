---
title: "Viitvõlgade ülevaade"
description: "Selles artiklis kirjeldatakse viitvõlgu ning antakse teavet nende seadistamise ja kannete loomise kohta."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fb120715090638bf7c6c3833822d942cb6dda8c5
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="accruals-overview"></a><span data-ttu-id="2d918-103">Viitvõlgade ülevaade</span><span class="sxs-lookup"><span data-stu-id="2d918-103">Accruals overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2d918-104">Selles artiklis kirjeldatakse viitvõlgu ning antakse teavet nende seadistamise ja kannete loomise kohta.</span><span class="sxs-lookup"><span data-stu-id="2d918-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="2d918-105">Viitvõlgu kasutatakse tekkepõhises arvestuses tulu jälgimiseks, mis on tuvastatud selle teenimise perioodil, mitte makse saamisel, ja kulude jälgimiseks, mis on tuvastatud nende toimumisel, mitte makse tegemisel.</span><span class="sxs-lookup"><span data-stu-id="2d918-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="2d918-106">Viitvõlgade skeemid</span><span class="sxs-lookup"><span data-stu-id="2d918-106">Accrual schemes</span></span>
<span data-ttu-id="2d918-107">Viitvõlgade skeeme kasutatakse edasilükatud tulu ja kulude määramiseks ja sama viitvõlgade skeemi saab kasutada nii tulu kui ka kulude puhul.</span><span class="sxs-lookup"><span data-stu-id="2d918-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="2d918-108">Pearaamatu viitvõlad jaotavad tööleherea kulud või tulu nii, et kulud ja tulud tuvastatakse kindlatel perioodidel.</span><span class="sxs-lookup"><span data-stu-id="2d918-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="2d918-109">Lehel **Viitvõlgade skeem** määrate viitvõla skeemi rakendamisel kasutatava deebet- ja kreeditkonto.</span><span class="sxs-lookup"><span data-stu-id="2d918-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="2d918-110">**Deebet** – teie määratav põhikonto, mis asendab töölehekande real deebeti põhikonto.</span><span class="sxs-lookup"><span data-stu-id="2d918-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="2d918-111">Seda kontot kasutatakse ka viitvõla tagasivõtmiseks pearaamatu tekkepõhiste kannete põhjal.</span><span class="sxs-lookup"><span data-stu-id="2d918-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="2d918-112">**Kreedit** – teie määratav põhikonto, mis asendab töölehekande real kreediti põhikonto.</span><span class="sxs-lookup"><span data-stu-id="2d918-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="2d918-113">Seda kontot kasutatakse ka viitvõla tagasivõtmiseks pearaamatu tekkepõhiste kannete põhjal.</span><span class="sxs-lookup"><span data-stu-id="2d918-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="2d918-114">Pärast kasutatavate kontode määratlemist saate määrata, kuidas kandenumber tekkepõhiste kannete loomisel luuakse.</span><span class="sxs-lookup"><span data-stu-id="2d918-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="2d918-115">Samuti saate määrata, kui tihti kandeid esineb, kannete loomise arvu ja millal kanded sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="2d918-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="2d918-116">Pärast viitvõlgade skeemi loomist saate seda pearaamatu viitvõlgade funktsiooni abil kasutada mõnel töölehel.</span><span class="sxs-lookup"><span data-stu-id="2d918-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="2d918-117">Pearaamatu viitvõlad</span><span class="sxs-lookup"><span data-stu-id="2d918-117">Ledger accruals</span></span>
<span data-ttu-id="2d918-118">Töölehe sisestamisel saate klõpsata suvandit **Pearaamatu viitvõlad** menüüs **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="2d918-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="2d918-119">Seejärel näete viitvõlgade skeemi valimisel töölehe baassummat, mis jaotatakse viitvõlgade skeemis määratud perioodiks.</span><span class="sxs-lookup"><span data-stu-id="2d918-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="2d918-120">Näiteks kui maksate töötaja terve aasta kindlustuse jaanuaris ja summa on 12 000, peate selle kulu tuvastama iga kuu.</span><span class="sxs-lookup"><span data-stu-id="2d918-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="2d918-121">Saate valida alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="2d918-121">You can select the start date.</span></span> <span data-ttu-id="2d918-122">Saate ka määrata, kas kogunenud summa põhineb kontol või vastaskontol.</span><span class="sxs-lookup"><span data-stu-id="2d918-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="2d918-123">Pärast valikute tegemist klõpsake kõikide viitvõlgade skeemi alusel loodud kannete nägemiseks valikut **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="2d918-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="2d918-124">Näiteks kui jaotate 12 000 väärtuses kindlustuskulud kogu aastale, näete iga kuu puhul 1000.</span><span class="sxs-lookup"><span data-stu-id="2d918-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="2d918-125">Pärast töölehe sisestamist saate vaadata kandeid, kasutades päringulehte **Pearaamatu kanded**.</span><span class="sxs-lookup"><span data-stu-id="2d918-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="2d918-126">Kui viitvõlgade skeemi ei saa rakendada (näiteks kui müügitellimuse arve või ostutellimuse arve on seotud), saate ettemakstud summa krediteerida ja kulu summa debiteerida.</span><span class="sxs-lookup"><span data-stu-id="2d918-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="2d918-127">Seejärel saate viitvõlgade skeemi rakendamisel valida suvandi **Vastaskonto**.</span><span class="sxs-lookup"><span data-stu-id="2d918-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="2d918-128">Lisateabe saamiseks vt [Viitvõlaskeemide loomine](tasks/create-accrual-schemes.md) ja [Pearaamatusse tekkepõhiste kannete loomine](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2d918-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

