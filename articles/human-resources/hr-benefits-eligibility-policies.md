---
title: Soodustuse saamise õiguse eeskirjad
description: Selles artiklis antakse teavet soodustuseks sobilikkuse poliitikate kohta, mis aitavad määratleda, kellel on õigus erisoodustustele.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a5046f1d32fb965c7cb3793daf1ba40b9c2a1d10
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805894"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="26de5-103">Soodustuse saamise õiguse eeskirjad</span><span class="sxs-lookup"><span data-stu-id="26de5-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="26de5-104">Selles artiklis antakse teavet soodustuseks sobilikkuse poliitikate kohta, mis aitavad määratleda, kellel on õigus erisoodustustele.</span><span class="sxs-lookup"><span data-stu-id="26de5-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="26de5-105">Soodustuste loomisel otsustate, millised töötajad milliseid soodustusi saavad.</span><span class="sxs-lookup"><span data-stu-id="26de5-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="26de5-106">Järgmises tabelis näidatakse soodustusi, mille võite kindlatele töötajatele kättesaadavaks teha.</span><span class="sxs-lookup"><span data-stu-id="26de5-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="26de5-107">Soodustus</span><span class="sxs-lookup"><span data-stu-id="26de5-107">Benefit</span></span>          | <span data-ttu-id="26de5-108">Kellele on soodustus saadaval</span><span class="sxs-lookup"><span data-stu-id="26de5-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="26de5-109">Tervisekindlustus</span><span class="sxs-lookup"><span data-stu-id="26de5-109">Health insurance</span></span> | <span data-ttu-id="26de5-110">Kõik töötajad</span><span class="sxs-lookup"><span data-stu-id="26de5-110">All employees</span></span>                   |
| <span data-ttu-id="26de5-111">Mobiiltelefon</span><span class="sxs-lookup"><span data-stu-id="26de5-111">Mobile phone</span></span>     | <span data-ttu-id="26de5-112">Müügipersonal, juhtkond</span><span class="sxs-lookup"><span data-stu-id="26de5-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="26de5-113">Parkimisload</span><span class="sxs-lookup"><span data-stu-id="26de5-113">Parking passes</span></span>   | <span data-ttu-id="26de5-114">Juhtkond</span><span class="sxs-lookup"><span data-stu-id="26de5-114">Executives</span></span>                      |

<span data-ttu-id="26de5-115">Soodustuse saamise õiguse poliitikate loomiseks kasutatakse järgmisi komponente.</span><span class="sxs-lookup"><span data-stu-id="26de5-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="26de5-116">Poliitika reegli tüübid</span><span class="sxs-lookup"><span data-stu-id="26de5-116">Policy rule types</span></span>
-   <span data-ttu-id="26de5-117">Soodustuse saamise õiguse poliitikad</span><span class="sxs-lookup"><span data-stu-id="26de5-117">Benefit eligibility policies</span></span>

<span data-ttu-id="26de5-118">Poliitika reeglitüübid määratlevad päringu parameetrid, mida kasutatakse kindlate poliitikareeglite väljatöötamisel.</span><span class="sxs-lookup"><span data-stu-id="26de5-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="26de5-119">Pärast poliitikareegli tüüpide loomist saate luua soodustuse saamise õiguse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="26de5-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="26de5-120">Poliitikad võimaldavad teil luua reeglite kogumi, mida rakendatakse ühele või mitmele juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="26de5-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="26de5-121">Igas poliitikas saate vaadata mis tahes varem loodud soodustuse saamise õiguse poliitika reegli tüüpe.</span><span class="sxs-lookup"><span data-stu-id="26de5-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="26de5-122">Määratlete poliitika reegli ulatuse.</span><span class="sxs-lookup"><span data-stu-id="26de5-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="26de5-123">Näiteks kui loote soodustuse saamise õiguse poliitika reegli tüübi nimega **Juht**, saate määrata, mis on selle poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="26de5-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="26de5-124">Selles näites võib reegel märkida, et reeglisse tuleks kaasata mis tahes ametinimetus, mis sisaldab sõna „juht”.</span><span class="sxs-lookup"><span data-stu-id="26de5-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="26de5-125">Pärast poliitikasse kaasatava reegli või reeglite parameetrite määratlemist saate määrata soodustusele konkreetsele reegli.</span><span class="sxs-lookup"><span data-stu-id="26de5-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]