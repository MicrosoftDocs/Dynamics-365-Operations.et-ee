---
title: Tootemudeli protsessi haldamine
description: Selle protseduuri käitamine nõuab toote konfiguratsioonimudeli olemasolu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921261"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="0e9e3-103">Tootemudeli protsessi haldamine</span><span class="sxs-lookup"><span data-stu-id="0e9e3-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e9e3-104">Selle protseduuri käitamine nõuab toote konfiguratsioonimudeli olemasolu.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="0e9e3-105">See protseduur kasutab tipptasemel kõlari mudelit demoettevõttes USMF, et juhatada teid läbi protsessi.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="0e9e3-106">Lisage protsessitoiming</span><span class="sxs-lookup"><span data-stu-id="0e9e3-106">Add a route operation</span></span>

1. <span data-ttu-id="0e9e3-107">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="0e9e3-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0e9e3-109">Valige selle harjutuse jaoks tipptasemel kõlari mudel.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="0e9e3-110">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="0e9e3-111">Laiendage jaotist **Protsessitoimingud**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="0e9e3-112">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-112">Select **Add**.</span></span>
1. <span data-ttu-id="0e9e3-113">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="0e9e3-114">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="0e9e3-115">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="0e9e3-116">Sisestage protsessitoimingu üksikasjad</span><span class="sxs-lookup"><span data-stu-id="0e9e3-116">Enter route operation details</span></span>

1. <span data-ttu-id="0e9e3-117">Valige **Protsessi operatsiooni üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="0e9e3-118">Sisestage või valige väärtus väljal **Toiming**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="0e9e3-119">Väljal **Toim. nr**</span><span class="sxs-lookup"><span data-stu-id="0e9e3-119">In the **Oper. No.**</span></span> <span data-ttu-id="0e9e3-120">number.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-120">field, enter a number.</span></span>
    * <span data-ttu-id="0e9e3-121">Toimingunumbrid määravad protsessi järjekorra.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="0e9e3-122">Iga protsessitoimingu atribuut võib saada statistilise väärtuse või olla vastendatud atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="0e9e3-123">Atribuudiga vastendamisel määratakse väärtus konfiguratsiooni osaks.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="0e9e3-124">Sisestage või valige väärtus väljal **Protsessigrupp**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0e9e3-125">Protsessigrupp määrab kuluarvutuse, tarbimise ja seadistuse põhikäitumise.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="0e9e3-126">Valige vahekaart **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="0e9e3-127">Valige vahekaart **Ajad**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="0e9e3-128">Sisestage arv väljale **Protsessi kogus**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="0e9e3-129">Määrake, mitu ühe toimingu käigus töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="0e9e3-130">Sisestage number väljale **Tunnid/aeg**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="0e9e3-131">Sisestage aja suhe.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="0e9e3-132">Märkige ruut **Määra**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="0e9e3-133">Sisestage number väljale **Käitusaeg**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="0e9e3-134">Määrake määratud koguse töötlemisaeg.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="0e9e3-135">Valige vahekaart **Ressursinõuded**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="0e9e3-136">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-136">Select **Add**.</span></span>
1. <span data-ttu-id="0e9e3-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0e9e3-138">Valige suvand väljal **Nõude tüüp**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="0e9e3-139">Otsustage, kas soovite määrata konkreetseid ressursse või võimalusi, mis neil peavad olema.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="0e9e3-140">Valige või sisestage väärtus väljal **Nõue**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="0e9e3-141">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]