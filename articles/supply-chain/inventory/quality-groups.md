---
title: Üksuse kvaliteedigrupid
description: Selles teemas kirjeldatakse, kuidas kauba kvaliteedigruppe kasutada ja luua toodete loogiliseks rühmitamiseks, et neid saaks kvaliteettellimuste automaatseks genereerimiseks määrata kvaliteediseostele.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022248"
---
# <a name="item-quality-groups"></a><span data-ttu-id="e69e0-103">Üksuse kvaliteedigrupid</span><span class="sxs-lookup"><span data-stu-id="e69e0-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e69e0-104">Kvaliteedigrupp tähistab kaupade üldisi testimisnõudeid.</span><span class="sxs-lookup"><span data-stu-id="e69e0-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="e69e0-105">Selles teemas kirjeldatakse, kuidas kauba kvaliteedigruppe kasutada ja luua toodete loogiliseks rühmitamiseks, et neid saaks kvaliteettellimuste automaatseks genereerimiseks määrata kvaliteediseostele.</span><span class="sxs-lookup"><span data-stu-id="e69e0-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="e69e0-106">Kvaliteedigrupile määratud kauba või kaubale määratud kvaliteedigruppide seadistamiseks, muutmiseks ja vaatamiseks minge **Varude haldus \> Seaded \> Kvaliteedigrupid**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="e69e0-107">Pärast katsenõuete määratlemist lehel **Katsegrupid** saate määratleda reeglid kvaliteettellimuste automaatseks koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="e69e0-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="e69e0-108">Protsessi hõlbustamiseks ei määratleta reegleid üksikutele kaupadele.</span><span class="sxs-lookup"><span data-stu-id="e69e0-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="e69e0-109">Selle asemel määratletakse reeglid kvaliteedigrupile, kasutades lehte **Kvaliteediseosed**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="e69e0-110">Kauba kvaliteedigrupi näide</span><span class="sxs-lookup"><span data-stu-id="e69e0-110">Example of an item quality group</span></span>

<span data-ttu-id="e69e0-111">Tootmisettevõte ostab mitmesuguseid ühesuguste sissetulekukontrolli katsenõuetega toormaterjale.</span><span class="sxs-lookup"><span data-stu-id="e69e0-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="e69e0-112">Seega määratleb ettevõte kvaliteedigrupi ja määrab sellele grupile toormaterjaliga seotud kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="e69e0-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="e69e0-113">Hiljem ostab ettevõte uut tüüpi toormaterjali, millel on samad katsenõuded.</span><span class="sxs-lookup"><span data-stu-id="e69e0-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="e69e0-114">Selle asemel, et seadistada uuele materjalile uued katsenõuded, lisab ettevõte uue materjali kaubakoodi olemasolevasse kvaliteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="e69e0-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="e69e0-115">Sama tootmisettevõte toodab ka ühesuguste tootmisalaste testimisnõuetega kaupu ja lähetab ühesuguste nõuetega kaubad lähetuseelsete testide tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="e69e0-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="e69e0-116">Ettevõte määratleb kaks täiendavat kvaliteedigruppi ja määrab seejärel igale grupile sobivad kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="e69e0-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="e69e0-117">Kvaliteedigrupi loomine</span><span class="sxs-lookup"><span data-stu-id="e69e0-117">Create a quality group</span></span>

<span data-ttu-id="e69e0-118">Kvaliteedigrupi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e69e0-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="e69e0-119">Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Kvaliteedigrupid**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="e69e0-120">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="e69e0-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e69e0-121">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="e69e0-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e69e0-122">**Kvaliteedigrupp** – Sisestage kvaliteedigrupi kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="e69e0-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="e69e0-123">**Kirjeldus** – Sisestage kvaliteedigrupi detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e69e0-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="e69e0-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e69e0-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="e69e0-125">Käsitsi kaupade lisamine kvaliteedigruppi</span><span class="sxs-lookup"><span data-stu-id="e69e0-125">Manually add items to a quality group</span></span>

<span data-ttu-id="e69e0-126">Kaupade käsitsi lisamiseks kvaliteedigruppi järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e69e0-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="e69e0-127">Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Kvaliteedigrupid**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="e69e0-128">Valige kvaliteedigrupp, millele soovite kaupu lisada.</span><span class="sxs-lookup"><span data-stu-id="e69e0-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="e69e0-129">Toimingupaanil valige käsk **Kaubad**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="e69e0-130">Ruudustiku rea lisamiseks valige **Kaubad kvaliteedigrupis** lehekülje tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e69e0-131">Seejärel seadistage uue rea jaoks välja **Kaubakood** väärtuseks kaubakood, mille soovite lisada.</span><span class="sxs-lookup"><span data-stu-id="e69e0-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="e69e0-132">Korrake eelmist etappi iga lisakauba puhul, mille lisama peate.</span><span class="sxs-lookup"><span data-stu-id="e69e0-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="e69e0-133">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="e69e0-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="e69e0-134">Mitme kauba lisamine kvaliteedigruppi</span><span class="sxs-lookup"><span data-stu-id="e69e0-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="e69e0-135">Mitme kauba lisamiseks kvaliteedigruppi järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e69e0-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="e69e0-136">Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Kvaliteedigrupid**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="e69e0-137">Looge või valige kvaliteedigrupp, millele soovite kaupu lisada.</span><span class="sxs-lookup"><span data-stu-id="e69e0-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="e69e0-138">Toimingupaanil valige käsk **Lisa kaubad**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="e69e0-139">Sisestage dialoogiboksis **Päring** lisatavate kaupade filtrikriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="e69e0-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="e69e0-140">Näiteks võite filtreerida kõiki kaupu konkreetses kaubagrupis.</span><span class="sxs-lookup"><span data-stu-id="e69e0-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="e69e0-141">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-141">Select **OK**.</span></span>
1. <span data-ttu-id="e69e0-142">Dialoogiboksis **Lisa kaupu** kuvatakse ruudustikus kõik päringuga sobivad kaubad.</span><span class="sxs-lookup"><span data-stu-id="e69e0-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="e69e0-143">Tulemuste ülevaatamine.</span><span class="sxs-lookup"><span data-stu-id="e69e0-143">Review the results.</span></span>

    <span data-ttu-id="e69e0-144">Kui muudatused on nõutavad, valige suvand **Vali**, et naasta dialoogiboksi **Päring** ja korrigeerida oma päringut.</span><span class="sxs-lookup"><span data-stu-id="e69e0-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="e69e0-145">Kui tulemused sisaldavad kõiki kaupu, mida soovite lisada, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="e69e0-146">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e69e0-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="e69e0-147">Kauba käsitsi seostamine kvaliteedigrupiga</span><span class="sxs-lookup"><span data-stu-id="e69e0-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="e69e0-148">Kaupade käsitsi kvaliteedigrupiga seostamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e69e0-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="e69e0-149">Avage **Varude haldus \> Seades \> Kvaliteedikontroll \> Kauba kvaliteedigrupid**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="e69e0-150">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="e69e0-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e69e0-151">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="e69e0-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e69e0-152">**Kaubakood** – Valige lisamiseks kaubakood.</span><span class="sxs-lookup"><span data-stu-id="e69e0-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="e69e0-153">**Kvaliteedigrupp** – Valige kaubale määratav kvaliteedigrupp.</span><span class="sxs-lookup"><span data-stu-id="e69e0-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="e69e0-154">Korrake eelmist sammu iga lisakauba ja kvaliteedigrupi kombinatsiooni puhul, mida tuleb lisada.</span><span class="sxs-lookup"><span data-stu-id="e69e0-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="e69e0-155">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="e69e0-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="e69e0-156">Kvaliteedigrupi käsitsi lisamine lehelt Väljastatud tooted</span><span class="sxs-lookup"><span data-stu-id="e69e0-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="e69e0-157">**Väljastatud tooted** lehelt käsitsi kvaliteedigrupi lisamiseks, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e69e0-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="e69e0-158">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e69e0-159">Valige toode, millele soovite kvaliteedigrupi määrata.</span><span class="sxs-lookup"><span data-stu-id="e69e0-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="e69e0-160">Toimingipaani **Varude haldus** vahekaardi **Kvaliteet** grupis, valige **kauba kvaliteedigrupid**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="e69e0-161">Ruudustiku rea lisamiseks valige **Kaubad kvaliteedigrupis** lehekülje tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e69e0-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e69e0-162">Seejärel määrake uue rea jaoks väli **Kvaliteedigrupp** kvaliteedigrupile, mille soovite tootele määrata.</span><span class="sxs-lookup"><span data-stu-id="e69e0-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="e69e0-163">Korrake eelmist sammu iga täiendava kvaliteedigrupi puhul, mida soovite tootele määrata.</span><span class="sxs-lookup"><span data-stu-id="e69e0-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="e69e0-164">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="e69e0-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e69e0-165">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e69e0-165">Additional resources</span></span>

- [<span data-ttu-id="e69e0-166">Kvaliteedijuhtimise testvahendid</span><span class="sxs-lookup"><span data-stu-id="e69e0-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="e69e0-167">Kvaliteedijuhtimise testid</span><span class="sxs-lookup"><span data-stu-id="e69e0-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="e69e0-168">Kvaliteedijuhtimise testgrupid</span><span class="sxs-lookup"><span data-stu-id="e69e0-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="e69e0-169">Kvaliteedijuhtimise testi muutujad</span><span class="sxs-lookup"><span data-stu-id="e69e0-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="e69e0-170">Kvaliteediseosed</span><span class="sxs-lookup"><span data-stu-id="e69e0-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]