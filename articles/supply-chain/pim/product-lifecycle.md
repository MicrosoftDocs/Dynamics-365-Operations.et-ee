---
title: Toote töötsükli olekute ülevaade
description: Toote elutsükli olek dokumenteerib väljastatud toote või tootevariandi elutsükli oleku.
author: cvocph
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: b5b0ceb1926de6efda239fdbc69fb36a9d4b28e0
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934836"
---
# <a name="product-lifecycle-state-overview"></a><span data-ttu-id="94f39-103">Toote töötsükli olekute ülevaade</span><span class="sxs-lookup"><span data-stu-id="94f39-103">Product lifecycle state overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94f39-104">Toote elutsükli olek dokumenteerib väljastatud toote või tootevariandi elutsükli oleku.</span><span class="sxs-lookup"><span data-stu-id="94f39-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="94f39-105">Toote elutsükli olekud määratleb kasutaja, tavaliselt tootejuht või tooteetaloni andmehaldur.</span><span class="sxs-lookup"><span data-stu-id="94f39-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="94f39-106">Kindel elutsükli olek võib mõjutada konkreetseid äriprotsesse, näiteks koondplaneerimist.</span><span class="sxs-lookup"><span data-stu-id="94f39-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   

<span data-ttu-id="94f39-107">Väljastatud toote või tootevariandi saab seostada toote elutsükli olekuga, mis dokumenteerib, millises elutsükli olekus konkreetne toode või variant praegu on.</span><span class="sxs-lookup"><span data-stu-id="94f39-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="94f39-108">Saate määratleda mis tahes arvu toote elutsükleid, määrates oleku nime ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="94f39-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="94f39-109">Saate valida ühe elutsükli oleku uute väljastatud toodete vaikeolekuks.</span><span class="sxs-lookup"><span data-stu-id="94f39-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="94f39-110">Väljastatud tootevariandid pärivad oma toote elutsükli oleku loomise ajal oma väljastatud tooteetalonilt.</span><span class="sxs-lookup"><span data-stu-id="94f39-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="94f39-111">Väljastatud tooteetaloni elutsükli oleku muutmisel saate värskendada kõik sama algolekuga variandid.</span><span class="sxs-lookup"><span data-stu-id="94f39-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="94f39-112">Uue toote elutsükli oleku loomine</span><span class="sxs-lookup"><span data-stu-id="94f39-112">Create a new product lifecycle state</span></span> 

- <span data-ttu-id="94f39-113">Uue toote elutsükli oleku loomiseks esitage või lugege tegevusejuhist **Uue toote elutsükli oleku loomine**.</span><span class="sxs-lookup"><span data-stu-id="94f39-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="94f39-114">Toote elutsükli vaikeoleku loomiseks esitage või lugege tegevusejuhist **Toote elutsükli vaikeoleku loomine**.</span><span class="sxs-lookup"><span data-stu-id="94f39-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="94f39-115">Toote elutsükli olekute seostamine väljastatud toodetega</span><span class="sxs-lookup"><span data-stu-id="94f39-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="94f39-116">Toote elutsükli oleku seostamiseks väljastatud toodete või tootevariantidega on mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="94f39-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="94f39-117">Uue väljastatud toote loomisel määratakse sellele automaatselt vaikimisi **Toote elutsükli olek**.</span><span class="sxs-lookup"><span data-stu-id="94f39-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="94f39-118">Toote väljastamisel juriidilisele isikule määratakse sellele automaatselt vaikimisi **Toote elutsükli olek**.</span><span class="sxs-lookup"><span data-stu-id="94f39-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="94f39-119">Tootevariandi väljastamisel juriidilisele isikule määratakse uuele variandile automaatselt selles juriidilises isikus väljasatud tooteetaloniga seostatud **Toote elutsükli olek**.</span><span class="sxs-lookup"><span data-stu-id="94f39-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="94f39-120">Toote elutsükli oleku käsitsi värskendamiseks on järgmised võimalused.</span><span class="sxs-lookup"><span data-stu-id="94f39-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="94f39-121">Loendileht **Väljastatud tooted** või **Üksikasjavaade**.</span><span class="sxs-lookup"><span data-stu-id="94f39-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="94f39-122">Loendileht **Väljastatud tootevariandid** või **Üksikasjavaade**.</span><span class="sxs-lookup"><span data-stu-id="94f39-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="94f39-123">Saate leida aegunud tooted või tootevariandid nõudluse põhjal ja seostada need elutsükli olekuga.</span><span class="sxs-lookup"><span data-stu-id="94f39-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="94f39-124">Üksikasjalikku teavet toote elutsükli olekute seostaimseks esitage või lugege kaht järgmist tegevusejuhist.</span><span class="sxs-lookup"><span data-stu-id="94f39-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="94f39-125">Toote elutsükli oleku seostamiseks väljastatud tooteetaloniga esitage või lugege tegevusejuhist **Toote elutsükli oleku määramine väljastatud tooteetalonile**.</span><span class="sxs-lookup"><span data-stu-id="94f39-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="94f39-126">Toote elutsükli oleku seostamiseks väljastatud tootega esitage või lugege tegevusejuhist **Toote elutsükli oleku määramine väljastatud tootele**.</span><span class="sxs-lookup"><span data-stu-id="94f39-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="94f39-127">Mõju koondplaneerimisele</span><span class="sxs-lookup"><span data-stu-id="94f39-127">Impact on master planning</span></span> 

<span data-ttu-id="94f39-128">Toote elutsükli olekul on ainult üks juhtlipp: **On planeerimiseks aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="94f39-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="94f39-129">Vaikimisi on selle sätteks kõigi loodud toote elutsükli olekut puhul **Jah**, kuid selle saab muuta sättele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="94f39-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="94f39-130">Kui valitud on säte **Ei**, on seostatud väljastatud tooted või väljastatud tootevariandid:</span><span class="sxs-lookup"><span data-stu-id="94f39-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="94f39-131">välistatud koondplaneerimisest;</span><span class="sxs-lookup"><span data-stu-id="94f39-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="94f39-132">välistatud koosluse taseme arvutusest.</span><span class="sxs-lookup"><span data-stu-id="94f39-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="94f39-133">Täpsema teabe saamiseks selle kohta, kuidas kasutada toote elutsükli olekut toodete välistamiseks koondplaneerimisest ja koosluse taseme arvutustest, esitage või lugege tegevusejuhist **Toote elutsükli oleku loomine toote välistamiseks koondplaneerimisest**.</span><span class="sxs-lookup"><span data-stu-id="94f39-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="94f39-134">Jõudluse huvides on väga soovitatav seostada kõik aegunud väljastatud tooted või tootevariandid, eriti kui töötate ühekordselt kasutatavate toote konfiguratsioonivariantidega, toote elutsükli olekuga, mis on koondplaneerimise jaoks inaktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="94f39-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  

## <a name="default-migration-import-and-export"></a><span data-ttu-id="94f39-135">Migratsiooni, impordi ja ekspordi vaikesätted</span><span class="sxs-lookup"><span data-stu-id="94f39-135">Default migration, import, and export</span></span> 

<span data-ttu-id="94f39-136">Andmeüksused toetavad toote elutsükli olekuid ja elutsükli oleku saab määrata kas väljastatud toote andmeüksuste või väljastatud variandi andmeüksuse kaudu muutuvaks.</span><span class="sxs-lookup"><span data-stu-id="94f39-136">The product lifecycle states are supported by data entities, and the lifecycle state can be set to a variable state through either the released product data entity or the released variant data entity.</span></span>

## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="94f39-137">Aegunud toodete ja tootevariantide leidmine</span><span class="sxs-lookup"><span data-stu-id="94f39-137">Find obsolete products and products variants</span></span> 

<span data-ttu-id="94f39-138">Saate käivitada simulatsioonanalüüsi aegunud väljastatud toodete või tootevariantide leidmiseks ning seejärel nende toote elutsükli oleku värskendada.</span><span class="sxs-lookup"><span data-stu-id="94f39-138">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="94f39-139">Aegunud toodete leidmiseks esitage ja lugege tegevusejuhist **Aegunud tootevariantide leidmine ja toote elutsükli oleku määramine**.</span><span class="sxs-lookup"><span data-stu-id="94f39-139">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="94f39-140">Tegevusejuhis näitab, kuidas leida aegunud väljastatud tooteid või tootevariante ja kuidas seostada toote elutsükli olek aegunud toodetega.</span><span class="sxs-lookup"><span data-stu-id="94f39-140">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="94f39-141">See näitab ka, kuidas vaadata simulatsiooni tulemusi ja hinnata, kui palju tooteid ning tootevariante uue toote elutsükli olekuga seostatakse, kui värskendus käivitatakse ilma simulatsioonita.</span><span class="sxs-lookup"><span data-stu-id="94f39-141">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

<span data-ttu-id="94f39-142">Käivitades analüüsi simulatsioonirežiimis, kuvatakse aegununa tuvastatud tooted ja tootevariandid kindlal vormil, kus neid saab hõlpsasti üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="94f39-142">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="94f39-143">Analüüs otsib kandeid ja konkreetseid koondandmeid, et tuvastada tooteid, millel puuduvad muutuval perioodil nõudlus ja koondandmed, mis võivad nõudlust põhjustada.</span><span class="sxs-lookup"><span data-stu-id="94f39-143">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="94f39-144">Uued väljastatud tooted muutuval perioodil saab analüüsist välja jätta.</span><span class="sxs-lookup"><span data-stu-id="94f39-144">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="94f39-145">Kui analüüsi simulatsioon tagastab oodatud tulemuse, saab kasutaja käivitada analüüsi ja määrata uue toote elutsükli oleku kõigile toodetele, mille analüüs tuvastas aegununa.</span><span class="sxs-lookup"><span data-stu-id="94f39-145">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  

> [!NOTE]
> <span data-ttu-id="94f39-146">Pange tähele, et kogu analüüs ja kõik värskendused tuleb teha samas juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="94f39-146">Note that all analysis and updates must be done within the same legal entity.</span></span>  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="94f39-147">Väljastatud toodete ja tootevariantide valimise ja värskendamise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="94f39-147">Criteria to select and update released products or product variants</span></span> 

<span data-ttu-id="94f39-148">Väljastatud toodete ja tootevariantide valimiseks ja värskendamiseks saate kasutada järgmisi kriteeriume.</span><span class="sxs-lookup"><span data-stu-id="94f39-148">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="94f39-149">Toote või tootevariandi toote elutsükli olek peab erinema uuest soovitud olekust.</span><span class="sxs-lookup"><span data-stu-id="94f39-149">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="94f39-150">Toode või tootevariant loodi mõni päev tagasi valiku dialoogiboksis sisestatud päevade arvu alusel.</span><span class="sxs-lookup"><span data-stu-id="94f39-150">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="94f39-151">Toote või tootevariandi puhul ei ole avatud tootetellimusi (= olek < lõpetatud).</span><span class="sxs-lookup"><span data-stu-id="94f39-151">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="94f39-152">Toote või tootevariandi pole avatud varude kandeid (= väljastamise olek valikult ReservPhysical valikule QuotationIssue või vastuvõtmise olek valikult Registreeritud valikule QuotationReceipt).</span><span class="sxs-lookup"><span data-stu-id="94f39-152">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="94f39-153">Toote või tootevariandi puhul pole viimaste päevade jooksul ühtki varude kandeid.</span><span class="sxs-lookup"><span data-stu-id="94f39-153">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="94f39-154">Toote või tootevariandi puhul puudub tulevane nõudlus või tarneprognoos.</span><span class="sxs-lookup"><span data-stu-id="94f39-154">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="94f39-155">Toote või tootevariandi puhul pole kauba laovarudele minimaalset varude taset määratud.</span><span class="sxs-lookup"><span data-stu-id="94f39-155">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="94f39-156">Toote või tootevariandi puhul pole aktiivset fikseeritud koguse kanban-reeglit.</span><span class="sxs-lookup"><span data-stu-id="94f39-156">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="94f39-157">Toote või tootevariandi puhul pole teenuse tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="94f39-157">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="94f39-158">Toote või tootetellimuse puhul pole aktiivseid ega tulevasi müüke või ostutellimuse ridu.</span><span class="sxs-lookup"><span data-stu-id="94f39-158">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="94f39-159">Toote või tootevarianti ei kasutata koosluses, mis on seostatud planeerimiseks aktiivse toote või tootevariandi puhul mitteaegunud kinnitatud koosluse versiooniga.</span><span class="sxs-lookup"><span data-stu-id="94f39-159">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94f39-160">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="94f39-160">Related topics</span></span>

-  [<span data-ttu-id="94f39-161">Toote töötsükli uue oleku loomine</span><span class="sxs-lookup"><span data-stu-id="94f39-161">Create a new product lifecycle state</span></span>](tasks/new-product-lifecycle-state.md)
-  [<span data-ttu-id="94f39-162">Toote töötsükli vaikeoleku loomine</span><span class="sxs-lookup"><span data-stu-id="94f39-162">Create a default product lifecycle state</span></span>](tasks/default-product-lifecycle-state.md)
-  [<span data-ttu-id="94f39-163">Toote elutsükli oleku määramine väljastatud tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="94f39-163">Assign a product lifecycle state to a released product master</span></span>](tasks/product-lifecycle-state-released-product-master.md)
-  [<span data-ttu-id="94f39-164">Toote elutsükli oleku määramine väljastatud tootele</span><span class="sxs-lookup"><span data-stu-id="94f39-164">Assign a product lifecycle state to a released product</span></span>](tasks/product-lifecycle-state-released-product.md)
-  [<span data-ttu-id="94f39-165">Aegunud tootevariantide leidmine ja neile toote elutsükli oleku määramine</span><span class="sxs-lookup"><span data-stu-id="94f39-165">Find obsolete product variants and assign a product lifecycle state</span></span>](tasks/obsolete-product-variants.md)
-  [<span data-ttu-id="94f39-166">Toote elutsükli oleku loomine toodete välistamiseks koondplaneerimisest</span><span class="sxs-lookup"><span data-stu-id="94f39-166">Create a product lifecycle state to exclude products from Master planning</span></span>](tasks/exclude-products-master-planning.md)
