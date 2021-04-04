---
title: Äridokumendi mallile uute väljade lisamine Microsoft Excelis
description: See teema annab teavet selle kohta, kuidas lisada äridokumendi halduse funktsiooni kasutades Microsoft Excelis äridokumendi malli uusi välju.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6368d763f44c015a6e85652b1880cfd86ff5ba09
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569017"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="39c65-103">Äridokumendi mallile uute väljade lisamine Microsoft Excelis</span><span class="sxs-lookup"><span data-stu-id="39c65-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="39c65-104">Saate lisada uusi välju mallile, mida kasutatakse Microsoft Exceli vormingus äridokumentide koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="39c65-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="39c65-105">Neid välju saab lisada kohatäidetena, mida kasutatakse loodud dokumentide täitmiseks rakendusest nõutava teabega.</span><span class="sxs-lookup"><span data-stu-id="39c65-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="39c65-106">Iga lisatava välja kohta saate määrata ka sidumise andmeallikatega, et määrata, millised rakenduse andmed väljale sisestatakse, kui malli kasutatakse äridokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="39c65-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="39c65-107">Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide.</span><span class="sxs-lookup"><span data-stu-id="39c65-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="39c65-108">Selles näites kirjeldatakse, kuidas värskendada malli, et täita vabas vormis arves loodud väljad.</span><span class="sxs-lookup"><span data-stu-id="39c65-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="39c65-109">Mallide muutmiseks äridokumentide halduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="39c65-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="39c65-110">Kuna äridokumentide haldus (BDM) on ehitatud raamistiku [elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md) peale, peate enne BDM-iga töötamise alustamist konfigureerima nõutud ER-i ja BDM-i parameetrid.</span><span class="sxs-lookup"><span data-stu-id="39c65-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="39c65-111">Logige Microsoft Dynamics 365 Finance’i eksemplari süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="39c65-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="39c65-112">Läbige näidise järgmised etapid teemas [Äridokumentide halduse ülevaade](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="39c65-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="39c65-113">Konfigureerige elektroonilise aruandluse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="39c65-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="39c65-114">Lülitage BDM sisse.</span><span class="sxs-lookup"><span data-stu-id="39c65-114">Turn on BDM.</span></span>

<span data-ttu-id="39c65-115">Nüüd saate hakata kasutama BDM-i äridokumentide mallide redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="39c65-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="39c65-116">Malli sisaldavate elektroonilise aruandluse lahenduste importimine</span><span class="sxs-lookup"><span data-stu-id="39c65-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="39c65-117">Selle protseduuri näites kasutatakse ametlikult avaldatud elektroonilise aruandluse lahendust.</span><span class="sxs-lookup"><span data-stu-id="39c65-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="39c65-118">Peate importima selle lahenduse elektroonilise aruandluse konfiguratsioonid oma praegusesse Finance’i eksemplari.</span><span class="sxs-lookup"><span data-stu-id="39c65-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="39c65-119">Selle lahenduse elektroonilise aruandluse konfiguratsioon **Vabas vormis arve (Excel)** sisaldab Exceli vormingus äridokumendi malli, mida saab BDM-i kasutades redigeerida.</span><span class="sxs-lookup"><span data-stu-id="39c65-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="39c65-120">Importige selle elektroonilise aruandluse vormingu konfiguratsiooni uusim versioon portaalist Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="39c65-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="39c65-121">Vastav ER-i andmemudel ja ER-i mudelivastenduse konfiguratsioonid imporditakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="39c65-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="39c65-122">Elektroonilise aruandluse konfiguratsioonide importimise kohta lisateabe saamiseks vt [ER-seadistuse töötsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="39c65-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS-i ühiste vahendite teegi leht](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="39c65-124">Elektroonilise aruandluse lahenduse malli redigeerimine</span><span class="sxs-lookup"><span data-stu-id="39c65-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="39c65-125">Logige sisse kasutajana, kellel on juurdepääs tööruumile **Äridokumentide haldus**.</span><span class="sxs-lookup"><span data-stu-id="39c65-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="39c65-126">Avage tööruum **Äridokumentide halduse**.</span><span class="sxs-lookup"><span data-stu-id="39c65-126">Open the **Business document management** workspace.</span></span>

    ![Äridokumentide halduse tööruum](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="39c65-128">Valige ruudustikus mall **Vabas vormis arve (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="39c65-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="39c65-129">Valige parempoolsel paanil **Uus mall**, et luua uus mall, mis põhineb valitud mallil.</span><span class="sxs-lookup"><span data-stu-id="39c65-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="39c65-130">Sisestage väljale **Pealkiri** uue malli pealkirjaks **Contoso vabas vormis arve (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="39c65-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="39c65-131">Muutmis alustamise kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="39c65-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="39c65-132">Kuvatakse BDM-i malli muutja leht.</span><span class="sxs-lookup"><span data-stu-id="39c65-132">The BDM template editor page appears.</span></span> <span data-ttu-id="39c65-133">Saate kasutada rakendust Microsoft 365, et redigeerida valitud malli veebis manustatud juhtelemendis.</span><span class="sxs-lookup"><span data-stu-id="39c65-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDM-i malli muutja leht](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="39c65-135">Malli uuele väljale sildi lisamine</span><span class="sxs-lookup"><span data-stu-id="39c65-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="39c65-136">Valige BDM-i malli muutja lehel Exceli lindil vahekaardil **Vaade** redigeeritava Exceli malli märkeruudud **Pealkirjad ja ruudujooned**.</span><span class="sxs-lookup"><span data-stu-id="39c65-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Märkeruudud Pealkirjad ja ruudujooned märgitud](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="39c65-138">Valige lahtrid **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="39c65-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="39c65-139">Valige Exceli lindi vahekaardil **Avaleht** suvand **Ühenda ja joonda keskel**, et ühendada valitud lahtrid uueks ühendatud lahtriks **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="39c65-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="39c65-140">Ühendatud lahtrisse **E8: F8** sisestage **URL**.</span><span class="sxs-lookup"><span data-stu-id="39c65-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="39c65-141">Valige ühendatud lahter **E7:F7**, valige **Vormingupintsel** ja seejärel valige ühendatud lahter **E8:F8**, et vormindada see sarnaselt ühendatud lahtrile **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="39c65-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Mallile lisatud uue välja silt](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="39c65-143">Malli vormindamine uue välja jaoks ruumi reserveerimiseks</span><span class="sxs-lookup"><span data-stu-id="39c65-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="39c65-144">Valige lehel BDM-i malli muutja ühendatud lahter **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="39c65-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="39c65-145">Valige Exceli lindi vahekaardil **Avaleht** suvand **Ühenda ja joonda keskel**, et ühendada valitud lahtrid uueks ühendatud lahtriks **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="39c65-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="39c65-146">Valige ühendatud lahter **G7:H7**, valige **Vormingupintsel** ja seejärel valige ühendatud lahter **G8:H8**, et vormindada see sarnaselt ühendatud lahtrile **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="39c65-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Uue välja jaoks reserveeritud ruum](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="39c65-148">Boksiväljal **Nimi** valige **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="39c65-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="39c65-149">Praeguse Exceli malli vahemik **CompanyInfo** sisaldab kõiki välju, mida kasutatakse loodud aruande päise täitmiseks koos praeguse ettevõtte kui müüja osapoole üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="39c65-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Vahemik CompanyInfo valitud](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="39c65-151">Mallile uue välja lisamine</span><span class="sxs-lookup"><span data-stu-id="39c65-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="39c65-152">Valige tegumiriba lehel **BDM-i malli muutja** suvand **Kuva vorming**.</span><span class="sxs-lookup"><span data-stu-id="39c65-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="39c65-153">Valige paanil **Malli struktuur** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="39c65-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39c65-154">Peate kohandama malli sektsiooni, mida soovite uue väljana kasutada.</span><span class="sxs-lookup"><span data-stu-id="39c65-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="39c65-155">Te juba tegite selle korrigeerimise ühendatud lahtri **G8:H8** vormindamisel.</span><span class="sxs-lookup"><span data-stu-id="39c65-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Mallile uue välja lisamine](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="39c65-157">Mallile uue välja lahtrina lisamiseks valige **Excel\lahter**.</span><span class="sxs-lookup"><span data-stu-id="39c65-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="39c65-158">Kui soovite mallile lisada uue vahemiku, saate valida **Excel\vahemik**.</span><span class="sxs-lookup"><span data-stu-id="39c65-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="39c65-159">Sisestatud vahemik võib sisaldada mitut lahtrit.</span><span class="sxs-lookup"><span data-stu-id="39c65-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="39c65-160">Saate need lahtrid lisada hiljem.</span><span class="sxs-lookup"><span data-stu-id="39c65-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="39c65-161">Pange tähele, et malli komponent **CompanyInfo** valitakse paanil **Malli struktuur** automaatselt, kuna see on praegu lisatava välja jaoks malli struktuuri kõige sobivam ülemkomponent.</span><span class="sxs-lookup"><span data-stu-id="39c65-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="39c65-162">Sisestage väljal **Exceli vahemik** suvand **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="39c65-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="39c65-163">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="39c65-163">Select **OK**.</span></span>

    ![Väli CompanyURL_Value lisatud malli struktuuri](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="39c65-165">Paanil **Malli struktuur** valige kolmikpunkti nupp (...) ja seejärel valige **Kuva seosed**.</span><span class="sxs-lookup"><span data-stu-id="39c65-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Kuva seosed valitud](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="39c65-167">Paan **Malli struktuur** näitab andmeallikaid, mis on asjakohases ER-vormingus saadaval.</span><span class="sxs-lookup"><span data-stu-id="39c65-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="39c65-168">Valige **CompanyInfo_Value** väljaks, mille plaanite asjakohase ER-vormingu andmeallikaga siduda.</span><span class="sxs-lookup"><span data-stu-id="39c65-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="39c65-169">Jaotises **Andmeallikas** paanil **Malli struktuur** laiendage suvandit **Mudel \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="39c65-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="39c65-170">Valige jaotises **CompanyInfo** üksus **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="39c65-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Üksus WebsiteURI valitud](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="39c65-172">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="39c65-172">Select **Bind**.</span></span>
11. <span data-ttu-id="39c65-173">Valige paanil **Malli struktuur** suvand **Salvesta** ja seejärel sulgege BDM-i malli muutja leht.</span><span class="sxs-lookup"><span data-stu-id="39c65-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="39c65-174">Tööruumi **Äridokumendi haldus** paremal paanil asuv vahekaart **Mall** näitab värskendatud malli.</span><span class="sxs-lookup"><span data-stu-id="39c65-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="39c65-175">Pange tähele, et ruudustikus on malli väli **Olek** muudetud suvandil **Mustand** ja väli **Redaktsioon** ei ole enam tühi.</span><span class="sxs-lookup"><span data-stu-id="39c65-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="39c65-176">Need muudatused näitavad, et selle malli muutmise protsess on alanud.</span><span class="sxs-lookup"><span data-stu-id="39c65-176">These changes indicate that the process of editing this template has been started.</span></span>

![Muudetud mall tööruumis Äridokumentide haldus](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="39c65-178">Ettevõtete sätete ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="39c65-178">Review company settings</span></span>

1.  <span data-ttu-id="39c65-179">Avage **Organisatsiooni haldus \> Organisatsioonid \> Juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="39c65-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="39c65-180">Kontrollige kiirkaardil **Kontaktteave**, kas ettevõtte URL on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="39c65-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Ettevõtte URL sisestatud lehele Juriidilised isikud](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="39c65-182">Äridokumentide loomine värskendatud malli testimiseks</span><span class="sxs-lookup"><span data-stu-id="39c65-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="39c65-183">Muutke rakenduses ettevõte valikule **USMF** ja avage **Müügireskontro \> Arved \> Kõik vabas vormis arved**.</span><span class="sxs-lookup"><span data-stu-id="39c65-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="39c65-184">Valige arve **FTI-00000002** ja seejärel valige **Prindihaldus**.</span><span class="sxs-lookup"><span data-stu-id="39c65-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="39c65-185">Vasakpoolsel paanil laiendage **Moodul – müügireskontro \> Dokumendid \> Vabas vormis arve**.</span><span class="sxs-lookup"><span data-stu-id="39c65-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="39c65-186">Suvandis **Vabas vormis arve** valge tase **Algne dokument**, et määratleda töötlemiseks arvete ulatus.</span><span class="sxs-lookup"><span data-stu-id="39c65-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="39c65-187">Valige paremal paanil väljal **Aruande vorming** mall **Contoso vabas vormis arve (Excel)** konkreetse dokumendi taseme jaoks.</span><span class="sxs-lookup"><span data-stu-id="39c65-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Mall Contoso vabas vormis arve (Excel) valitud](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="39c65-189">Praeguse lehe sulgemiseks vajutage **Paoklahvi (Esc)**.</span><span class="sxs-lookup"><span data-stu-id="39c65-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="39c65-190">Valige **Prindi \> Valitud**.</span><span class="sxs-lookup"><span data-stu-id="39c65-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="39c65-191">Laadige loodud dokument alla ja avage see Excelis.</span><span class="sxs-lookup"><span data-stu-id="39c65-191">Download the generated document, and open it in Excel.</span></span>

    ![Vabas vormis arve Excelis](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="39c65-193">Muudetud malliga luuakse valitud üksuse vabas tekstis arve aruanne.</span><span class="sxs-lookup"><span data-stu-id="39c65-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="39c65-194">Selleks, et analüüsida, kuidas malli muudatused mõjutavad seda aruannet, käivitage aruanne ühes rakenduse seansis kohe pärast malli muutmist teises rakenduse seansis.</span><span class="sxs-lookup"><span data-stu-id="39c65-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="39c65-195">Seotud lingid</span><span class="sxs-lookup"><span data-stu-id="39c65-195">Related links</span></span>

[<span data-ttu-id="39c65-196">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="39c65-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="39c65-197">Äridokumentide halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="39c65-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="39c65-198">OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine</span><span class="sxs-lookup"><span data-stu-id="39c65-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]