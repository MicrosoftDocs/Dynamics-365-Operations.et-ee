---
title: Hankekategooria hierarhia seadistamine
description: See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat.
author: RichardLuan
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44fd02d37ec4e6431ca25dc980ed1d1785e45fac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239346"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="b0d73-103">Hankekategooria hierarhia seadistamine</span><span class="sxs-lookup"><span data-stu-id="b0d73-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0d73-104">See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat.</span><span class="sxs-lookup"><span data-stu-id="b0d73-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="b0d73-105">Neid ülesandeid täidab üldjuhul ostujuht.</span><span class="sxs-lookup"><span data-stu-id="b0d73-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="b0d73-106">Enne, kui saate selle protseduuri käivitada, peab teil olema kategooriahierarhia, mille tüüp on Hange.</span><span class="sxs-lookup"><span data-stu-id="b0d73-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="b0d73-107">Demoettevõtte kasutamisel saate seda protseduuri käitada ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="b0d73-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="b0d73-108">Uue hankekategooria lisamine</span><span class="sxs-lookup"><span data-stu-id="b0d73-108">Add a new procurement category</span></span>
1. <span data-ttu-id="b0d73-109">Avage **Navigeerimispaan > Moodulid > Hanked > Partii > Hanke kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="b0d73-110">Valige Toimingupaanil **Kategooriahierarhia redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="b0d73-111">Lehe vasakus servas kuvatakse praegune hankekategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="b0d73-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="b0d73-112">Hakkate seda hierarhiat muutma.</span><span class="sxs-lookup"><span data-stu-id="b0d73-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="b0d73-113">Valige Toimingupaanil nupp **Uus kategooria sõlm**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="b0d73-114">Süsteem valib vaikimisi ülemise sõlme.</span><span class="sxs-lookup"><span data-stu-id="b0d73-114">The system selects the top node by default.</span></span> <span data-ttu-id="b0d73-115">Kui käitate seda protseduuri ülesandejuhendina, saate klõpsata nuppu Ava ja valida teise ülataseme sõlme, millesse oma uus sõlm lisada.</span><span class="sxs-lookup"><span data-stu-id="b0d73-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="b0d73-116">Kui see on tehtud, lukustage uuesti ülesandejuhend ja klõpsake sõlme Uus kategooria.</span><span class="sxs-lookup"><span data-stu-id="b0d73-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="b0d73-117">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b0d73-118">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="b0d73-119">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="b0d73-120">Hüüdnimi on valikuline.</span><span class="sxs-lookup"><span data-stu-id="b0d73-120">The friendly name is optional.</span></span> <span data-ttu-id="b0d73-121">See kuvatakse kategooriaotsingutes koos kategooria nimega.</span><span class="sxs-lookup"><span data-stu-id="b0d73-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="b0d73-122">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="b0d73-123">Toodete lisamine uude hankekategooriasse</span><span class="sxs-lookup"><span data-stu-id="b0d73-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="b0d73-124">Avage **Hanked > Partii > Hanke kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="b0d73-125">Valige äsjalisatud sõlm.</span><span class="sxs-lookup"><span data-stu-id="b0d73-125">Select the node you just added.</span></span> <span data-ttu-id="b0d73-126">Kui käitate seda protseduuri ülesandejuhendina, peate sõlme valimiseks võib-olla ülesandejuhendi avama.</span><span class="sxs-lookup"><span data-stu-id="b0d73-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="b0d73-127">Lülitage jaotist **Tooted** sisse välja.</span><span class="sxs-lookup"><span data-stu-id="b0d73-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="b0d73-128">Valige suvand **Lisa**, et seostada tooted hankekategooriaga.</span><span class="sxs-lookup"><span data-stu-id="b0d73-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="b0d73-129">Valige tooted, mille soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="b0d73-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="b0d73-130">Toodete lisamiseks tabelisse **Valitud** valige nool.</span><span class="sxs-lookup"><span data-stu-id="b0d73-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="b0d73-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0d73-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]