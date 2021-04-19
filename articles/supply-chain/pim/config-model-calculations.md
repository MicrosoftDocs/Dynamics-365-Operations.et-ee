---
title: Toote konfiguratsioonimudeli arvutamise
description: See teema kirjeldab, kuidas luua rakenduse toote konfiguratsioonimudelile atribuutide kalkulatsioone
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829614"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="dd07f-103">Toote konfiguratsioonimudeli arvutamise</span><span class="sxs-lookup"><span data-stu-id="dd07f-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd07f-104">See teema kirjeldab, kuidas luua rakenduse toote konfiguratsioonimudelile atribuutide kalkulatsioone.</span><span class="sxs-lookup"><span data-stu-id="dd07f-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dd07f-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="dd07f-105">Prerequisites</span></span>

<span data-ttu-id="dd07f-106">Arvutusi kasutatakse toote konfiguratsioonimudelis toote konfiguratsiooniväärtuste arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="dd07f-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="dd07f-107">Enne arvutuste määratlemist peab olemas olema seotud toote konfiguratsioonimudel.</span><span class="sxs-lookup"><span data-stu-id="dd07f-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="dd07f-108">Konfiguratsioonimudelite ja seotud ülesannete seadistusprotsessist ülevaate saamiseks vt [Toote konfiguratsioonimudeli seadistamine](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="dd07f-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="dd07f-109">Kalkulatsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="dd07f-109">Create a calculation</span></span>

<span data-ttu-id="dd07f-110">Arvutus koosneb avaldisest ja sihtatribuudist.</span><span class="sxs-lookup"><span data-stu-id="dd07f-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="dd07f-111">Lisateavet vt teemast [Toote konfiguratsioonimudeli kalkulatsioonide KKK](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="dd07f-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="dd07f-112">Olemasoleva tootemudeli arvutuse loomiseks järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="dd07f-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="dd07f-113">Minge asukohta **Tooteteabe haldus \> Üldine \> Toote konfiguratsioonimudelid**.</span><span class="sxs-lookup"><span data-stu-id="dd07f-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="dd07f-114">Avage toote konfiguratsioonimudel ja seejärel valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dd07f-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="dd07f-115">Valige kiirkaardil **Kalkulatsioonid** suvand **Lisa**, et lisada kalkulatsioon, ja seejärel määrake järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="dd07f-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="dd07f-116">**Nimi** – sisestage kalkulatsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="dd07f-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="dd07f-117">**Kirjeldus** – sisestage kalkulatsiooni kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="dd07f-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="dd07f-118">**Sihtatribuut** – valige atribuut, millele kalkulatsiooni teete.</span><span class="sxs-lookup"><span data-stu-id="dd07f-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="dd07f-119">Valige **Redigeeri avaldis**.</span><span class="sxs-lookup"><span data-stu-id="dd07f-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="dd07f-120">Lisage dialoogiboksi **Sisesta kalkulatsioon** nõutavad atribuudid, tehtemärgid ja väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd07f-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="dd07f-121">Lisateavet elementidega töötamise kohta vaadake jaotisest [Avaldiste piirangud ja tabelipiirangud tootekonfiguratsioonimudelites](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="dd07f-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="dd07f-122">Kui avaldis on valmis, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd07f-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="dd07f-123">Arvutusnäited</span><span class="sxs-lookup"><span data-stu-id="dd07f-123">Calculation examples</span></span>

<span data-ttu-id="dd07f-124">Selles jaotises kuvatakse mõned näited kalkulatsioonide töötamise kohta.</span><span class="sxs-lookup"><span data-stu-id="dd07f-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="dd07f-125">Näide 1</span><span class="sxs-lookup"><span data-stu-id="dd07f-125">Example 1</span></span>

<span data-ttu-id="dd07f-126">Sihtatribuut on kahendmuutuja tüüpi ja arvutus kasutab järgmist tingimuslikku-avaldist:</span><span class="sxs-lookup"><span data-stu-id="dd07f-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="dd07f-127">Avaldis tagastab sihtatribuudile väärtuse *Tõene*, kui `decimalAttribute2` on suurem kui `decimalAttribute1` või sellega võrdne.</span><span class="sxs-lookup"><span data-stu-id="dd07f-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="dd07f-128">Muidu tagastab see kahendväärtuse *Väär*.</span><span class="sxs-lookup"><span data-stu-id="dd07f-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="dd07f-129">Näide 2</span><span class="sxs-lookup"><span data-stu-id="dd07f-129">Example 2</span></span>

<span data-ttu-id="dd07f-130">Selles näites kasutatakse `textFixedList` sihtatribuudina tekstiatribuudi.</span><span class="sxs-lookup"><span data-stu-id="dd07f-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="dd07f-131">See atribuut sisaldab järgmist fikseeritud loendit.</span><span class="sxs-lookup"><span data-stu-id="dd07f-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="dd07f-132">Väärtus</span><span class="sxs-lookup"><span data-stu-id="dd07f-132">Value</span></span> | <span data-ttu-id="dd07f-133">Lahendaja väärtus</span><span class="sxs-lookup"><span data-stu-id="dd07f-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="dd07f-134">A</span><span class="sxs-lookup"><span data-stu-id="dd07f-134">A</span></span> | <span data-ttu-id="dd07f-135">1a</span><span class="sxs-lookup"><span data-stu-id="dd07f-135">1a</span></span> |
| <span data-ttu-id="dd07f-136">B</span><span class="sxs-lookup"><span data-stu-id="dd07f-136">B</span></span> | <span data-ttu-id="dd07f-137">2b</span><span class="sxs-lookup"><span data-stu-id="dd07f-137">2b</span></span> |
| <span data-ttu-id="dd07f-138">C</span><span class="sxs-lookup"><span data-stu-id="dd07f-138">C</span></span> | <span data-ttu-id="dd07f-139">2c</span><span class="sxs-lookup"><span data-stu-id="dd07f-139">2c</span></span> |

<span data-ttu-id="dd07f-140">Järgmine kuvatõmmis näitab, kuidas selle atribuudi sätted teie süsteemis võidakse kuvada.</span><span class="sxs-lookup"><span data-stu-id="dd07f-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="dd07f-141">![Atribuudi tüübi sätted, näiteks 2](media/model-calculations-example2.png "Atribuudi tüübi sätted, näiteks 2")</span><span class="sxs-lookup"><span data-stu-id="dd07f-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="dd07f-142">Atribuuti kasutatakse järgmises tingimuslikus lauses:</span><span class="sxs-lookup"><span data-stu-id="dd07f-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="dd07f-143">Kui `integerAttribute` väärtus on väiksem kui 150, tagastab see lause fikseeritud loendi *A* esimese kirje tekstiväärtuse. Vastasel juhul tagastab see fikseeritud loendis *C* kolmanda kirje tekstiväärtuse.</span><span class="sxs-lookup"><span data-stu-id="dd07f-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="dd07f-144">Fikseeritud loend on samaväärne null-põhise loeteluga (enum) ja selle väärtustele pääseb juurde sobiva täisarvu väärtusega.</span><span class="sxs-lookup"><span data-stu-id="dd07f-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="dd07f-145">Seetõttu vastendatakse esimene fikseeritud loendi väärtus (*A*) väärtuseks *0*, teine väärtus (*B*) *1*-ga ja kolmas väärtus (*C*) vastendatakse *2*-ga.</span><span class="sxs-lookup"><span data-stu-id="dd07f-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="dd07f-146">Näide 3</span><span class="sxs-lookup"><span data-stu-id="dd07f-146">Example 3</span></span>

<span data-ttu-id="dd07f-147">Selles näites kasutatakse `textFixedList` sihtatribuuti eelmisest näitest.</span><span class="sxs-lookup"><span data-stu-id="dd07f-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="dd07f-148">See kasutab ka teist tekstiatribuudi `textAttribute`, mis sisaldab järgmist fikseeritud loendit.</span><span class="sxs-lookup"><span data-stu-id="dd07f-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="dd07f-149">Väärtus</span><span class="sxs-lookup"><span data-stu-id="dd07f-149">Value</span></span> | <span data-ttu-id="dd07f-150">Lahendaja väärtus</span><span class="sxs-lookup"><span data-stu-id="dd07f-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="dd07f-151">AA</span><span class="sxs-lookup"><span data-stu-id="dd07f-151">AA</span></span> | <span data-ttu-id="dd07f-152">1aa</span><span class="sxs-lookup"><span data-stu-id="dd07f-152">1aa</span></span> |
| <span data-ttu-id="dd07f-153">BB</span><span class="sxs-lookup"><span data-stu-id="dd07f-153">BB</span></span> | <span data-ttu-id="dd07f-154">2bb</span><span class="sxs-lookup"><span data-stu-id="dd07f-154">2bb</span></span> |

<span data-ttu-id="dd07f-155">Järgmine kuvatõmmis näitab, kuidas selle atribuudi sätted teie süsteemis võidakse kuvada.</span><span class="sxs-lookup"><span data-stu-id="dd07f-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="dd07f-156">![Atribuudi tüübi sätted, näiteks 3](media/model-calculations-example3.png "Atribuudi tüübi sätted, näiteks 3")</span><span class="sxs-lookup"><span data-stu-id="dd07f-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="dd07f-157">Atribuudi `textFixedList` väärtus arvutatakse järgmise tingimusliku lause abil:</span><span class="sxs-lookup"><span data-stu-id="dd07f-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="dd07f-158">Kui `textAttribute` väärtusel on lahendusväärtus, mis võrdub *1aa*, tagastab see avaldis fikseeritud loendi `textFixedList` *A* esimese kirje tekstiväärtuse. Vastasel juhul tagastab see fikseeritud loendis `textFixedList` *C* kolmanda kirje tekstiväärtuse.</span><span class="sxs-lookup"><span data-stu-id="dd07f-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="dd07f-159">Tingimuslik lause peab kasutama atribuudi lahendaja väärtust.</span><span class="sxs-lookup"><span data-stu-id="dd07f-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="dd07f-160">Arvutustes saab kasutada ainult fikseeritud loendiga tekstiatribuute.</span><span class="sxs-lookup"><span data-stu-id="dd07f-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd07f-161">Vt ka</span><span class="sxs-lookup"><span data-stu-id="dd07f-161">See also</span></span>

- [<span data-ttu-id="dd07f-162">Toote konfiguratsioonimudelite arvutuste KKK</span><span class="sxs-lookup"><span data-stu-id="dd07f-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="dd07f-163">Avaldise piirangu lisamine toote konfiguratsioonimudelile</span><span class="sxs-lookup"><span data-stu-id="dd07f-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="dd07f-164">Toote konfiguratsioonimudelite ülevaade</span><span class="sxs-lookup"><span data-stu-id="dd07f-164">Product configuration models overview</span></span>](product-configuration-models.md)
