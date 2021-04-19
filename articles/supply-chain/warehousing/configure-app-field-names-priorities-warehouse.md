---
title: Laohalduse mobiilirakenduse Warehouse Management väljade konfigureerimine
description: See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamise mobiilirakenduse Warehouse Management kuvatud väljade nimesid ja prioriteete.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808818"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="57469-103">Laohalduse mobiilirakenduse Warehouse Management väljade konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="57469-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57469-104">See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamise mobiilirakenduse Warehouse Management kuvatud väljade nimesid ja prioriteete.</span><span class="sxs-lookup"><span data-stu-id="57469-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="57469-105">See teema kehtib laohalduse funktsioonidele.</span><span class="sxs-lookup"><span data-stu-id="57469-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="57469-106">See ei kehti funktsioonidele moodulis Varude haldus.</span><span class="sxs-lookup"><span data-stu-id="57469-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="57469-107">Mobiilirakendus Warehouse Management on rakendus, mille abil saate täita laos vajalikke ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="57469-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="57469-108">Saate määratleda ja konfigureerida rakenduses kasutatavaid väljanimetusi, samuti konfigureerida prioriteeti, millele väljanimed tuleb määrata.</span><span class="sxs-lookup"><span data-stu-id="57469-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="57469-109">See teema selgitab, kuidas neid mobiilirakenduse Warehouse Management väljade nimesid ja prioriteete määratleda ning konfigureerida ja kuidas neid kasutada.</span><span class="sxs-lookup"><span data-stu-id="57469-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="57469-110">Laorakenduse väljade nimede konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="57469-110">Configure warehouse app field names</span></span>

<span data-ttu-id="57469-111">Kui kasutate moodulit Ladustamine mobiilses seadmes, saate seadmes metaandmete kuvamise viisi konfigureerida lehel **Laorakenduse väljade nimed**.</span><span class="sxs-lookup"><span data-stu-id="57469-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="57469-112">Valige uues ettevõttes käsk **Loo vaikeseadistus**, et luua kõik väljanimed, mida kasutatakse lao mobiilse seadme töövoogudes, ning seejärel määrake neile eelistatud sisestusrežiim ja sisestustüüp.</span><span class="sxs-lookup"><span data-stu-id="57469-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="57469-113">Kui kõik väljanimed on loodud, saate valida järgmisi sisestusvalikuid.</span><span class="sxs-lookup"><span data-stu-id="57469-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57469-114">Suvand</span><span class="sxs-lookup"><span data-stu-id="57469-114">Option</span></span></th>
<th><span data-ttu-id="57469-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="57469-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57469-116">Eelistatud sisestusrežiim</span><span class="sxs-lookup"><span data-stu-id="57469-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="57469-117">See valik määratleb, kas valitud väljanime puhul kuvatakse skannimisväli või käsitsi sisestamise väli.</span><span class="sxs-lookup"><span data-stu-id="57469-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="57469-118">See aitab välju eristada olenevalt sellest, kas välja puhul kasutatakse vöötkoode.</span><span class="sxs-lookup"><span data-stu-id="57469-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="57469-119"><strong>Märkus.</strong> Väljanimede puhul, mille eelistatud sisestusrežiim on <strong>Skannimine</strong>, saate sisestada teavet käsitsi, kui vöötkood on loetamatu või kahjustunud.</span><span class="sxs-lookup"><span data-stu-id="57469-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57469-120">Sisestuse tüüp</span><span class="sxs-lookup"><span data-stu-id="57469-120">Input type</span></span></td>
<td><span data-ttu-id="57469-121">See valik määratleb, millist sisestustüüpi tuleb valitud väljanime puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="57469-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="57469-122">Saadaval on neli valikut.</span><span class="sxs-lookup"><span data-stu-id="57469-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="57469-123"><strong>Valik</strong> - sisaldab valikute loendit.</span><span class="sxs-lookup"><span data-stu-id="57469-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="57469-124">Selle valikuga väljanimesid ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="57469-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="57469-125"><strong>Kuupäev</strong> - kuupäevana määratud väljanimed kuvavad kuupäevavormingut koos sildiga.</span><span class="sxs-lookup"><span data-stu-id="57469-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="57469-126">Tänu sellele näevad laotöötajad, millises vormingus tuleb kuupäev sisestada.</span><span class="sxs-lookup"><span data-stu-id="57469-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="57469-127">Selle valikuga väljanimesid ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="57469-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="57469-128"><strong>Tähed</strong> - selle valiku korral kasutatakse rakenduses teabe käsitsi sisestamisel seadme klaviatuuri.</span><span class="sxs-lookup"><span data-stu-id="57469-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="57469-129">Klaviatuurikasutust saab muuta olenevalt kasutatavast seadmest.</span><span class="sxs-lookup"><span data-stu-id="57469-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="57469-130"><strong>Numbrid</strong> - selle valiku korral saate ainult numbreid kasutavate väljanimede puhul kuvada seadme klaviatuuri kasutamise asemel kohandatud numbriklahvistiku koos sisestusväljaga.</span><span class="sxs-lookup"><span data-stu-id="57469-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="57469-131">Laorakenduse väljade prioriteedi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="57469-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="57469-132">Lehel **Laorakenduse väljade prioriteet** saate panna väljanimed erinevatesse prioriteedigruppidesse.</span><span class="sxs-lookup"><span data-stu-id="57469-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="57469-133">See võimaldab otsustada, milline teave tuleb kuvada ülesande põhilehel, kui laotöötajad täidavad ülesandeid rakendust kasutades.</span><span class="sxs-lookup"><span data-stu-id="57469-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="57469-134">Kui klõpsate valikut **Loo vaikeseadistus**, luuakse prioriteedigruppide vaikekomplekt.</span><span class="sxs-lookup"><span data-stu-id="57469-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="57469-135">Prioriteedigruppe saab luua nii palju kui vaja, kuid ülesandelehel kuvatakse ainult kolm.</span><span class="sxs-lookup"><span data-stu-id="57469-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="57469-136">Kui süsteem saadab metaandmed rakendusse, määrab see igale väljale suhtelise prioriteedi olenevalt selle prioriteedigrupist ja rakendus kuvab ülesandelehel kolm esimest metaandmetes sisalduvat prioriteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="57469-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="57469-137">Ülejäänud metaandmed kuvatakse teisel, üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="57469-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="57469-138">Järgmises tabelis on toodud näide viiest prioriteedigrupist.</span><span class="sxs-lookup"><span data-stu-id="57469-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57469-139">Prioriteedigrupp</span><span class="sxs-lookup"><span data-stu-id="57469-139">Priority group</span></span></th>
<th><span data-ttu-id="57469-140">Määratud väljad</span><span class="sxs-lookup"><span data-stu-id="57469-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="57469-141">Prioriteet 10</span><span class="sxs-lookup"><span data-stu-id="57469-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="57469-142">Kaup</span><span class="sxs-lookup"><span data-stu-id="57469-142">Item</span></span></li>
<li><span data-ttu-id="57469-143">Kogus</span><span class="sxs-lookup"><span data-stu-id="57469-143">Quantity</span></span></li>
<li><span data-ttu-id="57469-144">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="57469-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="57469-145">Prioriteet 20</span><span class="sxs-lookup"><span data-stu-id="57469-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="57469-146">Kogumi positsioon</span><span class="sxs-lookup"><span data-stu-id="57469-146">Cluster position</span></span></li>
<li><span data-ttu-id="57469-147">Kogum</span><span class="sxs-lookup"><span data-stu-id="57469-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="57469-148">Prioriteet 30</span><span class="sxs-lookup"><span data-stu-id="57469-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="57469-149">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="57469-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="57469-150">Prioriteet 40</span><span class="sxs-lookup"><span data-stu-id="57469-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="57469-151">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="57469-151">Configuration</span></span></li>
<li><span data-ttu-id="57469-152">Värv</span><span class="sxs-lookup"><span data-stu-id="57469-152">Color</span></span></li>
<li><span data-ttu-id="57469-153">Suurus</span><span class="sxs-lookup"><span data-stu-id="57469-153">Size</span></span></li>
<li><span data-ttu-id="57469-154">Laad</span><span class="sxs-lookup"><span data-stu-id="57469-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="57469-155">Prioriteet 50</span><span class="sxs-lookup"><span data-stu-id="57469-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="57469-156">Koht</span><span class="sxs-lookup"><span data-stu-id="57469-156">Location</span></span></li>
<li><span data-ttu-id="57469-157">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="57469-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57469-158">Näiteks kui laotöötaja täidab ülesannet mobiilses seadmes, sisaldavad rakenduses kuvatavad metaandmed järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="57469-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="57469-159">Kaup</span><span class="sxs-lookup"><span data-stu-id="57469-159">Item</span></span>
-   <span data-ttu-id="57469-160">Kogus</span><span class="sxs-lookup"><span data-stu-id="57469-160">Quantity</span></span>
-   <span data-ttu-id="57469-161">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="57469-161">Unit of measure</span></span>
-   <span data-ttu-id="57469-162">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="57469-162">Item description</span></span>
-   <span data-ttu-id="57469-163">Suurus ja asukoht</span><span class="sxs-lookup"><span data-stu-id="57469-163">Size and Location</span></span>

<span data-ttu-id="57469-164">Ülaltoodud tabelis seadistatud laorakenduse väljade prioriteedi põhjal kuvatakse ülesandelehel järgmised kolm teaberida.</span><span class="sxs-lookup"><span data-stu-id="57469-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="57469-165">1. rida: kaup, kogus, mõõtühik</span><span class="sxs-lookup"><span data-stu-id="57469-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="57469-166">2. rida: kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="57469-166">Row 2: Item description</span></span>
-   <span data-ttu-id="57469-167">3. rida: suurus</span><span class="sxs-lookup"><span data-stu-id="57469-167">Row 3: Size</span></span>

<span data-ttu-id="57469-168">Ülejäänud metaandmeid, näiteks asukohta, ülesandelehel ei kuvata, kuid need kuvatakse üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="57469-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="57469-169">Lisateabe saamiseks ja kasutajaliidese näidete vaatamiseks lugege ajaveebipostitust [Announcing Finance and Operations – Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="57469-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="57469-170">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="57469-170">Additional resources</span></span>
--------

[<span data-ttu-id="57469-171">Laohalduse mobiilirakenduse installimine ja ühendamine</span><span class="sxs-lookup"><span data-stu-id="57469-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]