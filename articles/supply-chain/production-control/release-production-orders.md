---
title: Tootmistellimuste väljastamine
description: Väljastatud tootmistellimus on tellimus, millele on antud tootmiseks luba. Mõistet „väljastatud” kasutatakse tootmistellimuse töötsükli sellise oleku kirjeldamiseks, kus tootmistellimus on saadaval saadaval tootmistöödel ja laoprotsessides täitmiseks.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118b0d6300647135b22e42cc84a79f07e48d7ef4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811698"
---
# <a name="release-production-orders"></a><span data-ttu-id="f854d-104">Tootmistellimuste väljastamine</span><span class="sxs-lookup"><span data-stu-id="f854d-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f854d-105">Väljastatud tootmistellimus on tellimus, millele on antud tootmiseks luba.</span><span class="sxs-lookup"><span data-stu-id="f854d-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="f854d-106">Mõistet „väljastatud” kasutatakse tootmistellimuse töötsükli sellise oleku kirjeldamiseks, kus tootmistellimus on saadaval saadaval tootmistöödel ja laoprotsessides täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="f854d-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="f854d-107">Väljastatud oleku omadused</span><span class="sxs-lookup"><span data-stu-id="f854d-107">Characteristics of the Released state</span></span>

<span data-ttu-id="f854d-108">Olek **Väljastatud** on üks olek tootmistellimuse tsüklis.</span><span class="sxs-lookup"><span data-stu-id="f854d-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="f854d-109">Tootmistellimused, mille olek on **Väljastatud** on saadaval tootmistöödel ja laoprotsessides täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="f854d-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="f854d-110">Olekul **Väljastatud** on järgmised tunnused.</span><span class="sxs-lookup"><span data-stu-id="f854d-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="f854d-111">Tootmistellimuse saab seada olekusse **Väljastatud** kas tootmistellimuselt või pakktöötluse abil.</span><span class="sxs-lookup"><span data-stu-id="f854d-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="f854d-112">Tootmistellimuse saab ka automaatselt värskendada plaanitud tootmistellimustelt, mis on kinnitatud lehe **Kinnituse ajapiir** väljaga **Koondplaan**.</span><span class="sxs-lookup"><span data-stu-id="f854d-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="f854d-113">Olek **Väljastatud** on märguanne tööde operaatoritele, et tööde juhtimise moodulis tuleb käivitada tootmistööd.</span><span class="sxs-lookup"><span data-stu-id="f854d-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="f854d-114">Tootmisdokumendid, näiteks protsessikaardid, protsessitööd ja töökaardid pakuvad teavet tootmistööde kohta ja neid saab väljastada.</span><span class="sxs-lookup"><span data-stu-id="f854d-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="f854d-115">Füüsiliselt reserveeritud materjalide puhul luuakse laotöö materjalide komplekteerimiseks tootmistellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="f854d-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="f854d-116">Tööde väljastamine tööde juhtimisse</span><span class="sxs-lookup"><span data-stu-id="f854d-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="f854d-117">Kui tootmistellimus on väljastatud, on tellimusega seotud tootmistööd nähtaval ja registreerimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="f854d-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="f854d-118">Operaatorid saavad teha tööde registreerimisi, nagu Käivita, Peata ja Lõpetamine, kas lehel **Töökaardi terminal** või **Töökaardi seade**.</span><span class="sxs-lookup"><span data-stu-id="f854d-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="f854d-119">Registreeritud aeg ja kogus kantakse registreerimislehtedelt automaatselt üle tootmise töölehtedele, et jälgida tarbitud aega ja kogust.</span><span class="sxs-lookup"><span data-stu-id="f854d-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="f854d-120">Protsessi kaardid</span><span class="sxs-lookup"><span data-stu-id="f854d-120">Route cards</span></span>

<span data-ttu-id="f854d-121">Protsessikaart annab ülevaate teabest, mis on pärit protsessi ja operatsiooni seadistustest ning operatsiooni ja töö planeerimise meetoditest.</span><span class="sxs-lookup"><span data-stu-id="f854d-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="f854d-122">Protsessi tööd</span><span class="sxs-lookup"><span data-stu-id="f854d-122">Route jobs</span></span>

<span data-ttu-id="f854d-123">Protsessitöö loetleb kõik operatsiooni tööd üksikasjalikult ning hõlmab seadistus-, protsessi-, järjekorra- ja transpordiaegu.</span><span class="sxs-lookup"><span data-stu-id="f854d-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="f854d-124">Näiteks võib selline operatsioon nagu värvimine vajada eraldi töid, nagu seadistusaeg, käitusaeg (värvimisprotsessi jaoks) ja järjekorraaeg (kuivamiseks).</span><span class="sxs-lookup"><span data-stu-id="f854d-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="f854d-125">Töökaardid</span><span class="sxs-lookup"><span data-stu-id="f854d-125">Job cards</span></span>

<span data-ttu-id="f854d-126">Töökaart loetleb konkreetse operatsiooni üksiktööde numbrid.</span><span class="sxs-lookup"><span data-stu-id="f854d-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="f854d-127">Igal lehel kuvatakse üks töö.</span><span class="sxs-lookup"><span data-stu-id="f854d-127">One job appears on each page.</span></span> <span data-ttu-id="f854d-128">Töökaardile kaasatud tööd ja nende nende prognoositavad ajad on pärit protsessi ja operatsiooni seadistusteabest.</span><span class="sxs-lookup"><span data-stu-id="f854d-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="f854d-129">Töökaardilt saate avada lehe **Tootmise töölehe read**, **töökaart**.</span><span class="sxs-lookup"><span data-stu-id="f854d-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="f854d-130">Operatsiooniressursse käitavad inimesed saavad tootmisprotsessi kohta tagasisidet anda.</span><span class="sxs-lookup"><span data-stu-id="f854d-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="f854d-131">On olemas väljad, kuhu saate sisestada tarbimisstatistika ja teabe, nt tõrgete koguse.</span><span class="sxs-lookup"><span data-stu-id="f854d-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="f854d-132">Laotöö materjali komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="f854d-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="f854d-133">Töö toormaterjalide komplekteerimiseks luuakse väljastamise ajal.</span><span class="sxs-lookup"><span data-stu-id="f854d-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="f854d-134">Töö luuakse ainult enne tellimuse väljastamist tootmistellimuse jaoks füüsiliselt reserveeritud materjalide koguse kohta.</span><span class="sxs-lookup"><span data-stu-id="f854d-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="f854d-135">Toormaterjalide komplekteerimise jaoks laotöö loomiseks on nõutav järgmine seadistus.</span><span class="sxs-lookup"><span data-stu-id="f854d-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="f854d-136">Asukohakorraldus toormaterjalide komplekteerimiseks, mis määratleb, millisesse lao asukohta tuleb materjalid komplekteerida</span><span class="sxs-lookup"><span data-stu-id="f854d-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="f854d-137">Voomall toormaterjalide kohta, kus on konfigureeritud laotöö käivitamise poliitikad</span><span class="sxs-lookup"><span data-stu-id="f854d-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="f854d-138">Tootmise sisendasukoht, mis määratleb, kuhu materjalid pannakse</span><span class="sxs-lookup"><span data-stu-id="f854d-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="f854d-139">Litsentsiplaadiga kontrollitud asukohtade kasutamisel saate valida, kas toormaterjali komplekteerimistöö töötlemisel tuleb komplektida tellitud kogus või kauba kogu saadaolev kogus.</span><span class="sxs-lookup"><span data-stu-id="f854d-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="f854d-140">Selle suvandi määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f854d-140">To set this option:</span></span>

1. <span data-ttu-id="f854d-141">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted** ja avage asjakohane kaup.</span><span class="sxs-lookup"><span data-stu-id="f854d-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="f854d-142">Laiendage kiirkaarti **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="f854d-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="f854d-143">Valige väljale **Materjali komplekteerimine litsentsiplaadi asukohtades** üks järgmistest suvanditest.</span><span class="sxs-lookup"><span data-stu-id="f854d-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="f854d-144">*Tellimuse komplekteerimine*: komplekteerida tuleb ainult tellitud kogus.</span><span class="sxs-lookup"><span data-stu-id="f854d-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="f854d-145">*Koondamine*: võimalusel tuleb komplekteerida litsentsiplaadil saadaolev täielik kogus.</span><span class="sxs-lookup"><span data-stu-id="f854d-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="f854d-146">Selleks, et töötaja saaks komplekteerida litsentsiplaadi täiskoguse, ei tohi litsentsiplaat sisaldada segakaupu ja sellel ei tohi olla segadimensioone.</span><span class="sxs-lookup"><span data-stu-id="f854d-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="f854d-147">Kui litsentsiplaat sisaldab segadimensioone või segakaupu, jätkub komplekteerimine nii, nagu määrang oleks *Tellimuse komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="f854d-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]