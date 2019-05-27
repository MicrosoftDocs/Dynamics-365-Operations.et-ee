---
title: Toote konfiguratsioonimudelite arvutuste KKK
description: Selles teemas kirjeldatakse tootekonfiguratsiooni mudelite arvutusi ja selgitatakse arvutuste kasutamist koos piirangutega.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00e1956950154051d4a916a013c2200029772e37
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547097"
---
# <a name="calculations-for-product-configuration-models-faq"></a><span data-ttu-id="bb307-103">Toote konfiguratsioonimudelite arvutuste KKK</span><span class="sxs-lookup"><span data-stu-id="bb307-103">Calculations for product configuration models FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb307-104">Selles teemas kirjeldatakse tootekonfiguratsiooni mudelite arvutusi ja selgitatakse arvutuste kasutamist koos piirangutega.</span><span class="sxs-lookup"><span data-stu-id="bb307-104">This topic describes calculations for product configuration models and explains how to use calculations together with constraints.</span></span>

<span data-ttu-id="bb307-105">Arvutusi saab kasutada aritmeetiliste või loogiliste operatsioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="bb307-105">Calculations can be used for arithmetic or logical operations.</span></span> <span data-ttu-id="bb307-106">Need täiendavad avaldise piiranguid toote konfiguratsioonimudelites.</span><span class="sxs-lookup"><span data-stu-id="bb307-106">They complement expression constraints in product configuration models.</span></span> <span data-ttu-id="bb307-107">Saate määratleda arvutused lehel **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** ja luua seejärel arvutuste jaoks avaldisi avaldiseredaktoris.</span><span class="sxs-lookup"><span data-stu-id="bb307-107">You can define calculations on the **Constraint-based product configuration model details** page and then build expressions for the calculations in the expression editor.</span></span> <span data-ttu-id="bb307-108">Lisateabe saamiseks vt jaotist Arvutuste loomine.</span><span class="sxs-lookup"><span data-stu-id="bb307-108">For more information, see Create calculations.</span></span>

## <a name="what-is-a-calculation"></a><span data-ttu-id="bb307-109">Mis on arvutus?</span><span class="sxs-lookup"><span data-stu-id="bb307-109">What is a calculation?</span></span>
<span data-ttu-id="bb307-110">Arvutus on toote konfiguratsioonimudelis kasutatav element.</span><span class="sxs-lookup"><span data-stu-id="bb307-110">A calculation is an element that you can use in a product configuration model.</span></span> <span data-ttu-id="bb307-111">Arvutused täiendavad piiranguid, võimaldades teil kasutada kümnendarve väärtuste arvutamiseks toote konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="bb307-111">Calculations complement constraints by letting you use decimal numbers to calculate values when you configure a product.</span></span> <span data-ttu-id="bb307-112">Lisaks on arvutuste puhul võimalik kasutada suuremat arvu tehtemärke kui piirangute puhul.</span><span class="sxs-lookup"><span data-stu-id="bb307-112">Additionally, calculations have a larger set of available operators than constraints have.</span></span>  

<span data-ttu-id="bb307-113">Sarnaselt piirangule on arvutus seotud kindla komponendiga toote konfiguratsioonimudelis ja seda ei saa uuesti kasutada või teise komponendiga jagada.</span><span class="sxs-lookup"><span data-stu-id="bb307-113">Like a constraint, a calculation is associated with a specific component in a product configuration model, and can’t be reused by or shared with another component.</span></span> <span data-ttu-id="bb307-114">Üks oluline erinevus arvutuste ja piirangute vahel on see, et arvutused on imperatiivsed (ühesuunalised) ja piirangud on deklaratiivsed (kahesuunalised).</span><span class="sxs-lookup"><span data-stu-id="bb307-114">One important difference between calculations and constraints is that calculations are imperative (unidirectional), whereas constraints are declarative (bi-directional).</span></span> <span data-ttu-id="bb307-115">Lisateavet piirangute kohta saate jaotisest [Avaldise piirangud ja tabeli piirangud](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="bb307-115">For more information about constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span>  

<span data-ttu-id="bb307-116">Arvutus koosneb on sihtatribuudist ja arvutusavaldisest.</span><span class="sxs-lookup"><span data-stu-id="bb307-116">A calculation consists of a target attribute and a calculation expression.</span></span>

## <a name="what-is-a-target-attribute"></a><span data-ttu-id="bb307-117">Mis on sihtatribuut?</span><span class="sxs-lookup"><span data-stu-id="bb307-117">What is a target attribute?</span></span>
<span data-ttu-id="bb307-118">Sihtatribuut on atribuut, mis võtab avaldises vastu arvutuse tulemuse.</span><span class="sxs-lookup"><span data-stu-id="bb307-118">A target attribute is an attribute that receives the result of the calculation expression.</span></span>  

<span data-ttu-id="bb307-119">Järgmises valemis on sihtatribuut laudlina mõõt.</span><span class="sxs-lookup"><span data-stu-id="bb307-119">In the following expression, the target attribute is a tablecloth measurement:</span></span>  

<span data-ttu-id="bb307-120">**Avaldis:** If\[decimalAttribute1 &lt;= decimalAttribute2, tõene, väär\]</span><span class="sxs-lookup"><span data-stu-id="bb307-120">**Expression:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span></span>  

<span data-ttu-id="bb307-121">**DecimalAttribute1** on tabeli pikkus ja **decimalAttribute2** on laudlina pikkus.</span><span class="sxs-lookup"><span data-stu-id="bb307-121">**DecimalAttribute1** is the table length, and **decimalAttribute2** is the tablecloth length.</span></span> <span data-ttu-id="bb307-122">Avaldis tagastab väärtuse **Tõene** sihtatribuudile, kui **decimalAttribute2** on suurem kui **decimalAttribute1** või sellega võrdne.</span><span class="sxs-lookup"><span data-stu-id="bb307-122">The expression returns the value **True** to the target attribute if **decimalAttribute2** is greater than or equal to **decimalAttribute1**.</span></span> <span data-ttu-id="bb307-123">Muidu tagastab avaldis väärtuse **Väär**.</span><span class="sxs-lookup"><span data-stu-id="bb307-123">Otherwise, the expression returns **False**.</span></span> <span data-ttu-id="bb307-124">Seega on laudlina mõõt aktsepteeritav, kui laudlina pikkus on laua pikkusega sama või ületab laua pikkuse.</span><span class="sxs-lookup"><span data-stu-id="bb307-124">Therefore, the tablecloth measurement is acceptable if the tablecloth length is the same as or exceeds the length of the table.</span></span>

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a><span data-ttu-id="bb307-125">Milliseid atribuudi tüüpe saab sihtatribuutideks määrata?</span><span class="sxs-lookup"><span data-stu-id="bb307-125">What attribute types can be set to target attributes?</span></span>
<span data-ttu-id="bb307-126">Kõiki toote konfiguraatori puhul toetatud atribuuditüüpe saab määrata sihtatribuutideks, välja arvatud ilma fikseeritud loendita tekst.</span><span class="sxs-lookup"><span data-stu-id="bb307-126">All attribute types that the product configurator supports can be set to target attributes, except text without a fixed list.</span></span>

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a><span data-ttu-id="bb307-127">Kas sihtatribuudi väärtus saab arvutuses sisendatribuutide väärtusi piirata?</span><span class="sxs-lookup"><span data-stu-id="bb307-127">Can the value of a target attribute restrict the values of the input attributes in a calculation?</span></span>
<span data-ttu-id="bb307-128">Ei, sihtatribuudi väärtus ei saa sisendatribuutide väärtusi piirata, sest arvutused on ühesuunalised.</span><span class="sxs-lookup"><span data-stu-id="bb307-128">No, the value of a target attribute can’t restrict the values of the input attributes, because calculations are unidirectional.</span></span> <span data-ttu-id="bb307-129">Seetõttu määratakse sihtatribuudi väärtus sisendatribuudi väärtuse muudatuste alusel, kuid muudatus sihtatribuudi väärtuses ei mõjuta sisendatribuutide väärtust.</span><span class="sxs-lookup"><span data-stu-id="bb307-129">Therefore, the value of the target attribute is set based on changes in the value of the input attributes, but a change in the value of the target doesn’t affect the value of the input attributes.</span></span> <span data-ttu-id="bb307-130">See käitumine erineb piirangute käitumisest.</span><span class="sxs-lookup"><span data-stu-id="bb307-130">This behavior differs from the behavior for constraints.</span></span> <span data-ttu-id="bb307-131">Piirangud ilmnevad mõlemasuunaliselt.</span><span class="sxs-lookup"><span data-stu-id="bb307-131">Constraints occur in both directions.</span></span>

### <a name="example"></a><span data-ttu-id="bb307-132">Näide</span><span class="sxs-lookup"><span data-stu-id="bb307-132">Example</span></span>

<span data-ttu-id="bb307-133">Järgmises avaldises on arvutuse sihtväärtus toitejuhtme pikkus ja sisendväärtus on värv.</span><span class="sxs-lookup"><span data-stu-id="bb307-133">In the following expression, the target for the calculation is the length of a power cord, and the input value is a color:</span></span>  

<span data-ttu-id="bb307-134">**Avaldis:** \[If Color == "Roheline", 1,5, 1,0\]</span><span class="sxs-lookup"><span data-stu-id="bb307-134">**Expression:** \[If Color == "Green", 1.5, 1.0\]</span></span>  

<span data-ttu-id="bb307-135">Kauba konfigureerimisel määratakse toitejuhtme pikkuseks **1,5**, kui määrate värviatribuudiks **Roheline**.</span><span class="sxs-lookup"><span data-stu-id="bb307-135">When you configure the item, the length of the power cord is set to **1.5** if you specify **Green** as the value of color attribute.</span></span> <span data-ttu-id="bb307-136">Kui määrate mõne muu värvi, määratakse pikkuseks **1**.</span><span class="sxs-lookup"><span data-stu-id="bb307-136">If you specify any other color, the length is set to **1.0**.</span></span> <span data-ttu-id="bb307-137">Kuid kuna arvutused on ühesuunalised, ei määra arvutus värviatribuudi väärtuseks **Roheline**, kui määrate pikkuseks **1,5**.</span><span class="sxs-lookup"><span data-stu-id="bb307-137">However, because calculations are unidirectional, the calculation doesn't set the value of the color attribute to **Green** if you specify a length of **1.5**.</span></span>

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a><span data-ttu-id="bb307-138">Mis juhtub, kui arvutusel on täisarvu tüüpi sihtatribuut, kuid arvutus loob kümnendarvu?</span><span class="sxs-lookup"><span data-stu-id="bb307-138">What happens if a calculation has a target attribute of the integer type but a calculation generates a decimal number?</span></span>
<span data-ttu-id="bb307-139">Kui sihtatribuut on täisarvu tüüpi, kuid arvutus loob kümnendarvu, tagastatakse ainult arvutuse täisarvuline osa.</span><span class="sxs-lookup"><span data-stu-id="bb307-139">If a target attribute is of the integer type, but a calculation generates a decimal number, only the integer part of the calculated result is returned.</span></span> <span data-ttu-id="bb307-140">Kümnendosa eemaldatakse ja tulemust ei ümardata.</span><span class="sxs-lookup"><span data-stu-id="bb307-140">The decimal part is removed, and the result isn't rounded.</span></span> <span data-ttu-id="bb307-141">Näiteks arvu 12,70 tulemusena kuvatakse 12.</span><span class="sxs-lookup"><span data-stu-id="bb307-141">For example, a result of 12.70 is shown as 12.</span></span>

## <a name="when-do-calculations-occur"></a><span data-ttu-id="bb307-142">Millal arvutused toimuvad?</span><span class="sxs-lookup"><span data-stu-id="bb307-142">When do calculations occur?</span></span>
<span data-ttu-id="bb307-143">Arvutused toimuvad, kui on esitatud kõigi sisendatribuutide väärtus.</span><span class="sxs-lookup"><span data-stu-id="bb307-143">Calculations occur when a value has been provided for all input attributes.</span></span>

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a><span data-ttu-id="bb307-144">Kas saan sihtatribuudile arvutatud väärtuse üle kirjutada?</span><span class="sxs-lookup"><span data-stu-id="bb307-144">Can I overwrite the value that is calculated for the target attribute?</span></span>
<span data-ttu-id="bb307-145">Saate sihtatribuudile arvutatud väärtuse üle kirjutada, kui sihtatribuut pole määratud peidetuks või kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="bb307-145">You can overwrite the value that is calculated for the target attribute, unless the target attribute is set as hidden or read-only.</span></span>

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a><span data-ttu-id="bb307-146">Kuidas määrata sihtatribuut peidetuks või kirjutuskaitstuks?</span><span class="sxs-lookup"><span data-stu-id="bb307-146">How do I set a target attribute as hidden or read-only?</span></span>
<span data-ttu-id="bb307-147">Atribuudi määramiseks peidetuks või kirjutuskaitstuks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="bb307-147">To set an attribute as hidden or read-only, follow these steps.</span></span>

1.  <span data-ttu-id="bb307-148">Klõpsake valikuid **Tooteteabe haldus** &gt; **Üldine** &gt; **Toote konfiguratsioonimudelid**.</span><span class="sxs-lookup"><span data-stu-id="bb307-148">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="bb307-149">Valige toote konfiguratsioonimudel ja klõpsake seejärel tegevuspaanil suvandit **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="bb307-149">Select a product configuration model, and then, on the Action Pane, click **Edit**.</span></span>
3.  <span data-ttu-id="bb307-150">Valige lehel **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** sihtatribuudina kasutatav atribuut.</span><span class="sxs-lookup"><span data-stu-id="bb307-150">On the **Constraint-based product configuration model details** page, select the attribute to use as a target attribute.</span></span>
4.  <span data-ttu-id="bb307-151">Valige kiirkaardil **Atribuudid** suvand **Peidetud** või **Kirjutuskaitstud**.</span><span class="sxs-lookup"><span data-stu-id="bb307-151">On the **Attributes** FastTab, select **Hidden** or **Read-only**.</span></span>

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a><span data-ttu-id="bb307-152">Kas arvutus saab minu määratud väärtused üle kirjutada?</span><span class="sxs-lookup"><span data-stu-id="bb307-152">Can a calculation overwrite the values that I set?</span></span>
<span data-ttu-id="bb307-153">Nr</span><span class="sxs-lookup"><span data-stu-id="bb307-153">No.</span></span> <span data-ttu-id="bb307-154">Kasutatakse toote konfigureerimisel määratud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="bb307-154">The values that you set when you configure a product are the values that are used.</span></span> <span data-ttu-id="bb307-155">Arvutus, mis toimub, kui muudetakse arvutuse sisendväärtusi, ei saa konkreetse atribuudi kohta esitatud väärtusi üle kirjutada.</span><span class="sxs-lookup"><span data-stu-id="bb307-155">The calculation that occurs when the input values in a calculation are changed can’t overwrite the values that you provide for a specific attribute.</span></span>

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a><span data-ttu-id="bb307-156">Mis juhtub, kui eemaldan arvutusest sisendväärtuse?</span><span class="sxs-lookup"><span data-stu-id="bb307-156">What happens if I remove an input value in a calculation?</span></span>
<span data-ttu-id="bb307-157">Sisendväärtuse eemaldamisel arvutusest eemaldatakse ka sihtatribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="bb307-157">If you remove an input value in a calculation, the value of the target attribute is also removed.</span></span>

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a><span data-ttu-id="bb307-158">Miks saan tõrketeate, mis ütleb, et minu mudelis on vastuolu?</span><span class="sxs-lookup"><span data-stu-id="bb307-158">Why do I receive an error message that says that my model is in contradiction?</span></span>
<span data-ttu-id="bb307-159">See teade kuvatakse, kui arvutuses on viga või kui ühes või mitmes piirangus on vastuolu.</span><span class="sxs-lookup"><span data-stu-id="bb307-159">This message is shown when a calculation includes an error, or when a contradiction exists in one or more constraints.</span></span> <span data-ttu-id="bb307-160">Lisateavet piirangutes olevate vastuolude kohta saate jaotisest [Avaldise piirangud ja tabeli piirangud](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="bb307-160">For more information about contradictions in constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span> <span data-ttu-id="bb307-161">Siin on mõned olukorrad, kus arvutustes võib ilmneda vigu.</span><span class="sxs-lookup"><span data-stu-id="bb307-161">Here are some situations where errors can occur in calculations:</span></span>

-   <span data-ttu-id="bb307-162">Väärtus on jagatud nulliga (0).</span><span class="sxs-lookup"><span data-stu-id="bb307-162">A value is divided by 0 (zero).</span></span>
-   <span data-ttu-id="bb307-163">Kahe järgmise elemendi vahel on konflikt:</span><span class="sxs-lookup"><span data-stu-id="bb307-163">A conflict exists between the following two elements:</span></span>
    -   <span data-ttu-id="bb307-164">väärtused, mis on atribuudi puhul saadaval ja piiranguga piiratud;</span><span class="sxs-lookup"><span data-stu-id="bb307-164">The values that are available for an attribute and are limited by a constraint</span></span>
    -   <span data-ttu-id="bb307-165">arvutusega loodud väärtus.</span><span class="sxs-lookup"><span data-stu-id="bb307-165">A value that is generated by a calculation</span></span>
-   <span data-ttu-id="bb307-166">Arvutusega saadud väärtused on väljaspool atribuudi domeeni.</span><span class="sxs-lookup"><span data-stu-id="bb307-166">The values that are returned by the calculation are outside the domain of the attribute.</span></span> <span data-ttu-id="bb307-167">Näiteks on täisarv vahemikus \[1.. 10\], mis on arvutatud nulliks.</span><span class="sxs-lookup"><span data-stu-id="bb307-167">An example is an integer from \[1..10\] that is calculated to 0.</span></span>

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a><span data-ttu-id="bb307-168">Miks saan tõrketeate, kuigi minu tootemudeli kinnitamine õnnestus?</span><span class="sxs-lookup"><span data-stu-id="bb307-168">Why do I receive an error message even though I successfully validated my product model?</span></span>
<span data-ttu-id="bb307-169">Arvutusi ei kaasata kinnitamisse.</span><span class="sxs-lookup"><span data-stu-id="bb307-169">Calculations aren't included in the validation.</span></span> <span data-ttu-id="bb307-170">Vigade leidmiseks arvutustes peab konfiguratsioonimudelit testima.</span><span class="sxs-lookup"><span data-stu-id="bb307-170">You must test the product configuration model to find errors in calculations.</span></span> <span data-ttu-id="bb307-171">Toote konfiguratsioonimudeli testimiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="bb307-171">To test a product configuration model, follow these steps.</span></span>

1.  <span data-ttu-id="bb307-172">Klõpsake valikuid **Tooteteabe haldus** &gt; **Üldine** &gt; **Toote konfiguratsioonimudelid**.</span><span class="sxs-lookup"><span data-stu-id="bb307-172">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="bb307-173">Valige toote konfiguratsioonimudel ja klõpsake seejärel tegevuspaanil grupis **Käita** suvandit **Katse**.</span><span class="sxs-lookup"><span data-stu-id="bb307-173">Select a product configuration model, and then, on the Action Pane, in the **Run** group, click **Test**.</span></span>




