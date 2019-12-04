---
title: Põhivarakannete sisestamine sisestuskihtidele
description: See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul.
author: ShylaThompson
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
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8c4f4f41ed39447ae441dd8e01cfcf80c939b5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770708"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="6dd71-103">Põhivarakannete sisestamine sisestuskihtidele</span><span class="sxs-lookup"><span data-stu-id="6dd71-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dd71-104">See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul.</span><span class="sxs-lookup"><span data-stu-id="6dd71-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="6dd71-105">Põhivara amortiseeritakse sageli mitmel viisil ja eri eesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="6dd71-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="6dd71-106">Maksueesmärgil arvutatakse kulum praeguste maksureeglite alusel, et saavutada suurima võimalik maksustuseelne kulum, kuid aruandluseks arvutatakse kulum vastavalt raamatupidamisseadustele ja -standarditele.</span><span class="sxs-lookup"><span data-stu-id="6dd71-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="6dd71-107">Eri liiki kulumeid arvutatakse ja kirjendatakse sisestuskihtides ükshaaval.</span><span class="sxs-lookup"><span data-stu-id="6dd71-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="6dd71-108">Iga põhivaraga seotud raamat seadistatakse kindla sisestuskihi jaoks, millel on üldine kulumieesmärk.</span><span class="sxs-lookup"><span data-stu-id="6dd71-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="6dd71-109">Sisestuskihte on kümme: praegune, toimingud, maks ja seitse kohandatud kihti.</span><span class="sxs-lookup"><span data-stu-id="6dd71-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="6dd71-110">Raamatu puhul saab pearaamatusse sisestamise ka keelata, määrates valiku Sisesta pearaamatusse sätteks Ei.</span><span class="sxs-lookup"><span data-stu-id="6dd71-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="6dd71-111">Seejärel seatakse välja Sisestamiskiht väärtuseks automaatselt Puudub.</span><span class="sxs-lookup"><span data-stu-id="6dd71-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="6dd71-112">Tavaliselt kasutatakse raamatuid, mis pearaamatusse ei sisesta, maksuaruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="6dd71-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="6dd71-113">See lähenemine lisab paindlikkust vararegistri varasemate kannete kustutamisel, kuna neid pole pearaamatuga kooskõlastatud.</span><span class="sxs-lookup"><span data-stu-id="6dd71-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="6dd71-114">Põhivara töölehed määratletakse lehel Töölehtede nimed, valides suvandid Pearaamat > Töölehtede seadistus > Töölehtede nimed.</span><span class="sxs-lookup"><span data-stu-id="6dd71-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="6dd71-115">Iga tööleht, millele saate kulumeid sisestada, määratletakse töölehe nime alusel ainult ühe sisestuskihi kohta.</span><span class="sxs-lookup"><span data-stu-id="6dd71-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="6dd71-116">Töölehe sisestuskihti ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="6dd71-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="6dd71-117">See piirang aitab tagada, et iga sisestuskihi kanded hoitakse eraldi.</span><span class="sxs-lookup"><span data-stu-id="6dd71-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="6dd71-118">Iga sisestuskihi kohta peate looma vähemalt ühe töölehe.</span><span class="sxs-lookup"><span data-stu-id="6dd71-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="6dd71-119">Kui kasutate raamatuid, mis pearaamatusse ei sisesta, peate looma ka töölehe, milles sisestamiskihi sätteks on määratud Puudub.</span><span class="sxs-lookup"><span data-stu-id="6dd71-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="6dd71-120">Saate määrata põhivarakannete jaoks pearaamatukontosid lehel Põhivara sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="6dd71-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="6dd71-121">Igale sisestusreeglile tuleb valida vastav kandetüüp ja raamat ning seejärel määrata pearaamatukontod.</span><span class="sxs-lookup"><span data-stu-id="6dd71-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="6dd71-122">Saate seadistada sisestusreeglite kirje igale raamatule, mis sisestab pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="6dd71-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="6dd71-123">Tuletatud raamatute kasutamisel saate kandeid sisestada korraga eri sisestuskihtidesse.</span><span class="sxs-lookup"><span data-stu-id="6dd71-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="6dd71-124">Looge esmase raamatu kanded töölehel, mille sisestuskiht vastab raamatu sisestuskihile.</span><span class="sxs-lookup"><span data-stu-id="6dd71-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="6dd71-125">Sisestamise ajal kantakse tuletatud raamatu kanded vastavatesse sisestuskihtidesse.</span><span class="sxs-lookup"><span data-stu-id="6dd71-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="6dd71-126">Lisateavet vt teemadest [Tuletatud raamatud](derived-books.md) ja [Tuletatud raamatutega sisestus](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="6dd71-126">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>


