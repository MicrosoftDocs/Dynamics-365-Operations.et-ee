---
title: Microsoft Office stiili kasutajaliides äridokumendi halduses
description: See teema selgitab kuidas kasutada uut kasutajaliidest elektroonilise aruandluse (ER) raamistikku äridokumendi halduse funktsioonis.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881032"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="21a6f-103">Microsoft Office stiili kasutajaliides äridokumendi halduses</span><span class="sxs-lookup"><span data-stu-id="21a6f-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21a6f-104">Äridokumendi haldus võimaldab ärikasutajatel redigeerida äridokumendi malle Microsoft 365 teenuse või asjakohase Microsoft Office'i töölauarakendusega.</span><span class="sxs-lookup"><span data-stu-id="21a6f-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="21a6f-105">Muudatused võivad hõlmata kujunduse muudatusi või uusi juurutusi, või kasutajad võivad lisada kohatäited, et kaasata täiendavaid andmeid, ilma et peaksite lähtekoodi muutma.</span><span class="sxs-lookup"><span data-stu-id="21a6f-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="21a6f-106">Lisateavet äridokumentide haldusega töötamise kohta vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="21a6f-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="21a6f-107">Uus kasutajaliides (UI) on selgem ja seda on mugavam kasutada.</span><span class="sxs-lookup"><span data-stu-id="21a6f-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="21a6f-108">**Äridokumendi** ala näitab ainult malle, mis on saadaval praegusele pakkujale.</span><span class="sxs-lookup"><span data-stu-id="21a6f-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="21a6f-109">Eelmises kasutajaliideses loetleti vahekaardil **Mall** kõik mallid, mis olid saadaval kõigile pakkujatele.</span><span class="sxs-lookup"><span data-stu-id="21a6f-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="21a6f-110">Näitab kõiki malle, mille on loonud ja redigeerinud iga sama rolliga kasutaja.</span><span class="sxs-lookup"><span data-stu-id="21a6f-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="21a6f-111">Saate kasutada **Uue dokumendi** nuppu, mis võimaldab luua ja redigeerida malli elektroonilise aruandluse (ER) vormingu konfiguratsioonis, mida pakub teine pakkuja.</span><span class="sxs-lookup"><span data-stu-id="21a6f-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="21a6f-112">Selle teema näites on pakkuja Microsoft.</span><span class="sxs-lookup"><span data-stu-id="21a6f-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="21a6f-113">Teise võimalusena saate malli luua oma malli Exceli vormingus üles laadides.</span><span class="sxs-lookup"><span data-stu-id="21a6f-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="21a6f-114">[Äridokumendi halduse abil uue äridokumendi loomise](https://youtu.be/gAIYl-mM_pw) video (näidatud ülal) leiab [esitlusloendist Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) rakenduses YouTube.</span><span class="sxs-lookup"><span data-stu-id="21a6f-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="21a6f-115">Tee uus dokumendi kasutajaliides äridokumentide halduses kättesaadavaks</span><span class="sxs-lookup"><span data-stu-id="21a6f-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="21a6f-116">Et alustada uue dokumendi kasutajaliidese kasutamist äridokumentide halduses peate **Office'i sarnase kasutajaliidese kogemuse äridokumendi halduses** **Funktsiooni halduse** tööruumis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="21a6f-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="21a6f-117">Kõigi juriidiliste isikute jaoks selle funktsiooni sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="21a6f-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="21a6f-118">Valige **Fuktsioonide halduse** tööruumis vahekaardil **Kõik** loendis funktsioon **Office'i sarnase kasutajaliidese kogemus äridokumendi haldamises**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="21a6f-119">Valitud funktsiooni lubamiseks valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="21a6f-120">Uue funktsiooni kasutamiseks värskenda lehte.</span><span class="sxs-lookup"><span data-stu-id="21a6f-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="21a6f-121">Muutke teiste pakkujate malle</span><span class="sxs-lookup"><span data-stu-id="21a6f-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="21a6f-122">Valige **Äridokumentide halduse** tööruumis **Uus dokument**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Äridokumentide halduse tööruum](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="21a6f-124">Vahekaardil **Vali** valige mallina kasutatav dokument ja seejärel valige **Loo dokument**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Äridokumentide dialoogiboks](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="21a6f-126">Muutke vajadusel pealkiri uue dialoogiboksi väljal **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="21a6f-127">Pealkirja tekstiga nimetatakse ise tekkivat uut ER-vormingu seadistust.</span><span class="sxs-lookup"><span data-stu-id="21a6f-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="21a6f-128">Seda muudetavat malli sisaldava seadistuse (**Kliendi FTI aruande (GER) koopia**) mustandit ja ER-vormingu praeguse kasutaja puhul.</span><span class="sxs-lookup"><span data-stu-id="21a6f-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="21a6f-129">ER-vormingu põhiseadistuse muutmata algset malli kasutatakse selle ER-vormingu käivitamiseks kõikide kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="21a6f-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="21a6f-130">Muutke väljal **Nimi** isetekkiva muudetava malli esimese redaktsiooni nime.</span><span class="sxs-lookup"><span data-stu-id="21a6f-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="21a6f-131">Väljal **Kommentaar** värskendage isetekkiva muudetava malli redaktsiooni märkusi.</span><span class="sxs-lookup"><span data-stu-id="21a6f-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="21a6f-132">Muutmis alustamise kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dokumendi loomise dialoogiboks](./media/BDM_overview_new_template3.png)

<span data-ttu-id="21a6f-134">**Uue dokumendi** nuppu kasutatakse malli loomiseks ja redigeerimiseks elektroonilise aruandluse (ER) vormingu konfiguratsioonis, mida pakub teine pakkuja.</span><span class="sxs-lookup"><span data-stu-id="21a6f-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="21a6f-135">Selles näites on pakkuja Microsoft.</span><span class="sxs-lookup"><span data-stu-id="21a6f-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="21a6f-136">Kui valite suvandi **Uus dokument**, saate vaadata kõiki praeguse ja teiste pakkujate omanduses olevaid malle.</span><span class="sxs-lookup"><span data-stu-id="21a6f-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="21a6f-137">Pärast malli valimist avatakse see redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="21a6f-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="21a6f-138">Muudetud malli saab seejärel muuta uues ise loodavas ER-vormingus seadistusega.</span><span class="sxs-lookup"><span data-stu-id="21a6f-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="21a6f-139">Olemasolevat Exceli vormingut kasutava malli üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="21a6f-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="21a6f-140">Enne malli üleslaadimist vajaliku teabe esitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="21a6f-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="21a6f-141">Valige **Äridokumentide halduse** tööruumis **Uus dokument**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Äridokumentide halduse tööruum](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="21a6f-143">Klõpsake lehe **Uue malli loomine** vahekaardi **Üleslaadimine** vahekaardil **Mall** nuppu **Sirvi**, et leida ja valida Exceli fail, mida soovite mallina kasutada.</span><span class="sxs-lookup"><span data-stu-id="21a6f-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="21a6f-144">Jaotises **Mall** täidetakse väljad **Pealkiri** ja **Kirjeldus** automaatselt.</span><span class="sxs-lookup"><span data-stu-id="21a6f-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="21a6f-145">Nad määravad automaatselt loodava uue ER-vormingu konfiguratsiooni nime ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="21a6f-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="21a6f-146">Vajadusel saate neid välju redigeerida.</span><span class="sxs-lookup"><span data-stu-id="21a6f-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="21a6f-147">Määrake jaotise **Dokumendi liik** väljal **Nimi** äridokumendi liik.</span><span class="sxs-lookup"><span data-stu-id="21a6f-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="21a6f-148">Seda väärtust kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="21a6f-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Vahekaart Mall](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="21a6f-150">Klõpsake menüü **Andmeallikas** kiirkaardil **Filter** nuppu **Rakenda filter**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="21a6f-151">Jaotises **Andmeallikas** täidetakse väli **Nimi** automaatselt või saate väärtuse käsitsi valida.</span><span class="sxs-lookup"><span data-stu-id="21a6f-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="21a6f-152">Filtri abil saate otsida sobivat andmeallika nime nime, kirjelduse, riigi/regiooni tähise ja äridokumendi liigi alusel.</span><span class="sxs-lookup"><span data-stu-id="21a6f-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Andmeallika vahekaart](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="21a6f-154">Kiirkaarti **Filter** kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="21a6f-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="21a6f-155">Üleslaaditava dokumendi jaoks sobivaima andmeallika leidmiseks saate redigeerida kõiki filtrivälju.</span><span class="sxs-lookup"><span data-stu-id="21a6f-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="21a6f-156">Kiirkaardi **Filter** tingimusi kasutatakse **OR**-tingimustena.</span><span class="sxs-lookup"><span data-stu-id="21a6f-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="21a6f-157">Valige vahekaardil **Vastendamine** käsk **Tuvasta automaatselt**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="21a6f-158">Väli **Ruudi definitsioon** täidetakse automaatselt või saate väärtuse käsitsi valida.</span><span class="sxs-lookup"><span data-stu-id="21a6f-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="21a6f-159">Sellel vahekaardil kuvatakse malli ja mudeli elementide lõppvastendus.</span><span class="sxs-lookup"><span data-stu-id="21a6f-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Vahekaart Vastendamine](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="21a6f-161">Jaotise **Malli struktuur** vastendamine kasutab andmeallika siltide või kirjelduste täielikku vastendust kasutaja keeles ja malli lahtrinimes.</span><span class="sxs-lookup"><span data-stu-id="21a6f-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="21a6f-162">Malli loomise kinnitamiseks ja redigeerimisprotsessi alustamiseks valige **Loo dokument**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="21a6f-163">Lisateavet vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="21a6f-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="21a6f-164">Kui elektroonilises aruandluses pole teenusepakkujat, saate selle luua.</span><span class="sxs-lookup"><span data-stu-id="21a6f-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="21a6f-165">Kui aktiivset pakkujat pole, saate selle aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="21a6f-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="21a6f-166">Pakkuja loomiseks muutke väljal **Nimi** teenusepakkuja nime, värskendage uue pakkuja välja **Interneti-aadress** ja klõpsake kinnitamiseks nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="21a6f-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![BDM-is uue pakkuja loomine](./media/bdm_create_provider.png)
    
- <span data-ttu-id="21a6f-168">Olemasoleva pakkuja aktiveerimiseks valige väljal **Konfiguratsioonipakkuja** pakkuja pakkuja nimi ja valige **OK**, et seada pakkuja aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="21a6f-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Pakkuja aktiveerimine BDM-is](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="21a6f-170">Iga BDM-i mall viitab pakkujale kui konfiguratsiooni autorile.</span><span class="sxs-lookup"><span data-stu-id="21a6f-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="21a6f-171">Seetõttu on malli jaoks vaja aktiivset pakkujat.</span><span class="sxs-lookup"><span data-stu-id="21a6f-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
