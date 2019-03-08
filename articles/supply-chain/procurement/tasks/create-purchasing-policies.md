---
title: Ostupoliitikate loomine
description: See protseduur näitab, kuidas luua ostupoliitikaid, mis sobiksid teie ostu äriprotsessidega.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bd4d6f8625c91f2190e994f04cbec4548272f04
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "312895"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="ba7c6-103">Ostupoliitikate loomine</span><span class="sxs-lookup"><span data-stu-id="ba7c6-103">Create purchasing policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba7c6-104">See protseduur näitab, kuidas luua ostupoliitikaid, mis sobiksid teie ostu äriprotsessidega.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-104">This procedure shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="ba7c6-105">Enne ostupoliitikate loomist peate seadistama ostupoliitika parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="ba7c6-106">Ostupoliitikat on võimalik luua, muuta ja aegunuks määrata, kuid ostupoliitikat ei saa kustutada.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-106">It’s possible to create, modify, and retire a purchasing policy, but you can’t delete a purchasing policy.</span></span> <span data-ttu-id="ba7c6-107">Seda protseduuri viib tavaliselt läbi ostujuht.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="ba7c6-108">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="ba7c6-109">Saate häälestada poliitikaparameetrid</span><span class="sxs-lookup"><span data-stu-id="ba7c6-109">Set up policy parameters</span></span>
1. <span data-ttu-id="ba7c6-110">Avage jaotis Ostupoliitikad.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-110">Go to Purchasing policies.</span></span>
2. <span data-ttu-id="ba7c6-111">Klõpsake valikut Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-111">Click Parameters.</span></span>
    * <span data-ttu-id="ba7c6-112">Poliitika tähtsusjärjestuse reeglid kehtivad teie organisatsiooni erinevatele tasanditele.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="ba7c6-113">Kuvatavad organisatsiooniüksused olenevad teie organisatsiooni hierarhiast ja sellest, millistele hierarhia tasanditele on hanke sisekontrolli eesmärk määratud.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="ba7c6-114">Näiteks võib teie organisatsioonil olla juriidilisi isikuid, kulukeskusi, regioone ja osakondi, kuid vaid mõnel neist võib olla hanke sisekontrolli hierarhia eesmärk.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="ba7c6-115">Vaikimisi on saadaval organisatsiooni tüüp Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="ba7c6-116">Klõpsake vahekaarti Poliitika reegli tüübi parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-116">Click the Policy rule type parameters tab.</span></span>
4. <span data-ttu-id="ba7c6-117">Valige puult Ostupoliitika \ Ostutaotluse juhtimisreegel.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-117">In the tree, select 'Purchasing policy\Purchase requisition control rule'.</span></span>
    * <span data-ttu-id="ba7c6-118">Teie määrate poliitika tasandil poliitika otsuste tähtsuse järjekorra.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="ba7c6-119">Kuid mõne poliitika tüübi puhul saate alistada üksiku poliitikareegli tüüpide tähtsuse järjekorra.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="ba7c6-120">Näiteks võite määratleda ostupoliitikate tähtsuse järjekorraks: kulukeskus, osakond, ettevõte.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="ba7c6-121">Kataloogipoliitika reegli puhul võib tähtsuse järjekord olla: osakond, kulukeskus, ettevõte.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="ba7c6-122">Tähtsuse järjekorda saab muuta ainult kataloogipoliitika reeglite puhul.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="ba7c6-123">Kui töötaja taotluse loob, määratakse kuvatav kataloog töötaja osakonna, seejärel tema kulukeskuse ja seejärel tema ettevõttega seotud poliitikate alusel.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker’s department, then their cost center, and then their company.</span></span>  
    * <span data-ttu-id="ba7c6-124">Kui loetelus on mitu organisatsiooni tasandit, võite kasutada üles-/allanoolt ostutaotluse juhtimisreeglis tähtsusjärjestuse määramiseks.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-124">If there’s more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="ba7c6-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="ba7c6-126">Looge uus poliitika.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-126">Create a new policy</span></span>
1. <span data-ttu-id="ba7c6-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-127">Click New.</span></span>
2. <span data-ttu-id="ba7c6-128">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-128">In the Name field, type a value.</span></span>
3. <span data-ttu-id="ba7c6-129">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-129">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ba7c6-130">Ühe ostupoliitika saab rakendada ainult ühele organisatsiooni hierarhiale.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="ba7c6-131">Näiteks võib teil olla üks hierarhia nimega Geograafiline ja üks nimega Osakond ja kummalgi võib olla erinev ostupoliitika.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-131">For example, you could have one hierarchy called “Geographic” and one called “Department”, and have a different purchasing policy for each.</span></span>  
    * <span data-ttu-id="ba7c6-132">Valige organisatsioon, millele poliitika peaks kehtima.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="ba7c6-133">Klõpsake noolt valitud organisatsiooni lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-133">Click the arrow to add the selected organization.</span></span>
    * <span data-ttu-id="ba7c6-134">Seda protsessi saab korrata, lisades veel organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="ba7c6-135">Poliitikareegli lisamine</span><span class="sxs-lookup"><span data-stu-id="ba7c6-135">Add a policy rule</span></span>
1. <span data-ttu-id="ba7c6-136">Tehke loendis Poliitikareegli tüüp valik Taotluse eesmärgi reegel.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-136">In the Policy rule type list, select Requisition purpose rule.</span></span>
    * <span data-ttu-id="ba7c6-137">Saate luua reegli, mis määrab taotluse vaike-eesmärgi tüübiks tarbimise, kuid laseb selle asemel valida tüübi Täiendamine.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-137">You’ll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="ba7c6-138">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-138">Click Create policy rule.</span></span>
3. <span data-ttu-id="ba7c6-139">Tehke väljal Luba käsitsi alistamine valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-139">Select Yes in the Allow manual override field.</span></span>
4. <span data-ttu-id="ba7c6-140">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-140">Click Close.</span></span>
    * <span data-ttu-id="ba7c6-141">Nüüd saate seadistada ostupoliitikale teisi poliitikareegleid.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-141">Now you can set up other policy rules for the purchasing policy.</span></span>   <span data-ttu-id="ba7c6-142">Pange tähele, et poliitikareegli tüübil ei saa olla kattuvaid reegleid, mis on ühes hankepoliitikas korraga aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  
5. <span data-ttu-id="ba7c6-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-143">Close the page.</span></span>
6. <span data-ttu-id="ba7c6-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ba7c6-144">Close the page.</span></span>

