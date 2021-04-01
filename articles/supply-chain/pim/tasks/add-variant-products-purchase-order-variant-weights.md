---
title: Varianditoodete lisamine ostutellimustele, kasutades variandi kaalu
description: See protseduur selgitab variandimasside kasutamist ostutellimuse ridade automaatseks täitmiseks iga tootevariandi puhul.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cd4ca3652c1ce7422e8f80426a7b11545e09861
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242561"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="ce61b-103">Varianditoodete lisamine ostutellimustele, kasutades variandi kaalu</span><span class="sxs-lookup"><span data-stu-id="ce61b-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce61b-104">See protseduur selgitab variandimasside kasutamist ostutellimuse ridade automaatseks täitmiseks iga tootevariandi puhul.</span><span class="sxs-lookup"><span data-stu-id="ce61b-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="ce61b-105">Kui valite ostetava toote koguse, luuakse kõigi tootevariantide kohta ostutellimuse read koos soovitatud kogustega, mille aluseks on tootevariantidele konfigureeritud massid.</span><span class="sxs-lookup"><span data-stu-id="ce61b-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="ce61b-106">See protseduur ei hõlma tootedimensioonides ja tootevariantides massiväärtuste konfigureerimise etappe.</span><span class="sxs-lookup"><span data-stu-id="ce61b-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="ce61b-107">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="ce61b-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ce61b-108">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="ce61b-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="ce61b-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ce61b-109">Click New.</span></span>
3. <span data-ttu-id="ce61b-110">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ce61b-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ce61b-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ce61b-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ce61b-112">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="ce61b-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="ce61b-113">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ce61b-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ce61b-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ce61b-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ce61b-115">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ce61b-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ce61b-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ce61b-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ce61b-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ce61b-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ce61b-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ce61b-118">Click OK.</span></span>
12. <span data-ttu-id="ce61b-119">Lülitage jaotise Rea üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="ce61b-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="ce61b-120">Klõpsake vahekaarti Variandid.</span><span class="sxs-lookup"><span data-stu-id="ce61b-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="ce61b-121">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="ce61b-121">Click Add line.</span></span>
15. <span data-ttu-id="ce61b-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ce61b-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="ce61b-123">Sisestage väljale Kaubakood väärtus 0140.</span><span class="sxs-lookup"><span data-stu-id="ce61b-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="ce61b-124">Määrake koguse väärtuseks 1000.</span><span class="sxs-lookup"><span data-stu-id="ce61b-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="ce61b-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ce61b-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]