---
title: Osakondade loomine ja nende kaasamine osakonnahierarhiasse
description: Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala. Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid. Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks. Osakonnad võivad vastutada kasumi ja kahjumi eest.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 99ecdb936071c2c71dbfae1277d20aa6dc9ef0ca
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008788"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a><span data-ttu-id="9ee46-106">Osakondade loomine ja nende kaasamine osakonnahierarhiasse</span><span class="sxs-lookup"><span data-stu-id="9ee46-106">Create departments and include them in the department hierarchy</span></span>

<span data-ttu-id="9ee46-107">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala.</span><span class="sxs-lookup"><span data-stu-id="9ee46-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="9ee46-108">Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid.</span><span class="sxs-lookup"><span data-stu-id="9ee46-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="9ee46-109">Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="9ee46-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="9ee46-110">Osakonnad võivad vastutada kasumi ja kahjumi eest.</span><span class="sxs-lookup"><span data-stu-id="9ee46-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="9ee46-111">Osakond võib sisaldada kulukeskuste gruppi.</span><span class="sxs-lookup"><span data-stu-id="9ee46-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="9ee46-112">Ametikohti saab määrata osakondadele.</span><span class="sxs-lookup"><span data-stu-id="9ee46-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="9ee46-113">Osakonna loomiseks klõpsake valikuid **Inimressursid** &gt; **Osakonnad** &gt; **Osakonnad**.</span><span class="sxs-lookup"><span data-stu-id="9ee46-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="9ee46-114">Järgmises tabelis on kirjeldatud saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="9ee46-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="9ee46-115">Väli</span><span class="sxs-lookup"><span data-stu-id="9ee46-115">Field</span></span>               | <span data-ttu-id="9ee46-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9ee46-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee46-117">Nimi</span><span class="sxs-lookup"><span data-stu-id="9ee46-117">Name</span></span>                | <span data-ttu-id="9ee46-118">Sisestage osakonnale nimi.</span><span class="sxs-lookup"><span data-stu-id="9ee46-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="9ee46-119">Osakonna number</span><span class="sxs-lookup"><span data-stu-id="9ee46-119">Department number</span></span>   | <span data-ttu-id="9ee46-120">Vaikeväärtus võidakse luua automaatselt, kui viitele **Organisatsiooni kood** lehel **Numbriseeriad** määratakse numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="9ee46-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="9ee46-121">Otsingunimi</span><span class="sxs-lookup"><span data-stu-id="9ee46-121">Search name</span></span>         | <span data-ttu-id="9ee46-122">Sisestage nimi või lühend, mida osakonna otsimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="9ee46-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="9ee46-123">Memo</span><span class="sxs-lookup"><span data-stu-id="9ee46-123">Memo</span></span>                | <span data-ttu-id="9ee46-124">Sisestage kogu lisateave siia.</span><span class="sxs-lookup"><span data-stu-id="9ee46-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="9ee46-125">Hierarhias</span><span class="sxs-lookup"><span data-stu-id="9ee46-125">In hierarchy</span></span>        | <span data-ttu-id="9ee46-126">Valitud ruut näitab, et osakond on lisatud osakonnahierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="9ee46-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="9ee46-127">Lisateavet osakonna lisamise kohta osakonnahierarhiasse vt järgnevat artikli teavet.</span><span class="sxs-lookup"><span data-stu-id="9ee46-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="9ee46-128">DUNS-number</span><span class="sxs-lookup"><span data-stu-id="9ee46-128">DUNS number</span></span>         | <span data-ttu-id="9ee46-129">DUNS tähendab andmete universaalset nummerdussüsteemi.</span><span class="sxs-lookup"><span data-stu-id="9ee46-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="9ee46-130">See on üheksakohaline number, mille väljastab Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="9ee46-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="9ee46-131">Juhataja</span><span class="sxs-lookup"><span data-stu-id="9ee46-131">Manager</span></span>             | <span data-ttu-id="9ee46-132">Sisestage isik, kes osakonda juhib.</span><span class="sxs-lookup"><span data-stu-id="9ee46-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="9ee46-133">Aadressid</span><span class="sxs-lookup"><span data-stu-id="9ee46-133">Addresses</span></span>           | <span data-ttu-id="9ee46-134">Lisage osakonna aadress.</span><span class="sxs-lookup"><span data-stu-id="9ee46-134">Add the address information for the department.</span></span> <span data-ttu-id="9ee46-135">Näiteks lisage hoone postiaadress, kus osakond asub.</span><span class="sxs-lookup"><span data-stu-id="9ee46-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="9ee46-136">Kontaktteave</span><span class="sxs-lookup"><span data-stu-id="9ee46-136">Contact information</span></span> | <span data-ttu-id="9ee46-137">Lisage osakonna kontakkteave.</span><span class="sxs-lookup"><span data-stu-id="9ee46-137">Add contact information for the department.</span></span> <span data-ttu-id="9ee46-138">Näiteks lisage osakonna kasutajatoe telefoninumber.</span><span class="sxs-lookup"><span data-stu-id="9ee46-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="9ee46-139">Osakonna lisamiseks osakonnahierarhiasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9ee46-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="9ee46-140">Klõpsake valikuid **Inimressursid** &gt; **Osakonnad** &gt; **Osakonnahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="9ee46-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="9ee46-141">Klõpsake suvandit **Redigeeri** ja valige seejärel organisatsioon, mille alla peaks osakond kuuluma.</span><span class="sxs-lookup"><span data-stu-id="9ee46-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="9ee46-142">Klõpsake suvandit **Sisesta** ja valige loendist suvand **Osakond**.</span><span class="sxs-lookup"><span data-stu-id="9ee46-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="9ee46-143">Valige ilmuvast osakondade loendist hierarhiasse lisatav osakond.</span><span class="sxs-lookup"><span data-stu-id="9ee46-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="9ee46-144">Salvestage muudatused.</span><span class="sxs-lookup"><span data-stu-id="9ee46-144">Save your changes.</span></span> <span data-ttu-id="9ee46-145">Saate teate, et loodud on hierarhia mustandversioon.</span><span class="sxs-lookup"><span data-stu-id="9ee46-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="9ee46-146">Kui olete lõpetanud, klõpsake hierarhiakujundajas valikut **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="9ee46-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="9ee46-147">Saate sisestada jõustumiskuupäeva, mis näitab, millal hierarhia avaldada.</span><span class="sxs-lookup"><span data-stu-id="9ee46-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="9ee46-148">Näiteks uue osakonna lisamiseks järgmise kalendriaasta alguses määrake jõustumiskuupäevaks uue kalendriaasta 1. jaanuar.</span><span class="sxs-lookup"><span data-stu-id="9ee46-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="9ee46-149">Muudatused hierarhias jüustuvad sel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="9ee46-149">The changes to the hierarchy will take effect on that date.</span></span>

## <a name="steps-for-creating-a-department"></a><span data-ttu-id="9ee46-150">Osakonna loomise juhised</span><span class="sxs-lookup"><span data-stu-id="9ee46-150">Steps for creating a department</span></span>
<span data-ttu-id="9ee46-151">Uue osakonna loomise etapiviisilise protseduuri leiate artiklist [Uute osakondade määratlemine](../fin-and-ops/hr/tasks/define-new-departments.md).</span><span class="sxs-lookup"><span data-stu-id="9ee46-151">Refer to the [Define new departments](../fin-and-ops/hr/tasks/define-new-departments.md) article for the step-by-step procedure for creating a new department.</span></span> 