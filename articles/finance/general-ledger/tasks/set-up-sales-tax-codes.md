---
title: Käibemaksukoodide seadistamine
description: Selles teemas selgitatakse, kuidas seadistada käibemaksukoode rakenduses Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 594e8f0595ecace748a70860c1ccacaf90b7d279
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222187"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="c9950-103">Käibemaksukoodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="c9950-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9950-104">Selles teemas selgitatakse, kuidas seadistada käibemaksukoode.</span><span class="sxs-lookup"><span data-stu-id="c9950-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="c9950-105">Käibemaksukoodid luuakse iga kaudse maksu või kohustuse puhul, mida juriidiline isik on kohustatud arvutama, koguma ja käibemaksuhalduritele maksma.</span><span class="sxs-lookup"><span data-stu-id="c9950-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="c9950-106">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="c9950-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c9950-107">Avage **Navigeerimispaan > Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="c9950-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="c9950-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c9950-108">Select **New**.</span></span>
3. <span data-ttu-id="c9950-109">Sisestage väärtus väljale **Käibemaksukood**.</span><span class="sxs-lookup"><span data-stu-id="c9950-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="c9950-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c9950-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c9950-111">Valige ripploendit avades **Makseperiood**, et määrata, millisele maksumetile ja milliste intervallidega tuleb selle käibemaksu aruanded esitada ja maksud ära maksta.</span><span class="sxs-lookup"><span data-stu-id="c9950-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="c9950-112">Valige **Pearaamatusse kandmise grupp**, et määrata põhikontod käibemaksu pearaamatusse kandmiseks.</span><span class="sxs-lookup"><span data-stu-id="c9950-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="c9950-113">Laiendage kiirkaarti **Arvutused**.</span><span class="sxs-lookup"><span data-stu-id="c9950-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="c9950-114">See sisaldab mitmeid välju, mis juhivad seda, kuidas käibemaksu summasid arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="c9950-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="c9950-115">Täitke need väljad vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c9950-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="c9950-116">Valige liidese ülaosas **Toimingupaanil** valik **Käibemaksukood**.</span><span class="sxs-lookup"><span data-stu-id="c9950-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="c9950-117">Valige **Väärtused**.</span><span class="sxs-lookup"><span data-stu-id="c9950-117">Select **Values**.</span></span>
10. <span data-ttu-id="c9950-118">Sisestage väärtus sellele käibemaksukoodile veerus **väärtus**.</span><span class="sxs-lookup"><span data-stu-id="c9950-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="c9950-119">Kui päritolu välja kiirkaardil **Arvutused** on valitud summa üksuse kohta, korrutatakse väärtust kande kogusega, et arvutada käibemaksu summa.</span><span class="sxs-lookup"><span data-stu-id="c9950-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="c9950-120">Kui maksukood pole ühikupõhine maks, on väärtus protsent, mis rakendatakse selle maksukoodi päritolule käibemaksu summa arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c9950-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="c9950-121">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c9950-121">Select **Save**.</span></span>
12. <span data-ttu-id="c9950-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9950-122">Close the page.</span></span>
13. <span data-ttu-id="c9950-123">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c9950-123">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]