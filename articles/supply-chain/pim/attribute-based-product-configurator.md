---
title: Atribuudipõhised müügihinnad piirangupõhistele tootekonfiguratsioonidele
description: Selles teemas kirjeldatakse, kuidas luua müügihinna mudeleid müügihindadega, mis põhinevad komponentidel ja atribuutidel, mitte füüsilisel kooslusel ja protsessil.
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c0f9c1bb94b4dcc3c3c1e7656868ef6e6bd903db
ms.sourcegitcommit: 9ca63cbc6bc6d6baed9d45bce30d0b32e156301c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988318"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a><span data-ttu-id="2a06d-103">Atribuudipõhised müügihinnad piirangupõhistele tootekonfiguratsioonidele</span><span class="sxs-lookup"><span data-stu-id="2a06d-103">Attribute-based sales prices for constraint-based product configuration</span></span>

<span data-ttu-id="2a06d-104">Selles teemas kirjeldatakse, kuidas luua müügihinna mudeleid müügihindadega, mis põhinevad komponentidel ja atribuutidel, mitte füüsilisel kooslusel ja protsessil.</span><span class="sxs-lookup"><span data-stu-id="2a06d-104">This topic describes how to build sales price models with sales prices based on components and attributes rather than on the physical bill of material and the route.</span></span> <span data-ttu-id="2a06d-105">Igale tootekonfiguratsiooni mudelile saate luua mitu müügihinna mudelit.</span><span class="sxs-lookup"><span data-stu-id="2a06d-105">You can build several sales price models for each product configuration model.</span></span>

## <a name="set-relevant-product-information-management-parameters"></a><span data-ttu-id="2a06d-106">Asjakohaste tooteteabe halduse parameetrite seadmine</span><span class="sxs-lookup"><span data-stu-id="2a06d-106">Set relevant product information management parameters</span></span>

<span data-ttu-id="2a06d-107">Enne kui alustate oma hinnamudelite loomist, peate määratlema vaikevaluuta, mida kasutatakse müügihinna mudelite loomisel.</span><span class="sxs-lookup"><span data-stu-id="2a06d-107">Before you start building your price models, you must define a default currency, which is used when you build your sales price models.</span></span> <span data-ttu-id="2a06d-108">Samuti saate valida, kas lisada Microsoft Exceli fail, milles on kõikide tellimuse või pakkumise ridade hinnajaotus.</span><span class="sxs-lookup"><span data-stu-id="2a06d-108">You can also choose whether to attach a Microsoft Excel file with a price breakdown for all order or quotation lines.</span></span> <span data-ttu-id="2a06d-109">Hinnajaotus võimaldab teil jagada üksikasju klientidega selle kohta, kuidas te arvutasite konfigureeritud toote jaoks kindla müügihinna.</span><span class="sxs-lookup"><span data-stu-id="2a06d-109">The price breakdown will enable you to share details with customers about how you arrived at a specific sales price for a configured product.</span></span>

<span data-ttu-id="2a06d-110">Vaikevaluuta seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2a06d-110">To set your default currency:</span></span>

1. <span data-ttu-id="2a06d-111">Avage **Tooteteabe haldus \> Seadistus \> Tooteteabe halduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-111">Go to  **Product information management \> Setup \> Product information management parameters**.</span></span>
1. <span data-ttu-id="2a06d-112">Avage vahekaart **Piirangupõhise tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-112">Open the **Constraint-Based product configuration models** tab.</span></span>
1. <span data-ttu-id="2a06d-113">Avage ripploend **Vaikevaluuta** ja valige valuuta.</span><span class="sxs-lookup"><span data-stu-id="2a06d-113">Open the **Default currency** drop-down list and select your currency.</span></span>

    <span data-ttu-id="2a06d-114">![Vaikevaluuta seadmine piirangupõhise tootekonfiguratsiooni jaoks](media/prod-config-currency.png "Vaikevaluuta seadmine piirangupõhise tootekonfiguratsiooni jaoks")</span><span class="sxs-lookup"><span data-stu-id="2a06d-114">![Set the default currency for constraint-based product configuration](media/prod-config-currency.png "Set the default currency for constraint-based product configuration")</span></span>

1. <span data-ttu-id="2a06d-115">Kui soovite lisada kõigi tellimuse või pakkumise ridade hinnajaotusega Exceli faili, siis seadke jaotises **Hinnamudel** suvandi **Manusta** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="2a06d-115">If you'd like to attach an Excel file with a price breakdown for all order or quotation lines, then in the **Price model** section, set **Attach** to *Yes*.</span></span>

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a><span data-ttu-id="2a06d-116">Müügihinna mudelite loomine</span><span class="sxs-lookup"><span data-stu-id="2a06d-116">Build your sales price models</span></span>

<span data-ttu-id="2a06d-117">Müügihinna mudeli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2a06d-117">To build a sales price model:</span></span>

1. <span data-ttu-id="2a06d-118">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-118">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="2a06d-119">Valige sobiv tootekonfiguratsiooni mudel.</span><span class="sxs-lookup"><span data-stu-id="2a06d-119">Select the target product configuration model.</span></span>
1. <span data-ttu-id="2a06d-120">Valige toimingupaanil vahekaart **Mudel** ning valige rühmas **Seadistamine** suvand **Hinnamudelid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-120">On the Action pane, open the **Model** tab and, from the **Set up** group, select **Price models**.</span></span>
1. <span data-ttu-id="2a06d-121">Avaneb leht **Hinnamudelid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-121">The **Price models** page opens.</span></span>
1. <span data-ttu-id="2a06d-122">Valige hinnamudel või lisage ruudustikku uus.</span><span class="sxs-lookup"><span data-stu-id="2a06d-122">Select a price model or add a new one to the grid.</span></span>
1. <span data-ttu-id="2a06d-123">Valige **Redigeeri**, et avada valitud mudeli jaoks redigeerimisleht, mis sisaldab järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="2a06d-123">Select **Edit** to open the edit page for your selected model, which provides the following features:</span></span>
    - <span data-ttu-id="2a06d-124">Vormi päises kuvatakse vaikevaluuta ja seal saate oma hinna seadistamiseks lisada uusi valuutasid.</span><span class="sxs-lookup"><span data-stu-id="2a06d-124">The header of the form shows the default currency and lets you add new currencies for your price setup.</span></span>
    - <span data-ttu-id="2a06d-125">Vasakpoolne paan näitab kõiki tootemudeli komponente ja kasutajanõudeid.</span><span class="sxs-lookup"><span data-stu-id="2a06d-125">The left pane shows all the components and user requirements of the product model.</span></span> <span data-ttu-id="2a06d-126">Igal tootemudeli puu sõlmel võib olla üks baashinna avaldis ja ükskõik kui palju avaldisereegleid.</span><span class="sxs-lookup"><span data-stu-id="2a06d-126">Each node in the product model tree can have one base-price expression and an optional number of expression rules.</span></span> <span data-ttu-id="2a06d-127">Avaldisereegel koosneb tingimusest ja avaldisest ning iga avaldisereegel hõlmab tootesuvandit, mis aitab reguleerida toote hinda.</span><span class="sxs-lookup"><span data-stu-id="2a06d-127">An expression rule consists of a condition and an expression and each expression rule covers a product option that helps control the price of the product.</span></span>
    - <span data-ttu-id="2a06d-128">Kui koostate oma tingimused ja avaldised, saate kasutada samu tehtemärke, mis on saadaval tootemudeli arvutuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2a06d-128">When you build your conditions and expressions, you have the same operators available as for calculations in a product model.</span></span> <span data-ttu-id="2a06d-129">Avaldiseredaktor toetab nii tingimusi kui ka avaldisi.</span><span class="sxs-lookup"><span data-stu-id="2a06d-129">The expression editor also supports both conditions and expressions.</span></span>
1. <span data-ttu-id="2a06d-130">Valige vasakus veerus sõlm ja kasutage seejärel eelmises sammus kirjeldatud funktsioone, et luua selle jaoks hinnakujunduse reeglid (vt ka pärast seda toimingut toodud näidet).</span><span class="sxs-lookup"><span data-stu-id="2a06d-130">Select a node in the left column and then use the features described in the previous step to establish pricing rules for it (see also the example provided after this procedure).</span></span> <span data-ttu-id="2a06d-131">Korrake seda sammu vajaduse järgi iga sõlme puhul.</span><span class="sxs-lookup"><span data-stu-id="2a06d-131">Repeat this step for each node as needed.</span></span>

<span data-ttu-id="2a06d-132">Järgmises näites on toodud baashind 899,95 eurot staatilise arvuna, mida saab muuta ühe või mitme järgmise viie avaldisereegliga sõltuvalt kliendi valitud konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="2a06d-132">The following example shows a base price of a static number of 899.95 EUR, which can be modified by one or more of the following five expression rules, depending on the configuration selected by the customer:</span></span>

- <span data-ttu-id="2a06d-133">Valge korpuse puhul lahutage 59,95 eurot.</span><span class="sxs-lookup"><span data-stu-id="2a06d-133">For white cabinet finish, subtract 59.95 EUR.</span></span>
- <span data-ttu-id="2a06d-134">Nurgakaitsete puhul lisage 35,95 eurot.</span><span class="sxs-lookup"><span data-stu-id="2a06d-134">For corner protection, add 35.95 EUR.</span></span>
- <span data-ttu-id="2a06d-135">Metallist eesvõre puhul lisage 89,95 eurot.</span><span class="sxs-lookup"><span data-stu-id="2a06d-135">For a metal front grill, add 89.95 EUR.</span></span>
- <span data-ttu-id="2a06d-136">Puitu imiteeriva korpuse puhul lisage 119,95 eurot.</span><span class="sxs-lookup"><span data-stu-id="2a06d-136">For rosewood cabinet finish, add 119.95 EUR.</span></span>
- <span data-ttu-id="2a06d-137">Lisage 12,95 eurot iga kõlari kõrguse ühiku kohta.</span><span class="sxs-lookup"><span data-stu-id="2a06d-137">Add 12.95 EUR for each unit of speaker height.</span></span>

<span data-ttu-id="2a06d-138">![Näidishinnamudel](media/prod-config-rules-example.png "Näidishinnamudel")</span><span class="sxs-lookup"><span data-stu-id="2a06d-138">![Example price model](media/prod-config-rules-example.png "Example price model")</span></span>

## <a name="add-support-for-multiple-currencies"></a><span data-ttu-id="2a06d-139">Mitme valuuta toe lisamine</span><span class="sxs-lookup"><span data-stu-id="2a06d-139">Add support for multiple currencies</span></span>

<span data-ttu-id="2a06d-140">Konfigureeritava toote müümise korral kontrollib süsteem, kas hinnad on seadistatud otse kliendi valuutas.</span><span class="sxs-lookup"><span data-stu-id="2a06d-140">When a configurable product is sold, the system checks whether the prices have been set explicitly in the currency of the customer.</span></span> <span data-ttu-id="2a06d-141">Kui jah, siis kasutatakse otseseid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="2a06d-141">If so, the explicit values are used.</span></span> <span data-ttu-id="2a06d-142">Kui mitte, kasutab süsteem selle ettevõtte jaoks määratud valuutakursse, et teisendada vaikevaluutas väärtus kliendi valuutasse.</span><span class="sxs-lookup"><span data-stu-id="2a06d-142">If not, the system uses the currency exchange rates established for the sales company to convert the default currency value to the customer's currency.</span></span>

<span data-ttu-id="2a06d-143">Otseste hindade lisamiseks lisavaluutas tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2a06d-143">To add explicit prices in an additional currency:</span></span>

1. <span data-ttu-id="2a06d-144">Avage oma hinnamudeli jaoks redigeerimisleht, nagu on kirjeldatud jaotises [Müügihinna mudelite loomine](#build-price-model).</span><span class="sxs-lookup"><span data-stu-id="2a06d-144">Open the edit page for your price model, as described in [Build your sales price models](#build-price-model).</span></span>
1. <span data-ttu-id="2a06d-145">Valige hinnamudeli päises nupp **Lisa**, et avada rippdialoogiboks **Valuutad**, kus on loetletud saadaolevad valuutad.</span><span class="sxs-lookup"><span data-stu-id="2a06d-145">Select the **Add** button in the header of the price model to open the **Currencies** drop-down dialog box, which lists the available currencies.</span></span>
1. <span data-ttu-id="2a06d-146">Valige rippdialoogiboksis **Valuutad** valuuta, mille soovite lisada, ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-146">Select the currency you want to add in the **Currencies** drop-down dialog box and then select **OK**.</span></span>
1. <span data-ttu-id="2a06d-147">Ripploend **Praegune valuuta** sisaldab nüüd äsja lisatud valuutat ning kõiki muid valuutasid, mis võisid olla varem lisatud.</span><span class="sxs-lookup"><span data-stu-id="2a06d-147">The **Current currency** drop-down list now includes the currency that you just added, plus any other currencies that may have been added previously.</span></span> <span data-ttu-id="2a06d-148">Valige uus valuuta ja pange tähele, et jaotises **Avaldisereeglid** olev ruudustik sisaldab nüüd kaht avaldisevälja.</span><span class="sxs-lookup"><span data-stu-id="2a06d-148">Select your new currency and notice that the grid in the **Expression rules** section now includes two expression fields:</span></span>
    - <span data-ttu-id="2a06d-149">**Avaldis** – näitab hinna otsimiseks kasutatavat avaldist (või püsiväärtust), kasutades praegust valuutat, mis valiti suvandis **Praegune valuuta**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-149">**Expression** - Shows the expression (or constant value) for finding the price using the currency currently selected for **Current currency**.</span></span>
    - <span data-ttu-id="2a06d-150">**Vaikeavaldised** – näitab hinna otsimiseks kasutatavat avaldist (või püsiväärtust), kasutades vaikevaluutat (kuvatud väljal **Vaikevaluuta**).</span><span class="sxs-lookup"><span data-stu-id="2a06d-150">**Default expressions** - Shows the expression (or constant value) for finding the price using the default currently (shown in the **Default currency** field).</span></span>

    > [!NOTE]
    > <span data-ttu-id="2a06d-151">Avaldisereeglite välja **Tingimus** „omanik” on vaikevaluuta, mis tähendab, et te ei saa muuta tingimust teistes valuutades.</span><span class="sxs-lookup"><span data-stu-id="2a06d-151">The **Condition** field for the expression rules is "owned" by the default currency, which means that you can't modify the condition for other currencies.</span></span> <span data-ttu-id="2a06d-152">Samuti ei saa te lisada uusi avaldisereegleid, kui praegu on valitud valuuta, mis ei ole valitud suvandis **Praegune valuuta**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-152">You also can't add new expression rules while a currency other than the default currency is selected as the **Current currency**.</span></span>
1. <span data-ttu-id="2a06d-153">Redigeerige veerus **Avaldis** olevaid väärtusi praeguse valuuta jaoks vajaduse järgi.</span><span class="sxs-lookup"><span data-stu-id="2a06d-153">Edit values in the **Expression** column as needed for the current currency.</span></span>

<span data-ttu-id="2a06d-154">Alltoodud näites on _EUR_ vaikevaluuta ja _USD_ on lisatud lisavaluutana.</span><span class="sxs-lookup"><span data-stu-id="2a06d-154">In the example below, _EUR_ is the default currency, and _USD_ has been added as an additional currency.</span></span>

<span data-ttu-id="2a06d-155">![Mitme valuutaga mudeli näide](media/prod-config-rules-currency-example.png "Mitme valuutaga mudeli näide")</span><span class="sxs-lookup"><span data-stu-id="2a06d-155">![Example of a model with multiple currencies](media/prod-config-rules-currency-example.png "Example of a model with multiple currencies")</span></span>

> [!NOTE]
> <span data-ttu-id="2a06d-156">Te ei saa lisada avaldisereegleid, mis kehtivad ainult mittevaikevaluuta puhul.</span><span class="sxs-lookup"><span data-stu-id="2a06d-156">You can't add expression rules that are unique for a non-default currency.</span></span> <span data-ttu-id="2a06d-157">Avaldisereeglite loomiseks, mis kehtiksid ainult valuuta puhul, mis ei ole vaikevaluuta, seadke vaikevaluuta hinnaavaldise väärtus nulliks.</span><span class="sxs-lookup"><span data-stu-id="2a06d-157">To create expression rules that would be relevant only for a currency other than the default currency, set the price expression for the default currency to zero.</span></span> <span data-ttu-id="2a06d-158">Seejärel seadistage mittevaikevaluuta jaoks sobiv avaldis.</span><span class="sxs-lookup"><span data-stu-id="2a06d-158">Then set the appropriate expression for the non-default currency.</span></span>

## <a name="test-your-price-model"></a><span data-ttu-id="2a06d-159">Hinnamudeli katsetamine</span><span class="sxs-lookup"><span data-stu-id="2a06d-159">Test your price model</span></span>

<span data-ttu-id="2a06d-160">Et katsetada, kuidas müügihinnad töötavad konfiguratsiooniseansis, avage oma hinnamudeli jaoks redigeerimisleht, nagu on kirjeldatud jaotises [Müügihinna mudelite loomine](#build-price-model), ning valige seejärel toimingupaanil suvand **Testi**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-160">To test how the sales prices work in a configuration session, open the edit page for your price model, as described in [Build your sales price models](#build-price-model) and then select  **Test** on the Action Pane.</span></span> <span data-ttu-id="2a06d-161">Avaneb dialoogiboks **Hinnamudeli katsetamine**, kus saate teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="2a06d-161">The **Test product model** dialog box opens, where you can do the following:</span></span>

- <span data-ttu-id="2a06d-162">Kasutage siin pakutavaid konfiguratsiooniseadeid, et valida tootesuvandid, ja seejärel vaadake, kuidas need mõjutavad suvandi **Hind ja lähetuskuupäev** väärtust.</span><span class="sxs-lookup"><span data-stu-id="2a06d-162">Use the configuration settings offered here to select product options and then see how they affect the value shown for **Price and ship date**.</span></span>
- <span data-ttu-id="2a06d-163">Valige **Kuva hinnajaotus**, et laadida alla Exceli dokument, mis näitab hinna arvutamise kõiki üksikasju.</span><span class="sxs-lookup"><span data-stu-id="2a06d-163">Select **View price breakdown** to download an Excel document that shows full details about how the price was calculated.</span></span>

<span data-ttu-id="2a06d-164">![Oma tootemudeli katsetamine](media/prod-config-test.png "Oma tootemudeli katsetamine")</span><span class="sxs-lookup"><span data-stu-id="2a06d-164">![Test your product model](media/prod-config-test.png "Test your product model")</span></span>

<span data-ttu-id="2a06d-165">Allalaaditud arvutustabel näitab iga aktiivse hinnaelemendi puhul nii absoluutset väärtust kui ka kasumi protsenti.</span><span class="sxs-lookup"><span data-stu-id="2a06d-165">The downloaded spreadsheet shows both the absolute value and the contribution as a percentage for each active price element.</span></span> <span data-ttu-id="2a06d-166">Kui olete seadistanud lehel **Tooteteabe halduse parameetrid** hinnamudeli suvandi **Manusta**, lisatakse see Exceli leht tellimuse või pakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="2a06d-166">If you have set the **Attach** price model option on the **Product information management parameters** page, this Excel sheet gets attached to the order or quotation line.</span></span>

<span data-ttu-id="2a06d-167">![Exceli arvutustabel, milles on kuvatud hinnajaotus](media/prod-config-excel-example.png "Exceli arvutustabel, milles on kuvatud hinnajaotus")</span><span class="sxs-lookup"><span data-stu-id="2a06d-167">![Excel spreadsheet showing price breakdown](media/prod-config-excel-example.png "Excel spreadsheet showing price breakdown")</span></span>

## <a name="set-up-selection-criteria-for-price-models"></a><span data-ttu-id="2a06d-168">Valikukriteeriumide seadistamine hinnamudelite jaoks</span><span class="sxs-lookup"><span data-stu-id="2a06d-168">Set up selection criteria for price models</span></span>

<span data-ttu-id="2a06d-169">Kui teie hinnamudelid on seadistatud, tuleb teil luua vähemalt üks valikukriteerium, et hinnamudel pakkumise või tellimuse konfigureerimisel üles leida.</span><span class="sxs-lookup"><span data-stu-id="2a06d-169">When your price models are in place, you must establish at least one selection criterion to pick up the price model when you configure to quote or to order.</span></span> <span data-ttu-id="2a06d-170">Seda saate teha ühe või mitme päringu seadistamisega.</span><span class="sxs-lookup"><span data-stu-id="2a06d-170">You'll do this by setting up one or more queries.</span></span> <span data-ttu-id="2a06d-171">Koos ühtivate müügihinna mudelitega pakuvad päringud suurt paindlikkust, kui kohandate hindu kindlate klientide, regioonide, perioodide ja muude kriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="2a06d-171">In a combination with matching sales price models, the queries provide great flexibility in targeting sales prices for particular customers, regions, periods, and other criteria.</span></span>

<span data-ttu-id="2a06d-172">Valikukriteeriumide seadistamiseks hinnamudelite jaoks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2a06d-172">To set up selection criteria for price models:</span></span>

1. <span data-ttu-id="2a06d-173">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-173">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="2a06d-174">Valige sobiv tootekonfiguratsiooni mudel.</span><span class="sxs-lookup"><span data-stu-id="2a06d-174">Select the target product configuration model.</span></span>
1. <span data-ttu-id="2a06d-175">Valige toimingupaanil vahekaart **Mudel** ning valige rühmas **Seadistamine** suvand **Hinnamudeli kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-175">On the Action pane, open the **Model** tab and, from the **Set up** group, select **Price model criteria**.</span></span> <span data-ttu-id="2a06d-176">Avaneb leht **Hinnamudeli kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-176">The **Price model criteria** page opens.</span></span>
1. <span data-ttu-id="2a06d-177">Kui vajalikku päringurida ei ole veel olemas, valige toimingupaanil suvand **Uus**, et lisada ruudustikku uus rida, ning sätestage see järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2a06d-177">If the query row you need doesn't exist yet, select **New** on the Action Pane to add a new row to the grid and make the following settings for it:</span></span>
    - <span data-ttu-id="2a06d-178">**Nimi** – sisestage selle rea nimi.</span><span class="sxs-lookup"><span data-stu-id="2a06d-178">**Name** - Enter a name for this row.</span></span>
    - <span data-ttu-id="2a06d-179">**Kirjeldus** – kirjeldage lühidalt päringut ja milleks see on.</span><span class="sxs-lookup"><span data-stu-id="2a06d-179">**Description** - Briefly describe the query and what it is for.</span></span>
    - <span data-ttu-id="2a06d-180">**Hinnamudel** – valige [hinnamudel](#build-price-model) (praegusest konfiguratsiooni mudelist), mida päring käivitamisel rakendab.</span><span class="sxs-lookup"><span data-stu-id="2a06d-180">**Price model** - Select a [price model](#build-price-model) (from the current configuration model) that the query will apply when triggered.</span></span>
    - <span data-ttu-id="2a06d-181">**Tellimuse tüüp** – valige tellimuse tüüp, mille puhul päring rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="2a06d-181">**Order type** - Select the type of order where the query will apply.</span></span>
    - <span data-ttu-id="2a06d-182">**Kehtiv alates** – määrake esimene kuupäev, millal päring rakendub.</span><span class="sxs-lookup"><span data-stu-id="2a06d-182">**Valid from** - Specify the first day when the query will apply.</span></span>
    - <span data-ttu-id="2a06d-183">**Aegub** – määrake päringu rakendumise viimane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2a06d-183">**Expire by** - Specify the last date when the query will apply.</span></span>

    <span data-ttu-id="2a06d-184">![Hinnamudeli kriteeriumid](media/prod-config-price-model-criteria.png "Hinnamudeli kriteeriumid")</span><span class="sxs-lookup"><span data-stu-id="2a06d-184">![Price model criteria](media/prod-config-price-model-criteria.png "Price model criteria")</span></span>

1. <span data-ttu-id="2a06d-185">Valige päringu rida, mida soovite määratleda, ja seejärel valige **toimingupaanil** suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-185">Select the row for the query you want to define and then select **Edit** on the **Action Pane**.</span></span> <span data-ttu-id="2a06d-186">Avaneb päringukujundaja dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="2a06d-186">The query designer dialog box opens.</span></span> <span data-ttu-id="2a06d-187">See toimib nagu enamik päringukujundajaid rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2a06d-187">It works like most query designers in Supply Chain Management.</span></span> <span data-ttu-id="2a06d-188">Kasutage seda, et määratleda tingimused, mille alusel tuleks valitud rea puhul hinnamudelit rakendada.</span><span class="sxs-lookup"><span data-stu-id="2a06d-188">Use it to define the conditions under which the price model for the row you selected should be applied.</span></span>

1. <span data-ttu-id="2a06d-189">Korrake samme 4‑5 iga päringu puhul, mida teil vaja on.</span><span class="sxs-lookup"><span data-stu-id="2a06d-189">Repeat steps 4-5 for each query you require.</span></span>
    > [!TIP]
    > <span data-ttu-id="2a06d-190">Saate säästa aega, kopeerides olemasoleva rea, mis on juba sarnane uuega, mida teil on vaja lisada.</span><span class="sxs-lookup"><span data-stu-id="2a06d-190">You can save time by copying an existing row that is already similar to a new one that you need to add.</span></span> <span data-ttu-id="2a06d-191">Selleks valige sihtrida ja seejärel toimingupaanilt **Dubleeri**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-191">To do this, select a target row and then select **Duplicate** on the Action Pane.</span></span>

1. <span data-ttu-id="2a06d-192">Kui olete kriteeriumide seadistamise lõpetanud, pange need loendis **Hinnamudeli kriteeriumid** õigesse järjekorda.</span><span class="sxs-lookup"><span data-stu-id="2a06d-192">When you have finished setting up your criteria, arrange them into the proper order in the **Price model criteria** list.</span></span> <span data-ttu-id="2a06d-193">Rea ümberpaigutamiseks valige rida ja seejärel toimingupaanilt **Üles** või **Alla**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-193">To reposition a row, select the row and then select **Up** or **Down** on the Action Pane.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2a06d-194">Konfigureerimise ajal alustab süsteem otsingut loendi algusest ja kasutab esimest päringut, mis ühtib pakkumise või tellimuse rea andmetega.</span><span class="sxs-lookup"><span data-stu-id="2a06d-194">At configuration time, the system starts searching from the top of the list and uses the first query that matches the data on the quote or the order line.</span></span> <span data-ttu-id="2a06d-195">Seetõttu peate panema oma kõige täpsemad päringud ülevale.</span><span class="sxs-lookup"><span data-stu-id="2a06d-195">Therefore, you must put your most specific queries on top.</span></span> <span data-ttu-id="2a06d-196">Kui paigutate loendi algusesse üldise päringu, kasutatakse seda ka siis, kui loendis on allpool mõni päring, mis kehtib täpselt selle konfiguratsiooni kliendi või potentsiaalse kliendi puhul.</span><span class="sxs-lookup"><span data-stu-id="2a06d-196">If you place a general query at the top of the list, this is the one that will be used even though there might be a query further down the list that targets the exact customer or prospect of the configuration.</span></span>

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a><span data-ttu-id="2a06d-197">Atribuudipõhiste müügihindade seadmine tootemudeli versiooni jaoks</span><span class="sxs-lookup"><span data-stu-id="2a06d-197">Set attribute-based sales prices for the product model version</span></span>

<span data-ttu-id="2a06d-198">Viimane samm on määrata tootemudeli versiooni jaoks atribuudipõhised müügihinnad.</span><span class="sxs-lookup"><span data-stu-id="2a06d-198">The final step is to specify attribute-based sales prices for the product model version.</span></span> <span data-ttu-id="2a06d-199">Selleks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2a06d-199">To do this:</span></span>

1. <span data-ttu-id="2a06d-200">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-200">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="2a06d-201">Valige sobiv tootekonfiguratsiooni mudel.</span><span class="sxs-lookup"><span data-stu-id="2a06d-201">Select the target product configuration model.</span></span>
1. <span data-ttu-id="2a06d-202">Valige toimingupaanil vahekaart **Mudel** ning valige rühmas **Hinnamudeli üksikasjad** suvand **Versioonid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-202">On the Action Pane, open the **Model** tab and, from the **Product model details** group, select **Versions**.</span></span>
1. <span data-ttu-id="2a06d-203">Avaneb leht **Versioonid**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-203">The **Versions** page opens.</span></span> <span data-ttu-id="2a06d-204">Veenduge, et suvandi **Hinnakujundusmeetod** väärtuseks oleks seatud **Atribuudipõhine**.</span><span class="sxs-lookup"><span data-stu-id="2a06d-204">Make sure the **Pricing method** is set to **Attribute based**.</span></span>
    <span data-ttu-id="2a06d-205">![Hinnakujundusmeetodi seadmine atribuudipõhiseks](media/prod-config-versions.png "Hinnakujundusmeetodi seadmine atribuudipõhiseks")</span><span class="sxs-lookup"><span data-stu-id="2a06d-205">![Set the pricing method to attribute based](media/prod-config-versions.png "Set the pricing method to attribute based")</span></span>