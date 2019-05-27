---
title: Kauba transpordipiirangute seadistamine
description: Selle protseduuri saab seadistada transpordipiirangu, et vältida valitud kauba transportimist valitud keskuse kaudu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 900ea1476c95d295a151125afe46aebd9642630e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550441"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="dffc4-103">Kauba transpordipiirangute seadistamine</span><span class="sxs-lookup"><span data-stu-id="dffc4-103">Set up transportation constraints for an item</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dffc4-104">Selle protseduuri saab seadistada transpordipiirangu, et vältida valitud kauba transportimist valitud keskuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="dffc4-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="dffc4-105">Seda ülesannet täidab tavaliselt transpordi koordinaator.</span><span class="sxs-lookup"><span data-stu-id="dffc4-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="dffc4-106">Saate seda protseduuri kasutada demoettevõttes USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="dffc4-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="dffc4-107">Kauba piirangu loomine</span><span class="sxs-lookup"><span data-stu-id="dffc4-107">Create an item constaint</span></span>
1. <span data-ttu-id="dffc4-108">Minge asukohta Piirangud.</span><span class="sxs-lookup"><span data-stu-id="dffc4-108">Go to Constraints.</span></span>
2. <span data-ttu-id="dffc4-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dffc4-109">Click New.</span></span>
3. <span data-ttu-id="dffc4-110">Tippige väärtus väljale Kauba piirang.</span><span class="sxs-lookup"><span data-stu-id="dffc4-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="dffc4-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="dffc4-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dffc4-112">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="dffc4-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="dffc4-113">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="dffc4-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="dffc4-114">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="dffc4-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="dffc4-115">Sisestage või valige väärtus väljal Keskus.</span><span class="sxs-lookup"><span data-stu-id="dffc4-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="dffc4-116">Valige suvand väljal Piirangu tegevus.</span><span class="sxs-lookup"><span data-stu-id="dffc4-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="dffc4-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dffc4-117">Click Save.</span></span>
11. <span data-ttu-id="dffc4-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dffc4-118">Close the page.</span></span>

