---
title: ELi kandesertifikaadid
description: Artikkel annab teavet Euroopa Liidu (EL) kirjesertide kohta.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bf074f54448dd10f190263c09e731c4f4b7a61c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839770"
---
# <a name="eu-entry-certificates"></a><span data-ttu-id="30fe8-103">EL-i kandesertifikaadid</span><span class="sxs-lookup"><span data-stu-id="30fe8-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30fe8-104">Artikkel annab teavet Euroopa Liidu (EL) kirjesertide kohta.</span><span class="sxs-lookup"><span data-stu-id="30fe8-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="30fe8-105">Euroopa Liidu (ELi) kandesertifikaat võimaldab teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="30fe8-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="30fe8-106">Looge ja väljastage EL-i kandesertifikaat koos saatelehe või kliendiarvega kaupade või teenuste ELi riikidesse/regioonidesse tarnimiseks.</span><span class="sxs-lookup"><span data-stu-id="30fe8-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="30fe8-107">Võtke vastu EL-i kandesertifikaate, mille on allkirjastanud EL-i klient.</span><span class="sxs-lookup"><span data-stu-id="30fe8-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="30fe8-108">Laadige üles allkirjastatud EL-i kandesertifikaat, mille saite kliendilt või kolmandalt osapoolelt, kes vastutab kaupade kliendile tarnimise eest.</span><span class="sxs-lookup"><span data-stu-id="30fe8-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="30fe8-109">Seostage üleslaaditud EL-i kandesertifikaat kliendiarvega.</span><span class="sxs-lookup"><span data-stu-id="30fe8-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="30fe8-110">Värskendage üleslaaditud EL-i kandesertifikaadi olekut.</span><span class="sxs-lookup"><span data-stu-id="30fe8-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30fe8-111">Eeltingimused </span><span class="sxs-lookup"><span data-stu-id="30fe8-111">Prerequisites</span></span>
<span data-ttu-id="30fe8-112">Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.</span><span class="sxs-lookup"><span data-stu-id="30fe8-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30fe8-113">Kategooria</span><span class="sxs-lookup"><span data-stu-id="30fe8-113">Category</span></span></th>
<th><span data-ttu-id="30fe8-114">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="30fe8-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30fe8-115">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="30fe8-115">Country/region</span></span></td>
<td><span data-ttu-id="30fe8-116">Juriidilise isiku peamine aadress peab olema ELi liikmesriigis.</span><span class="sxs-lookup"><span data-stu-id="30fe8-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fe8-117">Seotud seadistustoimingud</span><span class="sxs-lookup"><span data-stu-id="30fe8-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="30fe8-118">Tehke lehel <strong>Müügireskontro parameetrid</strong> valikud <strong>Luba kandesertifikaadi haldamine</strong> ja <strong>Luba kandesertifikaadi väljastamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="30fe8-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="30fe8-119">Tehke lehe <strong>Kliendid</strong> kiirkaardil <strong>Arve ja tarne</strong> valik <strong>Kandesertifikaat on nõutav</strong>, näitamiseks, et ELi kandesertifikaat on kliendi puhul nõutav.</span><span class="sxs-lookup"><span data-stu-id="30fe8-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="30fe8-120">Märkige valik <strong>Väljasta kandesertifikaat</strong>, et väljastada kliendile juriidilise isiku ELi kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="30fe8-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="30fe8-121">Valige lehelt <strong>Müügireskontro parameetrid</strong> valiku <strong>Kandesertifikaat</strong> viitele numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="30fe8-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30fe8-122">Seotud kanded</span><span class="sxs-lookup"><span data-stu-id="30fe8-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="30fe8-123">Looge kliendikonto.</span><span class="sxs-lookup"><span data-stu-id="30fe8-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="30fe8-124">Looge müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="30fe8-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="30fe8-125">ELi kandesertifikaadi loomine, registreerimine ja üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="30fe8-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="30fe8-126">EL-i kandesertifikaadi saab luua automaatselt või käsitsi.</span><span class="sxs-lookup"><span data-stu-id="30fe8-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="30fe8-127">ELi kandesertifikaat luuakse ja prinditakse automaatselt, kui sisestate kliendi saatelehe või arve lehele **Saatelehe sisestamine** või **Arve sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="30fe8-128">Kliendi arve ELi kandesertifikaadi käsitsi loomiseks või uuesti printimiseks kasutage lehte **Arve tööleht**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="30fe8-129">Lisaks saate sisestada kolmanda osapoole väljastatud EL-i kandesertifikaadi üksikasjad lehele **Kandesertifikaadi tööleht**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="30fe8-130">ELi kandesertifikaadi loomine automaatselt või käsitsi</span><span class="sxs-lookup"><span data-stu-id="30fe8-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="30fe8-131">Saate luua ELi kandesertifikaadi automaatselt, kasutades saatelehte lehel **Kõik müügitellimused** või arvet lehel **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="30fe8-132">ELi kandesertifikaadi käsitsi loomiseks võite kasutada arvet lehel **Arve tööleht**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="30fe8-133">Kuid enne ELi kandesertifikaadi käsitsi loomist tuleb arve sertifikaadi olekut muuta.</span><span class="sxs-lookup"><span data-stu-id="30fe8-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="30fe8-134">ELi kandesertifikaadi registreerimine</span><span class="sxs-lookup"><span data-stu-id="30fe8-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="30fe8-135">Kui registreerimine on vajalik, saate registreerida kolmanda osapoole väljastatud EL-i kandesertifikaadi lehel **Kandesertifikaadi tööleht**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="30fe8-136">Vastuvõetud ELi kandesertifikaadi üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="30fe8-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="30fe8-137">Kasutage ELi kliendi allkirjaga vastuvõetud ELi kandesertifikaadi üleslaadimiseks lehte **Manused**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="30fe8-138">Pärast sertifikaadi üleslaadimist saate seostada selle arvega, et tõendada kaupade tarnimist.</span><span class="sxs-lookup"><span data-stu-id="30fe8-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="30fe8-139">See tõend on vajalik, kui peate väljastama arve, mis ei sisalda käibemaksu (KM), ja seda kasutatakse ka auditeerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="30fe8-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="30fe8-140">Valikuline: arve sertifikaadi oleku ja printimisoleku uuendamine</span><span class="sxs-lookup"><span data-stu-id="30fe8-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="30fe8-141">Saate uuendada kliendiarve kandesertifikaadi olekut ja printimisolekut, kasutades lehte **Arve tööleht**.</span><span class="sxs-lookup"><span data-stu-id="30fe8-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="30fe8-142">See teave on mõeldud süsteemi administraatoritele.</span><span class="sxs-lookup"><span data-stu-id="30fe8-142">Technical information for system administrators</span></span>
<span data-ttu-id="30fe8-143">Kui teil pole juurdepääsu lehtedele, mida kasutatakse selle ülesande täitmiseks, pöörduge oma süsteemiadministraatori poole ja edastage järgmises tabelis antud andmed.</span><span class="sxs-lookup"><span data-stu-id="30fe8-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30fe8-144">Kategooria</span><span class="sxs-lookup"><span data-stu-id="30fe8-144">Category</span></span></th>
<th><span data-ttu-id="30fe8-145">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="30fe8-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30fe8-146">Turberollid ja kohustused</span><span class="sxs-lookup"><span data-stu-id="30fe8-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="30fe8-147">Kaupade või teenuste jaoks EL-i kandesertifikaatide häälestamiseks ja loomiseks peate kuuluma turberolli, mis hõlmab järgmisi kohustusi.</span><span class="sxs-lookup"><span data-stu-id="30fe8-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="30fe8-148"><strong>Müügireskontro ametnik</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="30fe8-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="30fe8-149"><strong>Klienditeeninduse esindaja</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="30fe8-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="30fe8-150"><strong>Müügiametnik</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="30fe8-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="30fe8-151"><strong>Lähetusametnik</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="30fe8-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]