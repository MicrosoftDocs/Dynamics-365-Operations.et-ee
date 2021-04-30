---
title: Maksuarvutus (eelversioon)
description: Selles teemas selgitatakse maksuarvestuse võimekuse üldist ulatust ja funktsioone.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892345"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="1d151-103">Maksuarvutus (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="1d151-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1d151-104">Maksuarvestus on hüperskaleeritav mitmetasandiline teenus, mis võimaldab global tax engine maksu määramise ja arvutamise protsessi automatiseerida ja seda lihtsustada.</span><span class="sxs-lookup"><span data-stu-id="1d151-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="1d151-105">Maksumootor on täielikult konfigureeritav.</span><span class="sxs-lookup"><span data-stu-id="1d151-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="1d151-106">Elemendid, mida saab konfigureerida, sisaldavad, kuid ei ole piiratud maksustatavate andmemudelite, maksukoodide, maksu kohaldatavusmaatriksi ja maksuarvutuse valemiga.</span><span class="sxs-lookup"><span data-stu-id="1d151-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="1d151-107">Maksumootor töötab teenuste Microsoft Azure põhiplatvormil ja pakub tänapäevasttehnoloogiat ja kõrgetasemelist skaleeritavust.</span><span class="sxs-lookup"><span data-stu-id="1d151-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="1d151-108">Maksuarvutus integreerub Dynamics 365 Finance ja Dynamics 365 Supply Chain Management-iga.</span><span class="sxs-lookup"><span data-stu-id="1d151-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1d151-109">Lõpuks integreerub see ka Dynamics 365 Project Operations Dynamics 365 Commerce ja teiste esimese ja kolmanda osapoole rakendustega.</span><span class="sxs-lookup"><span data-stu-id="1d151-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="1d151-110">Maksuarvestuse on mikroteenuse põhine maksumootor, mis pakub astmelisi skaleeritavust.</span><span class="sxs-lookup"><span data-stu-id="1d151-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="1d151-111">Saate teha järgmisi toiminguid:</span><span class="sxs-lookup"><span data-stu-id="1d151-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="1d151-112">Konfigureerige maksuarvestus Regulatory Configuration Service'i (RCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="1d151-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="1d151-113">RCS on elektroonilise aruandluse (ER) kujundaja täiustatud versioon ja saadaval eraldi teenusena.</span><span class="sxs-lookup"><span data-stu-id="1d151-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="1d151-114">Konfigureerige maksumaatriks maksukoodide ja -määrade automaatseks määramiseks.</span><span class="sxs-lookup"><span data-stu-id="1d151-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="1d151-115">Konfigureerige maksumaatriks maksu registreerimise number automaatseks määramiseks.</span><span class="sxs-lookup"><span data-stu-id="1d151-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="1d151-116">Konfigureerige maksuarvutuse kujundajat valemite ja tingimuste määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="1d151-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="1d151-117">Jagage maksu määramist ja arvutuslahendust juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="1d151-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="1d151-118">Maksuarvutusteenuse kasutamiseks installige maksuarvutuse teenuse lisandmoodul oma projektist Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1d151-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1d151-119">Seejärel lõpetage seadistus RCS-s ja lubage maksu arvutamise teenus finantside ja Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1d151-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="1d151-120">Lisateavet leiate teemast [Maksuteenusega alustamine](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="1d151-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="1d151-121">Kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="1d151-121">Availability</span></span>

<span data-ttu-id="1d151-122">Maksuarvutus on avaliku eelvaateprogrammi kaudu saadaval ainult liivakasti keskkondades ja valitud klientide jaoks.</span><span class="sxs-lookup"><span data-stu-id="1d151-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="1d151-123">Lõpuks muutub see üldiselt kättesaadavaks kõigile klientidele ja tootmiskeskkondades.</span><span class="sxs-lookup"><span data-stu-id="1d151-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="1d151-124">Uusi funktsioone edastatakse, mistõttu kontrollige kindlasti kõige ajasemat dokumentatsiooni, et teada saada toetatud funktsioonide laovarudest ja ulatusest.</span><span class="sxs-lookup"><span data-stu-id="1d151-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="1d151-125">Maksuarvestus on juurutatud järgmistes Azure'i geograafilistes asukohtades.</span><span class="sxs-lookup"><span data-stu-id="1d151-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="1d151-126">See juurutatakse ka rohkematele Azure'i geograafilistele aseukohtades, sõltuvalt klientide vajadustest:</span><span class="sxs-lookup"><span data-stu-id="1d151-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="1d151-127">Ameerika Ühendriigid</span><span class="sxs-lookup"><span data-stu-id="1d151-127">United States</span></span>
- <span data-ttu-id="1d151-128">Euroopa</span><span class="sxs-lookup"><span data-stu-id="1d151-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="1d151-129">Maksuarvestus ei toeta kohapealset juurutamist Dynamics 365-s.</span><span class="sxs-lookup"><span data-stu-id="1d151-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="1d151-130">Samuti ei toeta see varasemaid versioone, nt Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="1d151-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="1d151-131">Esiletõstetud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1d151-131">Feature highlights</span></span>

- <span data-ttu-id="1d151-132">Konfigureerige maksumaatriks maksude automaatseks määramiseks ja arvutamiseks</span><span class="sxs-lookup"><span data-stu-id="1d151-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="1d151-133">Tugi mitme maksu registreerimisnumbritele</span><span class="sxs-lookup"><span data-stu-id="1d151-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="1d151-134">Üleviimistellimuse tugi maksu määramiseks ja arvutamiseks</span><span class="sxs-lookup"><span data-stu-id="1d151-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="1d151-135">Üleviimistellimuse tugi mitme maksu registreerimisnumbri määramiseks</span><span class="sxs-lookup"><span data-stu-id="1d151-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="1d151-136">Toetatud kanded</span><span class="sxs-lookup"><span data-stu-id="1d151-136">Supported transactions</span></span>

<span data-ttu-id="1d151-137">Maksuarvestus võib olla juriidiliste isikute ja kannete puhul võimaldatud.</span><span class="sxs-lookup"><span data-stu-id="1d151-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="1d151-138">Toetatud on järgmised kanded:</span><span class="sxs-lookup"><span data-stu-id="1d151-138">The following transactions are supported:</span></span>

- <span data-ttu-id="1d151-139">Müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="1d151-139">Sales process</span></span>

    - <span data-ttu-id="1d151-140">Müügipakkumine</span><span class="sxs-lookup"><span data-stu-id="1d151-140">Sales quotation</span></span>
    - <span data-ttu-id="1d151-141">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="1d151-141">Sales order</span></span>
    - <span data-ttu-id="1d151-142">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="1d151-142">Confirmation</span></span>
    - <span data-ttu-id="1d151-143">Komplekteerimisleht</span><span class="sxs-lookup"><span data-stu-id="1d151-143">Picking list</span></span>
    - <span data-ttu-id="1d151-144">Saateleht</span><span class="sxs-lookup"><span data-stu-id="1d151-144">Packing slip</span></span>
    - <span data-ttu-id="1d151-145">Müügiarve</span><span class="sxs-lookup"><span data-stu-id="1d151-145">Sales invoice</span></span>
    - <span data-ttu-id="1d151-146">Kreeditarve</span><span class="sxs-lookup"><span data-stu-id="1d151-146">Credit note</span></span>
    - <span data-ttu-id="1d151-147">Tagastustellimus</span><span class="sxs-lookup"><span data-stu-id="1d151-147">Return order</span></span>
    - <span data-ttu-id="1d151-148">Mitmesugused tasude päis</span><span class="sxs-lookup"><span data-stu-id="1d151-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="1d151-149">Mitmesuguste kulude rida</span><span class="sxs-lookup"><span data-stu-id="1d151-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="1d151-150">Ostuprotsess</span><span class="sxs-lookup"><span data-stu-id="1d151-150">Purchase process</span></span>

    - <span data-ttu-id="1d151-151">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="1d151-151">Purchase order</span></span>
    - <span data-ttu-id="1d151-152">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="1d151-152">Confirmation</span></span>
    - <span data-ttu-id="1d151-153">Saabunud kaupade loend</span><span class="sxs-lookup"><span data-stu-id="1d151-153">Receipts list</span></span>
    - <span data-ttu-id="1d151-154">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="1d151-154">Product receipt</span></span>
    - <span data-ttu-id="1d151-155">Ostuarve</span><span class="sxs-lookup"><span data-stu-id="1d151-155">Purchase invoice</span></span>
    - <span data-ttu-id="1d151-156">Mitmesugused tasude päis</span><span class="sxs-lookup"><span data-stu-id="1d151-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="1d151-157">Mitmesuguste kulude rida</span><span class="sxs-lookup"><span data-stu-id="1d151-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="1d151-158">Kreeditarve</span><span class="sxs-lookup"><span data-stu-id="1d151-158">Credit note</span></span>
    - <span data-ttu-id="1d151-159">Tagastustellimus</span><span class="sxs-lookup"><span data-stu-id="1d151-159">Return order</span></span>
    - <span data-ttu-id="1d151-160">Ostutaotlus</span><span class="sxs-lookup"><span data-stu-id="1d151-160">Purchase requisition</span></span>
    - <span data-ttu-id="1d151-161">Ostutaotluse rea lisakulud</span><span class="sxs-lookup"><span data-stu-id="1d151-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="1d151-162">Pakkumiskutse</span><span class="sxs-lookup"><span data-stu-id="1d151-162">Request for quotation</span></span>
    - <span data-ttu-id="1d151-163">Pakkumispäise lisakulunõue</span><span class="sxs-lookup"><span data-stu-id="1d151-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="1d151-164">Pakkumisrea lisakulunõue</span><span class="sxs-lookup"><span data-stu-id="1d151-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="1d151-165">Inventuuriprotsess</span><span class="sxs-lookup"><span data-stu-id="1d151-165">Inventory process</span></span>

    - <span data-ttu-id="1d151-166">Kandetellimus-- lähetus</span><span class="sxs-lookup"><span data-stu-id="1d151-166">Transfer order – ship</span></span>
    - <span data-ttu-id="1d151-167">Kandetellimus-- kättesaamine</span><span class="sxs-lookup"><span data-stu-id="1d151-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="1d151-168">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="1d151-168">Related resources</span></span>

[<span data-ttu-id="1d151-169">Maksuteenusega alustamine</span><span class="sxs-lookup"><span data-stu-id="1d151-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="1d151-170">Mitu käibemaksukohustuslase numbrit</span><span class="sxs-lookup"><span data-stu-id="1d151-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="1d151-171">Maksufunktsiooni tugi üleviimistellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="1d151-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="1d151-172">Kuidas koostada maksuteenuste laiendit</span><span class="sxs-lookup"><span data-stu-id="1d151-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)