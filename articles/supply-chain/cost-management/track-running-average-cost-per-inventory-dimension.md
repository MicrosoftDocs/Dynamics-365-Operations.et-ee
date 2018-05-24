---
title: "Jooksvate keskmiste kulude jälgimine varude dimensiooni alusel"
description: "Igale laokaubale on lisatud varude dimensioonigrupp. Seetõttu arvutatakse kauba jooksev keskmine omahind finantsiliselt jälgitavate varude dimensioonide valiku põhjal."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 48db7ff047a50343bd473d2c71f878e4ee2201e5
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="b3e6b-104">Jooksvate keskmiste kulude jälgimine varude dimensiooni alusel</span><span class="sxs-lookup"><span data-stu-id="b3e6b-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="b3e6b-105">Igale laokaubale on lisatud varude dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="b3e6b-106">Seetõttu arvutatakse kauba jooksev keskmine omahind finantsiliselt jälgitavate varude dimensioonide valiku põhjal.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="b3e6b-107">Varude dimensioone on kolm tüüpi: toote-, laoala ja jälgimisdimensioon.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="b3e6b-108">Tootedimensioonid hõlmavad konfiguratsiooni, suurust ja värvi.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="b3e6b-109">Tootedimensioone jälgitakse alati finantsiliselt.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="b3e6b-110">Laoala ja jälgimisdimensioonid hõlmavad tegevuskohta, ladu, asukohta, varude olekut, litsentsiplaati, partii numbrit ja seerianumbrit.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="b3e6b-111">Saate määrata, milliseid laoala ja jälgimisdimensioone finantsiliselt jälgitakse.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="b3e6b-112">**1. näide**</span><span class="sxs-lookup"><span data-stu-id="b3e6b-112">**Example 1**</span></span> 

<span data-ttu-id="b3e6b-113">Kui kaubaga seotud laoala dimensioonigruppi jälgitakse finantsiliselt lao järgi, arvutatakse jooksev keskmine omahind iga lao kohta.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="b3e6b-114">Arveldatud on järgmised ostutellimused:</span><span class="sxs-lookup"><span data-stu-id="b3e6b-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="b3e6b-115">Ostutellimus kogusele 2 omahinnaga 10,00 USA dollarit on arveldatud laole GW.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="b3e6b-116">Ostutellimus kogusele 3 omahinnaga 12,00 USA dollarit on arveldatud laole GW.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="b3e6b-117">Ostutellimus kogusele 5 omahinnaga 15,00 USA dollarit on arveldatud laole MW.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="b3e6b-118">Jooksev keskmine omahind lao GW puhul on 11,20 USA dollarit ja jooksev keskmine omahind lao MW puhul on 15,00 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="b3e6b-119">Müügitellimuse arve sisestatakse laole GW.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="b3e6b-120">Varude väärtus ja tuletusreegel (enne lao sulgemise käitamist ja ilma märgistuseta) on 11,20 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="b3e6b-121">Teine müügitellimus sisestatakse laole MW.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="b3e6b-122">Varude väärtus ja tuletusreegel (enne lao sulgemise käitamist ja ilma märgistuseta) on 15,00 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="b3e6b-123">**2. näide.** Kui kaubaga seotud laoala dimensioonigruppi jälgitakse finantsiliselt lao järgi ja jälgimisdimensioonigruppi jälgitakse finantsiliselt partiinumbri järgi, arvutatakse jooksev keskmine omahind iga partii kohta.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="b3e6b-124">**Märkus.** Soovitame alati vaadata kõigi jälgitavate finantsdimensioonide omahinda.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="b3e6b-125">Arveldatud on järgmised ostutellimused:</span><span class="sxs-lookup"><span data-stu-id="b3e6b-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="b3e6b-126">Ostutellimus kogusele 2 omahinnaga 10,00 USA dollarit on arveldatud laole GW ja partiile AAA.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="b3e6b-127">Ostutellimus kogusele 3 omahinnaga 12,00 USA dollarit on arveldatud laole GW ja partiile AAA.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="b3e6b-128">Ostutellimus kogusele 2 omahinnaga 15,00 USA dollarit on arveldatud laole GW ja partiile BBB.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="b3e6b-129">Jooksev keskmine omahind lao GW ja partii AAA puhul on 11,20 USA dollarit ning jooksev keskmine omahind lao MW ja partii BBB puhul on 15,00 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="b3e6b-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




