---
title: Tootekategooria haldamine ja loomine
description: "Selles teemas kirjeldatakse Retaili tootekategooriate halduskogemuse täiustusi. Need täiustused võimaldavad tootejuhtidel seostada Retaili tootehierarhia ja väljastatud toote üksikasjad."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: et-ee
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="e46b5-104">Tootekategooria haldamine ja loomine</span><span class="sxs-lookup"><span data-stu-id="e46b5-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="e46b5-105">Retaili tootekategooriates tehtud täiustused võimaldavad tootejuhtidel seostada Retaili tootehierarhia ja väljastatud toote üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e46b5-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="e46b5-106">Nende täiustuste kuvamiseks tehke tööruumis **Kategooria ja toote haldus** valik **Retaili tootehierarhia** lehe **Uus Retaili tootekategooria struktuur** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e46b5-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="e46b5-107">Varasemates väljaannetes olid toote atribuudid jagatud kohaldatava ulatuse alusel toote põhiatribuutideks ja jaetoote atribuutideks.</span><span class="sxs-lookup"><span data-stu-id="e46b5-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="e46b5-108">Jaetoote atribuudid olid *globaalsed*.</span><span class="sxs-lookup"><span data-stu-id="e46b5-108">Retail product properties were *global*.</span></span> <span data-ttu-id="e46b5-109">Teisisõnu: antud tooteatribuudi puhul jagatakse sama väärtust kõigi juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="e46b5-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="e46b5-110">Toote põhiatribuudid olid *juriidilise isiku põhised*.</span><span class="sxs-lookup"><span data-stu-id="e46b5-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="e46b5-111">Teisisõnu: antud tooteatribuut võib juriidiliste isikute lõikes erineda, tuginedes eraldi ettevõtete nõuetele.</span><span class="sxs-lookup"><span data-stu-id="e46b5-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="e46b5-112">Nende jaetoote kategooria tooteatribuutide täiustustega jätkame väljade eraldamist nende kohalduvuse alusel rühmas, peegeldades väljastatud toote üksikasjade vormi struktuuri.</span><span class="sxs-lookup"><span data-stu-id="e46b5-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="e46b5-113">Saate valida juriidilise isiku põhiste atribuutide haldamise kõigi juriidiliste isikute lõikes ja konkreetse juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="e46b5-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="e46b5-114">Valige lihtsalt **Kuva/redigeeri kõigi juriidiliste isikute puhul** või **Kuva/redigeeri konkreetse juriidilise isiku puhul**, nagu vaja.</span><span class="sxs-lookup"><span data-stu-id="e46b5-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="e46b5-115">Tootejuhid saavad määratleda ka vaikeväärtusi täiendavale tooteatribuutide kogumile eraldi kategooria tasandil.</span><span class="sxs-lookup"><span data-stu-id="e46b5-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="e46b5-116">Toode tuletab need atribuudiväärtused seose põhjal kategooriaga toote loomise ajal.</span><span class="sxs-lookup"><span data-stu-id="e46b5-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="e46b5-117">Valige atribuudid toodete värskendamiseks jaetoote kategooria vormilt</span><span class="sxs-lookup"><span data-stu-id="e46b5-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="e46b5-118">Võite kasutada loogilisi rühmitusatribuute valimiseks, millised värskendatud toote atribuudid tuleks seotud toodetele tõugata.</span><span class="sxs-lookup"><span data-stu-id="e46b5-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="e46b5-119">Tootejuhid saavad neid tuletatud tooteatribuute iga toote puhul muuta, et need vastaksid konkreetsetele ärinõuetele.</span><span class="sxs-lookup"><span data-stu-id="e46b5-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

