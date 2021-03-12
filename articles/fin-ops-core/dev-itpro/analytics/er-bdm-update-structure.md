---
title: Äridokumendimalli struktuuri värskendamine
description: See teema selgitab, kuidas värskendada äridokumendi malli struktuuri äridokumendi haldamise funktsiooni abil.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cb0188e372b5f6275472cf040d10bb796eed1858
ms.sourcegitcommit: 95d2fc0fa7d17d3a96f7969f12c985b018b4ff94
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/12/2020
ms.locfileid: "4728085"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="14338-103">Äridokumendimalli struktuuri värskendamine</span><span class="sxs-lookup"><span data-stu-id="14338-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="14338-104">**Malli struktuuri** paanil [äridokumendi halduse](er-business-document-management.md) malli redaktoris saate muuta äridokumendi malli, [lisades uued väljad](er-bdm-add-field-to-excel-template.md) Microsoft Exceli mallile.</span><span class="sxs-lookup"><span data-stu-id="14338-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="14338-105">Malli struktuuri värskendatakse seejärel automaatselt rakenduses Dynamics 365 Finance, nii et see kajastaks muudatusi, mida te paanil **Malli struktuur** tegite.</span><span class="sxs-lookup"><span data-stu-id="14338-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="14338-106">Samuti saate malli muuta, kasutades Office 365 veebipõhiseid funktsioone.</span><span class="sxs-lookup"><span data-stu-id="14338-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="14338-107">Näiteks saate lisada muudetavale töölehele uue nimega üksuse (nt pildi või kujundi).</span><span class="sxs-lookup"><span data-stu-id="14338-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="14338-108">Sel juhul malli struktuuri rakenduses Finance automaatselt ei värskendata ja lisatud üksus ei ilmu paanil **Malli struktuur**.</span><span class="sxs-lookup"><span data-stu-id="14338-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="14338-109">Värskendage malli struktuuri rakenduses Finance käsitsi, klõpsates malli redaktori lehel suvandi **Värskenda struktuuri**.</span><span class="sxs-lookup"><span data-stu-id="14338-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="14338-110">Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.</span><span class="sxs-lookup"><span data-stu-id="14338-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="14338-111">Näide. Äridokumendimalli struktuuri värskendamine</span><span class="sxs-lookup"><span data-stu-id="14338-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="14338-112">See näide näitab, kuidas süsteemiadministraator saab värskendada äridokumendi malli struktuuri rakenduses Finance pärast seda, kui mall on Office Online’is muudetud.</span><span class="sxs-lookup"><span data-stu-id="14338-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="14338-113">Järgmised jaotised selgitavad kaasatud etappe.</span><span class="sxs-lookup"><span data-stu-id="14338-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="14338-114">Äridokumendi malli redigeerimiseks ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="14338-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="14338-115">Tehke [äridokumendi halduse ülevaates](er-business-document-management.md) järgmised protseduurid.</span><span class="sxs-lookup"><span data-stu-id="14338-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="14338-116">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="14338-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="14338-117">Impordi ER-lahendused</span><span class="sxs-lookup"><span data-stu-id="14338-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="14338-118">Lubage äridokumentide haldus</span><span class="sxs-lookup"><span data-stu-id="14338-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="14338-119">Seadistage parameetrid</span><span class="sxs-lookup"><span data-stu-id="14338-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="14338-120">Äridokumendimallide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="14338-120">Edit a business document template</span></span>

1. <span data-ttu-id="14338-121">Valige **Äridokumentide halduse** tööruumis **Uus dokument**.</span><span class="sxs-lookup"><span data-stu-id="14338-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="14338-122">Valige lehel **Uue malli loomine** mall **Vabas vormis arve (ER-i näidis) (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="14338-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="14338-123">Valige **Loo dokument**.</span><span class="sxs-lookup"><span data-stu-id="14338-123">Select **Create document**.</span></span>
4. <span data-ttu-id="14338-124">Väljale **Pealkiri** sisestage väärtus **FTI näidis, Litware**.</span><span class="sxs-lookup"><span data-stu-id="14338-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="14338-125">Valige uue malli loomiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="14338-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14338-126">Kui te pole veel Office Online’i sisse loginud, [suunatakse teid Office 365 sisselogimise lehele](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="14338-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="14338-127">Rakenduse Finance keskkonda naasmiseks valige brauseris nupp **Tagasi**.</span><span class="sxs-lookup"><span data-stu-id="14338-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="14338-128">Uus mall on redigeerimiseks avatud Excel Online’i malli redaktori lehel manustatud juhtelemendis.</span><span class="sxs-lookup"><span data-stu-id="14338-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="14338-129">[![Äridokumentide halduse tööruumi kasutamine äridokumendi malli redigeerimise alustamiseks](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="14338-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="14338-130">Redigeeritava malli praeguse struktuuri läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="14338-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="14338-131">Klõpsake rakenduses Excel Online ribal vahekaardi **Vaade** grupi **Kuvamine** suvandit **Ruudujooned**.</span><span class="sxs-lookup"><span data-stu-id="14338-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="14338-132">Valige redigeeritavas mallis malli pealkirja kohal olev ristkülik.</span><span class="sxs-lookup"><span data-stu-id="14338-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="14338-133">See ristkülik on pilt, mille nimi on **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="14338-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="14338-134">Kui paan **Malli struktuur** on peidetud, valige **Kuva struktuur**.</span><span class="sxs-lookup"><span data-stu-id="14338-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="14338-135">Laiendage paanil **Malli struktuur** suvandit **Aruanne \> Arve \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="14338-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="14338-136">Pange tähele, et rakenduse Finance malli struktuuris on üksus **rptHeaderCompLogo** esitatud suvandi **Aruanne \> Arve \> rptHeader \> rptHeaderPart1** allüksusena.</span><span class="sxs-lookup"><span data-stu-id="14338-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="14338-137">[![Äridokumentide halduse tööruumi kasutamine redigeeritud malli praeguse struktuuri läbivaatamiseks](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="14338-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="14338-138">Äridokumendimalli struktuuri värskendamine kustutades pildi</span><span class="sxs-lookup"><span data-stu-id="14338-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="14338-139">Valige Excel Online’is redigeeritav mall, valige pilt **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="14338-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="14338-140">Valitud pildi redigeeritavast mallist kustutamiseks järgige üht järgmistest sammudest.</span><span class="sxs-lookup"><span data-stu-id="14338-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="14338-141">Valige klaviatuurilt klahv **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="14338-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="14338-142">Valige ja hoidke (või paremklõpsake) pilti ning valige seejärel suvand **Lõika**.</span><span class="sxs-lookup"><span data-stu-id="14338-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14338-143">Üksus **RptHeaderCompLogo** on praegu rakenduse Finance malli struktuuris endiselt alles, olgugi pilti enam Exceli malli ei lisata.</span><span class="sxs-lookup"><span data-stu-id="14338-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="14338-144">Valige **Värskenda struktuuri**, et sünkroonida redigeeritava malli struktuuri rakendustes Excel ja Finance.</span><span class="sxs-lookup"><span data-stu-id="14338-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="14338-145">Laiendage paanil **Malli struktuur** suvandit **Aruanne \> Arve \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="14338-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="14338-146">Pange tähele, et üksus **rptHeaderCompLogo** ei sisaldu enam rakenduse Finance malli struktuuris.</span><span class="sxs-lookup"><span data-stu-id="14338-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="14338-147">[![Äridokumentide halduse tööruumi kasutamine äridokumendi mallist pildi kustutamiseks](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="14338-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="14338-148">Äridokumendimalli struktuuri värskendamine lisades pildi</span><span class="sxs-lookup"><span data-stu-id="14338-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="14338-149">Klõpsake rakenduses Excel Online ribal vahekaardi **Lisamine** grupi **Illustratsioonid** suvandit **Pilt**.</span><span class="sxs-lookup"><span data-stu-id="14338-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="14338-150">Valige käsk **Vali fail**, sirvige pildini, mille soovite lisada, valige see ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="14338-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="14338-151">Valige nupp **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="14338-151">Select **Insert**.</span></span>
4. <span data-ttu-id="14338-152">Liigutage uut pilti, kuni see on õiges kohas.</span><span class="sxs-lookup"><span data-stu-id="14338-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="14338-153">Vaikimisi paneb pildile nime Excel.</span><span class="sxs-lookup"><span data-stu-id="14338-153">By default, Excel names the picture.</span></span> <span data-ttu-id="14338-154">Näiteks võib see panna pildi nimeks **Pilt 2**.</span><span class="sxs-lookup"><span data-stu-id="14338-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="14338-155">Valige **Värskenda struktuuri**, et sünkroonida redigeeritava malli struktuuri rakendustes Excel ja Finance.</span><span class="sxs-lookup"><span data-stu-id="14338-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="14338-156">Laiendage paanil **Malli struktuur** suvandit **Aruanne \> Arve \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="14338-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="14338-157">Pange tähele, et uus pilt on nüüd lisatud üksusena rakenduse Finance malli struktuuri.</span><span class="sxs-lookup"><span data-stu-id="14338-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="14338-158">[![Äridokumentide halduse tööruumi kasutamine äridokumendi mallile pildi lisamiseks](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="14338-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="14338-159">Seotud lingid</span><span class="sxs-lookup"><span data-stu-id="14338-159">Related links</span></span>

[<span data-ttu-id="14338-160">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="14338-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="14338-161">Äridokumentide halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="14338-161">Business document management overview</span></span>](er-business-document-management.md)
