---
title: EUR-00015 KM ID seadistamine
description: See protseduur selgitab KM ID registreerimise eeltingimusi, nt registreerimistüübi seadistamist ja selle määramist registreerimiskategooriale.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bf6fe6926a7cc1aecb1f0a2bb7f3c47cc8828e8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144318"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="a45d7-103">EUR-00015 KM ID seadistamine</span><span class="sxs-lookup"><span data-stu-id="a45d7-103">EUR-00015 Set up VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a45d7-104">See protseduur selgitab KM ID registreerimise eeltingimusi, nt registreerimistüübi seadistamist ja selle määramist registreerimiskategooriale.</span><span class="sxs-lookup"><span data-stu-id="a45d7-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="a45d7-105">Lisateavet registreerimise ID-de ja registreerimise ID töötlemise kohta, sealhulgas nõutavad eeltingimused, leiate spikriteemast Registreerimise ID-d.</span><span class="sxs-lookup"><span data-stu-id="a45d7-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="a45d7-106">Siin antud teave kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="a45d7-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="a45d7-107">Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmaseks aadressiks on Saksamaa, andmeid.</span><span class="sxs-lookup"><span data-stu-id="a45d7-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="a45d7-108">See ülesanne on mõeldud süsteemi administraatoritele.</span><span class="sxs-lookup"><span data-stu-id="a45d7-108">This task is intended for system administrators.</span></span> <span data-ttu-id="a45d7-109">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="a45d7-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="a45d7-110">Avage Organisatsioonihaldus > Globaalne aadressiraamat > Registreerimistüübid > Registreerimistüübid.</span><span class="sxs-lookup"><span data-stu-id="a45d7-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="a45d7-111">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a45d7-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="a45d7-112">Tippige KM ID väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a45d7-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="a45d7-113">KM-kood väljal Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="a45d7-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="a45d7-114">Sisestage või valige väärtus DEU väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="a45d7-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="a45d7-115">Tehke väljal Kordumatu valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a45d7-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="a45d7-116">Märkige see ruut kontrollimiseks, kas KM ID on kordumatu.</span><span class="sxs-lookup"><span data-stu-id="a45d7-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="a45d7-117">Valige Jah väljal Riigi puhul esmane.</span><span class="sxs-lookup"><span data-stu-id="a45d7-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="a45d7-118">Märkige see ruut, kui KM ID peaks kehtima kõigi määratud riigi/regiooni aadresside puhul.</span><span class="sxs-lookup"><span data-stu-id="a45d7-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="a45d7-119">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="a45d7-119">Click Create.</span></span>
9. <span data-ttu-id="a45d7-120">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a45d7-120">Click Add.</span></span>
10. <span data-ttu-id="a45d7-121">Sisestage või valige väärtus ITA väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="a45d7-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="a45d7-122">Tippige väljale Vorming ###########.</span><span class="sxs-lookup"><span data-stu-id="a45d7-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="a45d7-123">Seda tüüpi registreerimisnumbri sisestamisel valitud riigi/piirkonna puhul kontrollitakse registreerimise ID-d selle vormingu suhtes.</span><span class="sxs-lookup"><span data-stu-id="a45d7-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="a45d7-124">Märkige ruut Kordumatu.</span><span class="sxs-lookup"><span data-stu-id="a45d7-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="a45d7-125">Märkige see ruut kontrollimiseks, kas KM ID on kordumatu.</span><span class="sxs-lookup"><span data-stu-id="a45d7-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="a45d7-126">Märkige või tühjendage ruut Riigi puhul esmane.</span><span class="sxs-lookup"><span data-stu-id="a45d7-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="a45d7-127">Märkige see ruut, kui KM ID peaks kehtima kõigi määratud riigi/regiooni aadresside puhul.</span><span class="sxs-lookup"><span data-stu-id="a45d7-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="a45d7-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a45d7-128">Click Save.</span></span>
15. <span data-ttu-id="a45d7-129">Avage Organisatsioonihaldus > Globaalne aadressiraamat > Registreerimistüübid > Registreerimiskategooriad.</span><span class="sxs-lookup"><span data-stu-id="a45d7-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="a45d7-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a45d7-130">Click New.</span></span>
17. <span data-ttu-id="a45d7-131">Sisestage või valige väärtus KM ID, DEU väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="a45d7-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="a45d7-132">Valige väljal Registreerimiskategooria väärtus KM ID.</span><span class="sxs-lookup"><span data-stu-id="a45d7-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="a45d7-133">Määrake varem loodud registreerimistüüp eelmääratletud registreerimiskategooriale.</span><span class="sxs-lookup"><span data-stu-id="a45d7-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="a45d7-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a45d7-134">Click New.</span></span>
20. <span data-ttu-id="a45d7-135">Sisestage või valige väärtus KM ID, ITA väljal Riik/piirkond</span><span class="sxs-lookup"><span data-stu-id="a45d7-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="a45d7-136">Valige väljal Registreerimiskategooria väärtus KM ID.</span><span class="sxs-lookup"><span data-stu-id="a45d7-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="a45d7-137">Määrake loodud registreerimistüüp eelmääratletud registreerimiskategooriale.</span><span class="sxs-lookup"><span data-stu-id="a45d7-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="a45d7-138">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a45d7-138">Click Save.</span></span>

