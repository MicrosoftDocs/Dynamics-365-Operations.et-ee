---
title: Põhivaragruppide häälestamine
description: Selles teemas tutvustatakse, kuidas luua uut põhivara rühma.
author: saraschi2
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c1b97193f09cfbb943522ca7af6bace9a14d9cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819550"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="92c7d-103">Põhivaragruppide häälestamine</span><span class="sxs-lookup"><span data-stu-id="92c7d-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92c7d-104">Selles teemas tutvustatakse, kuidas luua uut põhivara rühma.</span><span class="sxs-lookup"><span data-stu-id="92c7d-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="92c7d-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="92c7d-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="92c7d-106">Avage navigeerimispaanil **Moodulid > Põhivarad > Seadistus > Põhivara rühmad**.</span><span class="sxs-lookup"><span data-stu-id="92c7d-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="92c7d-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92c7d-107">Select **New**.</span></span>
3. <span data-ttu-id="92c7d-108">Sisestage väärtus väljale **Põhivara rühm**.</span><span class="sxs-lookup"><span data-stu-id="92c7d-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="92c7d-109">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="92c7d-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="92c7d-110">Põhivarade ja numbrijada koodi automaatnummerdamine rühmas **Põhivara** kirjutab üle põhivara parameetrite sätted.</span><span class="sxs-lookup"><span data-stu-id="92c7d-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="92c7d-111">Saate seda muuta siin, kui selle põhivaragrupi varadel on teistest gruppidest erinev nummerdus.</span><span class="sxs-lookup"><span data-stu-id="92c7d-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="92c7d-112">Valige **Materjalid**.</span><span class="sxs-lookup"><span data-stu-id="92c7d-112">Select **Books**.</span></span>
6. <span data-ttu-id="92c7d-113">Sisestage või valige väärtus väljale **Raamat**.</span><span class="sxs-lookup"><span data-stu-id="92c7d-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="92c7d-114">Väli **Kuluarvestus** on seadistatud olekusse **Jah**, et vara materjal oleks kaasatud kulumi pakkumistesse.</span><span class="sxs-lookup"><span data-stu-id="92c7d-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="92c7d-115">Kui **Kuluarvestus** on seadistatud olekusse **Ei**, ei aegu vara automaatselt.</span><span class="sxs-lookup"><span data-stu-id="92c7d-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="92c7d-116">Seadistage vara kasutusiga aastates.</span><span class="sxs-lookup"><span data-stu-id="92c7d-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="92c7d-117">Pange tähele, et välja **Kuluperioodid** väärtust arvutatakse pärast teenindusaja seadistamist.</span><span class="sxs-lookup"><span data-stu-id="92c7d-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="92c7d-118">Valige suvand väljal **Kulukonventsioon**.</span><span class="sxs-lookup"><span data-stu-id="92c7d-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="92c7d-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="92c7d-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]