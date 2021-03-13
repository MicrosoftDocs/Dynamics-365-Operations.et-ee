---
title: Veose varude jälgimine hankija koostöö abil
description: See protseduur näitab, kuidas kasutada hankija koostööd teabe nägemiseks toote varude taseme kohta, mille olete kliendi juures olevasse saadetisse paigutanud.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2e782bed4cd9f2f13e2ee45afffaef277279131
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020125"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="2cd04-103">Veose varude jälgimine hankija koostöö abil</span><span class="sxs-lookup"><span data-stu-id="2cd04-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2cd04-104">See protseduur näitab, kuidas kasutada hankija koostööd teabe nägemiseks toote varude taseme kohta, mille olete kliendi juures olevasse saadetisse paigutanud.</span><span class="sxs-lookup"><span data-stu-id="2cd04-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="2cd04-105">Saate jälgida ka varude tarbimist, kui klient varude omandiõiguse üle võtab.</span><span class="sxs-lookup"><span data-stu-id="2cd04-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="2cd04-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="2cd04-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="2cd04-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="2cd04-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="2cd04-108">Tarbitud varude kuvamine</span><span class="sxs-lookup"><span data-stu-id="2cd04-108">View consumed inventory</span></span>
1. <span data-ttu-id="2cd04-109">Avage Hankija koostöö > Veose varud > Veose varudest saadud tooted.</span><span class="sxs-lookup"><span data-stu-id="2cd04-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="2cd04-110">Loendis on näha toote sissetuleku read, mis loodi, kui saadetise varude omandiõigus hankijalt kliendile üle läks.</span><span class="sxs-lookup"><span data-stu-id="2cd04-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="2cd04-111">Koguste ja muu teabe vaatamiseks võib olla vaja paremale kerida.</span><span class="sxs-lookup"><span data-stu-id="2cd04-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="2cd04-112">Selles loendis olevat teavet saab kasutada kliendile arvete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="2cd04-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="2cd04-113">Andmeid saab ka Microsoft Excelisse eksportida.</span><span class="sxs-lookup"><span data-stu-id="2cd04-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="2cd04-114">Klõpsake valikut Kuva ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="2cd04-114">Click View purchase order.</span></span>
3. <span data-ttu-id="2cd04-115">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="2cd04-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="2cd04-116">Rida on märgitud kui Saadetis ja päise jaotis näitab, et ostutellimuse olek on Vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="2cd04-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="2cd04-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2cd04-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="2cd04-118">Vabade kaubavarude vaatamine</span><span class="sxs-lookup"><span data-stu-id="2cd04-118">View on-hand inventory</span></span>
1. <span data-ttu-id="2cd04-119">Avage Hankija koostöö > Veose varud > Veose vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="2cd04-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="2cd04-120">Veose vaba kaubavaru lehel on näidatud teile kuuluvad varud kliendi laos.</span><span class="sxs-lookup"><span data-stu-id="2cd04-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="2cd04-121">Saate kuvada lisadimensioone nagu tegevuskoht ja ladu, klõpsates vahekaarti Kuva dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="2cd04-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

