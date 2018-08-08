--- 
title: "Põhivara ülekandmine"
description: "See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ea0e54dad6d8a48d628fc831b3fdbe7c0f68e892
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="0b4ab-103">Põhivara ülekandmine</span><span class="sxs-lookup"><span data-stu-id="0b4ab-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b4ab-104">See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="0b4ab-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="0b4ab-106">Minge jaotisse Põhivarad > Põhivarad > Põhivarad.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="0b4ab-107">Leidke ja valige loendist vara, mida soovite soetada.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="0b4ab-108">Klõpsake toimingupaanil suvandit Põhivara.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="0b4ab-109">Klõpsake suvandit Põhivara ülekandmine.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="0b4ab-110">Sisestage kuupäev väljale Ülekandmise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="0b4ab-111">Sisestage ülekandmise kirjeldamiseks kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="0b4ab-112">Selles loendis kuvatakse kõik põhivara raamatud.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="0b4ab-113">Märkige raamatud, mille soovite uude finantsdimensiooni kogumisse üle kanda.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="0b4ab-114">Loend kuvab valitud raamatu puhul olemasolevad finantsdimensiooni väärtused.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="0b4ab-115">Valige finantsdimensioon, mida soovite valitud põhivara raamatu puhul värskendada.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="0b4ab-116">Klõpsake väljal Finantsdimensioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="0b4ab-117">Vajaduse korral määrake muid finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="0b4ab-118">Kõik finantsdimensiooni väärtused muutuvad ülekande ilmnemisel, olenemata sellest, kas väärtus on sisestatud või tühjaks jäetud.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="0b4ab-119">Näiteks kui sisestasite väärtuse suvandi BusinessUnit puhul ja jätsite suvandite CostCenter ja Osakond finantsdimensioonid tühjaks.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="0b4ab-120">Kui teie konto struktuur lubab jätta parameetrite CostCenter ja Osakond väärtused tühjaks, on ülekandmise tulemusena igas väärtusmudelis parameetril BusinessUnit uus väärtus ja parameetrite CostCenter ja Osakond väärtus tühi.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="0b4ab-121">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-121">Click Update.</span></span>
    * <span data-ttu-id="0b4ab-122">Teil on võimalus muudatusi enne ülekande lõpetamist vaadata.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="0b4ab-123">Enne põhivara raamatu ülekandmist vaadake tulemusi.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="0b4ab-124">Klõpsake käsku Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="0b4ab-124">Click Transfer.</span></span>


