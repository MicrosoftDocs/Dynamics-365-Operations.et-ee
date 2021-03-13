---
title: ER-i konfiguratsioonide kujundamine loodud failides baidijärjestuse märkide alistamiseks
description: Selles teemas selgitatakse, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut, et luua baidijärjestuse märke (BOM) alistavaid aruandeid.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060815"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="f4722-103">ER-i konfiguratsioonide kujundamine loodud failides baidijärjestuse märkide alistamiseks</span><span class="sxs-lookup"><span data-stu-id="f4722-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4722-104">Saate kujundada [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [lahendused](er-quick-start1-new-solution.md) looma väljaminevaid dokumente.</span><span class="sxs-lookup"><span data-stu-id="f4722-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="f4722-105">Dokumentide teksti või XML-failidena loomiseks peab lahendus hõlmama ER-i [konfiguratsiooni](general-electronic-reporting.md#Configuration), mis sisaldab [ER-vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponenti.</span><span class="sxs-lookup"><span data-stu-id="f4722-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="f4722-106">Loodud failides märgikomplekti esindava [märkide kodeerimise](https://docs.microsoft.com/windows/win32/intl/character-sets) määratlemiseks peab ER-vorming sisaldama vormingu elementi **Üldine\\Fail**.</span><span class="sxs-lookup"><span data-stu-id="f4722-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="f4722-107">ER-vormingu komponendi konfigureerimiseks avage ER-i vormingu kujundajas ER-i konfiguratsiooni [mustandi](general-electronic-reporting.md#component-versioning) versioon ja lisage element **Üldine\\Fail**.</span><span class="sxs-lookup"><span data-stu-id="f4722-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="f4722-108">Määrake väljal **Kodeering** väljaminevate failide kodeering, mis luuakse käitusajal, kasutades seda komponenti.</span><span class="sxs-lookup"><span data-stu-id="f4722-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="f4722-109">Kui vorming sisaldab valet kodeerimisnime, ilmneb vormingu sätete muudatuste salvestamisel tõrge.</span><span class="sxs-lookup"><span data-stu-id="f4722-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Juurelemendi lisamine vormingu kujundaja lehel](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="f4722-111">Kui määrate kodeeringuks **UTF-8**, **UTF-16** või **UTF-32**, muutub valik **Alista BOM-i tärgid** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="f4722-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="f4722-112">Määrake see suvand valikule **Jah**, et alistada sissetulevates failides [baidijärjestuse märgid (BOM)](https://docs.microsoft.com/globalization/encoding/byte-order-mark), mis luuakse käitusajal, kui redigeeritav ER-vorming töötab.</span><span class="sxs-lookup"><span data-stu-id="f4722-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="f4722-113">Kui jätate välja **Kodeering** tühjaks, kasutatakse vaikimisi kodeerimist **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="f4722-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Vormingu kujundaja lehel BOM-i tärkide alistamise suvandi häälestamine](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="f4722-115">Käitusajal funktsioonide läbivaatamiseks läbige vastav protseduur.</span><span class="sxs-lookup"><span data-stu-id="f4722-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="f4722-116">Näiteks viige lõpule sammud teemas [Elektroonilise aruandluse vormingus XML-elementide käivitamise edasilükkamine](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="f4722-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="f4722-117">Kui olete läbinud selle teema jaotise [Vormingu muutmine nii, et arvutus põhineb loodud väljundil](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) sammud, järgige järgmisi lisajuhiseid.</span><span class="sxs-lookup"><span data-stu-id="f4722-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="f4722-118">Määrake UTF-i kodeering.</span><span class="sxs-lookup"><span data-stu-id="f4722-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="f4722-119">Valige element **Aruanne** tüübis **Üldine\\Fail**.</span><span class="sxs-lookup"><span data-stu-id="f4722-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="f4722-120">Väljal **Kodeerimine** määrake kodeering **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="f4722-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="f4722-121">Looge XML-fail, mis sisaldab BOM-i tärki.</span><span class="sxs-lookup"><span data-stu-id="f4722-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="f4722-122">Määrake suvand **Alista BOM-i tärgid** valikule **Ei**, et kaasata BOM-i tärgid loodud XML-failidesse.</span><span class="sxs-lookup"><span data-stu-id="f4722-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="f4722-123">Viige lõpule juhised jaotises [Lükka edasi kokkuvõtte XML-elemendi käivitamine nii, et arvutatud kogusummat kasutatakse](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) teemas [Elektroonilise aruandluse vormingus XML-elementide käivitamise edasilükkamine](er-defer-xml-element.md) ja salvestage loodud fail kujul **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="f4722-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="f4722-124">Looge XML-fail, mis ei sisalda BOM-i tärki.</span><span class="sxs-lookup"><span data-stu-id="f4722-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="f4722-125">Määrake suvand **Alista BOM-i tärgid** valikule **Jah**, et alistada BOM-i tärgid loodud XML-failides.</span><span class="sxs-lookup"><span data-stu-id="f4722-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="f4722-126">Viige lõpule juhised jaotises [Lükka edasi kokkuvõtte XML-elemendi käivitamine nii, et arvutatud kogusummat kasutatakse](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) teemas [Elektroonilise aruandluse vormingus XML-elementide käivitamise edasilükkamine](er-defer-xml-element.md) ja salvestage loodud fail kujul **SampleXmlReport(1).xml**.</span><span class="sxs-lookup"><span data-stu-id="f4722-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="f4722-127">Võrrelge failide võrdlemise utiliidis loodud faile.</span><span class="sxs-lookup"><span data-stu-id="f4722-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="f4722-128">Esimene erinevus, mida te märkate, on faili päis.</span><span class="sxs-lookup"><span data-stu-id="f4722-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="f4722-129">SampleXmlReport.xml file sisaldab BOM-i tärki, samas kui fail SampleXmlReport (1).xml ei sisalda.</span><span class="sxs-lookup"><span data-stu-id="f4722-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Loodud failide võrdlemine faili võrdlemise utiliiti kasutades](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="f4722-131">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f4722-131">See also</span></span>

- [<span data-ttu-id="f4722-132">Elektroonilise aruandluse vormingus XML-elementide käivitamise edasilükkamine</span><span class="sxs-lookup"><span data-stu-id="f4722-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)
