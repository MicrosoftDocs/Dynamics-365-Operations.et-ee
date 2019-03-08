---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (august 2018)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talent Core HR-i uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: cdf0893835c1ee9edd89c43b3c5c842d89e6d526
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304099"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-august-2018"></a><span data-ttu-id="8c97d-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (august 2018)</span><span class="sxs-lookup"><span data-stu-id="8c97d-103">What's new or changed in Dynamics 365 for Talent Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8c97d-104">**Järk 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="8c97d-104">**Build 8.1.104**</span></span>

<span data-ttu-id="8c97d-105">Selles teemas kirjeldatakse rakenduse Dynamics 365 for Talent Core HR uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="8c97d-105">This topic describes features that are either new or changed in Dynamics 365 for Talent Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="8c97d-106">Aeguvate kirjete vaatamine juhi iseteeninduses</span><span class="sxs-lookup"><span data-stu-id="8c97d-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="8c97d-107">Aeguvaid kirjeid saab vaadata juhi iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="8c97d-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="8c97d-108">Uute suvanditega saate konfigureerida, milline teave on juhtidele vaatamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="8c97d-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="8c97d-109">Kopeeritavad väljad on järgmised.</span><span class="sxs-lookup"><span data-stu-id="8c97d-109">These include:</span></span>

-   <span data-ttu-id="8c97d-110">Serdid</span><span class="sxs-lookup"><span data-stu-id="8c97d-110">Certificates</span></span>

-   <span data-ttu-id="8c97d-111">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="8c97d-111">Identification numbers</span></span>

-   <span data-ttu-id="8c97d-112">Katseajad</span><span class="sxs-lookup"><span data-stu-id="8c97d-112">Probation periods</span></span>

-   <span data-ttu-id="8c97d-113">Skriiningud</span><span class="sxs-lookup"><span data-stu-id="8c97d-113">Screenings</span></span>

-   <span data-ttu-id="8c97d-114">Katsed</span><span class="sxs-lookup"><span data-stu-id="8c97d-114">Tests</span></span>

<span data-ttu-id="8c97d-115">Selle funktsiooniga saate ka määrata päevade vahemiku, kust aeguvaid kirjeid otsida.</span><span class="sxs-lookup"><span data-stu-id="8c97d-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="8c97d-116">Konfigureeritavad ülekandmise tegevused</span><span class="sxs-lookup"><span data-stu-id="8c97d-116">Configurable transfer actions</span></span>

<span data-ttu-id="8c97d-117">Saate rolli järgi konfigureerida suvandeid, mis on saadaval ülekandmise taotluse sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="8c97d-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="8c97d-118">See funktsioon lisab paindlikkust organisatsiooni rollidele.</span><span class="sxs-lookup"><span data-stu-id="8c97d-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="8c97d-119">Näiteks juhtidel, kes taotlevad töötaja ülekandmisi, ei pruugi olla juurdepääsu tasusummade pakkumiseks või sisestamiseks või ülekandmise nõudega seostatavate ülesandeloendite valimiseks.</span><span class="sxs-lookup"><span data-stu-id="8c97d-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="8c97d-120">Sellisel juhul saavad juhid luua ja edastada ülekandmise taotlusi, aga neil pole lubatud sisestada kompensatsiooni või ülesandeloendi määramisi.</span><span class="sxs-lookup"><span data-stu-id="8c97d-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="8c97d-121">Samas konfiguratsioonis saab personaliosakond määrata uued tasuväärtused ja täiendavad kontroll-loendid, mis tuleb lõpule viia ülekandmise lõpetamise tulemusena.</span><span class="sxs-lookup"><span data-stu-id="8c97d-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="8c97d-122">Vaikimisi määratakse uued konfigureerimissuvandid nii, et need ei muuda võimalusi enne seda värskendust.</span><span class="sxs-lookup"><span data-stu-id="8c97d-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="8c97d-123">Puhkused ja puudumine</span><span class="sxs-lookup"><span data-stu-id="8c97d-123">Leave and absence</span></span>

<span data-ttu-id="8c97d-124">Puhkustes ja puudumistes on nüüd saadaval täiendavad kuupäevaväljad.</span><span class="sxs-lookup"><span data-stu-id="8c97d-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="8c97d-125">Selle funktsiooniga saate määrata lisandumisperioodi aluse plaani tasemel, et kasutada konkreetseid töötamise kuupäevi.</span><span class="sxs-lookup"><span data-stu-id="8c97d-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="8c97d-126">Tänu sellele saab puhkuse lisandumisprotsessi ajal kasutada muid kuupäevi peale plaani alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="8c97d-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="8c97d-127">Töövõtjakohaste kuupäevade suvandid hõlmavad järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="8c97d-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="8c97d-128">Kohandatud (saadaval enne seda värskendust)</span><span class="sxs-lookup"><span data-stu-id="8c97d-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="8c97d-129">Tähtpäeva kuupäev</span><span class="sxs-lookup"><span data-stu-id="8c97d-129">Anniversary date</span></span>

-   <span data-ttu-id="8c97d-130">Värbamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="8c97d-130">Original hire date</span></span>

-   <span data-ttu-id="8c97d-131">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="8c97d-131">Seniority date</span></span>

-   <span data-ttu-id="8c97d-132">Töötaja töösuhte korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c97d-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="8c97d-133">Töötaja töösuhte alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c97d-133">Worker’s start date</span></span>

<span data-ttu-id="8c97d-134">Kui konfigureeritud on töövõtjakohaste kuupäevade kasutamine, kasutatakse registreerimisprotsessi määratud kuupäeva lisandumisperioodide arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8c97d-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="8c97d-135">Lisandumisperioodi alus kuvatakse ka töövõtja plaani registreerimisel, et mõistaksite, mida lisandumisprotsessis kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="8c97d-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="8c97d-136">Microsoft Word integratsioon</span><span class="sxs-lookup"><span data-stu-id="8c97d-136">Microsoft Word integration</span></span>

<span data-ttu-id="8c97d-137">Dokumendimallid on lubatud terves Core HR-is.</span><span class="sxs-lookup"><span data-stu-id="8c97d-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="8c97d-138">Selle funktsiooniga saate luua kirju ja aruandeid loodud Wordi mallide põhjal.</span><span class="sxs-lookup"><span data-stu-id="8c97d-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="8c97d-139">Lisateavet selle funktsiooni kohta leiate teemast [Office’i integreerimise õppetükk](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span><span class="sxs-lookup"><span data-stu-id="8c97d-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="8c97d-140">Muud parandused</span><span class="sxs-lookup"><span data-stu-id="8c97d-140">Other fixes</span></span>

<span data-ttu-id="8c97d-141">Selles versioonis on ka hulk programmivigade parandusi, lisatud on uus üksusi, parandatud on olemasolevaid üksus ja muudetud on lokaliseeritud silte.</span><span class="sxs-lookup"><span data-stu-id="8c97d-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
