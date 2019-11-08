---
title: Sildiga varude inventuur
description: Selles teemas antakse teavet märgistusega inventuuri kohta, mille abil saate võrrelda lao tegelikku sisu vabade kaubavarudega.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd10c24045fae5db00e88f3b84d4dea7b2c82c37
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571089"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="0d73c-103">Sildiga varude inventuur</span><span class="sxs-lookup"><span data-stu-id="0d73c-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d73c-104">Selles teemas antakse teavet märgistusega inventuuri kohta, mille abil saate võrrelda lao tegelikku sisu vabade kaubavarudega.</span><span class="sxs-lookup"><span data-stu-id="0d73c-104">This topic provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="0d73c-105">Lehel **Märgistusega inventuur** lisatakse igale laokaubale märgistuse number, nt number vahemikus 1–500.</span><span class="sxs-lookup"><span data-stu-id="0d73c-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="0d73c-106">Inventuuri ajal sisestatakse kaubakood ja kogus vastavalt sildile.</span><span class="sxs-lookup"><span data-stu-id="0d73c-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="0d73c-107">Seda silti saab seejärel kasutada märgistusega inventuuri töölehele sisestamise alusena.</span><span class="sxs-lookup"><span data-stu-id="0d73c-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="0d73c-108">Pärast märgistusega inventuuri töölehe sisestamist luuakse lehel **Inventuur** uus inventuuritööleht.</span><span class="sxs-lookup"><span data-stu-id="0d73c-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="0d73c-109">Uus tööleht põhineb loodud märgistusega inventuuri töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="0d73c-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="0d73c-110">Märgistusega inventuuri läbiviimiseks kaupade puhul konkreetse laodimensiooni põhjal valige dimensioon lehel **Dimensiooni kuvamine**, mis kuvatakse, kui märgistusega inventuuri töölehe loote.</span><span class="sxs-lookup"><span data-stu-id="0d73c-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="0d73c-111">Näiteks kindlas laos olevate kaupade loendamiseks märkige ruut **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="0d73c-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="0d73c-112">Kui valida liugur **Lukusta kaubad inventuuri ajaks** lehel **Varude ja laohalduse parameetrid**, ei saa kaupu inventuuri ajal füüsiliselt muuta.</span><span class="sxs-lookup"><span data-stu-id="0d73c-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="0d73c-113">Kuid märgistusega inventuuri töölehtedel olevad kaubad pole inventuuri ajal lukus.</span><span class="sxs-lookup"><span data-stu-id="0d73c-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="0d73c-114">Laokandeid ei looda enne, kui sildiga inventuuri read sisestatakse ja inventuuritöölehele kantakse.</span><span class="sxs-lookup"><span data-stu-id="0d73c-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="0d73c-115">Kui sildid sisestatakse juhuslikult ja soovite tuvastada puuduvaid silte, klõpsake ridade sildi järgi sortimiseks veeru **Silt** päist.</span><span class="sxs-lookup"><span data-stu-id="0d73c-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d73c-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0d73c-116">Additional resources</span></span>

[<span data-ttu-id="0d73c-117">Tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="0d73c-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
