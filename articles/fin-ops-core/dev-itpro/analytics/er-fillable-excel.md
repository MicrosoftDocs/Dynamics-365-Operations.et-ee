---
title: Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus
description: Selles teemas antakse teavet selle kohta, kuidas kujundada elektroonilise aruandluse (ER) vormingut Exceli malli täitmiseks ja seejärel luua väljaminevaid Exceli vormingus dokumente.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5733e40c67f9c97b04f126f7c3cfea9d4f8f5b5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686534"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="bd64c-103">Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus</span><span class="sxs-lookup"><span data-stu-id="bd64c-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bd64c-104">Saate luua [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) vormingu konfiguratsiooni, millel on ER-i [vormingu komponent](general-electronic-reporting.md#FormatComponentOutbound), mida saate konfigureerida väljamineva Microsoft Exceli töövihiku vormingus dokumendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="bd64c-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="bd64c-105">Sellel otstarbel tuleb kasutada kindlaid ER-vormingu komponente.</span><span class="sxs-lookup"><span data-stu-id="bd64c-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="bd64c-106">Lisateabe saamiseks selle funktsiooni kohta, järgige teemas [Konfiguratsiooni kujundamine aruannete loomiseks OPENXML-vormingus](tasks/er-design-reports-openxml-2016-11.md) toodud etappe.</span><span class="sxs-lookup"><span data-stu-id="bd64c-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="bd64c-107">Uue ER-vormingu lisamine</span><span class="sxs-lookup"><span data-stu-id="bd64c-107">Add a new ER format</span></span>

<span data-ttu-id="bd64c-108">Kui lisate uue ER-vormingu konfiguratsiooni Exceli töövihiku vormingus väljamineva dokumendi loomiseks, peate valima väärtuse **Excel** vormingu atribuudi **Vormingu tüüp** jaoks või jätma atribuudi **Vormingu tüüp** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="bd64c-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="bd64c-109">Kui teete valiku **Excel**, saate konfigureerida vormingu väljamineva dokumendi loomiseks ainult Exceli vormingus.</span><span class="sxs-lookup"><span data-stu-id="bd64c-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="bd64c-110">Kui jätate atribuudi tühjaks, saate konfigureerida vormingu väljamineva dokumendi loomiseks mis tahes vormingus, mida ER-i raamistik toetab.</span><span class="sxs-lookup"><span data-stu-id="bd64c-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="bd64c-111">Konfiguratsiooni ER-vormingu komponendi konfigureerimiseks valige Toimingupaanil **Kujundaja** ja avage ER-vormingu komponent selle redigeerimiseks ER-i toimingu koostajas.</span><span class="sxs-lookup"><span data-stu-id="bd64c-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Konfiguratsioonide leht](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="bd64c-113">Exceli faili komponent</span><span class="sxs-lookup"><span data-stu-id="bd64c-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="bd64c-114">Käsitsi kirje</span><span class="sxs-lookup"><span data-stu-id="bd64c-114">Manual entry</span></span>

<span data-ttu-id="bd64c-115">Peate lisama konfigureeritud ER-vormingule komponendi **Excel\\File**, et luua Exceli vormingus väljaminev dokument.</span><span class="sxs-lookup"><span data-stu-id="bd64c-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Komponent Excel\File](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="bd64c-117">Väljamineva dokumendi paigutuse määramiseks lisage Exceli töövihik, millel on laiend .xlsx, komponendile **Excel\\File** väljaminevate dokumentide mallina kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="bd64c-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="bd64c-118">Malli käsitsi manustamisel peate kasutama [dokumendi tüüpi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), mis on konfigureeritud selleks otstarbeks [ER-i parameetrites](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="bd64c-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Komponendile Excel\fail manuse lisamine](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="bd64c-120">Selleks, et määrata, kuidas lisatud mall täidetakse konfigureeritud ER-vormingu käitamisel, tuleb teil lisada pesastatud komponendid **Leht**, **Vahemik** ja **Lahter** komponendile **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="bd64c-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="bd64c-121">Iga pesastatud komponent peab olema seostatud Exceli nimega üksusega.</span><span class="sxs-lookup"><span data-stu-id="bd64c-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="bd64c-122">Malli importimine</span><span class="sxs-lookup"><span data-stu-id="bd64c-122">Template import</span></span>

<span data-ttu-id="bd64c-123">Saate valida Toimingupaani **Excelist importimine** vahekaardi **Importimine**, et importida uus mall tühja ER-vormingusse.</span><span class="sxs-lookup"><span data-stu-id="bd64c-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="bd64c-124">Selles näites luuakse komponent **Excel\\File** automaatselt ja sellele manustatakse imporditud mall.</span><span class="sxs-lookup"><span data-stu-id="bd64c-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="bd64c-125">Kõik nõutavad ER-komponendid luuakse samuti automaatselt, võttes aluseks leitud Exceli nimega üksuste loendi.</span><span class="sxs-lookup"><span data-stu-id="bd64c-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Suvandi Excelist importimine valimine](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="bd64c-127">Kui soovite luua redigeeritavas ER-vormingus valikulise elemendi **Leht** seadke suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="bd64c-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="bd64c-128">Lehe komponent</span><span class="sxs-lookup"><span data-stu-id="bd64c-128">Sheet component</span></span>

<span data-ttu-id="bd64c-129">Komponent **Leht** tähistab manustatud Exceli töövihiku töölehte, mis tuleb ära täita.</span><span class="sxs-lookup"><span data-stu-id="bd64c-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="bd64c-130">Exceli malli töölehe nimi määratletakse selle komponendi atribuudis **Leht**.</span><span class="sxs-lookup"><span data-stu-id="bd64c-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="bd64c-131">See komponent on valikuline Exceli töövihikute puhul, mis sisaldavad ühte töölehte.</span><span class="sxs-lookup"><span data-stu-id="bd64c-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="bd64c-132">ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Leht** jaoks atribuudi **Lubatud**, et määrata, kas komponent tuleks lisada loodud dokumenti.</span><span class="sxs-lookup"><span data-stu-id="bd64c-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="bd64c-133">Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, lisatakse loodud dokumenti vastav tööleht.</span><span class="sxs-lookup"><span data-stu-id="bd64c-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="bd64c-134">Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär**, ei sisalda loodud dokument töölehte.</span><span class="sxs-lookup"><span data-stu-id="bd64c-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Lehe komponendi näide](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="bd64c-136">Vahemiku komponent</span><span class="sxs-lookup"><span data-stu-id="bd64c-136">Range component</span></span>

<span data-ttu-id="bd64c-137">Komponent **Vahemik** tähistab Exceli vahemikku, mida selle ER-komponendiga tuleb juhtida.</span><span class="sxs-lookup"><span data-stu-id="bd64c-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="bd64c-138">Vahemiku nimi määratletakse selle komponendi atribuudis **Exceli vahemik**.</span><span class="sxs-lookup"><span data-stu-id="bd64c-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="bd64c-139">Atribuut **Edastamise suund** määrab, kas ja kuidas vahemik kordub loodud dokumendis.</span><span class="sxs-lookup"><span data-stu-id="bd64c-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="bd64c-140">Kui atribuudi **Edastamise suund** värtuseks on seatud **Andmeedastust pole**, ei korrata loodud dokumendis vastavat Exceli vahemikku.</span><span class="sxs-lookup"><span data-stu-id="bd64c-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="bd64c-141">Kui atribuudi **Edastamise suund** värtuseks on seatud **Vertikaalne**, korratakse loodud dokumendis vastavat Exceli vahemikku.</span><span class="sxs-lookup"><span data-stu-id="bd64c-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="bd64c-142">Iga edastatud vahemik lisatakse Exceli mallis algse vahemiku alla.</span><span class="sxs-lookup"><span data-stu-id="bd64c-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="bd64c-143">Korduste arv määratletakse tüübi **Kirje loend** andmeallika kirjete arvu põhjal, mis seotakse selle ER-komponendiga.</span><span class="sxs-lookup"><span data-stu-id="bd64c-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="bd64c-144">Kui atribuudi **Edastamise suund** värtuseks on seatud **Horisontaalne**, korratakse loodud dokumendis vastavat Exceli vahemikku.</span><span class="sxs-lookup"><span data-stu-id="bd64c-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="bd64c-145">Iga edastatud vahemik lisatakse Exceli mallis algsest vahemikust paremale.</span><span class="sxs-lookup"><span data-stu-id="bd64c-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="bd64c-146">Korduste arv määratletakse tüübi **Kirje loend** andmeallika kirjete arvu põhjal, mis seotakse selle ER-komponendiga.</span><span class="sxs-lookup"><span data-stu-id="bd64c-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="bd64c-147">Horisontaalse edastamise kohta lisateabe saamiseks järgige teemas [Horisontaalselt laiendatavate vahemike kasutamine Exceli aruannete veergude lisamiseks dünaamiliselt](tasks/er-horizontal-1.md) toodud etappe.</span><span class="sxs-lookup"><span data-stu-id="bd64c-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="bd64c-148">Komponendil **Vahemik** võib olla muid pesastatud ER-komponente, mida kasutatakse vastavate Exceli nimega vahemike väärtuste sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="bd64c-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="bd64c-149">Kui mõnda grupi **Tekst** komponenti kasutatakse väärtuste sisestamiseks, sisestatakse väärtus Exceli vahemikku teksti väärtusena.</span><span class="sxs-lookup"><span data-stu-id="bd64c-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd64c-150">Saate kasutada seda mustrit sisestatud väärtuste vormindamiseks rakenduses määratletud lokaadi alusel.</span><span class="sxs-lookup"><span data-stu-id="bd64c-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="bd64c-151">Kui grupi **Excel** komponenti **Lahter** kasutatakse väärtuste sisestamiseks, sisestatakse väärtus Exceli vahemikku andmetüübi väärtusena, mis määratletakse selle komponendi **Lahter** sidumisega (nt **String**, **Tegelik** või **Täisarv**).</span><span class="sxs-lookup"><span data-stu-id="bd64c-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd64c-152">Saate kasutada seda mustrit, et lubada Exceli rakendusel vormindada sisestatud väärtusi kohaliku arvuti lokaadi alusel, mis avab väljamineva dokumendi.</span><span class="sxs-lookup"><span data-stu-id="bd64c-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="bd64c-153">ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Vahemik** jaoks atribuudi **Lubatud**, et määrata, kas komponent tuleks lisada loodud dokumenti.</span><span class="sxs-lookup"><span data-stu-id="bd64c-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="bd64c-154">Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, täidetakse loodud dokumedis vastav vahemik.</span><span class="sxs-lookup"><span data-stu-id="bd64c-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="bd64c-155">Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär** ja see vahemik ei esinda terveid ridu või veerge, ei täideta loodud dokumedis vastavat vahemikku.</span><span class="sxs-lookup"><span data-stu-id="bd64c-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="bd64c-156">Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär** ja see vahemik esindab terveid ridu või veerge, sisaldab loodud dokument neid ridu ja veerge peidetud ridade ja veergudena.</span><span class="sxs-lookup"><span data-stu-id="bd64c-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="bd64c-157">Lahtri komponent</span><span class="sxs-lookup"><span data-stu-id="bd64c-157">Cell component</span></span>

<span data-ttu-id="bd64c-158">Komponenti **Lahter** kasutatakse Exceli nimega lahtrite, kujundite ja piltide täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="bd64c-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="bd64c-159">Selleks, et näidata Exceli nimega objekti, mille peab täitma ER-komponent **Lahter**, peate määrama selle objekti nime komponendi **Lahter** atribuudis **Exceli vahemik**.</span><span class="sxs-lookup"><span data-stu-id="bd64c-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="bd64c-160">ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Lahter** jaoks atribuudi **Lubatud**, et määrata, kas objekt tuleks täita loodud dokumendis.</span><span class="sxs-lookup"><span data-stu-id="bd64c-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="bd64c-161">Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, täidetakse loodud dokumedis vastav objekt.</span><span class="sxs-lookup"><span data-stu-id="bd64c-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="bd64c-162">Selle komponendi **Lahter** sidumine määrab väärtuse, mis lisatakse vastavale objektile.</span><span class="sxs-lookup"><span data-stu-id="bd64c-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="bd64c-163">Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär**, ei täideta loodud dokumendis vastavat objekti.</span><span class="sxs-lookup"><span data-stu-id="bd64c-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="bd64c-164">Kui komponent **Lahter** konfigureeritakse sisestama väärtust lahtrisse, saab seda siduda andmeallikaga, mis tagastab primitiivse andmetüübi väärtuse (nt **String**, **Tegelik** või **Täisarv**).</span><span class="sxs-lookup"><span data-stu-id="bd64c-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="bd64c-165">Sellisel juhul sisestatakse väärtus lahtrisse sama andmetüübi väärtusena.</span><span class="sxs-lookup"><span data-stu-id="bd64c-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="bd64c-166">Kui komponent **Lahter** konfigureeritakse sisestama väärtust Exceli kujundisse, saab seda siduda andmeallikaga, mis tagastab primitiivse andmetüübi väärtuse (nt **String**, **Tegelik** või **Täisarv**).</span><span class="sxs-lookup"><span data-stu-id="bd64c-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="bd64c-167">Sellisel juhul sisestatakse väärtus Exceli kujundisse selle kujundi tekstina.</span><span class="sxs-lookup"><span data-stu-id="bd64c-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="bd64c-168">Andmetüüpide väärtused, mis ei ole **String**, teisendatakse tekstiks automaatselt.</span><span class="sxs-lookup"><span data-stu-id="bd64c-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="bd64c-169">Saate konfigureerida komponendi **Lahter** täitma kujundit ainult juhul, kui kujundi teksti atribuuti toetatakse.</span><span class="sxs-lookup"><span data-stu-id="bd64c-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="bd64c-170">Kui komponent **Lahter** konfigureeritakse sisestama väärtust Exceli pilti, saab seda siduda andmeallikaga, mis tagastab andmetüübi **Konteiner** väärtuse, mis esindab pilti binaarvormingus.</span><span class="sxs-lookup"><span data-stu-id="bd64c-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="bd64c-171">Sellisel juhul sisestatakse Exceli pildil olev väärtus pildina.</span><span class="sxs-lookup"><span data-stu-id="bd64c-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="bd64c-172">Kõik Exceli pildid ja kujundid on mõeldud kindla Exceli lahtri või vahemiku vasakusse ülanurka ankurdamiseks.</span><span class="sxs-lookup"><span data-stu-id="bd64c-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="bd64c-173">Kui soovite Exceli pilti või kujundit kopeerida, peate konfigureerima lahtri või vahemiku, millele see on ankurdatud, kopeeritud lahtri või vahemikuna.</span><span class="sxs-lookup"><span data-stu-id="bd64c-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="bd64c-174">Lisateavet piltide ja kujundite manustamise kohta leiate teemast [Piltide ja kujundite manustamine ER-i abil loodud dokumentidesse](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="bd64c-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="bd64c-175">Lehepiiri komponent</span><span class="sxs-lookup"><span data-stu-id="bd64c-175">Page break component</span></span>

<span data-ttu-id="bd64c-176">Komponent **PageBreak** sunnib Excelit uut lehte alustama.</span><span class="sxs-lookup"><span data-stu-id="bd64c-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="bd64c-177">See komponent pole nõutav, kui soovite kasutada Exceli vaikimisi lehekülgede saalimist, kuid peaksite seda kasutama juhul, kui soovite, et Excel järgiks teie ER-vormingut lehekülgede saalimise struktureerimisel.</span><span class="sxs-lookup"><span data-stu-id="bd64c-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="bd64c-178">Lisatud ER-vormingu redigeerimine</span><span class="sxs-lookup"><span data-stu-id="bd64c-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="bd64c-179">Malli värskendamine</span><span class="sxs-lookup"><span data-stu-id="bd64c-179">Update a template</span></span>

<span data-ttu-id="bd64c-180">Saate valida Toimingupaani **Excelist värskendamine** vahekaardi **Importimine**, et importida värskendatud mall redigeeritavasse ER-vormingusse.</span><span class="sxs-lookup"><span data-stu-id="bd64c-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="bd64c-181">Selle protsessi käigus asendatakse valitud komponent **Excel\\File** uue malliga.</span><span class="sxs-lookup"><span data-stu-id="bd64c-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="bd64c-182">Redigeeritava ER-vormingu sisu sünkroonitakse värskendatud ER-i malli sisuga.</span><span class="sxs-lookup"><span data-stu-id="bd64c-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="bd64c-183">Uus ER-vormingu komponent luuakse automaatselt iga Exceli nime kohta, kui redigeeritavast vormist ei leida ER-vormingu komponenti.</span><span class="sxs-lookup"><span data-stu-id="bd64c-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="bd64c-184">Redigeeritavast ER-vormingust kustutatakse kõik ER-vormingu komponendid, mille kohta ei ei leita sobivat Exceli nime.</span><span class="sxs-lookup"><span data-stu-id="bd64c-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="bd64c-185">Seadke suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**, kui soovite luua redigeeritavas ER-vormingus valikulise elemendi **Leht**.</span><span class="sxs-lookup"><span data-stu-id="bd64c-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="bd64c-186">Kui redigeeritav ER-vorming sisaldas algselt elemente **Leht**, soovitame teil värskendatud malli importimisel määdata suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="bd64c-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="bd64c-187">Vastasel juhul luuakse kõik algse elemendi **Leht** pesastatud elemendid nullist.</span><span class="sxs-lookup"><span data-stu-id="bd64c-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="bd64c-188">Seetõttu lähevad kõik uuesti loodud vorminguelementide sidumised värskendatud ER-vormingus kaotsi.</span><span class="sxs-lookup"><span data-stu-id="bd64c-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Exceli vorminguelemendi Leht suvandi loomine dialoogiboksis Excelist värskendamine](./media/er-excel-format-update-template.png)

<span data-ttu-id="bd64c-190">Selle funktsiooni kohta lisateabe saamiseks järgige teemas [Elekrtoonilise aruandluse muutmine Exceli mallide uuesti rakendamise teel](modify-electronic-reporting-format-reapply-excel-template.md) toodud etappe.</span><span class="sxs-lookup"><span data-stu-id="bd64c-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="bd64c-191">ER-vormingu kinnitamine</span><span class="sxs-lookup"><span data-stu-id="bd64c-191">Validate an ER format</span></span>

<span data-ttu-id="bd64c-192">Kui kinnitate redigeeritavat ER-vormingut, tehakse järjepidevuse kontroll, et veenduda, kas Exceli nimi on praegu kasutatavas Exceli mallis olemas.</span><span class="sxs-lookup"><span data-stu-id="bd64c-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="bd64c-193">Teid teavitatakse kõigist vastuoludest.</span><span class="sxs-lookup"><span data-stu-id="bd64c-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="bd64c-194">Osade vastuolude korral pakutakse probleemi automaatse lahendamise valikut.</span><span class="sxs-lookup"><span data-stu-id="bd64c-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Kinnitamise tõrketeated](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a><span data-ttu-id="bd64c-196">Exceli valemite arvutamise juhtimine</span><span class="sxs-lookup"><span data-stu-id="bd64c-196">Control the calculation of Excel formulas</span></span>

<span data-ttu-id="bd64c-197">Kui luuakse väljaminev töövihikuvormingus Microsoft Exceli dokument, võivad mõned selle dokumendi lahtrid sisaldada Exceli valemeid.</span><span class="sxs-lookup"><span data-stu-id="bd64c-197">When an outbound document in a Microsoft Excel workbook format is generated, some cells of this document might contain Excel formulas.</span></span> <span data-ttu-id="bd64c-198">Kui funktsioon **Luba EPPlusi teegi kasutamine elektroonilise aruandluse raamistikus** on lubatud, saate kontrollida, millal valemid arvutatakse, muutes kasutatavas Exceli mallis **arvutamise valikute** [parameetrit](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows).</span><span class="sxs-lookup"><span data-stu-id="bd64c-198">When the **Enable usage of EPPlus library in Electronic reporting framework** feature is enabled, you can control when the formulas are calculated by changing the value of the **Calculation Options** [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) in the Excel template that is being used:</span></span>

- <span data-ttu-id="bd64c-199">Valige suvand **Automaatne**, et arvutada kõik sõltuvad valemid iga kord uuesti, kui loodud dokumendile lisatakse uued vahemikud, lahtrid jne.</span><span class="sxs-lookup"><span data-stu-id="bd64c-199">Select **Automatic** to recalculate all dependent formulas every time a generated document is appended by new ranges, cells, etc.</span></span>
    >[!NOTE]
    > <span data-ttu-id="bd64c-200">See võib põhjustada mitut seotud valemit sisaldavate Exceli mallide korral jõudlusprobleemi.</span><span class="sxs-lookup"><span data-stu-id="bd64c-200">This might cause a performance issue for Excel templates that contain multiple related formulas.</span></span>
- <span data-ttu-id="bd64c-201">Valige **Käsitsi**, et vältida dokumendi loomisel valemi uuesti arvutamist.</span><span class="sxs-lookup"><span data-stu-id="bd64c-201">Select **Manual** to avoid formula recalculation when a document is generated.</span></span>
    >[!NOTE]
    > <span data-ttu-id="bd64c-202">Valemi uuesti arvutamine tehakse käsitsi, kui loodud dokument avatakse Excelit kasutades eelvaateks.</span><span class="sxs-lookup"><span data-stu-id="bd64c-202">Formula recalculation is manually forced when a generated document is opened for preview using Excel.</span></span>
    > <span data-ttu-id="bd64c-203">Ärge kasutage seda valikut, kui konfigureerite ER-i sihtkohta, mis eeldab loodud dokumendi kasutamist ilma selle eelvaateta Excelis (PDF-i teisendamine, meilimine jne)., kuna loodud dokument ei pruugi omada valemeid sisaldavates lahtrites väärtusi.</span><span class="sxs-lookup"><span data-stu-id="bd64c-203">Don't use this option if you configure an ER destination that assumes the usage of a generated document without its preview in Excel (PDF conversion, emailing, etc.)because the generated document might not contain values in cells that contain formulas.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd64c-204">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bd64c-204">Additional resources</span></span>

[<span data-ttu-id="bd64c-205">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="bd64c-205">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="bd64c-206">OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine</span><span class="sxs-lookup"><span data-stu-id="bd64c-206">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="bd64c-207">Elektroonilise aruandluse vormingute muutmine Exceli malle uuesti rakendades</span><span class="sxs-lookup"><span data-stu-id="bd64c-207">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="bd64c-208">Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes</span><span class="sxs-lookup"><span data-stu-id="bd64c-208">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="bd64c-209">Manustatud pildid ja kujutised ER-iga loodud dokumentides</span><span class="sxs-lookup"><span data-stu-id="bd64c-209">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="bd64c-210">Elektroonilise aruandluse (ER) konfigureerimine andmete tõmbamiseks Power BI-sse</span><span class="sxs-lookup"><span data-stu-id="bd64c-210">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
