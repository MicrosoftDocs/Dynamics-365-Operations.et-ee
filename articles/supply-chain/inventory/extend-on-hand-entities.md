---
title: Vaba kaubavaru andmeüksuste laiendamine
description: Selles teemas näidatakse, kuidas lisada laiendatud välju vaadetele INVENTORSITEONHANDENTITY ja INVENTWAREHOUSEONHANDENTITY, nii et vaba kaubavaru andmeüksuste võimalused oleksid saadaval ka laiendustes.
author: sherry-zheng
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7863f37e66727e2e80ea8c8b013ee49930e7c684
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829904"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="eb16c-103">Vaba kaubavaru andmeüksuste laiendamine</span><span class="sxs-lookup"><span data-stu-id="eb16c-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb16c-104">Microsoft Dynamics 365 Supply Chain Management pakub [laiendatavuse](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) funktsioone, mis võimaldavad teil [lisada tabelile välju laienduse kaudu](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span><span class="sxs-lookup"><span data-stu-id="eb16c-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="eb16c-105">Selles teemas näidatakse, kuidas lisada laiendatud välju vaadetele `INVENTORSITEONHANDENTITY` ja `INVENTWAREHOUSEONHANDENTITY`, nii et vaba kaubavaru andmeüksuste võimalused oleksid saadaval ka laiendustes.</span><span class="sxs-lookup"><span data-stu-id="eb16c-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="eb16c-106">Lisateavet andmeüksuste kohta leiate teemast [Andmehalduse ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="eb16c-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="eb16c-107">Siin on loend mõnest vaba kaubavaru üksusest.</span><span class="sxs-lookup"><span data-stu-id="eb16c-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="eb16c-108">Vaba kaubavaru laoala järgi</span><span class="sxs-lookup"><span data-stu-id="eb16c-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="eb16c-109">Vaba kaubavaru laoala järgi V2</span><span class="sxs-lookup"><span data-stu-id="eb16c-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="eb16c-110">Vaba kaubavaru lao järgi</span><span class="sxs-lookup"><span data-stu-id="eb16c-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="eb16c-111">Vaba kaubavaru lao järgi V2</span><span class="sxs-lookup"><span data-stu-id="eb16c-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="eb16c-112">Pärast väljade lisamist tabelitele, mida kasutab vaade `inventSiteOnHandView`, peate mootori sünkroonima, et laiendusi tuvastataks õigesti.</span><span class="sxs-lookup"><span data-stu-id="eb16c-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="eb16c-113">Laiendage laiendusvälja lisamise kaudu vaadet `InventSiteOnHandView`.</span><span class="sxs-lookup"><span data-stu-id="eb16c-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="eb16c-114">Laiendage laiendusväljade abil vaadet `InventSiteOnHandAggregatedView`.</span><span class="sxs-lookup"><span data-stu-id="eb16c-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="eb16c-115">Laiendage `InventSiteOnHandAggregatedViewBuilder`i klassi viewBuilder, muutes meetodit `getExtensionFields()`.</span><span class="sxs-lookup"><span data-stu-id="eb16c-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="eb16c-116">Sel viisil vastendate üksuse viewBuilder sünkroomise käitamisel vana vaate väljad uue vaate väljadega.</span><span class="sxs-lookup"><span data-stu-id="eb16c-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="eb16c-117">Näiteks olete laienduse kaudu lisanud tabelisse `InventTable` järgmised neli välja.</span><span class="sxs-lookup"><span data-stu-id="eb16c-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="eb16c-118">Kohandatud väli 1</span><span class="sxs-lookup"><span data-stu-id="eb16c-118">Custom field 1</span></span>
- <span data-ttu-id="eb16c-119">Kohandatud väli 2</span><span class="sxs-lookup"><span data-stu-id="eb16c-119">Custom field 2</span></span>
- <span data-ttu-id="eb16c-120">Kohandatud väli 3</span><span class="sxs-lookup"><span data-stu-id="eb16c-120">Custom field 3</span></span>
- <span data-ttu-id="eb16c-121">Kohandatud väli 4</span><span class="sxs-lookup"><span data-stu-id="eb16c-121">Custom field 4</span></span>

<span data-ttu-id="eb16c-122">Sel juhul peate muutma meetodit `getExtensionFields()` järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="eb16c-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="eb16c-123">Pärast nende juhiste järgimist saate uute väljade lisamise teel laiendada andmeüksusi „vaba kaubavaru laoala järgi” ja „vaba kaubavaru lao järgi”.</span><span class="sxs-lookup"><span data-stu-id="eb16c-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="eb16c-124">Sel viisil tagate, et laiendatud väljad tuvastatakse ja kaasatakse neid andmeüksusi kasutavate andmete migreerimisel.</span><span class="sxs-lookup"><span data-stu-id="eb16c-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]