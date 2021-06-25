---
title: Auditipoliitika rikkumised ja juhtumid
description: Artiklis selgitatakse, kuidas auditi poliitikareeglite rikkumistest auditijuhtumeid luuakse. See sisaldab ka teavet erinevate viiside kohta, kuidas auditireeglite kasutavad dokumendi valimise kuupäevavahemikku.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82d94be7a0ce915b0a2b86fb3894435afdd6f37a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187840"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="d01a3-104">Auditipoliitika rikkumised ja juhtumid</span><span class="sxs-lookup"><span data-stu-id="d01a3-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d01a3-105">Artiklis selgitatakse, kuidas auditi poliitikareeglite rikkumistest auditijuhtumeid luuakse.</span><span class="sxs-lookup"><span data-stu-id="d01a3-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="d01a3-106">See sisaldab ka teavet erinevate viiside kohta, kuidas auditireeglite kasutavad dokumendi valimise kuupäevavahemikku.</span><span class="sxs-lookup"><span data-stu-id="d01a3-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

## <a name="how-audit-cases-are-generated"></a><span data-ttu-id="d01a3-107">Auditijuhtumite loomine</span><span class="sxs-lookup"><span data-stu-id="d01a3-107">How audit cases are generated</span></span>

<span data-ttu-id="d01a3-108">Auditipoliitikaid kasutatakse kuluaruannete, ostutellimuste ja hankija arvete tuvastamiseks, mis ei ole kooskõlas ärireeglitega, mille määratlete ja konfigureerite auditipoliitika reeglitena.</span><span class="sxs-lookup"><span data-stu-id="d01a3-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="d01a3-109">Auditipoliitikaid käitatakse pakktöötlusrežiimis.</span><span class="sxs-lookup"><span data-stu-id="d01a3-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="d01a3-110">Auditipoliitika käitamisel käivitatakse samal ajal kõik sellesse poliitikasse kuuluvad poliitikareeglid.</span><span class="sxs-lookup"><span data-stu-id="d01a3-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="d01a3-111">Iga poliitika reegel hindab dokumentide kogumit.</span><span class="sxs-lookup"><span data-stu-id="d01a3-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="d01a3-112">Poliitika reegel valib dokumendid, mis on dokumendi valiku kuupäevavahemikus ja mis ühtivad määratud kriteeriumidega.</span><span class="sxs-lookup"><span data-stu-id="d01a3-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="d01a3-113">Näiteks võib üks poliitika reegel valida kuluaruanded, milles on menüüd, mis ületavad 50,00.</span><span class="sxs-lookup"><span data-stu-id="d01a3-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="d01a3-114">Teine poliitika reegel võib valida hankija arved, mis tuleb tasuda kindlale hankijale.</span><span class="sxs-lookup"><span data-stu-id="d01a3-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="d01a3-115">Iga kogumis valitud dokumendi puhul luuakse rikkumine.</span><span class="sxs-lookup"><span data-stu-id="d01a3-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="d01a3-116">See rikkumine on kirje selle kohta, et konkreetne dokument, nt arve 12345, ei ole poliitika reegliga kooskõlas.</span><span class="sxs-lookup"><span data-stu-id="d01a3-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="d01a3-117">Mitme auditi rikkumise kirjed on grupeeritud kokku ja seostatakse auditijuhtumitega.</span><span class="sxs-lookup"><span data-stu-id="d01a3-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="d01a3-118">Vaikimisi grupeeritakse iga auditipoliitika juhtumid auditipoliitika reegli järgi.</span><span class="sxs-lookup"><span data-stu-id="d01a3-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="d01a3-119">Soovi korral saate valida muud grupeerimiskriteeriumid, kasutades lehte **Juhtumite grupeerimise kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="d01a3-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="d01a3-120">Näiteks saate grupeerida kulupäiseid projekti ID ja hankija arveid hankija konto järgi.</span><span class="sxs-lookup"><span data-stu-id="d01a3-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="d01a3-121">Sel juhul grupeeritakse kõik sama projekti ID-ga kulu päise rikkumised samasse juhtumisse ja samasse juhtumisse grupeeritakse ka kõik sama hankija kontoga hankija arved.</span><span class="sxs-lookup"><span data-stu-id="d01a3-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="d01a3-122">Auditipoliitika reeglite puhul, mis põhinevad päringu tüübil **Duplikaat**, ei grupeerita rikkumisi poliitika reegli või kriteeriumide järgi, mis on määratud lehel **Juhtumite grupeerimise kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="d01a3-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="d01a3-123">Selle asemel grupeeritakse need auditipoliitika reeglisse integreeritud kriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="d01a3-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="d01a3-124">Näiteks kui poliitika reegel hindab kuluaruandeid sama summa, kaupmehe ID ja kuupäeva dubleeritud kulude puhul, on kõik kulud, millel on neil väljadel samad väärtused, üks juhtum.</span><span class="sxs-lookup"><span data-stu-id="d01a3-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="d01a3-125">Kõik kulud, millel on erinevad väärtused, on eraldi juhtum.</span><span class="sxs-lookup"><span data-stu-id="d01a3-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="d01a3-126">Pärast auditi juhtumite loomist käsitsetakse neid juhtumihalduse tüüpiliste protsesside abil.</span><span class="sxs-lookup"><span data-stu-id="d01a3-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="d01a3-127">Dokumendi valiku kuupäevavahemikud</span><span class="sxs-lookup"><span data-stu-id="d01a3-127">Document selection date ranges</span></span>
<span data-ttu-id="d01a3-128">Auditi poliitika käitamisel valib iga poliitika reegel määratud tüüpi dokumendid, millel on dokumendi valiku kuupäevavahemiku kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d01a3-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="d01a3-129">Dokumendivaliku kuupäevavahemik määratletakse lehel **Lisavalikud**.</span><span class="sxs-lookup"><span data-stu-id="d01a3-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="d01a3-130">Mitme dokumendiga on seostatud rohkem kui üks kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d01a3-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="d01a3-131">Auditipoliitika reegli kasutatav kuupäeva väli on määratletud lehel **Poliitika reegli tüüp**.</span><span class="sxs-lookup"><span data-stu-id="d01a3-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="d01a3-132">Järgmiselt on toodud muud moodused, mil auditi poliitika dokumendi valiku kuupäevavahemikku kasutab.</span><span class="sxs-lookup"><span data-stu-id="d01a3-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="d01a3-133">Poliitika kasutab iga poliitika reegli versiooni, mis kehtib dokumendi valiku kuupäevavahemiku viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="d01a3-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="d01a3-134">Saate vaadata iga poliitika reegli kehtivuse kuupäevi loendilehel **Auditipoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="d01a3-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d01a3-135">Poliitika kasutab organisatsiooni sõlmi, mis on seostatud poliitikaga dokumendi valiku kuupäevavahemiku viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="d01a3-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="d01a3-136">Loendilehel **Auditipoliitikad** kuvatakse ainult organisatsiooni sõlmed, mis on praegu poliitikaga seostatud.</span><span class="sxs-lookup"><span data-stu-id="d01a3-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d01a3-137">Poliitika reeglite puhul, mis põhinevad päringu tüübil **loendiotsing**, hindab poliitika dokumente jälgitavate üksuste osas, mis jõustuvad dokumendi valiku kuupäevavahemiku viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="d01a3-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="d01a3-138">Lisateavet vt teemast [Auditipoliitika reeglid](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="d01a3-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]