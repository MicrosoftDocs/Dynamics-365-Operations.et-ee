---
title: Varade loomine ja soetamine ostureskontrost
description: See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cb9a37c65fb8eab4db6084b91a71c13a45ba42c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442397"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="c0e6a-103">Varade loomine ja soetamine ostureskontrost</span><span class="sxs-lookup"><span data-stu-id="c0e6a-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0e6a-104">See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="c0e6a-105">See kasutab raamatupidamis- ja ostureskontroametnikke ja demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="c0e6a-106">Põhivara parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="c0e6a-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="c0e6a-107">Paanil **Navigeerimispaan** avage **Moodulid > Põhivarad > Seadistus > Põhivara parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="c0e6a-108">Laiendage kiirkaart **Ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="c0e6a-109">Märkige märkeruut **Luba vara soetamine ostmiselt**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="c0e6a-110">Märkige märkeruut **Loo vara toote sissetuleku või arve sisestamise ajal**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="c0e6a-111">Uue hankija arve koostamine</span><span class="sxs-lookup"><span data-stu-id="c0e6a-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="c0e6a-112">Paanil **Navigeerimispaan** avage **Moodulid > Ostureskontro > Tööruumid > Hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="c0e6a-113">Klõpsake **Uus hankija arve**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="c0e6a-114">Väljal **Arve konto** klõpsake rippmenüü nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c0e6a-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c0e6a-116">Sisestage väärtus väljale **Arv**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="c0e6a-117">Väljale **Sisestuskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="c0e6a-118">Klõpsake käsku **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-118">Click **Add line**.</span></span>
8. <span data-ttu-id="c0e6a-119">Väljal **Kaubakood** klõpsake ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="c0e6a-120">Põhivara soetamisel saab kasutada mitteladustatavaid kaupu või hankekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="c0e6a-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c0e6a-122">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="c0e6a-123">Üks arve rida loob ainult ühe põhivara, olenemata kogusest.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="c0e6a-124">Arve koguse välja väärtus kantakse üle põhivara kogusele.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="c0e6a-125">Sisestage arv väljale **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="c0e6a-126">Laiendage kiirkaarti **Rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="c0e6a-127">Klõpsake vahekaarti **Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="c0e6a-128">Märkige märkeruut **Loo uus põhivara**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="c0e6a-129">Väljal **Põhivara grupp** klõpsake rippmenüü nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="c0e6a-130">Valige loendist uue põhivara loomiseks kasutatav põhivara grupp.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="c0e6a-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c0e6a-132">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-132">Click **Post**.</span></span> <span data-ttu-id="c0e6a-133">Põhivara luuakse ja soetatakse arve sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="c0e6a-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

