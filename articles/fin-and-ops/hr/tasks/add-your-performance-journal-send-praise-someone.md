---
title: Jõudluse töölehele kirje lisamine ja teistele tänu saatmine
description: Jõudluse töölehel on teave, mis on seotud sellega, kuidas olete oma eesmärke saavutanud või millised on teie tulemused mingil perioodil.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f2f8e0e858a27bec09eee6f7f02dc952fe8e408
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "856458"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="dd732-103">Jõudluse töölehele kirje lisamine ja teistele tänu saatmine</span><span class="sxs-lookup"><span data-stu-id="dd732-103">Add to your performance journal and send praise to someone</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd732-104">Jõudluse töölehel on teave, mis on seotud sellega, kuidas olete oma eesmärke saavutanud või millised on teie tulemused mingil perioodil.</span><span class="sxs-lookup"><span data-stu-id="dd732-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="dd732-105">Töölehe kaudu saab ka kolleegi tegevusi kiita.</span><span class="sxs-lookup"><span data-stu-id="dd732-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="dd732-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="dd732-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dd732-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="dd732-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="dd732-108">Avage Kõik tööruumid > Töötaja iseteenindus.</span><span class="sxs-lookup"><span data-stu-id="dd732-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="dd732-109">Klõpsake valikut Jõudluse tööraamat.</span><span class="sxs-lookup"><span data-stu-id="dd732-109">Click Performance journal.</span></span>
3. <span data-ttu-id="dd732-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dd732-110">Click New.</span></span>
4. <span data-ttu-id="dd732-111">Sisestage väärtus väljale Pealkiri.</span><span class="sxs-lookup"><span data-stu-id="dd732-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="dd732-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="dd732-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="dd732-113">Jõudluse töölehe kuupäev on töölehe loomise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="dd732-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="dd732-114">Allikas näitab, kust jõudluse tööleht pärineb.</span><span class="sxs-lookup"><span data-stu-id="dd732-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="dd732-115">Kui teie selle loote, on selle lähtekoht Minu tööleht.</span><span class="sxs-lookup"><span data-stu-id="dd732-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="dd732-116">Kui selle loob teie juht, on selle lähtekoht Juhi tööleht.</span><span class="sxs-lookup"><span data-stu-id="dd732-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="dd732-117">Saate seda töölehte oma juhiga jagada või muuta selle nähtavaks ainult endale.</span><span class="sxs-lookup"><span data-stu-id="dd732-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="dd732-118">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="dd732-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="dd732-119">Sisestage kuupäev väljale Lõpetamiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="dd732-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="dd732-120">Valige Jah väljalt Arenguplaan.</span><span class="sxs-lookup"><span data-stu-id="dd732-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="dd732-121">Tippige väärtus väljale Märksõnad.</span><span class="sxs-lookup"><span data-stu-id="dd732-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="dd732-122">Klõpsake valikut Lisa väline link.</span><span class="sxs-lookup"><span data-stu-id="dd732-122">Click Add external link.</span></span>
11. <span data-ttu-id="dd732-123">Tippige väljale Kirjeldus väärtus Envision.</span><span class="sxs-lookup"><span data-stu-id="dd732-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="dd732-124">Sisestage internetiaadressi väljale väärtus https://www.microsoft.com/en/envision/default.</span><span class="sxs-lookup"><span data-stu-id="dd732-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="dd732-125">Klõpsake nupu Salvesta all olevat selgitust „Jõudluse tööleht” ruudustikku naasmiseks.</span><span class="sxs-lookup"><span data-stu-id="dd732-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="dd732-126">Valitud töölehe või töölehed saab lisada eesmärgile, nii et see kuvatakse, kui eesmärgi avad.</span><span class="sxs-lookup"><span data-stu-id="dd732-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="dd732-127">Kiirkaardile Lingid lisatakse link. Kui lisate eesmärgile töölehe ja seejärel lisate eesmärgi hindamisse, kuvatakse tööleht automaatselt hindamises.</span><span class="sxs-lookup"><span data-stu-id="dd732-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="dd732-128">Valitud töölehe või töölehed saab lisada hindamisele, nii et see kuvatakse, kui hindamise avad.</span><span class="sxs-lookup"><span data-stu-id="dd732-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="dd732-129">Kiirkaardile Lingid lisatakse link.</span><span class="sxs-lookup"><span data-stu-id="dd732-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="dd732-130">Klõpsake nuppu Kiirlisamine.</span><span class="sxs-lookup"><span data-stu-id="dd732-130">Click Quick add.</span></span>
15. <span data-ttu-id="dd732-131">Sisestage väärtus väljale Pealkiri.</span><span class="sxs-lookup"><span data-stu-id="dd732-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="dd732-132">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="dd732-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="dd732-133">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dd732-133">Click Save.</span></span>
18. <span data-ttu-id="dd732-134">Klõpsake nuppu Saada kiitus.</span><span class="sxs-lookup"><span data-stu-id="dd732-134">Click Send praise.</span></span>
19. <span data-ttu-id="dd732-135">Valige ettevõtte töötajate nimekirjas olev inimene.</span><span class="sxs-lookup"><span data-stu-id="dd732-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="dd732-136">Sisestage väljale Kirjeldus tekst „Aitäh abi eest konverentsil!”.</span><span class="sxs-lookup"><span data-stu-id="dd732-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="dd732-137">Klõpsake käsku Saada.</span><span class="sxs-lookup"><span data-stu-id="dd732-137">Click Send.</span></span>

