---
title: Kaubavaru omandiõiguse muutmine tootmise nõudluse põhjal
description: See protseduur näitab, kuidas määrata saadetise varude omanikuks hankija asemel teie juriidiline isik, kui on olemas nõudlus tootmises olevate varude järele.
author: perlynne
manager: AnnBe
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cf45e838afcb55e15175811f4d38be07d7a484d
ms.sourcegitcommit: 315388bba3a766691e341f9f2a4fa7a091f2aa18
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/14/2019
ms.locfileid: "1874873"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="211d1-103">Kaubavaru omandiõiguse muutmine tootmise nõudluse põhjal</span><span class="sxs-lookup"><span data-stu-id="211d1-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="211d1-104">See protseduur näitab, kuidas määrata saadetise varude omanikuks hankija asemel teie juriidiline isik, kui on olemas nõudlus tootmises olevate varude järele.</span><span class="sxs-lookup"><span data-stu-id="211d1-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="211d1-105">See omandiõiguse muutmine toimub varude omandiõiguse muutmise töölehe sisestamisega.</span><span class="sxs-lookup"><span data-stu-id="211d1-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="211d1-106">Omandiõiguse muutmise töölehe ridu saab luua käsitsi või (nagu selles salvestises näidatud) olemasoleva tootmise nõudluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="211d1-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="211d1-107">Tavaliselt teeb seda tööde järelevaataja.</span><span class="sxs-lookup"><span data-stu-id="211d1-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="211d1-108">Saate seda protseduuri kasutada demoettevõttes USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="211d1-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="211d1-109">Kui kasutate oma andmeid, siis veenduge, et teil oleksid olemas järgmised eeltingimused: varude töölehe nimi, mis on seadistatud varude omandiõiguse muutmiseks, füüsiliselt registreeritud hankijale kuuluvad vabad kaubad ja vähemalt üks materjali tootmistellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="211d1-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="211d1-110">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="211d1-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="211d1-111">Väljaminevate saadetiste protsesse ei toetata valmiskujul ja automaatset omandiõiguse päeviku töötlemist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="211d1-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="211d1-112">Varude omanikuvahetuse töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="211d1-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="211d1-113">Minge jaotisse Varud > Töölehe sisestused > Kaubad > Varude omanikuvahetus.</span><span class="sxs-lookup"><span data-stu-id="211d1-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="211d1-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="211d1-114">Click New.</span></span>
    * <span data-ttu-id="211d1-115">Varude omanikuvahetuse töölehe kaudu määratakse saadetise varude omanikuks hankija asemel praegune juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="211d1-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="211d1-116">Omanikuvahetuseks vabastatakse hankijale kuuluv vaba kaubavaru ja vormistatakse siis selle varu sissetulek praeguses juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="211d1-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="211d1-117">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="211d1-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="211d1-118">Saate valida ainult neid laotöölehtede nimesid, mille töölehe tüüp on Omanikuvahetus.</span><span class="sxs-lookup"><span data-stu-id="211d1-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="211d1-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="211d1-119">Click OK.</span></span>
5. <span data-ttu-id="211d1-120">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="211d1-120">Click Functions.</span></span>
6. <span data-ttu-id="211d1-121">Klõpsake valikut Tootmistellimustest töölehe ridade loomine.</span><span class="sxs-lookup"><span data-stu-id="211d1-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="211d1-122">Saate alustada omanikuvahetuse protsessi, esitades päringu kõigi tootmise ridade kohta, millel on tooraine tarbimise nõue.</span><span class="sxs-lookup"><span data-stu-id="211d1-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="211d1-123">Tehke valik väljal Kaasatavad lao väljamineku olekud.</span><span class="sxs-lookup"><span data-stu-id="211d1-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="211d1-124">See valik võimaldab filtreerida laokannete väljastamisoleku järgi.</span><span class="sxs-lookup"><span data-stu-id="211d1-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="211d1-125">Näiteks saate luua töölehe read varudele, mille füüsilised olekud on Komplekteeritud ja Reserveeritud.</span><span class="sxs-lookup"><span data-stu-id="211d1-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="211d1-126">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="211d1-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="211d1-127">Selles jaotises saate rakendada täiendavat filtreerimist.</span><span class="sxs-lookup"><span data-stu-id="211d1-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="211d1-128">Näiteks saate valida kindla toormaterjali kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="211d1-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="211d1-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="211d1-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="211d1-130">Varude omanikuvahetuse töölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="211d1-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="211d1-131">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="211d1-131">Click Post.</span></span>
    * <span data-ttu-id="211d1-132">Töölehe sisestamisel vabastatakse hankijale kuuluvad varud, kasutades viidet Omanikuvahetus.</span><span class="sxs-lookup"><span data-stu-id="211d1-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="211d1-133">Seejärel saadakse varud vabade varudena, kasutades laokannet, mida uuendatakse ostutellimuse toote sissetulekuga.</span><span class="sxs-lookup"><span data-stu-id="211d1-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="211d1-134">Pange tähele, et luuakse ainult sisestatud töölehega seotud kanded.</span><span class="sxs-lookup"><span data-stu-id="211d1-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="211d1-135">Ühtegi eeldatavat laokannet ei looda.</span><span class="sxs-lookup"><span data-stu-id="211d1-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="211d1-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="211d1-136">Click OK.</span></span>
3. <span data-ttu-id="211d1-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="211d1-137">Close the page.</span></span>

