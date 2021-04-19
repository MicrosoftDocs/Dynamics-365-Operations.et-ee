---
title: Garantiilepingud
description: Selles teemas selgitatakse garantiilepinguid varahalduses.
author: johanhoffmann
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5644b5076aeda30d5535c0128497e267359583a2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808204"
---
# <a name="warranty-agreements"></a><span data-ttu-id="5ba2f-103">Garantiilepingud</span><span class="sxs-lookup"><span data-stu-id="5ba2f-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="5ba2f-104">Varahalduses saate seadistada garantii tingimused, mida saab siduda vara või varatüübiga.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="5ba2f-105">Garantiitingimused luuakse kindla perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="5ba2f-106">Garantii saab seadistada nii, et see võimaldaks täielikku katvust või osalist katvust, ning saate seadistada tundide, kulude ja kaupadega seotud tingimused.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="5ba2f-107">Esimene samm on luua hankija garantiilepingud, mis teil on oma varustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="5ba2f-108">Seejärel lisage varade või varatüüpide garantiilepingud.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="5ba2f-109">Hankija garantiilepinguid kasutatakse ainult informatiivsel eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="5ba2f-110">Kui hankija garantii on seadistatud varale, saate vaadata vara garantii laovarude perioodi.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="5ba2f-111">Garantiilepingu loomine</span><span class="sxs-lookup"><span data-stu-id="5ba2f-111">Create a warranty agreement</span></span>

<span data-ttu-id="5ba2f-112">Garantiileping võib sisaldada mitut lepingurida, mis katavad tööaja, kulude ja kaupade garantii.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="5ba2f-113">Valige **Varahaldus** \> **Seadistus** \> **Varad** \> **Garantii**.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="5ba2f-114">Valige **Uus**, et luua uus toode.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="5ba2f-115">Sisestage garantii ID väljale **Garantii**.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="5ba2f-116">Väljale **Nimi** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="5ba2f-117">Kiirkaardil **Üksikasjad** kuvatakse väljal **Varad** aktiivsete varade arv, mis kasutavad garantiilepingut.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="5ba2f-118">Järgige kiirkaardil **Garantiiread** neid toiminguid garantiilepingusse kaasatavate ridade lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="5ba2f-119">Valige suvand **Lisa rida**, et lisada garantiile uus tingimus.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="5ba2f-120">Väljale **Rida** sisestatakse automaatselt seerianumber.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="5ba2f-121">Valige garantiiperioodi tüüp väljal **Periood**.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="5ba2f-122">Sisestage number väljale **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="5ba2f-123">See väli määratleb perioodide arvu, millele garantii peaks kehtima.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="5ba2f-124">Sisestage väljale **Protsent** garantii rea laovarude protsent.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="5ba2f-125">Protsent näitab, kui palju teie ettevõte katab.</span><span class="sxs-lookup"><span data-stu-id="5ba2f-125">The percentage indicates how much is covered by your company.</span></span>

![Garantiileht](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]