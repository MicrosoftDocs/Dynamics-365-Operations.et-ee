---
title: ER-i sihtkoha tüübi printer
description: Selles teemas selgitatakse, kuidas konfigureerida printeri sihtkohta iga elektroonilise aruandluse (ER) vormingu komponendi FOLDER või FILE jaoks.
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 83081f8c17a903cd447a34596df2e61ebda0cafc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753428"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="59da9-103">Printeri sihtkoht</span><span class="sxs-lookup"><span data-stu-id="59da9-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59da9-104">Saate loodud dokumendi otse printimiseks otse võrguprinterisse saata.</span><span class="sxs-lookup"><span data-stu-id="59da9-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59da9-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="59da9-105">Prerequisites</span></span>

<span data-ttu-id="59da9-106">Enne alustamist peate installima ja konfigureerima dokumendi marsruudi agendi ning seejärel registreerima võrgu printerid.</span><span class="sxs-lookup"><span data-stu-id="59da9-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="59da9-107">Lisateavet saate teemast [Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="59da9-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="59da9-108">Printeri sihtkoha kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="59da9-108">Make the Printer destination available</span></span>

<span data-ttu-id="59da9-109">Selleks, et **printeri** sihtkoht oleks saadaval Microsofti Dynamics 365 Finance praeguses eksemplaris, minge **Funktsioonide halduse** tööruumi ja lülitage järgmised funktsioonid sisse selles järjekorras:</span><span class="sxs-lookup"><span data-stu-id="59da9-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="59da9-110">Teisenda elektroonilise aruandluse väljaminevad dokumendid Microsoft Office'i vormingutest PDF-iks</span><span class="sxs-lookup"><span data-stu-id="59da9-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="59da9-111">Dokumendi marsruudivaliku agent väljaminevate dokumentide elektroonilise aruandluse sihtkohana</span><span class="sxs-lookup"><span data-stu-id="59da9-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="59da9-112">[![ER printeri sihtkoha funktsiooni sisselülitamine funktsioonide halduses](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="59da9-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="59da9-113">Kohaldatavus</span><span class="sxs-lookup"><span data-stu-id="59da9-113">Applicability</span></span>

<span data-ttu-id="59da9-114">**Printeri** sihtkoha saab konfigureerida ainult faili komponentide jaoks, mida kasutatakse väljundi loomiseks kas prinditavas PDF-vormingus (PDF-i liitmine või PDF-vormingu elemendid) või Microsoft Office Excel/Word vormingus.</span><span class="sxs-lookup"><span data-stu-id="59da9-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="59da9-115">Kui väljund luuakse PDF-vormingus, saadetakse see printerisse.</span><span class="sxs-lookup"><span data-stu-id="59da9-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="59da9-116">Kui väljund luuakse Microsoft Office vormingus, teisendatakse see automaatselt PDF-vormingusse ja seejärel saadetakse printerisse.</span><span class="sxs-lookup"><span data-stu-id="59da9-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="59da9-117">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="59da9-117">Limitations</span></span>

<span data-ttu-id="59da9-118">**Printeri** sihtkohta rakendatakse ainult pilve juurutamiseks.</span><span class="sxs-lookup"><span data-stu-id="59da9-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="59da9-119">Printimise sihtkoha kasutamine</span><span class="sxs-lookup"><span data-stu-id="59da9-119">Use the Printer destination</span></span>

1. <span data-ttu-id="59da9-120">Seadke **Lubatud** suvand väärtusele **Jah**, et saata loodud dokument printerisse.</span><span class="sxs-lookup"><span data-stu-id="59da9-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="59da9-121">Valige väljal **Printeri nimi** vajalik võrguprinter.</span><span class="sxs-lookup"><span data-stu-id="59da9-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="59da9-122">Seadke suvand **Kas soovite salvestada printimise arhiivi?** väärtusele **Jah**, et salvestada loodud väljund printimise arhiivi, nii et see on edasiseks printimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="59da9-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="59da9-123">Arhiveeritud väljundi juurde pääsemiseks hiljem avage **Organisatsiooni haldus** \> **Päringud ja aruanded** \> **Aruannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="59da9-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="59da9-124">[![Printimise sihtkoha kasutamine](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="59da9-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="59da9-125">Suvand **Teisendamine PDF-iks** ei pea **Printeri** sihtkoha konfigureerimisel olema sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="59da9-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="59da9-126">PDF-i teisendamine printimiseks toimub isegi siis, kui suvand on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="59da9-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="59da9-127">Kindla [lehe paigutuse](electronic-reporting-destinations.md#SelectPdfPageOrientation) kasutamiseks väljamineva Exceli vormingus dokumendi printimiseks, peate sisse lülitama suvandi **Teisenda PDF-iks**.</span><span class="sxs-lookup"><span data-stu-id="59da9-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="59da9-128">Kui määrate suvandi **Teisenda PDF-iks** väärtuseks **Jah**, on saadaval väli **Lehe paigutus**.</span><span class="sxs-lookup"><span data-stu-id="59da9-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="59da9-129">Väljal **Lehe paigutus** saate valida lehe paigutuse.</span><span class="sxs-lookup"><span data-stu-id="59da9-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59da9-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="59da9-130">Additional resources</span></span>

- [<span data-ttu-id="59da9-131">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="59da9-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="59da9-132">Elektroonilise aruandluse (ER) sihtkohad</span><span class="sxs-lookup"><span data-stu-id="59da9-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
