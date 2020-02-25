---
title: Uus dokumendi kasutajaliides äridokumendi halduses
description: See teema annab teavet selle kohta, kuidas kasutada uut dokumendi kasutajaliidest (UI) elektroonilise aruandluse (ER) raamistiku äridokumendi halduse funktsioonis.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4acde9703c721ab7c20d1603299a10dda91b23c4
ms.sourcegitcommit: b8f8ccab2cd9d848e5ecd71caaf0a63237e2236b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2020
ms.locfileid: "2957059"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="b80d6-103">Uus dokumendi kasutajaliides äridokumendi halduses</span><span class="sxs-lookup"><span data-stu-id="b80d6-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b80d6-104">Äridokumendi haldus võimaldab ärikasutajatel redigeerida äridokumendi malle teenuse Microsoft Office 365 või vastava Microsoft Office töölauarakendusega.</span><span class="sxs-lookup"><span data-stu-id="b80d6-104">Business document management lets business users edit business document templates by using a Microsoft Office 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="b80d6-105">Muudatused võivad hõlmata kujunduse muudatusi või uusi juurutusi, või kasutajad võivad lisada kohatäited, et kaasata täiendavaid andmeid, ilma et peaksite lähtekoodi muutma.</span><span class="sxs-lookup"><span data-stu-id="b80d6-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="b80d6-106">Lisateavet äridokumentide haldusega töötamise kohta vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b80d6-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="b80d6-107">Uus dokumendi kasutajaliides (UI) on selgem ja seda on mugavam kasutada.</span><span class="sxs-lookup"><span data-stu-id="b80d6-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="b80d6-108">**Äridokumendi** ala näitab ainult malle, mis on saadaval praegusele pakkujale.</span><span class="sxs-lookup"><span data-stu-id="b80d6-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="b80d6-109">**Uue dokumendi** nupp võimaldab kasutajatel luua ja redigeerida malli elektroonilise aruandluse (ER) vormingu konfiguratsioonis, mida pakub teine pakkuja.</span><span class="sxs-lookup"><span data-stu-id="b80d6-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="b80d6-110">Selle teema näites on pakkuja Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b80d6-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="b80d6-111">Tee uus dokumendi kasutajaliides äridokumentide halduses kättesaadavaks</span><span class="sxs-lookup"><span data-stu-id="b80d6-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="b80d6-112">Et alustada uue dokumendi kasutajaliidese kasutamist äridokumentide halduses peate **Office'i sarnase kasutajaliidese kogemuse äridokumendi halduses** **Funktsiooni halduse** tööruumis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="b80d6-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="b80d6-113">Kõigi juriidiliste isikute jaoks selle funktsiooni sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b80d6-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="b80d6-114">Valige **Fuktsioonide halduse** tööruumis vahekaardil **Uus** loendis funktsioon **Office'i sarnase kasutajaliidese kogemus äridokumendi haldamises**.</span><span class="sxs-lookup"><span data-stu-id="b80d6-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="b80d6-115">Valitud funktsiooni lubamiseks valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="b80d6-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="b80d6-116">Uue funktsiooni kasutamiseks värskenda lehte.</span><span class="sxs-lookup"><span data-stu-id="b80d6-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="b80d6-117">Muutke teiste pakkujate malle</span><span class="sxs-lookup"><span data-stu-id="b80d6-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="b80d6-118">Valige **Äridokumentide halduse** tööruumis **Uus dokument**.</span><span class="sxs-lookup"><span data-stu-id="b80d6-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Äridokumentide halduse tööruum](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="b80d6-120">Dialoogiaknas valige mallina kasutatav dokument ja seejärel valige **Loo dokument**.</span><span class="sxs-lookup"><span data-stu-id="b80d6-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Äridokumentide dialoogiboks](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="b80d6-122">Muutke vajadusel pealkiri uue dialoogiboksi väljal **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="b80d6-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="b80d6-123">Pealkirja tekstiga nimetatakse ise tekkivat uut ER-vormingu seadistust.</span><span class="sxs-lookup"><span data-stu-id="b80d6-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="b80d6-124">Seda muudetavat malli sisaldava seadistuse (**Kliendi FTI aruande (GER) koopia**) mustandit ja ER-vormingu praeguse kasutaja puhul.</span><span class="sxs-lookup"><span data-stu-id="b80d6-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="b80d6-125">ER-vormingu põhiseadistuse muutmata algset malli kasutatakse selle ER-vormingu käivitamiseks kõikide kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="b80d6-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="b80d6-126">Muutke väljal **Nimi** isetekkiva muudetava malli esimese redaktsiooni nime.</span><span class="sxs-lookup"><span data-stu-id="b80d6-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="b80d6-127">Väljal **Kommentaar** värskendage isetekkiva muudetava malli redaktsiooni märkusi.</span><span class="sxs-lookup"><span data-stu-id="b80d6-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="b80d6-128">Muutmis alustamise kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b80d6-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dokumendi loomise dialoogiboks](./media/BDM_overview_new_template3.png)

<span data-ttu-id="b80d6-130">**Uue dokumendi** nuppu kasutatakse malli loomiseks ja redigeerimiseks elektroonilise aruandluse (ER) vormingu konfiguratsioonis, mida pakub teine pakkuja.</span><span class="sxs-lookup"><span data-stu-id="b80d6-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="b80d6-131">Selles näites on pakkuja Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b80d6-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="b80d6-132">Kui valite suvandi **Uus dokument**, saate vaadata kõiki praeguse ja teiste pakkujate omanduses olevaid malle.</span><span class="sxs-lookup"><span data-stu-id="b80d6-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="b80d6-133">Pärast malli valimist avatakse see redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b80d6-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="b80d6-134">Muudetud malli saab seejärel muuta uues ise loodavas ER-vormingus seadistusega.</span><span class="sxs-lookup"><span data-stu-id="b80d6-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="b80d6-135">Lisateavet vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b80d6-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>
