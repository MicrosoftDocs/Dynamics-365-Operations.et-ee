---
title: Hankekategooria hierarhia seadistamine
description: See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat.
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e45c80718c73ad785643c2a5fc0e712b291104d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426552"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="69bf9-103">Hankekategooria hierarhia seadistamine</span><span class="sxs-lookup"><span data-stu-id="69bf9-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69bf9-104">See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat.</span><span class="sxs-lookup"><span data-stu-id="69bf9-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="69bf9-105">Neid ülesandeid täidab üldjuhul ostujuht.</span><span class="sxs-lookup"><span data-stu-id="69bf9-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="69bf9-106">Enne, kui saate selle protseduuri käivitada, peab teil olema kategooriahierarhia, mille tüüp on Hange.</span><span class="sxs-lookup"><span data-stu-id="69bf9-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="69bf9-107">Demoettevõtte kasutamisel saate seda protseduuri käitada ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="69bf9-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="69bf9-108">Uue hankekategooria lisamine</span><span class="sxs-lookup"><span data-stu-id="69bf9-108">Add a new procurement category</span></span>
1. <span data-ttu-id="69bf9-109">Avage **Navigeerimispaan > Moodulid > Hanked > Partii > Hanke kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="69bf9-110">Valige Toimingupaanil **Kategooriahierarhia redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="69bf9-111">Lehe vasakus servas kuvatakse praegune hankekategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="69bf9-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="69bf9-112">Hakkate seda hierarhiat muutma.</span><span class="sxs-lookup"><span data-stu-id="69bf9-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="69bf9-113">Valige Toimingupaanil nupp **Uus kategooria sõlm**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="69bf9-114">Süsteem valib vaikimisi ülemise sõlme.</span><span class="sxs-lookup"><span data-stu-id="69bf9-114">The system selects the top node by default.</span></span> <span data-ttu-id="69bf9-115">Kui käitate seda protseduuri ülesandejuhendina, saate klõpsata nuppu Ava ja valida teise ülataseme sõlme, millesse oma uus sõlm lisada.</span><span class="sxs-lookup"><span data-stu-id="69bf9-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="69bf9-116">Kui see on tehtud, lukustage uuesti ülesandejuhend ja klõpsake sõlme Uus kategooria.</span><span class="sxs-lookup"><span data-stu-id="69bf9-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="69bf9-117">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="69bf9-118">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="69bf9-119">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="69bf9-120">Hüüdnimi on valikuline.</span><span class="sxs-lookup"><span data-stu-id="69bf9-120">The friendly name is optional.</span></span> <span data-ttu-id="69bf9-121">See kuvatakse kategooriaotsingutes koos kategooria nimega.</span><span class="sxs-lookup"><span data-stu-id="69bf9-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="69bf9-122">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="69bf9-123">Toodete lisamine uude hankekategooriasse</span><span class="sxs-lookup"><span data-stu-id="69bf9-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="69bf9-124">Avage **Hanked > Partii > Hanke kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="69bf9-125">Valige äsjalisatud sõlm.</span><span class="sxs-lookup"><span data-stu-id="69bf9-125">Select the node you just added.</span></span> <span data-ttu-id="69bf9-126">Kui käitate seda protseduuri ülesandejuhendina, peate sõlme valimiseks võib-olla ülesandejuhendi avama.</span><span class="sxs-lookup"><span data-stu-id="69bf9-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="69bf9-127">Lülitage jaotist **Tooted** sisse välja.</span><span class="sxs-lookup"><span data-stu-id="69bf9-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="69bf9-128">Valige suvand **Lisa**, et seostada tooted hankekategooriaga.</span><span class="sxs-lookup"><span data-stu-id="69bf9-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="69bf9-129">Valige tooted, mille soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="69bf9-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="69bf9-130">Toodete lisamiseks tabelisse **Valitud** valige nool.</span><span class="sxs-lookup"><span data-stu-id="69bf9-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="69bf9-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="69bf9-131">Select **OK**.</span></span>
