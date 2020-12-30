---
title: Kandidaatide valikutööriistade tuvastamine ja juurutamine
description: Vabade kohtade täitmiseks piisava hulga kvalifitseeritud kandidaatide leidmine võib olla keeruline, eriti kui ametikoht nõuab unikaalseid oskusi.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4e7ed6feaa1b5b27fcfc0ec99a2d75415fe7d6a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693060"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="d34e0-103">Kandidaatide valikutööriistade tuvastamine ja juurutamine</span><span class="sxs-lookup"><span data-stu-id="d34e0-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d34e0-104">Vabade kohtade täitmiseks piisava hulga kvalifitseeritud kandidaatide leidmine võib olla keeruline, eriti kui ametikoht nõuab unikaalseid oskusi.</span><span class="sxs-lookup"><span data-stu-id="d34e0-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="d34e0-105">Siiski võivad vajatavate oskustega kandidaadid aga juba teie organisatsioonis töötada.</span><span class="sxs-lookup"><span data-stu-id="d34e0-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="d34e0-106">Saate otsida olemasolevate töötajate või uute kandidaatide seast kindlate oskustega spetsialiste.</span><span class="sxs-lookup"><span data-stu-id="d34e0-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="d34e0-107">See võimaldab värbajal kiiresti koguda ja üle vaadata kandidaadid, kes on praegu või varem vabale ametikohale kandideerinud, või leida potentsiaalne kandidaat olemasolevate töötajate seast.</span><span class="sxs-lookup"><span data-stu-id="d34e0-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="d34e0-108">Saate seda ülesande salvestist kasutades õppida, kuidas oskuste kaardistamise funktsioon aitab teil vabale ametikohale õiget inimest leida.</span><span class="sxs-lookup"><span data-stu-id="d34e0-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="d34e0-109">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d34e0-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d34e0-110">Avage Personaliarvestus > Pädevused > Oskuste analüüs > Oskuste kaardistamise profiilid.</span><span class="sxs-lookup"><span data-stu-id="d34e0-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="d34e0-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d34e0-111">Click New.</span></span>
3. <span data-ttu-id="d34e0-112">Sisestage oma oskuste kaardistamise nimi väljale Oskuste kaardistamine.</span><span class="sxs-lookup"><span data-stu-id="d34e0-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="d34e0-113">Näide: raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="d34e0-113">Example: Accountant.</span></span>
4. <span data-ttu-id="d34e0-114">Sisestage oskuste kaardistamise kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d34e0-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="d34e0-115">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d34e0-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="d34e0-116">Klõpsake nuppu Too reeglid.</span><span class="sxs-lookup"><span data-stu-id="d34e0-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="d34e0-117">Valige otsingu aluseks isik, töö või kursus ning tõmmake funktsiooni Too reeglid abil andmed tunnistuse, oskuse ja hariduse kohta.</span><span class="sxs-lookup"><span data-stu-id="d34e0-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="d34e0-118">Seejärel saate kriteeriumeid lisada või eemaldada, määrata kriteeriumide valikulisust ning anda kriteeriumidele tähtsus.</span><span class="sxs-lookup"><span data-stu-id="d34e0-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="d34e0-119">Klõpsake vahekaarti Töö.</span><span class="sxs-lookup"><span data-stu-id="d34e0-119">Click Job.</span></span>
8. <span data-ttu-id="d34e0-120">Sisestage või valige väärtus väljal Töö.</span><span class="sxs-lookup"><span data-stu-id="d34e0-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="d34e0-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d34e0-121">Click OK.</span></span>
10. <span data-ttu-id="d34e0-122">Laiendage kiirkaarti Vahemik ja lisage mistahes täiendavat teavet, näiteks osakond.</span><span class="sxs-lookup"><span data-stu-id="d34e0-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="d34e0-123">Tunnistuste vaatamiseks või redigeerimiseks laiendage kiirkaarti Tunnistused.</span><span class="sxs-lookup"><span data-stu-id="d34e0-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="d34e0-124">Oskuste vaatamiseks või redigeerimiseks laiendage kiirkaarti Oskused.</span><span class="sxs-lookup"><span data-stu-id="d34e0-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="d34e0-125">Hariduse kriteeriumide vaatamiseks või redigeerimiseks laiendage kiirkaarti Haridus.</span><span class="sxs-lookup"><span data-stu-id="d34e0-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="d34e0-126">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="d34e0-126">Click Execute.</span></span>
15. <span data-ttu-id="d34e0-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d34e0-127">Click OK.</span></span>
16. <span data-ttu-id="d34e0-128">Klõpsake vahekaarti Tulemus.</span><span class="sxs-lookup"><span data-stu-id="d34e0-128">Click Result.</span></span>
17. <span data-ttu-id="d34e0-129">Klõpsake vahekaarti Tulemus.</span><span class="sxs-lookup"><span data-stu-id="d34e0-129">Click Result.</span></span>
18. <span data-ttu-id="d34e0-130">Klõpsake Jätka.</span><span class="sxs-lookup"><span data-stu-id="d34e0-130">Click Resume.</span></span>
19. <span data-ttu-id="d34e0-131">Klõpsake vahekaarti Tunnistused.</span><span class="sxs-lookup"><span data-stu-id="d34e0-131">Click Certificates.</span></span>
    * <span data-ttu-id="d34e0-132">Saate süvitsi minna iga loendis oleva isiku andmetesse ja vaadata nende hariduse, oskuste ja professionaalse kogemuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d34e0-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="d34e0-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d34e0-133">Close the page.</span></span>
21. <span data-ttu-id="d34e0-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d34e0-134">Close the page.</span></span>
22. <span data-ttu-id="d34e0-135">Valige tulemus uuesti.</span><span class="sxs-lookup"><span data-stu-id="d34e0-135">Select result again.</span></span>
23. <span data-ttu-id="d34e0-136">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="d34e0-136">Click Report.</span></span>
    * <span data-ttu-id="d34e0-137">Parimad vasted loetletakse aruande ülaosas.</span><span class="sxs-lookup"><span data-stu-id="d34e0-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="d34e0-138">Näete, et vaheelement on loetletud.</span><span class="sxs-lookup"><span data-stu-id="d34e0-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="d34e0-139">See on näitab erinevust oskuste kaardistamisel üles loetletud ja isikule määratud oskuste taseme vahel.</span><span class="sxs-lookup"><span data-stu-id="d34e0-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="d34e0-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d34e0-140">Close the page.</span></span>
25. <span data-ttu-id="d34e0-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d34e0-141">Click Save.</span></span>

