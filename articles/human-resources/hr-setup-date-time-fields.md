---
title: Kuupäeva ja kellaaja väljade mõistmine
description: Saate teada, mida oodata kuupäeva ja kellaaja väljade kasutamisel rakenduses Microsoft Dynamics 365 Human Resources. Saate selgust, mida oodata kuupäeva ja kellaaja andmetega suhtlemisel rakenduses Human Resources, välises allikas või teenuses Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 027e46d53fd9704f5483e90409be53c1510e8cd4
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529848"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="ef9a7-104">Kuupäeva ja kellaaja väljade mõistmine</span><span class="sxs-lookup"><span data-stu-id="ef9a7-104">Understand Date and Time fields</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ef9a7-105">**Kuupäeva ja kellaaja** väljad on põhimõiste rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ef9a7-106">Oluline on mõista, kuidas töötada **kuupäeva ja kellaaja** andmetega rakenduse Dynamics 365 Human Resources vormidel, teenuses Common Data Service ja välistes allikates.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="ef9a7-107">Kuupäeva ja kuupäeva ning kellaaja andmetüüpide erinevuse mõistmine</span><span class="sxs-lookup"><span data-stu-id="ef9a7-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="ef9a7-108">**Kuupäeva ja kellaaja** väljad sisaldavad ajavööndi teavet, kuid **kuupäeva** väljad mitte.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="ef9a7-109">**Kuupäeva** väljadel kuvatakse sama teave igas asukohas.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="ef9a7-110">Kui sisestate **kuupäeva** väljale kuupäeva, kirjutab Human Resources andmebaasi sama kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="ef9a7-111">Kui kuvate andmeid väljal **Kuupäev ja kellaaeg**, kohandab Human Resources kuupäeva ja kellaaja vastavalt kasutaja ajavööndile, mis on seatud vormis **Kasutaja valikud** (**Üldine > Häälestus > Kasutaja valikud**).</span><span class="sxs-lookup"><span data-stu-id="ef9a7-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="ef9a7-112">Väljale sisestatud kuupäeva ja kellaaja teave ei pruugi olla sama, mis andmebaasi kirjutatud teave.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="ef9a7-113">[![Kasutaja valikute vorm](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="ef9a7-114">Kuupäeva ja kellaaja väljadest arusaamine vormides</span><span class="sxs-lookup"><span data-stu-id="ef9a7-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="ef9a7-115">Andmete sisestamisel väljale **kuupäev ja kellaaeg** ei ole ekraanil kuvatavad andmed andmebaasi salvestatud andmetega samad, kui kasutaja ajavööndiks ei ole seatud UTC.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="ef9a7-116">**Kuupäeva ja kellaaja** väljade andmed talletatakse alati UTC-s.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="ef9a7-117">[![Töötaja vorm](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="ef9a7-118">Kuupäeva ja kellaaja väljadest arusaamine andmebaasis</span><span class="sxs-lookup"><span data-stu-id="ef9a7-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="ef9a7-119">Kui Human Resources kirjutab andmebaasi **kuupäeva ja kellaaja** väärtuse, talletatakse andmed UTC-s.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="ef9a7-120">See võimaldab kasutajatel näha mis tahes **kuupäeva ja kellaaja** andmeid võrreldes nende kasutaja valikutes määratletud ajavööndiga.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="ef9a7-121">Ülaltoodud näites on algusaeg ajahetk, mitte konkreetne kuupäev.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="ef9a7-122">Muutes sisselogitud kasutaja ajavööndit GMT + 12:00 kuni GMT UTC, näitab just loodud kirje 05/01/2019 12:00:00 asemel 04/30/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="ef9a7-123">Alltoodud näites muutub töötaja 000724 töösuhe aktiivseks samal ajal, sõltumata ajavööndist.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="ef9a7-124">Töötaja on aktiivne 04/30/2019 GMT ajavööndis, mis on sama, mis 05/01/2019 GMT + 12:00-ajavöönd.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="ef9a7-125">Mõlemad viitavad samale ajale ja mitte kindlale kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="ef9a7-126">[![Töötaja vorm](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="ef9a7-127">Kuupäeva ja kellaaja andmed andmehaldusraamistikus, Excelis, ühises andmeteenuses Common Data Service ja teenuses Power BI.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="ef9a7-128">Andmete halduse raamistik, Exceli lisandmoodul, Common Data Service ja Power BI aruandlus on kõik loodud, et suhelda andmetega otse andmebaasi tasemel.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="ef9a7-129">Kuna puudub klient, kelle jaoks **kuupäeva ja kellaaja** andmeid kasutaja ajavööndiga korrigeerida, on kõik **kuupäeva ja kellaaja** väärtused UTC-s, mis võib põhjustada mõningaid valesid oletusi, kui sisestate või vaatate andmeid.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="ef9a7-130">**Kuupäeva ja kellaaja** andmete puhul, mis esitatakse DMFi kaudu, Excelis või teenuses Common Data Service, eeldatakse, et andmebaas on UTC-s.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="ef9a7-131">See võib tekitada segadust, kui esitatud **kuupäeva ja kellaaja** väärtust ei kuvata ootuspäraselt, kuna andmeid vaataval kasutajal pole kasutaja ajavööndiks seatud UTC.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="ef9a7-132">Sama asi võib juhtuda, kui andmeid eksporditakse vastupidiselt.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="ef9a7-133">Eksporditud DMF-üksuse **kuupäeva ja kellaaga** andmed võivad olla erinevad sellest, mis kuvatakse Dynamics clientis.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="ef9a7-134">Kui kasutate välisallikaid, nagu DMF, et vaadata või luua andmeid, on oluline meeles pidada, et **kuupäeva ja kellaaja** väärtusi arvestatakse vaikimisi UTC-s, hoolimata kasutaja arvuti või selle praeguse kasutaja ajavööndi sätete ajavööndist.</span><span class="sxs-lookup"><span data-stu-id="ef9a7-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="ef9a7-135">Erinevates tootepiirkondades kuvatud sama kirje näited</span><span class="sxs-lookup"><span data-stu-id="ef9a7-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="ef9a7-136">**Rakenduse Human Resources kasutaja ajavööndiks on seatud UTC**</span><span class="sxs-lookup"><span data-stu-id="ef9a7-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="ef9a7-137">[![Töötaja vorm](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="ef9a7-138">**Rakenduse Human Resources kasutaja ajavööndiks on seatud GMT +12.00**</span><span class="sxs-lookup"><span data-stu-id="ef9a7-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="ef9a7-139">[![Töötaja vorm](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="ef9a7-140">**Excel OData kaudu**</span><span class="sxs-lookup"><span data-stu-id="ef9a7-140">**Excel Via OData**</span></span>

<span data-ttu-id="ef9a7-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="ef9a7-142">**DMFi ajastamine**</span><span class="sxs-lookup"><span data-stu-id="ef9a7-142">**DMF Staging**</span></span>

<span data-ttu-id="ef9a7-143">[![DMFi ajastamine](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="ef9a7-144">**DMFi eksport**</span><span class="sxs-lookup"><span data-stu-id="ef9a7-144">**DMF Export**</span></span>

<span data-ttu-id="ef9a7-145">[![DMFi ajastamine](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="ef9a7-146">**Excel läbi Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="ef9a7-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="ef9a7-147">[![Excel läbi Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="ef9a7-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="ef9a7-148">Vt ka</span><span class="sxs-lookup"><span data-stu-id="ef9a7-148">See also</span></span>

[<span data-ttu-id="ef9a7-149">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="ef9a7-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="ef9a7-150">Kasutaja eelistatud ajavöönd</span><span class="sxs-lookup"><span data-stu-id="ef9a7-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
