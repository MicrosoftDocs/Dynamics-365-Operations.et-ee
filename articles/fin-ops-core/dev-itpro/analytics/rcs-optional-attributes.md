---
title: Failide importimine XML-vormingus koos valikuliste atribuutidega
description: Selles teemas kirjeldatakse ER-vormingute kujundamist, mis määravad XML-atribuute sissetulevate elektrooniliste dokumentide sõelumiseks XML-vormingus.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 399f19197a729c11eaff94d708c837caef0d366d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562948"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="dc0f9-103">Failide importimine XML-vormingus koos valikuliste atribuutidega</span><span class="sxs-lookup"><span data-stu-id="dc0f9-103">Import files in XML format with optional attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc0f9-104">Saate kujundada elektroonilise aruandluse (ER) vormingud sõeluma sissetulevaid dokumente XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="dc0f9-105">XML-elementide teatud atribuute saab loodud ER-vormingus määratleda valikuliselt.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="dc0f9-106">See võimaldab teil selliste XML-atribuutidega ja ilma nendeta sissetulevaid faile õigesti käsistseda.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="dc0f9-107">Seejärel saate neist failidest pärit sisu kasutada rakenduse andmete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="dc0f9-108">Selle funktsiooni kohta lisateabe saamiseks läbige etapid teemas [(RCS) Failide importimine XML-vormingus koos valikuliste atribuutidega](tasks/import-files-xml-format-optional-attributes.md), mis on osa 7.5.4.3 omandada/arendada IT-teenuse/-lahenduse komponentide hankimise/arendamise (10677) äriprotsessist.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="dc0f9-109">Saate selle tegevuse juhise ja seotud näitefailid alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="dc0f9-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="dc0f9-110">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="dc0f9-110">Content description</span></span>       | <span data-ttu-id="dc0f9-111">Fail</span><span class="sxs-lookup"><span data-stu-id="dc0f9-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="dc0f9-112">Näidisfail XML-vormingus</span><span class="sxs-lookup"><span data-stu-id="dc0f9-112">Sample file in XML format</span></span> | <span data-ttu-id="dc0f9-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="dc0f9-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="dc0f9-114">Ülesande juhis</span><span class="sxs-lookup"><span data-stu-id="dc0f9-114">Task guide</span></span>                | <span data-ttu-id="dc0f9-115">RCS failide importimine XML-vormingus koos valikuliste atribuutidega.axtr</span><span class="sxs-lookup"><span data-stu-id="dc0f9-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="dc0f9-116">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kujundada elektroonilise aruandluse (ER) vormingu konfiguratsiooni failide importimiseks XML-vormingus koos valikuliste atribuutidega.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="dc0f9-117">Etappide lõpuleviimiseks, peate esmalt läbima etapid protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="dc0f9-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="dc0f9-118">Enne alustamist laadige alla ja salvestage lokaalselt fail IncomingDocumentToLearnHowToHandleOptionalAttributes.xml Microsofti allalaadimiskeskusest (https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="dc0f9-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="dc0f9-119">Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="dc0f9-120">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="dc0f9-121">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-121">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="dc0f9-122">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="dc0f9-123">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="dc0f9-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="dc0f9-124">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="dc0f9-125">Sisestage väljale **Nimi** „Mudel XML-faili importimiseks”.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="dc0f9-126">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="dc0f9-127">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-127">Click **Designer**.</span></span>
5. <span data-ttu-id="dc0f9-128">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="dc0f9-129">Sisestage väljale **Nimi** "Juur".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="dc0f9-130">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-130">Click **Add**.</span></span>
8. <span data-ttu-id="dc0f9-131">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="dc0f9-132">Sisestage väljale **Nimi** "Loend".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-132">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="dc0f9-133">Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-133">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="dc0f9-134">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-134">Click **Add**.</span></span>
12.    <span data-ttu-id="dc0f9-135">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-135">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="dc0f9-136">Sisestage väljale **Nimi** "Kood".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-136">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="dc0f9-137">Valige väljalt **Üksuse tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-137">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="dc0f9-138">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-138">Click **Add**.</span></span>
16.    <span data-ttu-id="dc0f9-139">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-139">Click **Save**.</span></span>
17.    <span data-ttu-id="dc0f9-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-140">Close the page.</span></span>
18.    <span data-ttu-id="dc0f9-141">Klõpsake valikut **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-141">Click **Change status**.</span></span>
19.    <span data-ttu-id="dc0f9-142">Klõpsake valikut **Vii lõpule**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-142">Click **Complete**.</span></span>
20.    <span data-ttu-id="dc0f9-143">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="dc0f9-144">Vormingu loomine andmete impordiks</span><span class="sxs-lookup"><span data-stu-id="dc0f9-144">Create a format for data import</span></span>
1. <span data-ttu-id="dc0f9-145">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="dc0f9-146">Sisestage väljale **Uus** valik "Vorming põhineb andmemudelil Mudel XML-faili importimiseks".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="dc0f9-147">Sisestage väljale **Nimi** „Vorming XML-faili importimiseks”.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-147">In the **Nam** e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="dc0f9-148">Valige väljal **Toetab andmeimporti** valik **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="dc0f9-149">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="dc0f9-150">Vormingu kujundamine XML-vormingus sissetuleva faili sõelumiseks</span><span class="sxs-lookup"><span data-stu-id="dc0f9-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="dc0f9-151">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-151">Click **Designer**.</span></span>
2. <span data-ttu-id="dc0f9-152">Klõpsake suvandit **Lisa juur** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="dc0f9-153">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="dc0f9-154">Sisestage väljale **Nimi** "Juur".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="dc0f9-155">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-155">Click **OK**.</span></span>
6. <span data-ttu-id="dc0f9-156">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="dc0f9-157">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="dc0f9-158">Sisestage väljale **Nimi** "Dokument".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="dc0f9-159">Valige väljal **Mitmekordsus** suvand **One many**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-159">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="dc0f9-160">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-160">Click **OK**.</span></span>
11.    <span data-ttu-id="dc0f9-161">Tehke puul valik **root\document**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-161">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="dc0f9-162">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-162">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="dc0f9-163">Valige puul suvand **XML\Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-163">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="dc0f9-164">Sisestage väljale **Nimi** "ID".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-164">In the **Name** field, type 'id'.</span></span>
15.    <span data-ttu-id="dc0f9-165">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-165">Click **OK**.</span></span>
16.    <span data-ttu-id="dc0f9-166">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="dc0f9-167">Vormingu vastenduse kujundamine sõelutud teabe andmemudelile salvestamiseks</span><span class="sxs-lookup"><span data-stu-id="dc0f9-167">Design a format mapping to save parsed information to data model</span></span>
1.    <span data-ttu-id="dc0f9-168">Klõpsake valikut **Vormingu vastendamine mudeliga**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-168">Click **Map format to model**.</span></span>
2.    <span data-ttu-id="dc0f9-169">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-169">Click **New**.</span></span>
3.    <span data-ttu-id="dc0f9-170">Sisestage või valige väärtus väljal **Määratlused**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-170">In the **Definition** field, enter or select a value.</span></span>
4.    <span data-ttu-id="dc0f9-171">Sisestage väljale **Nimi** "Vastendamine".</span><span class="sxs-lookup"><span data-stu-id="dc0f9-171">In the **Name** field, type 'Mapping'.</span></span>
5.    <span data-ttu-id="dc0f9-172">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-172">Click **Save**.</span></span>
6.    <span data-ttu-id="dc0f9-173">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-173">Click **Designer**.</span></span>
7.    <span data-ttu-id="dc0f9-174">Laiendage puul valikut **format**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-174">In the tree, expand **format**.</span></span>
8.    <span data-ttu-id="dc0f9-175">Laiendage puul valikut **formatoot: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.    <span data-ttu-id="dc0f9-176">Valige puul \**formatoot: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="dc0f9-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="dc0f9-177">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-177">(document)\*\*.</span></span>
10.    <span data-ttu-id="dc0f9-178">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-178">Click **Bind**.</span></span>
11.    <span data-ttu-id="dc0f9-179">Laiendage puul valikut \**formatoot: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="dc0f9-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="dc0f9-180">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-180">(document)\*\*.</span></span>
12.    <span data-ttu-id="dc0f9-181">Valige puul \**formatoot: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="dc0f9-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="dc0f9-182">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-182">(document)\id\*\*.</span></span>
13.    <span data-ttu-id="dc0f9-183">Laiendage puul valikut **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-183">In the tree, expand **List = format.root.document**.</span></span>
14.    <span data-ttu-id="dc0f9-184">Valige puul **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-184">In the tree, select **List = format.root.document\Code**.</span></span>
15.    <span data-ttu-id="dc0f9-185">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-185">Click **Bind**.</span></span>
16.    <span data-ttu-id="dc0f9-186">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-186">Click **Save**.</span></span>
17.    <span data-ttu-id="dc0f9-187">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="dc0f9-188">Vormingu vastendamise käivitamine</span><span class="sxs-lookup"><span data-stu-id="dc0f9-188">Run format mapping</span></span>
1. <span data-ttu-id="dc0f9-189">Klõpsake nuppu **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-189">Click **Run**.</span></span>
2. <span data-ttu-id="dc0f9-190">Klõpsake nuppu **Sirvi** ja valige fail **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="dc0f9-191">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="dc0f9-192">Valitud faili ei ole imporditud, kuna vormingu kujundus eeldab atribuudi „ID” olemasolu „dokumendi” elemendi jaoks, kuid imporditud fail ei sisalda sellist atribuuti.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-192">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="dc0f9-193">Vormingu struktuuri muutmine, et käsitseda XML-atribuuti valikulisena</span><span class="sxs-lookup"><span data-stu-id="dc0f9-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="dc0f9-194">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-194">Close the page.</span></span>
2. <span data-ttu-id="dc0f9-195">Laiendage puul valikut **root\document**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="dc0f9-196">Tehke puul valik **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="dc0f9-197">Valige väljal **Tühjenda puuduva atribuudi string** suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="dc0f9-198">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="dc0f9-199">Muudatuste katsetamiseks vormingu vastenduse käivitamine</span><span class="sxs-lookup"><span data-stu-id="dc0f9-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="dc0f9-200">Klõpsake valikut **Vormingu vastendamine mudeliga**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="dc0f9-201">Klõpsake nuppu **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-201">Click **Run**.</span></span>
3. <span data-ttu-id="dc0f9-202">Klõpsake nuppu **Sirvi** ja valige fail **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="dc0f9-203">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-203">Click **OK**.</span></span>
5. <span data-ttu-id="dc0f9-204">Vaadake genereeritud fail üle.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-204">Review the generated file.</span></span> <span data-ttu-id="dc0f9-205">Pange tähele, et sama fail on imporditud, kuna vormingu kujundus arvestab nüüd „dokumendi” elemendi „ID” atribuuti valikulisena.</span><span class="sxs-lookup"><span data-stu-id="dc0f9-205">Note that same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]