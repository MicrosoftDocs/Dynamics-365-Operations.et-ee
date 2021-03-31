---
title: Põhivara kulumi arvutamine juriidiliste isikute lõikes
description: Mitme juriidilise isiku põhivara kulumit saab käitada ühe etapina.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d228c387e8a6bf956f729a69e2296130db32dbd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210043"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="8f4cc-103">Põhivara kulumi arvutamine juriidiliste isikute lõikes</span><span class="sxs-lookup"><span data-stu-id="8f4cc-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f4cc-104">Mitme juriidilise isiku põhivara kulumit saab käitada ühe etapina.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="8f4cc-105">See protseduur näitab, kuidas seadistada ja käitada protsessi mitme juriidilise isiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="8f4cc-106">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="8f4cc-107">Kontsernisiseste kulumikäituste töölehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="8f4cc-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="8f4cc-108">Avage Põhivarad > Seadistus > Põhivarade parameetrid.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="8f4cc-109">Laiendage jaotist Põhivara ettepanekud.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="8f4cc-110">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-110">Click Add.</span></span>
4. <span data-ttu-id="8f4cc-111">Valige või sisestage väärtus väljal Sisestamiskiht.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="8f4cc-112">Valige või sisestage väärtus väljal Töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="8f4cc-113">Korrake töölehe seadistust iga juriidilise isiku lehel Põhivara parameetrid.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="8f4cc-114">Amortiseerimine</span><span class="sxs-lookup"><span data-stu-id="8f4cc-114">Depreciation run</span></span>
1. <span data-ttu-id="8f4cc-115">Avage Põhivarad > Töölehe kirjed > Kulumisoovituse koostamine.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="8f4cc-116">Valige või sisestage väärtus väljal Sisestamiskiht.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="8f4cc-117">Töölehe nimi põhineb põhivara parameetrites määratud vaikesättel.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="8f4cc-118">Seda saab praeguse juriidilise isiku jaoks siin muuta.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="8f4cc-119">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="8f4cc-120">Valige kulumikäitusesse kaasatavad juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="8f4cc-121">Loendis kuvatakse ainult juriidilised isikud, kelle töölehed on põhivara parameetrite lehel põhivara ettepanekute jaoks häälestatud.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="8f4cc-122">Valige väljal Sisesta töölehed väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="8f4cc-123">Filtreerimisväljad hõlmavad kõiki selle kulumikäituse jaoks valitud juriidiliste isikute põhivarasid, gruppe ja raamatuid.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="8f4cc-124">Suvand Pakktöötlus on vaikimisi lubatud.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="8f4cc-125">Kui suvand on lubatud, toimub kulumitöölehe loomine ja sisestamine taustal.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="8f4cc-126">Klõpsake suvandit Loo tööleht.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-126">Click Create journal.</span></span>
6. <span data-ttu-id="8f4cc-127">Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.</span><span class="sxs-lookup"><span data-stu-id="8f4cc-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]