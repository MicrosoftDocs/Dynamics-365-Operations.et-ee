---
title: Auditipoliitika reeglid
description: Auditipoliitikaga saate hinnata kuluaruandeid, hankija arveid ja ostutellimusi, et kontrollida, kas need vastavad loodud poliitikareeglitele. Kõik auditi poliitikaga seotud reeglid käitatakse pakett-režiimis vastavalt teie määratud graafikule.  Iga poliitikareegel on poliitikareegli tüübi eksemplar. Iga poliitikareegli tüübi puhul saab korraga aktiivne olla vaid üks reegel.
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de6406029aa88424863dd9a47505f5b3ad27f237
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177314"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="419ff-106">Auditipoliitika reeglid</span><span class="sxs-lookup"><span data-stu-id="419ff-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="419ff-107">Auditipoliitikaga saate hinnata kuluaruandeid, hankija arveid ja ostutellimusi, et kontrollida, kas need vastavad loodud poliitikareeglitele.</span><span class="sxs-lookup"><span data-stu-id="419ff-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="419ff-108">Kõik auditi poliitikaga seotud reeglid käitatakse pakett-režiimis vastavalt teie määratud graafikule.</span><span class="sxs-lookup"><span data-stu-id="419ff-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="419ff-109">Iga poliitikareegel on poliitikareegli tüübi eksemplar.</span><span class="sxs-lookup"><span data-stu-id="419ff-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="419ff-110">Iga poliitikareegli tüübi puhul saab korraga aktiivne olla vaid üks reegel.</span><span class="sxs-lookup"><span data-stu-id="419ff-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="419ff-111">Päringud ja päringu tüübid</span><span class="sxs-lookup"><span data-stu-id="419ff-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="419ff-112">Auditipoliitika reegli loomisel valite esmalt poliitikareegli tüübi.</span><span class="sxs-lookup"><span data-stu-id="419ff-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="419ff-113">Poliitikareegli tüübiga määratakse rakendusobjektide puu (AOT) päring, mida kasutatakse poliitikareegli loomisel alguspunktina.</span><span class="sxs-lookup"><span data-stu-id="419ff-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="419ff-114">Samuti määratakse poliitikareegli jaoks kasutatav päringu tüüp.</span><span class="sxs-lookup"><span data-stu-id="419ff-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="419ff-115">Päring määrab, millist lähtedokumenti poliitikareegel hindab.</span><span class="sxs-lookup"><span data-stu-id="419ff-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="419ff-116">See määrab ka lähtedokumendi väljad, mis näitavad dokumentide auditi jaoks valimisel kasutatavat juriidilist isikut ja kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="419ff-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="419ff-117">Päringu tüübiga määratakse päringulehe ja lehe Auditipoliitika reegel vaikeväljad.</span><span class="sxs-lookup"><span data-stu-id="419ff-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="419ff-118">Järgmises tabelis on auditi poliitikareeglite jaoks saadaolevad päringu tüübid.</span><span class="sxs-lookup"><span data-stu-id="419ff-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="419ff-119">Päringu tüüp</span><span class="sxs-lookup"><span data-stu-id="419ff-119">Query type</span></span></th>
<th><span data-ttu-id="419ff-120">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="419ff-120">Purpose</span></span></th>
<th><span data-ttu-id="419ff-121">Lisateave</span><span class="sxs-lookup"><span data-stu-id="419ff-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="419ff-122">Tinglik</span><span class="sxs-lookup"><span data-stu-id="419ff-122">Conditional</span></span></td>
<td><span data-ttu-id="419ff-123">Võrrelge lähtedokumendi atribuute määratud väärtustega.</span><span class="sxs-lookup"><span data-stu-id="419ff-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="419ff-124">Koonda</span><span class="sxs-lookup"><span data-stu-id="419ff-124">Aggregate</span></span></td>
<td><span data-ttu-id="419ff-125">Võrrelge mitut lähtedokumenti või lähtedokumendi rida poliitikareegliga, koondades arvväärtusi.</span><span class="sxs-lookup"><span data-stu-id="419ff-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="419ff-126">Diskreetimine</span><span class="sxs-lookup"><span data-stu-id="419ff-126">Sampling</span></span></td>
<td><span data-ttu-id="419ff-127">Valige kindla protsendimäära alusel juhuslikult lähtedokumendid, et kontrollida poliitika rikkumist.</span><span class="sxs-lookup"><span data-stu-id="419ff-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="419ff-128">Kui valite selle suvandi, kasutage auditiks juhuslikult valitavate dokumentide protsendi määramiseks lehte Auditipoliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="419ff-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="419ff-129">Duplikaat</span><span class="sxs-lookup"><span data-stu-id="419ff-129">Duplicate</span></span></td>
<td><span data-ttu-id="419ff-130">Hinnake lähtedokumente kontrollimaks, kas nende määratud väljadel on topeltkirjeid.</span><span class="sxs-lookup"><span data-stu-id="419ff-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="419ff-131">Kui valite selle suvandi, määrake lehel Auditipoliitika reegel päevade arv, mis liidetakse dokumentide valimise kuupäevavahemiku algusele, kui dokumentidest otsitakse topeltkirjeid.</span><span class="sxs-lookup"><span data-stu-id="419ff-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="419ff-132">Loendi otsing</span><span class="sxs-lookup"><span data-stu-id="419ff-132">List search</span></span></td>
<td><span data-ttu-id="419ff-133">Otsige lähtedokumentidest kindlaid üksusi.</span><span class="sxs-lookup"><span data-stu-id="419ff-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="419ff-134">Päringu juurdokumendi määratleb auditeeritava dokumendi.</span><span class="sxs-lookup"><span data-stu-id="419ff-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="419ff-135">Päring peab olema loendipäring, mis sisaldab viidet tabelile dirpartytable.</span><span class="sxs-lookup"><span data-stu-id="419ff-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="419ff-136">Seda suvandit saab kasutada ainult järgmiste AOT päringutega.</span><span class="sxs-lookup"><span data-stu-id="419ff-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="419ff-137"><span class="ui">AuditPolicyExpenseList</span> (kuluaruande jälgitavad töötajad)</span><span class="sxs-lookup"><span data-stu-id="419ff-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="419ff-138"><span class="ui">AuditPolicyPurchList</span> (ostutellimuse jälgitavad hankijad)</span><span class="sxs-lookup"><span data-stu-id="419ff-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="419ff-139"><span class="ui">AuditPolicyVendInvoiceList</span> (hankija arve jälgitavad hankijad)</span><span class="sxs-lookup"><span data-stu-id="419ff-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="419ff-140">Selle suvandi valimisel määrake jälgitavad üksused lehel Auditipoliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="419ff-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="419ff-141">Märksõna otsing</span><span class="sxs-lookup"><span data-stu-id="419ff-141">Keyword search</span></span></td>
<td><span data-ttu-id="419ff-142">Kontrollige, kas lähtedokumentides on teatud sõnu.</span><span class="sxs-lookup"><span data-stu-id="419ff-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="419ff-143">Selle suvandi valimisel sisestage otsitavad sõnad lehel Auditipoliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="419ff-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="419ff-144">Lehel Auditipoliitika reegel on ka suvandid, millega saate määrata tabelid ja väljad, millest sisestatud sõnu otsida.</span><span class="sxs-lookup"><span data-stu-id="419ff-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="419ff-145">Üldparameetrid</span><span class="sxs-lookup"><span data-stu-id="419ff-145">Common parameters</span></span>
<span data-ttu-id="419ff-146">Kõigil kindla auditipoliitika poliitikareeglitel on samad partiiparameetrid ja sama dokumendi valiku kuupäevavahemik.</span><span class="sxs-lookup"><span data-stu-id="419ff-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="419ff-147">Need parameetrid on määratud poliitikas lehel Lisavalikud.</span><span class="sxs-lookup"><span data-stu-id="419ff-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="419ff-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="419ff-148">Additional resources</span></span>
--------

<span data-ttu-id="419ff-149">[Auditipoliitika rikkumised ja juhtumid](audit-policy-violations-cases.md)
[Lähtedokumentide jaoks auditipoliitikate määratlemine](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="419ff-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>

