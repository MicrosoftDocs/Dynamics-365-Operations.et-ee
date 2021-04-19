---
title: Kauba transpordipiirangute seadistamine
description: Selle protseduuri saab seadistada transpordipiirangu, et vältida valitud kauba transportimist valitud keskuse kaudu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8488ec154412840bf88779eeffc3d4ff52aabd22
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818988"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="82465-103">Kauba transpordipiirangute seadistamine</span><span class="sxs-lookup"><span data-stu-id="82465-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82465-104">Selle protseduuri saab seadistada transpordipiirangu, et vältida valitud kauba transportimist valitud keskuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="82465-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="82465-105">Seda ülesannet täidab tavaliselt transpordi koordinaator.</span><span class="sxs-lookup"><span data-stu-id="82465-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="82465-106">Saate seda protseduuri kasutada demoettevõttes USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="82465-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="82465-107">Kauba piirangu loomine</span><span class="sxs-lookup"><span data-stu-id="82465-107">Create an item constaint</span></span>
1. <span data-ttu-id="82465-108">Minge asukohta Piirangud.</span><span class="sxs-lookup"><span data-stu-id="82465-108">Go to Constraints.</span></span>
2. <span data-ttu-id="82465-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="82465-109">Click New.</span></span>
3. <span data-ttu-id="82465-110">Tippige väärtus väljale Kauba piirang.</span><span class="sxs-lookup"><span data-stu-id="82465-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="82465-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="82465-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="82465-112">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="82465-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="82465-113">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="82465-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="82465-114">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="82465-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="82465-115">Sisestage või valige väärtus väljal Keskus.</span><span class="sxs-lookup"><span data-stu-id="82465-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="82465-116">Valige suvand väljal Piirangu tegevus.</span><span class="sxs-lookup"><span data-stu-id="82465-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="82465-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="82465-117">Click Save.</span></span>
11. <span data-ttu-id="82465-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="82465-118">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]