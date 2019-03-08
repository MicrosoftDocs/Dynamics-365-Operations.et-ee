---
title: Varade loomine ja soetamine ostureskontrost
description: See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "316414"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="35244-103">Varade loomine ja soetamine ostureskontrost</span><span class="sxs-lookup"><span data-stu-id="35244-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35244-104">See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga.</span><span class="sxs-lookup"><span data-stu-id="35244-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="35244-105">See kasutab raamatupidamis- ja ostureskontroametnikke ja demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="35244-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="35244-106">Põhivara parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="35244-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="35244-107">Avage Põhivarad > Seadistus > Põhivarade parameetrid.</span><span class="sxs-lookup"><span data-stu-id="35244-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="35244-108">Laiendage või ahendage jaotist Ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="35244-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="35244-109">Märkige ruut Luba vara soetamine ostmiselt.</span><span class="sxs-lookup"><span data-stu-id="35244-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="35244-110">Märkige ruut Loo vara toote sissetuleku või arve sisestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="35244-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="35244-111">Uue hankija arve koostamine</span><span class="sxs-lookup"><span data-stu-id="35244-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="35244-112">Avage Ostureskontro > Tööruumid > Hankija arved.</span><span class="sxs-lookup"><span data-stu-id="35244-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="35244-113">Klõpsake suvandit Uus hankija arve.</span><span class="sxs-lookup"><span data-stu-id="35244-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="35244-114">Klõpsake väljal Arve konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="35244-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="35244-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="35244-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="35244-116">Sisestage väärtus väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="35244-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="35244-117">Sisestage kuupäev väljale Sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="35244-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="35244-118">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="35244-118">Click Add line.</span></span>
8. <span data-ttu-id="35244-119">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="35244-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35244-120">Põhivara soetamisel saab kasutada mitteladustatavaid kaupu või hankekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="35244-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="35244-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="35244-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="35244-122">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="35244-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="35244-123">Üks arve rida loob ainult ühe põhivara, olenemata kogusest.</span><span class="sxs-lookup"><span data-stu-id="35244-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="35244-124">Arve koguse välja väärtus kantakse üle põhivara kogusele.</span><span class="sxs-lookup"><span data-stu-id="35244-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="35244-125">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="35244-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="35244-126">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="35244-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="35244-127">Klõpsake vahekaarti Põhivara.</span><span class="sxs-lookup"><span data-stu-id="35244-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="35244-128">Märkige ruut Loo uus põhivara.</span><span class="sxs-lookup"><span data-stu-id="35244-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="35244-129">Klõpsake väljal Põhivara grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="35244-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="35244-130">Valige loendist uue põhivara loomiseks kasutatav põhivara grupp.</span><span class="sxs-lookup"><span data-stu-id="35244-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="35244-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="35244-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="35244-132">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="35244-132">Click Post.</span></span>
    * <span data-ttu-id="35244-133">Põhivara luuakse ja soetatakse arve sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="35244-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

