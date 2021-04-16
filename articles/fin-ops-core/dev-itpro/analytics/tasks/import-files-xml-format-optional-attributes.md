---
title: (RCS) Failide importimine XML-vormingus koos valikuliste atribuutidega
description: Selles teemas kirjeldatakse, kuidas saab kasutaja kujundada elektroonilise aruandluse vormingu konfiguratsiooni failide importimiseks XML-vormingus koos valikuliste atribuutidega.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25ced72bc1bb1b18996c8bab986270fde0557ed3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744863"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="fa2af-103">(RCS) Failide importimine XML-vormingus koos valikuliste atribuutidega</span><span class="sxs-lookup"><span data-stu-id="fa2af-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa2af-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kujundada elektroonilise aruandluse (ER) vormingu konfiguratsiooni failide importimiseks XML-vormingus koos valikuliste atribuutidega.</span><span class="sxs-lookup"><span data-stu-id="fa2af-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="fa2af-105">Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.</span><span class="sxs-lookup"><span data-stu-id="fa2af-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="fa2af-106">Enne alustamist laadige alla ja salvestage lokaalselt fail IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="fa2af-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="fa2af-107">Avage **Kõik tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="fa2af-108">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="fa2af-109">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="fa2af-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="fa2af-110">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="fa2af-111">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="fa2af-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="fa2af-112">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="fa2af-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="fa2af-113">Sisestage väljale **Nimi** „Mudel XML-faili importimiseks”.</span><span class="sxs-lookup"><span data-stu-id="fa2af-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="fa2af-114">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="fa2af-115">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="fa2af-116">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="fa2af-117">Sisestage väljale **Nimi** "Juur".</span><span class="sxs-lookup"><span data-stu-id="fa2af-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="fa2af-118">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-118">Click **Add**.</span></span>
8.    <span data-ttu-id="fa2af-119">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="fa2af-120">Sisestage väljale **Nimi** "Loend".</span><span class="sxs-lookup"><span data-stu-id="fa2af-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="fa2af-121">Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="fa2af-122">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-122">Click **Add**.</span></span>
12.    <span data-ttu-id="fa2af-123">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="fa2af-124">Sisestage väljale **Nimi** "Kood".</span><span class="sxs-lookup"><span data-stu-id="fa2af-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="fa2af-125">Valige väljalt **Üksuse tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="fa2af-126">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-126">Click **Add**.</span></span>
16.    <span data-ttu-id="fa2af-127">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-127">Click **Save**.</span></span>
17.    <span data-ttu-id="fa2af-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa2af-128">Close the page.</span></span>
18.    <span data-ttu-id="fa2af-129">Klõpsake valikut **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="fa2af-130">Klõpsake valikut **Vii lõpule**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="fa2af-131">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="fa2af-132">Vormingu loomine andmete impordiks</span><span class="sxs-lookup"><span data-stu-id="fa2af-132">Create a format for data import</span></span>
1.    <span data-ttu-id="fa2af-133">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="fa2af-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="fa2af-134">Sisestage väljale **Uus** valik "Vorming põhineb andmemudelil Mudel XML-faili importimiseks".</span><span class="sxs-lookup"><span data-stu-id="fa2af-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="fa2af-135">Sisestage välja **Nimi** „Vorming XML-faili importimiseks”.</span><span class="sxs-lookup"><span data-stu-id="fa2af-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="fa2af-136">Valige väljal **Toetab andmeimporti** valik **Jah**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="fa2af-137">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="fa2af-138">Vormingu kujundamine XML-vormingus sissetuleva faili sõelumiseks</span><span class="sxs-lookup"><span data-stu-id="fa2af-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="fa2af-139">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="fa2af-140">Klõpsake suvandit **Lisa juur** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="fa2af-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="fa2af-141">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="fa2af-142">Sisestage väljale **Nimi** "Juur".</span><span class="sxs-lookup"><span data-stu-id="fa2af-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="fa2af-143">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-143">Click **OK**.</span></span>
6.    <span data-ttu-id="fa2af-144">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="fa2af-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="fa2af-145">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="fa2af-146">Sisestage väljale **Nimi** "Dokument".</span><span class="sxs-lookup"><span data-stu-id="fa2af-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="fa2af-147">Valige väljal **Mitmekordsus** suvand **One many**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="fa2af-148">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-148">Click **OK**.</span></span>
11.    <span data-ttu-id="fa2af-149">Tehke puul valik **root\document**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="fa2af-150">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="fa2af-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="fa2af-151">Valige puul suvand **XML\Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="fa2af-152">Sisestage väljale **Nimi** tüübi ID.</span><span class="sxs-lookup"><span data-stu-id="fa2af-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="fa2af-153">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-153">Click **OK**.</span></span>
16.    <span data-ttu-id="fa2af-154">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="fa2af-155">Vormingu vastenduse kujundamine sõelutud teabe andmemudelile salvestamiseks</span><span class="sxs-lookup"><span data-stu-id="fa2af-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="fa2af-156">Klõpsake valikut **Vormingu vastendamine mudeliga**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="fa2af-157">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-157">Click **New**.</span></span>
3. <span data-ttu-id="fa2af-158">Sisestage või valige väärtus väljal **Määratlused**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="fa2af-159">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="fa2af-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="fa2af-160">Sisestage väljale **Nimi** "Vastendamine".</span><span class="sxs-lookup"><span data-stu-id="fa2af-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="fa2af-161">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-161">Click **Save**.</span></span>
7. <span data-ttu-id="fa2af-162">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-162">Click **Designer**.</span></span>
8. <span data-ttu-id="fa2af-163">Laiendage puul valikut **format**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="fa2af-164">Laiendage puul valikut **formatoot: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="fa2af-165">Valige puul \**formatoot: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="fa2af-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="fa2af-166">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="fa2af-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="fa2af-167">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="fa2af-168">Laiendage puul valikut \**formatoot: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="fa2af-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="fa2af-169">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="fa2af-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="fa2af-170">Valige puul \**formatoot: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="fa2af-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="fa2af-171">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="fa2af-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="fa2af-172">Laiendage puul valikut **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="fa2af-173">Valige puul **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="fa2af-174">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="fa2af-175">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-175">Click **Save**.</span></span>
18.    <span data-ttu-id="fa2af-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa2af-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="fa2af-177">Vormingu vastendamine käivitamine</span><span class="sxs-lookup"><span data-stu-id="fa2af-177">Run format mapping</span></span>
1. <span data-ttu-id="fa2af-178">Klõpsake nuppu **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-178">Click **Run**.</span></span>
2. <span data-ttu-id="fa2af-179">Klõpsake nuppu **Sirvi** ja valige suvand **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="fa2af-180">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="fa2af-181">Valitud faili ei ole imporditud, kuna vormingu kujundus eeldab atribuudi „ID” olemasolu „dokumendi” elemendi jaoks, kuid imporditud fail ei sisalda sellist atribuuti.</span><span class="sxs-lookup"><span data-stu-id="fa2af-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="fa2af-182">Vormingu struktuuri muutmine, et käsitseda XML-atribuuti valikulisena</span><span class="sxs-lookup"><span data-stu-id="fa2af-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="fa2af-183">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa2af-183">Close the page.</span></span>
2. <span data-ttu-id="fa2af-184">Laiendage puul valikut **root\document**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="fa2af-185">Tehke puul valik **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="fa2af-186">Valige suvand **Jah** väljas **Tühjenda puuduva atribuudi string**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="fa2af-187">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="fa2af-188">Muudatuste katsetamiseks vormingu vastenduse käivitamine</span><span class="sxs-lookup"><span data-stu-id="fa2af-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="fa2af-189">Klõpsake valikut **Vormingu vastendamine mudeliga**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="fa2af-190">Klõpsake nuppu **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-190">Click **Run**.</span></span>
3. <span data-ttu-id="fa2af-191">Klõpsake nuppu **Sirvi** ja valige fail **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="fa2af-192">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa2af-192">Click **OK**.</span></span>
5. <span data-ttu-id="fa2af-193">Vaadake genereeritud fail üle.</span><span class="sxs-lookup"><span data-stu-id="fa2af-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="fa2af-194">Sama fail on imporditud, kuna vormingu kujundus võtab nüüd dokumendi elemendi ID atribuuti arvesse valikulisena.</span><span class="sxs-lookup"><span data-stu-id="fa2af-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]