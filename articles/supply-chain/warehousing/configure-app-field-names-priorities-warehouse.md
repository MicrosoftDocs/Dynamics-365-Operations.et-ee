---
title: Rakenduse väljanimede konfigureerimine rakenduses Ladustamine
description: See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamisrakenduse väljade nimesid ning prioriteete Dynamics 365 Supply Chain Managementis.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9b02b93895757580b323a4cd891909d5551ea55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205755"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="f19b7-103">Rakenduse väljanimede konfigureerimine rakenduses Ladustamine</span><span class="sxs-lookup"><span data-stu-id="f19b7-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f19b7-104">See teema kirjeldab, kuidas määratleda ja konfigureerida ladustamisrakenduse väljade nimesid ning prioriteete Dynamics 365 Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="f19b7-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="f19b7-105">See teema kehtib laohalduse funktsioonidele.</span><span class="sxs-lookup"><span data-stu-id="f19b7-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="f19b7-106">See ei kehti funktsioonidele moodulis Varude haldus.</span><span class="sxs-lookup"><span data-stu-id="f19b7-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="f19b7-107">Ladustamine on rakendus, mille abil saate täita laos vajalikke ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="f19b7-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="f19b7-108">Saate määratleda ja konfigureerida rakenduses kasutatavaid väljanimetusi, samuti konfigureerida prioriteeti, millele väljanimed tuleb määrata.</span><span class="sxs-lookup"><span data-stu-id="f19b7-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="f19b7-109">See teema selgitab, kuidas neid ladustamisrakenduse väljade nimesid ja prioriteete määratleda ning konfigureerida ja kuidas neid moodulis Ladustamine kasutada.</span><span class="sxs-lookup"><span data-stu-id="f19b7-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="f19b7-110">Üksikasjalikku teavet selle kohta, kuidas konfigureerida lao ühendamist, leiate juhendist [Laorakenduse installimise ja konfigureerimise ülevaade](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="f19b7-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the Warehousing app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="f19b7-111">Laorakenduse väljade nimede konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f19b7-111">Configure warehouse app field names</span></span>

<span data-ttu-id="f19b7-112">Kui kasutate moodulit Ladustamine mobiilses seadmes, saate seadmes metaandmete kuvamise viisi konfigureerida lehel **Laorakenduse väljade nimed**.</span><span class="sxs-lookup"><span data-stu-id="f19b7-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="f19b7-113">Valige uues ettevõttes käsk **Loo vaikeseadistus**, et luua kõik väljanimed, mida kasutatakse lao mobiilse seadme töövoogudes, ning seejärel määrake neile eelistatud sisestusrežiim ja sisestustüüp.</span><span class="sxs-lookup"><span data-stu-id="f19b7-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="f19b7-114">Kui kõik väljanimed on loodud, saate valida järgmisi sisestusvalikuid.</span><span class="sxs-lookup"><span data-stu-id="f19b7-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f19b7-115">Suvand</span><span class="sxs-lookup"><span data-stu-id="f19b7-115">Option</span></span></th>
<th><span data-ttu-id="f19b7-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f19b7-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f19b7-117">Eelistatud sisestusrežiim</span><span class="sxs-lookup"><span data-stu-id="f19b7-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="f19b7-118">See valik määratleb, kas valitud väljanime puhul kuvatakse skannimisväli või käsitsi sisestamise väli.</span><span class="sxs-lookup"><span data-stu-id="f19b7-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="f19b7-119">See aitab välju eristada olenevalt sellest, kas välja puhul kasutatakse vöötkoode.</span><span class="sxs-lookup"><span data-stu-id="f19b7-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="f19b7-120"><strong>Märkus.</strong> Väljanimede puhul, mille eelistatud sisestusrežiim on <strong>Skannimine</strong>, saate sisestada teavet käsitsi, kui vöötkood on loetamatu või kahjustunud.</span><span class="sxs-lookup"><span data-stu-id="f19b7-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f19b7-121">Sisestuse tüüp</span><span class="sxs-lookup"><span data-stu-id="f19b7-121">Input type</span></span></td>
<td><span data-ttu-id="f19b7-122">See valik määratleb, millist sisestustüüpi tuleb valitud väljanime puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="f19b7-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="f19b7-123">Saadaval on neli valikut.</span><span class="sxs-lookup"><span data-stu-id="f19b7-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="f19b7-124"><strong>Valik</strong> - sisaldab valikute loendit.</span><span class="sxs-lookup"><span data-stu-id="f19b7-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="f19b7-125">Selle valikuga väljanimesid ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="f19b7-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="f19b7-126"><strong>Kuupäev</strong> - kuupäevana määratud väljanimed kuvavad kuupäevavormingut koos sildiga.</span><span class="sxs-lookup"><span data-stu-id="f19b7-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="f19b7-127">Tänu sellele näevad laotöötajad, millises vormingus tuleb kuupäev sisestada.</span><span class="sxs-lookup"><span data-stu-id="f19b7-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="f19b7-128">Selle valikuga väljanimesid ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="f19b7-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="f19b7-129"><strong>Tähed</strong> - selle valiku korral kasutatakse rakenduses teabe käsitsi sisestamisel seadme klaviatuuri.</span><span class="sxs-lookup"><span data-stu-id="f19b7-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="f19b7-130">Klaviatuurikasutust saab muuta olenevalt kasutatavast seadmest.</span><span class="sxs-lookup"><span data-stu-id="f19b7-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="f19b7-131"><strong>Numbrid</strong> - selle valiku korral saate ainult numbreid kasutavate väljanimede puhul kuvada seadme klaviatuuri kasutamise asemel kohandatud numbriklahvistiku koos sisestusväljaga.</span><span class="sxs-lookup"><span data-stu-id="f19b7-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="f19b7-132">Laorakenduse väljade prioriteedi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f19b7-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="f19b7-133">Lehel **Laorakenduse väljade prioriteet** saate panna väljanimed erinevatesse prioriteedigruppidesse.</span><span class="sxs-lookup"><span data-stu-id="f19b7-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="f19b7-134">See võimaldab otsustada, milline teave tuleb kuvada ülesande põhilehel, kui laotöötajad täidavad ülesandeid rakendust kasutades.</span><span class="sxs-lookup"><span data-stu-id="f19b7-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="f19b7-135">Kui klõpsate valikut **Loo vaikeseadistus**, luuakse prioriteedigruppide vaikekomplekt.</span><span class="sxs-lookup"><span data-stu-id="f19b7-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="f19b7-136">Prioriteedigruppe saab luua nii palju kui vaja, kuid ülesandelehel kuvatakse ainult kolm.</span><span class="sxs-lookup"><span data-stu-id="f19b7-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="f19b7-137">Kui süsteem saadab metaandmed rakendusse, määrab see igale väljale suhtelise prioriteedi olenevalt selle prioriteedigrupist ja rakendus kuvab ülesandelehel kolm esimest metaandmetes sisalduvat prioriteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="f19b7-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="f19b7-138">Ülejäänud metaandmed kuvatakse teisel, üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="f19b7-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="f19b7-139">Järgmises tabelis on toodud näide viiest prioriteedigrupist.</span><span class="sxs-lookup"><span data-stu-id="f19b7-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f19b7-140">Prioriteedigrupp</span><span class="sxs-lookup"><span data-stu-id="f19b7-140">Priority group</span></span></th>
<th><span data-ttu-id="f19b7-141">Määratud väljad</span><span class="sxs-lookup"><span data-stu-id="f19b7-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="f19b7-142">Prioriteet 10</span><span class="sxs-lookup"><span data-stu-id="f19b7-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="f19b7-143">Kaup</span><span class="sxs-lookup"><span data-stu-id="f19b7-143">Item</span></span></li>
<li><span data-ttu-id="f19b7-144">Kogus</span><span class="sxs-lookup"><span data-stu-id="f19b7-144">Quantity</span></span></li>
<li><span data-ttu-id="f19b7-145">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="f19b7-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="f19b7-146">Prioriteet 20</span><span class="sxs-lookup"><span data-stu-id="f19b7-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="f19b7-147">Kogumi positsioon</span><span class="sxs-lookup"><span data-stu-id="f19b7-147">Cluster position</span></span></li>
<li><span data-ttu-id="f19b7-148">Kogum</span><span class="sxs-lookup"><span data-stu-id="f19b7-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="f19b7-149">Prioriteet 30</span><span class="sxs-lookup"><span data-stu-id="f19b7-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="f19b7-150">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f19b7-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="f19b7-151">Prioriteet 40</span><span class="sxs-lookup"><span data-stu-id="f19b7-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="f19b7-152">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="f19b7-152">Configuration</span></span></li>
<li><span data-ttu-id="f19b7-153">Värv</span><span class="sxs-lookup"><span data-stu-id="f19b7-153">Color</span></span></li>
<li><span data-ttu-id="f19b7-154">Suurus</span><span class="sxs-lookup"><span data-stu-id="f19b7-154">Size</span></span></li>
<li><span data-ttu-id="f19b7-155">Laad</span><span class="sxs-lookup"><span data-stu-id="f19b7-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="f19b7-156">Prioriteet 50</span><span class="sxs-lookup"><span data-stu-id="f19b7-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="f19b7-157">Koht</span><span class="sxs-lookup"><span data-stu-id="f19b7-157">Location</span></span></li>
<li><span data-ttu-id="f19b7-158">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="f19b7-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f19b7-159">Näiteks kui laotöötaja täidab ülesannet mobiilses seadmes, sisaldavad rakenduses kuvatavad metaandmed järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="f19b7-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="f19b7-160">Kaup</span><span class="sxs-lookup"><span data-stu-id="f19b7-160">Item</span></span>
-   <span data-ttu-id="f19b7-161">Kogus</span><span class="sxs-lookup"><span data-stu-id="f19b7-161">Quantity</span></span>
-   <span data-ttu-id="f19b7-162">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="f19b7-162">Unit of measure</span></span>
-   <span data-ttu-id="f19b7-163">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f19b7-163">Item description</span></span>
-   <span data-ttu-id="f19b7-164">Suurus ja asukoht</span><span class="sxs-lookup"><span data-stu-id="f19b7-164">Size and Location</span></span>

<span data-ttu-id="f19b7-165">Ülaltoodud tabelis seadistatud laorakenduse väljade prioriteedi põhjal kuvatakse ülesandelehel järgmised kolm teaberida.</span><span class="sxs-lookup"><span data-stu-id="f19b7-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="f19b7-166">1. rida: kaup, kogus, mõõtühik</span><span class="sxs-lookup"><span data-stu-id="f19b7-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="f19b7-167">2. rida: kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f19b7-167">Row 2: Item description</span></span>
-   <span data-ttu-id="f19b7-168">3. rida: suurus</span><span class="sxs-lookup"><span data-stu-id="f19b7-168">Row 3: Size</span></span>

<span data-ttu-id="f19b7-169">Ülejäänud metaandmeid, näiteks asukohta, ülesandelehel ei kuvata, kuid need kuvatakse üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="f19b7-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="f19b7-170">Lisateabe saamiseks ja kasutajaliidese näidete vaatamiseks lugege ajaveebipostitust [Announcing Finance and Operations – Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="f19b7-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="f19b7-171">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f19b7-171">Additional resources</span></span>
--------

[<span data-ttu-id="f19b7-172">Ladustamisrakenduse installimise ja konfigureerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="f19b7-172">Install and configure the Warehousing app overview</span></span>](install-configure-warehousing-app.md)
