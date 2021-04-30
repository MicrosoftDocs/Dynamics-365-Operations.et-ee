---
title: Kuupäeva ja kellaaja väljade mõistmine
description: Saate teada, mida oodata kuupäeva ja kellaaja väljade kasutamisel rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a8bc27bb4560b4a15aef483ff465c4b943bf02b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889880"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="1aad1-103">Kuupäeva ja kellaaja väljade ülevaade</span><span class="sxs-lookup"><span data-stu-id="1aad1-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1aad1-104">**Kuupäeva ja kellaaja** väljad on põhimõiste rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1aad1-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1aad1-105">Oluline on mõista, kuidas töötada **Kuupäeva ja kellaaja** andmetega rakenduse Dataverse vormidel, teenuses ja välistes allikates.</span><span class="sxs-lookup"><span data-stu-id="1aad1-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="1aad1-106">Kuupäeva ja kuupäeva ning kellaaja andmetüüpide erinevuse mõistmine</span><span class="sxs-lookup"><span data-stu-id="1aad1-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="1aad1-107">**Kuupäeva ja kellaaja** väljad sisaldavad ajavööndi teavet, kuid **kuupäeva** väljad mitte.</span><span class="sxs-lookup"><span data-stu-id="1aad1-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="1aad1-108">**Kuupäeva** väljadel kuvatakse sama teave igas asukohas.</span><span class="sxs-lookup"><span data-stu-id="1aad1-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="1aad1-109">Kui sisestate **kuupäeva** väljale kuupäeva, kirjutab Human Resources andmebaasi sama kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="1aad1-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="1aad1-110">Kui kuvate andmeid väljal **Kuupäev ja kellaaeg**, kohandab Human Resources kuupäeva ja kellaaja vastavalt kasutaja ajavööndile, mis on seatud vormis **Kasutaja valikud** (**Üldine > Häälestus > Kasutaja valikud**).</span><span class="sxs-lookup"><span data-stu-id="1aad1-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="1aad1-111">Väljale sisestatud kuupäeva ja kellaaja teave ei pruugi olla sama, mis andmebaasi kirjutatud teave.</span><span class="sxs-lookup"><span data-stu-id="1aad1-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="1aad1-112">[![Kasutaja valikute vorm](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="1aad1-113">Kuupäeva ja kellaaja väljadest arusaamine vormides</span><span class="sxs-lookup"><span data-stu-id="1aad1-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="1aad1-114">Ekraanil kuvatavad **kuupäev ja kellaaeg** ei ole andmebaasi salvestatud andmetega samad, kui kasutaja ajavööndiks ei ole seatud UTC.</span><span class="sxs-lookup"><span data-stu-id="1aad1-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1aad1-115">**Kuupäeva ja kellaaja** väljade andmed talletatakse alati UTC-s.</span><span class="sxs-lookup"><span data-stu-id="1aad1-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="1aad1-116">[![Töötaja vormi UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="1aad1-117">Kuupäeva ja kellaaja väljadest arusaamine andmebaasis</span><span class="sxs-lookup"><span data-stu-id="1aad1-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="1aad1-118">Kui Human Resources kirjutab andmebaasi **kuupäeva ja kellaaja** väärtuse, talletatakse andmed UTC-s.</span><span class="sxs-lookup"><span data-stu-id="1aad1-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="1aad1-119">See võimaldab kasutajatel näha mis tahes **kuupäeva ja kellaaja** andmeid võrreldes nende kasutaja valikutes määratletud ajavööndiga.</span><span class="sxs-lookup"><span data-stu-id="1aad1-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="1aad1-120">Ülaltoodud näites on algusaeg ajahetk, mitte konkreetne kuupäev.</span><span class="sxs-lookup"><span data-stu-id="1aad1-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="1aad1-121">Muutes sisselogitud kasutaja ajavööndit GMT + 12:00 kuni GMT UTC, näitab kirje 05/01/2019 12:00:00 asemel 04/30/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="1aad1-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="1aad1-122">Alltoodud näites muutub töötaja 000724 töösuhe aktiivseks samal ajal, sõltumata ajavööndist.</span><span class="sxs-lookup"><span data-stu-id="1aad1-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="1aad1-123">Töötaja on aktiivne 04/30/2019 GMT ajavööndis, mis on sama, mis 05/01/2019 GMT + 12:00-ajavöönd.</span><span class="sxs-lookup"><span data-stu-id="1aad1-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="1aad1-124">Mõlemad viitavad samale ajale ja mitte kindlale kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="1aad1-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="1aad1-125">[![Töötaja vormi GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="1aad1-126">Kuupäeva ja kellaaja andmed andmehaldusraamistikus, Excelis, ühises andmeteenuses Dataverse ja teenuses Power BI.</span><span class="sxs-lookup"><span data-stu-id="1aad1-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="1aad1-127">Andmete halduse raamistik, Exceli lisandmoodul, Dataverse ja Power BI aruandlus on kõik loodud, et suhelda andmetega otse andmebaasi tasemel.</span><span class="sxs-lookup"><span data-stu-id="1aad1-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="1aad1-128">Kuna puudub klient, kelle jaoks **kuupäeva ja kellaaja** andmeid kasutaja ajavööndiga korrigeerida, on kõik **kuupäeva ja kellaaja** väärtused UTC-s, mis võib põhjustada mõningaid valesid oletusi, kui sisestate või vaatate andmeid.</span><span class="sxs-lookup"><span data-stu-id="1aad1-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="1aad1-129">**Kuupäeva ja kellaaja** andmete puhul, mis esitatakse DMFi kaudu, Excelis või teenuses Dataverse, eeldatakse, et andmebaas on UTC-s.</span><span class="sxs-lookup"><span data-stu-id="1aad1-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="1aad1-130">See võib tekitada segadust, kui esitatud **kuupäeva ja kellaaja** väärtust ei kuvata ootuspäraselt, kuna andmeid vaataval kasutajal pole kasutaja ajavööndiks seatud UTC.</span><span class="sxs-lookup"><span data-stu-id="1aad1-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="1aad1-131">Sama asi võib juhtuda, kui andmeid eksporditakse vastupidiselt.</span><span class="sxs-lookup"><span data-stu-id="1aad1-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="1aad1-132">Eksporditud DMF-üksuse **kuupäeva ja kellaaga** andmed võivad olla erinevad sellest, mis kuvatakse Dynamics clientis.</span><span class="sxs-lookup"><span data-stu-id="1aad1-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="1aad1-133">Kui kasutate välisallikaid, nagu DMF, et vaadata või luua andmeid, pidage meeles, et **kuupäeva ja kellaaja** väärtusi arvestatakse vaikimisi UTC-s, hoolimata kasutaja arvuti või selle praeguse kasutaja ajavööndi sätete ajavööndist.</span><span class="sxs-lookup"><span data-stu-id="1aad1-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="1aad1-134">Erinevates tootepiirkondades kuvatud sama kirje näited</span><span class="sxs-lookup"><span data-stu-id="1aad1-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="1aad1-135">**Rakenduse Human Resources kasutaja ajavööndiks on seatud UTC**</span><span class="sxs-lookup"><span data-stu-id="1aad1-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="1aad1-136">[![Töötaja vorm seatud UTC-le](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="1aad1-137">**Rakenduse Human Resources kasutaja ajavööndiks on seatud GMT +12.00**</span><span class="sxs-lookup"><span data-stu-id="1aad1-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="1aad1-138">[![Töötaja vorm seatud GMT-le](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="1aad1-139">**Excel OData kaudu**</span><span class="sxs-lookup"><span data-stu-id="1aad1-139">**Excel Via OData**</span></span>

<span data-ttu-id="1aad1-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="1aad1-141">**DMFi ajastamine**</span><span class="sxs-lookup"><span data-stu-id="1aad1-141">**DMF Staging**</span></span>

<span data-ttu-id="1aad1-142">[![DMFi ajastamine](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="1aad1-143">**DMFi eksport**</span><span class="sxs-lookup"><span data-stu-id="1aad1-143">**DMF Export**</span></span>

<span data-ttu-id="1aad1-144">[![DMF eksport](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="1aad1-145">**Excel läbi Dataverse**</span><span class="sxs-lookup"><span data-stu-id="1aad1-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="1aad1-146">[![Excel läbi Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="1aad1-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="1aad1-147">Vt ka</span><span class="sxs-lookup"><span data-stu-id="1aad1-147">See also</span></span>

[<span data-ttu-id="1aad1-148">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="1aad1-148">Date and time data</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="1aad1-149">Kasutaja eelistatud ajavöönd</span><span class="sxs-lookup"><span data-stu-id="1aad1-149">User preferred time zones</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]