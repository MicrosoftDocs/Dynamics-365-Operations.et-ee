---
title: Registreerimismärgi sildi printimise lubamine
description: Selles teemas näidatakse, kuidas lubada SSCC (serial shipping conteiner code) sildi automaatne printimine pärast seda, kui viimane üksus on müügivalimise tööprotsessis laost valitud.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a608e9a2356f9dd49bbec1bcbe5489af5931d44
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830878"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="1998f-103">Registreerimismärgi sildi printimise lubamine</span><span class="sxs-lookup"><span data-stu-id="1998f-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1998f-104">Selles teemas näidatakse, kuidas lubada SSCC (serial shipping conteiner code) sildi automaatne printimine pärast seda, kui viimane üksus on müügivalimise tööprotsessis laost valitud.</span><span class="sxs-lookup"><span data-stu-id="1998f-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="1998f-105">Võite seda protseduuri käitada demoettevõtte USMF-i andmetega.</span><span class="sxs-lookup"><span data-stu-id="1998f-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="1998f-106">Kui käitate seda omaenda andmeid kasutades, peaksite määrama litsentsiplaatide numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="1998f-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="1998f-107">Enne ülesande juurde asumist peaksite määrama sildiprinteri.</span><span class="sxs-lookup"><span data-stu-id="1998f-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="1998f-108">Avage Organisatsiooni haldus > Seadistus > Võrguprinterid.</span><span class="sxs-lookup"><span data-stu-id="1998f-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="1998f-109">Klõpsake Toimingupaanil Suvandid, seejärel klõpsake nuppu Laadi dokumendi marsruudivaliku agendi installer alla.</span><span class="sxs-lookup"><span data-stu-id="1998f-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="1998f-110">Käitage installer ja veenduge enne protseduuriga jätkamist, et töötav võrguprinter on seatud olekusse Aktiivne.</span><span class="sxs-lookup"><span data-stu-id="1998f-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="1998f-111">GS1 ettevõtteprefiksi seadistus</span><span class="sxs-lookup"><span data-stu-id="1998f-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="1998f-112">Minge **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1998f-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="1998f-113">Sisestage väljale **GS1 ettevõtte eesliide** oma GS1 ettevõtte numbri 7 numbrit.</span><span class="sxs-lookup"><span data-stu-id="1998f-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="1998f-114">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1998f-114">Select **Save**.</span></span>
4. <span data-ttu-id="1998f-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1998f-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="1998f-116">SSCC-identifitseerimisnumbri numbriseeria seadistus</span><span class="sxs-lookup"><span data-stu-id="1998f-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="1998f-117">Avage **Navigeerimispaan > Moodulid > Organisatsiooni haldus > Numbriseeriad > Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="1998f-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="1998f-118">Väljal **Ala** valige sobiv valik.</span><span class="sxs-lookup"><span data-stu-id="1998f-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="1998f-119">Väljal **Viide** valige sobiv valik.</span><span class="sxs-lookup"><span data-stu-id="1998f-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="1998f-120">Sisestage väärtus väljale **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="1998f-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="1998f-121">Laiendage jaotist **Segmendid**.</span><span class="sxs-lookup"><span data-stu-id="1998f-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="1998f-122">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1998f-122">Select **Edit**.</span></span>
7. <span data-ttu-id="1998f-123">Tabelis **Segmendid** valige esimene rida</span><span class="sxs-lookup"><span data-stu-id="1998f-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="1998f-124">Valige **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="1998f-124">Select **Remove**.</span></span>
9. <span data-ttu-id="1998f-125">Valige **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="1998f-125">Select **Remove**.</span></span>
10. <span data-ttu-id="1998f-126">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1998f-126">Select **Save**.</span></span>
11. <span data-ttu-id="1998f-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1998f-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="1998f-128">Dokumendi marsruudivaliku paigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="1998f-128">Create the document route layout</span></span>
1. <span data-ttu-id="1998f-129">Avage **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Dokumentide suunamine > Dokumentide suunamise paigutused**.</span><span class="sxs-lookup"><span data-stu-id="1998f-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="1998f-130">Saate lubada SSCC-paigutuse.</span><span class="sxs-lookup"><span data-stu-id="1998f-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="1998f-131">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1998f-131">Select **New**.</span></span>
3. <span data-ttu-id="1998f-132">Sisestage väärtus väljale **Paigutuse ID**.</span><span class="sxs-lookup"><span data-stu-id="1998f-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="1998f-133">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="1998f-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1998f-134">Valige **Lisa teksti lõppu**.</span><span class="sxs-lookup"><span data-stu-id="1998f-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="1998f-135">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1998f-135">Select **Save**.</span></span>
7. <span data-ttu-id="1998f-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1998f-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="1998f-137">Dokumendi marsruudivaliku häälestamine</span><span class="sxs-lookup"><span data-stu-id="1998f-137">Set up the document routing</span></span>
1. <span data-ttu-id="1998f-138">Avage **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Dokumentide suunamine > Dokumentide suunamine**.</span><span class="sxs-lookup"><span data-stu-id="1998f-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="1998f-139">Väljal **Töökäsu tüüp** valige sobiv valik.</span><span class="sxs-lookup"><span data-stu-id="1998f-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="1998f-140">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1998f-140">Select **New**.</span></span>
4. <span data-ttu-id="1998f-141">Sisestage väärtus väljale **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="1998f-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="1998f-142">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="1998f-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="1998f-143">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1998f-143">Select **New**.</span></span>
7. <span data-ttu-id="1998f-144">Väljale **Paigutuse ID** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1998f-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="1998f-145">Sisestage väljale **Nimi** printeri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="1998f-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="1998f-146">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1998f-146">Select **Save**.</span></span>
10. <span data-ttu-id="1998f-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1998f-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="1998f-148">Mobiilse seadme menüü loomine</span><span class="sxs-lookup"><span data-stu-id="1998f-148">Create mobile device menu</span></span>
1. <span data-ttu-id="1998f-149">Avage **Navigeerimispaan avage Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="1998f-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="1998f-150">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1998f-150">Select **New**.</span></span>
3. <span data-ttu-id="1998f-151">Sisestage väärtus väljale **Menüü-üksuse nimi**.</span><span class="sxs-lookup"><span data-stu-id="1998f-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="1998f-152">Sisestage väärtus väljale **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="1998f-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="1998f-153">Väljal **Režiim** valige sobiv valik.</span><span class="sxs-lookup"><span data-stu-id="1998f-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="1998f-154">Valige väärtus **Jah** väljal **Kasuta olemasolevat tööd**.</span><span class="sxs-lookup"><span data-stu-id="1998f-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="1998f-155">Valige väärtus **Jah** väljal **Loo litsentsi plaat**.</span><span class="sxs-lookup"><span data-stu-id="1998f-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="1998f-156">Laiendage jaotist **Tööklassid**.</span><span class="sxs-lookup"><span data-stu-id="1998f-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="1998f-157">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1998f-157">Select **New**.</span></span>
10. <span data-ttu-id="1998f-158">Väljale **Tööklassi ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="1998f-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="1998f-159">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1998f-159">Select **Save**.</span></span>
12. <span data-ttu-id="1998f-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1998f-160">Close the page.</span></span>
13. <span data-ttu-id="1998f-161">Avage **Navigeerimispaan avage Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="1998f-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="1998f-162">Valige puus menüüelement, mille olete varem loonud.</span><span class="sxs-lookup"><span data-stu-id="1998f-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="1998f-163">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1998f-163">Select **Edit**.</span></span>
16. <span data-ttu-id="1998f-164">Menüüelemendi menüüsse lisamiseks valige nool.</span><span class="sxs-lookup"><span data-stu-id="1998f-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="1998f-165">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1998f-165">Select **Save**.</span></span>
18. <span data-ttu-id="1998f-166">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1998f-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="1998f-167">Töömalli värskendus</span><span class="sxs-lookup"><span data-stu-id="1998f-167">Update a work template</span></span>
1. <span data-ttu-id="1998f-168">Minge **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Töö > Töö mallid**.</span><span class="sxs-lookup"><span data-stu-id="1998f-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="1998f-169">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1998f-169">Select **Edit**.</span></span>
3. <span data-ttu-id="1998f-170">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1998f-170">Select **New**.</span></span>
4. <span data-ttu-id="1998f-171">Väljal **Töö tüüp** valige **Prindi**.</span><span class="sxs-lookup"><span data-stu-id="1998f-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="1998f-172">Väljal **Tööklassi ID** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1998f-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="1998f-173">Valige **Nihuta üles**.</span><span class="sxs-lookup"><span data-stu-id="1998f-173">Select **Move up**.</span></span>
7. <span data-ttu-id="1998f-174">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1998f-174">Select **Save**.</span></span>
8. <span data-ttu-id="1998f-175">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1998f-175">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]