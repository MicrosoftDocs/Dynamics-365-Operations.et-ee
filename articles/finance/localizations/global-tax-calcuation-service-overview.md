---
title: Maksuarvutus (eelversioon)
description: Selles teemas selgitatakse maksuarvestuse võimekuse üldist ulatust ja funktsioone.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021928"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="62ffd-103">Maksuarvutus (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="62ffd-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="62ffd-104">Maksuarvestus on hüperskaleeritav mitmetasandiline teenus, mis võimaldab global tax engine maksu määramise ja arvutamise protsessi automatiseerida ja seda lihtsustada.</span><span class="sxs-lookup"><span data-stu-id="62ffd-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="62ffd-105">Maksumootor on täielikult konfigureeritav.</span><span class="sxs-lookup"><span data-stu-id="62ffd-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="62ffd-106">Elemendid, mida saab konfigureerida, sisaldavad, kuid ei ole piiratud maksustatavate andmemudelite, maksukoodide, maksu kohaldatavusmaatriksi ja maksuarvutuse valemiga.</span><span class="sxs-lookup"><span data-stu-id="62ffd-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="62ffd-107">Maksumootor töötab teenuste Microsoft Azure põhiplatvormil ja pakub tänapäevasttehnoloogiat ja kõrgetasemelist skaleeritavust.</span><span class="sxs-lookup"><span data-stu-id="62ffd-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="62ffd-108">Maksuarvutus integreerub Dynamics 365 Finance ja Dynamics 365 Supply Chain Management-iga.</span><span class="sxs-lookup"><span data-stu-id="62ffd-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="62ffd-109">Lõpuks integreerub see ka Dynamics 365 Project Operations Dynamics 365 Commerce ja teiste esimese ja kolmanda osapoole rakendustega.</span><span class="sxs-lookup"><span data-stu-id="62ffd-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="62ffd-110">Maksuarvestuse on mikroteenuse põhine maksumootor, mis pakub astmelisi skaleeritavust.</span><span class="sxs-lookup"><span data-stu-id="62ffd-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="62ffd-111">Saate teha järgmisi toiminguid:</span><span class="sxs-lookup"><span data-stu-id="62ffd-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="62ffd-112">Konfigureerige maksuarvestus Regulatory Configuration Service'i (RCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="62ffd-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="62ffd-113">RCS on elektroonilise aruandluse (ER) kujundaja täiustatud versioon ja saadaval eraldi teenusena.</span><span class="sxs-lookup"><span data-stu-id="62ffd-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="62ffd-114">Konfigureerige maksumaatriks maksukoodide ja -määrade automaatseks määramiseks.</span><span class="sxs-lookup"><span data-stu-id="62ffd-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="62ffd-115">Konfigureerige maksumaatriks maksu registreerimise number automaatseks määramiseks.</span><span class="sxs-lookup"><span data-stu-id="62ffd-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="62ffd-116">Konfigureerige maksuarvutuse kujundajat valemite ja tingimuste määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="62ffd-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="62ffd-117">Jagage maksu määramist ja arvutuslahendust juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="62ffd-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="62ffd-118">Maksuarvutusteenuse kasutamiseks installige maksuarvutuse teenuse lisandmoodul oma projektist Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="62ffd-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="62ffd-119">Seejärel lõpetage seadistus RCS-s ja lubage maksu arvutamise teenus finantside ja Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="62ffd-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="62ffd-120">Lisateavet leiate teemast [Maksuteenusega alustamine](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="62ffd-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="62ffd-121">Kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="62ffd-121">Availability</span></span>

<span data-ttu-id="62ffd-122">Maksuarvutus on avaliku eelvaateprogrammi kaudu saadaval ainult liivakasti keskkondades ja valitud klientide jaoks.</span><span class="sxs-lookup"><span data-stu-id="62ffd-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="62ffd-123">Lõpuks muutub see üldiselt kättesaadavaks kõigile klientidele ja tootmiskeskkondades.</span><span class="sxs-lookup"><span data-stu-id="62ffd-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="62ffd-124">Uusi funktsioone edastatakse, mistõttu kontrollige kindlasti kõige ajasemat dokumentatsiooni, et teada saada toetatud funktsioonide laovarudest ja ulatusest.</span><span class="sxs-lookup"><span data-stu-id="62ffd-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="62ffd-125">Maksuarvestus on juurutatud järgmistes Azure'i geograafilistes asukohtades.</span><span class="sxs-lookup"><span data-stu-id="62ffd-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="62ffd-126">See juurutatakse ka rohkematele Azure'i geograafilistele aseukohtades, sõltuvalt klientide vajadustest:</span><span class="sxs-lookup"><span data-stu-id="62ffd-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="62ffd-127">Ameerika Ühendriigid</span><span class="sxs-lookup"><span data-stu-id="62ffd-127">United States</span></span>
- <span data-ttu-id="62ffd-128">Euroopa</span><span class="sxs-lookup"><span data-stu-id="62ffd-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="62ffd-129">Maksuarvestus ei toeta kohapealset juurutamist Dynamics 365-s.</span><span class="sxs-lookup"><span data-stu-id="62ffd-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="62ffd-130">Samuti ei toeta see varasemaid versioone, nt Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="62ffd-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="62ffd-131">Esiletõstetud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="62ffd-131">Feature highlights</span></span>

- <span data-ttu-id="62ffd-132">Konfigureerige maksumaatriks maksude automaatseks määramiseks ja arvutamiseks</span><span class="sxs-lookup"><span data-stu-id="62ffd-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="62ffd-133">Tugi mitme maksu registreerimisnumbritele</span><span class="sxs-lookup"><span data-stu-id="62ffd-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="62ffd-134">Üleviimistellimuse tugi maksu määramiseks ja arvutamiseks</span><span class="sxs-lookup"><span data-stu-id="62ffd-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="62ffd-135">Üleviimistellimuse tugi mitme maksu registreerimisnumbri määramiseks</span><span class="sxs-lookup"><span data-stu-id="62ffd-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="62ffd-136">Toetatud kanded</span><span class="sxs-lookup"><span data-stu-id="62ffd-136">Supported transactions</span></span>

<span data-ttu-id="62ffd-137">Maksuarvestus võib olla juriidiliste isikute ja kannete puhul võimaldatud.</span><span class="sxs-lookup"><span data-stu-id="62ffd-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="62ffd-138">Toetatud on järgmised kanded:</span><span class="sxs-lookup"><span data-stu-id="62ffd-138">The following transactions are supported:</span></span>

- <span data-ttu-id="62ffd-139">Müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="62ffd-139">Sales process</span></span>

    - <span data-ttu-id="62ffd-140">Müügipakkumine</span><span class="sxs-lookup"><span data-stu-id="62ffd-140">Sales quotation</span></span>
    - <span data-ttu-id="62ffd-141">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="62ffd-141">Sales order</span></span>
    - <span data-ttu-id="62ffd-142">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="62ffd-142">Confirmation</span></span>
    - <span data-ttu-id="62ffd-143">Komplekteerimisleht</span><span class="sxs-lookup"><span data-stu-id="62ffd-143">Picking list</span></span>
    - <span data-ttu-id="62ffd-144">Saateleht</span><span class="sxs-lookup"><span data-stu-id="62ffd-144">Packing slip</span></span>
    - <span data-ttu-id="62ffd-145">Müügiarve</span><span class="sxs-lookup"><span data-stu-id="62ffd-145">Sales invoice</span></span>
    - <span data-ttu-id="62ffd-146">Kreeditarve</span><span class="sxs-lookup"><span data-stu-id="62ffd-146">Credit note</span></span>
    - <span data-ttu-id="62ffd-147">Tagastustellimus</span><span class="sxs-lookup"><span data-stu-id="62ffd-147">Return order</span></span>
    - <span data-ttu-id="62ffd-148">Mitmesugused tasude päis</span><span class="sxs-lookup"><span data-stu-id="62ffd-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="62ffd-149">Mitmesuguste kulude rida</span><span class="sxs-lookup"><span data-stu-id="62ffd-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="62ffd-150">Ostuprotsess</span><span class="sxs-lookup"><span data-stu-id="62ffd-150">Purchase process</span></span>

    - <span data-ttu-id="62ffd-151">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="62ffd-151">Purchase order</span></span>
    - <span data-ttu-id="62ffd-152">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="62ffd-152">Confirmation</span></span>
    - <span data-ttu-id="62ffd-153">Saabunud kaupade loend</span><span class="sxs-lookup"><span data-stu-id="62ffd-153">Receipts list</span></span>
    - <span data-ttu-id="62ffd-154">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="62ffd-154">Product receipt</span></span>
    - <span data-ttu-id="62ffd-155">Ostuarve</span><span class="sxs-lookup"><span data-stu-id="62ffd-155">Purchase invoice</span></span>
    - <span data-ttu-id="62ffd-156">Mitmesugused tasude päis</span><span class="sxs-lookup"><span data-stu-id="62ffd-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="62ffd-157">Mitmesuguste kulude rida</span><span class="sxs-lookup"><span data-stu-id="62ffd-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="62ffd-158">Kreeditarve</span><span class="sxs-lookup"><span data-stu-id="62ffd-158">Credit note</span></span>
    - <span data-ttu-id="62ffd-159">Tagastustellimus</span><span class="sxs-lookup"><span data-stu-id="62ffd-159">Return order</span></span>
    - <span data-ttu-id="62ffd-160">Ostutaotlus</span><span class="sxs-lookup"><span data-stu-id="62ffd-160">Purchase requisition</span></span>
    - <span data-ttu-id="62ffd-161">Ostutaotluse rea lisakulud</span><span class="sxs-lookup"><span data-stu-id="62ffd-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="62ffd-162">Pakkumiskutse</span><span class="sxs-lookup"><span data-stu-id="62ffd-162">Request for quotation</span></span>
    - <span data-ttu-id="62ffd-163">Pakkumispäise lisakulunõue</span><span class="sxs-lookup"><span data-stu-id="62ffd-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="62ffd-164">Pakkumisrea lisakulunõue</span><span class="sxs-lookup"><span data-stu-id="62ffd-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="62ffd-165">Inventuuriprotsess</span><span class="sxs-lookup"><span data-stu-id="62ffd-165">Inventory process</span></span>

    - <span data-ttu-id="62ffd-166">Kandetellimus-- lähetus</span><span class="sxs-lookup"><span data-stu-id="62ffd-166">Transfer order – ship</span></span>
    - <span data-ttu-id="62ffd-167">Kandetellimus-- kättesaamine</span><span class="sxs-lookup"><span data-stu-id="62ffd-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="62ffd-168">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="62ffd-168">Related resources</span></span>

[<span data-ttu-id="62ffd-169">Maksuteenusega alustamine</span><span class="sxs-lookup"><span data-stu-id="62ffd-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="62ffd-170">Mitu käibemaksukohustuslase numbrit</span><span class="sxs-lookup"><span data-stu-id="62ffd-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="62ffd-171">Maksufunktsiooni tugi üleviimistellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="62ffd-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="62ffd-172">Kuidas koostada maksuteenuste laiendit</span><span class="sxs-lookup"><span data-stu-id="62ffd-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)