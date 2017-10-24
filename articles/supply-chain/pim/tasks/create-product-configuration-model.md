--- 
title: Toote konfiguratsioonimudeli loomine
description: "See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente)."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 866a4f29723e10eb0a1e1be86d6d4f6da8a69b1c
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="1f57d-103">Toote konfiguratsioonimudeli loomine</span><span class="sxs-lookup"><span data-stu-id="1f57d-103">Create a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f57d-104">See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente).</span><span class="sxs-lookup"><span data-stu-id="1f57d-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="1f57d-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="1f57d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="1f57d-106">Tootemudeli loomine</span><span class="sxs-lookup"><span data-stu-id="1f57d-106">Create a product model</span></span>
1. <span data-ttu-id="1f57d-107">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="1f57d-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="1f57d-108">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="1f57d-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="1f57d-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="1f57d-109">Click New.</span></span>
4. <span data-ttu-id="1f57d-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1f57d-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1f57d-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="1f57d-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="1f57d-112">Valige suvand väljal Lahendaja strateegia.</span><span class="sxs-lookup"><span data-stu-id="1f57d-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="1f57d-113">Lahendaja strateegia määrab, kuidas piiranguid piirangupõhises toote konfiguratsioonimudelis töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="1f57d-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="1f57d-114">See valik võib mõjutada toote konfiguratsioonimudeli toimimist.</span><span class="sxs-lookup"><span data-stu-id="1f57d-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="1f57d-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1f57d-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1f57d-116">Juurkomponent tähistab toote konfiguratsioonimudelit, kuid seda saab kasutada ka muudes tootemudelites.</span><span class="sxs-lookup"><span data-stu-id="1f57d-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="1f57d-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1f57d-117">Click OK.</span></span>
9. <span data-ttu-id="1f57d-118">Valige suvand väljal Taaskasuta konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="1f57d-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="1f57d-119">Kui konfiguratsioonide taaskasutuse parameetri sätteks on määratud Jah, kontrollib süsteem identseid konfiguratsioone pärast iga konfiguratsiooniseanssi ja kasutab uuesti, kui leitakse täpne vaste.</span><span class="sxs-lookup"><span data-stu-id="1f57d-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="1f57d-120">Atribuutide lisamine</span><span class="sxs-lookup"><span data-stu-id="1f57d-120">Add attributes</span></span>
1. <span data-ttu-id="1f57d-121">Laiendage jaotist Atribuudid.</span><span class="sxs-lookup"><span data-stu-id="1f57d-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="1f57d-122">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1f57d-122">Click Add.</span></span>
3. <span data-ttu-id="1f57d-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1f57d-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1f57d-124">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1f57d-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1f57d-125">Sisestage väärtus väljale Lahendaja nimi.</span><span class="sxs-lookup"><span data-stu-id="1f57d-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="1f57d-126">Lahendaja nime kasutab toote konfiguraatori piirangu lahendaja.</span><span class="sxs-lookup"><span data-stu-id="1f57d-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="1f57d-127">See ei tohi sisaldada tühikuid ega erimärke, v.a _ (allkriips).</span><span class="sxs-lookup"><span data-stu-id="1f57d-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="1f57d-128">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="1f57d-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1f57d-129">Kirjeldav tekst kuvatakse konfiguratsiooni kasutajale ja seetõttu võib sellest õige atribuudi väärtuse valimisel abi olla.</span><span class="sxs-lookup"><span data-stu-id="1f57d-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="1f57d-130">Sisestage või valige väärtus väljal Atribuudi tüüp.</span><span class="sxs-lookup"><span data-stu-id="1f57d-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="1f57d-131">Atribuudi tüüp määrab, millised väärtused on atribuudi jaoks saadaval.</span><span class="sxs-lookup"><span data-stu-id="1f57d-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="1f57d-132">Märkige ruut Lisa taaskasutusse.</span><span class="sxs-lookup"><span data-stu-id="1f57d-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="1f57d-133">See valik on saadaval ainult siis, kui valitakse suvand Taaskasuta konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="1f57d-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="1f57d-134">Atribuudi lisamine taaskasutuse märkeruutu tähendab, et seda atribuuti arvestatakse, kui süsteem täpset vastet otsib.</span><span class="sxs-lookup"><span data-stu-id="1f57d-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="1f57d-135">Alamkomponentide lisamine</span><span class="sxs-lookup"><span data-stu-id="1f57d-135">Add subcomponents</span></span>
1. <span data-ttu-id="1f57d-136">Laiendage jaotist Alamkomponendid.</span><span class="sxs-lookup"><span data-stu-id="1f57d-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="1f57d-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1f57d-137">Click Add.</span></span>
3. <span data-ttu-id="1f57d-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1f57d-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1f57d-139">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1f57d-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1f57d-140">Sisestage väärtus väljale Lahendaja nimi.</span><span class="sxs-lookup"><span data-stu-id="1f57d-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="1f57d-141">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="1f57d-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="1f57d-142">Valige või sisestage väärtus väljal Komponent.</span><span class="sxs-lookup"><span data-stu-id="1f57d-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="1f57d-143">Iga alamkomponent peab viitama komponendi definitsioonile.</span><span class="sxs-lookup"><span data-stu-id="1f57d-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="1f57d-144">See mudel toetab taaskasutatavaid komponente ja tagab, et kui komponent on määratletud, saab seda kasutada paljudes tootemudelites.</span><span class="sxs-lookup"><span data-stu-id="1f57d-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="1f57d-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1f57d-145">Click Save.</span></span>
9. <span data-ttu-id="1f57d-146">Klõpsake valikut Koosluse rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1f57d-146">Click BOM line details.</span></span>
    * <span data-ttu-id="1f57d-147">Koosluse rea üksikasjade vorm võimaldab kasutajal valida alamkomponendile vajalikud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="1f57d-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="1f57d-148">Igale atribuudile saab anda püsiväärtuse või selle saab vastendada atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="1f57d-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="1f57d-149">Atribuudiga vastendamisel saab koosluse rea atribuut erinevad väärtused, olenevalt konfiguratsiooni valikust.</span><span class="sxs-lookup"><span data-stu-id="1f57d-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="1f57d-150">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="1f57d-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="1f57d-151">Iga alamkomponent tähistab piirangupõhise konfiguratsioonitehnoloogiaga konfigureeritavat tooteetaloni.</span><span class="sxs-lookup"><span data-stu-id="1f57d-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="1f57d-152">Viidatakse kaubakoodi kaudu.</span><span class="sxs-lookup"><span data-stu-id="1f57d-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="1f57d-153">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="1f57d-153">Select the Set check box.</span></span>
12. <span data-ttu-id="1f57d-154">Tehke väljal Arvutus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="1f57d-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="1f57d-155">Arvutamise suvandi seadistamine tagab, et toode kaasatakse toote kuluarvutusse.</span><span class="sxs-lookup"><span data-stu-id="1f57d-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="1f57d-156">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="1f57d-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="1f57d-157">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="1f57d-157">Select the Set check box.</span></span>
15. <span data-ttu-id="1f57d-158">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="1f57d-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1f57d-159">Koguse väli määratleb, kui palju seda toodet konfigureeritud tootes tarbitakse.</span><span class="sxs-lookup"><span data-stu-id="1f57d-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="1f57d-160">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="1f57d-160">Select the Set check box.</span></span>
17. <span data-ttu-id="1f57d-161">Sisestage number väljale Seeria kohta.</span><span class="sxs-lookup"><span data-stu-id="1f57d-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="1f57d-162">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1f57d-162">Click OK.</span></span>


