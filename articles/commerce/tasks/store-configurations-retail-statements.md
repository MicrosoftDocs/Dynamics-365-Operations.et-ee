---
title: " Jaemüügi väljavõtete kauplusekonfiguratsioonid"
description: See protseduur selgitab kaupluse konfiguratsioone, mis mõjutavad Commerce’i väljavõtete loomise ja sisestamise viisi.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b73282abd2df92b3f466f7c1c6c210173001fd7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022237"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="0195a-103"> Jaemüügi väljavõtete kauplusekonfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="0195a-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0195a-104">See protseduur selgitab kaupluse konfiguratsioone, mis mõjutavad Commerce’i väljavõtete loomise ja sisestamise viisi.</span><span class="sxs-lookup"><span data-stu-id="0195a-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="0195a-105">Kaupluste finantsdimensioone käsitletakse teises protseduuris.</span><span class="sxs-lookup"><span data-stu-id="0195a-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="0195a-106">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="0195a-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="0195a-107">Avage **Navigatsioonipaneelil** suvand **Moodulid > Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="0195a-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="0195a-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0195a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0195a-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0195a-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0195a-110">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0195a-110">Click **Edit**.</span></span>
5. <span data-ttu-id="0195a-111">Kiirkaardi **Väljavõte/sulgemine** seadistused mõjutavad väljavõtte loomist, kinnitamist ja sisestamist kaupluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="0195a-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="0195a-112">Laiendage kiirkaarti **Väljavõte/sulgemise**.</span><span class="sxs-lookup"><span data-stu-id="0195a-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="0195a-113">Valige väljas **Väljavõttemeetod** meetod, mille järgi soovite väljavõtte ridu grupeerida.</span><span class="sxs-lookup"><span data-stu-id="0195a-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="0195a-114">Valige suvand Jah väljas **Üks väljavõte päevas**, kui väljavõtte loomise pakett-tööst väljavõtete loomisel tuleb päevas luua vaid üks väljavõte.</span><span class="sxs-lookup"><span data-stu-id="0195a-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="0195a-115">Väli **Päevakassa arvutamine** määratleb, kas päevakassad tuleb kokku liita või kasutada viimast.</span><span class="sxs-lookup"><span data-stu-id="0195a-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="0195a-116">Valige väljas **Ümardamine** pearaamatukonto, millesse ümardamiserinevused sisestada.</span><span class="sxs-lookup"><span data-stu-id="0195a-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="0195a-117">Väljal **Maksimaalse ümardamiserinevus** saate sisestada maksimaalse lubatud ümardamiserinevuse.</span><span class="sxs-lookup"><span data-stu-id="0195a-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="0195a-118">Väljale **Sisestamine** saate sisestada väljavõtte puhul lubatud maksimaalse sisestamise koguerinevuse.</span><span class="sxs-lookup"><span data-stu-id="0195a-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="0195a-119">Väljale **Vahetus** saate sisestada väljavõtte maksimaalse vahetuse koguerinevuse.</span><span class="sxs-lookup"><span data-stu-id="0195a-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="0195a-120">Väljale **Kanne** saate sisestada väljavõtterea maksimaalse koguerinevuse.</span><span class="sxs-lookup"><span data-stu-id="0195a-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="0195a-121">Väljal **Sulgemismeetod** saate määratleda, kas väljavõttesse kaasatavad kanded peaksid olema osa suletud vahetusest või võivad need olla mis tahes kanded määratletud kuupäeva-/kellaajavahemikus.</span><span class="sxs-lookup"><span data-stu-id="0195a-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="0195a-122">Väljale **Tööpäeva lõpp** saate sisestada kellaaja, kui pärast keskööd toimuvad kanded tuleb sisestada koos eelmise päevaga.</span><span class="sxs-lookup"><span data-stu-id="0195a-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="0195a-123">Valige suvand Jah väljal **Sisesta tööpäevana**, kui pärast keskööd toimuvad kanded tuleb sisestada eelmise päeva osana.</span><span class="sxs-lookup"><span data-stu-id="0195a-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="0195a-124">Valige suvand Jah väljal **Poolitatud väjavõttemeetodi järgi**, kui soovite määratleda iga väljavõttemeetodi jaoks loodavaid väljavõtteid.</span><span class="sxs-lookup"><span data-stu-id="0195a-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="0195a-125">Sellest on abi, kui sisestusjõudlust tuleb suurte kandemahtudega kaupluste puhul suurendada, kuna see loob palju väiksemaid väljavõtteid, mida saab korraga töödelda.</span><span class="sxs-lookup"><span data-stu-id="0195a-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="0195a-126">Väljal **Vaikeklient** saate kiirkaardil **Üldine** valida kliendikonto, mida kasutada kohale tulevatele klientidele müümisel.</span><span class="sxs-lookup"><span data-stu-id="0195a-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

