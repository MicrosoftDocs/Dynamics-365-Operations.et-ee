---
title: Soodustuse saamise õiguse eeskirjad
description: Selles artiklis antakse teavet soodustuseks sobilikkuse poliitikate kohta, mis aitavad määratleda, kellel on õigus erisoodustustele.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 5bd11e5dceb831968c8458ec07d2aca8fb660763
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898476"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="b4637-103">Soodustuse saamise õiguse eeskirjad</span><span class="sxs-lookup"><span data-stu-id="b4637-103">Benefit eligibility policies</span></span>

<span data-ttu-id="b4637-104">Selles teemas antakse teavet soodustuseks sobivuse poliitikate kohta, mis aitavad määratleda, kellel on õigus erisoodustustele.</span><span class="sxs-lookup"><span data-stu-id="b4637-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="b4637-105">Soodustuste loomisel otsustate, millised töötajad milliseid soodustusi saavad.</span><span class="sxs-lookup"><span data-stu-id="b4637-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="b4637-106">Järgmises tabelis näidatakse soodustusi, mille võite kindlatele töötajatele kättesaadavaks teha.</span><span class="sxs-lookup"><span data-stu-id="b4637-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="b4637-107">Soodustus</span><span class="sxs-lookup"><span data-stu-id="b4637-107">Benefit</span></span>          | <span data-ttu-id="b4637-108">Kellele on soodustus saadaval</span><span class="sxs-lookup"><span data-stu-id="b4637-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="b4637-109">Tervisekindlustus</span><span class="sxs-lookup"><span data-stu-id="b4637-109">Health insurance</span></span> | <span data-ttu-id="b4637-110">Kõik töötajad</span><span class="sxs-lookup"><span data-stu-id="b4637-110">All employees</span></span>                   |
| <span data-ttu-id="b4637-111">Mobiiltelefon</span><span class="sxs-lookup"><span data-stu-id="b4637-111">Mobile phone</span></span>     | <span data-ttu-id="b4637-112">Müügipersonal, juhtkond</span><span class="sxs-lookup"><span data-stu-id="b4637-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="b4637-113">Parkimisload</span><span class="sxs-lookup"><span data-stu-id="b4637-113">Parking passes</span></span>   | <span data-ttu-id="b4637-114">Juhtkond</span><span class="sxs-lookup"><span data-stu-id="b4637-114">Executives</span></span>                      |

<span data-ttu-id="b4637-115">Soodustuse saamise õiguse poliitikate loomiseks kasutatakse järgmisi komponente.</span><span class="sxs-lookup"><span data-stu-id="b4637-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="b4637-116">Poliitika reegli tüübid</span><span class="sxs-lookup"><span data-stu-id="b4637-116">Policy rule types</span></span>
-   <span data-ttu-id="b4637-117">Soodustuse saamise õiguse poliitikad</span><span class="sxs-lookup"><span data-stu-id="b4637-117">Benefit eligibility policies</span></span>

<span data-ttu-id="b4637-118">Poliitika reeglitüübid määratlevad päringu parameetrid, mida kasutatakse kindlate poliitikareeglite väljatöötamisel.</span><span class="sxs-lookup"><span data-stu-id="b4637-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="b4637-119">Pärast poliitikareegli tüüpide loomist saate luua soodustuse saamise õiguse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="b4637-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="b4637-120">Poliitikad võimaldavad teil luua reeglite kogumi, mida rakendatakse ühele või mitmele juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="b4637-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="b4637-121">Igas poliitikas saate vaadata mis tahes varem loodud soodustuse saamise õiguse poliitika reegli tüüpe.</span><span class="sxs-lookup"><span data-stu-id="b4637-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="b4637-122">Määratlete poliitika reegli ulatuse.</span><span class="sxs-lookup"><span data-stu-id="b4637-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="b4637-123">Näiteks kui loote soodustuse saamise õiguse poliitika reegli tüübi nimega **Juht**, saate määrata, mis on selle poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="b4637-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="b4637-124">Selles näites võib reegel märkida, et reeglisse tuleks kaasata mis tahes ametinimetus, mis sisaldab sõna „juht”.</span><span class="sxs-lookup"><span data-stu-id="b4637-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="b4637-125">Pärast poliitikasse kaasatava reegli või reeglite parameetrite määratlemist saate määrata soodustusele konkreetsele reegli.</span><span class="sxs-lookup"><span data-stu-id="b4637-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b4637-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b4637-126">Additional resources</span></span>
--------

[<span data-ttu-id="b4637-127">Soodustusprogrammi määratlemine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="b4637-127">Define and manage a benefits program</span></span>](manage-benefit-program.md)



