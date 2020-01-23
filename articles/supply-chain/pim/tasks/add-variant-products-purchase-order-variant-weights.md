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
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adb2300e51f8b5383eee4dea0dffe4129dc8a536
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934813"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="ef3ce-103">Varianditoodete lisamine ostutellimustele, kasutades variandi kaalu</span><span class="sxs-lookup"><span data-stu-id="ef3ce-103">Add variant products to purchase orders using variant weights</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef3ce-104">See protseduur selgitab variandimasside kasutamist ostutellimuse ridade automaatseks täitmiseks iga tootevariandi puhul.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="ef3ce-105">Kui valite ostetava toote koguse, luuakse kõigi tootevariantide kohta ostutellimuse read koos soovitatud kogustega, mille aluseks on tootevariantidele konfigureeritud massid.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="ef3ce-106">See protseduur ei hõlma tootedimensioonides ja tootevariantides massiväärtuste konfigureerimise etappe.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="ef3ce-107">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ef3ce-108">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="ef3ce-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-109">Click New.</span></span>
3. <span data-ttu-id="ef3ce-110">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ef3ce-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ef3ce-112">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="ef3ce-113">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ef3ce-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ef3ce-115">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ef3ce-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ef3ce-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ef3ce-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-118">Click OK.</span></span>
12. <span data-ttu-id="ef3ce-119">Lülitage jaotise Rea üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="ef3ce-120">Klõpsake vahekaarti Variandid.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="ef3ce-121">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-121">Click Add line.</span></span>
15. <span data-ttu-id="ef3ce-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="ef3ce-123">Sisestage väljale Kaubakood väärtus 0140.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="ef3ce-124">Määrake koguse väärtuseks 1000.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="ef3ce-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ef3ce-125">Click Save.</span></span>

