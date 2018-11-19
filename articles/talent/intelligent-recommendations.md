---
title: Intelligentsed soovitused
description: "Selles teemas kirjeldatakse, kuidas masinõppe abil töökohtadele ja töökoha kandidaatidele soovitusi anda."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.contentlocale: et-ee
ms.lasthandoff: 11/12/2018

---

# <a name="intelligent-recommendations"></a><span data-ttu-id="593fb-103">Intelligentsed soovitused</span><span class="sxs-lookup"><span data-stu-id="593fb-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="593fb-104">Masinõpe võib aidata värbajatel ja värbamisjuhtidel kiiresti tuvastada ametikoha parimad kandidaadid.</span><span class="sxs-lookup"><span data-stu-id="593fb-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="593fb-105">Samuti võib see aidata potentsiaalsetel tööotsijatel leida ametikoha, mis sobib kõige paremini nende profiili ja huvidega.</span><span class="sxs-lookup"><span data-stu-id="593fb-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="593fb-106">Nende funktsioonide kasutamisel ja tagasiside andmisel soovitused täiustuvad.</span><span class="sxs-lookup"><span data-stu-id="593fb-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="593fb-107">Intelligentse soovituse funktsioon on saadaval ainult tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="593fb-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="593fb-108">Kandidaadi ja töökoha soovitusfunktsioonide lubamiseks peab administraator nende jaoks eelvaatesuvandid sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="593fb-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="593fb-109">Veenduge Halduskeskuse **Funktsiooni halduse** vahekaardil, et **Eelvaate funktsioonide** suvand oleks määratud olekusse **Sees**.</span><span class="sxs-lookup"><span data-stu-id="593fb-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="593fb-110">Seejärel veenduge, et individuaalsed **Kandidaadi soovitamise** ja **Töökoha soovitamise** suvandid oleks määratus olekusse **Sees**.</span><span class="sxs-lookup"><span data-stu-id="593fb-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="593fb-111">Kandidaadisoovitused</span><span class="sxs-lookup"><span data-stu-id="593fb-111">Candidate recommendations</span></span>

<span data-ttu-id="593fb-112">Kuna töösisestused võivad meelitada sadu kandidaate, võib värbajatel ja värbamisjuhtidel olla keeruline leida kandidaate, kelle oskused ja taust ametikohale kõige paremini vastaksid.</span><span class="sxs-lookup"><span data-stu-id="593fb-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="593fb-113">Analüüsides töö kirjelduse ja nõuete ning kandidaatide elulookirjelduste ja profiilide andmete vahelist korrelatsiooni, võib masinõpet kasutada kandidaadisoovituste koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="593fb-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="593fb-114">Kandidaadisoovitused võivad aidata värbajatel ja värbamisjuhtidel tipptalente tuvastada ning neid kiiremini vestluse etappi viia.</span><span class="sxs-lookup"><span data-stu-id="593fb-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="593fb-115">Iga töö puhul, millel on rohkem kui kümme kandidaati või potentsiaalset tööotsijat, kellel on elulookirjeldused ja täidetud profiilid, ilmuvad kandidaadid või potentsiaalsed tööotsijad, kes vastavad kõige paremini töö nõutele, jaotisesse **Kandidaadid, keda kaaluda**, **Töö** lehel.</span><span class="sxs-lookup"><span data-stu-id="593fb-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="593fb-116">Iga soovitatud kandidaadi kohta saate kandidaadi profiili ülevaatamiseks ja tema avalduse suhtes meetmete rakendamiseks valida kandidaadi kaardilt **Kuva kandidaat**.</span><span class="sxs-lookup"><span data-stu-id="593fb-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="593fb-117">Kandidaadi profiili avamiseks uuel vahekaardil võite kasutada kolmikpunkti nuppu (**...**). Kolmikpunkti nuppu saate kasutada ka soovituse kohta tagasiside andmiseks.</span><span class="sxs-lookup"><span data-stu-id="593fb-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="593fb-118">Sel viisil saate aidata soovitusmootorit peenhäälestada ja tulevasi soovitusi täiustada.</span><span class="sxs-lookup"><span data-stu-id="593fb-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="593fb-119">Kõik soovitused, mis teile ei meeldi, eemaldatakse **Kandidaadid, keda kaaluda** jaotisest pärast **Töö** lehe värskendamist.</span><span class="sxs-lookup"><span data-stu-id="593fb-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="593fb-120">Saate tagasiside kaardi abil viidata, miks te soovitust kasulikuks ei pidanud.</span><span class="sxs-lookup"><span data-stu-id="593fb-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="593fb-121">Töösoovitused</span><span class="sxs-lookup"><span data-stu-id="593fb-121">Job recommendations</span></span> 

<span data-ttu-id="593fb-122">Kui potentsiaalne töövõtja kasutab karjäärisaiti tööle kandideerimiseks, soovitatakse talle ka organisatsiooni teisi vabasid ametikohti.</span><span class="sxs-lookup"><span data-stu-id="593fb-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="593fb-123">Need soovitused põhinevad potentsiaalse töövõtja varasematel avadustel ja tema elulool või kandidaadi profiilil.</span><span class="sxs-lookup"><span data-stu-id="593fb-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="593fb-124">Seega aitavad töösoovitused potentsiaalsetel töövõtjatel kiiresti tuvastada neile sobivaimad tööd.</span><span class="sxs-lookup"><span data-stu-id="593fb-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="593fb-125">Potentsiaalsetele töövõtjatele pakutakse töösoovitusi, kui karjäärisaidile sisestatakse rohkem kui kümme tööd.</span><span class="sxs-lookup"><span data-stu-id="593fb-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="593fb-126">Potentsiaalsed töövõtjad saavad töösisestuse üksikasju vaadata soovituse kaardilt.</span><span class="sxs-lookup"><span data-stu-id="593fb-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="593fb-127">Nad saavad soovituste kohta ka tagasisidet anda, et tulevasi soovitusi täiustada aidata.</span><span class="sxs-lookup"><span data-stu-id="593fb-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>

