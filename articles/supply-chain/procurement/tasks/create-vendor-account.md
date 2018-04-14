--- 
title: Hankija konto loomine
description: See protseduur selgitab, kuidas luua hankijakontot ning lisada aadressi ja kontaktteavet.
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 829a0bbb1b5ab01728c096872b0ada27cfc570c9
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="5d1f4-103">Hankija konto loomine</span><span class="sxs-lookup"><span data-stu-id="5d1f4-103">Create a vendor account</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d1f4-104">See protseduur selgitab, kuidas luua hankijakontot ning lisada aadressi ja kontaktteavet.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="5d1f4-105">Protseduur ei näita, kuidas täita kõiki välju ostmiseks ja lõplikuks eesmärgiks.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="5d1f4-106">Lisateavet nende väljade kohta leiate väljade kirjeldusest.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="5d1f4-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="5d1f4-108">Hankijakontod loob tavaliselt hankespetsialist või müügireskontro personal.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="5d1f4-109">Hankija konto loomine</span><span class="sxs-lookup"><span data-stu-id="5d1f4-109">Create a vendor account</span></span>
1. <span data-ttu-id="5d1f4-110">Tehke valik Hanked > Hankijad > Kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="5d1f4-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-111">Click New.</span></span>
3. <span data-ttu-id="5d1f4-112">Sisestage väärtus väljale Hankija konto.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="5d1f4-113">Väärtus võidakse sisestada automaatselt.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-113">The value may be populated automatically.</span></span> <span data-ttu-id="5d1f4-114">Sel juhul võite selle etapi vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="5d1f4-115">Saate luua hankijakontod isikule või organisatsioonile.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="5d1f4-116">See mõjutab, millised väljad on saadaval.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-116">This will affect which fields are available.</span></span> <span data-ttu-id="5d1f4-117">Selles näites loome organisatsioonile hankija konto.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="5d1f4-118">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="5d1f4-119">Kui teie hankija on süsteemis juba registreeritud osapool, saate ta sellele väljale valida ripploendi abil ning uus hankijakonto pärib juba registreeritud aadressi ja kontaktteabe.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="5d1f4-120">Sisestage või valige väärtus väljal Grupp.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="5d1f4-121">Hankijagruppi kasutatakse nende hankijate grupeerimiseks, kellel on mis tahes järgmised ühised parameetrid: maksetingimused, tasakaalustusperiood, varude sisestamise pearaamatukontod, sh käibemaksugrupp, vaikepearaamatukontod, tootefiltri koodid või tarneprognoosi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="5d1f4-122">Sisestage arv väljale Töötajate arv.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="5d1f4-123">Sisestage väärtus väljale Organisatsiooni number.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="5d1f4-124">Aadressi lisamine</span><span class="sxs-lookup"><span data-stu-id="5d1f4-124">Add an address</span></span>
1. <span data-ttu-id="5d1f4-125">Laiendage jaotist Aadressid.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="5d1f4-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-126">Click Add.</span></span>
3. <span data-ttu-id="5d1f4-127">Sisestage või valige väärtus väljal Eesmärk.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="5d1f4-128">Saate valida ühe või mitu eesmärki.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-128">You can select one or more purposes.</span></span> <span data-ttu-id="5d1f4-129">Neid kasutatakse, et valida õige aadress antud eesmärgi jaoks.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="5d1f4-130">Näiteks kui eesmärk on Arve, kasutatakse seda aadressi arvete saatmisel.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="5d1f4-131">Sisestage väärtus väljale Nimi või kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="5d1f4-132">Sisestage või valige väärtus väljal Riik/piirkond.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="5d1f4-133">Sisestage aadressi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-133">Enter the address details.</span></span> <span data-ttu-id="5d1f4-134">Valitud riik/piirkond määratleb teile kuvatavad väljad olenevalt selle riigi/piirkonna aadressivormingust.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="5d1f4-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="5d1f4-136">Kontaktteabe lisamine</span><span class="sxs-lookup"><span data-stu-id="5d1f4-136">Add contact information</span></span>
1. <span data-ttu-id="5d1f4-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-137">Click Add.</span></span>
2. <span data-ttu-id="5d1f4-138">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="5d1f4-139">Valige suvand väljalt Tüüp.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="5d1f4-140">Sisestage väärtus väljale Kontaktnumber/aadress.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="5d1f4-141">Saate valida märkeruudu Esmane, kui see on esmane kontakt.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="5d1f4-142">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-142">Click Save.</span></span>
6. <span data-ttu-id="5d1f4-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-143">Close the page.</span></span>
7. <span data-ttu-id="5d1f4-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5d1f4-144">Close the page.</span></span>


