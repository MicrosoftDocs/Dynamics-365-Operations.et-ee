---
title: Tulu tuvastamise ülevaade
description: Sellest teemast leiate teavet tulu tuvastamise funktsiooni kohta. See funktsioon pakub paindlikku raamistikku, mis võimaldab teil määratleda ettevõtte erireeglid nii tuluhinna kui ka tulugraafiku kajastamiseks mitme elemendiga tellimuste puhul.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: d1aeb0cf556582ff53ca00c6bb8d863a088950b9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184113"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="443be-104">Tulu tuvastamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="443be-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> <span data-ttu-id="443be-105">Tulu tuvastamise funktsiooni ei saa veel funktsioonihalduse kaudu sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="443be-105">The Revenue recognition feature can't yet be turned on through Feature management.</span></span> <span data-ttu-id="443be-106">Praegu peate selle sisselülitamiseks kasutama konfiguratsioonivõtmeid.</span><span class="sxs-lookup"><span data-stu-id="443be-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="443be-107">Mitut elementi müüvad ettevõtted (nt tooted, teenused, kordustellimused jne) peavad olema võimelised tagama mitme elemendiga tellimusi, et saaks tulu tuvastada kindlate ettevõtte- ja valdkonnaspetsiifiliste juhiste alusel.</span><span class="sxs-lookup"><span data-stu-id="443be-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="443be-108">Üldiselt saab tulu tuvastamise protsessi kasutada järgmiste ülesannete täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="443be-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="443be-109">Tulude jaotamine aitab tagada, et vastav tulu hind tuvastatakse mitme elemendiga tellimuste komponentide väärtuse alusel.</span><span class="sxs-lookup"><span data-stu-id="443be-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="443be-110">Lükake edasi tulu, põhinedes tulugraafikul, mis kajastab lepingujärgset ajavahemikku ja tulu tuvastamise protsente aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="443be-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

<span data-ttu-id="443be-111">Tulu tuvastamise funktsioon pakub paindlikku raamistikku, mis võimaldab teil määratleda ettevõtte erireeglid nii tuluhinna kui ka tulugraafiku kajastamiseks.</span><span class="sxs-lookup"><span data-stu-id="443be-111">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="443be-112">Väljastatud tooteid kasutatakse müügitellimuse dokumentide tulu tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="443be-112">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="443be-113">Välja saadetud tooted sisaldavad seadistust, mis on vajalik tuluhinna ja tulugraafiku määramiseks.</span><span class="sxs-lookup"><span data-stu-id="443be-113">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="443be-114">Müügitellimus võib pärineda aja- ja materjalikulu projektist.</span><span class="sxs-lookup"><span data-stu-id="443be-114">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="443be-115">Ettevõtted saavad kasutada tulugraafiku funktsiooni tuluhinna funktsiooni kasutamata.</span><span class="sxs-lookup"><span data-stu-id="443be-115">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="443be-116">Seetõttu kasutatakse hindu müügitellimuse ridadel kas tulu või edasilükkunud tuluna.</span><span class="sxs-lookup"><span data-stu-id="443be-116">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="443be-117">Kui müügitellimuse real on olemas tulugraafik, lükatakse müügitellimuse rea hind edasi.</span><span class="sxs-lookup"><span data-stu-id="443be-117">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="443be-118">Kui müügitellimuse real pole tulugraafikut, sisestatakse müügitellimuse rea hind tulukonto arvele.</span><span class="sxs-lookup"><span data-stu-id="443be-118">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="443be-119">Tuluhind arvutatakse kas müügitellimuse kinnitamisel või arve sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="443be-119">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="443be-120">Enne arve sisestamist tuluhinna eelvaate nägemiseks peate müügitellimuse kinnitama.</span><span class="sxs-lookup"><span data-stu-id="443be-120">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="443be-121">Kui müügitellimus on kinnitatud, luuakse ka eeldatav tulugraafik, kui mõnel müügitellimuse real on tulugraafik.</span><span class="sxs-lookup"><span data-stu-id="443be-121">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="443be-122">Müügitellimuse arveldamisel kustutatakse eeldatav tulugraafik ja see asendatakse tegeliku tulu kajastamise graafikuga.</span><span class="sxs-lookup"><span data-stu-id="443be-122">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="443be-123">Tulu kajastamise graafiku üksikasjad kinnitatakse iga müügitellimuse rea kohta.</span><span class="sxs-lookup"><span data-stu-id="443be-123">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="443be-124">Tänu sellele saab tulu tuvastamise haldur vaadata üksikasju ja saab vabastada read tulule, kui lepinguline kohustus on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="443be-124">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="443be-125">Iga perioodi lõpus saab tulu tuvastamise haldur luua tulutöölehe, et vabastada kõik graafikuread, mille tähtaeg on samal päeval või varasem tema määratud kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="443be-125">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date that he or she defines.</span></span> <span data-ttu-id="443be-126">Seda tulutöölehet ei sisestata kohe.</span><span class="sxs-lookup"><span data-stu-id="443be-126">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="443be-127">Tänu sellele saab tulu tuvastamise haldur kinnitada, et õiged summad vabastatakse edasilükkunud tulult tegelikule tulule.</span><span class="sxs-lookup"><span data-stu-id="443be-127">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="443be-128">Kui lepingumuudatus põhjustab uue müügitellimuse rea lisamise kas olemasolevale müügitellimusele või uuele müügitellimusele, saab tuluhinna kõigi müügitellimuste ridade korrigeerimiseks ümberjaotamise protsessi käitada.</span><span class="sxs-lookup"><span data-stu-id="443be-128">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
