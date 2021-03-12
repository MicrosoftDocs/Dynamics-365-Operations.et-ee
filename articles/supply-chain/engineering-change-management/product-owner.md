---
title: Tooteomanikud
description: Teema annab teavet tooteomanike kohta. Tooteomanikud on kasutajad, kes vastutavad konkreetsete toodete eest. Neid tooteid saavad väljastada ainult grupi liikmed. Tooteomanikku saab kasutada ka kinnitamise töövoos.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 90f5596f9b5fc45e78cc49a3309c45864e07e70b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967329"
---
# <a name="product-owners"></a><span data-ttu-id="88bf0-106">Tooteomanikud</span><span class="sxs-lookup"><span data-stu-id="88bf0-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88bf0-107">Tooteomanikud on kasutajad, kes vastutavad konkreetsete toodete eest.</span><span class="sxs-lookup"><span data-stu-id="88bf0-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="88bf0-108">Kui tooteomaniku grupp on määratud tootele, saavad toote väljastada ainult selle grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="88bf0-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="88bf0-109">Tooteomanikku saab kasutada ka kinnitamise töövoos tehniliste muudatuste halduses.</span><span class="sxs-lookup"><span data-stu-id="88bf0-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="88bf0-110">Tooteomanikud on globaalsed sätted.</span><span class="sxs-lookup"><span data-stu-id="88bf0-110">Product owners are global settings.</span></span> <span data-ttu-id="88bf0-111">Seetõttu on need kättesaadavad kõikidele juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="88bf0-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="88bf0-112">Tooteomaniku grupi loomine</span><span class="sxs-lookup"><span data-stu-id="88bf0-112">Create a product owner group</span></span>

<span data-ttu-id="88bf0-113">Tooteomaniku grupi loomiseks ja sellele liikmete lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="88bf0-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="88bf0-114">Valige **Tehniliste muudatuste haldus \> Häälestus \> Tooteomanikud**.</span><span class="sxs-lookup"><span data-stu-id="88bf0-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="88bf0-115">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="88bf0-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="88bf0-116">Sisestage väljale **Tooteomanik** grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="88bf0-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="88bf0-117">Väljale **Nimi** sisestage grupi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="88bf0-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="88bf0-118">Kiirkaardile **Liikmed** lisage töötajad, kes peaksid olema grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="88bf0-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="88bf0-119">Tootele tooteomaniku määramine</span><span class="sxs-lookup"><span data-stu-id="88bf0-119">Assign a product owner to a product</span></span>

<span data-ttu-id="88bf0-120">Tootele tooteomaniku määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="88bf0-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="88bf0-121">Avage asjakohase toote või tooteetaloni leht **Toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="88bf0-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="88bf0-122">Kiirkaardil **Üldine** määrake väljale **Tooteomanik** asjakohase tooteomaniku rühma nimi.</span><span class="sxs-lookup"><span data-stu-id="88bf0-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="88bf0-123">Kui tooteomanik on tootele määratud, saavad sätet **Tooteomanik** redigeerida ainult tooteomaniku grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="88bf0-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="88bf0-124">Tooteomanik on nähtav ka lehel **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="88bf0-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="88bf0-125">Toote omanikud ja toote väljalasked</span><span class="sxs-lookup"><span data-stu-id="88bf0-125">Product owners and product releases</span></span>

<span data-ttu-id="88bf0-126">Selle toote saavad väljastada ainult tooteomaniku grupi kasutajad.</span><span class="sxs-lookup"><span data-stu-id="88bf0-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="88bf0-127">Siiski on tegu erandiga, kui toode on tütarüksus ja selle emaüksuse väljastaja on emaüksuse omanik.</span><span class="sxs-lookup"><span data-stu-id="88bf0-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="88bf0-128">Teisisõnu, kui toode on osa mõnest teise toote kooslusest, ei kontrolli süsteem koosluse iga üksuse tooteomanikku.</span><span class="sxs-lookup"><span data-stu-id="88bf0-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="88bf0-129">See kontrollib ainult emaüksuse tooteomanikku.</span><span class="sxs-lookup"><span data-stu-id="88bf0-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="88bf0-130">Näiteks toode X on määratud *Disainkappide* toote omaniku grupile.</span><span class="sxs-lookup"><span data-stu-id="88bf0-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="88bf0-131">Toode X on ühtlasi osa toote Y kooslusest, mis on määratud tooteomaniku grupile *Kõlaridisain*.</span><span class="sxs-lookup"><span data-stu-id="88bf0-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="88bf0-132">Kui tooteomaniku grupi *Kujunduskõlarid* kasutaja väljastab toote Y ja selle koosluse, väljastatakse toode X koos tootega Y.</span><span class="sxs-lookup"><span data-stu-id="88bf0-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="88bf0-133">Tooteomanikud ja kinnitused</span><span class="sxs-lookup"><span data-stu-id="88bf0-133">Product owners and approvals</span></span>

<span data-ttu-id="88bf0-134">Kuna tooteomanikud teavad, kas konkreetsetest tehnilistest muudatustest on toodetele kasu, on sageli mõistlik kaasata need tehniliste muudatuste halduses kinnitamise protsessi osana.</span><span class="sxs-lookup"><span data-stu-id="88bf0-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="88bf0-135">Saate selle lähenemise rakendada, häälestades tooteomanikud osalevate pakkujatena töövoogudes, mida kasutatakse tehniliste muudatuste haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="88bf0-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="88bf0-136">Süsteem määrab seejärel töövoodes kinnitamise ülesanded, mis põhinevad tehniliste muudatuste taotlustes ja tehnilise muudatuste tellimustes olevatel toodetel.</span><span class="sxs-lookup"><span data-stu-id="88bf0-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="88bf0-137">Lisateavet vt teemast [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="88bf0-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
