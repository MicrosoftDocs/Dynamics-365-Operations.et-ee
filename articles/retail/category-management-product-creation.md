---
title: Tootekategooria haldus
description: "Selles teemas kirjeldatakse, kuidas tootejuhid saavad kasutada jaemüügi tootekategooriaid jaemüügi tootehierarhia ja väljastatud toote üksikasjade vaheliste seoste haldamiseks."
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
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: et-ee
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="945e6-103">Täiustatud toote ja kategooria haldus</span><span class="sxs-lookup"><span data-stu-id="945e6-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="945e6-104">Selles teemas kirjeldatakse täiustatud viisi jaemüügi tootekategooriate ja toodete haldamiseks rakenduses Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="945e6-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="945e6-105">Need täiustused võimaldavad tootejuhtidel vaadata tooteatribuutide üldist struktuuri jaemüügi tootehierarhia ja väljastatud toote üksikasjade vahel.</span><span class="sxs-lookup"><span data-stu-id="945e6-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="945e6-106">Lisateabe saamiseks jaemüügi tootekategooriate haldamise kohta valige tööruumis **Kategooria ja toote haldus** suvand **Jaemüügi tootehierarhia** ja vaadake lehe **Jaemüügi tootekategooria** täiustatud struktuuri.</span><span class="sxs-lookup"><span data-stu-id="945e6-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Kategooria ja toote halduse tööruum](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="945e6-108">Varasemates versioonides olid toote atribuudid jagatud kohaldatava ulatuse alusel **toote põhiatribuutideks** ja **jaetoote atribuutideks**.</span><span class="sxs-lookup"><span data-stu-id="945e6-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="945e6-109">**Jaetoote atribuudid** olid kohaldatava ulatuse järgi *globaalsed*, mis tähendab, et antud **jaetoote atribuudi** korral on sama väärtus ühiskasutuses kõigi juriidiliste isikute korral.</span><span class="sxs-lookup"><span data-stu-id="945e6-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="945e6-110">**Toote põhiatribuudid** on *juriidilise isiku põhised*.</span><span class="sxs-lookup"><span data-stu-id="945e6-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="945e6-111">Teisisõnu: antud **toote põhiatribuudi** korral võib väärtus juriidiliste isikute lõikes erineda, tuginedes eraldi ettevõtete nõuetele.</span><span class="sxs-lookup"><span data-stu-id="945e6-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="945e6-112">Jaemüügi tootekategooria täiustatud struktuuris on tooteatribuudid loogiliselt eraldatud nende kohalduvuse alusel grupis, peegeldades väljastatud toote üksikasjade vormi struktuuri.</span><span class="sxs-lookup"><span data-stu-id="945e6-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Väljade grupeerimine nende kohaldatavuse ulatuse põhjal](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="945e6-114">Saate valida juriidilise isiku põhiste atribuutide haldamise kõigi juriidiliste isikute lõikes ja konkreetse juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="945e6-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="945e6-115">Valige kas **Kuva/redigeeri kõigi juriidiliste isikute puhul** või **Kuva/redigeeri konkreetse juriidilise isiku puhul**.</span><span class="sxs-lookup"><span data-stu-id="945e6-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Individuaalse ja kõigi juriidiliste isikute vaate vahel valimine](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Individuaalse ja kõigi juriidiliste isikute vaate vahel valimine](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="945e6-118">Eelmiste versioonidega võrreldes saab tootejuht uues jaemüügi tootekategooria struktuuris määrata ka vaikeväärtusi täiendavale tooteatribuutide kogumile eraldi kategooria tasandil.</span><span class="sxs-lookup"><span data-stu-id="945e6-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="945e6-119">Toote loomise ajal pärib toode need tooteatribuudi vaikeväärtused, põhinedes nende seosel individuaalse kategooriaga jaemüügi tootehierarhiast.</span><span class="sxs-lookup"><span data-stu-id="945e6-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="945e6-120">Neid päritud tooteatribuute saab ka iga toote puhul muuta, et need vastaksid konkreetsetele ärinõuetele.</span><span class="sxs-lookup"><span data-stu-id="945e6-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="945e6-121">Valige atribuudid toodete värskendamiseks jaetoote kategooria vormilt</span><span class="sxs-lookup"><span data-stu-id="945e6-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="945e6-122">Saate seda uut tooteatribuutide täiustatud struktuuri kasutada selleks, et valida, millised värskendatud tooteatribuudid tuleb seotud toodetele tõugata.</span><span class="sxs-lookup"><span data-stu-id="945e6-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Toodete värskendamise uus täiustatud vaade](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="945e6-124">Tootejuhid saavad neid tuletatud tooteatribuute iga toote puhul muuta, et need vastaksid konkreetsetele ärinõuetele.</span><span class="sxs-lookup"><span data-stu-id="945e6-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


