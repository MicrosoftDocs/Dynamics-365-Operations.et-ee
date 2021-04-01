---
title: Lisakulumi seadistamine
description: See protseduur kirjeldab kulumi erihüvitise loomist ja selle seostamist põhivararaamatuga.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6627e7fa9a1eb1a9131ec7e2c3cc823b49b286cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257557"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="2f83b-103">Lisakulumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="2f83b-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f83b-104">See protseduur kirjeldab kulumi erihüvitise loomist ja selle seostamist põhivararaamatuga.</span><span class="sxs-lookup"><span data-stu-id="2f83b-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="2f83b-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="2f83b-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="2f83b-106">Kulumi erihüvitise loomine</span><span class="sxs-lookup"><span data-stu-id="2f83b-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="2f83b-107">Avage Põhivarad > Seadistus > Kulumi erihüvitis.</span><span class="sxs-lookup"><span data-stu-id="2f83b-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="2f83b-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2f83b-108">Click New.</span></span>
3. <span data-ttu-id="2f83b-109">Sisestage väärtus väljale Kulumi erihüvitis.</span><span class="sxs-lookup"><span data-stu-id="2f83b-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="2f83b-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="2f83b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2f83b-111">Sisestage number väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="2f83b-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="2f83b-112">Kui protsenti ei näidatud, määrake summa.</span><span class="sxs-lookup"><span data-stu-id="2f83b-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="2f83b-113">Kulumi erihüvitise seostamine põhivaragrupi raamatuga</span><span class="sxs-lookup"><span data-stu-id="2f83b-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="2f83b-114">Avage Põhivarad > Seadistus > Põhivaragrupid.</span><span class="sxs-lookup"><span data-stu-id="2f83b-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="2f83b-115">Valige loendist kulumi erihüvitisega seostatud põhivaragrupp.</span><span class="sxs-lookup"><span data-stu-id="2f83b-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="2f83b-116">Klõpsake valikut Raamatud.</span><span class="sxs-lookup"><span data-stu-id="2f83b-116">Click Books.</span></span>
4. <span data-ttu-id="2f83b-117">Valige loendist kulumi erihüvitisega seostatud raamat.</span><span class="sxs-lookup"><span data-stu-id="2f83b-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="2f83b-118">Klõpsake suvandit Kulumi erihüvitis.</span><span class="sxs-lookup"><span data-stu-id="2f83b-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="2f83b-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2f83b-119">Click New.</span></span>
7. <span data-ttu-id="2f83b-120">Sisestage või valige väärtus väljal Kulumi erihüvitis.</span><span class="sxs-lookup"><span data-stu-id="2f83b-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="2f83b-121">Protsendi või Summa vaikeväärtus tuleb kulumi erihüvitise seadistusest.</span><span class="sxs-lookup"><span data-stu-id="2f83b-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="2f83b-122">Sisestage arv väljale Prioriteet.</span><span class="sxs-lookup"><span data-stu-id="2f83b-122">In the Priority field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]