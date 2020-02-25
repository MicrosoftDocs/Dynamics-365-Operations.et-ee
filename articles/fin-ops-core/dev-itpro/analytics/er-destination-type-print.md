---
title: ER-i sihtkoha tüübi printer
description: Sellest teemast leiate teatevt, kuidas konfigureerida printerit sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks kas PDFi või Microsoft Office vormingus (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
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
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019727"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="db4ca-103">Printeri sihtkoht</span><span class="sxs-lookup"><span data-stu-id="db4ca-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db4ca-104">Saate loodud dokumendi otse printimiseks otse võrguprinterisse saata.</span><span class="sxs-lookup"><span data-stu-id="db4ca-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="db4ca-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="db4ca-105">Prerequisites</span></span>

<span data-ttu-id="db4ca-106">Enne alustamist peate installima ja konfigureerima dokumendi marsruudi agendi ning seejärel registreerima võrgu printerid.</span><span class="sxs-lookup"><span data-stu-id="db4ca-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="db4ca-107">Lisateavet saate teemast [Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="db4ca-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="db4ca-108">Printeri sihtkoha kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="db4ca-108">Make the Printer destination available</span></span>

<span data-ttu-id="db4ca-109">Selleks, et **printeri** sihtkoht oleks saadaval Microsofti Dynamics 365 Finance praeguses eksemplaris, minge **Funktsioonide halduse** tööruumi ja lülitage järgmised funktsioonid sisse selles järjekorras:</span><span class="sxs-lookup"><span data-stu-id="db4ca-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="db4ca-110">Teisenda elektroonilise aruandluse väljaminevad dokumendid Microsoft Office'i vormingutest PDF-iks</span><span class="sxs-lookup"><span data-stu-id="db4ca-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="db4ca-111">Dokumendi marsruudivaliku agent väljaminevate dokumentide elektroonilise aruandluse sihtkohana</span><span class="sxs-lookup"><span data-stu-id="db4ca-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="db4ca-112">[![ER printeri sihtkoha funktsiooni sisselülitamine funktsioonide halduses](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="db4ca-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="db4ca-113">Kohaldatavus</span><span class="sxs-lookup"><span data-stu-id="db4ca-113">Applicability</span></span>

<span data-ttu-id="db4ca-114">**Printeri** sihtkoha saab konfigureerida ainult faili komponentide jaoks, mida kasutatakse väljundi loomiseks kas prinditavas PDF-vormingus (PDF-i liitmine või PDF-vormingu elemendid) või Microsoft Office Excel/Word vormingus.</span><span class="sxs-lookup"><span data-stu-id="db4ca-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="db4ca-115">Kui väljund luuakse PDF-vormingus, saadetakse see printerisse.</span><span class="sxs-lookup"><span data-stu-id="db4ca-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="db4ca-116">Kui väljund luuakse Microsoft Office vormingus, teisendatakse see automaatselt PDF-vormingusse ja seejärel saadetakse printerisse.</span><span class="sxs-lookup"><span data-stu-id="db4ca-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="db4ca-117">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="db4ca-117">Limitations</span></span>

<span data-ttu-id="db4ca-118">See funktsioon on eelvaate funktsioon ja seda kasutatakse tingimustes, mida on kirjeldatud teemas [Microsoft Dynamics 365 eelvaadete kasutamise täiendavad tingimused](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="db4ca-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="db4ca-119">**Printeri** sihtkohta rakendatakse ainult pilve juurutamiseks.</span><span class="sxs-lookup"><span data-stu-id="db4ca-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="db4ca-120">Printimise sihtkoha kasutamine</span><span class="sxs-lookup"><span data-stu-id="db4ca-120">Use the Printer destination</span></span>

1. <span data-ttu-id="db4ca-121">Seadke **Lubatud** suvand väärtusele **Jah**, et saata loodud dokument printerisse.</span><span class="sxs-lookup"><span data-stu-id="db4ca-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="db4ca-122">Valige väljal **Printeri nimi** vajalik võrguprinter.</span><span class="sxs-lookup"><span data-stu-id="db4ca-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="db4ca-123">Seadke suvand **Kas soovite salvestada printimise arhiivi?** väärtusele **Jah**, et salvestada loodud väljund printimise arhiivi, nii et see on edasiseks printimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="db4ca-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="db4ca-124">Arhiveeritud väljundi juurde pääsemiseks hiljem avage **Organisatsiooni haldus** \> **Päringud ja aruanded** \> **Aruannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="db4ca-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="db4ca-125">[![Printimise sihtkoha kasutamine](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="db4ca-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="db4ca-126">Suvand **Teisendamine PDF-iks** ei pea **Printeri** sihtkoha konfigureerimisel olema sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="db4ca-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="db4ca-127">PDF-i teisendamine printimiseks toimub isegi siis, kui suvand on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="db4ca-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db4ca-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="db4ca-128">Additional resources</span></span>

- [<span data-ttu-id="db4ca-129">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="db4ca-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="db4ca-130">Elektroonilise aruandluse (ER) sihtkohad</span><span class="sxs-lookup"><span data-stu-id="db4ca-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
