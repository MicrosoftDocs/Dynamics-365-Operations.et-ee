---
title: Toote elutsükli oleku loomine toodete välistamiseks koondplaneerimisest
description: See protseduur kirjeldab, kuidas luua uut toote elutsükli olekut, mis välistab tooted koondplaneerimisest ja koosluse taseme arvutusest.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818033"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="c6e1e-103">Toote elutsükli oleku loomine toodete välistamiseks koondplaneerimisest</span><span class="sxs-lookup"><span data-stu-id="c6e1e-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6e1e-104">See protseduur kirjeldab, kuidas luua uut toote elutsükli olekut, mis välistab tooted koondplaneerimisest ja koosluse taseme arvutusest.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="c6e1e-105">Aegunud oleku loomine</span><span class="sxs-lookup"><span data-stu-id="c6e1e-105">Create an obsolete state</span></span>
1. <span data-ttu-id="c6e1e-106">Avage Tooteteabe haldus > Häälestus > Toote elutsükli olek.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="c6e1e-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-107">Click New.</span></span>
3. <span data-ttu-id="c6e1e-108">Tippige väärtus väljale Olek.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="c6e1e-109">Valige Ei väljal On planeerimiseks aktiivne.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="c6e1e-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="c6e1e-111">Aegunud oleku seostamine väljastatud tootega</span><span class="sxs-lookup"><span data-stu-id="c6e1e-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="c6e1e-112">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-112">Close the page.</span></span>
2. <span data-ttu-id="c6e1e-113">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="c6e1e-114">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c6e1e-115">Näiteks filtreerige välja Otsingunimi väärtusega „M00”.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="c6e1e-116">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-116">Click Edit.</span></span>
5. <span data-ttu-id="c6e1e-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c6e1e-118">Väljal Toote elutsükli olek sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-118">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]