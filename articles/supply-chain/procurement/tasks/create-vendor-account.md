---
title: Hankija konto loomine
description: See protseduur selgitab, kuidas luua hankijakontot ning lisada aadressi ja kontaktteavet.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017203"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="5d61b-103">Hankija konto loomine</span><span class="sxs-lookup"><span data-stu-id="5d61b-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d61b-104">See protseduur selgitab, kuidas luua hankijakontot ning lisada aadressi ja kontaktteavet.</span><span class="sxs-lookup"><span data-stu-id="5d61b-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="5d61b-105">Protseduur ei näita, kuidas täita kõiki välju ostmiseks ja lõplikuks eesmärgiks.</span><span class="sxs-lookup"><span data-stu-id="5d61b-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="5d61b-106">Lisateavet nende väljade kohta leiate väljade kirjeldusest.</span><span class="sxs-lookup"><span data-stu-id="5d61b-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="5d61b-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="5d61b-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="5d61b-108">Hankijakontod loob tavaliselt hankespetsialist või müügireskontro personal.</span><span class="sxs-lookup"><span data-stu-id="5d61b-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="5d61b-109">Hankija konto loomine</span><span class="sxs-lookup"><span data-stu-id="5d61b-109">Create a vendor account</span></span>
1. <span data-ttu-id="5d61b-110">Avage **Navigeerimispaan > Moodulid > Hanked > Hankijad > Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="5d61b-111">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-111">Click **New**.</span></span>
3. <span data-ttu-id="5d61b-112">Sisestage väärtus väljale **Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="5d61b-113">Väärtus võidakse sisestada automaatselt.</span><span class="sxs-lookup"><span data-stu-id="5d61b-113">The value may be populated automatically.</span></span> <span data-ttu-id="5d61b-114">Sel juhul võite selle etapi vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="5d61b-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="5d61b-115">Saate luua hankijakontod isikule või organisatsioonile.</span><span class="sxs-lookup"><span data-stu-id="5d61b-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="5d61b-116">See mõjutab, millised väljad on saadaval.</span><span class="sxs-lookup"><span data-stu-id="5d61b-116">This will affect which fields are available.</span></span> <span data-ttu-id="5d61b-117">Selles näites loome organisatsioonile hankija konto.</span><span class="sxs-lookup"><span data-stu-id="5d61b-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="5d61b-118">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="5d61b-119">Kui teie hankija on süsteemis juba registreeritud osapool, saate ta sellele väljale valida ripploendi abil ning uus hankijakonto pärib juba registreeritud aadressi ja kontaktteabe.</span><span class="sxs-lookup"><span data-stu-id="5d61b-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="5d61b-120">Sisestage või valige väärtus väljal **Grupp**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="5d61b-121">Hankijagruppi kasutatakse nende hankijate grupeerimiseks, kellel on mis tahes järgmised ühised parameetrid: maksetingimused, tasakaalustusperiood, varude sisestamise pearaamatukontod, sh käibemaksugrupp, vaikepearaamatukontod, tootefiltri koodid või tarneprognoosi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="5d61b-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="5d61b-122">Sisestage arv väljale **Töötajate arv**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="5d61b-123">Sisestage väärtus väljale **Organisatsiooni number**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="5d61b-124">Aadressi lisamine</span><span class="sxs-lookup"><span data-stu-id="5d61b-124">Add an address</span></span>
1. <span data-ttu-id="5d61b-125">Laiendage jaotist **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="5d61b-126">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-126">Click **Add**.</span></span>
3. <span data-ttu-id="5d61b-127">Sisestage või valige väärtus väljal **Eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="5d61b-128">Saate valida ühe või mitu eesmärki.</span><span class="sxs-lookup"><span data-stu-id="5d61b-128">You can select one or more purposes.</span></span> <span data-ttu-id="5d61b-129">Neid kasutatakse, et valida õige aadress antud eesmärgi jaoks.</span><span class="sxs-lookup"><span data-stu-id="5d61b-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="5d61b-130">Näiteks kui eesmärk on „Arve”, kasutatakse seda aadressi arvete saatmisel.</span><span class="sxs-lookup"><span data-stu-id="5d61b-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="5d61b-131">Sisestage väärtus väljale **Nimi või kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="5d61b-132">Sisestage või valige väärtus väljale **Riik/regioon**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="5d61b-133">Sisestage aadressi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="5d61b-133">Enter the address details.</span></span> <span data-ttu-id="5d61b-134">Valitud riik/regioon määratleb teile kuvatavad väljad olenevalt selle riigi/regiooni aadressivormingust.</span><span class="sxs-lookup"><span data-stu-id="5d61b-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="5d61b-135">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="5d61b-136">Kontaktteabe lisamine</span><span class="sxs-lookup"><span data-stu-id="5d61b-136">Add contact information</span></span>
1. <span data-ttu-id="5d61b-137">Laiendage jaotist **Kontaktteave**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="5d61b-138">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-138">Click **Add**.</span></span>
3. <span data-ttu-id="5d61b-139">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="5d61b-140">Valige suvand väljalt **Tüüp**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="5d61b-141">Sisestage väärtus väljale **Kontaktnumber/aadress**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="5d61b-142">Saate valida märkeruudu Esmane, kui see on esmane kontakt.</span><span class="sxs-lookup"><span data-stu-id="5d61b-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="5d61b-143">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5d61b-143">Click **Save**.</span></span>
7. <span data-ttu-id="5d61b-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5d61b-144">Close the page.</span></span>
8. <span data-ttu-id="5d61b-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5d61b-145">Close the page.</span></span>

