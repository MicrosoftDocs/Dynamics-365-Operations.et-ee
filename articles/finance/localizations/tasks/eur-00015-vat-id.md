---
title: EUR-00015 KM ID seadistamine
description: See protseduur selgitab KM ID registreerimise eeltingimusi, nt registreerimistüübi seadistamist ja selle määramist registreerimiskategooriale.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5488bb020209d6bf6fb39ae0b4f897f5513bdf93
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821799"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="e17d5-103">EUR-00015 KM ID seadistamine</span><span class="sxs-lookup"><span data-stu-id="e17d5-103">EUR-00015 Set up VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e17d5-104">See protseduur selgitab KM ID registreerimise eeltingimusi, nt registreerimistüübi seadistamist ja selle määramist registreerimiskategooriale.</span><span class="sxs-lookup"><span data-stu-id="e17d5-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="e17d5-105">Lisateavet registreerimise ID-de ja registreerimise ID töötlemise kohta, sealhulgas nõutavad eeltingimused, leiate spikriteemast Registreerimise ID-d.</span><span class="sxs-lookup"><span data-stu-id="e17d5-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="e17d5-106">Siin antud teave kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="e17d5-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="e17d5-107">Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmaseks aadressiks on Saksamaa, andmeid.</span><span class="sxs-lookup"><span data-stu-id="e17d5-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="e17d5-108">See ülesanne on mõeldud süsteemi administraatoritele.</span><span class="sxs-lookup"><span data-stu-id="e17d5-108">This task is intended for system administrators.</span></span> <span data-ttu-id="e17d5-109">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="e17d5-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="e17d5-110">Avage Organisatsioonihaldus > Globaalne aadressiraamat > Registreerimistüübid > Registreerimistüübid.</span><span class="sxs-lookup"><span data-stu-id="e17d5-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="e17d5-111">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e17d5-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="e17d5-112">Tippige KM ID väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e17d5-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="e17d5-113">KM-kood väljal Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e17d5-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="e17d5-114">Sisestage või valige väärtus DEU väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="e17d5-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="e17d5-115">Tehke väljal Kordumatu valik Jah.</span><span class="sxs-lookup"><span data-stu-id="e17d5-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="e17d5-116">Märkige see ruut kontrollimiseks, kas KM ID on kordumatu.</span><span class="sxs-lookup"><span data-stu-id="e17d5-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="e17d5-117">Valige Jah väljal Riigi puhul esmane.</span><span class="sxs-lookup"><span data-stu-id="e17d5-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="e17d5-118">Märkige see ruut, kui KM ID peaks kehtima kõigi määratud riigi/regiooni aadresside puhul.</span><span class="sxs-lookup"><span data-stu-id="e17d5-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="e17d5-119">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="e17d5-119">Click Create.</span></span>
9. <span data-ttu-id="e17d5-120">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e17d5-120">Click Add.</span></span>
10. <span data-ttu-id="e17d5-121">Sisestage või valige väärtus ITA väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="e17d5-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="e17d5-122">Tippige väljale Vorming ###########.</span><span class="sxs-lookup"><span data-stu-id="e17d5-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="e17d5-123">Seda tüüpi registreerimisnumbri sisestamisel valitud riigi/piirkonna puhul kontrollitakse registreerimise ID-d selle vormingu suhtes.</span><span class="sxs-lookup"><span data-stu-id="e17d5-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="e17d5-124">Märkige ruut Kordumatu.</span><span class="sxs-lookup"><span data-stu-id="e17d5-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="e17d5-125">Märkige see ruut kontrollimiseks, kas KM ID on kordumatu.</span><span class="sxs-lookup"><span data-stu-id="e17d5-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="e17d5-126">Märkige või tühjendage ruut Riigi puhul esmane.</span><span class="sxs-lookup"><span data-stu-id="e17d5-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="e17d5-127">Märkige see ruut, kui KM ID peaks kehtima kõigi määratud riigi/regiooni aadresside puhul.</span><span class="sxs-lookup"><span data-stu-id="e17d5-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="e17d5-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e17d5-128">Click Save.</span></span>
15. <span data-ttu-id="e17d5-129">Avage Organisatsioonihaldus > Globaalne aadressiraamat > Registreerimistüübid > Registreerimiskategooriad.</span><span class="sxs-lookup"><span data-stu-id="e17d5-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="e17d5-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e17d5-130">Click New.</span></span>
17. <span data-ttu-id="e17d5-131">Sisestage või valige väärtus KM ID, DEU väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="e17d5-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="e17d5-132">Valige väljal Registreerimiskategooria väärtus KM ID.</span><span class="sxs-lookup"><span data-stu-id="e17d5-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="e17d5-133">Määrake varem loodud registreerimistüüp eelmääratletud registreerimiskategooriale.</span><span class="sxs-lookup"><span data-stu-id="e17d5-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="e17d5-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e17d5-134">Click New.</span></span>
20. <span data-ttu-id="e17d5-135">Sisestage või valige väärtus KM ID, ITA väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="e17d5-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="e17d5-136">Valige väljal Registreerimiskategooria väärtus KM ID.</span><span class="sxs-lookup"><span data-stu-id="e17d5-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="e17d5-137">Määrake loodud registreerimistüüp eelmääratletud registreerimiskategooriale.</span><span class="sxs-lookup"><span data-stu-id="e17d5-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="e17d5-138">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e17d5-138">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]