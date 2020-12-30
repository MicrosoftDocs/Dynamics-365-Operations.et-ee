---
title: Küsimustike tulemuste vaatamine ja hindamine
description: See artikkel selgitab, kuidas saate vaadata ja hinnata vastajate täidetavate küsimustike tulemusi.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: ceb21af75dca2756d8e07f315ddee0246554c854
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418213"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="a4f23-103">Küsimustike tulemuste vaatamine ja hindamine</span><span class="sxs-lookup"><span data-stu-id="a4f23-103">View and evaluate the results of questionnaires</span></span>

<span data-ttu-id="a4f23-104">See artikkel selgitab, kuidas saate vaadata ja hinnata vastajate täidetavate küsimustike tulemusi.</span><span class="sxs-lookup"><span data-stu-id="a4f23-104">This article explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="a4f23-105">Pärast seda, kui vastajad on küsimustiku täitnud, saate vaadata ja hinnata küsimustiku tulemusi järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="a4f23-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="a4f23-106">**Täidetud vastamissessioonid** – saate kuvada vastajate täidetud küsimustike üksikasjad ja koostada aruandeid vastuste ning teenitud punktide summeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="a4f23-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="a4f23-107">**Tulemusegrupid** – saate kuvada tulemusegrupi üksikasjad ja küsimustike statistika.</span><span class="sxs-lookup"><span data-stu-id="a4f23-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="a4f23-108">Tulemusegrupi statistika saab luua ühe küsimustiku vastamissessiooni või kõigi vastamissessioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="a4f23-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="a4f23-109">**Küsimustiku statistika** – saate määrata kriteeriumid konkreetse vastajagrupi statistika arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="a4f23-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="a4f23-110">Samuti saate luua mitmesuguseid aruandeid inimese, vastamissessiooni või tulemusegrupi järgi sorditud tulemuste vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="a4f23-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="a4f23-111">Saadaval on järgmised täidetud küsimustikega seotud aruanded.</span><span class="sxs-lookup"><span data-stu-id="a4f23-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="a4f23-112">Vastused</span><span class="sxs-lookup"><span data-stu-id="a4f23-112">Answers</span></span>
-   <span data-ttu-id="a4f23-113">Vastused küsimustiku kohta</span><span class="sxs-lookup"><span data-stu-id="a4f23-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="a4f23-114">Vastused isiku kohta</span><span class="sxs-lookup"><span data-stu-id="a4f23-114">Answers per person</span></span>
-   <span data-ttu-id="a4f23-115">Tagasiside analüüs</span><span class="sxs-lookup"><span data-stu-id="a4f23-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="a4f23-116">Vastamissessiooni tulemused</span><span class="sxs-lookup"><span data-stu-id="a4f23-116">Answer session results</span></span>

<span data-ttu-id="a4f23-117">Pärast seda, kui vastajad on küsimustiku täitnud, saate vaadata täidetud vastamissessioonide tulemusi.</span><span class="sxs-lookup"><span data-stu-id="a4f23-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="a4f23-118">Vastamissessioon on ühe kasutaja vastus küsimustikule.</span><span class="sxs-lookup"><span data-stu-id="a4f23-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="a4f23-119">Täidetud vastamissessioonide üksikasju saab vaadata lehel **Vastused**.</span><span class="sxs-lookup"><span data-stu-id="a4f23-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="a4f23-120">Lehel **Vastused** olevaid vastamissessioone filtreeritakse mitmesugusel viisil, olenevalt sellest, kuidas lehe avate.</span><span class="sxs-lookup"><span data-stu-id="a4f23-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="a4f23-121">Kõik küsimustikud</span><span class="sxs-lookup"><span data-stu-id="a4f23-121">All questionnaires</span></span>
-   <span data-ttu-id="a4f23-122">Konkreetne küsimustik</span><span class="sxs-lookup"><span data-stu-id="a4f23-122">A specific questionnaire</span></span>
-   <span data-ttu-id="a4f23-123">Kindel isik</span><span class="sxs-lookup"><span data-stu-id="a4f23-123">A specific person</span></span>

<span data-ttu-id="a4f23-124">Lehelt **Vastused** saate vaadata vastuste üksikasju, teenitud punkte, vastaja vastuseid igas tulemusegrupis ja küsimuste hierarhiat, mida valitud küsimustikus kasutati, kui küsimuste hierarhiat kasutati.</span><span class="sxs-lookup"><span data-stu-id="a4f23-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="a4f23-125">Võimalik on koostada ja printida ka järgmisi aruandeid.</span><span class="sxs-lookup"><span data-stu-id="a4f23-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="a4f23-126">**Tulemuste aruanne** – see aruanne kuvab graafiliselt valitud vastamissessiooni puhul tulemusegrupi kohta teenitud punktid.</span><span class="sxs-lookup"><span data-stu-id="a4f23-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="a4f23-127">**Vastuste aruanne** – see aruanne kuvab vastused, mille vastaja iga küsimuse puhul küsimustikust valis.</span><span class="sxs-lookup"><span data-stu-id="a4f23-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="a4f23-128">**Valed vastused** – see aruanne kuvab vastaja valitud valede vastustega seotud teabe.</span><span class="sxs-lookup"><span data-stu-id="a4f23-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

> [!NOTE]
> <span data-ttu-id="a4f23-129">Aruanne **Tulemused** on saadaval ainult juhul, kui kasutate küsimustikus tulemusegruppe ja tegite valiku lehel **Küsimustikud** valiku **Tulemuste leht**.</span><span class="sxs-lookup"><span data-stu-id="a4f23-129">The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="a4f23-130">Aruanne **Vastus** ja aruanne **Valed vastused** on saadaval ainult juhul, kui tegite valiku **Vastuste aruanne** lehel **Küsimustikud**.</span><span class="sxs-lookup"><span data-stu-id="a4f23-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="a4f23-131">Küsimustiku statistika</span><span class="sxs-lookup"><span data-stu-id="a4f23-131">Questionnaire statistics</span></span>

<span data-ttu-id="a4f23-132">Saate kasutada küsimustiku statistikat täidetud küsimustiku tulemuste analüüsimiseks, tuginedes teie määratletud arvutustele.</span><span class="sxs-lookup"><span data-stu-id="a4f23-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="a4f23-133">Arvutuste määratlemiseks peate täitma järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="a4f23-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="a4f23-134">Valige statistika arvutamise ja kuvamise kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="a4f23-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="a4f23-135">Saate kuvada statistika küsimustiku, küsimuste, küsimuseridade või tulemusegruppide kaupa.</span><span class="sxs-lookup"><span data-stu-id="a4f23-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="a4f23-136">Valige diagrammi tüüp, mida tulemuste kuvamisel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="a4f23-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="a4f23-137">Valige võrgust inimeste tüübid (nt töötajad, kontaktisikud või kandidaadid), kelle vastuseid arvestada.</span><span class="sxs-lookup"><span data-stu-id="a4f23-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="a4f23-138">Võite arvestada ka anonüümselt täidetud küsimustike vastuseid.</span><span class="sxs-lookup"><span data-stu-id="a4f23-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="a4f23-139">Saate seadistada tulemuste analüüsimiseks vanusel või staažil põhinevaid intervalle.</span><span class="sxs-lookup"><span data-stu-id="a4f23-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="a4f23-140">Saate valida või kontrollida statistikateema kitsendamise sätteid.</span><span class="sxs-lookup"><span data-stu-id="a4f23-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="a4f23-141">Näiteks sihtnumbri valimisel saate analüüsida selle geograafilise piirkonna kõigi vastajate tulemusi.</span><span class="sxs-lookup"><span data-stu-id="a4f23-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="a4f23-142">Valige või kinnitage kriteeriumid tulemuste analüüsimiseks vastaja või küsimustiku omaduste põhjal.</span><span class="sxs-lookup"><span data-stu-id="a4f23-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="a4f23-143">Näiteks kui teete valiku **Sihtnumber**, saate analüüsida vastaja asukoha ja õigete vastuste seost.</span><span class="sxs-lookup"><span data-stu-id="a4f23-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="a4f23-144">Teie määratud seaded salvestatakse ja saate neid tulemuste ümberarvutamiseks regulaarselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="a4f23-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>