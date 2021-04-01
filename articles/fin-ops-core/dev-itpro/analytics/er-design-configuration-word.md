---
title: Uue ER-i konfiguratsiooni loomine Wordi vormingus aruannete loomiseks
description: See teema selgitab, kuidas kasutajad saavad konfigureerida uut elektroonilise aruandluse (ER) vormingu looma aruanded Microsoft Word dokumentidena.
author: NickSelin
manager: AnnBe
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 535e46eb033bf2796ab8e4b0d2e29767ad0a8cdf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094150"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a><span data-ttu-id="59730-103">Uue ER-i konfiguratsiooni loomine Wordi vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="59730-103">Design a new ER configuration to generate reports in Word format</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59730-104">Aruannete Microsoft Wordi dokumentidena loomiseks peate kujundama aruannete jaoks malli, kasutades näiteks Wordi töölauarakendust.</span><span class="sxs-lookup"><span data-stu-id="59730-104">To generate reports as Microsoft Word documents, you must design a template for the reports by using, for example, the Word desktop application.</span></span> <span data-ttu-id="59730-105">Järgmisel joonisel on näidatud kontrollaruande näidismall, mille saab luua, et näidata töödeldud hankija maksete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="59730-105">The following illustration shows the sample template for the control report that can be generated to show details of processed vendor payments.</span></span>

![Näidismalli kontrollaruanne Wordi töölauarakenduses](./media/er-design-configuration-word-image1.png)

<span data-ttu-id="59730-107">Wordi vormingus aruannete Wordi dokumendi mallina kasutamiseks saate konfigureerida uue [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [lahenduse](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="59730-107">To use a Word document as a template for reports in Word format, you can configure a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="59730-108">See lahendus peab sisaldama ER-i [konfiguratsiooni](general-electronic-reporting.md#Configuration), mis sisaldab ER-i [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponenti.</span><span class="sxs-lookup"><span data-stu-id="59730-108">This solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span>

> [!NOTE]
> <span data-ttu-id="59730-109">Kui loote Wordi vormingus aruannete loomiseks uue ER-vormingu konfiguratsiooni, peate valima kas suvandi **Word** dialoogiboksi **Konfiguratsiooni loomine** vormingutüübiks või jätma välja **Vormingu tüüp** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="59730-109">When you create a new ER format configuration to generate reports in Word format, you must either select **Word** as the format type in the **Create configuration** drop-down dialog box or leave the **Format type** field blank.</span></span>

![Vormingu konfiguratsiooni loomine lehel Konfiguratsioonid](./media/er-design-configuration-word-image2.gif)

<span data-ttu-id="59730-111">Lahenduse ER-vormingu komponent peab sisaldama vormingu elementi **Excel\\Fail** ja see vorminguelement peab olema lingitud Wordi dokumendiga, mida kasutatakse käitusajal aruannete loomise mallina.</span><span class="sxs-lookup"><span data-stu-id="59730-111">The ER format component of the solution must contain the **Excel\\File** format element, and that format element must be linked to the Word document that will be used as the template for generated reports at runtime.</span></span> <span data-ttu-id="59730-112">ER-vormingu komponendi konfigureerimiseks peate ER-i vormingu kujundajas avama loodud ER-i konfiguratsiooni [mustandi](general-electronic-reporting.md#component-versioning) versiooni.</span><span class="sxs-lookup"><span data-stu-id="59730-112">To configure the ER format component, you must open the [draft](general-electronic-reporting.md#component-versioning) version of the created ER configuration in the ER format designer.</span></span> <span data-ttu-id="59730-113">Seejärel lisage element **Excel\\Fail**, lisage redigeeritavale ER-vormingule oma Wordi mall ja linkige see mall lisatud elemendile **Excel\\Fail**.</span><span class="sxs-lookup"><span data-stu-id="59730-113">Then add the **Excel\\File** element, attach your Word template to the editable ER format, and link that template to the **Excel\\File** element that you added.</span></span>

> [!NOTE]
> <span data-ttu-id="59730-114">Malli manustamisel peate kasutama [dokumendi tüüpi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), mis on varem selleks otstarbeks ER-i parameetrites [konfigureeritud](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="59730-114">When you attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has previously been [configured](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

![Malli lisamine vormingukujundaja lehele](./media/er-design-configuration-word-image3.gif)

<span data-ttu-id="59730-116">Saate lisada pesastatud elemendid **Excel\\Vahemik** ja **Excel\\Lahter** elemendile **Excel\\Fail**, et määrata andmestruktuur, mis sisestatakse käitusajal loodud aruannetesse.</span><span class="sxs-lookup"><span data-stu-id="59730-116">You can add **Excel\\Range** and **Excel\\Cell** nested elements for the **Excel\\File** element to specify the structure of data that will be entered in generated reports at runtime.</span></span> <span data-ttu-id="59730-117">Seejärel peate need elemendid siduma redigeeritavate ER-vormingu andmeallikatega, et määrata tegelikud andmed, mis sisestatakse käitusajal loodud aruannetesse.</span><span class="sxs-lookup"><span data-stu-id="59730-117">You must then bind those elements to data sources of the editable ER format to specify the actual data that will be entered in generated reports at runtime.</span></span>

![Pesastatud elementide lisamine vormingu kujundaja lehel](./media/er-design-configuration-word-image4.gif)

<span data-ttu-id="59730-119">Kui salvestate oma muudatused kujundamise ajal ER-vormingusse, talletatakse hierarhilise vormingu struktuur manustatud Wordi mallis [kohandatud XML-i osana](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), mille nimi on **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="59730-119">When you save your changes to the ER format at design time, the hierarchical format structure is stored in the attached Word template as a [custom XML part](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) that is named **Report**.</span></span> <span data-ttu-id="59730-120">Peate avama muudetud malli, laadima selle rakendusest Finance alla, salvestama selle kohalikult ning avama selle Wordi töölauarakenduses.</span><span class="sxs-lookup"><span data-stu-id="59730-120">You must access the modified template, download it from Finance, store it locally, and open it in the Word desktop application.</span></span> <span data-ttu-id="59730-121">Järgmisel joonisel on näidatud kohalikult salvestatud näidismall kontrollaruande jaoks, mis sisaldab kohandatud XML-i osa **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="59730-121">The following illustration shows the locally stored sample template for the control report that contains the **Report** custom XML part.</span></span>

![Näidisaruande malli eelvaade Wordi töölauarakenduses](./media/er-design-configuration-word-image5.gif)

<span data-ttu-id="59730-123">Kui vorminguelementide **Excel\\Vahemik** ja **Excel\\Lahter** sidumised toimuvad käitusajal, lisatakse iga sidumise edastatud andmed loodud Wordi dokumenti kohandatud XML-i osa **Aruanne** individuaalse väljana.</span><span class="sxs-lookup"><span data-stu-id="59730-123">When bindings of **Excel\\Range** and **Excel\\Cell** format elements are run at runtime, the data that every binding delivers comes into the generated Word document as an individual field of the **Report** custom XML part.</span></span> <span data-ttu-id="59730-124">Loodud dokumendis kohandatud XML-i osa väljadelt väärtuste sisestamiseks peate lisama oma Wordi mallile sobivad [sisukontrollid](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word), mis toimivad käitusajal täidetud andmete kohatäidetena.</span><span class="sxs-lookup"><span data-stu-id="59730-124">To enter the values from the fields of the custom XML part in a generated document, you must add the appropriate Word [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) to your Word template to serve as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="59730-125">Sisukontrollide täitmise määratlemiseks vastendage iga sisukontroll kohandatud XML-i osa **Aruanne** vastava väljaga.</span><span class="sxs-lookup"><span data-stu-id="59730-125">To specify how content controls are filled in, map every content control to the appropriate field of the **Report** custom XML part.</span></span>

![Sisukontrollide lisamine ja vastendamine Wordi töölauarakenduses](./media/er-design-configuration-word-image6.gif)

<span data-ttu-id="59730-127">Seejärel peate asendama redigeeritavas ER-vormingus Wordi originaalmalli muudetud malliga, mis sisaldab nüüd Wordi sisukontrolle, mis vastendati kohandatud XML-i osa **Aruanne** väljadega.</span><span class="sxs-lookup"><span data-stu-id="59730-127">You must then replace the original Word template of the editable ER format with the modified template that now contains Word content controls that were mapped to the fields of the **Report** custom XML part.</span></span>

![Malli asendamine vormingukujundaja lehel](./media/er-design-configuration-word-image7.gif)

<span data-ttu-id="59730-129">Konfigureeritud ER-vormingu käivitamisel kasutatakse uue aruande loomiseks lisatud Wordi malli.</span><span class="sxs-lookup"><span data-stu-id="59730-129">When you run the configured ER format, the attached Word template is used to generate a new report.</span></span> <span data-ttu-id="59730-130">Tegelikud andmed talletatakse Wordi aruandes kohandatud XML-i osana nimega **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="59730-130">The actual data is stored in the Word report as a custom XML part that is named **Report**.</span></span> <span data-ttu-id="59730-131">Loodud aruande avamisel täidetakse Wordi sisukontrollid kohandatud XML-i osa **Aruanne** andmetega.</span><span class="sxs-lookup"><span data-stu-id="59730-131">When the generated report is opened, the Word content controls are filled in with data from the **Report** custom XML part.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="59730-132">Korduma kippuvad küsimused</span><span class="sxs-lookup"><span data-stu-id="59730-132">Frequently asked questions</span></span>

<span data-ttu-id="59730-133">**Küsimus.** Ma konfigureerisin ER-vormingu, et printida Wordi dokument, mis sisaldab ettevõtte aadressi.</span><span class="sxs-lookup"><span data-stu-id="59730-133">**Question:** I configured an ER format to print a Word document that contains a company address.</span></span> <span data-ttu-id="59730-134">Wordi dokumendis lisasin selle ER-vormingu jaoks RTF-teksti sisukontrolli ettevõtte aadressi esitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="59730-134">In the Word template for this ER format, I inserted a rich text content control to present a company address.</span></span> <span data-ttu-id="59730-135">Rakenduses Finance sisestasin ettevõtte aadressi mitmerealise tekstina ja vajutasin **sisestusklahvi**, et lisada igale sisestatud reale kaubatagastuse.</span><span class="sxs-lookup"><span data-stu-id="59730-135">In Finance, I entered the company address as multiline text and selected **Enter** to add a carriage return for every line that I entered.</span></span> <span data-ttu-id="59730-136">Seega ma eeldan, et ettevõtte aadress ilmub loodud dokumentides mitmerealise tekstina.</span><span class="sxs-lookup"><span data-stu-id="59730-136">Therefore, I expect the company address to appear as multiline text in generated documents.</span></span> <span data-ttu-id="59730-137">Selle asemel ilmub aadress ühe tekstireana, mis sisaldab kaubatagastuste asemel erisümboleid.</span><span class="sxs-lookup"><span data-stu-id="59730-137">However, the address appears as a single line of text that contains special symbols instead of carriage returns.</span></span> <span data-ttu-id="59730-138">Mis mu sätetel viga on?</span><span class="sxs-lookup"><span data-stu-id="59730-138">What is wrong with my settings?</span></span>

<span data-ttu-id="59730-139">**Vastus.** RTF-teksti sisukontrolli asemel peate kasutama lihtteksti sisukontrolli ja valima juhtelemendi atribuutides märkeruudu **Luba kaubatagastused (mitu paragrahvi)**.</span><span class="sxs-lookup"><span data-stu-id="59730-139">**Answer:** Instead of using a rich text content control, you must use a plain text content control and select the **Allow carriage returns (multiple paragraphs)** check box in the control's properties.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59730-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="59730-140">Additional resources</span></span>

- [<span data-ttu-id="59730-141">Exceli mallidega ER-i konfiguratsioonide taaskasutamine Wordi vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="59730-141">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="59730-142">Manustatud pildid ja kujutised ER-iga loodud dokumentides</span><span class="sxs-lookup"><span data-stu-id="59730-142">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)