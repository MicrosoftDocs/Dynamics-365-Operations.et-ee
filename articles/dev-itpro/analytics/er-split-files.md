---
title: "Loodud XML-failide tükeldamine failimahu ja sisukoguse alusel"
description: "See teema annab teavet loodud failide tükeldamise kohta failimahu ja sisuüksuste koguse alusel."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 8c3899d5c6602b3afe13b447b40f0b4dcc701448
ms.contentlocale: et-ee
ms.lasthandoff: 08/13/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="d4efe-103">Loodud XML-failide tükeldamine failimahu ja sisukoguse alusel</span><span class="sxs-lookup"><span data-stu-id="d4efe-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d4efe-104">Saate kujundada elektroonilise aruandluse vormingud looma väljaminevaid dokumente XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="d4efe-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="d4efe-105">Mõnikord saab neid dokumente aktseptida ainult siis, kui need vastavad teatud kriteeriumidele, nagu maksimaalne failimaht või mõningate XML-sõlmede maksimaalne arv.</span><span class="sxs-lookup"><span data-stu-id="d4efe-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="d4efe-106">Saate kujundada elektroonilise aruandluse vormingud looma elektroonilisi dokumente, mis täidavad nende dokumentide saajate määratud nõudeid.</span><span class="sxs-lookup"><span data-stu-id="d4efe-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="d4efe-107">Vorminguelemendi FILE puhul saate määratleda failimahu piirangu elektroonilise aruandluse avaldisena.</span><span class="sxs-lookup"><span data-stu-id="d4efe-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="d4efe-108">Kui elektroonilise aruandluse aruande loomisel ületatakse määratud piirang, lõpetab elektrooniline aruandlus praeguse faili loomise ja liigub edasi järgmise faili loomise juurde.</span><span class="sxs-lookup"><span data-stu-id="d4efe-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="d4efe-109">Vormingu XML ELEMENT puhul saate määratleda elementide arvu piirangu elektroonilise aruandluse avaldisena.</span><span class="sxs-lookup"><span data-stu-id="d4efe-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="d4efe-110">Kui elektroonilise aruandluse aruande käitamisel ületab XML-sõlmede arv loodud failis selle määratud piirangu, lõpetab elektrooniline aruandlus praeguse faili loomise ja liigub edasi järgmise faili loomise juurde.</span><span class="sxs-lookup"><span data-stu-id="d4efe-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="d4efe-111">Mis tahes vorminguelemendi XML SEQUENCE puhul saate määratleda tütarelementide arvu piirangu elektroonilise aruandluse avaldisena.</span><span class="sxs-lookup"><span data-stu-id="d4efe-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="d4efe-112">Kui elektroonilise aruandluse aruande käitamisel ületab vorminguelemendi pesastatud XML-sõlmede arv loodud failis selle määratud piirangu, lõpetab elektrooniline aruandlus praeguse faili loomise ja liigub edasi järgmise faili loomise juurde.</span><span class="sxs-lookup"><span data-stu-id="d4efe-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="d4efe-113">Saate märkida mis tahes vorminguelemendi XML ELEMENT mittemurtavaks.</span><span class="sxs-lookup"><span data-stu-id="d4efe-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="d4efe-114">Sel moel saate hoida XML-sõlmede pesastatud üksused, mis on loodud vorminguelemendi all, ühes loodud failis.</span><span class="sxs-lookup"><span data-stu-id="d4efe-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="d4efe-115">Peale vorminguelementide XML ELEMENT ja XML SEQUENCE kasutamise XML-sõlmede lisamiseks loodud faili saate kasutada vorminguelementi RAW XML.</span><span class="sxs-lookup"><span data-stu-id="d4efe-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="d4efe-116">Vorminguelemendi RAW XML abil lisatud sõlmi ei võeta siiski arvesse sõlmede arvu arvutamisel, et hinnata elementide arvu piiranguid.</span><span class="sxs-lookup"><span data-stu-id="d4efe-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="d4efe-117">Kui olete konfigureerinud failisihtkohad vorminguelemendile FILE, mis on konfigureeritud loodud väljundi tükeldamiseks alati, kui konkreetne piirang ületatakse, saadetakse iga loodud väljundi tükk konfigureeritud faili sihtkohta eraldi failina.</span><span class="sxs-lookup"><span data-stu-id="d4efe-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="d4efe-118">Väljundi tükeldamisel loodud failidele kordumatu nime andmiseks peate konfigureerima vorminguelemendile FILE elektroonilise aruandluse avaldise.</span><span class="sxs-lookup"><span data-stu-id="d4efe-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="d4efe-119">Kui kaasate elektroonilise aruandluse andmeallika tüübiga NUMBER SEQUENCE, suureneb numbriseeria iga tükeldatud väljundi tüki puhul.</span><span class="sxs-lookup"><span data-stu-id="d4efe-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="d4efe-120">Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusejuhist **Elektrooniline aruandlus: XML-failide tükeldamine failimahu või sisuüksuste koguse põhjal**, mis on osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** ja mille saab alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="d4efe-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="d4efe-121">See tegevusejuhis viib teid läbi elektroonilise aruandluse vormingu konfigureerimise protsessi loodud failide tükeldamiseks failimahu ja sisuüksuste koguse piirangute põhjal.</span><span class="sxs-lookup"><span data-stu-id="d4efe-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="d4efe-122">Tegevusejuhise lõpuleviimiseks peate alla laadima järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="d4efe-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="d4efe-123">Elektroonilise aruandluse mudeli konfiguratsioon – XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="d4efe-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="d4efe-124">Elektroonilise aruandluse vormingu konfiguratsioon – XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="d4efe-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="d4efe-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d4efe-125">Additional resources</span></span>
[<span data-ttu-id="d4efe-126">Elektroonilise aruandluse sihtkohad</span><span class="sxs-lookup"><span data-stu-id="d4efe-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="d4efe-127">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="d4efe-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

