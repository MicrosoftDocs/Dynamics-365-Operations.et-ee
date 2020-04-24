---
title: Garantiilepingud
description: Selles teemas selgitatakse garantiilepinguid varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e9cbb9068101f3004179f338da18af0369190807
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215374"
---
# <a name="warranty-agreements"></a><span data-ttu-id="7af22-103">Garantiilepingud</span><span class="sxs-lookup"><span data-stu-id="7af22-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="7af22-104">Varahalduses saate seadistada garantii tingimused, mida saab siduda vara või varatüübiga.</span><span class="sxs-lookup"><span data-stu-id="7af22-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="7af22-105">Garantiitingimused luuakse kindla perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="7af22-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="7af22-106">Garantii saab seadistada nii, et see võimaldaks täielikku katvust või osalist katvust, ning saate seadistada tundide, kulude ja kaupadega seotud tingimused.</span><span class="sxs-lookup"><span data-stu-id="7af22-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="7af22-107">Esimene samm on luua hankija garantiilepingud, mis teil on oma varustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="7af22-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="7af22-108">Seejärel lisage varade või varatüüpide garantiilepingud.</span><span class="sxs-lookup"><span data-stu-id="7af22-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="7af22-109">Hankija garantiilepinguid kasutatakse ainult informatiivsel eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="7af22-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="7af22-110">Kui hankija garantii on seadistatud varale, saate vaadata vara garantii laovarude perioodi.</span><span class="sxs-lookup"><span data-stu-id="7af22-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="7af22-111">Garantiilepingu loomine</span><span class="sxs-lookup"><span data-stu-id="7af22-111">Create a warranty agreement</span></span>

<span data-ttu-id="7af22-112">Garantiileping võib sisaldada mitut lepingurida, mis katavad tööaja, kulude ja kaupade garantii.</span><span class="sxs-lookup"><span data-stu-id="7af22-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="7af22-113">Valige **Varahaldus** \> **Seadistus** \> **Varad** \> **Garantii**.</span><span class="sxs-lookup"><span data-stu-id="7af22-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="7af22-114">Valige **Uus**, et luua uus toode.</span><span class="sxs-lookup"><span data-stu-id="7af22-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="7af22-115">Sisestage garantii ID väljale **Garantii**.</span><span class="sxs-lookup"><span data-stu-id="7af22-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="7af22-116">Väljale **Nimi** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="7af22-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="7af22-117">Kiirkaardil **Üksikasjad** kuvatakse väljal **Varad** aktiivsete varade arv, mis kasutavad garantiilepingut.</span><span class="sxs-lookup"><span data-stu-id="7af22-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="7af22-118">Järgige kiirkaartidel **Tunnigarantii** ja **Kaubagarantii** neid samme, et lisada ridu, mis tuleb kaasata tundide või kaupadega seotud garantiilepingusse.</span><span class="sxs-lookup"><span data-stu-id="7af22-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="7af22-119">Valige suvand **Lisa rida**, et lisada garantiile uus tingimus.</span><span class="sxs-lookup"><span data-stu-id="7af22-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="7af22-120">Väljale **Rida** sisestatakse automaatselt seerianumber.</span><span class="sxs-lookup"><span data-stu-id="7af22-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="7af22-121">Valige garantiiperioodi tüüp väljal **Periood**.</span><span class="sxs-lookup"><span data-stu-id="7af22-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="7af22-122">Sisestage number väljale **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="7af22-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="7af22-123">See väli määratleb perioodide arvu, millele garantii peaks kehtima.</span><span class="sxs-lookup"><span data-stu-id="7af22-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="7af22-124">Sisestage väljale **Protsent** garantii rea laovarude protsent.</span><span class="sxs-lookup"><span data-stu-id="7af22-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="7af22-125">Protsent näitab, kui palju teie ettevõte katab.</span><span class="sxs-lookup"><span data-stu-id="7af22-125">The percentage indicates how much is covered by your company.</span></span>

![Garantii leht](media/01-warranty.png)
