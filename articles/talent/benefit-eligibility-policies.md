---
title: "Soodustuse saamise õiguse eeskirjad"
description: "Selles artiklis antakse teavet soodustuseks sobilikkuse poliitikate kohta, mis aitavad määratleda, kellel on õigus erisoodustustele."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 46dba3a61cf96b19b5bc4d2956d028bbbeaaa60e
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="47197-103">Soodustuse saamise õiguse eeskirjad</span><span class="sxs-lookup"><span data-stu-id="47197-103">Benefit eligibility policies</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="47197-104">Selles teemas antakse teavet soodustuseks sobivuse poliitikate kohta, mis aitavad määratleda, kellel on õigus erisoodustustele.</span><span class="sxs-lookup"><span data-stu-id="47197-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="47197-105">Soodustuste loomisel otsustate, millised töötajad milliseid soodustusi saavad.</span><span class="sxs-lookup"><span data-stu-id="47197-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="47197-106">Järgmises tabelis näidatakse soodustusi, mille võite kindlatele töötajatele kättesaadavaks teha.</span><span class="sxs-lookup"><span data-stu-id="47197-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="47197-107">Soodustus</span><span class="sxs-lookup"><span data-stu-id="47197-107">Benefit</span></span>          | <span data-ttu-id="47197-108">Kellele on soodustus saadaval</span><span class="sxs-lookup"><span data-stu-id="47197-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="47197-109">Tervisekindlustus</span><span class="sxs-lookup"><span data-stu-id="47197-109">Health insurance</span></span> | <span data-ttu-id="47197-110">Kõik töötajad</span><span class="sxs-lookup"><span data-stu-id="47197-110">All employees</span></span>                   |
| <span data-ttu-id="47197-111">Mobiiltelefon</span><span class="sxs-lookup"><span data-stu-id="47197-111">Mobile phone</span></span>     | <span data-ttu-id="47197-112">Müügipersonal, juhtkond</span><span class="sxs-lookup"><span data-stu-id="47197-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="47197-113">Parkimisload</span><span class="sxs-lookup"><span data-stu-id="47197-113">Parking passes</span></span>   | <span data-ttu-id="47197-114">Juhtkond</span><span class="sxs-lookup"><span data-stu-id="47197-114">Executives</span></span>                      |

<span data-ttu-id="47197-115">Soodustuse saamise õiguse poliitikate loomiseks kasutatakse järgmisi komponente.</span><span class="sxs-lookup"><span data-stu-id="47197-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="47197-116">Poliitika reegli tüübid</span><span class="sxs-lookup"><span data-stu-id="47197-116">Policy rule types</span></span>
-   <span data-ttu-id="47197-117">Soodustuse saamise õiguse poliitikad</span><span class="sxs-lookup"><span data-stu-id="47197-117">Benefit eligibility policies</span></span>

<span data-ttu-id="47197-118">Poliitika reeglitüübid määratlevad päringu parameetrid, mida kasutatakse kindlate poliitikareeglite väljatöötamisel.</span><span class="sxs-lookup"><span data-stu-id="47197-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="47197-119">Pärast poliitikareegli tüüpide loomist saate luua soodustuse saamise õiguse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="47197-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="47197-120">Poliitikad võimaldavad teil luua reeglite kogumi, mida rakendatakse ühele või mitmele juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="47197-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="47197-121">Igas poliitikas saate vaadata mis tahes varem loodud soodustuse saamise õiguse poliitika reegli tüüpe.</span><span class="sxs-lookup"><span data-stu-id="47197-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="47197-122">Määratlete poliitika reegli ulatuse.</span><span class="sxs-lookup"><span data-stu-id="47197-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="47197-123">Näiteks kui loote soodustuse saamise õiguse poliitika reegli tüübi nimega **Juht**, saate määrata, mis on selle poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="47197-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="47197-124">Selles näites võib reegel märkida, et reeglisse tuleks kaasata mis tahes ametinimetus, mis sisaldab sõna „juht”.</span><span class="sxs-lookup"><span data-stu-id="47197-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="47197-125">Pärast poliitikasse kaasatava reegli või reeglite parameetrite määratlemist saate määrata soodustusele konkreetsele reegli.</span><span class="sxs-lookup"><span data-stu-id="47197-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="47197-126">Vt ka</span><span class="sxs-lookup"><span data-stu-id="47197-126">See also</span></span>
--------

[<span data-ttu-id="47197-127">Soodustusprogrammi määratlemine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="47197-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




