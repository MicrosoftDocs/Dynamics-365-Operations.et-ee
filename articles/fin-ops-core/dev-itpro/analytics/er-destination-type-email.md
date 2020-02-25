---
title: ER-i sihtkoha tüübi e-post
description: Sellest teemast leiate teatevt, kuidas konfigureerida e-post sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019726"
---
# <span data-ttu-id="2f1b8-103"><a name="EmailDestinationType">Meili sihtkoht</a></span><span class="sxs-lookup"><span data-stu-id="2f1b8-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f1b8-104">Saate konfigureerida faili sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="2f1b8-105">Sihtkoha sätte põhjal tarnitakse loodud dokument e-kirja manusena.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="2f1b8-106">Määrake valiku **Lubatud** väärtuseks **Jah** väljundfaili saatmiseks meiliga.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="2f1b8-107">Kui see valik on lubatud, saate määrata meili adressaadid ning redigeerida meilisõnumi teemat ja kehateksti.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="2f1b8-108">Saate seadistada meilide teema ja kehateksti jaoks püsiteksti või kasutada meilitekstide loomiseks elektroonilise aruandluse [valemeid](er-formula-language.md), et dünaamiliselt luua e-kirja tekste.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="2f1b8-109">Elektroonilise aruandluse meiliaadresside konfigureerimiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="2f1b8-110">Konfiguratsiooni saab lõpule viia samamoodi, nagu prindihalduse funktsioon seda lõpule viib, või saate meiliaadressi lahendada, kasutades viitena ER konfiguratsioonile valemi kaudu.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="2f1b8-111">[![Meili sihtkoha lubamine](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="2f1b8-112">Meiliaadressi tüübid</span><span class="sxs-lookup"><span data-stu-id="2f1b8-112">Email address types</span></span>

<span data-ttu-id="2f1b8-113">Kui klõpsate valikut **Redigeeri** välja **Saaja** või **Koopia** puhul, kuvatakse dialoogiboks **Meili saaja**.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="2f1b8-114">Seejärel saate valida kasutatava meiliaadressi tüübi.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="2f1b8-115">**Konfiguratsiooni e-posti** ja **Prindihalduse** e-posti tüübid on praegu toetatud.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="2f1b8-116">[![Meilitüübi valimine](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="2f1b8-117">Prindihaldus</span><span class="sxs-lookup"><span data-stu-id="2f1b8-117">Print management</span></span>

<span data-ttu-id="2f1b8-118">Kui valite meilitüübi **Prindihaldus**, saate sisestada väljale **Saaja** fikseeritud meiliaadressid.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="2f1b8-119">[![Fikseeritud e-posti aadresside konfigureerimine](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="2f1b8-120">Fikseerimata meiliaadresside kasutamiseks tuleb valida failisihtkohaks meiliallika tüüp.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="2f1b8-121">Toetatakse järgmisi väärtusi: **Klient**, **Hankija**, **Potentsiaalne klient**, **Kontakt**, **Konkurent**, **Töötaja**, **Kandidaat**, **Potentsiaalne hankija** ja **Keelatud hankija**.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="2f1b8-122">Pärast meiliallika tüübi valimist avage välja **Meiliallika konto** kõrval oleva nupu abil vorm **Valemi kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="2f1b8-123">Saate kasutada seda vormi, et lisada valem, mis tagastab käitusaja, valitud allika tüübi **osapoole konto** töödeldud dokumendilt e-posti sihtkohta.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="2f1b8-124">[![E-posti allika konto konfigureerimine](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="2f1b8-125">Valemid on ER-i konfiguratsiooni põhised.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="2f1b8-126">Sisestage väljale **Valem** dokumendipõhine viide kliendi või hankija osapoole tüübile.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="2f1b8-127">Tippimise asemel võite otsida üles andmeallika sõlme, mis tähistab kliendi või hankija kontot, ja klõpsata siis valemi värskendamiseks nuppu **Lisa andmeallikas**.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="2f1b8-128">Näiteks kui kasutate **ISO 20022 kreeditülekande** konfiguratsiooni, tähistab hankija kontot sõlm `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="2f1b8-129">Kui sisestate stringi väärtuse, näiteks `"DE-001"`ja salvestate valemi, saadetakse meilisõnum hankija kontaktisikule, **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="2f1b8-130">[![Valemikoostaja leht](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="2f1b8-131">[![E-posti allika konto konfigureerimine](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="2f1b8-132">Konfigureerimismeil</span><span class="sxs-lookup"><span data-stu-id="2f1b8-132">Configuration email</span></span>

<span data-ttu-id="2f1b8-133">Kasutage seda meilitüüpi, kui kasutataval konfiguratsioonil on andmeallikates sõlm, mis tagastab **meiliaadressi**.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="2f1b8-134">Õigesti vormindatud meiliaadressi saamiseks saate kasutada valemikujundajas sisalduvaid andmeallikaid ja funktsioone.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="2f1b8-135">Näiteks kui kasutate **ISO 20022 kreeditülekande** konfiguratsiooni, tähistab hankija konto kontaktisiku meiliaadressi sõlm `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="2f1b8-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="2f1b8-136">[![E-posti allika aadressi konfigureerimine](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f1b8-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2f1b8-137">Additional resources</span></span>

- [<span data-ttu-id="2f1b8-138">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="2f1b8-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2f1b8-139">Elektroonilise aruandluse (ER) sihtkohad</span><span class="sxs-lookup"><span data-stu-id="2f1b8-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="2f1b8-140">Valemikoostaja elektroonilises aruandluses (ER)</span><span class="sxs-lookup"><span data-stu-id="2f1b8-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
