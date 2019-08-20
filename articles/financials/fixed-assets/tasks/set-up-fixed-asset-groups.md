---
title: Saate häälestada põhivaragruppe.
description: See protseduur näitab, kuidas luua uut põhivaragruppi.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f52b73c07aad1047d6e6e7caf80daecc9c26e7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839781"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="bfbdf-103">Saate häälestada põhivaragruppe.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bfbdf-104">See protseduur näitab, kuidas luua uut põhivaragruppi.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="bfbdf-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="bfbdf-106">Avage Põhivarad > Seadistus > Põhivaragrupid.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="bfbdf-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-107">Click New.</span></span>
3. <span data-ttu-id="bfbdf-108">Sisestage väärtus väljale Põhivara grupp.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="bfbdf-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="bfbdf-110">Põhivaragrupi suvandid Nummerda põhivarad automaatselt ja Numbriseeria kood alistavad põhivarade parameetrite sätted.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="bfbdf-111">Saate seda muuta siin, kui selle põhivaragrupi varadel on teistest gruppidest erinev nummerdus.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="bfbdf-112">Klõpsake valikut Raamatud.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-112">Click Books.</span></span>
6. <span data-ttu-id="bfbdf-113">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="bfbdf-114">Väli Kulumiarvestus on seatud valikule Jah, mistõttu kaasatakse vara raamat kulumisoovitustesse.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="bfbdf-115">Kui väli Kulumiarvestus on seatud valikule Ei, ei amortiseerita vara automaatselt.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="bfbdf-116">Seadistage vara kasutusiga aastates.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="bfbdf-117">Pange tähele, et välja Kulumiperioodid väärtus arvutatakse pärast kasutusea seadistamist.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="bfbdf-118">Valige suvand väljalt Kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="bfbdf-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bfbdf-119">Close the page.</span></span>

