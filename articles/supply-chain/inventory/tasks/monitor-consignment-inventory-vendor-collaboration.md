---
title: Veose varude jälgimine hankija koostöö abil
description: See protseduur näitab, kuidas kasutada hankija koostööd teabe nägemiseks toote varude taseme kohta, mille olete kliendi juures olevasse saadetisse paigutanud.
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e397c12b9f605d1c864ce053477090ed8c1700
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839267"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="f2cb4-103">Veose varude jälgimine hankija koostöö abil</span><span class="sxs-lookup"><span data-stu-id="f2cb4-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2cb4-104">See protseduur näitab, kuidas kasutada hankija koostööd teabe nägemiseks toote varude taseme kohta, mille olete kliendi juures olevasse saadetisse paigutanud.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="f2cb4-105">Saate jälgida ka varude tarbimist, kui klient varude omandiõiguse üle võtab.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="f2cb4-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="f2cb4-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="f2cb4-108">Tarbitud varude kuvamine</span><span class="sxs-lookup"><span data-stu-id="f2cb4-108">View consumed inventory</span></span>
1. <span data-ttu-id="f2cb4-109">Avage Hankija koostöö > Veose varud > Veose varudest saadud tooted.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="f2cb4-110">Loendis on näha toote sissetuleku read, mis loodi, kui saadetise varude omandiõigus hankijalt kliendile üle läks.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="f2cb4-111">Koguste ja muu teabe vaatamiseks võib olla vaja paremale kerida.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="f2cb4-112">Selles loendis olevat teavet saab kasutada kliendile arvete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="f2cb4-113">Andmeid saab ka Microsoft Excelisse eksportida.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="f2cb4-114">Klõpsake valikut Kuva ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-114">Click View purchase order.</span></span>
3. <span data-ttu-id="f2cb4-115">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="f2cb4-116">Rida on märgitud kui Saadetis ja päise jaotis näitab, et ostutellimuse olek on Vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="f2cb4-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="f2cb4-118">Vabade kaubavarude vaatamine</span><span class="sxs-lookup"><span data-stu-id="f2cb4-118">View on-hand inventory</span></span>
1. <span data-ttu-id="f2cb4-119">Avage Hankija koostöö > Veose varud > Veose vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="f2cb4-120">Veose vaba kaubavaru lehel on näidatud teile kuuluvad varud kliendi laos.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="f2cb4-121">Saate kuvada lisadimensioone nagu tegevuskoht ja ladu, klõpsates vahekaarti Kuva dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f2cb4-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]