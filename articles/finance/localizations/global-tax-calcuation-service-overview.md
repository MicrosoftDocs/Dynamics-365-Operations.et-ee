---
title: Maksuarvutusteenus (Eelversioon)
description: Selles teemas selgitatakse maksuarvutusteenuse üldist ulatust ja funktsioone.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818220"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="9d327-103">Maksuarvutusteenus (Eelversioon)</span><span class="sxs-lookup"><span data-stu-id="9d327-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="9d327-104">Maksuarvestuse teenus on hyper-skaleeritav mitmetasandiline teenus, mis võimaldab global tax engine maksu määramise ja arvutamise protsessi automatiseerida ja seda lihtsustada.</span><span class="sxs-lookup"><span data-stu-id="9d327-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="9d327-105">Maksumootor on täielikult konfigureeritav.</span><span class="sxs-lookup"><span data-stu-id="9d327-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="9d327-106">Elemendid, mida saab konfigureerida, sisaldavad, kuid ei ole piiratud maksustatavate andmemudelite, maksukoodide, maksu kohaldatavusmaatriksi ja maksuarvutuse valemiga.</span><span class="sxs-lookup"><span data-stu-id="9d327-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="9d327-107">Maksumootor töötab teenuste Microsoft Azure põhiplatvormil ja pakub tänapäevasttehnoloogiat ja kõrgetasemelist skaleeritavust.</span><span class="sxs-lookup"><span data-stu-id="9d327-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="9d327-108">Maksuarvutuse teenus integreerub Dynamics 365 Finance ja Dynamics 365 Supply Chain Management-iga.</span><span class="sxs-lookup"><span data-stu-id="9d327-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9d327-109">Lõpuks integreerub see ka Dynamics 365 Project Operations Dynamics 365 Commerce ja teiste esimese ja kolmanda osapoole rakendustega.</span><span class="sxs-lookup"><span data-stu-id="9d327-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="9d327-110">Maksuarvestuse teenus on Microsoftipõhine maksumootor, mis pakub astmelisi skaleeritavust.</span><span class="sxs-lookup"><span data-stu-id="9d327-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="9d327-111">Saate teha järgmisi toiminguid:</span><span class="sxs-lookup"><span data-stu-id="9d327-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="9d327-112">Konfigureerige maksu arvutamise teenus regulatiivse konfiguratsiooniteenuse (RCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="9d327-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="9d327-113">RCS on elektroonilise aruandluse (ER) kujundaja täiustatud versioon ja saadaval eraldi teenusena.</span><span class="sxs-lookup"><span data-stu-id="9d327-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="9d327-114">Konfigureerige maksumaatriks maksukoodide ja -määrade automaatseks määramiseks.</span><span class="sxs-lookup"><span data-stu-id="9d327-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="9d327-115">Konfigureerige maksumaatriks maksu registreerimise number automaatseks määramiseks.</span><span class="sxs-lookup"><span data-stu-id="9d327-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="9d327-116">Konfigureerige maksuarvutuse kujundajat valemite ja tingimuste määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="9d327-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="9d327-117">Jagage maksu määramist ja arvutuslahendust juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="9d327-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="9d327-118">Maksuarvutusteenuse kasutamiseks installige maksuarvutuse teenuse lisandmoodul oma projektist Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9d327-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9d327-119">Seejärel lõpetage seadistus RCS-s ja lubage maksu arvutamise teenus finantside ja Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9d327-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="9d327-120">Lisateavet leiate teemast [Maksuteenusega alustamine](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="9d327-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="9d327-121">Kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="9d327-121">Availability</span></span>

<span data-ttu-id="9d327-122">Maksuarvutusteenus on avaliku eelvaateprogrammi kaudu saadaval ainult liivakasti keskkondades ja valitud klientide jaoks.</span><span class="sxs-lookup"><span data-stu-id="9d327-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="9d327-123">Lõpuks muutub see üldiselt kättesaadavaks kõigile klientidele ja tootmiskeskkondades.</span><span class="sxs-lookup"><span data-stu-id="9d327-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="9d327-124">Uued funktsioonid tarnitakse ka edaspidi maksuarvestuse teenuses.</span><span class="sxs-lookup"><span data-stu-id="9d327-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="9d327-125">Seetõttu kontrollige kindlasti kõige ajasemat dokumentatsiooni, et teada saada toetatud funktsioonide laovarudest ja ulatusest.</span><span class="sxs-lookup"><span data-stu-id="9d327-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="9d327-126">Maksu arvutamise teenus on juurutatud järgmistes Azure'i geograafilistes asukohtades.</span><span class="sxs-lookup"><span data-stu-id="9d327-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="9d327-127">See juurutatakse ka rohkematele Azure'i geograafilistele aseukohtades, sõltuvalt klientide vajadustest:</span><span class="sxs-lookup"><span data-stu-id="9d327-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="9d327-128">Ameerika Ühendriigid</span><span class="sxs-lookup"><span data-stu-id="9d327-128">United States</span></span>
- <span data-ttu-id="9d327-129">Euroopa</span><span class="sxs-lookup"><span data-stu-id="9d327-129">Europe</span></span>
- <span data-ttu-id="9d327-130">Prantsusmaa</span><span class="sxs-lookup"><span data-stu-id="9d327-130">France</span></span>
- <span data-ttu-id="9d327-131">Ühendkuningriik</span><span class="sxs-lookup"><span data-stu-id="9d327-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="9d327-132">Maksu arvutamise teenus ei toeta kohapealset juurutamist Dynamics 365-s.</span><span class="sxs-lookup"><span data-stu-id="9d327-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="9d327-133">Samuti ei toeta see varasemaid versioone, nt Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="9d327-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="9d327-134">Esiletõstetud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="9d327-134">Feature highlights</span></span>

- <span data-ttu-id="9d327-135">Konfigureerige maksumaatriks maksude automaatseks määramiseks ja arvutamiseks</span><span class="sxs-lookup"><span data-stu-id="9d327-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="9d327-136">Tugi mitme käibemaksu(VAT) registreerimisnumbritele</span><span class="sxs-lookup"><span data-stu-id="9d327-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="9d327-137">Üleviimistellimuse tugi maksu määramiseks ja arvutamiseks</span><span class="sxs-lookup"><span data-stu-id="9d327-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="9d327-138">Üleviimistellimuse tugi mitme käibemaksu registreerimisnumbri määramiseks</span><span class="sxs-lookup"><span data-stu-id="9d327-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="9d327-139">Toetatud kanded</span><span class="sxs-lookup"><span data-stu-id="9d327-139">Supported transactions</span></span>

<span data-ttu-id="9d327-140">Maksu arvutamise teenused võivad olla juriidiliste isikute ja kannete puhul võimaldatud.</span><span class="sxs-lookup"><span data-stu-id="9d327-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="9d327-141">Toetatud on järgmised kanded:</span><span class="sxs-lookup"><span data-stu-id="9d327-141">The following transactions are supported:</span></span>

- <span data-ttu-id="9d327-142">Müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="9d327-142">Sales process</span></span>

    - <span data-ttu-id="9d327-143">Müügipakkumine</span><span class="sxs-lookup"><span data-stu-id="9d327-143">Sales quotation</span></span>
    - <span data-ttu-id="9d327-144">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="9d327-144">Sales order</span></span>
    - <span data-ttu-id="9d327-145">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="9d327-145">Confirmation</span></span>
    - <span data-ttu-id="9d327-146">Komplekteerimisleht</span><span class="sxs-lookup"><span data-stu-id="9d327-146">Picking list</span></span>
    - <span data-ttu-id="9d327-147">Saateleht</span><span class="sxs-lookup"><span data-stu-id="9d327-147">Packing slip</span></span>
    - <span data-ttu-id="9d327-148">Müügiarve</span><span class="sxs-lookup"><span data-stu-id="9d327-148">Sales invoice</span></span>
    - <span data-ttu-id="9d327-149">Kreeditarve</span><span class="sxs-lookup"><span data-stu-id="9d327-149">Credit note</span></span>
    - <span data-ttu-id="9d327-150">Tagastustellimus</span><span class="sxs-lookup"><span data-stu-id="9d327-150">Return order</span></span>
    - <span data-ttu-id="9d327-151">Mitmesugused tasude päis</span><span class="sxs-lookup"><span data-stu-id="9d327-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="9d327-152">Mitmesuguste kulude rida</span><span class="sxs-lookup"><span data-stu-id="9d327-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="9d327-153">Ostuprotsess</span><span class="sxs-lookup"><span data-stu-id="9d327-153">Purchase process</span></span>

    - <span data-ttu-id="9d327-154">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="9d327-154">Purchase order</span></span>
    - <span data-ttu-id="9d327-155">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="9d327-155">Confirmation</span></span>
    - <span data-ttu-id="9d327-156">Saabunud kaupade loend</span><span class="sxs-lookup"><span data-stu-id="9d327-156">Receipts list</span></span>
    - <span data-ttu-id="9d327-157">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="9d327-157">Product receipt</span></span>
    - <span data-ttu-id="9d327-158">Ostuarve</span><span class="sxs-lookup"><span data-stu-id="9d327-158">Purchase invoice</span></span>
    - <span data-ttu-id="9d327-159">Mitmesugused tasude päis</span><span class="sxs-lookup"><span data-stu-id="9d327-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="9d327-160">Mitmesuguste kulude rida</span><span class="sxs-lookup"><span data-stu-id="9d327-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="9d327-161">Kreeditarve</span><span class="sxs-lookup"><span data-stu-id="9d327-161">Credit note</span></span>
    - <span data-ttu-id="9d327-162">Tagastustellimus</span><span class="sxs-lookup"><span data-stu-id="9d327-162">Return order</span></span>
    - <span data-ttu-id="9d327-163">Ostutaotlus</span><span class="sxs-lookup"><span data-stu-id="9d327-163">Purchase requisition</span></span>
    - <span data-ttu-id="9d327-164">Ostutaotluse rea lisakulud</span><span class="sxs-lookup"><span data-stu-id="9d327-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="9d327-165">Pakkumiskutse</span><span class="sxs-lookup"><span data-stu-id="9d327-165">Request for quotation</span></span>
    - <span data-ttu-id="9d327-166">Pakkumispäise lisakulunõue</span><span class="sxs-lookup"><span data-stu-id="9d327-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="9d327-167">Pakkumisrea lisakulunõue</span><span class="sxs-lookup"><span data-stu-id="9d327-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="9d327-168">Inventuuriprotsess</span><span class="sxs-lookup"><span data-stu-id="9d327-168">Inventory process</span></span>

    - <span data-ttu-id="9d327-169">Kandetellimus-- lähetus</span><span class="sxs-lookup"><span data-stu-id="9d327-169">Transfer order – ship</span></span>
    - <span data-ttu-id="9d327-170">Kandetellimus-- kättesaamine</span><span class="sxs-lookup"><span data-stu-id="9d327-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="9d327-171">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="9d327-171">Related resources</span></span>

[<span data-ttu-id="9d327-172">Maksuteenusega alustamine</span><span class="sxs-lookup"><span data-stu-id="9d327-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="9d327-173">Mitu käibemaksukohustuslase numbrit</span><span class="sxs-lookup"><span data-stu-id="9d327-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="9d327-174">Maksufunktsiooni tugi üleviimistellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="9d327-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="9d327-175">Kuidas koostada maksuteenuste laiendit</span><span class="sxs-lookup"><span data-stu-id="9d327-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
