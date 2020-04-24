---
title: Toote konfiguratsioonimudeli loomine
description: See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente).
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9577005fb4fc016670713c36e40263ff30030caf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203752"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="a0563-103">Toote konfiguratsioonimudeli loomine</span><span class="sxs-lookup"><span data-stu-id="a0563-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0563-104">See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente).</span><span class="sxs-lookup"><span data-stu-id="a0563-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="a0563-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="a0563-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="a0563-106">Tootemudeli loomine</span><span class="sxs-lookup"><span data-stu-id="a0563-106">Create a product model</span></span>
1. <span data-ttu-id="a0563-107">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="a0563-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a0563-108">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="a0563-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="a0563-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="a0563-109">Click New.</span></span>
4. <span data-ttu-id="a0563-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a0563-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a0563-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="a0563-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a0563-112">Valige suvand väljal Lahendaja strateegia.</span><span class="sxs-lookup"><span data-stu-id="a0563-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="a0563-113">Lahendaja strateegia määrab, kuidas piiranguid piirangupõhises toote konfiguratsioonimudelis töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="a0563-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="a0563-114">See valik võib mõjutada toote konfiguratsioonimudeli toimimist.</span><span class="sxs-lookup"><span data-stu-id="a0563-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="a0563-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a0563-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a0563-116">Juurkomponent tähistab toote konfiguratsioonimudelit, kuid seda saab kasutada ka muudes tootemudelites.</span><span class="sxs-lookup"><span data-stu-id="a0563-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="a0563-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a0563-117">Click OK.</span></span>
9. <span data-ttu-id="a0563-118">Valige suvand väljal Taaskasuta konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="a0563-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="a0563-119">Kui konfiguratsioonide taaskasutuse parameetri sätteks on määratud Jah, kontrollib süsteem identseid konfiguratsioone pärast iga konfiguratsiooniseanssi ja kasutab uuesti, kui leitakse täpne vaste.</span><span class="sxs-lookup"><span data-stu-id="a0563-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="a0563-120">Atribuutide lisamine</span><span class="sxs-lookup"><span data-stu-id="a0563-120">Add attributes</span></span>
1. <span data-ttu-id="a0563-121">Laiendage jaotist Atribuudid.</span><span class="sxs-lookup"><span data-stu-id="a0563-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="a0563-122">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a0563-122">Click Add.</span></span>
3. <span data-ttu-id="a0563-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a0563-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a0563-124">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a0563-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a0563-125">Sisestage väärtus väljale Lahendaja nimi.</span><span class="sxs-lookup"><span data-stu-id="a0563-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="a0563-126">Lahendaja nime kasutab toote konfiguraatori piirangu lahendaja.</span><span class="sxs-lookup"><span data-stu-id="a0563-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="a0563-127">See ei tohi sisaldada tühikuid ega erimärke, v.a _ (allkriips).</span><span class="sxs-lookup"><span data-stu-id="a0563-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="a0563-128">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="a0563-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a0563-129">Kirjeldav tekst kuvatakse konfiguratsiooni kasutajale ja seetõttu võib sellest õige atribuudi väärtuse valimisel abi olla.</span><span class="sxs-lookup"><span data-stu-id="a0563-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="a0563-130">Sisestage või valige väärtus väljal Atribuudi tüüp.</span><span class="sxs-lookup"><span data-stu-id="a0563-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="a0563-131">Atribuudi tüüp määrab, millised väärtused on atribuudi jaoks saadaval.</span><span class="sxs-lookup"><span data-stu-id="a0563-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="a0563-132">Märkige ruut Lisa taaskasutusse.</span><span class="sxs-lookup"><span data-stu-id="a0563-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="a0563-133">See valik on saadaval ainult siis, kui valitakse suvand Taaskasuta konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="a0563-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="a0563-134">Atribuudi lisamine taaskasutuse märkeruutu tähendab, et seda atribuuti arvestatakse, kui süsteem täpset vastet otsib.</span><span class="sxs-lookup"><span data-stu-id="a0563-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="a0563-135">Alamkomponentide lisamine</span><span class="sxs-lookup"><span data-stu-id="a0563-135">Add subcomponents</span></span>
1. <span data-ttu-id="a0563-136">Laiendage jaotist Alamkomponendid.</span><span class="sxs-lookup"><span data-stu-id="a0563-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="a0563-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a0563-137">Click Add.</span></span>
3. <span data-ttu-id="a0563-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a0563-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a0563-139">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a0563-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a0563-140">Sisestage väärtus väljale Lahendaja nimi.</span><span class="sxs-lookup"><span data-stu-id="a0563-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="a0563-141">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="a0563-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="a0563-142">Valige või sisestage väärtus väljal Komponent.</span><span class="sxs-lookup"><span data-stu-id="a0563-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="a0563-143">Iga alamkomponent peab viitama komponendi definitsioonile.</span><span class="sxs-lookup"><span data-stu-id="a0563-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="a0563-144">See mudel toetab taaskasutatavaid komponente ja tagab, et kui komponent on määratletud, saab seda kasutada paljudes tootemudelites.</span><span class="sxs-lookup"><span data-stu-id="a0563-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="a0563-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a0563-145">Click Save.</span></span>
9. <span data-ttu-id="a0563-146">Klõpsake valikut Koosluse rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="a0563-146">Click BOM line details.</span></span>
    * <span data-ttu-id="a0563-147">Koosluse rea üksikasjade vorm võimaldab kasutajal valida alamkomponendile vajalikud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="a0563-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="a0563-148">Igale atribuudile saab anda püsiväärtuse või selle saab vastendada atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="a0563-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="a0563-149">Atribuudiga vastendamisel saab koosluse rea atribuut erinevad väärtused, olenevalt konfiguratsiooni valikust.</span><span class="sxs-lookup"><span data-stu-id="a0563-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="a0563-150">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a0563-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a0563-151">Iga alamkomponent tähistab piirangupõhise konfiguratsioonitehnoloogiaga konfigureeritavat tooteetaloni.</span><span class="sxs-lookup"><span data-stu-id="a0563-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="a0563-152">Viidatakse kaubakoodi kaudu.</span><span class="sxs-lookup"><span data-stu-id="a0563-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="a0563-153">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="a0563-153">Select the Set check box.</span></span>
12. <span data-ttu-id="a0563-154">Tehke väljal Arvutus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a0563-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="a0563-155">Arvutamise suvandi seadistamine tagab, et toode kaasatakse toote kuluarvutusse.</span><span class="sxs-lookup"><span data-stu-id="a0563-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="a0563-156">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="a0563-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="a0563-157">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="a0563-157">Select the Set check box.</span></span>
15. <span data-ttu-id="a0563-158">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="a0563-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a0563-159">Koguse väli määratleb, kui palju seda toodet konfigureeritud tootes tarbitakse.</span><span class="sxs-lookup"><span data-stu-id="a0563-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="a0563-160">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="a0563-160">Select the Set check box.</span></span>
17. <span data-ttu-id="a0563-161">Sisestage number väljale Seeria kohta.</span><span class="sxs-lookup"><span data-stu-id="a0563-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="a0563-162">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a0563-162">Click OK.</span></span>

