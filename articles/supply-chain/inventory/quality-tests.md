---
title: Kvaliteedijuhtimise testid
description: See teema kirjeldab, kuidas luua teste, mida saab kasutada kvaliteettellimuste jaoks Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021680"
---
# <a name="quality-management-tests"></a><span data-ttu-id="f1c51-103">Kvaliteedijuhtimise testid</span><span class="sxs-lookup"><span data-stu-id="f1c51-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1c51-104">See teema kirjeldab, kuidas luua teste, mida saab kasutada kvaliteettellimuste jaoks Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f1c51-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f1c51-105">Kasutate lehte **Testid**, et määratleda ja vaadata üksikuid teste, mis määravad, kas teie tooted vastavad kvaliteedinõuetele.</span><span class="sxs-lookup"><span data-stu-id="f1c51-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="f1c51-106">Saate määrata katsegrupile vähemalt ühe eraldi katse.</span><span class="sxs-lookup"><span data-stu-id="f1c51-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="f1c51-107">Sellisel juhul määrate ka testipõhised andmed, nt vastuvõetavad mõõtmisväärtused.</span><span class="sxs-lookup"><span data-stu-id="f1c51-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="f1c51-108">Kvantitatiivsete testide puhul kasutatakse mõõtmise väärtusi.</span><span class="sxs-lookup"><span data-stu-id="f1c51-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="f1c51-109">Kvalitatiivsete testide puhul kasutatakse testi muutujaid.</span><span class="sxs-lookup"><span data-stu-id="f1c51-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="f1c51-110">Kvantitatiivse testi jaoks on välja **Tüüp** väärtuseks määratud *Murd* või *Täisarv*.</span><span class="sxs-lookup"><span data-stu-id="f1c51-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="f1c51-111">Mõõtühik on samuti täpsustatud.</span><span class="sxs-lookup"><span data-stu-id="f1c51-111">A unit of measure is also specified.</span></span> <span data-ttu-id="f1c51-112">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse numbritena.</span><span class="sxs-lookup"><span data-stu-id="f1c51-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="f1c51-113">Kvalitatiivsete katsete puhul väli **Tüüp** on seatud valikule *Suvand*.</span><span class="sxs-lookup"><span data-stu-id="f1c51-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="f1c51-114">Kvalitatiivsed katsed nõuavad lisateavet mõõdetava katsemuutuja ja selle loetletud valikute kohta.</span><span class="sxs-lookup"><span data-stu-id="f1c51-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="f1c51-115">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse tulemuse järgi.</span><span class="sxs-lookup"><span data-stu-id="f1c51-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="f1c51-116">Testile saate soovi korral määrata testimisinstrumendi.</span><span class="sxs-lookup"><span data-stu-id="f1c51-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="f1c51-117">Kvaliteeditellimustega testide loomiseks ja kasutamiseks ei pea testimisinstrumente vaja olema.</span><span class="sxs-lookup"><span data-stu-id="f1c51-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="f1c51-118">Lisateavet vt [Kvaliteedijuhtimise testvahendid](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="f1c51-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="f1c51-119">Samuti võite soovi korral määrata testi jaoks ühiku, et näidata mõõtühikut, milles test tulemused on salvestatud.</span><span class="sxs-lookup"><span data-stu-id="f1c51-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="f1c51-120">Näiteks võib temperatuuri test sisaldada kas Fahrenheiti või Celsiuse kraadi ühikut.</span><span class="sxs-lookup"><span data-stu-id="f1c51-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="f1c51-121">Testi näide</span><span class="sxs-lookup"><span data-stu-id="f1c51-121">Example of a test</span></span>

<span data-ttu-id="f1c51-122">Tootmisettevõte teeb ostetud materjalile kaks testi: kvantitatiivne materjali kvaliteedi test ja pakendikahjustuste kvalitatiivne test.</span><span class="sxs-lookup"><span data-stu-id="f1c51-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="f1c51-123">Ettevõte määrab lisateabe kvalitatiivse testi kohta, et määratleda testi muutuja (kahjustatud pakend) ja selle tulemused.</span><span class="sxs-lookup"><span data-stu-id="f1c51-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="f1c51-124">Ettevõte kasutab lehte **Katsegrupid**, et määrata katsegrupile kaks katset ning määrata katsepõhine teave.</span><span class="sxs-lookup"><span data-stu-id="f1c51-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="f1c51-125">testgrupp määratakse kvaliteettellimusele, nii et ettevõte saab teavitada kahe katse katsetulemustest.</span><span class="sxs-lookup"><span data-stu-id="f1c51-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="f1c51-126">Katse loomine</span><span class="sxs-lookup"><span data-stu-id="f1c51-126">Create a test</span></span>

<span data-ttu-id="f1c51-127">Testi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f1c51-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="f1c51-128">Avage **Varud \> Seaded \> Kvaliteedijuhtimine \> Testid**.</span><span class="sxs-lookup"><span data-stu-id="f1c51-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="f1c51-129">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="f1c51-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="f1c51-130">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="f1c51-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f1c51-131">**Test** – Sisestage testi kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="f1c51-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="f1c51-132">**Kirjeldus** – Sisestage testi detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f1c51-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="f1c51-133">**Tüüp** – Valige testi tulemuste tüüp.</span><span class="sxs-lookup"><span data-stu-id="f1c51-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="f1c51-134">Kvantitatiivsete katsete puhul valige *Murd* või *Täisarv*.</span><span class="sxs-lookup"><span data-stu-id="f1c51-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="f1c51-135">Kvalitatiivsete testide jaoks valige *Suvand*.</span><span class="sxs-lookup"><span data-stu-id="f1c51-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="f1c51-136">**Testvahend** – Valige [testvahend](quality-test-instruments.md), mida peaks testil kasutama.</span><span class="sxs-lookup"><span data-stu-id="f1c51-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="f1c51-137">**Ühik** – kui valisite *Tüüp* väljal *Murd* või **Täisarv** (st kui test on kvantitatiivne test), valige mõõtühik, milles testitulemused tuleks salvestada.</span><span class="sxs-lookup"><span data-stu-id="f1c51-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="f1c51-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f1c51-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="f1c51-139">Pärast testi salvestamist ei saa te enam ruudustikul välja **Tüüp** redigeerida.</span><span class="sxs-lookup"><span data-stu-id="f1c51-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="f1c51-140">Kui peate testi jaoks salvestatavat testitulemuste tüüpi muutma, valige **Muuda kvaliteettesti tüüpi** tegevuspaanil.</span><span class="sxs-lookup"><span data-stu-id="f1c51-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="f1c51-141">Dialoogiaknas **Muuda kvaliteettesti tüüpi**, seadke välja **Uus tüüp** väärtuseks soovitud tüüp ja seejärel valige dialoogiakna sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1c51-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1c51-142">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f1c51-142">Additional resources</span></span>

- [<span data-ttu-id="f1c51-143">Kvaliteedijuhtimise testvahendid</span><span class="sxs-lookup"><span data-stu-id="f1c51-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="f1c51-144">Kvaliteedijuhtimise testgrupid</span><span class="sxs-lookup"><span data-stu-id="f1c51-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="f1c51-145">Kvaliteedijuhtimise testi muutujad</span><span class="sxs-lookup"><span data-stu-id="f1c51-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="f1c51-146">Kvaliteediseosed</span><span class="sxs-lookup"><span data-stu-id="f1c51-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
