--- 
title: "Saate häälestada põhivaragruppe."
description: "See protseduur näitab, kuidas luua uut põhivaragruppi."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c44ce1219c0fc860d621aa32c8eec7c5d640fa03
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="98bb2-103">Saate häälestada põhivaragruppe.</span><span class="sxs-lookup"><span data-stu-id="98bb2-103">Set up fixed asset groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98bb2-104">See protseduur näitab, kuidas luua uut põhivaragruppi.</span><span class="sxs-lookup"><span data-stu-id="98bb2-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="98bb2-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="98bb2-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="98bb2-106">Avage Põhivarad > Seadistus > Põhivaragrupid.</span><span class="sxs-lookup"><span data-stu-id="98bb2-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="98bb2-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="98bb2-107">Click New.</span></span>
3. <span data-ttu-id="98bb2-108">Sisestage väärtus väljale Põhivara grupp.</span><span class="sxs-lookup"><span data-stu-id="98bb2-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="98bb2-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="98bb2-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="98bb2-110">Põhivaragrupi suvandid Nummerda põhivarad automaatselt ja Numbriseeria kood alistavad põhivarade parameetrite sätted.</span><span class="sxs-lookup"><span data-stu-id="98bb2-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="98bb2-111">Saate seda muuta siin, kui selle põhivaragrupi varadel on teistest gruppidest erinev nummerdus.</span><span class="sxs-lookup"><span data-stu-id="98bb2-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="98bb2-112">Klõpsake valikut Raamatud.</span><span class="sxs-lookup"><span data-stu-id="98bb2-112">Click Books.</span></span>
6. <span data-ttu-id="98bb2-113">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="98bb2-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="98bb2-114">Väli Kulumiarvestus on seatud valikule Jah, mistõttu kaasatakse vara raamat kulumisoovitustesse.</span><span class="sxs-lookup"><span data-stu-id="98bb2-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="98bb2-115">Kui väli Kulumiarvestus on seatud valikule Ei, ei amortiseerita vara automaatselt.</span><span class="sxs-lookup"><span data-stu-id="98bb2-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="98bb2-116">Seadistage vara kasutusiga aastates.</span><span class="sxs-lookup"><span data-stu-id="98bb2-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="98bb2-117">Pange tähele, et välja Kulumiperioodid väärtus arvutatakse pärast kasutusea seadistamist.</span><span class="sxs-lookup"><span data-stu-id="98bb2-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="98bb2-118">Valige suvand väljalt Kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="98bb2-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="98bb2-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="98bb2-119">Close the page.</span></span>


