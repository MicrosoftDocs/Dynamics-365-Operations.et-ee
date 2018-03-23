---
title: "Saate küsimustiku tulemusi vaadata ja hinnata"
description: "See teema selgitab, kuidas saate vaadata ja hinnata vastajate täidetavate küsimustike tulemusi."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 7ae83192924a790451d8da511638c7fc1cd92f90
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a><span data-ttu-id="6c21d-103">Saate küsimustiku tulemusi vaadata ja hinnata</span><span class="sxs-lookup"><span data-stu-id="6c21d-103">View and evaluate the results of a questionnaire</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="6c21d-104">See teema selgitab, kuidas saate vaadata ja hinnata vastajate täidetavate küsimustike tulemusi.</span><span class="sxs-lookup"><span data-stu-id="6c21d-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="6c21d-105">Pärast seda, kui vastajad on küsimustiku täitnud, saate vaadata ja hinnata küsimustiku tulemusi järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="6c21d-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="6c21d-106">**Täidetud vastamissessioonid** – saate kuvada vastajate täidetud küsimustike üksikasjad ja koostada aruandeid vastuste ning teenitud punktide summeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6c21d-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="6c21d-107">**Tulemusegrupid** – saate kuvada tulemusegrupi üksikasjad ja küsimustike statistika.</span><span class="sxs-lookup"><span data-stu-id="6c21d-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="6c21d-108">Tulemusegrupi statistika saab luua ühe küsimustiku vastamissessiooni või kõigi vastamissessioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="6c21d-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="6c21d-109">**Küsimustiku statistika** – saate määrata kriteeriumid konkreetse vastajagrupi statistika arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="6c21d-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="6c21d-110">Samuti saate luua mitmesuguseid aruandeid inimese, vastamissessiooni või tulemusegrupi järgi sorditud tulemuste vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="6c21d-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="6c21d-111">Saadaval on järgmised täidetud küsimustikega seotud aruanded.</span><span class="sxs-lookup"><span data-stu-id="6c21d-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="6c21d-112">Vastused</span><span class="sxs-lookup"><span data-stu-id="6c21d-112">Answers</span></span>
-   <span data-ttu-id="6c21d-113">Vastused küsimustiku kohta</span><span class="sxs-lookup"><span data-stu-id="6c21d-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="6c21d-114">Vastused isiku kohta</span><span class="sxs-lookup"><span data-stu-id="6c21d-114">Answers per person</span></span>
-   <span data-ttu-id="6c21d-115">Tagasiside analüüs</span><span class="sxs-lookup"><span data-stu-id="6c21d-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="6c21d-116">Vastamissessiooni tulemused</span><span class="sxs-lookup"><span data-stu-id="6c21d-116">Answer session results</span></span>
<span data-ttu-id="6c21d-117">Pärast seda, kui vastajad on küsimustiku täitnud, saate vaadata täidetud vastamissessioonide tulemusi.</span><span class="sxs-lookup"><span data-stu-id="6c21d-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="6c21d-118">Vastamissessioon on ühe kasutaja vastus küsimustikule.</span><span class="sxs-lookup"><span data-stu-id="6c21d-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="6c21d-119">Täidetud vastamissessioonide üksikasju saab vaadata lehel **Vastused**.</span><span class="sxs-lookup"><span data-stu-id="6c21d-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="6c21d-120">Lehel **Vastused** olevaid vastamissessioone filtreeritakse mitmesugusel viisil, olenevalt sellest, kuidas lehe avate.</span><span class="sxs-lookup"><span data-stu-id="6c21d-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="6c21d-121">Kõik küsimustikud</span><span class="sxs-lookup"><span data-stu-id="6c21d-121">All questionnaires</span></span>
-   <span data-ttu-id="6c21d-122">Konkreetne küsimustik</span><span class="sxs-lookup"><span data-stu-id="6c21d-122">A specific questionnaire</span></span>
-   <span data-ttu-id="6c21d-123">Kindel isik</span><span class="sxs-lookup"><span data-stu-id="6c21d-123">A specific person</span></span>

<span data-ttu-id="6c21d-124">Lehelt **Vastused** saate vaadata vastuste üksikasju, teenitud punkte, vastaja vastuseid igas tulemusegrupis ja küsimuste hierarhiat, mida valitud küsimustikus kasutati, kui küsimuste hierarhiat kasutati.</span><span class="sxs-lookup"><span data-stu-id="6c21d-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="6c21d-125">Võimalik on koostada ja printida ka järgmisi aruandeid.</span><span class="sxs-lookup"><span data-stu-id="6c21d-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="6c21d-126">**Tulemuste aruanne** – see aruanne kuvab graafiliselt valitud vastamissessiooni puhul tulemusegrupi kohta teenitud punktid.</span><span class="sxs-lookup"><span data-stu-id="6c21d-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="6c21d-127">**Vastuste aruanne** – see aruanne kuvab vastused, mille vastaja iga küsimuse puhul küsimustikust valis.</span><span class="sxs-lookup"><span data-stu-id="6c21d-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="6c21d-128">**Valed vastused** – see aruanne kuvab vastaja valitud valede vastustega seotud teabe.</span><span class="sxs-lookup"><span data-stu-id="6c21d-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="6c21d-129">**Märkus.** Aruanne **Tulemused** on saadaval ainult juhul, kui kasutate küsimustikus tulemusegruppe ja tegite valiku lehel **Küsimustikud** valiku **Tulemuste leht**.</span><span class="sxs-lookup"><span data-stu-id="6c21d-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="6c21d-130">Aruanne **Vastus** ja aruanne **Valed vastused** on saadaval ainult juhul, kui tegite valiku **Vastuste aruanne** lehel **Küsimustikud**.</span><span class="sxs-lookup"><span data-stu-id="6c21d-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="6c21d-131">Küsimustiku statistika</span><span class="sxs-lookup"><span data-stu-id="6c21d-131">Questionnaire statistics</span></span>
<span data-ttu-id="6c21d-132">Saate kasutada küsimustiku statistikat täidetud küsimustiku tulemuste analüüsimiseks, tuginedes teie määratletud arvutustele.</span><span class="sxs-lookup"><span data-stu-id="6c21d-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="6c21d-133">Arvutuste määratlemiseks peate täitma järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="6c21d-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="6c21d-134">Valige statistika arvutamise ja kuvamise kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="6c21d-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="6c21d-135">Saate kuvada statistika küsimustiku, küsimuste, küsimuseridade või tulemusegruppide kaupa.</span><span class="sxs-lookup"><span data-stu-id="6c21d-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="6c21d-136">Valige diagrammi tüüp, mida tulemuste kuvamisel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="6c21d-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="6c21d-137">Valige võrgust inimeste tüübid (nt töötajad, kontaktisikud või kandidaadid), kelle vastuseid arvestada.</span><span class="sxs-lookup"><span data-stu-id="6c21d-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="6c21d-138">Võite arvestada ka anonüümselt täidetud küsimustike vastuseid.</span><span class="sxs-lookup"><span data-stu-id="6c21d-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="6c21d-139">Saate seadistada tulemuste analüüsimiseks vanusel või staažil põhinevaid intervalle.</span><span class="sxs-lookup"><span data-stu-id="6c21d-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="6c21d-140">Saate valida või kontrollida statistikateema kitsendamise sätteid.</span><span class="sxs-lookup"><span data-stu-id="6c21d-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="6c21d-141">Näiteks sihtnumbri valimisel saate analüüsida selle geograafilise piirkonna kõigi vastajate tulemusi.</span><span class="sxs-lookup"><span data-stu-id="6c21d-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="6c21d-142">Valige või kinnitage kriteeriumid tulemuste analüüsimiseks vastaja või küsimustiku omaduste põhjal.</span><span class="sxs-lookup"><span data-stu-id="6c21d-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="6c21d-143">Näiteks kui teete valiku **Sihtnumber**, saate analüüsida vastaja asukoha ja õigete vastuste seost.</span><span class="sxs-lookup"><span data-stu-id="6c21d-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="6c21d-144">Teie määratud seaded salvestatakse ja saate neid tulemuste ümberarvutamiseks regulaarselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="6c21d-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="see-also"></a><span data-ttu-id="6c21d-145">Vt ka</span><span class="sxs-lookup"><span data-stu-id="6c21d-145">See also</span></span>
--------

[<span data-ttu-id="6c21d-146">Küsimustike kavandamine</span><span class="sxs-lookup"><span data-stu-id="6c21d-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="6c21d-147">Küsimustike kasutamine</span><span class="sxs-lookup"><span data-stu-id="6c21d-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="6c21d-148">Küsimustike laialisaatmine ja täitmine</span><span class="sxs-lookup"><span data-stu-id="6c21d-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)


