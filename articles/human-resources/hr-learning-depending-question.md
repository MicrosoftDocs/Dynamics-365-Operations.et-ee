---
title: Eelmise küsimuse vastusest sõltuva küsimuse koostamine
description: Tingimuslike küsimuste abil saate määrata, milliseid järelküsimusi vastajale eelmise küsimuse vastuse põhjal esitatakse.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4295b49336ec7ac3cff4deba675bc63511be48de
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429539"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="ee80c-103">Eelmise küsimuse vastusest sõltuva küsimuse koostamine</span><span class="sxs-lookup"><span data-stu-id="ee80c-103">Make a question dependent on the answer of the previous question</span></span>



<span data-ttu-id="ee80c-104">Tingimuslike küsimuste abil saate määrata, milliseid järelküsimusi vastajale eelmise küsimuse vastuse põhjal esitatakse.</span><span class="sxs-lookup"><span data-stu-id="ee80c-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="ee80c-105">Näiteks kui küsite Kas eelistate kohvi või teed?, saab loogilise järelküsimuse määrata olenevalt sellest, kas vastaja valib vastuseks kohvi või tee.</span><span class="sxs-lookup"><span data-stu-id="ee80c-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="ee80c-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ee80c-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="ee80c-107">Olemasoleva küsimustiku leidmine</span><span class="sxs-lookup"><span data-stu-id="ee80c-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="ee80c-108">Avage Küsimustik > Kujundus > Küsimustikud.</span><span class="sxs-lookup"><span data-stu-id="ee80c-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="ee80c-109">Valige loendist küsimustik WorkFH.</span><span class="sxs-lookup"><span data-stu-id="ee80c-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="ee80c-110">Kõikide küsimuste ja alamküsimuste lisamine küsimustikku</span><span class="sxs-lookup"><span data-stu-id="ee80c-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="ee80c-111">Klõpsake suvandit Küsimused.</span><span class="sxs-lookup"><span data-stu-id="ee80c-111">Click Questions.</span></span>
2. <span data-ttu-id="ee80c-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ee80c-112">Click New.</span></span>
3. <span data-ttu-id="ee80c-113">Valige küsimus number 00016 väljalt Küsimus.</span><span class="sxs-lookup"><span data-stu-id="ee80c-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="ee80c-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ee80c-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ee80c-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ee80c-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ee80c-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ee80c-116">Click Save.</span></span>
7. <span data-ttu-id="ee80c-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ee80c-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="ee80c-118">Küsimustiku järjestuse määramine tingimuslikuks ja küsimuse muutmine asjakohasest küsimusest sõltuvaks</span><span class="sxs-lookup"><span data-stu-id="ee80c-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="ee80c-119">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ee80c-119">Click Edit.</span></span>
2. <span data-ttu-id="ee80c-120">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="ee80c-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="ee80c-121">Valige väljalt Küsimuste järjekord suvand Tingimuslik.</span><span class="sxs-lookup"><span data-stu-id="ee80c-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="ee80c-122">Klõpsake suvandit Tinglik küsimus.</span><span class="sxs-lookup"><span data-stu-id="ee80c-122">Click Conditional question.</span></span>
5. <span data-ttu-id="ee80c-123">Valige puult suvand Küsimused\selgitage, miks vastasite eelmisele küsimusele selliselt?.</span><span class="sxs-lookup"><span data-stu-id="ee80c-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="ee80c-124">Valige küsimus 00009 väljalt Esmane küsimus.</span><span class="sxs-lookup"><span data-stu-id="ee80c-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="ee80c-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ee80c-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ee80c-126">Sisestage väljale Vastus see vastuse suvandi vastuse seeria ID, millest soovite küsimuse sõltuvaks teha.</span><span class="sxs-lookup"><span data-stu-id="ee80c-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="ee80c-127">Näiteks sisestage esimese vastuse suvandi puhul 1.</span><span class="sxs-lookup"><span data-stu-id="ee80c-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="ee80c-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ee80c-128">Click Save.</span></span>
10. <span data-ttu-id="ee80c-129">Valige puul suvand Küsimused\mulle makstakse tehtava töö eest õiglast tasu.</span><span class="sxs-lookup"><span data-stu-id="ee80c-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="ee80c-130">Pange tähele, et küsimuse puud värskendatakse sõltuvuse näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee80c-130">Note that the question tree updated to show the dependency.</span></span>  

