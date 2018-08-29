---
title: Retaili tootekategooriate ja toodete haldamine
description: "Selles teemas kirjeldatakse, kuidas tootejuhid saavad kasutada Retaili tootekategooriaid Retaili tootehierarhia ja väljastatud toote üksikasjade vaheliste seoste haldamiseks."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 19c972164474c972aab642c3cccc67cf396a6cb2
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="76d5b-103">Retaili tootekategooriate ja toodete haldamine</span><span class="sxs-lookup"><span data-stu-id="76d5b-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="76d5b-104">Selles teemas kirjeldatakse täiustatud viisi Retaili tootekategooriate ja toodete haldamiseks rakenduses Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="76d5b-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="76d5b-105">Täiustused võimaldavad tootejuhtidel vaadata tooteatribuutide üldist struktuuri Retaili tootehierarhia ja väljastatud toote üksikasjade vahel.</span><span class="sxs-lookup"><span data-stu-id="76d5b-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="76d5b-106">Lisateavet Retaili tootekategooriate haldamise kohta vaadake tööruumi **Kategooria ja toote haldus** tööruumi paanilt **Retaili tootehierarhia**.</span><span class="sxs-lookup"><span data-stu-id="76d5b-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="76d5b-107">Pange tähele kuvatava lehe **Retaili tootehierarhia** täiustatud struktuuri.</span><span class="sxs-lookup"><span data-stu-id="76d5b-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="76d5b-108">Retaili varasemates versioonides olid toote atribuudid jagatud kohaldatava ulatuse alusel *toote põhiatribuutideks* ja *Retaili tooteatribuutideks*.</span><span class="sxs-lookup"><span data-stu-id="76d5b-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="76d5b-109">Retaili tooteatribuudid on kohaldatava ulatuse järgi *globaalsed*.</span><span class="sxs-lookup"><span data-stu-id="76d5b-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="76d5b-110">Teisisõnu: antud Retaili tooteatribuudi puhul jagatakse sama väärtust kõigi juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="76d5b-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="76d5b-111">See-eest toote põhiatribuudid on *juriidilise isiku põhised*.</span><span class="sxs-lookup"><span data-stu-id="76d5b-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="76d5b-112">Teisisõnu: antud toote põhiatribuudi korral võib väärtus juriidiliste isikute lõikes erineda, olenevalt iga juriidilise isiku ärivajadustest.</span><span class="sxs-lookup"><span data-stu-id="76d5b-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="76d5b-113">Retaili tootekategooria täiustatud struktuuris on tooteatribuudid loogiliselt eraldatud nende kohalduvuse alusel grupis, peegeldades väljastatud toote üksikasjade vormi struktuuri.</span><span class="sxs-lookup"><span data-stu-id="76d5b-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Väljade grupeerimine atribuutide kohaldatavuse ulatuse põhjal](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="76d5b-115">Saate valida juriidilise isiku põhiste atribuutide haldamise kõigi juriidiliste isikute lõikes ja konkreetse juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="76d5b-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="76d5b-116">Atribuutide haldamiseks kõigi juriidiliste isikute lõikes valige **Kuva kõigi juriidiliste isikute puhul** (või **Redigeeri kõigi juriidiliste isikute puhul**).</span><span class="sxs-lookup"><span data-stu-id="76d5b-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Kuvamine/redigeerimine kõigi juriidiliste isikute puhul](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="76d5b-118">Konkreetse juriidilise isiku atribuutide haldamiseks valige **Kuva konkreetse juriidilise isiku puhul** (või **Redigeeri konkreetse juriidilise isiku puhul**).</span><span class="sxs-lookup"><span data-stu-id="76d5b-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Kuvamine/redigeerimine konkreetse juriidilise isiku puhul](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="76d5b-120">Lisaks saab tootejuht täiustatud Retaili tootekategooria struktuuris määrata nüüd vaikeväärtusi täiendavale tooteatribuutide kogumile eraldi kategooria tasandil.</span><span class="sxs-lookup"><span data-stu-id="76d5b-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="76d5b-121">Seejärel pärivad tooted loomise ajal need tooteatribuudi vaikeväärtused, põhinedes nende atribuutide seosel individuaalse kategooriaga Retaili tootehierarhiast.</span><span class="sxs-lookup"><span data-stu-id="76d5b-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="76d5b-122">Neid päritud tooteatribuute saab ka iga toote puhul muuta, et need oleksid konkreetse äri vajadustega kooskõlas.</span><span class="sxs-lookup"><span data-stu-id="76d5b-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="76d5b-123">Atribuutide valimine toodete värskendamiseks Retaili hierarhia lehelt</span><span class="sxs-lookup"><span data-stu-id="76d5b-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="76d5b-124">Saate uut tooteatribuutide täiustatud struktuuri kasutada selleks, et valida, millised värskendatud tooteatribuudid tuleb seotud toodetele tõugata.</span><span class="sxs-lookup"><span data-stu-id="76d5b-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="76d5b-125">Valige lehe **Retaili tootehierarhia** tegumiribalt **Kategooria** ja seejärel dialoogiboksi **Värskenda tooteid** avamiseks **Värskenda tooteid**.</span><span class="sxs-lookup"><span data-stu-id="76d5b-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialoogiboks Värskenda tooteid](media/NewUpdateProductsEnhancedView.PNG)


