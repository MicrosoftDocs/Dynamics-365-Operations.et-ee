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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 153b6437205d5a849fa6a90c0d3b9f3d51dd6768
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557355"
---
# <a name="derived-books"></a><span data-ttu-id="2db5a-103">Tuletatud raamatud</span><span class="sxs-lookup"><span data-stu-id="2db5a-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2db5a-104">Selles artiklis antakse ülevaade tuletatud raamatu funktsioonist.</span><span class="sxs-lookup"><span data-stu-id="2db5a-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="2db5a-105">Tuletatud raamatuid kasutatakse kindla intervalliga plaanitud põhivara raamatu kannete sisestamise lihtsustamiseks.</span><span class="sxs-lookup"><span data-stu-id="2db5a-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="2db5a-106">Saate valida ühe raamatu esmaseks raamatuks.</span><span class="sxs-lookup"><span data-stu-id="2db5a-106">You choose one book as the primary book.</span></span> <span data-ttu-id="2db5a-107">Tavaliselt on see raamat, mida kasutatakse kulumi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="2db5a-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="2db5a-108">Seejärel saate sellega siduda muud raamatud, mis on seadistatud esmase raamatuga sama intervalliga kandeid sisestama.</span><span class="sxs-lookup"><span data-stu-id="2db5a-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="2db5a-109">Maksukulumi raamatud seadistatakse sageli tuletatud raamatutena.</span><span class="sxs-lookup"><span data-stu-id="2db5a-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="2db5a-110">Kõige tavalisemad tuletatud raamatutesse sisestamiseks seadistatud kanded on soetamised, soetuse korrigeerimised ja likvideerimised.</span><span class="sxs-lookup"><span data-stu-id="2db5a-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="2db5a-111">Näide</span><span class="sxs-lookup"><span data-stu-id="2db5a-111">Example</span></span>

<span data-ttu-id="2db5a-112">Raamatud B ja C on seadistatud raamatu A tuletatud raamatutena soetuskande tüübi puhul.</span><span class="sxs-lookup"><span data-stu-id="2db5a-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="2db5a-113">Sisestate raamatusse A vara 123 soetuskande summas 1500.00.</span><span class="sxs-lookup"><span data-stu-id="2db5a-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="2db5a-114">Kande sisestamisel luuakse soetuskanne ning sisestatakse varasse 123 raamatu B puhul ja varasse 123 raamatu C puhul väärtusega 1500,00.</span><span class="sxs-lookup"><span data-stu-id="2db5a-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="2db5a-115">Kui valmistate ette esmase raamatu kandeid põhivara töölehele sisestamiseks, saate vaadata ja muuta ka tuletatud raamatute kandeid.</span><span class="sxs-lookup"><span data-stu-id="2db5a-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="2db5a-116">Tuletatud väärtusega kandeid ei kuvata esmase raamatu kannete ettevalmistamisel mõnel muul töölehel.</span><span class="sxs-lookup"><span data-stu-id="2db5a-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="2db5a-117">Esmase raamatu kannete sisestamisel sisestatakse need siiski määratud kontodele ja sisestuskihtidele.</span><span class="sxs-lookup"><span data-stu-id="2db5a-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="2db5a-118">Raamatud, mis on seadistatud kannete sisestamiseks esmaste raamatute intervallidest erinevate intervallidega, tuleb põhivaraga siduda eraldi, mitte tuletatud raamatutena.</span><span class="sxs-lookup"><span data-stu-id="2db5a-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="2db5a-119">Lisateavet vt teemast [Sisestamine tuletatud raamatute kaudu](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="2db5a-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>



