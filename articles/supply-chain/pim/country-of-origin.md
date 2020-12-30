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
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425922"
---
# <a name="country-of-origin"></a><span data-ttu-id="04ee6-105">Päritoluriik</span><span class="sxs-lookup"><span data-stu-id="04ee6-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="04ee6-106">Paljud organisatsioonid väljastavad oma hankijatele sertifikaate, et tagada toodete vastavuse kindlatele sertifitseerimisstandarditele.</span><span class="sxs-lookup"><span data-stu-id="04ee6-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="04ee6-107">Need sertifikaadid sõltuvad sageli päritoluriigist.</span><span class="sxs-lookup"><span data-stu-id="04ee6-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="04ee6-108">Päritoluriigi funktsioon võimaldab teil seostada toodet selle päritoluriigiga ja jälgida toote sertifikatsioone.</span><span class="sxs-lookup"><span data-stu-id="04ee6-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="04ee6-109">Päritoluriigi funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="04ee6-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="04ee6-110">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="04ee6-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="04ee6-111">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="04ee6-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="04ee6-112">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="04ee6-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="04ee6-113">**Moodul:** *Tooteteabe haldus*</span><span class="sxs-lookup"><span data-stu-id="04ee6-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="04ee6-114">**Funktsiooni nimi:** *päritoluriigi haldamise funktsioon*</span><span class="sxs-lookup"><span data-stu-id="04ee6-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="04ee6-115">Lähte- ja sihtkriikide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="04ee6-115">Configure source and destination countries</span></span>

<span data-ttu-id="04ee6-116">Enne tootele sertifikatsiooni väljastamist, peate linkima toote selle sihtriigi ja päritoluriigiga.</span><span class="sxs-lookup"><span data-stu-id="04ee6-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="04ee6-117">Avage jaotis **Tooteteabe haldus \> Seadistamine \> Toote vastavus \> Päritoluriik \> Päritoluriigi reeglid**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="04ee6-118">Valige redigeerimiseks olemasolev riigi häälestus või valige toimingupaanilt **Uus** uue riigi häälestuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="04ee6-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="04ee6-119">Määrake valitud või uue riigi jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04ee6-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="04ee6-120">Väli</span><span class="sxs-lookup"><span data-stu-id="04ee6-120">Field</span></span> | <span data-ttu-id="04ee6-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="04ee6-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="04ee6-122">Kauba number</span><span class="sxs-lookup"><span data-stu-id="04ee6-122">Item number</span></span> | <span data-ttu-id="04ee6-123">Valige toote kaubakood.</span><span class="sxs-lookup"><span data-stu-id="04ee6-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="04ee6-124">Sihtriik</span><span class="sxs-lookup"><span data-stu-id="04ee6-124">Destination country</span></span> | <span data-ttu-id="04ee6-125">Valige riik, kuhu te toote saadate.</span><span class="sxs-lookup"><span data-stu-id="04ee6-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="04ee6-126">Päritoluriik</span><span class="sxs-lookup"><span data-stu-id="04ee6-126">Origin country</span></span> | <span data-ttu-id="04ee6-127">Valige riik, kust te toodet saadate.</span><span class="sxs-lookup"><span data-stu-id="04ee6-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="04ee6-128">Selle seadistuse eesmärk on aidata teil luua koosluste aruanne, kus saate lisada päritoluriigi igale osale, mille jaoks lähte-ja sihtriigid määratakse.</span><span class="sxs-lookup"><span data-stu-id="04ee6-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="04ee6-129">See aruanne aitab teil saada terviklikku ülevaadet sellest, kust teie osad pärit on ja kuhu need lähevad.</span><span class="sxs-lookup"><span data-stu-id="04ee6-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="04ee6-130">Hankija sertifikaatide jälgimine</span><span class="sxs-lookup"><span data-stu-id="04ee6-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="04ee6-131">Saate kasutada lehte **Päritoluriigi hankija sertifikaadid**, et jälgida hankijatele väljastatavaid sertifikaate.</span><span class="sxs-lookup"><span data-stu-id="04ee6-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="04ee6-132">Peate otsustama, milliseid sertifikaadi dokumente te väljastate ja kuidas te neid klientidele teatate.</span><span class="sxs-lookup"><span data-stu-id="04ee6-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="04ee6-133">See funktsioon annab teile sertifikaatidest ülevaate.</span><span class="sxs-lookup"><span data-stu-id="04ee6-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="04ee6-134">Samuti saate valida, kas vastavad sertifikaadi numbrid kuvatakse arvetel, saatelehtedel ja/või tellimuse kinnitustel.</span><span class="sxs-lookup"><span data-stu-id="04ee6-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="04ee6-135">Sertifikaadi teabe häälestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="04ee6-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="04ee6-136">Avage jaotis **Tooteteabe haldus \> Seadistamine \> Toote vastavus \> Päritoluriik \> Päritoluriigi hankija sertifikaadid**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="04ee6-137">Valige redigeerimiseks olemasolev sertifikaadi häälestus või valige toimingupaanilt **Uus** uue sertifikaadi häälestuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="04ee6-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="04ee6-138">Määrake valitud või uue sertifikaadi jaoks järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="04ee6-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="04ee6-139">Väli</span><span class="sxs-lookup"><span data-stu-id="04ee6-139">Field</span></span> | <span data-ttu-id="04ee6-140">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="04ee6-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="04ee6-141">Hankija konto</span><span class="sxs-lookup"><span data-stu-id="04ee6-141">Vendor account</span></span> | <span data-ttu-id="04ee6-142">Valige hankija, kellele väljastasite sertifikaadi.</span><span class="sxs-lookup"><span data-stu-id="04ee6-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="04ee6-143">Kauba number</span><span class="sxs-lookup"><span data-stu-id="04ee6-143">Item number</span></span> | <span data-ttu-id="04ee6-144">Valige kaup, millele väljastasite sertifikaadi.</span><span class="sxs-lookup"><span data-stu-id="04ee6-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="04ee6-145">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="04ee6-145">Country/region</span></span> | <span data-ttu-id="04ee6-146">Sihtriik või -piirkond, kus peate seda sertifikaati kasutama.</span><span class="sxs-lookup"><span data-stu-id="04ee6-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="04ee6-147">Serdi number</span><span class="sxs-lookup"><span data-stu-id="04ee6-147">Certificate number</span></span> | <span data-ttu-id="04ee6-148">Sisestage väljastatud sertifikaadi ID-number.</span><span class="sxs-lookup"><span data-stu-id="04ee6-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="04ee6-149">Jõustunud</span><span class="sxs-lookup"><span data-stu-id="04ee6-149">Effective</span></span> | <span data-ttu-id="04ee6-150">Valige praeguse sertifikaadi kehtivuse esimene kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04ee6-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="04ee6-151">Aegumine</span><span class="sxs-lookup"><span data-stu-id="04ee6-151">Expiration</span></span> | <span data-ttu-id="04ee6-152">Valige praeguse sertifikaadi kehtivuse viimane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04ee6-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="04ee6-153">Arvele printimine</span><span class="sxs-lookup"><span data-stu-id="04ee6-153">Print on invoice</span></span> | <span data-ttu-id="04ee6-154">Märkige see ruut, et printida sertifikaadi number arvetele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul.</span><span class="sxs-lookup"><span data-stu-id="04ee6-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="04ee6-155">Saatelehele printimine</span><span class="sxs-lookup"><span data-stu-id="04ee6-155">Print on packing slip</span></span> | <span data-ttu-id="04ee6-156">Märkige see ruut, et printida sertifikaadi number saatelehtedele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul.</span><span class="sxs-lookup"><span data-stu-id="04ee6-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="04ee6-157">Müügitellimusele printimine</span><span class="sxs-lookup"><span data-stu-id="04ee6-157">Print on sales order</span></span> | <span data-ttu-id="04ee6-158">Märkige see ruut, et printida sertifikaadi number müügitellimustele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul.</span><span class="sxs-lookup"><span data-stu-id="04ee6-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="04ee6-159">Päritoluriigi koosluse aruannete lisamine</span><span class="sxs-lookup"><span data-stu-id="04ee6-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="04ee6-160">Kui loote koosluse aruande, saate lisada päritoluriigi igale osale, millele määrasite lähte- ja sihtriiriigid lehel **Päritoluriigi reeglid**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="04ee6-161">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="04ee6-162">Valige või looge toode, et avada selle leht **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="04ee6-163">Tehke tegumiriba vahekaardil **Projekteeri** grupis **Kooslus** valik **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="04ee6-164">Valige kuvatava lehe toimingupaanilt **Kooslus \> Prindi**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="04ee6-165">Määrake dialoogiboksi **Koosluse read** väljale **Sihtriik** see sihtriik, mida soovite oma aruandes kuvada.</span><span class="sxs-lookup"><span data-stu-id="04ee6-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="04ee6-166">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="04ee6-166">Select **OK**.</span></span>

<span data-ttu-id="04ee6-167">Luuakse ja kuvatakse aruanne teabega iga osa päritoluriigi kohta.</span><span class="sxs-lookup"><span data-stu-id="04ee6-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="04ee6-168">Siin on aruande näide.</span><span class="sxs-lookup"><span data-stu-id="04ee6-168">Here is an example of the report.</span></span>

<span data-ttu-id="04ee6-169">![Päritoluriigi aruanne](media/country-of-origin-report.png "Päritoluriigi aruanne")</span><span class="sxs-lookup"><span data-stu-id="04ee6-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
