---
title: Varianditoodete lisamine ostutellimustele, kasutades variandi kaalu
description: See protseduur selgitab variandimasside kasutamist ostutellimuse ridade automaatseks täitmiseks iga tootevariandi puhul.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446260a09bd5177877637ac8a288ad584dfa2b2b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568692"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="4fe2c-103">Varianditoodete lisamine ostutellimustele, kasutades variandi kaalu</span><span class="sxs-lookup"><span data-stu-id="4fe2c-103">Add variant products to purchase orders using variant weights</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4fe2c-104">See protseduur selgitab variandimasside kasutamist ostutellimuse ridade automaatseks täitmiseks iga tootevariandi puhul.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="4fe2c-105">Kui valite ostetava toote koguse, luuakse kõigi tootevariantide kohta ostutellimuse read koos soovitatud kogustega, mille aluseks on tootevariantidele konfigureeritud massid.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="4fe2c-106">See protseduur ei hõlma tootedimensioonides ja tootevariantides massiväärtuste konfigureerimise etappe.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="4fe2c-107">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4fe2c-108">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="4fe2c-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-109">Click New.</span></span>
3. <span data-ttu-id="4fe2c-110">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4fe2c-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4fe2c-112">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="4fe2c-113">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4fe2c-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4fe2c-115">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4fe2c-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4fe2c-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4fe2c-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-118">Click OK.</span></span>
12. <span data-ttu-id="4fe2c-119">Lülitage jaotise Rea üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="4fe2c-120">Klõpsake vahekaarti Variandid.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="4fe2c-121">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-121">Click Add line.</span></span>
15. <span data-ttu-id="4fe2c-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="4fe2c-123">Sisestage väljale Kaubakood väärtus 0140.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="4fe2c-124">Määrake koguse väärtuseks 1000.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="4fe2c-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-125">Click Save.</span></span>

