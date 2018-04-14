---
title: Elektroonilise aruandluse vormingu muutmine Microsoft Exceli malli uuesti rakendades
description: "Teemas selgitatakse, kuidas muuta ettevõtte dokumentide loomiseks kasutatava elektroonilise aruandluse (ER) vormingut, rakendades muudetud Exceli malli uuesti."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: eb0a37acebb61c7f4f06724bf0234211072f1e98
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="f0738-103">Elektroonilise aruandluse vormingu muutmine Microsoft Exceli malli uuesti rakendades</span><span class="sxs-lookup"><span data-stu-id="f0738-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f0738-104">Elektroonilise aruandluse (ER) tööriista kasutatakse elektroonilises vormingus äridokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f0738-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="f0738-105">Ettevõtte dokumendi loomiseks tuleb luua ER-i vorming ja seejärel kasutada ER-i kujundajat äridokumendi paigutuse määratlemiseks ja sellesse kaasatavate andmete määramiseks.</span><span class="sxs-lookup"><span data-stu-id="f0738-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="f0738-106">Seejärel saate käivitada ER-i vormingu äridokumendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f0738-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="f0738-107">ER-i tööriist võimaldab luua äridokumente Microsoft Exceli failidena.</span><span class="sxs-lookup"><span data-stu-id="f0738-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="f0738-108">Saate kasutada Exceli dokumenti nende dokumentide mallina.</span><span class="sxs-lookup"><span data-stu-id="f0738-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="f0738-109">ER-i kujundajas dokumendi paigutuse määratlemiseks võite importida mallina kasutatava Exceli dokumendi sisu määratletud ER-i vormingusse.</span><span class="sxs-lookup"><span data-stu-id="f0738-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="f0738-110">Üksikasjaliku teabe saamiseks ja stsenaariumi harjutamiseks käivitage tegevusjuhis **Elektrooniline aruandlus. Konfiguratsioon OPENXML-vormingus aruannete loomiseks** (äriprotsessi 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677) osa).</span><span class="sxs-lookup"><span data-stu-id="f0738-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="f0738-111">Kui muudate äridokumendi mallina kasutatavat Exceli dokumenti, võimaldab uus ER-i funktsioon värskendatud malli uuesti ER-i vormingule rakendada.</span><span class="sxs-lookup"><span data-stu-id="f0738-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="f0738-112">Seejärel värskendatakse ER-i vormingut, et see järgiks uuendatud malli.</span><span class="sxs-lookup"><span data-stu-id="f0738-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="f0738-113">Selle funktsiooni kohta lisateabe saamiseks käivitage tegevuse juhis **Elektroonilise aruandluse vormingu muutmine Microsoft Exceli malli uuesti rakendades** (7.5.5.3 omandada/arendamise see/elektroonilist komponentide (10683) äriprotsessi osa).</span><span class="sxs-lookup"><span data-stu-id="f0738-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="f0738-114">Tegevuse juhise värskendatud malli importimise etapis kasutage mallina maksearuande Exceli faili SampleVendPaymWsReport2 muudetud malli.</span><span class="sxs-lookup"><span data-stu-id="f0738-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

