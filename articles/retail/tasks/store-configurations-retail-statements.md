--- 
title: " Jaemüügi väljavõtete kauplusekonfiguratsioonid"
description: "See protseduur selgitab jaekaupluse konfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cac676c9c6ebb6769fe7e30ac08a2c8334befc24
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="2581e-103"> Jaemüügi väljavõtete kauplusekonfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="2581e-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2581e-104">See protseduur selgitab jaekaupluse konfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi.</span><span class="sxs-lookup"><span data-stu-id="2581e-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="2581e-105">Jaekaupluste finantsdimensioone käsitletakse teises protseduuris.</span><span class="sxs-lookup"><span data-stu-id="2581e-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="2581e-106">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2581e-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="2581e-107">Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.</span><span class="sxs-lookup"><span data-stu-id="2581e-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="2581e-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2581e-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2581e-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2581e-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2581e-110">Jaotise Väljavõte/sulgemine sätted mõjutavad väljavõtte loomist, kinnitamist ja sisestamist kaupluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="2581e-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="2581e-111">Avage jaotis Väljavõte/sulgemine.</span><span class="sxs-lookup"><span data-stu-id="2581e-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="2581e-112">Valige meetod, mille järgi soovite väljavõtte ridu grupeerida.</span><span class="sxs-lookup"><span data-stu-id="2581e-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="2581e-113">Valige suvand Jah, kui väljavõtte loomise pakett-tööst väljavõtete loomisel tuleb päevas luua vaid üks väljavõte.</span><span class="sxs-lookup"><span data-stu-id="2581e-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="2581e-114">Väli Päevakassa arvutamine määratleb, kas päevakassad tuleb kokku liita või kasutada viimast.</span><span class="sxs-lookup"><span data-stu-id="2581e-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="2581e-115">Valige pearaamatukonto, millesse ümardamiserinevused sisestada.</span><span class="sxs-lookup"><span data-stu-id="2581e-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="2581e-116">Väljal Maksimaalsne ümardamiserinevus saate sisestada maksimaalse lubatud ümardamiserinevuse.</span><span class="sxs-lookup"><span data-stu-id="2581e-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="2581e-117">Väljale Sisestamine saate sisestada väljavõtte puhul lubatud maksimaalne sisestamise koguerinevuse.</span><span class="sxs-lookup"><span data-stu-id="2581e-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="2581e-118">Väljale Vahetus saate sisestada väljavõtte maksimaalne vahetuse koguerinevuse.</span><span class="sxs-lookup"><span data-stu-id="2581e-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="2581e-119">Väljale Kanne saate sisestada väljavõtterea maksimaalne koguerinevuse.</span><span class="sxs-lookup"><span data-stu-id="2581e-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="2581e-120">Väljal Sulgemismeetod saate määratleda, kas väljavõttesse kaasatavad kanded peaksid olema osa suletud vahetusest või võivad need olla mis tahes kanded määratletud kuupäeva-/kellaajavahemikus.</span><span class="sxs-lookup"><span data-stu-id="2581e-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="2581e-121">Väljale Tööpäeva lõpp saate sisestada kellaaja, kui pärast keskööd toimuvad kanded tuleb sisestada koos eelmise päevaga.</span><span class="sxs-lookup"><span data-stu-id="2581e-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="2581e-122">Valige suvand Jah, kui pärast keskööd toimuvad kanded tuleb sisestada eelmise päeva osana.</span><span class="sxs-lookup"><span data-stu-id="2581e-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="2581e-123">Valige suvand Jah, kui soovite määratleda iga väljavõttemeetodi jaoks loodavaid väljavõtteid.</span><span class="sxs-lookup"><span data-stu-id="2581e-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="2581e-124">Sellest on abi, kui sisestusjõudlust tuleb suurte kandemahtudega kaupluste puhul suurendada, kuna see loob palju väiksemaid väljavõtteid, mida saab korraga töödelda.</span><span class="sxs-lookup"><span data-stu-id="2581e-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="2581e-125">Väljal Vaikeklient saate valida kliendikonto, mida kasutada kohale tulevatele klientidele müümisel.</span><span class="sxs-lookup"><span data-stu-id="2581e-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


