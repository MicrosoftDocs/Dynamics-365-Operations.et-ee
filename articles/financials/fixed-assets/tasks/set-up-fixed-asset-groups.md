---
title: Põhivaragruppide häälestamine
description: Selles teemas tutvustatakse, kuidas luua uut põhivara rühma.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867531"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="c67ff-103">Põhivaragruppide häälestamine</span><span class="sxs-lookup"><span data-stu-id="c67ff-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c67ff-104">Selles teemas tutvustatakse, kuidas luua uut põhivara rühma.</span><span class="sxs-lookup"><span data-stu-id="c67ff-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="c67ff-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="c67ff-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="c67ff-106">Avage navigeerimispaanil **Moodulid > Põhivarad > Seadistus > Põhivara rühmad**.</span><span class="sxs-lookup"><span data-stu-id="c67ff-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="c67ff-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c67ff-107">Select **New**.</span></span>
3. <span data-ttu-id="c67ff-108">Sisestage väärtus väljale **Põhivara rühm**.</span><span class="sxs-lookup"><span data-stu-id="c67ff-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="c67ff-109">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c67ff-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="c67ff-110">Põhivarade ja numbrijada koodi automaatnummerdamine rühmas **Põhivara** kirjutab üle põhivara parameetrite sätted.</span><span class="sxs-lookup"><span data-stu-id="c67ff-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="c67ff-111">Saate seda muuta siin, kui selle põhivaragrupi varadel on teistest gruppidest erinev nummerdus.</span><span class="sxs-lookup"><span data-stu-id="c67ff-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="c67ff-112">Valige **Materjalid**.</span><span class="sxs-lookup"><span data-stu-id="c67ff-112">Select **Books**.</span></span>
6. <span data-ttu-id="c67ff-113">Sisestage või valige väärtus väljale **Raamat**.</span><span class="sxs-lookup"><span data-stu-id="c67ff-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="c67ff-114">Väli **Kuluarvestus** on seadistatud olekusse **Jah**, et vara materjal oleks kaasatud kulumi pakkumistesse.</span><span class="sxs-lookup"><span data-stu-id="c67ff-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="c67ff-115">Kui **Kuluarvestus** on seadistatud olekusse **Ei**, ei aegu vara automaatselt.</span><span class="sxs-lookup"><span data-stu-id="c67ff-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="c67ff-116">Seadistage vara kasutusiga aastates.</span><span class="sxs-lookup"><span data-stu-id="c67ff-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="c67ff-117">Pange tähele, et välja **Kuluperioodid** väärtust arvutatakse pärast teenindusaja seadistamist.</span><span class="sxs-lookup"><span data-stu-id="c67ff-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="c67ff-118">Valige suvand väljal **Kulukonventsioon**.</span><span class="sxs-lookup"><span data-stu-id="c67ff-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="c67ff-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c67ff-119">Close the page.</span></span>

