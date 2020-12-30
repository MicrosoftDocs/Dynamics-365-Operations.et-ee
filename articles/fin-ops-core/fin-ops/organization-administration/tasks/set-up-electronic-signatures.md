---
title: Digitaalallkirjade seadistamine
description: Kasutage seda protseduuri digitaalallkirjade seadistamiseks.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 088fe3c42b00a6a495aeee19a4e3640054a8aa2a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694761"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="f15b8-103">Digitaalallkirjade seadistamine</span><span class="sxs-lookup"><span data-stu-id="f15b8-103">Set up electronic signatures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f15b8-104">Kasutage seda protseduuri digitaalallkirjade seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="f15b8-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="f15b8-105">Elektronallkiri kinnitab isiku, kes käivitab või kinnitab protsessi.</span><span class="sxs-lookup"><span data-stu-id="f15b8-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="f15b8-106">Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid.</span><span class="sxs-lookup"><span data-stu-id="f15b8-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="f15b8-107">Digitaalallkirja konfiguratsioonivõtme lubamine</span><span class="sxs-lookup"><span data-stu-id="f15b8-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="f15b8-108">Minge jaotisse Süsteemihaldus > Seadistus > Litsentsi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="f15b8-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="f15b8-109">Laiendage puul üksust Administreerimine.</span><span class="sxs-lookup"><span data-stu-id="f15b8-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="f15b8-110">Kontrollige, kas ruut Digitaalallkirjastamine on märgitud.</span><span class="sxs-lookup"><span data-stu-id="f15b8-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="f15b8-111">Kui ruut Digitaalallkirjastamine ei ole märgitud, peate lubama hooldusrežiimi.</span><span class="sxs-lookup"><span data-stu-id="f15b8-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="f15b8-112">Hooldusrežiimi saab selles keskkonnas lubada, käivitades teenustes Lifecycle Services hooldustöö või kasutades kohalikult tööriista Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="f15b8-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="f15b8-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f15b8-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="f15b8-114">Digitaalallkirja parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="f15b8-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="f15b8-115">Minge jaotisse Organisatsiooni haldamine > Seadistus > Digitaalallkirjastamine > Digitaalallkirjastamise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="f15b8-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="f15b8-116">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f15b8-116">Click Edit.</span></span>
3. <span data-ttu-id="f15b8-117">Sisestage väärtus väljale Teade.</span><span class="sxs-lookup"><span data-stu-id="f15b8-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="f15b8-118">Sisestage teatis, mille allkirjastajad saavad allkirja nõudes.</span><span class="sxs-lookup"><span data-stu-id="f15b8-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="f15b8-119">Saate sisestada mis tahes teksti.</span><span class="sxs-lookup"><span data-stu-id="f15b8-119">You can enter any text.</span></span> <span data-ttu-id="f15b8-120">Tavaliselt kirjeldatakse kasutajale dokumendi elektronallkirjastamist.</span><span class="sxs-lookup"><span data-stu-id="f15b8-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="f15b8-121">Kui soovite sisestada teate teksti ka muudes keeltes, klõpsake nuppu Tõlked.</span><span class="sxs-lookup"><span data-stu-id="f15b8-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="f15b8-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f15b8-122">Click Save.</span></span>
5. <span data-ttu-id="f15b8-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f15b8-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="f15b8-124">Digitaalallkirjadele põhjusekoodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="f15b8-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="f15b8-125">Minge jaotisse Organisatsiooni haldamine > Seadistus > Digitaalallkirjastamine > Digitaalallkirjastamise põhjusekoodid.</span><span class="sxs-lookup"><span data-stu-id="f15b8-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="f15b8-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f15b8-126">Click New.</span></span>
    * <span data-ttu-id="f15b8-127">Põhjusekoodid peab seadistama enne elektronallkirjade kasutamist.</span><span class="sxs-lookup"><span data-stu-id="f15b8-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="f15b8-128">Dokumendi allkirjastamisel on vajalik kehtiv põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="f15b8-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="f15b8-129">Allkirjastaja valib põhjusekoodi elektronallkirja eesmärgile viitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f15b8-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="f15b8-130">Põhjusekoodi saab kasutada näiteks seaduslikule kinnitusele viitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f15b8-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="f15b8-131">Sisestage väärtus väljale Põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="f15b8-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="f15b8-132">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="f15b8-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f15b8-133">Vajaduse korral sisestage täiendavad põhjusekoodid.</span><span class="sxs-lookup"><span data-stu-id="f15b8-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="f15b8-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f15b8-134">Click Save.</span></span>
6. <span data-ttu-id="f15b8-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f15b8-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="f15b8-136">Olemasolevate protsesside digitaalalkirjastamise nõudmine</span><span class="sxs-lookup"><span data-stu-id="f15b8-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="f15b8-137">Minge jaotisse Organisatsiooni haldamine > Seadistus > Digitaalallkirjastamine > Digitaalallkirjastamise nõuded.</span><span class="sxs-lookup"><span data-stu-id="f15b8-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="f15b8-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f15b8-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f15b8-139">Saate valida digitaalallkirjastamist nõudev protsess.</span><span class="sxs-lookup"><span data-stu-id="f15b8-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="f15b8-140">Valige või tühjendage ruut Allkiri nõutav.</span><span class="sxs-lookup"><span data-stu-id="f15b8-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="f15b8-141">Korrake neid etappe iga digitaalallkirjastamist nõudva protsessi puhul.</span><span class="sxs-lookup"><span data-stu-id="f15b8-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="f15b8-142">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f15b8-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="f15b8-143">Digitaalallkirjastamiseks kohandatud nõude loomine</span><span class="sxs-lookup"><span data-stu-id="f15b8-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="f15b8-144">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f15b8-144">Click New.</span></span>
2. <span data-ttu-id="f15b8-145">Valige või tühjendage ruut Allkiri nõutav.</span><span class="sxs-lookup"><span data-stu-id="f15b8-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="f15b8-146">Sisestage väljale Nimi digitaalallkirjastamist nõudva protsessi nimi.</span><span class="sxs-lookup"><span data-stu-id="f15b8-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="f15b8-147">Klõpsake väljal Tabeli nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f15b8-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f15b8-148">Leidke ja valige loendist tabel, kuhu allkirjastatavad andmed salvestada.</span><span class="sxs-lookup"><span data-stu-id="f15b8-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="f15b8-149">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f15b8-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f15b8-150">Klõpsake väljal Välja nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f15b8-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f15b8-151">Leidke ja valige loendist tabeli välja nimi, mida soovite jälgida.</span><span class="sxs-lookup"><span data-stu-id="f15b8-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="f15b8-152">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f15b8-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f15b8-153">Määrake allkirjanõude kord.</span><span class="sxs-lookup"><span data-stu-id="f15b8-153">Specify when a signature is required.</span></span>     <span data-ttu-id="f15b8-154">Valige suvand Alati, kui allkiri on nõutav välja andmete muutumisel.</span><span class="sxs-lookup"><span data-stu-id="f15b8-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="f15b8-155">Valige suvand Ainult, kui allkiri on nõutav ainult teatud tingimustel.</span><span class="sxs-lookup"><span data-stu-id="f15b8-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="f15b8-156">Suvandi Ainult valimisel peate valima ka ühe järgmistest suvanditest: Kirje sisestamisel, Kirje värskendamisel või Kirje kustutamisel.</span><span class="sxs-lookup"><span data-stu-id="f15b8-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="f15b8-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f15b8-157">Click Save.</span></span>
11. <span data-ttu-id="f15b8-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f15b8-158">Close the page.</span></span>

