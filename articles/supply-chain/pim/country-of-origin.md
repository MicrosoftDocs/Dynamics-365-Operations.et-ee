---
title: Päritoluriik
description: Paljud organisatsioonid väljastavad oma hankijatele sertifikaate, et tagada toodete vastavuse kindlatele sertifitseerimisstandarditele. Need sertifikaadid sõltuvad sageli päritoluriigist. Selles teemas antakse teavet päritoluriigi funktsiooni kohta, mis võimaldab teil seostada toodet selle päritoluriigiga ja jälgida toote sertifikatsioone.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596222"
---
# <a name="country-of-origin"></a><span data-ttu-id="20742-105">Päritoluriik</span><span class="sxs-lookup"><span data-stu-id="20742-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20742-106">Paljud organisatsioonid väljastavad oma hankijatele sertifikaate, et tagada toodete vastavuse kindlatele sertifitseerimisstandarditele.</span><span class="sxs-lookup"><span data-stu-id="20742-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="20742-107">Need sertifikaadid sõltuvad sageli päritoluriigist.</span><span class="sxs-lookup"><span data-stu-id="20742-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="20742-108">Päritoluriigi funktsioon võimaldab teil seostada toodet selle päritoluriigiga ja jälgida toote sertifikatsioone.</span><span class="sxs-lookup"><span data-stu-id="20742-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="20742-109">Lähte- ja sihtkriikide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="20742-109">Configure source and destination countries</span></span>

<span data-ttu-id="20742-110">Enne tootele sertifikatsiooni väljastamist, peate linkima toote selle sihtriigi ja päritoluriigiga.</span><span class="sxs-lookup"><span data-stu-id="20742-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="20742-111">Avage jaotis **Tooteteabe haldus \> Seadistamine \> Toote vastavus \> Päritoluriik \> Päritoluriigi reeglid**.</span><span class="sxs-lookup"><span data-stu-id="20742-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="20742-112">Valige redigeerimiseks olemasolev riigi häälestus või valige toimingupaanilt **Uus** uue riigi häälestuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="20742-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="20742-113">Määrake valitud või uue riigi jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="20742-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="20742-114">Field</span><span class="sxs-lookup"><span data-stu-id="20742-114">Field</span></span> | <span data-ttu-id="20742-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="20742-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="20742-116">Kauba number</span><span class="sxs-lookup"><span data-stu-id="20742-116">Item number</span></span> | <span data-ttu-id="20742-117">Valige toote kaubakood.</span><span class="sxs-lookup"><span data-stu-id="20742-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="20742-118">Sihtriik</span><span class="sxs-lookup"><span data-stu-id="20742-118">Destination country</span></span> | <span data-ttu-id="20742-119">Valige riik, kuhu te toote saadate.</span><span class="sxs-lookup"><span data-stu-id="20742-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="20742-120">Päritoluriik</span><span class="sxs-lookup"><span data-stu-id="20742-120">Origin country</span></span> | <span data-ttu-id="20742-121">Valige riik, kust te toodet saadate.</span><span class="sxs-lookup"><span data-stu-id="20742-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="20742-122">Selle seadistuse eesmärk on aidata teil luua koosluste aruanne, kus saate lisada päritoluriigi igale osale, mille jaoks lähte-ja sihtriigid määratakse.</span><span class="sxs-lookup"><span data-stu-id="20742-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="20742-123">See aruanne aitab teil saada terviklikku ülevaadet sellest, kust teie osad pärit on ja kuhu need lähevad.</span><span class="sxs-lookup"><span data-stu-id="20742-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="20742-124">Hankija sertifikaatide jälgimine</span><span class="sxs-lookup"><span data-stu-id="20742-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="20742-125">Saate kasutada lehte **Päritoluriigi hankija sertifikaadid**, et jälgida hankijatele väljastatavaid sertifikaate.</span><span class="sxs-lookup"><span data-stu-id="20742-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="20742-126">Peate otsustama, milliseid sertifikaadi dokumente te väljastate ja kuidas te neid klientidele teatate.</span><span class="sxs-lookup"><span data-stu-id="20742-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="20742-127">See funktsioon annab teile sertifikaatidest ülevaate.</span><span class="sxs-lookup"><span data-stu-id="20742-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="20742-128">Samuti saate valida, kas vastavad sertifikaadi numbrid kuvatakse arvetel, saatelehtedel ja/või tellimuse kinnitustel.</span><span class="sxs-lookup"><span data-stu-id="20742-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="20742-129">Sertifikaadi teabe häälestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="20742-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="20742-130">Avage jaotis **Tooteteabe haldus \> Seadistamine \> Toote vastavus \> Päritoluriik \> Päritoluriigi hankija sertifikaadid**.</span><span class="sxs-lookup"><span data-stu-id="20742-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="20742-131">Valige redigeerimiseks olemasolev sertifikaadi häälestus või valige toimingupaanilt **Uus** uue sertifikaadi häälestuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="20742-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="20742-132">Määrake valitud või uue sertifikaadi jaoks järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="20742-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="20742-133">Field</span><span class="sxs-lookup"><span data-stu-id="20742-133">Field</span></span> | <span data-ttu-id="20742-134">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="20742-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="20742-135">Hankija konto</span><span class="sxs-lookup"><span data-stu-id="20742-135">Vendor account</span></span> | <span data-ttu-id="20742-136">Valige hankija, kellele väljastasite sertifikaadi.</span><span class="sxs-lookup"><span data-stu-id="20742-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="20742-137">Kauba number</span><span class="sxs-lookup"><span data-stu-id="20742-137">Item number</span></span> | <span data-ttu-id="20742-138">Valige kaup, millele väljastasite sertifikaadi.</span><span class="sxs-lookup"><span data-stu-id="20742-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="20742-139">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="20742-139">Country/region</span></span> | <span data-ttu-id="20742-140">Sihtriik või -piirkond, kus peate seda sertifikaati kasutama.</span><span class="sxs-lookup"><span data-stu-id="20742-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="20742-141">Serdi number</span><span class="sxs-lookup"><span data-stu-id="20742-141">Certificate number</span></span> | <span data-ttu-id="20742-142">Sisestage väljastatud sertifikaadi ID-number.</span><span class="sxs-lookup"><span data-stu-id="20742-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="20742-143">Jõustunud</span><span class="sxs-lookup"><span data-stu-id="20742-143">Effective</span></span> | <span data-ttu-id="20742-144">Valige praeguse sertifikaadi kehtivuse esimene kuupäev.</span><span class="sxs-lookup"><span data-stu-id="20742-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="20742-145">Aegumine</span><span class="sxs-lookup"><span data-stu-id="20742-145">Expiration</span></span> | <span data-ttu-id="20742-146">Valige praeguse sertifikaadi kehtivuse viimane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="20742-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="20742-147">Arvele printimine</span><span class="sxs-lookup"><span data-stu-id="20742-147">Print on invoice</span></span> | <span data-ttu-id="20742-148">Märkige see ruut, et printida sertifikaadi number arvetele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul.</span><span class="sxs-lookup"><span data-stu-id="20742-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="20742-149">Saatelehele printimine</span><span class="sxs-lookup"><span data-stu-id="20742-149">Print on packing slip</span></span> | <span data-ttu-id="20742-150">Märkige see ruut, et printida sertifikaadi number saatelehtedele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul.</span><span class="sxs-lookup"><span data-stu-id="20742-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="20742-151">Müügitellimusele printimine</span><span class="sxs-lookup"><span data-stu-id="20742-151">Print on sales order</span></span> | <span data-ttu-id="20742-152">Märkige see ruut, et printida sertifikaadi number müügitellimustele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul.</span><span class="sxs-lookup"><span data-stu-id="20742-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="20742-153">Päritoluriigi koosluse aruannete lisamine</span><span class="sxs-lookup"><span data-stu-id="20742-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="20742-154">Kui loote koosluse aruande, saate lisada päritoluriigi igale osale, millele määrasite lähte- ja sihtriiriigid lehel **Päritoluriigi reeglid**.</span><span class="sxs-lookup"><span data-stu-id="20742-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="20742-155">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="20742-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="20742-156">Valige või looge toode, et avada selle leht **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="20742-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="20742-157">Tehke tegumiriba vahekaardil **Projekteeri** grupis **Kooslus** valik **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="20742-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="20742-158">Valige kuvatava lehe toimingupaanilt **Kooslus \> Prindi**.</span><span class="sxs-lookup"><span data-stu-id="20742-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="20742-159">Määrake dialoogiboksi **Koosluse read** väljale **Sihtriik** see sihtriik, mida soovite oma aruandes kuvada.</span><span class="sxs-lookup"><span data-stu-id="20742-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="20742-160">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="20742-160">Select **OK**.</span></span>

<span data-ttu-id="20742-161">Luuakse ja kuvatakse aruanne teabega iga osa päritoluriigi kohta.</span><span class="sxs-lookup"><span data-stu-id="20742-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="20742-162">Siin on aruande näide.</span><span class="sxs-lookup"><span data-stu-id="20742-162">Here is an example of the report.</span></span>

<span data-ttu-id="20742-163">![Päritoluriigi aruanne](media/country-of-origin-report.png "Päritoluriigi aruanne")</span><span class="sxs-lookup"><span data-stu-id="20742-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
