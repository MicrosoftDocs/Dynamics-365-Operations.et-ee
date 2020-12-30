---
title: Kandidaadi ja avalduse andmete käsitsi sisestamine
description: See protseduur näitab, kuidas kandidaatide ja nende avalduse teavet käsitsi säilitada.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ea39e86ace40cd8e3ad2733b7f7f7a873a963e7
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693036"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="e75bc-103">Kandidaadi ja avalduse andmete käsitsi sisestamine</span><span class="sxs-lookup"><span data-stu-id="e75bc-103">Enter applicant and application data manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e75bc-104">See protseduur näitab, kuidas kandidaatide ja nende avalduse teavet käsitsi säilitada.</span><span class="sxs-lookup"><span data-stu-id="e75bc-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="e75bc-105">Saate sisestada ja säilitada kandidaatide isikuandmeid, vestluse kuupäevi ja aegu, viiteid, pädevusi ja erivajaduse taotlusi.</span><span class="sxs-lookup"><span data-stu-id="e75bc-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="e75bc-106">Saate värskendada ka kandidaatide kandideerimisavalduste olekut ja luua kandidaatidega suhtlemiseks kirju või meilisõnumeid.</span><span class="sxs-lookup"><span data-stu-id="e75bc-106">You can also update the status of applicants' applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="e75bc-107">Kandidaadi kirje loomisel luuakse selle kandidaadi isiku kirje globaalses aadressiraamatus.</span><span class="sxs-lookup"><span data-stu-id="e75bc-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="e75bc-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e75bc-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="e75bc-109">Uue kandidaadi kirje loomine</span><span class="sxs-lookup"><span data-stu-id="e75bc-109">Create a new applicant record</span></span>
1. <span data-ttu-id="e75bc-110">Avage Personaliarvestus > Värbamine > Kandidaadid > Kandidaadid.</span><span class="sxs-lookup"><span data-stu-id="e75bc-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="e75bc-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e75bc-111">Click New.</span></span>
3. <span data-ttu-id="e75bc-112">Sisestage väärtus väljale Eesnimi.</span><span class="sxs-lookup"><span data-stu-id="e75bc-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="e75bc-113">Sisestage väärtus väljale Perekonnanimi.</span><span class="sxs-lookup"><span data-stu-id="e75bc-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="e75bc-114">Olemasolul saate sisestada kandidaadi täiendavat teavet.</span><span class="sxs-lookup"><span data-stu-id="e75bc-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="e75bc-115">Teave võib sisaldada näiteks kandidaadi kõrgeimat kraadi, praegust ametinimetust või eelmist tööandjat.</span><span class="sxs-lookup"><span data-stu-id="e75bc-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="e75bc-116">Laiendage jaotist Kontaktteave.</span><span class="sxs-lookup"><span data-stu-id="e75bc-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="e75bc-117">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e75bc-117">Click Add.</span></span>
7. <span data-ttu-id="e75bc-118">Sisestage väljale Kirjeldus suvand Kommunikatsiooni meil.</span><span class="sxs-lookup"><span data-stu-id="e75bc-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="e75bc-119">Valige suvand väljalt Tüüp.</span><span class="sxs-lookup"><span data-stu-id="e75bc-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="e75bc-120">Sisestage väärtus väljale Kontaktnumber/aadress.</span><span class="sxs-lookup"><span data-stu-id="e75bc-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="e75bc-121">Seda meiliaadressi kasutatakse kandidaadiga meili teel suhtlemiseks.</span><span class="sxs-lookup"><span data-stu-id="e75bc-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="e75bc-122">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e75bc-122">Click Add.</span></span>
11. <span data-ttu-id="e75bc-123">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e75bc-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="e75bc-124">Sisestage väärtus väljale Kontaktnumber/aadress.</span><span class="sxs-lookup"><span data-stu-id="e75bc-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="e75bc-125">Kandidaadi isikuandmed.</span><span class="sxs-lookup"><span data-stu-id="e75bc-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="e75bc-126">Vajaduse korral saate sisestada kandidaadi puhul isiklikku lisateavet.</span><span class="sxs-lookup"><span data-stu-id="e75bc-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="e75bc-127">See võib hõlmata näiteks sünnikuupäeva, etnilist päritolu, sugu või perekonnaseisu.</span><span class="sxs-lookup"><span data-stu-id="e75bc-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="e75bc-128">Klõpsake toimingupaanil suvandit Pädevused.</span><span class="sxs-lookup"><span data-stu-id="e75bc-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="e75bc-129">Saate sisestada kandidaadi kompetentsi profiili, mis hõlmab nende oskusi, töökogemusi, haridust, katseid või tunnistusi.</span><span class="sxs-lookup"><span data-stu-id="e75bc-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="e75bc-130">Seda teavet saab kasutada kandidaadi oskuste vastendamiseks teie ettevõtte andmetes määratud töödega seotud oskustega.</span><span class="sxs-lookup"><span data-stu-id="e75bc-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="e75bc-131">Kandidaadi avalduse loomine</span><span class="sxs-lookup"><span data-stu-id="e75bc-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="e75bc-132">Klõpsake suvandit Avaldused.</span><span class="sxs-lookup"><span data-stu-id="e75bc-132">Click Applications.</span></span>
2. <span data-ttu-id="e75bc-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e75bc-133">Click New.</span></span>
3. <span data-ttu-id="e75bc-134">Klõpsake väljal Värbamisprojekt otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e75bc-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e75bc-135">Värbamisprojekti valides seostatakse kandidaat kindla sellesse värbamisprojekti kaasatud avamisega.</span><span class="sxs-lookup"><span data-stu-id="e75bc-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="e75bc-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e75bc-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e75bc-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e75bc-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e75bc-138">Vaikimisi põhinevad töö ja osakond valitud värbamisprojektil.</span><span class="sxs-lookup"><span data-stu-id="e75bc-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="e75bc-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e75bc-139">Click Save.</span></span>
    * <span data-ttu-id="e75bc-140">Pärast avalduse salvestamist saate lisada sellele dokumente, sealhulgas kandidaadi kogemuse, auhinnad ja kaaskirja.</span><span class="sxs-lookup"><span data-stu-id="e75bc-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

