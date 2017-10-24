---
title: "Rakenduse väljanimede konfigureerimine rakenduses Ladustamine"
description: "See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamisrakenduse väljade nimesid ning prioriteete Finance and Operationsis."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdfc651ea76ea0d35dd3fec43b44cdad177ed96d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="0f6fa-103">Rakenduse väljanimede konfigureerimine rakenduses Ladustamine</span><span class="sxs-lookup"><span data-stu-id="0f6fa-103">Configure app field names in Warehousing app</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0f6fa-104">See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamisrakenduse väljade nimesid ning prioriteete Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="0f6fa-105">**Märkus.** See teema kehtib mooduli Laohaldus funktsioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="0f6fa-106">See ei kehti funktsioonidele moodulis Varude haldus.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="0f6fa-107">Finance and Operations – ladustamine on rakendus, mille abil saate täita laos vajalikke ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="0f6fa-108">Saate määratleda ja konfigureerida rakenduses kasutatavaid väljanimetusi, samuti konfigureerida prioriteeti, millele väljanimed tuleb määrata.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="0f6fa-109">See teema selgitab, kuidas neid ladustamisrakenduse väljade nimesid ja prioriteete määratleda ning konfigureerida ja kuidas neid Finance and Operationsi moodulis Ladustamine kasutada.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="0f6fa-110">Üksikasjalikku teavet Finance and Operationsi mooduli Ladustamine ühenduse konfigureerimise kohta vaadake õppetükist [Finance and Operationsi mooduli Ladustamine installimine ja konfigureerimine](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="0f6fa-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

<a name="configure-warehouse-app-field-names"></a><span data-ttu-id="0f6fa-111">Laorakenduse väljade nimede konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0f6fa-111">Configure warehouse app field names</span></span>
===================================

<span data-ttu-id="0f6fa-112">Kui kasutate Finance and Operationsi moodulit Ladustamine mobiilses seadmes, saate seadmes metaandmete kuvamise viisi konfigureerida lehel **Laorakenduse väljade nimed**.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="0f6fa-113">Valige Finance and Operationsi uues ettevõttes käsk **Loo vaikeseadistus**, et luua kõik väljanimed, mida kasutatakse lao mobiilse seadme töövoogudes, ning seejärel määrake neile eelistatud sisestusrežiim ja sisestustüüp.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="0f6fa-114">Kui kõik väljanimed on loodud, saate valida järgmisi sisestusvalikuid.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f6fa-115">Suvand</span><span class="sxs-lookup"><span data-stu-id="0f6fa-115">Option</span></span></th>
<th><span data-ttu-id="0f6fa-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f6fa-117">Eelistatud sisestusrežiim</span><span class="sxs-lookup"><span data-stu-id="0f6fa-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="0f6fa-118">See valik määratleb, kas valitud väljanime puhul kuvatakse skannimisväli või käsitsi sisestamise väli.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="0f6fa-119">See aitab välju eristada olenevalt sellest, kas välja puhul kasutatakse vöötkoode.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="0f6fa-120"><strong>Märkus.</strong> Väljanimede puhul, mille eelistatud sisestusrežiim on <strong>Skannimine</strong>, saate sisestada teavet käsitsi, kui vöötkood on loetamatu või kahjustunud.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f6fa-121">Sisestuse tüüp</span><span class="sxs-lookup"><span data-stu-id="0f6fa-121">Input type</span></span></td>
<td><span data-ttu-id="0f6fa-122">See valik määratleb, millist sisestustüüpi tuleb valitud väljanime puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="0f6fa-123">Saadaval on neli valikut.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="0f6fa-124"><strong>Valik</strong> - sisaldab valikute loendit.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="0f6fa-125">Selle valikuga väljanimesid ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="0f6fa-126"><strong>Kuupäev</strong> - kuupäevana määratud väljanimed kuvavad kuupäevavormingut koos sildiga.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="0f6fa-127">Tänu sellele näevad laotöötajad, millises vormingus tuleb kuupäev sisestada.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="0f6fa-128">Selle valikuga väljanimesid ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="0f6fa-129"><strong>Tähed</strong> - selle valiku korral kasutatakse rakenduses teabe käsitsi sisestamisel seadme klaviatuuri.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="0f6fa-130">Klaviatuurikasutust saab muuta olenevalt kasutatavast seadmest.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="0f6fa-131"><strong>Numbrid</strong> - selle valiku korral saate ainult numbreid kasutavate väljanimede puhul kuvada seadme klaviatuuri kasutamise asemel kohandatud numbriklahvistiku koos sisestusväljaga.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="0f6fa-132">Laorakenduse väljade prioriteedi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0f6fa-132">Configure warehouse app field priority</span></span>
======================================

<span data-ttu-id="0f6fa-133">Lehel **Laorakenduse väljade prioriteet** saate panna väljanimed erinevatesse prioriteedigruppidesse.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="0f6fa-134">See võimaldab otsustada, milline teave tuleb kuvada ülesande põhilehel, kui laotöötajad täidavad ülesandeid rakendust kasutades.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="0f6fa-135">Kui klõpsate valikut **Loo vaikeseadistus**, luuakse prioriteedigruppide vaikekomplekt.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="0f6fa-136">Prioriteedigruppe saab luua nii palju kui vaja, kuid ülesandelehel kuvatakse ainult kolm.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="0f6fa-137">Kui Finance and Operations saadab metaandmed rakendusse, määrab see igale väljale suhtelise prioriteedi olenevalt selle prioriteedigrupist ja rakendus kuvab ülesandelehel kolm esimest metaandmetes sisalduvat prioriteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="0f6fa-138">Ülejäänud metaandmed kuvatakse teisel, üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="0f6fa-139">Järgmises tabelis on toodud näide viiest prioriteedigrupist.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f6fa-140">Prioriteedigrupp</span><span class="sxs-lookup"><span data-stu-id="0f6fa-140">Priority group</span></span></th>
<th><span data-ttu-id="0f6fa-141">Määratud väljad</span><span class="sxs-lookup"><span data-stu-id="0f6fa-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="0f6fa-142">Prioriteet 10</span><span class="sxs-lookup"><span data-stu-id="0f6fa-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="0f6fa-143">Kaup</span><span class="sxs-lookup"><span data-stu-id="0f6fa-143">Item</span></span></li>
<li><span data-ttu-id="0f6fa-144">Kogus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-144">Quantity</span></span></li>
<li><span data-ttu-id="0f6fa-145">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="0f6fa-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="0f6fa-146">Prioriteet 20</span><span class="sxs-lookup"><span data-stu-id="0f6fa-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="0f6fa-147">Kogumi positsioon</span><span class="sxs-lookup"><span data-stu-id="0f6fa-147">Cluster position</span></span></li>
<li><span data-ttu-id="0f6fa-148">Kogum</span><span class="sxs-lookup"><span data-stu-id="0f6fa-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="0f6fa-149">Prioriteet 30</span><span class="sxs-lookup"><span data-stu-id="0f6fa-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="0f6fa-150">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="0f6fa-151">Prioriteet 40</span><span class="sxs-lookup"><span data-stu-id="0f6fa-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="0f6fa-152">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="0f6fa-152">Configuration</span></span></li>
<li><span data-ttu-id="0f6fa-153">Värv</span><span class="sxs-lookup"><span data-stu-id="0f6fa-153">Color</span></span></li>
<li><span data-ttu-id="0f6fa-154">Suurus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-154">Size</span></span></li>
<li><span data-ttu-id="0f6fa-155">Laad</span><span class="sxs-lookup"><span data-stu-id="0f6fa-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="0f6fa-156">Prioriteet 50</span><span class="sxs-lookup"><span data-stu-id="0f6fa-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="0f6fa-157">Koht</span><span class="sxs-lookup"><span data-stu-id="0f6fa-157">Location</span></span></li>
<li><span data-ttu-id="0f6fa-158">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="0f6fa-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f6fa-159">Näiteks kui laotöötaja täidab ülesannet mobiilses seadmes, sisaldavad rakenduses kuvatavad metaandmed järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="0f6fa-160">Kaup</span><span class="sxs-lookup"><span data-stu-id="0f6fa-160">Item</span></span>
-   <span data-ttu-id="0f6fa-161">Kogus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-161">Quantity</span></span>
-   <span data-ttu-id="0f6fa-162">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="0f6fa-162">Unit of measure</span></span>
-   <span data-ttu-id="0f6fa-163">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-163">Item description</span></span>
-   <span data-ttu-id="0f6fa-164">Suurus ja asukoht</span><span class="sxs-lookup"><span data-stu-id="0f6fa-164">Size and Location</span></span>

<span data-ttu-id="0f6fa-165">Ülaltoodud tabelis seadistatud laorakenduse väljade prioriteedi põhjal kuvatakse ülesandelehel järgmised kolm teaberida.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="0f6fa-166">1. rida: kaup, kogus, mõõtühik</span><span class="sxs-lookup"><span data-stu-id="0f6fa-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="0f6fa-167">2. rida: kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-167">Row 2: Item description</span></span>
-   <span data-ttu-id="0f6fa-168">3. rida: suurus</span><span class="sxs-lookup"><span data-stu-id="0f6fa-168">Row 3: Size</span></span>

<span data-ttu-id="0f6fa-169">Ülejäänud metaandmeid, näiteks asukohta, ülesandelehel ei kuvata, kuid need kuvatakse üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="0f6fa-170">Lisateabe saamiseks ja kasutajaliidese näidete vaatamiseks lugege ajaveebipostitust [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="0f6fa-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="see-also"></a><span data-ttu-id="0f6fa-171">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0f6fa-171">See also</span></span>
--------

[<span data-ttu-id="0f6fa-172">Microsoft Dynamics 365 for Finance and Operationsi mooduli Ladustamine installimine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0f6fa-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




