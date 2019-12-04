---
title: Põhivara ülekandmine
description: See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186827"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="fc1f2-103">Põhivara ülekandmine</span><span class="sxs-lookup"><span data-stu-id="fc1f2-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc1f2-104">See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="fc1f2-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="fc1f2-106">Avage navigeerimispaanil **Moodulid > Põhivara > Põhivara > Põhivara**.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="fc1f2-107">Leidke ja valige loendist vara, mida soovite soetada.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="fc1f2-108">Klõpsake toimingupaanil **Põhivara**.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="fc1f2-109">Klõpsake **Põhivara edastamine**.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="fc1f2-110">Sisestage kuupäev väljale **Edastuse kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="fc1f2-111">Sisestage ülekandmise kirjeldamiseks kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="fc1f2-112">Selles loendis kuvatakse kõik põhivara raamatud.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="fc1f2-113">Märkige raamatud, mille soovite uude finantsdimensiooni kogumisse üle kanda.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="fc1f2-114">Loend kuvab valitud raamatu puhul olemasolevad finantsdimensiooni väärtused.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="fc1f2-115">Valige finantsdimensioon, mida soovite valitud põhivara raamatu puhul värskendada.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="fc1f2-116">Klõpsake väljal **Finantsdimensioon** ripplonedi nuppu otsingu avamiseks.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="fc1f2-117">Vajaduse korral määrake muid finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="fc1f2-118">Kõik finantsdimensiooni väärtused muutuvad ülekande ilmnemisel, olenemata sellest, kas väärtus on sisestatud või tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="fc1f2-119">Näiteks kui sisestasite väärtuse suvandi BusinessUnit puhul ja jätsite suvandite CostCenter ja Osakond finantsdimensioonid tühjaks.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="fc1f2-120">Kui teie konto struktuur lubab jätta parameetrite CostCenter ja Osakond väärtused tühjaks, on ülekandmise tulemusena igas väärtusmudelis parameetril BusinessUnit uus väärtus ja parameetrite CostCenter ja Osakond väärtus tühi.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="fc1f2-121">Klõpsake **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-121">Click **Update**.</span></span>
    * <span data-ttu-id="fc1f2-122">Teil on võimalus muudatusi enne ülekande lõpetamist vaadata.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="fc1f2-123">Enne põhivara raamatu ülekandmist vaadake tulemusi.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="fc1f2-124">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="fc1f2-124">Click **Transfer**.</span></span>
