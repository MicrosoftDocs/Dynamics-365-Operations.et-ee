---
title: Tuletatud raamatud
description: Selles artiklis antakse ülevaade tuletatud raamatu funktsioonist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c31116ba234bd1fce445ac382fe8f8aea263a66
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769473"
---
# <a name="derived-books"></a><span data-ttu-id="9b759-103">Tuletatud raamatud</span><span class="sxs-lookup"><span data-stu-id="9b759-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b759-104">Selles artiklis antakse ülevaade tuletatud raamatu funktsioonist.</span><span class="sxs-lookup"><span data-stu-id="9b759-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="9b759-105">Tuletatud raamatuid kasutatakse kindla intervalliga plaanitud põhivara raamatu kannete sisestamise lihtsustamiseks.</span><span class="sxs-lookup"><span data-stu-id="9b759-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="9b759-106">Saate valida ühe raamatu esmaseks raamatuks.</span><span class="sxs-lookup"><span data-stu-id="9b759-106">You choose one book as the primary book.</span></span> <span data-ttu-id="9b759-107">Tavaliselt on see raamat, mida kasutatakse kulumi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="9b759-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="9b759-108">Seejärel saate sellega siduda muud raamatud, mis on seadistatud esmase raamatuga sama intervalliga kandeid sisestama.</span><span class="sxs-lookup"><span data-stu-id="9b759-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="9b759-109">Maksukulumi raamatud seadistatakse sageli tuletatud raamatutena.</span><span class="sxs-lookup"><span data-stu-id="9b759-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="9b759-110">Kõige tavalisemad tuletatud raamatutesse sisestamiseks seadistatud kanded on soetamised, soetuse korrigeerimised ja likvideerimised.</span><span class="sxs-lookup"><span data-stu-id="9b759-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="9b759-111">Näide</span><span class="sxs-lookup"><span data-stu-id="9b759-111">Example</span></span>

<span data-ttu-id="9b759-112">Raamatud B ja C on seadistatud raamatu A tuletatud raamatutena soetuskande tüübi puhul.</span><span class="sxs-lookup"><span data-stu-id="9b759-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="9b759-113">Sisestate raamatusse A vara 123 soetuskande summas 1500.00.</span><span class="sxs-lookup"><span data-stu-id="9b759-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="9b759-114">Kande sisestamisel luuakse soetuskanne ning sisestatakse varasse 123 raamatu B puhul ja varasse 123 raamatu C puhul väärtusega 1500,00.</span><span class="sxs-lookup"><span data-stu-id="9b759-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="9b759-115">Kui valmistate ette esmase raamatu kandeid põhivara töölehele sisestamiseks, saate vaadata ja muuta ka tuletatud raamatute kandeid.</span><span class="sxs-lookup"><span data-stu-id="9b759-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="9b759-116">Tuletatud väärtusega kandeid ei kuvata esmase raamatu kannete ettevalmistamisel mõnel muul töölehel.</span><span class="sxs-lookup"><span data-stu-id="9b759-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="9b759-117">Esmase raamatu kannete sisestamisel sisestatakse need siiski määratud kontodele ja sisestuskihtidele.</span><span class="sxs-lookup"><span data-stu-id="9b759-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="9b759-118">Raamatud, mis on seadistatud kannete sisestamiseks esmaste raamatute intervallidest erinevate intervallidega, tuleb põhivaraga siduda eraldi, mitte tuletatud raamatutena.</span><span class="sxs-lookup"><span data-stu-id="9b759-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="9b759-119">Lisateavet leiate teemast [Postitage tuletatud raamatutega](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="9b759-119">For more information, see [Post with derived books](post-derived-value-models.md).</span></span>



