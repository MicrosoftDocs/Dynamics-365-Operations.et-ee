---
title: Tootekategooriate ja toodete haldamine
description: Selles teemas kirjeldatakse, kuidas tootejuhid saavad kasutada tootekategooriaid Commerce'i tootehierarhia ja väljastatud toote üksikasjade vaheliste seoste haldamiseks.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 95a4bac6beeaf5fad449027d93132fc1499288a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215482"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="c951d-103">Tootekategooriate ja toodete haldamine</span><span class="sxs-lookup"><span data-stu-id="c951d-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="c951d-104">Selles teemas kirjeldatakse täiustatud viisi tootekategooriate ja toodete haldamiseks rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c951d-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c951d-105">Täiustused võimaldavad tootejuhtidel vaadata tooteatribuutide üldist struktuuri tootehierarhia ja väljastatud toote üksikasjade vahel.</span><span class="sxs-lookup"><span data-stu-id="c951d-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="c951d-106">Lisateavet tootekategooriate haldamise kohta vaadake tööruumi **Kategooria ja toote haldus** tööruumi paanilt **Commerce'i tootehierarhia**.</span><span class="sxs-lookup"><span data-stu-id="c951d-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="c951d-107">Pange tähele kuvatava lehe **Commerce'i tootehierarhia** täiustatud struktuuri.</span><span class="sxs-lookup"><span data-stu-id="c951d-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="c951d-108">Rakenduse varasemates versioonides olid toote atribuudid jagatud kohaldatava ulatuse alusel *toote põhiatribuutideks* ja *Retaili tooteatribuutideks*.</span><span class="sxs-lookup"><span data-stu-id="c951d-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="c951d-109">Retaili tooteatribuudid on kohaldatava ulatuse järgi *globaalsed*.</span><span class="sxs-lookup"><span data-stu-id="c951d-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="c951d-110">Teisisõnu: antud tooteatribuudi puhul jagatakse sama väärtust kõigi juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="c951d-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="c951d-111">See-eest toote põhiatribuudid on *juriidilise isiku põhised*.</span><span class="sxs-lookup"><span data-stu-id="c951d-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="c951d-112">Teisisõnu: antud toote põhiatribuudi korral võib väärtus juriidiliste isikute lõikes erineda, olenevalt iga juriidilise isiku ärivajadustest.</span><span class="sxs-lookup"><span data-stu-id="c951d-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="c951d-113">Tootekategooria täiustatud struktuuris on tooteatribuudid loogiliselt eraldatud nende kohalduvuse alusel grupis, peegeldades väljastatud toote üksikasjade vormi struktuuri.</span><span class="sxs-lookup"><span data-stu-id="c951d-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Väljade grupeerimine atribuutide kohaldatavuse ulatuse põhjal](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="c951d-115">Saate valida juriidilise isiku põhiste atribuutide haldamise kõigi juriidiliste isikute lõikes ja konkreetse juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="c951d-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="c951d-116">Atribuutide haldamiseks kõigi juriidiliste isikute lõikes valige **Kuva kõigi juriidiliste isikute puhul** (või **Redigeeri kõigi juriidiliste isikute puhul**).</span><span class="sxs-lookup"><span data-stu-id="c951d-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Kuvamine/redigeerimine kõigi juriidiliste isikute puhul](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="c951d-118">Konkreetse juriidilise isiku atribuutide haldamiseks valige **Kuva konkreetse juriidilise isiku puhul** (või **Redigeeri konkreetse juriidilise isiku puhul**).</span><span class="sxs-lookup"><span data-stu-id="c951d-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Kuvamine/redigeerimine konkreetse juriidilise isiku puhul](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="c951d-120">Lisaks saab tootejuht täiustatud tootekategooria struktuuris määrata nüüd vaikeväärtusi täiendavale tooteatribuutide kogumile eraldi kategooria tasandil.</span><span class="sxs-lookup"><span data-stu-id="c951d-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="c951d-121">Seejärel pärivad tooted loomise ajal need tooteatribuudi vaikeväärtused, põhinedes nende atribuutide seosel individuaalse kategooriaga tootehierarhiast.</span><span class="sxs-lookup"><span data-stu-id="c951d-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="c951d-122">Neid päritud tooteatribuute saab ka iga toote puhul muuta, et need oleksid konkreetse äri vajadustega kooskõlas.</span><span class="sxs-lookup"><span data-stu-id="c951d-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="c951d-123">Atribuutide valimine toodete värskendamiseks Commerce'i tootehierarhia lehelt</span><span class="sxs-lookup"><span data-stu-id="c951d-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="c951d-124">Saate uut tooteatribuutide täiustatud struktuuri kasutada selleks, et valida, millised värskendatud tooteatribuudid tuleb seotud toodetele tõugata.</span><span class="sxs-lookup"><span data-stu-id="c951d-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="c951d-125">Valige lehe **Commerce'i tootehierarhia** tegumiribalt **Kategooria** ja seejärel dialoogiboksi **Värskenda tooteid** avamiseks **Värskenda tooteid**.</span><span class="sxs-lookup"><span data-stu-id="c951d-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialoogiboks Värskenda tooteid](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]