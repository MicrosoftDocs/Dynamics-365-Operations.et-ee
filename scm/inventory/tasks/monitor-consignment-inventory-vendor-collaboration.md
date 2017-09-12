---
title: "Veose varude jälgimine hankija koostöö abil"
description: "See protseduur näitab, kuidas kasutada hankija koostööd teabe nägemiseks toote varude taseme kohta, mille olete kliendi juures olevasse saadetisse paigutanud."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 567be29bd9989b3471b22d5a970ed0e51e4549ec
ms.contentlocale: et-ee
ms.lasthandoff: 09/12/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="d6754-103">Veose varude jälgimine hankija koostöö abil</span><span class="sxs-lookup"><span data-stu-id="d6754-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6754-104">See protseduur näitab, kuidas kasutada hankija koostööd teabe nägemiseks toote varude taseme kohta, mille olete kliendi juures olevasse saadetisse paigutanud.</span><span class="sxs-lookup"><span data-stu-id="d6754-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="d6754-105">Saate jälgida ka varude tarbimist, kui klient varude omandiõiguse üle võtab.</span><span class="sxs-lookup"><span data-stu-id="d6754-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="d6754-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="d6754-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="d6754-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="d6754-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="d6754-108">Tarbitud varude kuvamine</span><span class="sxs-lookup"><span data-stu-id="d6754-108">View consumed inventory</span></span>
1. <span data-ttu-id="d6754-109">Avage Hankija koostöö > Veose varud > Veose varudest saadud tooted.</span><span class="sxs-lookup"><span data-stu-id="d6754-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="d6754-110">Loendis on näha toote sissetuleku read, mis loodi, kui saadetise varude omandiõigus hankijalt kliendile üle läks.</span><span class="sxs-lookup"><span data-stu-id="d6754-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="d6754-111">Koguste ja muu teabe vaatamiseks võib olla vaja paremale kerida.</span><span class="sxs-lookup"><span data-stu-id="d6754-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="d6754-112">Selles loendis olevat teavet saab kasutada kliendile arvete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="d6754-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="d6754-113">Andmeid saab ka Microsoft Excelisse eksportida.</span><span class="sxs-lookup"><span data-stu-id="d6754-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="d6754-114">Klõpsake valikut Kuva ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="d6754-114">Click View purchase order.</span></span>
3. <span data-ttu-id="d6754-115">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d6754-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="d6754-116">Rida on märgitud kui Saadetis ja päise jaotis näitab, et ostutellimuse olek on Vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="d6754-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="d6754-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6754-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="d6754-118">Vabade kaubavarude vaatamine</span><span class="sxs-lookup"><span data-stu-id="d6754-118">View on-hand inventory</span></span>
1. <span data-ttu-id="d6754-119">Avage Hankija koostöö > Veose varud > Veose vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="d6754-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="d6754-120">Veose vaba kaubavaru lehel on näidatud teile kuuluvad varud kliendi laos.</span><span class="sxs-lookup"><span data-stu-id="d6754-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="d6754-121">Saate kuvada lisadimensioone nagu tegevuskoht ja ladu, klõpsates vahekaarti Kuva dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="d6754-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

