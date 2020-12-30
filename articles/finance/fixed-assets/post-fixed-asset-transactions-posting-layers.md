---
title: Põhivarakannete sisestamine sisestuskihtidele
description: See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a80e4d1a081b5bd8c58238b0f154f8fbdc660ccb
ms.sourcegitcommit: f80819c67c0a7475315fc68ce1cb568831e2c0e7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2020
ms.locfileid: "4493668"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="87845-103">Põhivarakannete sisestamine sisestuskihtidele</span><span class="sxs-lookup"><span data-stu-id="87845-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87845-104">See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul.</span><span class="sxs-lookup"><span data-stu-id="87845-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="87845-105">Põhivara amortiseeritakse sageli mitmel viisil ja eri eesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="87845-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="87845-106">Maksueesmärgil arvutatakse kulum praeguste maksureeglite alusel, et saavutada suurima võimalik maksustuseelne kulum, kuid aruandluseks arvutatakse kulum vastavalt raamatupidamisseadustele ja -standarditele.</span><span class="sxs-lookup"><span data-stu-id="87845-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="87845-107">Eri liiki kulumeid arvutatakse ja kirjendatakse sisestuskihtides ükshaaval.</span><span class="sxs-lookup"><span data-stu-id="87845-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="87845-108">Iga põhivaraga seotud raamat seadistatakse kindla sisestuskihi jaoks, millel on üldine kulumieesmärk.</span><span class="sxs-lookup"><span data-stu-id="87845-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="87845-109">Sisestuskihte on kümme: praegune, toimingud, maks ja seitse kohandatud kihti.</span><span class="sxs-lookup"><span data-stu-id="87845-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="87845-110">Raamatu puhul saab pearaamatusse sisestamise ka keelata, määrates valiku Sisesta pearaamatusse sätteks Ei.</span><span class="sxs-lookup"><span data-stu-id="87845-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="87845-111">Seejärel seatakse välja Sisestamiskiht väärtuseks automaatselt Puudub.</span><span class="sxs-lookup"><span data-stu-id="87845-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="87845-112">Tavaliselt kasutatakse raamatuid, mis pearaamatusse ei sisesta, maksuaruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="87845-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="87845-113">See lähenemine lisab paindlikkust vararegistri varasemate kannete kustutamisel, kuna neid pole pearaamatuga kooskõlastatud.</span><span class="sxs-lookup"><span data-stu-id="87845-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="87845-114">Põhivara töölehed määratletakse lehel Töölehtede nimed, valides suvandid Pearaamat > Töölehtede seadistus > Töölehtede nimed.</span><span class="sxs-lookup"><span data-stu-id="87845-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="87845-115">Iga tööleht, millele saate kulumeid sisestada, määratletakse töölehe nime alusel ainult ühe sisestuskihi kohta.</span><span class="sxs-lookup"><span data-stu-id="87845-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="87845-116">Töölehe sisestuskihti ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="87845-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="87845-117">See piirang aitab tagada, et iga sisestuskihi kanded hoitakse eraldi.</span><span class="sxs-lookup"><span data-stu-id="87845-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="87845-118">Iga sisestuskihi kohta peate looma vähemalt ühe töölehe.</span><span class="sxs-lookup"><span data-stu-id="87845-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="87845-119">Kui kasutate raamatuid, mis pearaamatusse ei sisesta, peate looma ka töölehe, milles sisestamiskihi sätteks on määratud Puudub.</span><span class="sxs-lookup"><span data-stu-id="87845-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="87845-120">Saate määrata põhivarakannete jaoks pearaamatukontosid lehel Põhivara sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="87845-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="87845-121">Igale sisestusreeglile tuleb valida vastav kandetüüp ja raamat ning seejärel määrata pearaamatukontod.</span><span class="sxs-lookup"><span data-stu-id="87845-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="87845-122">Saate seadistada sisestusreeglite kirje igale raamatule, mis sisestab pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="87845-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="87845-123">Põhivara saab sisestada dokumentidesse, mis toetavad ainult **Praegust** sisestamiskihti, nagu näiteks **Ostutellimus**, **Ootel hankija arve**, **Müügitellimus** või **Vabas vormis arve**.</span><span class="sxs-lookup"><span data-stu-id="87845-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="87845-124">Põhivara ID valimisel ükskõik millisel nendest dokumentidest on vararaamat filtreeritud **Kehtiva** sisestamiskihiga raamatule ja seda täidetakse sisestamise ajal automaatselt, kui süsteem valideerib, et põhivara sisestamiskihiti on **Kehtiv**.</span><span class="sxs-lookup"><span data-stu-id="87845-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="87845-125">Kui seda valideerimist ei saa lõpule viia, siis sisestamise protsess peatatakse.</span><span class="sxs-lookup"><span data-stu-id="87845-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="87845-126">Tuletatud raamatute kasutamisel saate kandeid sisestada korraga eri sisestuskihtidesse.</span><span class="sxs-lookup"><span data-stu-id="87845-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="87845-127">Esmase raamatu kanded luuakse tööraamatus või algdokumendis, kus sisestamiskiht vastab raamatu sisestamiskihile.</span><span class="sxs-lookup"><span data-stu-id="87845-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="87845-128">Sisestamise ajal kantakse tuletatud raamatu kanded vastavatesse sisestuskihtidesse.</span><span class="sxs-lookup"><span data-stu-id="87845-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="87845-129">Lisateavet vt teemadest [Tuletatud raamatud](derived-books.md) ja [Tuletatud raamatutega sisestus](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="87845-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



