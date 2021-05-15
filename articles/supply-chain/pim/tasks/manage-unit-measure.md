---
title: Mõõtühikute haldamine
description: Selles teemas kirjeldatakse, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921337"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="9208a-103">Mõõtühikute haldamine</span><span class="sxs-lookup"><span data-stu-id="9208a-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9208a-104">Selles teemas kirjeldatakse, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.</span><span class="sxs-lookup"><span data-stu-id="9208a-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="9208a-105">Avage ühikute leht</span><span class="sxs-lookup"><span data-stu-id="9208a-105">Open the Units page</span></span>

<span data-ttu-id="9208a-106">Süsteemis saadaolevate mõõtühikute loomiseks ja tööks minge **organisatsioonihalduse \> häälestusüksuste \> ühikute \> üksusesse**.</span><span class="sxs-lookup"><span data-stu-id="9208a-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="9208a-107">Selle teema ülejäänud jaotised kirjeldavad, mida saate teha lehel **Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="9208a-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="9208a-108">Standardühikute ja teisenduste loomine</span><span class="sxs-lookup"><span data-stu-id="9208a-108">Create standard units and conversions</span></span>

<span data-ttu-id="9208a-109">Kui teie süsteem ei sisalda juba kõige sagedamini kasutatavaid mõõtühikuid meetermõõdustiku ja/või USA standardsüsteemi (USCS) jaoks, võib ühiku häälestusviisard aidata teil kiiresti baasühikumääratluste ja teisendustega alustada.</span><span class="sxs-lookup"><span data-stu-id="9208a-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="9208a-110">Viisardi lõpuleviimiseks valige **tegevuspaanil ühiku loomise viisard** ja järgige seejärel ekraanil olevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="9208a-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="9208a-111">Mõõtühiku loomine või redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9208a-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="9208a-112">Mõõtühiku loomiseks või redigeerimiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="9208a-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="9208a-113">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="9208a-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="9208a-114">Olemasoleva üksuse redigeerimiseks valige see loendipaanilt.</span><span class="sxs-lookup"><span data-stu-id="9208a-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="9208a-115">Uue ühiku loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9208a-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="9208a-116">Määrake uue kirje päises järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="9208a-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="9208a-117">**Ühik** – sisestage ID või sümbol, mida kasutada üksusele viitamiseks süsteemikeeles.</span><span class="sxs-lookup"><span data-stu-id="9208a-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="9208a-118">See ID või sümbol on tavaliselt ühiku tavaühend, nt *ea* igaühe või *cm* sentimeetri kohta.</span><span class="sxs-lookup"><span data-stu-id="9208a-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="9208a-119">**Kirjeldus** – Sisestage mõõtühikule süsteemikeeles kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="9208a-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="9208a-120">See nimi on tavaliselt üksuse täielik nimi, nt *Iga* või *Sentimeeter*.</span><span class="sxs-lookup"><span data-stu-id="9208a-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="9208a-121">Määrake kiirkaardil **Üldine** järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="9208a-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="9208a-122">**Ühiku klass** – valige atribuut, mida ühik mõõtühiku abil (nt pikkus, ala, mass või kogus).</span><span class="sxs-lookup"><span data-stu-id="9208a-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="9208a-123">**Ühikutesüsteem** – valige mõõtmissüsteem, kuhu ühik kuulub (*meetermõõdustiku ühikud* või *Ameerika Ühendriikide tavamõõdustiku ühikud*).</span><span class="sxs-lookup"><span data-stu-id="9208a-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="9208a-124">**Baasühik** – määrake see suvand väärtusele *Jah*, et kasutada praegust ühikut ühiku klassis baasühikuna.</span><span class="sxs-lookup"><span data-stu-id="9208a-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="9208a-125">Sel juhul peate sinult ühiku klassis määrama ainult baasühiku ja iga ühikuklassi lisaühiku vahelise teisendusteguri.</span><span class="sxs-lookup"><span data-stu-id="9208a-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="9208a-126">Süsteem saab seejärel läbi viia teisendusi kõikide selle ühiku klassi ühikute vahel.</span><span class="sxs-lookup"><span data-stu-id="9208a-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="9208a-127">Seepärast on teisenduste seadistamine lihtsam.</span><span class="sxs-lookup"><span data-stu-id="9208a-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="9208a-128">Näiteks kui gallon on *mahuühiku* klassi baasühik, peate seadistama teisendustegurid kvartilt gallonile ja pint-st gallonini.</span><span class="sxs-lookup"><span data-stu-id="9208a-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="9208a-129">Süsteem saab seejärel teisendada ka kvartilt pindiks.</span><span class="sxs-lookup"><span data-stu-id="9208a-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="9208a-130">Teil võib ühiku klassi kohta olla ainult üks baasühik.</span><span class="sxs-lookup"><span data-stu-id="9208a-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="9208a-131">**Süsteemi ühik** – määrake see suvand väärtusele *Jah*, et kasutada oletatavat ühikut ühiku kõigi täpsustamata mõõdete puhul.</span><span class="sxs-lookup"><span data-stu-id="9208a-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="9208a-132">Näiteks kui koguse sisestamiseks kasutatav väli ei luba ühikut määrata (kui kasutaja ei vali ühikut), kasutab süsteem ühikut, mis on määratud klassi *Kogus* süsteemiühikuks.</span><span class="sxs-lookup"><span data-stu-id="9208a-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="9208a-133">Teil võib ühiku klassi kohta olla ainult üks süsteemi ühik.</span><span class="sxs-lookup"><span data-stu-id="9208a-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="9208a-134">**Kümnendarvuline täpsus** – määrake komakohtade arv, milleni praeguse ühiku jaoks määratud või teisendatud väärtused tuleb ümardada.</span><span class="sxs-lookup"><span data-stu-id="9208a-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="9208a-135">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9208a-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="9208a-136">Ühiku teisenduste määratlemine</span><span class="sxs-lookup"><span data-stu-id="9208a-136">Define unit translations</span></span>

<span data-ttu-id="9208a-137">ID või sümboli tõlgete ja mõõtühiku kirjelduse määratlemiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="9208a-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="9208a-138">Looge või valige üksus, mille jaoks tõlkeid luua.</span><span class="sxs-lookup"><span data-stu-id="9208a-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="9208a-139">Valige toimingupaanil suvand **Ühiku tekstid**.</span><span class="sxs-lookup"><span data-stu-id="9208a-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="9208a-140">Kuvatakse **ühiku tekstid** tekstide leht.</span><span class="sxs-lookup"><span data-stu-id="9208a-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="9208a-141">Kasutate seda lehekülge, et määrata valitud üksuse ID või sümboli tõlked.</span><span class="sxs-lookup"><span data-stu-id="9208a-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="9208a-142">Neid tõlkeid saab seejärel kasutada välistes dokumentides kliendi- või hankijaspetsiifilistes keeltes.</span><span class="sxs-lookup"><span data-stu-id="9208a-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="9208a-143">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9208a-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9208a-144">Valige **keeleväljal** keel, millesse tuleb ühiku ID või sümbol tõlkida.</span><span class="sxs-lookup"><span data-stu-id="9208a-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="9208a-145">Sisestage väljale **Tekst** ühiku ID või sümboli tõlge valitud keeles.</span><span class="sxs-lookup"><span data-stu-id="9208a-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="9208a-146">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9208a-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9208a-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9208a-147">Close the page.</span></span>
1. <span data-ttu-id="9208a-148">Valige **Toimingupaanil** **Ümberarvestatud ühiku kirjeldused**.</span><span class="sxs-lookup"><span data-stu-id="9208a-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="9208a-149">Kuvatakse lehekülg **Tõlgitud ühiku kirjeldused**.</span><span class="sxs-lookup"><span data-stu-id="9208a-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="9208a-150">Kasutate seda lehekülge, et määrata valitud üksusele keelepõhiseid kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="9208a-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="9208a-151">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9208a-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9208a-152">Valige **keeleväljal** keel, millesse tuleb ühiku kirjeldus tõlkida.</span><span class="sxs-lookup"><span data-stu-id="9208a-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="9208a-153">Sisestage väljale **Kirjeldus** ühiku kirjelduse tõlge valitud keeles.</span><span class="sxs-lookup"><span data-stu-id="9208a-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="9208a-154">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9208a-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9208a-155">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9208a-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="9208a-156">Ühiku teisendamise reeglite määratlemine</span><span class="sxs-lookup"><span data-stu-id="9208a-156">Define unit conversion rules</span></span>

<span data-ttu-id="9208a-157">Mõõtühikute vaheliste teisendusreeglite määratlemiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="9208a-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="9208a-158">Looge või valige üksus, mille jaoks defineerida teisendusreegleid.</span><span class="sxs-lookup"><span data-stu-id="9208a-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="9208a-159">Valige toimingupaanilt suvand **Ühiku teisendused**.</span><span class="sxs-lookup"><span data-stu-id="9208a-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="9208a-160">Avaneb leht **Ühiku teisendused**.</span><span class="sxs-lookup"><span data-stu-id="9208a-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="9208a-161">Seda lehte kasutate, et defineerida reeglid valitud mõõtühiku teisendamiseks muudesse mõõtühikutesse valitud ühiku klassis.</span><span class="sxs-lookup"><span data-stu-id="9208a-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="9208a-162">Valige üks järgmistest vahekaartidest, sõltuvalt teisendustüübist, mida soovite seadistada:</span><span class="sxs-lookup"><span data-stu-id="9208a-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="9208a-163">**Standardsed teisendused** – saate seadistada kõigi toodete standardsed teisendusreeglid.</span><span class="sxs-lookup"><span data-stu-id="9208a-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="9208a-164">**Klassisisesed teisendused** – saate seadistada tootepõhised teisendusreeglid ühikute jaoks samas ühikuklassis.</span><span class="sxs-lookup"><span data-stu-id="9208a-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="9208a-165">**Klassisisesed teisendused** – saate seadistada tootepõhised teisendusreeglid ühikute jaoks üle ühikuklasside.</span><span class="sxs-lookup"><span data-stu-id="9208a-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="9208a-166">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="9208a-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="9208a-167">Uue teisenduse loomiseks valige tööriistaribalt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9208a-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="9208a-168">Olemasoleva teisenduse redigeerimiseks valige teisendus ruudustikus ja seejärel valige tööriistaribal **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="9208a-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="9208a-169">Määrake järgmised väljad kuvatavas ripp-dialoogiboksis.</span><span class="sxs-lookup"><span data-stu-id="9208a-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="9208a-170">**Toode** – valige konkreetne toode, mille suhtes teisendus kehtib.</span><span class="sxs-lookup"><span data-stu-id="9208a-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="9208a-171">See väli on saadaval ainult klassisiseste ja klassisiseste teisenduste puhul.</span><span class="sxs-lookup"><span data-stu-id="9208a-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="9208a-172">**Valemi paigutus** – jätke selle välja väärtuseks *Lihtne*, et määrata lihtne teisendamine, sel on üks tegur.</span><span class="sxs-lookup"><span data-stu-id="9208a-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="9208a-173">Seadistage see väärtusele *Täpsem*, et seadistada keerukam võrrand.</span><span class="sxs-lookup"><span data-stu-id="9208a-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="9208a-174">Täpsemate võrrandite vorming erineb olenevalt ühiku klassist.</span><span class="sxs-lookup"><span data-stu-id="9208a-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="9208a-175">**Vormi ühik** – sellel väljal kuvatakse valitud ühik.</span><span class="sxs-lookup"><span data-stu-id="9208a-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="9208a-176">Tavaliselt ei tohi te seda väärtust muuta.</span><span class="sxs-lookup"><span data-stu-id="9208a-176">Usually, you should not change the value.</span></span> <span data-ttu-id="9208a-177">(Kui muudate väärtust, peate avama väärtuse valitud ühiku **ühikuteisenduste** leht, et pärast salvestamist vaadata oma uut teisendust.)</span><span class="sxs-lookup"><span data-stu-id="9208a-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="9208a-178">**Ühikuks** – valige ühik, milleks teisendada.</span><span class="sxs-lookup"><span data-stu-id="9208a-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="9208a-179">**Ümardamine** – valige, kuidas murrud ümardada, võttes aluseks valitud ühiku **kümnendarvuline** täpsusväärtus (*Lähimani* *Üles* või *Alla*).</span><span class="sxs-lookup"><span data-stu-id="9208a-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="9208a-180">**Teisendusvalem** – kasutage rippmenüü ülemises ülaosas allesolevaid välju kahe ühiku vahelise teisendamise valemi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="9208a-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="9208a-181">Saadaolevad väljad varieeruvad sõltuvalt valitud ühiku klassist ja valemi kavandist.</span><span class="sxs-lookup"><span data-stu-id="9208a-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="9208a-182">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9208a-182">Select **OK**.</span></span>
1. <span data-ttu-id="9208a-183">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9208a-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="9208a-184">Samuti saate seadistada ühikuteisendused tootevariandi kohta.</span><span class="sxs-lookup"><span data-stu-id="9208a-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="9208a-185">Lisateavet saate jaotisest [Mõõtühiku teisendus tootevariandi kohta](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="9208a-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
