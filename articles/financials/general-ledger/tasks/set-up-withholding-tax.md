---
title: Kinnipeetava maksu seadistamine
description: Kinnipeetav maks on maks hankijatele, mis ei loo käibemaksukandeid.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337229"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="e5998-103">Kinnipeetava maksu seadistamine</span><span class="sxs-lookup"><span data-stu-id="e5998-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5998-104">Kinnipeetav maks on maks hankijatele, mis ei loo käibemaksukandeid.</span><span class="sxs-lookup"><span data-stu-id="e5998-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="e5998-105">Hankija maksetelt arvutatav kinnipeetav maks on kohustus.</span><span class="sxs-lookup"><span data-stu-id="e5998-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="e5998-106">Seetõttu on kinnipeetava maksu sisestamisel kehtivad kontod ainult bilansikontod või kohustuste kontod.</span><span class="sxs-lookup"><span data-stu-id="e5998-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="e5998-107">See ülesande juhend näitab, kuidas kinnipeetavat maksu seadistada.</span><span class="sxs-lookup"><span data-stu-id="e5998-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="e5998-108">Avage Maks > Kaudsed maksud > Kinnipeetav maks > Kinnipeetava maksu koodid.</span><span class="sxs-lookup"><span data-stu-id="e5998-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="e5998-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e5998-109">Click New.</span></span>
3. <span data-ttu-id="e5998-110">Sisestage väärtus väljale Kinnipeetava maksu kood.</span><span class="sxs-lookup"><span data-stu-id="e5998-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="e5998-111">Sisestage kinnipeetava maksu koodi nimi väljale Kinnipeetava maksu nimi.</span><span class="sxs-lookup"><span data-stu-id="e5998-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="e5998-112">Valige väljal Põhikonto kinnipeetava maksu kohustuse sisestamiseks kasutatav põhikonto.</span><span class="sxs-lookup"><span data-stu-id="e5998-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="e5998-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e5998-113">Click Save.</span></span>
7. <span data-ttu-id="e5998-114">Klõpsake suvandit Väärtused.</span><span class="sxs-lookup"><span data-stu-id="e5998-114">Click Values.</span></span>
8. <span data-ttu-id="e5998-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e5998-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e5998-116">Sisestage väljale Väärtus kinnipeetava maksu arvutamiseks kasutatav protsent.</span><span class="sxs-lookup"><span data-stu-id="e5998-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="e5998-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e5998-117">Click Save.</span></span>
11. <span data-ttu-id="e5998-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e5998-118">Close the page.</span></span>
12. <span data-ttu-id="e5998-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e5998-119">Click Save.</span></span>
13. <span data-ttu-id="e5998-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e5998-120">Close the page.</span></span>
14. <span data-ttu-id="e5998-121">Avage Maks > Kaudsed maksud > Kinnipeetav maks > Kinnipeetava maksu grupid.</span><span class="sxs-lookup"><span data-stu-id="e5998-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="e5998-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e5998-122">Click New.</span></span>
16. <span data-ttu-id="e5998-123">Sisestage kinnipeetava maksu grupi identifikaator väljale Kinnipeetava maksu grupp.</span><span class="sxs-lookup"><span data-stu-id="e5998-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="e5998-124">Sisestage kinnipeetava maksu grupi nimi väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e5998-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="e5998-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e5998-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="e5998-126">Valige kinnipeetava maksu kood väljalt Kinnipeetava maksu kood.</span><span class="sxs-lookup"><span data-stu-id="e5998-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="e5998-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5998-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="e5998-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e5998-128">Click Save.</span></span>

