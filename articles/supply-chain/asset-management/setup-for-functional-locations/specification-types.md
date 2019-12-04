---
title: Hoolduse atribuudi tüübid
description: Selles teemas selgitatakse, kuidas luua varahalduses atribuudi tüüpe.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 625e2c6a6b385c69d33ec4325a462310a37f1eed
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812187"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="d53ac-103">Hoolduse atribuudi tüübid</span><span class="sxs-lookup"><span data-stu-id="d53ac-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d53ac-104">Selles teemas selgitatakse, kuidas luua varahalduses atribuudi tüüpe.</span><span class="sxs-lookup"><span data-stu-id="d53ac-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="d53ac-105">Atribuute kasutatakse erinevate elementide omaduste kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="d53ac-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="d53ac-106">Saate seadistada atribuudid järgmistele elementidele.</span><span class="sxs-lookup"><span data-stu-id="d53ac-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="d53ac-107">Töö asukoha tüübid</span><span class="sxs-lookup"><span data-stu-id="d53ac-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="d53ac-108">Töö asukohtade loomine</span><span class="sxs-lookup"><span data-stu-id="d53ac-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="d53ac-109">Vara tüübid</span><span class="sxs-lookup"><span data-stu-id="d53ac-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="d53ac-110">Varad</span><span class="sxs-lookup"><span data-stu-id="d53ac-110">Assets</span></span>

<span data-ttu-id="d53ac-111">Seadistatavad atribuudid erinevad vastavalt elemendile.</span><span class="sxs-lookup"><span data-stu-id="d53ac-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="d53ac-112">Näiteks saate funktsionaalsele asukohale seadistada atribuudid konfiguratsiooni ja asukoha füüsilise suuruse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d53ac-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="d53ac-113">Vara tüübi ja vara korral saate seadistada atribuudid mootorimahule, energiatarbele ja maksimaalsele koormusele erinevatel tingimustel.</span><span class="sxs-lookup"><span data-stu-id="d53ac-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="d53ac-114">Atribuudi tüüpide loomine</span><span class="sxs-lookup"><span data-stu-id="d53ac-114">Create attribute types</span></span>

<span data-ttu-id="d53ac-115">Saate luua oma atribuudi tüüpe.</span><span class="sxs-lookup"><span data-stu-id="d53ac-115">You can create your own attribute types.</span></span> <span data-ttu-id="d53ac-116">Lisaks saate edastada tootedimensioone rakendusest lehele **Atribuudi tüübid**.</span><span class="sxs-lookup"><span data-stu-id="d53ac-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="d53ac-117">Valige **Varahaldus**\>**Häälestus**\>**Atribuudi tüübid**.</span><span class="sxs-lookup"><span data-stu-id="d53ac-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="d53ac-118">Esimesel korral kui atribuudi tüüpe seadistate, valige **Tootedimensioonide loomine**, et edastada automaatselt standardsed tootedimensioonid.</span><span class="sxs-lookup"><span data-stu-id="d53ac-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="d53ac-119">Valige uue atribuudi tüübi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d53ac-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="d53ac-120">Väljale **Atribuudi tüüp** sisestage atribuudi tüübi nimi.</span><span class="sxs-lookup"><span data-stu-id="d53ac-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="d53ac-121">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d53ac-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="d53ac-122">Väljale **Ühik** valige vastavalt vajadusele vastav atribuudi ühik.</span><span class="sxs-lookup"><span data-stu-id="d53ac-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="d53ac-123">Valige väljal **Andmetüüp** ühiku andmetüüp.</span><span class="sxs-lookup"><span data-stu-id="d53ac-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="d53ac-124">Kui valisite andmetüübiks **String**, toimige atribuudi tüübi väärtuste loomiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d53ac-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="d53ac-125">Valige atribuudi tüüp ja seejärel valige **Väärtused**.</span><span class="sxs-lookup"><span data-stu-id="d53ac-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="d53ac-126">Valige väljal **Atribuudi väärtused** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d53ac-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="d53ac-127">Valige väljal **Atribuudi tüüp** atribuudi tüüp (dimensioon).</span><span class="sxs-lookup"><span data-stu-id="d53ac-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="d53ac-128">Sisestage väljale **Väärtus** seotud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d53ac-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="d53ac-129">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d53ac-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="d53ac-130">Salvesta kirje.</span><span class="sxs-lookup"><span data-stu-id="d53ac-130">Save the record.</span></span>
    7. <span data-ttu-id="d53ac-131">Naaske lehele **Atribuudi tüübid**.</span><span class="sxs-lookup"><span data-stu-id="d53ac-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="d53ac-132">Salvesta kirje.</span><span class="sxs-lookup"><span data-stu-id="d53ac-132">Save the record.</span></span>

    <span data-ttu-id="d53ac-133">Väli **Funktsionaalsed asukoha tüübid** näitab funktsionaalsete asukohtade arvu, mis atribuudi tüüpi kasutavad.</span><span class="sxs-lookup"><span data-stu-id="d53ac-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="d53ac-134">Väli **Vara tüübid** näitab seda kasutavate vara tüüpide arvu.</span><span class="sxs-lookup"><span data-stu-id="d53ac-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
