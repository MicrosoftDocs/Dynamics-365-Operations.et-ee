---
title: "Väliskataloogide kasutamine e-hanke väljaregistreerimiseks"
description: "See teema selgitab, kuidas kasutada väliseid katalooge ostutaotluste koostamiseks ja esitamiseks."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8ccf810d3ecfeb35e86e7b552f7e59fc7660aa01
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="f1f55-103">Väliskataloogide kasutamine e-hanke väljaregistreerimiseks</span><span class="sxs-lookup"><span data-stu-id="f1f55-103">Use external catalogs for PunchOut eProcurement</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f1f55-104">Kasutades väliseid katalooge e-hanke väljaregistreerimiseks pole teil vaja hoida oma koondandmetes teavet oma hankija toodete kohta.</span><span class="sxs-lookup"><span data-stu-id="f1f55-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="f1f55-105">Selle asemel teisendatakse ostukorv hankija veebisaidil ostutaotluse ridadeks, millel on õiged tooteandmed.</span><span class="sxs-lookup"><span data-stu-id="f1f55-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="f1f55-106">Peaksite vältima oma hankija toodete kirjelduste ja hindade hoidmist oma toote koondandmetes.</span><span class="sxs-lookup"><span data-stu-id="f1f55-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="f1f55-107">Selle asemel kasutage e-hanke väljaregistreerimiseks väliseid katalooge.</span><span class="sxs-lookup"><span data-stu-id="f1f55-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="f1f55-108">Siis, kui töötajad koostavad ostutaotlusi, saavad nad registreerida end välja hankija välisele kataloogisaidile (teisisõnu lahkuvad nad teie süsteemist ja lähevad hankija saidile).</span><span class="sxs-lookup"><span data-stu-id="f1f55-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="f1f55-109">Siis saab tooted, mis lisatakse hankija veebisaidil ostukorvi, teisendada ostutaotluse ridadeks.</span><span class="sxs-lookup"><span data-stu-id="f1f55-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="f1f55-110">Seetõttu saate õige tooteteabe: toote ID, nimi, hind jne.</span><span class="sxs-lookup"><span data-stu-id="f1f55-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="f1f55-111">Väliste kataloogide kasutamiseks peab töötaja looma ostutaotluse lehel **Minu ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="f1f55-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="f1f55-112">Töötajat, kes ostutaotluse loob, nimetatakse ostutaotluse koostajaks.</span><span class="sxs-lookup"><span data-stu-id="f1f55-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="f1f55-113">Koostajana võite teha järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="f1f55-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="f1f55-114">Kasutage reatoimingut **Välised kataloogid**, et avada leht, mis sisaldab kõiki konkreetse nõude esitaja, ostva juriidilise isiku ja vastuvõtva tootmisüksuse puhul saadaolevaid väliseid katalooge.</span><span class="sxs-lookup"><span data-stu-id="f1f55-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="f1f55-115">Olenevalt teie õigustest muutke nõude esitajat, ostvat juriidilist isikut ja vastuvõtvat tootmisüksust.</span><span class="sxs-lookup"><span data-stu-id="f1f55-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="f1f55-116">Nende väärtuste muutmisel võib muutuda nõude esitajale kättesaadavate väliste kataloogide loend.</span><span class="sxs-lookup"><span data-stu-id="f1f55-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="f1f55-117">Saadaolevad välised kataloogid olenevad ostva juriidilise isiku või vastuvõtva tootmisüksuse kehtivatest aktiivsetest ostupoliitikatest.</span><span class="sxs-lookup"><span data-stu-id="f1f55-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="f1f55-118">Need poliitikad võivad lubada või keelata juurdepääsu konkreetsetele hankekategooriatele.</span><span class="sxs-lookup"><span data-stu-id="f1f55-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="f1f55-119">Seetõttu võib see mõjutada nende hankekategooriatega vastendatud väliste kataloogide loendit.</span><span class="sxs-lookup"><span data-stu-id="f1f55-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="f1f55-120">Poliitikate seadistamise kohta leiate lisateavet jaotisest [Ostupoliitikad](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="f1f55-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="f1f55-121">Konkreetsete hankekategooriate puhul väliste kataloogide leidmiseks sisestage tekst kataloogi otsinguväljale.</span><span class="sxs-lookup"><span data-stu-id="f1f55-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="f1f55-122">Toodete lisamiseks hankija välisest kataloogist hankija veebisaidil klõpsake välist kataloogi.</span><span class="sxs-lookup"><span data-stu-id="f1f55-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="f1f55-123">Seejärel lisage ostukorvi tooteid ja makske. Ostukorvi read edastatakse rakendusse Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f1f55-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="f1f55-124">Kui hankekategooriate puhul on mitu valikut, siis valige enne ostutaotlusele ridade lisamist õige hankekategooria.</span><span class="sxs-lookup"><span data-stu-id="f1f55-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="f1f55-125">Pärast ostutaotlusele ridade lisamist võite lisada veel ridu, väliseid katalooge kasutamata.</span><span class="sxs-lookup"><span data-stu-id="f1f55-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="f1f55-126">Teise võimalusena võite jätkata väliste kataloogide kasutamist ridade lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="f1f55-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="f1f55-127">Kui ostutaotlus on valmis, kasutage toimingut **Töövoog** > **Edasta**, et edastada see kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f1f55-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

