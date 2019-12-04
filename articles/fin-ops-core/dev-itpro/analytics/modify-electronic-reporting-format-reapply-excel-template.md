---
title: Elektroonilise aruandluse vormingute muutmine Exceli malle uuesti rakendades
description: Teemas selgitatakse, kuidas muuta ettevõtte dokumentide loomiseks kasutatava elektroonilise aruandluse (ER) vormingut, rakendades muudetud Exceli malli uuesti.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
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
ms.openlocfilehash: 7381f198bef0e5f0401d4c39e085cf603aefb766
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185309"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="da16b-103">Elektroonilise aruandluse vormingute muutmine Exceli malle uuesti rakendades</span><span class="sxs-lookup"><span data-stu-id="da16b-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da16b-104">Elektroonilise aruandluse (ER) tööriista kasutatakse elektroonilises vormingus äridokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="da16b-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="da16b-105">Ettevõtte dokumendi loomiseks tuleb luua ER-i vorming ja seejärel kasutada ER-i kujundajat äridokumendi paigutuse määratlemiseks ja sellesse kaasatavate andmete määramiseks.</span><span class="sxs-lookup"><span data-stu-id="da16b-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="da16b-106">Seejärel saate käivitada ER-i vormingu äridokumendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="da16b-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="da16b-107">ER-i tööriist võimaldab luua äridokumente Microsoft Exceli failidena.</span><span class="sxs-lookup"><span data-stu-id="da16b-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="da16b-108">Saate kasutada Exceli dokumenti nende dokumentide mallina.</span><span class="sxs-lookup"><span data-stu-id="da16b-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="da16b-109">ER-i kujundajas dokumendi paigutuse määratlemiseks võite importida mallina kasutatava Exceli dokumendi sisu määratletud ER-i vormingusse.</span><span class="sxs-lookup"><span data-stu-id="da16b-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="da16b-110">Üksikasjaliku teabe saamiseks ja stsenaariumi harjutamiseks käivitage tegevusjuhis **Elektrooniline aruandlus. Konfiguratsioon OPENXML-vormingus aruannete loomiseks** (äriprotsessi 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677) osa).</span><span class="sxs-lookup"><span data-stu-id="da16b-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="da16b-111">Kui muudate äridokumendi mallina kasutatavat Exceli dokumenti, võimaldab uus ER-i funktsioon värskendatud malli uuesti ER-i vormingule rakendada.</span><span class="sxs-lookup"><span data-stu-id="da16b-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="da16b-112">Seejärel värskendatakse ER-i vormingut, et see järgiks uuendatud malli.</span><span class="sxs-lookup"><span data-stu-id="da16b-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="da16b-113">Selle funktsiooni kohta lisateabe saamiseks käivitage tegevuse juhis **Elektroonilise aruandluse vormingu muutmine Exceli malli uuesti rakendades** (7.5.5.3 omandada/arendamise see/elektroonilist komponentide (10683) äriprotsessi osa).</span><span class="sxs-lookup"><span data-stu-id="da16b-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="da16b-114">Tegevuse juhise värskendatud malli importimise etapis kasutage mallina maksearuande Exceli faili SampleVendPaymWsReport2 muudetud malli.</span><span class="sxs-lookup"><span data-stu-id="da16b-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>