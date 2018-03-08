---
title: "Küsimustiku kujundamine"
description: "See teema kirjeldab küsimustiku koostamise protsessi. Esimene samm on küsimustiku kavandamine. Küsimustiku kavandamisel ei kirjutata ainult küsimusi ja vastuseid, vaid luuakse ka struktuur, mis võimaldab vastuste salvestamise ja tabelisse paigutamise."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 506c4db7cd37fd85b3e132e7900eafdc4385fa5a
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---

# <a name="design-a-questionnaire"></a><span data-ttu-id="b8265-105">Küsimustiku kujundamine</span><span class="sxs-lookup"><span data-stu-id="b8265-105">Design a questionnaire</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="b8265-106">See teema kirjeldab küsimustiku koostamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="b8265-106">This topic describes the process for creating a questionnaire.</span></span> <span data-ttu-id="b8265-107">Esimene samm on küsimustiku kavandamine.</span><span class="sxs-lookup"><span data-stu-id="b8265-107">The first step is to design the questionnaire.</span></span> <span data-ttu-id="b8265-108">Küsimustiku kavandamisel ei kirjutata ainult küsimusi ja vastuseid, vaid luuakse ka struktuur, mis võimaldab vastuste salvestamise ja tabelisse paigutamise.</span><span class="sxs-lookup"><span data-stu-id="b8265-108">When you design a questionnaire, you not only write the questions and answers, but also create the structure that enables answers to be recorded and tabulated.</span></span> 

<span data-ttu-id="b8265-109">Hoolikalt koostatud küsimustik võib aidata tõsta kogutavate andmete kvaliteeti.</span><span class="sxs-lookup"><span data-stu-id="b8265-109">A carefully designed questionnaire can help increase the quality of the data that you collect.</span></span> <span data-ttu-id="b8265-110">Hoolika kavandamise kaudu saate küsimustiku jaoks sobival ajal paremini sobivaid võimalusi valida.</span><span class="sxs-lookup"><span data-stu-id="b8265-110">Through careful design, you can better select the appropriate options at the appropriate time for a questionnaire.</span></span> <span data-ttu-id="b8265-111">Järgmised punktid aitavad tulemuslikku küsimustikku kavandada.</span><span class="sxs-lookup"><span data-stu-id="b8265-111">The following points can help you plan an effective questionnaire:</span></span>

-   <span data-ttu-id="b8265-112">Määratlege selgelt küsimustiku eesmärk, et tagada küsimustega eesmärgi toetamine.</span><span class="sxs-lookup"><span data-stu-id="b8265-112">Clearly define the purpose of the questionnaire to help guarantee that the questions support the purpose.</span></span>
-   <span data-ttu-id="b8265-113">Määrake inimene või inimeste grupp, kes peaksid küsimustiku täitma.</span><span class="sxs-lookup"><span data-stu-id="b8265-113">Determine the individual person or the group of people who should complete the questionnaire.</span></span>
-   <span data-ttu-id="b8265-114">Kirjutage küsimustikus sisalduvad küsimused üles ja lisage valikvastused, kui vaja.</span><span class="sxs-lookup"><span data-stu-id="b8265-114">Write questions that will appear on the questionnaire, and include answer choices, if applicable.</span></span>
-   <span data-ttu-id="b8265-115">Veenduge, et küsimustik kulgeb loogiliselt, et vastajate huvi püsiks.</span><span class="sxs-lookup"><span data-stu-id="b8265-115">Be sure that the questionnaire flows logically, so that respondents remain engaged.</span></span>
-   <span data-ttu-id="b8265-116">Pange küsimused ja vastused vastajale esitamise järjekorda.</span><span class="sxs-lookup"><span data-stu-id="b8265-116">Arrange questions and answers in the order that they should be presented to respondents in.</span></span>
-   <span data-ttu-id="b8265-117">Otsustage vajaduse korral, kuidas tuleks tulemusi hinnata.</span><span class="sxs-lookup"><span data-stu-id="b8265-117">Decide how the results should be evaluated, if applicable.</span></span>
-   <span data-ttu-id="b8265-118">Otsustage, kas on vaja lisafunktsioone.</span><span class="sxs-lookup"><span data-stu-id="b8265-118">Decide whether you’ll need additional features.</span></span> <span data-ttu-id="b8265-119">Näiteks määrake, kas ja kuidas tuleks tulemused kategooriatesse jagada, kas on vaja ajapiirangut või kas kõik küsimused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="b8265-119">For example, determine whether and how results should be categorized, whether a time limit is required, or whether all the questions will be mandatory.</span></span>

<span data-ttu-id="b8265-120">Kavandamise faas sisaldab nelja ülesannete kategooriat, mis tuleb läbida järgmises järjekorras.</span><span class="sxs-lookup"><span data-stu-id="b8265-120">The design phase includes four categories of tasks that you must complete in this order:</span></span>

1.  <span data-ttu-id="b8265-121">Seadistage vajalikud eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="b8265-121">Set up prerequisites, as required.</span></span>
2.  <span data-ttu-id="b8265-122">Seadistage vajaduse korral vastusegrupid ja vastused.</span><span class="sxs-lookup"><span data-stu-id="b8265-122">Set up answer groups and answers, if applicable.</span></span>
3.  <span data-ttu-id="b8265-123">Seadistage küsimused ja nende seosed vastusegruppidega.</span><span class="sxs-lookup"><span data-stu-id="b8265-123">Set up questions and their association with the answer groups.</span></span>
4.  <span data-ttu-id="b8265-124">Seadistage küsimustik ja lisage sellele küsimused.</span><span class="sxs-lookup"><span data-stu-id="b8265-124">Set up the questionnaire itself, and attach questions to it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b8265-125">Eeltingimused </span><span class="sxs-lookup"><span data-stu-id="b8265-125">Prerequisites</span></span>
<span data-ttu-id="b8265-126">Mõned eeltingimused peavad olema kehtestatud enne, kui saate küsimustikke, vastuseid ja küsimusi luua.</span><span class="sxs-lookup"><span data-stu-id="b8265-126">Some prerequisites must be in place before you can create questionnaires, answers, and questions.</span></span> <span data-ttu-id="b8265-127">Kuid kõigi funktsioonide kasutamiseks pole kohustuslikud kõik eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="b8265-127">However, not all prerequisites are required for full functionality.</span></span>

### <a name="required"></a><span data-ttu-id="b8265-128">Nõutav</span><span class="sxs-lookup"><span data-stu-id="b8265-128">Required</span></span>

| <span data-ttu-id="b8265-129">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="b8265-129">Prerequisite</span></span>        | <span data-ttu-id="b8265-130">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b8265-130">Description</span></span>                |
|---------------------|----------------------------|
| <span data-ttu-id="b8265-131">Küsimustike tüübid</span><span class="sxs-lookup"><span data-stu-id="b8265-131">Questionnaire types</span></span> | <span data-ttu-id="b8265-132">Saate küsimustikud kategooriatesse jagada.</span><span class="sxs-lookup"><span data-stu-id="b8265-132">Categorize questionnaires.</span></span> |
| <span data-ttu-id="b8265-133">Küsimuste tüübid</span><span class="sxs-lookup"><span data-stu-id="b8265-133">Question types</span></span>      | <span data-ttu-id="b8265-134">Saate küsimused kategooriatesse jagada.</span><span class="sxs-lookup"><span data-stu-id="b8265-134">Categorize questions.</span></span>      |

### <a name="optional"></a><span data-ttu-id="b8265-135">Valikuline</span><span class="sxs-lookup"><span data-stu-id="b8265-135">Optional</span></span>

| <span data-ttu-id="b8265-136">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="b8265-136">Prerequisite</span></span>             | <span data-ttu-id="b8265-137">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b8265-137">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b8265-138">Küsimustiku parameetrid</span><span class="sxs-lookup"><span data-stu-id="b8265-138">Questionnaire parameters</span></span> | <span data-ttu-id="b8265-139">Saate muuta küsimustike peamisi juhtelemente ja vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="b8265-139">Modify basic controls and default settings for questionnaires.</span></span> |

### <a name="questionnaire-types"></a><span data-ttu-id="b8265-140">Küsimustike tüübid</span><span class="sxs-lookup"><span data-stu-id="b8265-140">Questionnaire types</span></span>

<span data-ttu-id="b8265-141">Küsimustike tüübid on kohustuslikud ja need tuleb määrata küsimustiku koostamisel.</span><span class="sxs-lookup"><span data-stu-id="b8265-141">Questionnaire types are required and must be assigned when you create a questionnaire.</span></span> <span data-ttu-id="b8265-142">Küsimustike tüübid aitavad küsimustikke hõlpsamini hallata ja klassifitseerida.</span><span class="sxs-lookup"><span data-stu-id="b8265-142">Questionnaire types help you manage and classify questionnaires more easily.</span></span> <span data-ttu-id="b8265-143">Kasutage küsimustike tüüpe küsimustike klassifitseerimiseks ja üksteisest eristamiseks.</span><span class="sxs-lookup"><span data-stu-id="b8265-143">Use questionnaire types to classify questionnaires and differentiate them from each other.</span></span> <span data-ttu-id="b8265-144">Näiteks kui teil on mitu küsimustikku, mille vahel valida, võite neid tüübi järgi filtreerida, et konkreetset küsimustikku oleks lihtsam leida.</span><span class="sxs-lookup"><span data-stu-id="b8265-144">For example, if you have multiple questionnaires to select from, you can filter them by type to help make it easier to find a particular questionnaire.</span></span> <span data-ttu-id="b8265-145">Siin on mõned näited küsimustike tüüpide kohta.</span><span class="sxs-lookup"><span data-stu-id="b8265-145">Here are some examples of questionnaire types:</span></span>

-   <span data-ttu-id="b8265-146">inimressursside areng,</span><span class="sxs-lookup"><span data-stu-id="b8265-146">Human resource development</span></span>
-   <span data-ttu-id="b8265-147">kliendiülevaated,</span><span class="sxs-lookup"><span data-stu-id="b8265-147">Customer surveys</span></span>
-   <span data-ttu-id="b8265-148">Protsessi ülevaade</span><span class="sxs-lookup"><span data-stu-id="b8265-148">Review process</span></span>

### <a name="question-types"></a><span data-ttu-id="b8265-149">Küsimuste tüübid</span><span class="sxs-lookup"><span data-stu-id="b8265-149">Question types</span></span>

<span data-ttu-id="b8265-150">Küsimuse tüübid on kohustuslikud ja need tuleb määrata küsimuse koostamisel.</span><span class="sxs-lookup"><span data-stu-id="b8265-150">Question types are required and must be assigned when you create a question.</span></span> 

<span data-ttu-id="b8265-151">Saate kasutada küsimuste tüüpe aruandluse eesmärgil küsimuste kategoriseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b8265-151">Use question types to categorize questions for reporting.</span></span> <span data-ttu-id="b8265-152">Küsimuste tüübid muudavad ka küsimuste leidmise lihtsamaks, kuna saate tüüpe lehel **Küsimused** filtritena kasutada.</span><span class="sxs-lookup"><span data-stu-id="b8265-152">Question types also make it easier to find questions, because you can use types as filters on the **Questions** page.</span></span> <span data-ttu-id="b8265-153">Siin on mõned näited küsimuste tüüpide kohta.</span><span class="sxs-lookup"><span data-stu-id="b8265-153">Here are some examples of question types:</span></span>

-   <span data-ttu-id="b8265-154">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="b8265-154">Human resource</span></span>
-   <span data-ttu-id="b8265-155">Ärijuhtimine</span><span class="sxs-lookup"><span data-stu-id="b8265-155">Managing business</span></span>
-   <span data-ttu-id="b8265-156">Kursuse hindamine</span><span class="sxs-lookup"><span data-stu-id="b8265-156">Course evaluation</span></span>

### <a name="questionnaire-parameters"></a><span data-ttu-id="b8265-157">Küsimustiku parameetrid</span><span class="sxs-lookup"><span data-stu-id="b8265-157">Questionnaire parameters</span></span>

<span data-ttu-id="b8265-158">Küsimustiku parameetrid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="b8265-158">Questionnaire parameters are optional.</span></span> <span data-ttu-id="b8265-159">Te ei pruugi neid kasutada, olenevalt teie ettevõtte vajadustest.</span><span class="sxs-lookup"><span data-stu-id="b8265-159">You might not use them, depending on your company’s requirements.</span></span> 

<span data-ttu-id="b8265-160">Küsimustiku parameetrid määratlevad küsimustiku anonüümsuse, numbriseeriakoodid ja viitetüübid.</span><span class="sxs-lookup"><span data-stu-id="b8265-160">Questionnaire parameters define the anonymity, number sequence codes, and reference types of a questionnaire.</span></span> <span data-ttu-id="b8265-161">Kui organisatsioon küsimustiku laiali saadab, võib olla vaja võimaldada kasutajatel anonüümseks jääda.</span><span class="sxs-lookup"><span data-stu-id="b8265-161">When an organization distributes a questionnaire, the option to allow respondents to remain anonymous might be of concern.</span></span> 

<span data-ttu-id="b8265-162">Küsimuste ja vastuste korraldamiseks kasutatakse numbriseeriakoode.</span><span class="sxs-lookup"><span data-stu-id="b8265-162">The number sequence codes are used to organize questions and answers.</span></span> <span data-ttu-id="b8265-163">Nende numbriseeriakoodide põhjal määratakse kaupadele automaatselt väärtused.</span><span class="sxs-lookup"><span data-stu-id="b8265-163">Based on these number sequence codes, values are automatically assigned to items.</span></span> 

<span data-ttu-id="b8265-164">Kõik parameetrid tuleks määratleda enne andmete loomise alustamist.</span><span class="sxs-lookup"><span data-stu-id="b8265-164">You should define all parameters before you begin to create your data.</span></span> <span data-ttu-id="b8265-165">Küsimustiku parameetri sätteid saab igal ajal muuta.</span><span class="sxs-lookup"><span data-stu-id="b8265-165">You can modify the questionnaire parameter settings at any time.</span></span>

## <a name="questionnaire-components"></a><span data-ttu-id="b8265-166">Küsimustiku osad</span><span class="sxs-lookup"><span data-stu-id="b8265-166">Questionnaire components</span></span>
<span data-ttu-id="b8265-167">Küsimustikud hõlmavad kolme põhielementi: vastusegruppe, mis sisaldavad valikvastustega küsimuste vastuseid, küsimusi ja küsimustikku ennast.</span><span class="sxs-lookup"><span data-stu-id="b8265-167">Questionnaires comprise three main elements: answer groups that contain the answers for multiple choice questions, questions, and the questionnaire itself.</span></span> <span data-ttu-id="b8265-168">Soovi korral saab küsimustiku küsimused tulemusegruppidesse jagada.</span><span class="sxs-lookup"><span data-stu-id="b8265-168">You can optionally group the questions on a questionnaire into result groups.</span></span> <span data-ttu-id="b8265-169">Tulemusegrupid võimaldavad küsimusi kategoriseerida ja küsimustikku edasi analüüsida.</span><span class="sxs-lookup"><span data-stu-id="b8265-169">Result groups let you categorize questions and provide further analysis on the questionnaire.</span></span> 

<span data-ttu-id="b8265-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span><span class="sxs-lookup"><span data-stu-id="b8265-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span></span>

### <a name="answer-groups-and-answers"></a><span data-ttu-id="b8265-171">Vastusegrupid ja vastused</span><span class="sxs-lookup"><span data-stu-id="b8265-171">Answer groups and answers</span></span>

<span data-ttu-id="b8265-172">Olenevalt küsimuse teemast saavad vastajad küsimustele vastata kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="b8265-172">Respondents can answer a question in two ways, depending on the subject of the question:</span></span>

-   <span data-ttu-id="b8265-173">Avatud küsimused ei vaja teatud vormis vastuseid.</span><span class="sxs-lookup"><span data-stu-id="b8265-173">Open-ended questions don’t require responses in a specific format.</span></span> <span data-ttu-id="b8265-174">Vastajad saavad tippida vastuse tekstina, numbritega, kuupäeva või kellaajana.</span><span class="sxs-lookup"><span data-stu-id="b8265-174">Respondents can type a response as text, a number, a date, or a time.</span></span> <span data-ttu-id="b8265-175">Need küsimused nõuavad vastajatelt vastustes tavaliselt subjektiivset teavet, nt arvamust, kirjeldust, hinnangut või prognoosi.</span><span class="sxs-lookup"><span data-stu-id="b8265-175">These questions typically require that the respondents provide subjective information in their answers, such as an opinion, description, evaluation, or estimate.</span></span>
-   <span data-ttu-id="b8265-176">Suletud küsimused nõuavad, et vastaja valiks vastuse võimalike õigete vastuste hulgast.</span><span class="sxs-lookup"><span data-stu-id="b8265-176">Closed-ended questions require that the respondent select an answer in a list of possible correct answers.</span></span>

<span data-ttu-id="b8265-177">Võimaliku vastuste loendi esitamiseks suletud küsimustele võite luua vastused lehel **Vastusegrupid**.</span><span class="sxs-lookup"><span data-stu-id="b8265-177">To provide a list of possible answers for closed-ended questions, you can create answers on the **Answer groups** page.</span></span> 

<span data-ttu-id="b8265-178">Vastusegrupid ja vastused on komponendid, mis moodustavad küsimuste aluseks oleva teabe põhiosa.</span><span class="sxs-lookup"><span data-stu-id="b8265-178">Answer groups and answers are components that make up the main body of information that questions are created from.</span></span> <span data-ttu-id="b8265-179">Pärast vastusegrupi loomist saate seostada selle vastusegrupi küsimusega väljal **Vastusegrupp** lehel **Küsimused**.</span><span class="sxs-lookup"><span data-stu-id="b8265-179">After you create an answer group, you can associate the answer group with a question in the **Answer group** field on the **Questions** page.</span></span> 

<span data-ttu-id="b8265-180">Vastusegruppi saab kasutada samas küsimustikus rohkem kui ühe küsimuse puhul ja ka rohkem kui ühes küsimustikus.</span><span class="sxs-lookup"><span data-stu-id="b8265-180">An answer group can be used for more than one question on the same questionnaire, and can also be used on more than one questionnaire.</span></span> 

<span data-ttu-id="b8265-181">**Märkus.** Kui muudate vastuse teksti vastusegruppides, mida on juba täidetud küsimustikes kasutatud, võib andmeid olla raske hinnata ja küsimustiku tulemused ei pruugi enam kehtida.</span><span class="sxs-lookup"><span data-stu-id="b8265-181">**Note:** If you modify answer text in answer groups that have already been used on completed questionnaires, data can become difficult to evaluate, and questionnaire results might no longer be valid.</span></span> <span data-ttu-id="b8265-182">Kui teil on vaja vastusegruppi muuta, kaaluge olemasoleva grupi muutmise asemel uue vastusegrupi loomist.</span><span class="sxs-lookup"><span data-stu-id="b8265-182">If you must change an answer group, consider creating a new answer group instead of changing an existing one.</span></span> <span data-ttu-id="b8265-183">Küsimuse või vastusega seotud või vastatud vastusegruppe ei saa kustutada.</span><span class="sxs-lookup"><span data-stu-id="b8265-183">You can't delete answer groups that are attached to a question or answer, or that have been answered.</span></span>

### <a name="questions"></a><span data-ttu-id="b8265-184">Küsimused</span><span class="sxs-lookup"><span data-stu-id="b8265-184">Questions</span></span>

<span data-ttu-id="b8265-185">Küsimustik peab sisaldama küsimusi.</span><span class="sxs-lookup"><span data-stu-id="b8265-185">A questionnaire must contain questions.</span></span> <span data-ttu-id="b8265-186">Küsimused võivad olla avatud või suletud.</span><span class="sxs-lookup"><span data-stu-id="b8265-186">Questions can be either open-ended or closed-ended.</span></span>

-   <span data-ttu-id="b8265-187">Avatud küsimuste vastuseid ei kontrollita ja vastajad saavad oma vastused tippida.</span><span class="sxs-lookup"><span data-stu-id="b8265-187">The responses to open-ended questions aren't controlled, and respondents can type their answers.</span></span>
-   <span data-ttu-id="b8265-188">Suletud küsimused nõuavad eelnevalt määratud vastusevalikute loendit ja küsimusi saab ehitada üles nii, et vastaja võib valida mitu vastust.</span><span class="sxs-lookup"><span data-stu-id="b8265-188">Closed-ended questions require a list of predefined response options, and the questions can be structured to let a respondent select multiple responses.</span></span> <span data-ttu-id="b8265-189">Küsimused tuleks kavandada nii, et nende abil saaks vastajalt konkreetset teavet, ja need tuleb siduda vastusegrupiga, mis annab igale suletud küsimusele vastusevariandid.</span><span class="sxs-lookup"><span data-stu-id="b8265-189">Questions should be designed to elicit specific information from a respondent and must be linked to an answer group that provides the response options for each closed-ended question.</span></span> 
     -  <span data-ttu-id="b8265-190">**Märkus.** enne suletud küsimuste seadistamist tuleb luua vastusegrupid ja vastused.</span><span class="sxs-lookup"><span data-stu-id="b8265-190">**Note:** Before you can set up closed-ended questions, you must create answer groups and answers.</span></span>

<span data-ttu-id="b8265-191">Küsimused saab paigutada tingimuslikku küsimuste hierarhiasse, nii et sekundaarsed küsimused sõltuvad vastusest, mille vastaja eelmisele küsimusele valib.</span><span class="sxs-lookup"><span data-stu-id="b8265-191">Questions can be arranged in a conditional question hierarchy, so that secondary questions depend on the answer that the respondent selects for the previous question.</span></span> <span data-ttu-id="b8265-192">Saate kõigepealt küsimused kirjutada ja siis need hiljem hierarhiasse paigutada.</span><span class="sxs-lookup"><span data-stu-id="b8265-192">You can write the questions first and then arrange them into a hierarchy later.</span></span>

## <a name="setting-up-questionnaires"></a><span data-ttu-id="b8265-193">Küsimustike seadistamine</span><span class="sxs-lookup"><span data-stu-id="b8265-193">Setting up questionnaires</span></span>
<span data-ttu-id="b8265-194">**Märkus.** Enne küsimustiku seadistamist peate seadistama vastused, küsimused ja eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="b8265-194">**Note:** Before you can set up a questionnaire, you must set up answers, questions, and prerequisites.</span></span> 

<span data-ttu-id="b8265-195">Iga küsimustiku jaoks saate määrata järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="b8265-195">For each questionnaire, you can specify the following information:</span></span>

-   <span data-ttu-id="b8265-196">Kohustuslikele küsimustele vastamise aeg kokku või ajapiir.</span><span class="sxs-lookup"><span data-stu-id="b8265-196">The total time or time limit to answer mandatory questions.</span></span>
-   <span data-ttu-id="b8265-197">Kas kõik küsimused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="b8265-197">Whether all questions are mandatory.</span></span>
-   <span data-ttu-id="b8265-198">Kas arvestada küsimustiku puhul punkte.</span><span class="sxs-lookup"><span data-stu-id="b8265-198">Whether to calculate points on a questionnaire.</span></span>
-   <span data-ttu-id="b8265-199">Kuidas kategoriseerida tulemusi.</span><span class="sxs-lookup"><span data-stu-id="b8265-199">How to categorize results.</span></span>
-   <span data-ttu-id="b8265-200">Kas küsimustik on saadaval piiratud vastajate grupile.</span><span class="sxs-lookup"><span data-stu-id="b8265-200">Whether the questionnaire will be available to a restricted set of respondents.</span></span>
-   <span data-ttu-id="b8265-201">Kas iga küsimustiku lehe taustana tuleks kuvada vormimall.</span><span class="sxs-lookup"><span data-stu-id="b8265-201">Whether a form template should be displayed as a background behind each page of the questionnaire.</span></span>
-   <span data-ttu-id="b8265-202">Kas on vaja lisamärkusi, et selgitada vastajatele küsimustiku eesmärki.</span><span class="sxs-lookup"><span data-stu-id="b8265-202">Whether additional notes are required in order to clarify the intent of the questionnaire for the respondents.</span></span>
-   <span data-ttu-id="b8265-203">Kas on vaja kuvada küsimused kindlas järjestuses või valida need kaustast juhuslikult.</span><span class="sxs-lookup"><span data-stu-id="b8265-203">Whether to display questions in a fixed order or randomly select them from a pool.</span></span>
-   <span data-ttu-id="b8265-204">Kas küsimusi esitatakse ainult juhul, kui eelmiste puhul anti teatud vastuseid.</span><span class="sxs-lookup"><span data-stu-id="b8265-204">Whether questions will be asked only if specific responses are given for previous answers.</span></span>

### <a name="set-up-a-questionnaire"></a><span data-ttu-id="b8265-205">Küsimustiku seadistamine</span><span class="sxs-lookup"><span data-stu-id="b8265-205">Set up a questionnaire</span></span>

<span data-ttu-id="b8265-206">Peamine leht, mida küsimustiku seadistamiseks kasutatakse, on leht **Küsimustikud**.</span><span class="sxs-lookup"><span data-stu-id="b8265-206">The primary page that you use to set up a questionnaire is the **Questionnaires** page.</span></span> <span data-ttu-id="b8265-207">Küsimustiku seadistamiseks tehke järjest järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="b8265-207">To set up a questionnaire, complete the following tasks in order:</span></span>

1.  <span data-ttu-id="b8265-208">Looge küsimustik.</span><span class="sxs-lookup"><span data-stu-id="b8265-208">Create a questionnaire.</span></span>
2.  <span data-ttu-id="b8265-209">Järgige ühte neist toimingutest küsimustikule küsimuste lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="b8265-209">Follow one of these steps to attach questions to the questionnaire:</span></span>
    -   <span data-ttu-id="b8265-210">Tulemusegruppide kasutamisel saate lisada küsimustikule küsimusi tulemusegruppide abil.</span><span class="sxs-lookup"><span data-stu-id="b8265-210">If you're using result groups, you can attach questions to a questionnaire by using result groups.</span></span> <span data-ttu-id="b8265-211">Seadistage esmalt küsimustikule tulemusegrupid ja seejärel lisage tulemusegruppidesse küsimusi.</span><span class="sxs-lookup"><span data-stu-id="b8265-211">First set up the result groups for the questionnaire, and then add questions to the result groups.</span></span>
    -   <span data-ttu-id="b8265-212">Kui te tulemusegruppe ei kasuta, võite lisada küsimused otse küsimustikku.</span><span class="sxs-lookup"><span data-stu-id="b8265-212">If you aren't using result groups, you can attach questions directly to the questionnaire.</span></span>

3.  <span data-ttu-id="b8265-213">Vajaduse korral seadistage tingimuslike küsimuste hierarhia.</span><span class="sxs-lookup"><span data-stu-id="b8265-213">Set up a conditional question hierarchy, if it's required.</span></span>
4.  <span data-ttu-id="b8265-214">Testige küsimustikku.</span><span class="sxs-lookup"><span data-stu-id="b8265-214">Test the questionnaire.</span></span>

<span data-ttu-id="b8265-215">Klõpsake lehel **Küsimustikud** valikut **Kinnita** testimiseks, kas küsimustik on õigesti koostatud.</span><span class="sxs-lookup"><span data-stu-id="b8265-215">On the **Questionnaires** page, click **Validate** to test whether the questionnaire is assembled correctly.</span></span> <span data-ttu-id="b8265-216">Kuid samuti tasub täita küsimustik ja testida seda ise enne laiali saatmist.</span><span class="sxs-lookup"><span data-stu-id="b8265-216">However, it's also a good idea to complete the questionnaire and test it yourself before you distribute it.</span></span>

### <a name="modify-a-questionnaire"></a><span data-ttu-id="b8265-217">Küsimustiku muutmine</span><span class="sxs-lookup"><span data-stu-id="b8265-217">Modify a questionnaire</span></span>

<span data-ttu-id="b8265-218">Lehel **Küsimustikud** saab teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="b8265-218">You can complete the following tasks on the **Questionnaires** page:</span></span>

-   <span data-ttu-id="b8265-219">Muuta küsimustiku teavet (nt tulemusegruppe ja küsimusi).</span><span class="sxs-lookup"><span data-stu-id="b8265-219">Modify information in the questionnaire, such as the result groups and questions.</span></span>
-   <span data-ttu-id="b8265-220">Kustutada ja lisada küsimusi.</span><span class="sxs-lookup"><span data-stu-id="b8265-220">Delete and add questions.</span></span>
-   <span data-ttu-id="b8265-221">muuta tulemustegruppe ja järjekorranumbreid.</span><span class="sxs-lookup"><span data-stu-id="b8265-221">Make changes in the result groups and sequence number.</span></span> 

<span data-ttu-id="b8265-222">**Ettevaatust!** Olge ettevaatlikud vastatud küsimustike muutmisel.</span><span class="sxs-lookup"><span data-stu-id="b8265-222">**Caution:** Be careful when you change questionnaires that have already been answered.</span></span> <span data-ttu-id="b8265-223">Muudatused võivad vähendada statistika täpsust ja seetõttu muuta selle hindamiseks ebapiisavaks.</span><span class="sxs-lookup"><span data-stu-id="b8265-223">Changes can reduce the accuracy of statistics and therefore make them a poor basis for evaluation.</span></span> <span data-ttu-id="b8265-224">Vastatud küsimuse muutmise asemel võiksite luua uue küsimuse.</span><span class="sxs-lookup"><span data-stu-id="b8265-224">Consider creating a new question instead of changing a question that has already been answered.</span></span>

<span data-ttu-id="b8265-225">Küsimustikus ei saa kustutada järgmist tüüpi küsimusi.</span><span class="sxs-lookup"><span data-stu-id="b8265-225">In a questionnaire, you can't delete the following types of questions:</span></span>

-   <span data-ttu-id="b8265-226">Küsimustikuga seotud küsimused</span><span class="sxs-lookup"><span data-stu-id="b8265-226">Questions that are attached to a questionnaire</span></span>
-   <span data-ttu-id="b8265-227">Juba vastatud küsimused, mis seetõttu kuvatakse dialoogiboksis **Vastused**.</span><span class="sxs-lookup"><span data-stu-id="b8265-227">Questions that have already been answered and therefore appear in the **Answers** dialog box.</span></span>

### <a name="result-groups"></a><span data-ttu-id="b8265-228">Tulemustegrupid</span><span class="sxs-lookup"><span data-stu-id="b8265-228">Result groups</span></span>

<span data-ttu-id="b8265-229">Tulemusegrupid on valikulised, kui seote küsimused küsimustikega.</span><span class="sxs-lookup"><span data-stu-id="b8265-229">Result groups are optional when you attach questions to a questionnaire.</span></span> 

<span data-ttu-id="b8265-230">Tulemusegruppi kasutatakse punktide arvestamiseks ja küsimustiku tulemuste kategooriatesse jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="b8265-230">A result group is used to calculate points and categorize the results of a questionnaire.</span></span> <span data-ttu-id="b8265-231">Kui kasutate tulemusegruppe, saate teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="b8265-231">If you use result groups, you can perform the following tasks:</span></span>

-   <span data-ttu-id="b8265-232">Hinnata küsimustiku tulemusi punktide statistika alusel.</span><span class="sxs-lookup"><span data-stu-id="b8265-232">Evaluate questionnaire results, based on point statistics.</span></span>
-   <span data-ttu-id="b8265-233">Hinnata vastaja skoori iga seadistatud tulemusegrupi puhul.</span><span class="sxs-lookup"><span data-stu-id="b8265-233">Evaluate a respondent’s score for each result group that you set up.</span></span>
-   <span data-ttu-id="b8265-234">Tulemuste analüüsimise hõlbustamiseks tehke iga tulemustegruppi kohta statistikat.</span><span class="sxs-lookup"><span data-stu-id="b8265-234">Generate statistics for each result group to help you analyze results.</span></span>
-   <span data-ttu-id="b8265-235">Printida aruande, milles kuvatakse iga tulemusegrupi tulemused ja ka valikulised punktid/tekstid, mis põhinevad igas tulemusegrupis teenitud punktidel.</span><span class="sxs-lookup"><span data-stu-id="b8265-235">Print a report that shows results for each result group, and also optional points/texts that are based on points that are earned in each result group.</span></span>

<span data-ttu-id="b8265-236">**Märkus.** Enne tulemusegruppide seadistamist tuleb teha järgmine seadistus.</span><span class="sxs-lookup"><span data-stu-id="b8265-236">**Note:** Before you can set up result groups, you must complete the following tasks:</span></span>

-   <span data-ttu-id="b8265-237">Seadistage suletud küsimused.</span><span class="sxs-lookup"><span data-stu-id="b8265-237">Set up closed-ended questions.</span></span> <span data-ttu-id="b8265-238">Suletud küsimuste puhul peab sisendi tüüp lehel **Küsimused** olema **Märkeruut**, **Alternatiivne nupp** või **Liitboks**.</span><span class="sxs-lookup"><span data-stu-id="b8265-238">For a closed-ended question, the input type on the **Questions** page must be **Check box**, **Alternative button**, or **Combo box**.</span></span>
-   <span data-ttu-id="b8265-239">Määrake vastusegrupis iga küsimuse juurde vastuse punktide arv.</span><span class="sxs-lookup"><span data-stu-id="b8265-239">Define points for answers in the answer groups that are assigned to each question.</span></span>
-   <span data-ttu-id="b8265-240">Seadistage küsimustik.</span><span class="sxs-lookup"><span data-stu-id="b8265-240">Set up a questionnaire.</span></span>

<span data-ttu-id="b8265-241">Küsimuste sidumiseks küsimustikega tulemusegruppide abil seadistage kõigepealt küsimustiku tulemusegrupid ja lisage siis tulemusegruppidesse küsimusi.</span><span class="sxs-lookup"><span data-stu-id="b8265-241">To attach questions to a questionnaire by using result groups, first set up the result groups for the questionnaire, and then add questions to the result groups.</span></span> <span data-ttu-id="b8265-242">Kui te tulemusegruppe ei kasuta, võite siduda küsimused otse küsimustikuga.</span><span class="sxs-lookup"><span data-stu-id="b8265-242">If you don't use result groups, you can attach questions directly to a questionnaire.</span></span> 

<span data-ttu-id="b8265-243">Saate seadistada mitu tulemusegruppi, et hinnata punkte, mida vastaja igas kategoorias teenib.</span><span class="sxs-lookup"><span data-stu-id="b8265-243">You can set up multiple result groups to evaluate the points that a respondent earns in each category.</span></span> <span data-ttu-id="b8265-244">Pärast küsimustiku täitmist saate vaadata igas tulemusegrupis saadud punkte.</span><span class="sxs-lookup"><span data-stu-id="b8265-244">After a questionnaire is completed, you can view the points that have been achieved for each result group.</span></span> 

<span data-ttu-id="b8265-245">**Näpunäide.** Küsimustiku hindamiseks punktide, kuid mitte eraldi kategooriate abil võite lisada kõik küsimused ühte tulemusegruppi.</span><span class="sxs-lookup"><span data-stu-id="b8265-245">**Tip:** To evaluate a questionnaire by using points but not separate categories, you can add all questions to a single result group.</span></span> 

<span data-ttu-id="b8265-246">Iga tulemusegrupi kohta saab seadistada ka vähemalt ühe punktidel põhineva teate, mille vastajad pärast küsimustiku täitmist saavad.</span><span class="sxs-lookup"><span data-stu-id="b8265-246">For each result group, you can also set up one or more point-based messages that respondents receive after they complete a questionnaire.</span></span> <span data-ttu-id="b8265-247">Kuvatav tekst võib varieeruda, olenevalt punktisummast, mille vastaja tulemusegrupis saavutas.</span><span class="sxs-lookup"><span data-stu-id="b8265-247">The text that is shown can vary, depending on the score that a respondent achieves in a result group.</span></span> <span data-ttu-id="b8265-248">Punktidel põhinevate teadete kasutamiseks tuleb määratleda punktide intervallid ja iga intervalli kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b8265-248">To use point-based messages, you must define point intervals and a description of each interval.</span></span> <span data-ttu-id="b8265-249">Kui vastaja saavutab punktisumma konkreetses intervallis, lisatakse tulemuste aruandesse selle intervalli tekst.</span><span class="sxs-lookup"><span data-stu-id="b8265-249">When a respondent achieves a score in a specific interval, the text for that interval is included on the results report.</span></span> 

<span data-ttu-id="b8265-250">Kuna tulemusegrupp on seotud konkreetsete küsimuseplokkide punktidega, saate kasutada küsimustiku puhul ainult konkreetset tulemusegruppi.</span><span class="sxs-lookup"><span data-stu-id="b8265-250">Because a result group is related to the points that are associated with specific sets of questions on a questionnaire, you can use only a specific result group for a questionnaire.</span></span>

#### <a name="example-pointstexts-for-result-group-3"></a><span data-ttu-id="b8265-251">Näiteks: punktid/tekstid tulemusegrupile 3</span><span class="sxs-lookup"><span data-stu-id="b8265-251">Example: Points/texts for result group 3</span></span>

<span data-ttu-id="b8265-252">Kasutate juhtimisküsimustikku, milles on 15 küsimust kolmes kategoorias.</span><span class="sxs-lookup"><span data-stu-id="b8265-252">You're using a questionnaire for a leadership test that has 15 questions in three categories.</span></span> <span data-ttu-id="b8265-253">Loote kolm tulemusegruppi ja lisate igasse tulemusegruppi viis küsimust.</span><span class="sxs-lookup"><span data-stu-id="b8265-253">You create three result groups and add five questions to each result group.</span></span> <span data-ttu-id="b8265-254">Seejärel summeeritakse punktid kolmes grupis.</span><span class="sxs-lookup"><span data-stu-id="b8265-254">Points are then totaled in the three groups.</span></span> <span data-ttu-id="b8265-255">Kolm tulemusegruppi on järgmised.</span><span class="sxs-lookup"><span data-stu-id="b8265-255">The three result groups are as follows:</span></span>

-   <span data-ttu-id="b8265-256">Loovus</span><span class="sxs-lookup"><span data-stu-id="b8265-256">Creative abilities</span></span>
-   <span data-ttu-id="b8265-257">Juhivõimed</span><span class="sxs-lookup"><span data-stu-id="b8265-257">Leadership abilities</span></span>
-   <span data-ttu-id="b8265-258">Tehnilised teadmised</span><span class="sxs-lookup"><span data-stu-id="b8265-258">Technical abilities</span></span>

<span data-ttu-id="b8265-259">Punktipõhiste sõnumite kasutamiseks seadistate igale tulemusegrupile tekstivahemikud.</span><span class="sxs-lookup"><span data-stu-id="b8265-259">To use point-based messages, you set up text intervals for each result group.</span></span> <span data-ttu-id="b8265-260">Igale küsimusele määratakse kaks punkti.</span><span class="sxs-lookup"><span data-stu-id="b8265-260">Each question is assigned two points.</span></span> <span data-ttu-id="b8265-261">Seetõttu on iga tulemustegrupi maksimaalse punktisumma 10.</span><span class="sxs-lookup"><span data-stu-id="b8265-261">Therefore, the maximum point total in each result group is 10.</span></span> 

<span data-ttu-id="b8265-262">Järgmises tabelis on toodud punktipõhised sõnumid, mille määratlete tulemustegrupile „juhivõimed”.</span><span class="sxs-lookup"><span data-stu-id="b8265-262">The following table shows the point-based messages that you define for the “leadership abilities” result group.</span></span>

| <span data-ttu-id="b8265-263">Punktivahemik</span><span class="sxs-lookup"><span data-stu-id="b8265-263">Point interval</span></span> | <span data-ttu-id="b8265-264">Tekst</span><span class="sxs-lookup"><span data-stu-id="b8265-264">Text</span></span>                                       |
|----------------|--------------------------------------------|
| <span data-ttu-id="b8265-265">1 kuni 3</span><span class="sxs-lookup"><span data-stu-id="b8265-265">1 to 3</span></span>         | <span data-ttu-id="b8265-266">Teil on keskmised juhivõimed.</span><span class="sxs-lookup"><span data-stu-id="b8265-266">You have average leadership abilities.</span></span>     |
| <span data-ttu-id="b8265-267">4 kuni 7</span><span class="sxs-lookup"><span data-stu-id="b8265-267">4 to 7</span></span>         | <span data-ttu-id="b8265-268">Teil on head juhivõimed.</span><span class="sxs-lookup"><span data-stu-id="b8265-268">You have good leadership abilities.</span></span>        |
| <span data-ttu-id="b8265-269">8 kuni 10</span><span class="sxs-lookup"><span data-stu-id="b8265-269">8 to 10</span></span>        | <span data-ttu-id="b8265-270">Teil on suurepärased juhivõimed.</span><span class="sxs-lookup"><span data-stu-id="b8265-270">You have outstanding leadership abilities.</span></span> |

<span data-ttu-id="b8265-271">Saate seadistada punktivahemikud ja tekstid igale tulemusegrupile küsimustikus.</span><span class="sxs-lookup"><span data-stu-id="b8265-271">You can set up point intervals and texts for each result group on a questionnaire.</span></span> <span data-ttu-id="b8265-272">Iga vastaja skooril põhinevad tekstid kuvatakse iga tulemusegrupi puhul.</span><span class="sxs-lookup"><span data-stu-id="b8265-272">Texts that correspond to each respondent’s score are displayed for each result group.</span></span> 

<span data-ttu-id="b8265-273">**Märkus.** Saate intervalle ja tekste muuta.</span><span class="sxs-lookup"><span data-stu-id="b8265-273">**Note:** You can change intervals and texts.</span></span> <span data-ttu-id="b8265-274">Kuid kui küsimustik on täidetud, võivad muudatused põhjustada eelmiste ja uute tulemusearuannete vahel erinevusi.</span><span class="sxs-lookup"><span data-stu-id="b8265-274">However, if a questionnaire has been completed, changes might cause differences between previous and new result reports.</span></span>

### <a name="conditional-question-hierarchies"></a><span data-ttu-id="b8265-275">Tingimuslike küsimuste hierarhiad</span><span class="sxs-lookup"><span data-stu-id="b8265-275">Conditional question hierarchies</span></span>

<span data-ttu-id="b8265-276">Tingimuslike küsimuste hierarhiad on küsimustiku seadistamisel valikulised.</span><span class="sxs-lookup"><span data-stu-id="b8265-276">Conditional question hierarchies are optional when you set up a questionnaire.</span></span> 

<span data-ttu-id="b8265-277">**Märkus.** Enne tingimuslike küsimuste hierarhia seadistamist tuleb siduda küsimustikuga küsimused, millele on määratud vastusegrupid.</span><span class="sxs-lookup"><span data-stu-id="b8265-277">**Note:** Before you can set up a conditional question hierarchy, you must attach questions that have assigned answer groups to the questionnaire.</span></span> 

<span data-ttu-id="b8265-278">Tingimuslike küsimuste kasutamiseks küsimustikus küsimuste hierarhia loomiseks võite luua küsimuste esitamise järjekorra sõltuvalt vastusest, mille vastaja iga küsimuse puhul valib.</span><span class="sxs-lookup"><span data-stu-id="b8265-278">To use conditional questions to create a question hierarchy in a questionnaire, you can make the sequence that questions are presented in depend on the answer that a respondent selects for each question.</span></span> <span data-ttu-id="b8265-279">Võttes küsimuste järjestuse aluseks vastajate vastusevaliku, saate küsimustikku kohandada sel ajal, kui vastaja seda täidab.</span><span class="sxs-lookup"><span data-stu-id="b8265-279">By basing the question sequence on a respondent’s answer, you can modify the questionnaire as the respondent completes it.</span></span>

#### <a name="examples"></a><span data-ttu-id="b8265-280">Näited</span><span class="sxs-lookup"><span data-stu-id="b8265-280">Examples</span></span>

<span data-ttu-id="b8265-281">Juriidiline isik pakub oma klientidele nii kaupu kui ka teenuseid.</span><span class="sxs-lookup"><span data-stu-id="b8265-281">A legal entity offers both items and services to its customers.</span></span> <span data-ttu-id="b8265-282">Nagu sellistel puhkudel tavaliselt juhtub, ostavad mõned kliendid ainult kaupu, mõned ainult teenuseid ja mõned nii kaupu kui ka teenuseid.</span><span class="sxs-lookup"><span data-stu-id="b8265-282">As typically occurs in such cases, some customers purchase only items, some purchase only services, and some purchase both items and services.</span></span> <span data-ttu-id="b8265-283">Seega, kui juriidiline isik saadab laiali kliendirahulolu uuringu, rakendatakse küsimustikus tingimuslikku struktuuri, et kliendid, kes ostavad ainult teenuseid, ei peaks vastama kaupu puudutavatele küsimustele.</span><span class="sxs-lookup"><span data-stu-id="b8265-283">Therefore, when the legal entity distributes a customer satisfaction survey, it applies a conditional structure to the questionnaire, so that customers who purchase only services don't have to answer questions about items.</span></span> 

<span data-ttu-id="b8265-284">Teine võimalus on seadistada küsimustik nii, et kui vastaja valib küsimusele 1 vastuse A, on küsimus 2 küsimuste järjekorras järgmine.</span><span class="sxs-lookup"><span data-stu-id="b8265-284">Alternatively, you set up a questionnaire so that if a respondent selects answer A for question 1, question 2 is next in the question sequence.</span></span> <span data-ttu-id="b8265-285">Kuid kui vastaja valib küsimuse 1 puhul vastuse B, on järgmine küsimus 5.</span><span class="sxs-lookup"><span data-stu-id="b8265-285">However, if the respondent selects answer B for question 1, question 5 is next.</span></span>

<a name="see-also"></a><span data-ttu-id="b8265-286">Vt ka</span><span class="sxs-lookup"><span data-stu-id="b8265-286">See also</span></span>
--------

[<span data-ttu-id="b8265-287">Küsimustike kasutamine</span><span class="sxs-lookup"><span data-stu-id="b8265-287">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="b8265-288">Küsimustike laialisaatmine ja täitmine</span><span class="sxs-lookup"><span data-stu-id="b8265-288">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

[<span data-ttu-id="b8265-289">Küsimustike tulemuste vaatamine ja hindamine</span><span class="sxs-lookup"><span data-stu-id="b8265-289">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


